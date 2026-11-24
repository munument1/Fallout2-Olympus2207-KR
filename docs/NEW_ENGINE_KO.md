# Olympus 2207 독립형 한국어 텍스트 엔진 설치 안내

**한국어 출력 엔진 v1.2.5 이상이 필요합니다.** Steam을 포함한 기존 설치 폴더를 지정할 수 있습니다.

## Nexus에서 ZIP 하나로 설치

[Nexus 한글 패치 ZIP](https://www.nexusmods.com/fallout2/mods/191?tab=files)을 **olympus.exe가 있는 Olympus 2207 1.2a 폴더**에 풀고 **olympus.exe**를 실행하세요. ZIP에는 이 방식에 필요한 번역과 한국어 출력 파일이 함께 들어 있습니다. 구형 패치로 실행 파일이 바뀌었다면 먼저 원본으로 복구하세요.

## GitHub 번역 ZIP으로 설치

1. Olympus 2207 **1.2 원본 및 1.2a 패치**를 설치하고 게임을 종료합니다.
2. [한국어 번역 데이터 ZIP](https://github.com/munument1/Fallout2-Olympus2207-KR/releases/download/v2026.10.17-native-beta.1/Fallout2-Olympus2207-KR-native-beta-data.zip)을 **olympus.exe가 있는 폴더**에 풉니다.
3. [한국어 출력 엔진 v1.2.5](https://github.com/munument1/Fallout2-Korean-Text-Engine/releases/tag/v1.2.5)의 **Fallout2-Korean-Native-Setup.exe**를 실행해 같은 폴더를 지정합니다. 설치기가 한국어 설정을 적용합니다.
4. **olympus.exe** 또는 기존 모드 런처로 실행합니다.

Olympus에 포함된 **Extended sfall 4.2.6**과 고해상도 패치 구성을 사용하세요. 설치기는 기존 sfall을 유지하고 새 실행 파일의 CRC를 등록합니다.

## 구형 한패나 이전 엔진에서 업데이트

- 구형 **KR1.1**을 적용했다면 원본 **olympus.exe**, **ddraw.dll**, **ddraw.ini**와 고해상도 패치 구성을 복구한 뒤 위 순서대로 설치하세요. 원본을 별도 폴더에 새로 설치해 적용할 수도 있습니다.
- 이전 독립형 엔진을 설치했다면 설치기의 **복구** 기능을 먼저 실행하고 v1.2.5를 적용하세요.

## 확인 범위

Olympus 2207 1.2a에서 메인 메뉴, 캐릭터 선택, 첫 대화와 시작 튜토리얼 안내창 두 개를 확인했습니다. 긴 안내문도 여러 줄로 표시됩니다.

## 파일 보존과 복구

- 번역 ZIP은 게임 스크립트, EXE, sfall DLL 및 전체 CFG를 덮어쓰지 않습니다.
- 기존 모드에 포함된 sfall을 버전 확인 없이 일반 최신판으로 교체하지 않습니다. 독립형 엔진은 기존 DLL을 유지하고 필요한 ExtraCRC만 설정에 추가합니다.
- 설치기는 전체 게임을 복제하지 않고 수정 대상 원본 파일만 korean_engine_backup_v2에 저장합니다. 바이너리 EXE를 변경하므로 최소 원본 파일 복구 기록은 유지합니다.
- 사용자가 별도로 교체한 sfall DLL은 엔진 자체의 --restore로 돌아오지 않습니다. 그런 변경은 별도의 원본 DLL 보관이 필요합니다.
- 기존 번역 내용과 CP949 텍스트는 다시 번역하거나 일괄 치환하지 않습니다. UTF-8로 저장된 일부 파일은 ZIP 빌드 시 손실 없는 CP949 변환을 수행합니다.

[구형 설치 방식 보관본](LEGACY_INSTALLATION_KO.md)
