# GM-TRPG

스마트폰 브라우저에서 사용하는 6인 온라인 TRPG 웹앱입니다.

## 포함 기능
- GM 1명 + 플레이어 최대 5명 (방 전체 최대 6명)
- 6자리 방 코드 생성 및 참가
- Firebase Realtime Database 실시간 동기화
- 자유 행동 선언 및 테이블 장면 공개
- D4 / D6 / D8 / D10 / D12 / D20 / D100
- 캐릭터 능력치, HP, 소지품, 상태 기록
- GM 전용 메모 및 플레이어별 비밀 메시지
- 세션 기록
- 모바일 반응형 화면

## 1. Firebase 준비 (최초 1회)
1. https://console.firebase.google.com/ 에서 프로젝트를 생성합니다.
2. 프로젝트 설정 > 내 앱 > 웹 앱을 추가하고 Firebase 설정값을 확인합니다.
3. Authentication > Sign-in method에서 **익명(Anonymous)** 로그인을 활성화합니다.
4. Realtime Database를 생성합니다.
5. Realtime Database > Rules에 `firebase-database.rules.json` 내용을 붙여넣고 게시합니다.
6. 웹 앱의 API Key, Project ID, Database URL, App ID를 웹앱 연결 화면에 입력합니다.

> Firebase 웹 설정의 API Key는 웹 앱 식별용 공개 설정값입니다. 서비스 계정 키나 비공개 서버 키는 절대 입력하거나 GitHub에 올리지 마세요.

## 2. GitHub에 업로드
1. 저장소 https://github.com/GOGUMA5560/GM-TRPG 를 엽니다.
2. Add file > Upload files를 누릅니다.
3. 이 폴더의 `index.html`, `firebase-database.rules.json`, `README.md`를 업로드합니다.
4. Commit changes를 누릅니다.

## 3. GitHub Pages 배포
1. 저장소의 Settings > Pages로 이동합니다.
2. Build and deployment의 Source를 **Deploy from a branch**로 선택합니다.
3. Branch를 `main`, 폴더를 `/ (root)`로 선택하고 Save를 누릅니다.
4. 잠시 후 `https://goguma5560.github.io/GM-TRPG/` 에서 접속합니다.

## 4. 플레이
1. 각 기기에서 배포 주소를 엽니다.
2. 각 기기에서 같은 Firebase 설정값으로 연결합니다.
3. GM이 이름을 입력하고 새 방 만들기를 누릅니다.
4. GM이 방 코드를 공유합니다.
5. 플레이어가 이름과 방 코드를 입력해 참가합니다.

## 보안 및 현재 한계
- 이 버전은 빠르게 실제 멀티기기 테스트를 할 수 있는 초기 MVP입니다.
- Firebase 규칙은 방 참가자별 데이터 접근을 제한하지만, 게임 내 GM/플레이어 역할은 클라이언트에서 지정하는 구조이므로 공개 서비스 전에는 서버 측 역할 검증을 추가해야 합니다.
- 방 코드는 초대받은 사람에게만 공유하세요.
- 익명 계정은 브라우저 데이터 삭제/기기 변경 시 새 UID가 될 수 있습니다. 재접속·계정 연동은 후속 개발 대상입니다.
- 무료 Firebase 사용량에는 한도가 있으며, 사용량과 요금 정책을 확인하세요.
