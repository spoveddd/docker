# Prometheus Monitoring Stack

## Описание проекта
Данный стек предназначен для мониторинга Nginx-сервера с использованием Prometheus, Grafana и Alertmanager. Он также поддерживает проверки доступности (Blackbox Exporter) и отправку уведомлений в Telegram через Alertmanager Bot.

## Предварительные требования
- Docker (версия 20.10 или выше).
- Docker Compose (версия 1.29 или выше).
- Операционная система Linux (проверено на Ubuntu 22.04).

## Содержание проекта

### Основные компоненты
- **Prometheus**: Система мониторинга и сбора метрик.
- **Grafana**: Визуализация данных и построение дашбордов.
- **Alertmanager**: Управление алертами и уведомлениями.
- **Node Exporter**: Сбор метрик о системе.
- **Blackbox Exporter**: Проверка доступности внешних ресурсов.
- **Alertmanager Bot**: Интеграция Alertmanager с Telegram.

## Установка

1. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/spoveddd/prometheus_stack.git
   cd prometheus_stack
   ```

2. Отредактируйте конфигурационные файлы:
   - `docker-compose.yml`: Укажите ваш Telegram токен {{TOKEN BOT}} и ID администратора {{ADMIN TOKEN}}.
   - `prometheus/prometheus.yml`: Добавьте при необходимости цели для мониторинга.
   - `blackbox/blackbox.yml`: Добавьте сайты для проверки доступности.

3. Запустите стек:
   ```bash
   docker-compose up -d
   ```

4. Откройте браузер:
   - Prometheus: [http://localhost:9090](http://localhost:9090)
   - Grafana: [http://localhost:3000](http://localhost:3000) (логин/пароль: admin/admin)

## Как остановить

Для остановки используйте:
```bash
docker-compose down
```

## Лицензия
MIT License. Свободное использование с указанием автора.

