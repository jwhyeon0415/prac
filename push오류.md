# 소스트리에서 push 오류

컴퓨터에서는 잘 작동하는 노트북에서는 안 됨<br>
<br>
git 특강 중 sourcetree에서 push를 과정에서 문제가 발생<br>
<br>
commit까진 다 되는데 push를 하려 하면 푸시할 브랜치 목록에 아무것도 띄지 않음..<br>
Push 버튼을 눌러도 아무 반응 없음<br>
<br>
(터미널에서 Git을 통해 강제 푸시는 가능했음)<br>
(Pull, Commit은 가능했음)<br>
(중간중간에 계속 Pull, Commit 해봄)<br>
<br>
온갖 방법을 다 해봤는데 해결되지 않음<br>
- 도구 -> 옵션 -> Git -> Git 버전 -> System (검색하보니 버전을 업그레이드 하는 것이라 나와있는데 System 버튼이 활성화되어 있지 않았음)
- 도구 -> 옵션 -> Git -> 브랜치 푸시를 '간단'에서 '업스트림'으로 변경
- 도구 -> 옵션 -> 인증 -> 계정 편집/추가
- 설정 -> 원격 -> 경로 -> 주소에서 github.com 앞에 token 추가
- 설정 -> 원격 -> 경로 -> 주소에서 github.com 앞에 'token@' 추가
- 설정 -> 원격 -> 경로 -> 주소에서 github.com 앞에 token@ 추가
- git, souretree 제거 후 다시 다운로드
- 설정 -> 원격 -> 설정 파일 편집... -> 메모장에서 연 후 검색 결과와 내용 비교 -> 동일...
- 다시 git, souretree 관련 폴더까지 모두 제거 후 다시 다운로드
- 도구 -> 옵션 -> Git -> Git 버전 -> Embedded<br>
=> 와 드디어 뜬다
<br>
- 푸시 목록이 나타나고 드디어 됨....
<br>
- 근데 CredentialHelperSelector 창이 떠서 뭐가 잘못될까봐 검색
- Windows PowerShell에서 'cd$env:LOCALDATA\Atlassian\SourceTree\git_local\mingw32\bin\' 치라는데 경로를 찾을 수가 없어서 그냥 원래 체크되어 있던 'manager-core'로 선택<br>
-> github token 사용해서 인증 후 push 성공
<br>
- 저 창이 push할 때마다 계속 뜸 -> Always use this from now on 체크
<br>
-> 확인용 내용