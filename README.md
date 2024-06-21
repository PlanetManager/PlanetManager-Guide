# PlanetManager
**PlanetEarth - User Auto Auth System   
Developer : <a href="https://discord.com/users/894564302613254164" title="Kaga's Discord" target="_blank">KagaX0426</a>, <a href="https://discord.com/users/717219505562189885" title="Ruma's Discord" target="_blank">ridanit_ruma</a>, <a href="https://discord.com/users/781088270830141441" title="200mill's Discord" target="_blank">200mill</a>   
Discord : [Click here](https://discord.gg/NshmCh4ptY, "Link : PlanetManager Discord Server")   
WebSite : [Click here](https://planetmanager.inizeno.com, "Link : PlanetManager Introduce Site")**   
<br />
### ***Before Use This Service...***
> - PlanetManager는 플레닛어스 사용자라면 누구나 사용이 가능합니다.
> - 해당 서비스는 플레닛어스의 외부 디스코드 서버에서 유저들의 인증을 간편하게 하기 위해 개발되었습니다. 다른목적으로 사용하는것은 추천해 드리지 않습니다.
> - 본 Markdown 문서는 PlanetManager 디스코드 봇의 사용 방법을 기재하고 있습니다.
<br />

### ***User Guide***
#### 1. 디스코드 서버와 서비스의 연동
`/search [<Name> / All]`   
명령어를 입력한 디스코드 서버를 플레닛매니저와 연동합니다.
- `<Name>` : 마을 또는 국가 이름
  - 마을 또는 국가를 디스코드 서버와 연동합니다. 1계정 당 최대 2개의 서버를 연동할 수 있으며 시장, 또는 총리만 등록 가능 합니다.
- `<All>` : 모든 국가를 등록합니다
  - 주로 연맹 디스코드와 같은 대규모 집단에서 사용합니다. 이는 서비스 관리자의 허가를 받아야 연동할 수 있습니다.

`/unconnect [<Name> / (None)]`   
해당 디스코드 서버와 플레닛매니저를 연동 해제 합니다. 해당 디스코드 서버의 소유자만 실행할 수 있습니다.
- `<Name>` : 디스코드 서버 이름
  - 사용자가 선택한 디스코드 서버를 연동 해제 합니다.
- `<None>` : 아무런 값도 입력되어져 있지 않는 경우
  - 명령어가 입력된 디스코드 서버를 연동 해제 합니다. 만약 명령어가 입력된 곳이 길드가 아니거나 자신이 소유자가 아니라면 디스코드 서버 이름이 꼭 필요합니다.

`/serverlist`   
자신의 계정으로 연동된 디스코드 서버를 보여줍니다.   

#### 2. 역할 설정
`/setrole [Mayor / DeputyMayor / Citizen / External] [<Role>]`   
유저의 인게임 계급에 따라 어떤 역할을 부여할지 설정합니다.   
- `Mayor` : 유저가 시장일 경우
  - `<Role>` 역할을 지급합니다.
- `DeputyMayor` : 유저가 부시장일 경우
  - `<Role>` 역할을 지급합니다.
- `Citizen` : 유저가 시민일 경우
  - `<Role>` 역할을 지급합니다.
- `External` : 유저가 해당 디스코드에 등록된 국가 또는 마을과 전혀 연관이 없는 외부인일 경우
  - `<Role>` 역할을 지급합니다.

#### 3. 자동 역할 부여
`/autorole [On / Off / Write / Accept]`   
자동으로 유저에게 역할을 부여할 것인지 선택합니다.   
- `On` : On 일 경우
  - 자동으로 유저에게 역할을 부여합니다.
- `Off` : Off 일 경우
  - 자동으로 유저에게 역할을 부여하지 않습니다.
- `Write` : Write 일 경우
  - 유저가 마인크래프트 닉네임, 소속 국가, 소속 마을을 입력하면 내용이 일치한지 자동으로 확인하고 역할을 줍니다.
- `Accept` : Accept 일 경우
  - 유저가 관리자가 지정한 양식에 따라 입력한 경우 관리자에게 승인 요청 메시지가 발송되고, 관리자가 승인 시 역할을 자동으로 지급합니다.
  - 관리자가 autorole 항목을 Accept로 설정하려면, 명령어 입력후 나오는 양식 설정 페이지를 작성해야 합니다.
  - 양식을 수정하고 싶은 경우, 명령어를 한번 더 입력해 주시기 바랍니다.

##### 3.1. 자동 역할 부여 시스템
역할 중에 마을 이름이나 국가 이름 중 일치하는것이 있다면 해당 유저에게 그 역할을 자동으로 지급합니다.
해당 시스템은 위 `/autorole` 명령어로 끄고 켤 수 있습니다.   
   
예로들어 @Great_Canada 라는 역할이 있다면 인게임에서 Great_Canada 라는 국가가 있기 때문에 캐나다 소속 유저들은 모두 이 역할을 받게 됩니다.
마찬가지로 @Monument_Town 이라는 역할이 있다면 Monument Town 마을 소속 유저들은 모두 이 역할을 받게 됩니다.   
   
하지만 @캐나다 | Canada 와 같은 역할을 지급하고 싶은 경우에는 PlanetManager 디스코드 봇이 액세스 할 수 있는 채널에 설정 메시지를 올리고, 해당 메시지를 `/setproperties [<Channel>] [<MessageId>]`를 통해 불러와야 합니다. (한번 불러온 이후로는 불러오지 않아도 됩니다. 만약 메시지의 위치가 바뀐 경우, 다시 불러와야 합니다.)   
   
메시지의 형식은 다음과 같습니다.
```json
{
  "마을이나 국가의 UUID" : {"@something", "CustomName"},
  "마을이나 국가의 UUID" : {"@something", "CustomName"}
}
```
1. 중괄호 필수
2. 문자열 형식(쌍따옴표 두개 권유)으로 작성할것
3. Key에는 마을이나 국가의 UUID, Value에는 쌍따옴표로 감싸진 역할 멘션 형식으로 작성할것
4. 1개 이상일때는 마지막 항목을 제외한 모든 항목의 뒤에 콤마(,)를 붙일것.
   
위 규칙은 json 파일의 기본적인 규칙이므로, 만약 이를 어길시 디스코드 봇은 json 파일 형식 변환중 오류가 발생했음을 당사자에게 알립니다.   
   
해당 메시지를 속성으로 추가하시면, 이제 여러분만의 역할을 설정하여 유저들에게 자동으로 지급할 수 있는 시스템이 완성됩니다!   
   
`CustomName` 항목은 Great_Canada를 캐나다 로 줄인것과 같이 우리가 평소에 부르는 마을 또는 국가의 이름을 적어주시면 됩니다.
이는 {Town}과 {Nation} (서비스에서 사용할 수 있는)변수를 설정합니다.   
Value의 둘중 한 한목이나 두 항목 다 공란("")으로 두셔도 상관 없습니다.

#### 4. 유저 닉네임 편집
`/setTitle [<String>]`
유저의 이름 앞에 들어갈 문자열을 설정합니다. 문자열의 마지막에 공란은 자동으로 들어갑니다.   
- <String> : 문자열
  - 이 항목에 Planet 를 입력하면 Planet ridanit_ruma 로 유저의 닉네임이 자동으로 수정됩니다.

`/setSurname [<String>]`
유저의 이름 뒤에 들어갈 문자열을 설정합니다. 문자열의 맨 앞에 공란은 자동으로 들어갑니다.   
- <String> : 문자열
  - 이 항목에 User 를 입력하면 ridanit_ruma User 로 유저의 닉네임이 자동으로 수정됩니다.

**위 두 명령어는 함께 사용이 가능합니다. 또한 {Town} 또는 {Nation}으로 유저의 마을 이름, 국가 이름을 넣을 수 있습니다.(관련 문서는 [여기](#31-자동-역할-부여-시스템, "자동 역할 부여 시스템")를 참조)**

#### 5. 인증 성공시 유저에게 보내는 메시지
`/sendmessage [Mayor / DeputyMayor / Citizen / External] [<Message>]`
인증을 성공하면 해당하는 유저에게 지정된 메시지를 보냅니다.
- `Mayor` : 유저가 시장일 경우
  - `<Message>` 를 전송합니다.
- `DeputyMayor` : 유저가 부시장일 경우
  - `<Message>` 를 전송합니다.
- `Citizen` : 유저가 시민일 경우
  - `<Message>` 를 전송합니다.
- `External` : 유저가 해당 디스코드에 등록된 국가 또는 마을과 전혀 연관이 없는 외부인일 경우
  - `<Message>` 를 전송합니다.
**Message 란에 {Town}과 {Nation}을 사용할 수 있습니다. (관련 문서는 [여기](#31-자동-역할-부여-시스템, "자동 역할 부여 시스템")를 참조)**   
   
**지금까지 PlanetManager 서비스 유저 가이드였습니다. 앞으로도 더욱 편리한 플레닛어스 생활 즐기시기 바랍니다. 감사합니다.**
> 본 카가와 이백밀, 그리고 루마로 이루어진 팀은 플레닛어스 외부 팀 입니다.
> 위 서비스는 플레닛어스를 즐기는 모든 사람들이 이용할 수 있습니다.
> 이 서비스가 여러분들에게 도움이 될 수 있도록 항상 노력하겠습니다.
> 원하는 기능이 있다면 [디스코드 서버](https://discord.gg/NshmCh4ptY, "Link : PlanetManager Discord Server")에 방문하셔서 의견을 서로 공유하실 수 있습니다.

with Kaga, 200mill, and ruma.
