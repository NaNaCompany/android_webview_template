# Android WebView App Template

안드로이드 스튜디오 없이, GitHub Actions를 통해 빌드할 수 있는 간단한 웹뷰 앱 템플릿입니다.

## 📁 프로젝트 구조

이 폴더(`android-webview-template/`)를 그대로 GitHub 저장소에 올리시면 됩니다.

주요 파일:
- **`app/src/main/res/values/strings.xml`**: 앱 이름과 연결할 웹사이트 URL 설정
- **`app/src/main/AndroidManifest.xml`**: 권한 및 설정 (기본적으로 인터넷 권한 포함됨)
- **`.github/workflows/build.yml`**: GitHub Actions 빌드 스크립트 (수정 불필요)

## 🛠️ 설정 방법 (커스터마이징)

### 1. 앱 이름 및 URL 변경
`app/src/main/res/values/strings.xml` 파일을 열어 다음 내용을 수정하세요.

```xml
<resources>
    <!-- 앱 이름 -->
    <string name="app_name">내 앱 이름</string>
    
    <!-- 연결할 웹사이트 URL -->
    <string name="webview_url">https://www.example.com</string>
</resources>
```

### 2. 앱 아이콘 변경
`app/src/main/res/` 폴더 내의 `mipmap-`으로 시작하는 폴더들에 있는 이미지를 교체하면 됩니다.
- 가장 쉬운 방법: [Android Asset Studio](https://romannurik.github.io/AndroidAssetStudio/icons-launcher.html) 같은 사이트에서 아이콘을 생성한 뒤, 다운로드 받은 `res` 폴더의 내용물로 `app/src/main/res/`를 덮어씌우세요.
- 파일명은 반드시 `ic_launcher` (기본) 및 `ic_launcher_round` (원형) 여야 합니다.

## 🚀 빌드 방법 (GitHub Actions)

1. **GitHub 업로드**: 이 `android-webview-template` 폴더 안의 모든 파일을 새로운 GitHub Repository에 업로드(Push)합니다.
2. **Actions 탭 확인**: 저장소의 **Actions** 탭으로 이동하면 "Build Android APK" 워크플로우가 자동으로 실행되는 것을 볼 수 있습니다.
3. **다운로드**:
    - 워크플로우 실행이 초록색 체크(성공)로 끝나면 해당 실행 기록을 클릭합니다.
    - 화면 하단의 **Artifacts** 섹션에서 `app-debug`를 클릭하면 APK 파일이 다운로드됩니다.
    - 다운로드된 압축을 풀면 `app-debug.apk`가 나옵니다.

## 📱 설치 및 테스트
다운로드 받은 APK를 안드로이드 폰에 넣고 설치하세요.
(디버그 서명된 앱이므로 Play 프로텍트 경고가 뜰 수 있으며, "무시하고 설치"를 선택하면 됩니다.)
