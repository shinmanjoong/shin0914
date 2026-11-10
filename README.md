# 운세·타로·로또 — Android 프로젝트

Android Studio(최신 안정판)에서 이 폴더를 열면 됩니다. (Open → 이 폴더 선택 → Gradle Sync)

## Google Play용 AAB 만들기
1. 메뉴 **Build → Generate Signed App Bundle / APK → Android App Bundle** 선택
2. **Create new...** 로 업로드 키(.jks)를 만들고 비밀번호를 기록해 둡니다. 키 파일은 잃어버리면 복구가 어려우니 별도 보관하세요.
3. **release** 로 빌드하면 `app/release/app-release.aab` 가 생깁니다.
4. Play Console → 앱 만들기 → 프로덕션/비공개 테스트에 이 AAB를 업로드합니다. (Play 앱 서명 사용을 권장합니다.)

## 설정값
- 패키지명(applicationId): `app.saju.fortune` — Play에 올리면 바꿀 수 없으니 올리기 전에 원하는 값으로 수정하세요. (app/build.gradle 의 namespace/applicationId, MainActivity 패키지 폴더·선언)
- targetSdk 36 / minSdk 24 / versionCode 1 (업데이트마다 versionCode를 1씩 올려야 합니다)
- 앱 화면은 `app/src/main/assets/www/index.html` 입니다.
