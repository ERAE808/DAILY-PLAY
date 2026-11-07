# DAILY PLAY · 데일리플레이

혼자 사용하려고 만들었는데 생각보다 나쁘지않아 혼자쓰기 아쉬워서 배포합니다.

여러 게임의 일일·주간 할 일과 이벤트 일정을 관리하는 Windows 데스크톱 프로그램입니다.

 **ChatGPT AI를 활용하여 개발했습니다.**


**[DAILY PLAY 2.7.6 정식 릴리스](https://github.com/ERAE808/DAILY-PLAY/releases/tag/v2.7.6)** · **[ZIP 다운로드](https://github.com/ERAE808/DAILY-PLAY/releases/download/v2.7.6/DAILY-PLAY-2.7.6.zip)** · [SHA-256 파일](https://github.com/ERAE808/DAILY-PLAY/releases/download/v2.7.6/DAILY-PLAY-2.7.6.zip.sha256)

[사용 안내](docs/USAGE.md) · [개인정보·통신 안내](docs/PRIVACY.md) · [1.0~2.7.6 변경 이력](docs/CHANGELOG.md) · [기술·공개 범위 안내](docs/TRANSPARENCY.md)

## 다운로드

현재 공개 파일은 **2.7.6 · `DAILY-PLAY-2.7.6.zip`**입니다. ZIP 전체를 쓰기 가능한 로컬 폴더에 풀고 `DailyPlay-Folder.exe`를 실행하세요. `app` 폴더는 실행 파일 옆에 그대로 둡니다.

ZIP 크기는 514,802 bytes이며 SHA-256은 `851AC0E317C9A55625510CD62E01561584DDDBE797FBCDCD0DB3E6B01EBFFE5A`입니다. 기록은 `%LOCALAPPDATA%\DailyPlay.Folder.State`에 별도로 저장됩니다. 기존 2.6 기록을 자동으로 가져오거나 합치지 않습니다.

Releases의 **Assets**에서 `DAILY-PLAY-2.7.6.zip`을 선택하세요. GitHub가 자동으로 제공하는 `Source code (zip/tar.gz)`는 저장소 자료의 압축이며 이 버전의 실행용 패키지가 아닙니다.

## 주요 기능

| 기능 | 설명 |
|---|---|
| 미니바·알림판 | 게임별 진행 상황, 일일·주간·특별퀘스트 확인 |
| 수동 조작 | 완료 체크·해제, 수치·일정 수정, 자동 관리 복귀 |
| 달력 | 일정과 마감 확인 |
| 온라인 갱신 | 공개 일정·공지 조회 및 출처 확인 |
| 화면인식 | 동의 후 지원 게임 화면의 진행도 판독 |
| 설정 | 표시·테마·자동실행·갱신·화면인식 설정 |

대상 게임은 명조, 명일방주: 엔드필드, 젠레스 존 제로, 소녀전선2: 망명, 트릭컬 리바이브입니다. 현재 정식 화면인식 자동반영 대상은 **젠레스 존 제로·소녀전선2: 망명**이며 지원 화면과 항목에 한정됩니다. 화면인식은 기본 OFF입니다.

## 사용 기술과 AI 활용

- ChatGPT AI를 활용해 개발했습니다. AI 활용 사실이 모든 동작의 정확성이나 보안 인증을 의미하지는 않습니다.
- 현재 구현은 Windows PowerShell·WPF·.NET Framework와 C# 실행 호스트를 사용합니다.
- **Velopack은 이전 설치형 패키지 제작과 설치 초기화·상태 확인에 사용했습니다. 2.7.6 폴더형 ZIP은 Velopack을 포함하거나 실행하지 않으며 ZIP 압축에도 사용하지 않습니다.**
- 2.7.6의 새 버전 안내는 앱이 GitHub Releases를 조회해 다운로드 페이지를 여는 기능입니다. 앱 내 자동 다운로드·업데이트 적용은 향후 개발 항목입니다.

## 개발환경과 실행환경

개발환경은 Windows 11 25H2 x64(빌드 26200.9711), Windows PowerShell 5.1.26100.9711, .NET Framework 4.8.1입니다. C# 실행 호스트 빌드에는 .NET Framework C# 컴파일러를 사용하며 ZIP은 .NET 압축 라이브러리로 생성합니다.

2.7.6 폴더형 구성의 실행 요구사항은 Windows x64, Windows PowerShell 5.1, .NET Framework 4.7.2 이상입니다. 개발환경 정보가 모든 Windows 버전·PC에서의 지원을 보장하지는 않습니다. 실행 파일과 PowerShell 스크립트는 미서명입니다. 인터넷 출처 표식이 남은 스크립트는 실행 정책에 따라 차단될 수 있으며, 해당 조건의 실제 실행과 온라인 평판은 확인되지 않았습니다.

## 향후 개발 방향

다음은 계획이며 현재 제공 기능이나 출시 일정의 확정 안내가 아닙니다.

- 기반 언어를 C#으로 점진적으로 교체
- .NET 10으로 전환
- Velopack을 이용한 앱 내 자체 업데이트 추가
- 명조·명일방주: 엔드필드 화면인식 추가
- 현재 5개 게임 외 추가 게임의 일정 갱신, 화면인식 지원 확대
- 보안 서명 적용 또는 Microsoft Store를 통한 배포 방식 강화 준비

전환 과정에서도 기존 기록·설정과 수동 조작을 보존하고, 업데이트 여부와 시점을 사용자가 선택하도록 준비합니다.

## 투명성과 공개 범위

변경 이력, 사용 기술·AI 활용, 실행 요구사항, 정보 처리·외부 통신, 알려진 제한과 사용자용 개발 방향을 안내합니다. **2.7.6 ZIP에는 앱 실행에 필요한 PowerShell 스크립트가 원문으로 포함됩니다.** 별도 개발 원본 전체·개발 도구·개인정보·인증정보·내부 작업 자료는 공개하지 않습니다.

현재 및 향후 릴리스는 GitHub에서 무료로 배포합니다. 제작자가 권리를 보유한 부분의 CC BY-NC-SA 4.0 및 제3자 자료에 대한 조건은 [무료 배포·이용 안내](docs/LICENSE-NOTICE.md), 실제 공개 범위는 [기술·공개 범위 안내](docs/TRANSPARENCY.md)를 확인하세요.

## 문제 제보

[GitHub Issues](https://github.com/ERAE808/DAILY-PLAY/issues)에 앱 버전, Windows 버전, 재현 순서, 기대한 동작과 실제 동작을 적어 주세요. 원본 기록 폴더·계정 정보·UID·개인정보가 보이는 게임 화면은 올리지 마세요.
