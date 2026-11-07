# Загрузка исходников патча 2.5

В этот репозиторий необходимо добавить содержимое архива `UpravlenieDomami_patch_2_5_source.zip` **с сохранением структуры папок**.

## Что должно появиться в корне репозитория

```
UpravlenieDomami-Android-2.5/
  app/
    build.gradle
    src/main/AndroidManifest.xml
    src/main/java/ru/dommanagement/local/MainActivity.java
    src/main/assets/index.html
    src/main/assets/yaroslavka-card.png
    src/main/assets/monolit-card.png
    src/main/assets/banya-card.png
    ...
  build.gradle
  settings.gradle
  gradle.properties
  README_RU.txt
PATCH_2_5_README_RU.md
.github/workflows/android.yml
```

## На ПК
1. Скачайте и распакуйте архив 2.5.
2. На GitHub откройте репозиторий, выберите **Add file → Upload files**.
3. Перетащите **папку `UpravlenieDomami-Android-2.5` целиком** из проводника в область загрузки, а также `PATCH_2_5_README_RU.md`.
4. Проверьте в предварительном списке, что пути начинаются с `UpravlenieDomami-Android-2.5/` и сохраняют `app/src/main/`, затем нажмите **Commit changes**.
5. Перейдите **Actions → Android 2.5 — Debug APK**, после успешной сборки скачайте артефакт APK.

**Важно:** загружать один ZIP недостаточно. Не размещайте `AndroidManifest.xml` или `MainActivity.java` в корне репозитория.

## Известные ограничения
Полноценный GPT-помощник, серверная синхронизация Android/iOS, полноценные права пользователей и точное воспроизведение всего дизайна в патче пока не реализованы.

**Проверить перед выпуском APK:** в оригинальном архиве `app/build.gradle` может содержать `versionName '2.4'`; необходимо изменить на `2.5` и согласовать `versionCode` для установки поверх прежних версий. Сам факт сборки APK не означает готовности и безопасности приложения.
