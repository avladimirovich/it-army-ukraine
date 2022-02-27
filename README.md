# it-army-ukraine

## Спочатку

1. Купити на настроїти любий сервер з Ubuntu. Головний критерій - потужність процесора.
1. [Настроїти термінал](terminal.md).

## 1. Під'єднатись до сервера

1. Відкрийте [термінал](terminal.md).
1. Виконайте команду `ssh root@xxx.xxx.xxx.xxx`, де:
  - `root` - це ім'я юзера сервера.
  - `xxx.xxx.xxx.xxx` - ip адреса сервера.
1. В перший раз потрібно погодитиь, написавши `yes`.
1. Ввести пароль.

## 2. Встановити потрібні програми (тільки один раз)

- Докер. Виконати команду `https://raw.githubusercontent.com/SecorD0/utils/main/installers/docker.sh`
- Screen. Виконати команду: `sudo apt install screen`

## 3. Тепер до дії. Логіка така:

1. Почитаємо нову сессію. Пишемо `screen -S {name}`, де:
   - `name` - назва сессії, наприклад `123`.
1. Запускаємо команду. Конкретні команди я тут опублікувати не можу, слідкуйте за телеграм каналами.
1. тиснемо 2 комбінації на клавіатурі одну за одною: `ctrl+a, ctrl+d`
1. міняємо команду і заново починаючи з 1.

## 4. Моніторинг

Запускаємо команду `htop`, наблюдаємо за нагрузкою сервера.
Щоб вийти з режиму `htop`, натисніть F10.

Для переключення між відкритими сессіями, користуємось командами:

- `screen -ls` - показати список сессій.
- `screen -r {name}` - перейти в сессію з назвою `{name}`.
- `screen -XS {name} quit` - завершити сессію з назвою `{name}`
