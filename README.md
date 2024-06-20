# PlanetManager
**PlanetEarth - User Auto Auth System   
Maker : KagaX0426, ridanit_ruma, 200mill**   
<br />
### ***Before Use This Service...***
> - PlanetManager는 플레닛어스 사용자라면 누구나 사용이 가능합니다.
> - 해당 서비스는 플레닛어스의 외부 디스코드 서버에서 유저들의 인증을 간편하게 하기 위해 개발되었습니다. 다른목적으로 사용하는것은 추천해 드리지 않습니다.
> - 본 Markdown 문서는 PlanetManager 디스코드 봇의 사용 방법을 기재하고 있습니다.
<br />

### ***User Guide***
#### 디스코드 서버와 서비스의 연동
`/search [<Name> / <All>]`
명령어를 입력한 디스코드 서버를 플레닛매니저와 연동합니다.
- `<Name>` : 마을 또는 국가 이름
  - 마을 또는 국가를 디스코드 서버와 연동합니다. 1계정 당 최대 2개의 서버를 연동할 수 있으며 시장, 또는 총리만 등록 가능 합니다.
- `<All>` : 모든 국가를 등록합니다
  - 주로 연맹 디스코드와 같은 대규모 집단에서 사용합니다. 이는 서비스 관리자의 허가를 받아야 연동할 수 있습니다.

`/unconnect [<Name> / <None>]`
해당 디스코드 서버와 플레닛매니저를 연동 해제 합니다. 해당 디스코드 서버의 소유자만 실행할 수 있습니다.
- `<Name>` : 디스코드 서버 이름
  - 사용자가 선택한 디스코드 서버를 연동 해제 합니다.
- `<None>` : 아무런 값도 입력되어져 있지 않는 경우
  - 명령어가 입력된 디스코드 서버를 연동 해제 합니다. 만약 명령어가 입력된 곳이 길드가 아니거나 자신이 소유자가 아니라면 디스코드 서버 이름이 꼭 필요합니다.

#### 유저가 디스코드 서버에 참가 했을때

