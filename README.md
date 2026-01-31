# jayjazy.github.io

DeepLink Practice App을 위한 App Links 검증 및 웹 인터페이스를 제공하는 GitHub Pages 저장소입니다.

## 개요

이 저장소는 Android App Links를 활성화하기 위해 필요한 Digital Asset Links 파일과 웹 인터페이스를 호스팅합니다.

## 주요 파일

### 1. Digital Asset Links 검증 파일

**경로:** `/.well-known/assetlinks.json`

Android App Links가 작동하기 위해 필수적인 도메인 소유권 검증 파일입니다.

```json
[{
  "relation": ["delegate_permission/common.handle_all_urls"],
  "target": {
    "namespace": "android_app",
    "package_name": "com.jay.deeplinkapp",
    "sha256_cert_fingerprints": [
      "95:da:36:be:28:79:2e:a2:f4:ff:d8:93:7b:f6:ff:62:c7:e8:31:af:f8:96:4d:7b:1d:72:19:9a:d5:a7:3a:40"
    ]
  }
}]
```

**역할:**
- Android 시스템이 `com.jay.deeplinkapp` 앱이 `jayjazy.github.io` 도메인을 처리할 권한이 있음을 확인
- 앱 설치 시 자동으로 도메인 검증 수행
- 검증 성공 시 웹 링크 클릭 시 선택창 없이 바로 앱이 열림

## 관련 링크

- [Android App Links 공식 문서](https://developer.android.com/training/app-links)
- [Digital Asset Links 설명](https://developers.google.com/digital-asset-links/v1/getting-started)
- [GitHub Pages 문서](https://docs.github.com/en/pages)

## 라이선스

이 프로젝트는 학습 목적으로 만들어진 샘플입니다.
