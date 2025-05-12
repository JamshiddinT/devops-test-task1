# Тестовая задача для DevOps / DevOps test task

Пожалуйста, проверьте Helm-чарт приложения и отметьте любые обнаруженные ошибки.
Вам не нужно исправлять каждый YAML-манифест — достаточно указать, где есть проблемы.

Требования к helm чарту:
- Развёртывание без простоя
- 100% доступность
- Возможность разворачивать несколько релизов из разных веток в одном и том же namespace (для тестирования)

Решение отправляйте в текстовом формате с описанием всех найденных проблем. 

Проверка не должна занять более 30–40 минут.

---

Please review the application's Helm chart and identify any errors found.
You do not need to correct every YAML manifest—simply indicate where issues exist.

Helm chart requirements:

- Zero-downtime deployment
- 100% availability
- Ability to deploy multiple releases from different branches within the same namespace (for testing purposes)
Submit the solution in plain text format, detailing all identified problems.

The review should not take more than 30–40 minutes.

# О приложении

Приложение для загрузки и получения картинки

## Функциональность

Загрузка картинки

```sh
curl -F 'image=@/path/to/image.png' my-app.com/upload
```

Получение картинки

```sh
curl http://my-app.com/image -o image.jpg
```

При загрузки следующей картинки предыдущая удаляется

## Требования

- Zero-downtime deployment
- 100% uptime
- Возможность делать несколько релизов для разных веток в один неймспейс (для тестирования)

## Локальный запуск приложения

```sh
make start-app
```

## Деплой

Сборка

```sh
make publish-app BRANCH=master
```

Деплой helm чарта (используется helm 3)

```sh
make deploy HELM=helm
```
