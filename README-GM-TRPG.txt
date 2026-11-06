GM-TRPG 설치 안내

포함 파일
- gm-trpg.html: 온라인 TRPG 웹앱
- firebase-database.rules.json: Firebase Realtime Database 보안 규칙

중요: 기존 Firebase 프로젝트 ID와 Database URL은 앱에 미리 입력되어 있습니다. 하지만 Database URL만으로 Firebase 웹 앱의 apiKey와 appId를 알아낼 수는 없습니다. 따라서 최초 1회 웹 앱 설정 JSON을 붙여 넣어야 하며, 저장 후에는 해당 기기에서 자동 연결됩니다. 이 설정값은 Firebase Console의 프로젝트 설정 > 내 앱 > SDK 설정 및 구성에서 확인할 수 있습니다.

Firebase 준비
1. Firebase Console에서 프로젝트 gm-trpg-d3974를 엽니다.
2. Authentication > Sign-in method에서 익명(Anonymous) 로그인을 사용 설정합니다.
3. Realtime Database > Rules에서 firebase-database.rules.json 내용을 붙여 넣고 게시합니다.
4. 웹 앱 설정 JSON을 gm-trpg.html의 온라인 연결 준비 칸에 붙여 넣고 저장합니다.
5. GitHub 저장소의 기존 gm-trpg.html을 이 파일로 교체하고 커밋합니다.

주의
- 익명 로그인과 보안 규칙이 설정되지 않으면 방 생성/참가가 실패합니다.
- 비밀 정보는 GM과 지정된 플레이어만 읽도록 별도 경로와 규칙으로 분리했습니다.
- 이 버전은 세션용 기본 기능(방, 장면, 행동, 주사위, 캐릭터, 비밀 정보, 기록)을 구현한 첫 완성본이며, 실제 멀티기기 테스트가 필요합니다.
