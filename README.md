# DAILY PLAY · 데일리플레이

혼자 사용하려고 만들었는데 생각보다 괜찮아서 배포합니다.

여러 게임의 일일·주간 할 일과 이벤트 일정을 관리하는 Windows 데스크톱 프로그램입니다.

 **ChatGPT AI를 활용하여 개발했습니다.**


**[DAILY PLAY 2.7.9 정식 릴리스](https://github.com/ERAE808/DAILY-PLAY/releases/tag/v2.7.9)** · **[ZIP 다운로드](https://github.com/ERAE808/DAILY-PLAY/releases/download/v2.7.9/DAILY-PLAY-2.7.9.zip)** · [SHA-256 파일](https://github.com/ERAE808/DAILY-PLAY/releases/download/v2.7.9/DAILY-PLAY-2.7.9.zip.sha256)

[사용 안내](docs/USAGE.md) · [개인정보·통신 안내](docs/PRIVACY.md) · [1.0~2.7.9 변경 이력](docs/CHANGELOG.md) · [기술·공개 범위 안내](docs/TRANSPARENCY.md)

## 다운로드

현재 공개 파일은 **2.7.9 · `DAILY-PLAY-2.7.9.zip`**입니다. ZIP 전체를 쓰기 가능한 로컬 폴더에 풀고 `DailyPlay-Folder.exe`를 실행하세요. `app`과 `runtime` 폴더는 실행 파일 옆에 그대로 둡니다.

ZIP 크기는 101,187,556 바이트이며 SHA-256은 `124F5909831AEAFA728070B6C6BE3ED5C1876A0EEF4217E36971C39CDBE062C9`입니다. 기록은 `%LOCALAPPDATA%\DailyPlay.Folder.State`에 별도로 저장됩니다. 같은 Windows 계정에서 이전 ZIP 앱을 종료한 뒤 새 폴더의 2.7.9를 실행하면 이 위치의 기록을 사용합니다.

Releases의 **Assets**에서 `DAILY-PLAY-2.7.9.zip`을 선택하세요. GitHub가 자동으로 제공하는 `Source code (zip/tar.gz)`는 저장소 자료의 압축이며 이 버전의 실행용 패키지가 아닙니다.

## 주요 기능

| 기능 | 설명 |
|---|---|
| 미니바·알림판 | 게임별 진행 상황, 일일·주간·특별퀘스트 확인 |
| 수동 조작 | 완료 체크·해제, 수치·일정 수정, 자동 관리 복귀 |
| 달력 | 일정과 마감 확인 |
| 온라인 갱신 | 공개 일정·공지 조회 및 출처 확인 |
| 화면인식 | 동의 후 지원 게임 화면의 진행도 판독 |
| 설정 | 표시·테마·자동실행·갱신·화면인식 설정 |

대상 게임은 명조, 명일방주: 엔드필드, 젠레스 존 제로, 소녀전선2: 망명, 트릭컬 리바이브, 붕괴: 스타레일입니다. 정식 화면인식은 젠레스 존 제로, 소녀전선2: 망명, 명일방주: 엔드필드, 명조: 워더링 웨이브의 지원 화면과 항목에 적용됩니다. 화면인식은 동의 후 켤 수 있으며 기본값은 OFF입니다. 스타레일은 체크리스트와 일정 갱신을 지원합니다.

화면인식은 게임별 공식클라이언트에서 작동합니다.

## 사용 기술과 AI 활용

ChatGPT AI를 활용해 개발했으며 C# 실행 호스트와 WPF, 내장 .NET 10·PowerShell 7을 사용합니다.

Velopack은 이전 설치형 패키지의 제작과 설치 초기화·상태 확인에 사용했습니다. 2.7.9 폴더형 ZIP의 Velopack 사용 범위는 없습니다. 앱은 GitHub Releases에서 새 버전을 확인하고 다운로드 페이지를 안내합니다. 사용자가 새 ZIP을 내려받아 전환합니다.

## 개발환경과 실행환경

배포 대상은 Windows x64입니다. .NET Desktop Runtime 10.0.15와 PowerShell 7.6.10은 ZIP에 포함됩니다. 한국어 화면인식에는 Windows 한국어 OCR 기능이 필요합니다. 개발에는 Windows 11 25H2 x64(빌드 26200.9974), .NET SDK 10.0.403, C# 및 WPF를 사용했습니다. 폴더형 ZIP은 .NET 압축 라이브러리로 만들었습니다.

실행 파일과 앱 스크립트는 미서명입니다. 다운로드 출처가 표시된 ZIP을 Windows 파일 탐색기로 풀면 출처 표식이 스크립트에도 붙을 수 있습니다. 이 표식이 붙은 미서명 스크립트는 2.7.9의 PowerShell 실행 정책에 따라 시작 시 차단됩니다. [실행 문제 해결](docs/USAGE.md#실행-문제-해결)

## 향후 개발 방향

아래 항목은 향후 계획이며 일정은 미정입니다.

- 기반언어 C#으로 변경 및 PowerShell 의존도 삭제
- Velopack을 이용한 앱 내 자체 업데이트 추가
- 화면인식 사용 가능한 4개 게임의 화면인식 지원 항목 확대
- 원신, 블루아카이브 자동 일정갱신 추가.
- 보안 서명 적용 또는 Microsoft Store를 통한 배포 방식 강화 준비

## 투명성과 공개 범위

ZIP에는 앱 실행용 PowerShell 원문 76개와 번들 PowerShell 모듈이 포함됩니다. 동봉 런타임의 라이선스는 `runtime/notices`에서 확인할 수 있습니다. 게임 아이콘은 각 권리자에게 권리가 있습니다.

현재 및 향후 릴리스는 GitHub에서 무료로 배포합니다. 제작자가 권리를 보유한 부분의 CC BY-NC-SA 4.0 및 제3자 자료에 대한 조건은 [무료 배포·이용 안내](docs/LICENSE-NOTICE.md), 실제 공개 범위는 [기술·공개 범위 안내](docs/TRANSPARENCY.md)를 확인하세요.

## 문제 제보

[GitHub Issues](https://github.com/ERAE808/DAILY-PLAY/issues)에 앱 버전, Windows 버전, 재현 순서, 기대한 동작과 실제 동작을 적어 주세요. 원본 기록 폴더·계정 정보·UID·개인정보가 보이는 게임 화면은 올리지 마세요.
