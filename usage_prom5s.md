# Использование prom5s (prometheus)

## **Prom5s** производит сбор, хранение, анализ и отображение метрик о работе:

* хоста (сервера) - NodeExporter
* docker сервиса и контейнеров - cAdvisor
* СУБД PostgreSQL - Postgres_exporter

Метрики экспортеров собираются и хранятся в БД [Prometheus](http://prometheus.io), доступ через www сервис - ссылка на cis сервисе dcape: `www-prom5s`.
Также [Prometheus](http://prometheus.io) анализирует метрики и рассылает предупреждения на e-mail или сервисы типа Slack о различных событиях (достижение значением установленного порога, прогнозируемое достижение значения и т.п.).
Подробная документация по работе с [Prometheus](https://prometheus.io/docs/introduction/overview/)

Метики из БД [Prometheus](http://prometheus.io) отображаются на приборных панелях [Grafana](http://grafana.io), доступ через www сервис - ссылка на cis сервисе dcape: `grafana-prom5s`.
Для доступа - нажать кнопку "Sing Up", заполнить поля.
Смотрите также [информацию](http://docs.grafana.org/tutorials/screencasts/) по работе с панелями Grafana.  

Grafana сохраняет свои настройки иданные в именованном томе "grafana_data". При обновлении не теряются данные метрик. Но при необходимости смены паролей, нужно перед обновлением остановить контейнер и убедится в том, что именованый том удален.

## License

The MIT License (MIT), see [LICENSE](LICENSE).

2018 Maxim Danilin <zan@whiteants.net>
