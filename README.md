# 올림푸스 2207 한국어 번역

이 저장소는 한국어 번역 데이터를 배포합니다. 한국어 출력에는 **엔진 v1.2.5 이상**이 필요합니다.

## 설치

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

[자세한 설치 및 복구 안내](docs/NEW_ENGINE_KO.md) · [구형 설치 방식 기록](docs/LEGACY_INSTALLATION_KO.md)

## 번역 파일과 패키지

기존 MSG의 `{ID}{음성}{본문}` 구조와 번역을 유지한다. CP949 파일을 일괄 재변환하지 않는다. UTF-8 한국어 텍스트가 있으면 클래식 ZIP 생성 시에만 CP949로 엄격 변환한다. 표현할 수 없는 문자는 `?`로 바꾸지 않고 빌드를 중단한다. 원본 파일은 변경하지 않는다.

```shell
python tools/build_translation.py --output dist/korean-classic-data.zip
```

패키지에 포함한 파일 해시와 변환 목록은 `translation-manifest.json`에 들어간다. RPU의 mods 내 한국어 폴더는 배포 ZIP에서 data 아래에 합쳐 로드 순서 설정의 누락을 피한다. 게임 데이터의 언어를 중국어나 일본어로 바꾸지 않는다.

## 이전 배포 방식과 크레디트

[이전 안내와 크레디트](docs/LEGACY_INSTALLATION_KO.md)는 이력 확인용이다. 원본 게임·원본 모드 파일은 포함하지 않는다. 기존 번역자와 원본 모드·sfall·글꼴 제작자의 기여를 유지한다.
