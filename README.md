# DAILY PLAY · 데일리플레이

혼자 사용하려고 만들었는데 생각보다 괜찮아서 배포합니다.

여러 게임의 일일·주간 할 일과 이벤트 일정을 관리하는 Windows 데스크톱 프로그램입니다.

 **ChatGPT AI를 활용하여 개발했습니다.**

**[DAILY PLAY 2.8.0 정식 릴리스](https://github.com/ERAE808/DAILY-PLAY/releases/tag/v2.8.0)** · **[ZIP 다운로드](https://github.com/ERAE808/DAILY-PLAY/releases/download/v2.8.0/DAILY-PLAY-2.8.0.zip)** · [SHA-256 파일](https://github.com/ERAE808/DAILY-PLAY/releases/download/v2.8.0/DAILY-PLAY-2.8.0.zip.sha256)

[사용 안내](docs/USAGE.md) · [개인정보·통신 안내](docs/PRIVACY.md) · [1.0~2.8.0 변경 이력](docs/CHANGELOG.md) · [기술·공개 범위 안내](docs/TRANSPARENCY.md)

## 다운로드

Releases의 **Assets**에서 `DAILY-PLAY-2.8.0.zip`을 내려받고 SHA-256을 확인하세요. ZIP 크기는 80,795,311바이트이며 SHA-256은 `A1682B842583C8E81233E76C91EA8A1D9464464DE904A5EC179811F665CBEB86`입니다.

ZIP 전체를 쓰기 가능한 로컬 폴더에 풀고 `DailyPlay-Folder.exe`를 실행하세요. `app`과 `runtime` 폴더는 실행 파일 옆에 함께 둡니다. 기록은 `%LOCALAPPDATA%\DailyPlay.Folder.State`에 저장됩니다. 같은 Windows 계정에서 이전 폴더판을 종료한 뒤 새 폴더판을 열면 기존 기록을 사용합니다.

GitHub가 자동으로 제공하는 `Source code (zip/tar.gz)`에는 이 저장소의 문서가 들어 있습니다. 앱은 **Assets**의 `DAILY-PLAY-2.8.0.zip`으로 실행하세요.

## 주요 기능

| 기능 | 설명 |
|---|---|
| 미니바·알림판 | 게임별 진행 상황, 일일·주간·특별퀘스트 확인 |
| 수동 조작 | 완료 체크·해제, 수치·일정 수정, 자동 관리 복귀 |
| 달력 | 일정과 마감 확인 |
| 온라인 갱신 | 공개 일정·공지 조회 및 출처 확인 |
| 화면인식 | 동의 후 지원 게임 화면의 진행도 판독 |
| 설정 | 표시·테마·자동실행·갱신·화면인식 설정 |

대상 게임은 명조, 명일방주: 엔드필드, 젠레스 존 제로, 소녀전선2: 망명, 트릭컬 리바이브, 붕괴: 스타레일, 원신입니다. 정식 화면인식은 젠레스 존 제로, 소녀전선2: 망명, 명일방주: 엔드필드, 명조: 워더링 웨이브의 지원 화면과 항목에 적용됩니다. 화면인식은 동의 후 켤 수 있으며 기본값은 OFF입니다. 스타레일과 원신은 체크리스트와 일정 갱신을 지원합니다.

화면인식은 각 게임의 공식 클라이언트에서 지원되는 화면에 적용됩니다.

## 사용 기술과 AI 활용

ChatGPT AI를 활용해 개발했습니다. C#과 WPF로 동작하며 .NET 10 데스크톱 런타임을 함께 제공합니다. 앱의 실행과 기능에 PowerShell 설치가 필요하지 않습니다.

Velopack은 과거 설치형 패키지의 제작과 설치 초기화·상태 확인에 사용했습니다. 현재 ZIP은 .NET 압축 라이브러리로 만들며, C# 앱이 GitHub Releases에서 공개 버전을 확인합니다. 사용자가 다운로드 페이지에서 새 ZIP을 받아 교체합니다.

## 개발환경과 실행환경

배포 대상은 Windows x64입니다. ZIP에 .NET Desktop Runtime 10.0.15가 들어 있습니다. 한국어 화면인식에는 Windows 한국어 OCR 기능이 필요합니다. 개발에는 Windows 11 25H2 x64(빌드 26200.9974), .NET SDK 10.0.403, C# 및 WPF를 사용했습니다.

실행 파일은 미서명입니다. 다운로드한 실행 파일에 Windows의 보안 경고가 표시될 수 있습니다. 실행 전에 배포 출처와 파일의 SHA-256을 확인하세요. [실행 문제 해결](docs/USAGE.md#실행-문제-해결)

## 향후 개발 방향

아래 항목은 향후 계획이며 일정은 미정입니다.

- Velopack을 이용한 앱 내 자체 업데이트 추가
- 화면인식 사용 가능한 4개 게임의 화면인식 지원 항목 확대
- 블루아카이브 자동 일정갱신 추가.
- 보안 서명 적용 또는 Microsoft Store를 통한 배포 방식 강화 준비

## 투명성과 공개 범위

동봉 런타임의 라이선스와 제3자 안내는 `app/assets/notices`에 있습니다. Windows SDK 구성요소에는 [Microsoft Windows SDK 이용 조건](https://learn.microsoft.com/en-us/legal/windows-sdk/license)이 적용됩니다. 게임 이름과 아이콘의 권리는 각 권리자에게 있습니다.

현재 및 향후 릴리스는 GitHub에서 무료로 배포합니다. 제작자가 권리를 보유한 부분의 CC BY-NC-SA 4.0과 제3자 자료에 대한 조건은 [무료 배포·이용 안내](docs/LICENSE-NOTICE.md)에서 확인하세요.

## 문제 제보

[GitHub Issues](https://github.com/ERAE808/DAILY-PLAY/issues)에 앱 버전, Windows 버전, 재현 순서, 기대한 동작과 실제 동작을 적어 주세요. 원본 기록 폴더·계정 정보·UID·개인정보가 보이는 게임 화면은 올리지 마세요.
