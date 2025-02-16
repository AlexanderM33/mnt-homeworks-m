# Домашнее задание к занятию 15 «Система сбора логов Elastic Stack»



## Задание 1

Вам необходимо поднять в докере и связать между собой:

- elasticsearch (hot и warm ноды);
- logstash;
- kibana;
- filebeat.

Logstash следует сконфигурировать для приёма по tcp json-сообщений.

Filebeat следует сконфигурировать для отправки логов docker вашей системы в logstash.

В директории [help](./help) находится манифест docker-compose и конфигурации filebeat/logstash для быстрого 
выполнения этого задания.

Результатом выполнения задания должны быть:

- скриншот `docker ps` через 5 минут после старта всех контейнеров (их должно быть 5);
- скриншот интерфейса kibana;
- docker-compose манифест (если вы не использовали директорию help);
- ваши yml-конфигурации для стека (если вы не использовали директорию help).

![VirtualBox_FEDORA_15_01_2024_22_23_50](https://github.com/AlexanderM33/mnt-homeworks-m/assets/122460278/94789128-6bea-46c8-84fb-590820de73c9)

![VirtualBox_FEDORA_15_01_2024_22_22_55](https://github.com/AlexanderM33/mnt-homeworks-m/assets/122460278/6f2345bc-de64-4f62-9c47-52bea2399563)




## Задание 2

Перейдите в меню [создания index-patterns  в kibana](http://localhost:5601/app/management/kibana/indexPatterns/create) и создайте несколько index-patterns из имеющихся.

Перейдите в меню просмотра логов в kibana (Discover) и самостоятельно изучите, как отображаются логи и как производить поиск по логам.

В манифесте директории help также приведенно dummy-приложение, которое генерирует рандомные события в stdout-контейнера.
Эти логи должны порождать индекс logstash-* в elasticsearch. Если этого индекса нет — воспользуйтесь советами и источниками из раздела «Дополнительные ссылки» этого задания.

![6](https://github.com/AlexanderM33/mnt-homeworks-m/assets/122460278/fd668821-489c-4c07-ab52-8c66c48f48c2)

![5](https://github.com/AlexanderM33/mnt-homeworks-m/assets/122460278/009cf4eb-b57d-4968-bf7f-d6c9ecdae66c)

![7](https://github.com/AlexanderM33/mnt-homeworks-m/assets/122460278/f79716ae-1365-4eae-aa43-ed93cb657820)

![4](https://github.com/AlexanderM33/mnt-homeworks-m/assets/122460278/2a3a1e0c-369d-453b-b255-240591d6766d)

![3](https://github.com/AlexanderM33/mnt-homeworks-m/assets/122460278/850a6e1b-8f46-4126-88a9-34672bff29fd)



 
---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---



## Дополнительные ссылки

При выполнении задания используйте дополнительные ресурсы:

- [поднимаем elk в docker](https://www.elastic.co/guide/en/elastic-stack-get-started/current/get-started-docker.html);
- [поднимаем elk в docker с filebeat и docker-логами](https://www.sarulabs.com/post/5/2019-08-12/sending-docker-logs-to-elasticsearch-and-kibana-with-filebeat.html);
- [конфигурируем logstash](https://www.elastic.co/guide/en/logstash/current/configuration.html);
- [плагины filter для logstash](https://www.elastic.co/guide/en/logstash/current/filter-plugins.html);
- [конфигурируем filebeat](https://www.elastic.co/guide/en/beats/libbeat/5.3/config-file-format.html);
- [привязываем индексы из elastic в kibana](https://www.elastic.co/guide/en/kibana/current/index-patterns.html);
- [как просматривать логи в kibana](https://www.elastic.co/guide/en/kibana/current/discover.html);
- [решение ошибки increase vm.max_map_count elasticsearch](https://stackoverflow.com/questions/42889241/how-to-increase-vm-max-map-count).

В процессе выполнения в зависимости от системы могут также возникнуть не указанные здесь проблемы.

Используйте output stdout filebeat/kibana и api elasticsearch для изучения корня проблемы и её устранения.

## Задание повышенной сложности

Не используйте директорию [help](./help) при выполнении домашнего задания.
 
