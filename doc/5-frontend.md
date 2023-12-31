## Запуск сервиса frontend
- [Преведущий этап (Запуск сервиса backend)](./4-backend.md)

> Frontend запускается на React, так что здесь мы рассмотрим только настройку и dev-запуск, полный деплой рассмартивается в следующем этапе.

Перейдём к папке frontend
```bash
$ cd ~/stateynik/frontend
```

Установим пакеты
```bash
$ yarn
```

Установим ссылку на backend в .env
```bash
$ nano .env
```

```env
VITE_APP_URL=<ваша url backend сервиса, в нашем случае https://rgit.nosqd.ru/api>
```

Запустим dev версию (`--host` нужен для доступа из вне)
```bash
$ yarn dev --host 0.0.0.0 --port 5173
```

Откроем в браузере http://<url сервера>:5173 (если на вашем backend сервисе установлен SSL, сайт работать не будет по причине не согласовоности http и https)

Вы настроили сервис frontend, информация по настройке с nginx доступна в следующем этапе.

- [Следующий этап (Настройка доменных имён и reverse-proxy через nginx)](./6-domains.md)