# Court Insight

Windows용 농구 분석 프로그램의 배포 및 버전 업데이트 저장소입니다.

## 다운로드와 실행

[최신 버전 다운로드](https://github.com/kwut76511/court-insight/releases/latest)

1. Releases의 Assets에서 **CourtInsight-Windows-v1.1.0.zip**처럼 Windows ZIP 파일을 받습니다.
2. 압축을 풀고 CourtInsight.exe를 실행합니다. update-config.json은 실행 파일과 같은 폴더에 둡니다.
3. 기존 1.0 사용자는 실행 중인 앱을 닫고 1.1 패키지를 처음 한 번 설치해야 합니다. 기존 data 폴더를 유지하면 같은 Windows 계정에서 설정과 수집 기록을 계속 사용할 수 있습니다.

## 두 가지 업데이트

- **데이터 업데이트**: 선택한 리그의 경기와 선수 자료를 새로 수집합니다.
- **버전 업데이트**: 배포자가 새 버전을 Releases에 게시하면 다운로드, 서명·파일 검증, 프로그램 교체와 재시작을 진행합니다. 새 버전 시작에 실패하면 이전 버전으로 복구합니다. 프로그램 버전 업데이트에는 농구 API 키가 필요 없습니다.

실행 파일과 업데이트 설정은 쓰기 가능한 같은 폴더에 보관하세요. 개인 설정과 수집 자료는 로컬 data 폴더에 저장됩니다.

## API 키 설정

1. [API-Sports 대시보드](https://dashboard.api-football.com/)에 가입하고 이메일을 인증한 뒤 로그인합니다. 주소에 football이 있어도 API-Sports 공용 대시보드입니다.
2. **Account → My Access → API key**에서 키를 확인합니다.
3. 앱의 **연결 설정**에 키를 입력하고 저장합니다. 농구 상품은 **API-BASKETBALL**입니다.

각 사용자는 자신의 키를 사용합니다. 키를 이 저장소나 Issues에 올리지 마세요. API 키는 Windows 사용자 계정에 묶어 암호화해 로컬 저장합니다.

## 지원 리그와 현재 한계

선택 항목: CBA, NBA, KBL, B.LEAGUE PREMIER, 호주 NBL, EuroLeague, PBA.

KBL·NBA·NBL은 공개 데이터 연결을 사용합니다. CBA·B.LEAGUE PREMIER·EuroLeague·PBA는 API-Sports 키와 해당 대회·시즌에 대한 제공 범위 확인이 필요합니다. B.LEAGUE PREMIER 지원 여부와 전 선수의 직전 3시즌 기록·확정 선발·부상 정보는 완비되지 않았습니다. 키 등록만으로 누락 자료가 모두 해결되지는 않습니다.

자료가 충족되면 직전 3시즌 기록에 기본 60%·25%·15% 가중치를 적용합니다. 부족한 자료는 표시하며 예측 조건을 충족하지 못하면 계산을 보류합니다. 예측 모델의 실전 적중률은 검증되지 않았습니다.

[API-BASKETBALL 제공 범위와 요금](https://api-sports.io/sports/basketball)

CourtInsight.exe와 update.json은 자동 업데이트에 사용됩니다. 일반 사용자는 Windows ZIP 파일을 다운로드하세요.
