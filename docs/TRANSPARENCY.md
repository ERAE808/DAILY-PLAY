# 사용 기술·AI 활용·공개 범위

[처음으로](../README.md) · [변경 이력](CHANGELOG.md)

이 문서는 사용 기술과 공개 원칙을 설명합니다. 현재 제공 기능, 배포 버전, 향후 계획을 구분합니다.

## ChatGPT AI 활용

DAILY PLAY는 **ChatGPT AI를 활용하여 개발한 프로그램**입니다. 공개할 내용과 제품의 변경 방향은 개발자가 결정합니다. AI 활용 사실은 보안 인증이나 오류 없는 동작을 보장하는 표기가 아닙니다.

## 배포와 Velopack 사용 범위

Velopack은 과거 설치형 패키지의 제작과 설치 초기화·상태 확인에 사용했습니다. 현재 ZIP은 .NET 압축 라이브러리로 만들며, C# 앱이 GitHub Releases에서 공개 버전을 확인합니다. 사용자가 다운로드 페이지에서 새 ZIP을 받아 교체합니다.

## 2.8.0의 배포 구성

- Windows x64용으로 컴파일한 C# 앱과 자체 포함 .NET 10 데스크톱 런타임을 배포합니다. 앱은 PowerShell 없이 실행됩니다.
- 저장소에는 사용자용 문서, Releases에는 실행용 ZIP과 체크섬을 제공합니다.
- 동봉 런타임의 라이선스와 제3자 안내는 `app/assets/notices`에 있습니다. Windows SDK 구성요소에는 [Microsoft Windows SDK 이용 조건](https://learn.microsoft.com/en-us/legal/windows-sdk/license)이 적용됩니다. 게임 이름과 아이콘의 권리는 각 권리자에게 있습니다.

## PC에 저장하는 기록과 외부 통신

- ZIP용 기록과 설정은 `%LOCALAPPDATA%\DailyPlay.Folder.State`에 보관합니다.
- 화면인식은 기본 OFF입니다. 동의한 뒤 지원되는 화면을 PC에서 판독할 수 있습니다. 수동 수정과 자동 관리 복귀를 지원합니다.
- 일정 갱신은 공개 웹 자료를 사용하고, 버전 확인은 GitHub Releases API를 사용합니다. 사이트는 접속 과정에서 IP 주소와 접속 시각 등 통신 정보를 받을 수 있습니다.

실행 파일은 미서명입니다. 다운로드한 실행 파일에 Windows의 보안 경고가 표시될 수 있습니다. 실행 전에 배포 출처와 파일의 SHA-256을 확인하세요. 자세한 내용은 [사용 안내](USAGE.md)와 [개인정보·통신 안내](PRIVACY.md)에서 확인하세요.

제작자가 권리를 보유한 부분의 이용 조건은 [무료 배포·이용 안내](LICENSE-NOTICE.md)에 있습니다.
