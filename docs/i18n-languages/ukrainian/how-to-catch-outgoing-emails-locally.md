<!-- do not translate this -->
| [Read these guidelines in other languages](/docs/i18n-languages) |
|-|
<!-- do not translate this -->

# Як локально відловлювати отримання вихідних електронних листів без їх реальної відправки (Потрібно тільки для робочих процесів електроної пошти)

> **Замітка:** Це не **обов'язковий** крок - потрібно тільки при роботі з робочими процесами електронної пошти

## Вступ

Деякі робочі процеси електронної пошти (наприклад оновлення електронної пошти користувача) вимагають щоб внутрішній сервер через api відправляв електронні листи. Під час розробки ви можете використовувати інструмент для локального відловлення електронної пошти, замість того щоб використовувати реального постачальника електронної пошти та відправляти реальні електронні листи. MailHog - це один з таких засобів тестування електронної пошти для розробників, який ловить електронні листи, надіслані вашим локальним екземляром freeCodeCamp.

## Установка MailHog

MailHog може бути встановлений на macOS, Windows and Linux.

- [Установка MailHog on macOS](#installing-mailhog-on-macos)
- [Установка MailHog on Windows](#installing-mailhog-on-windows)
- [Установка MailHog on Linux](#installing-mailhog-on-linux)

### Встановлення MailHog на macOS

Як встановити MailHog на macOS з допомогою [Homebrew](https://brew.sh/):

```bash
brew install mailhog
brew services start mailhog
```

Дані команди встановлять і запустять службу MailHog у фоновому режимі.

Після цього ви можете перейти безпосередньо до  [використання MailHog](#using-mailhog).

### Установка MailHog on Windows

Завантажте останню версію MailHog з  [офіційного репозиторію](https://github.com/mailhog/MailHog/releases). Виберіть посилання для вашої версії Windows (32 або 64 біт) і .exe файл буде завантажений на ваш комп'ютер.

Після завершення завантаження, клікніть на файл. Можливо, ви отримаєте повідомлення брандмауера Windows де вам потрібно буде дозволити доступ до MailHog. Як тільки ви це зробите, стандартна підказка командного рядка Windows відкриється з уже запущеним MailHog.

Щоб закрити MailHog, закрийте командний рядок. Щоб запустити його знову, клікніть той же .exe файл. Вам не потрібно завантажувати кожен раз новий файл.

Потім ви можете перейти беспосередньо до [використання MailHog](#using-mailhog).

### Установка MailHog on Linux

Спочатку встановіть [Go](https://golang.org).

Для систем на базі Debian, таких як Ubuntu і Linux Mint, виконайте команду

```bash
sudo apt-get install golang
```

Для CentOS, Fedora, Red Hat Linux та інших систем на основі RPM виконайте команду:

```bash
sudo dnf install golang
```

Або:

```bash
sudo yum install golang
```

Задайте шлях до Go:

```bash
echo "export GOPATH=$HOME/go" >> ~/.profile
echo 'export PATH=$PATH:/usr/local/go/bin:$GOPATH/bin' >> ~/.profile
source ~/.profile
```

Потім встановіть і запустіть MailHog:

```bash
go get github.com/mailhog/MailHog
sudo cp /home/$(whoami)/go/bin/MailHog /usr/local/bin/mailhog
mailhog
```

Тепер ви можете перейти до [використання MailHog](#using-mailhog).

## Використання MailHog

Після того, як ви встановили MailHog і запустили його, вам потрібно відкрити поштову скриньку MailHog в своєму браузері, відкрити нову вкладку або вікно і перейти за адресою [http://localhost:8025](http://localhost:8025)

![MailHog Screenshot 1](images/mailhog/1.jpg)

Коли ваша freeCodeCamp збірка відправить електронного листа, ви побачите його на екрані, як показано нижче:

![MailHog Screenshot 2](images/mailhog/2.jpg)

Відкрийте електронний лист, і ви побачите дві вкладки, де ви можете переглянути вміст: звичайний текст і джерело. Переконайтеся, що ви перебуваєте на вкладці звичайного тексту.

![MailHog Screenshot 3](images/mailhog/3.jpg)

Будь-які посилання в листі так само повинні бути доступні для перегляду.

## Корисні посилання

- З будь-якими іншими питаннями, пов'язаних з MailHog або інструкціями по призначених для користувача налаштувань, ви можете ознайомитися в [MailHog](https://github.com/mailhog/MailHog)