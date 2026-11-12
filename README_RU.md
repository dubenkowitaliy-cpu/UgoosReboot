# Ugoos Reboot

Минимальное Android-приложение для Ugoos AM6B+ под Android 9.

- Название в лаунчере: **Перезагрузка**
- Package: `com.cranium.reboot`
- Min SDK: 23 (Android 6.0)
- Target SDK: 28 (Android 9)
- Разрешения Android: не запрашивает
- Сеть, реклама, фоновые службы: отсутствуют
- Root запрашивается через Magisk только после подтверждения пользователем
- Команда: `su -c reboot`

При запуске отображается большая кнопка. Перед перезагрузкой приложение спрашивает подтверждение, чтобы избежать случайного рестарта с пульта.

## Сборка APK в Android Studio

Нужны Android Studio, JDK 17 и Android SDK Platform 34.

1. Распакуйте архив.
2. Откройте папку `UgoosReboot` в Android Studio.
3. Дождитесь синхронизации Gradle.
4. Выберите **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. APK будет в `app/build/outputs/apk/debug/app-debug.apk`.

## Установка через ADB из PowerShell

```powershell
.\adb.exe install .\app-debug.apk
```

После первого нажатия «Перезагрузить» подтвердите root-доступ для `com.cranium.reboot` в Magisk. В Projectivy добавьте приложение «Перезагрузка» в избранное.

## Важно

Это исходный проект, не готовый APK. APK нужно собрать в Android Studio. Само приложение не меняет разделы, загрузчик, CoreELEC или Dual Boot.
