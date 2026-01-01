# Android WebView App Generator

이 프로젝트는 나만의 안드로이드 웹뷰 앱을 **설정 파일 수정만으로** 쉽게 만들 수 있는 템플릿입니다. 안드로이드 스튜디오가 없어도 GitHub Actions가 자동으로 앱을 빌드해줍니다.

## 🚀 사용 방법

### 1단계: 설정 변경 (`config.yml`)
`config.yml` 파일을 열어 내 앱 이름과 연결할 웹사이트 주소를 적으세요.

```yaml
app_name: "내 멋진 앱"
webview_url: "https://www.example.com"
```

### 2단계: 아이콘 등록 (`icon.png`)
이 폴더에 있는 `icon.png` 파일을 원하는 앱 아이콘 이미지로 교체하세요.
- 파일 이름은 반드시 `icon.png` 여야 합니다.
- 고해상도(512x512 이상) 이미지를 권장합니다.

### 3단계: GitHub에 업로드
이 폴더의 모든 파일을 GitHub 저장소(Repository)에 업로드(Commit & Push)하세요.
(폴더 구조를 그대로 유지해야 합니다.)

## 📦 앱 다운로드 (APK)

1. GitHub 저장소 상단의 **Actions** 탭을 클릭합니다.
2. 실행 중이거나 완료된 **Build Custom Android APK** 워크플로우를 클릭합니다.
3. 빌드가 성공(초록색 체크)하면, 페이지 하단의 **Artifacts** 영역에서 `app-debug`를 클릭하여 다운로드합니다.
4. 압축을 풀고 나온 `apk` 파일을 스마트폰에 설치합니다.

---
**참고**: 내부에 포함된 `android-webview-template` 폴더는 실제 안드로이드 프로젝트 소스코드입니다. 개발자가 아니라면 수정할 필요가 없습니다.
