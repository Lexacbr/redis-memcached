# Домашнее задание к занятию «Кеширование Redis/memcached»
---

### Задание 1. Кеширование 

Приведите примеры проблем, которые может решить кеширование. 

---
### Ответ 1

Кэширование позволяет увеличивать производительность за счёт использования сохранённых ранее данных, вроде ответов на сетевые запросы или результатов вычислений. Благодаря кэшу, при очередном обращении клиента за одними и теми же данными, сервер может обслуживать запросы быстрее. Кэширование — эффективный архитектурный паттерн, так как большинство программ часто обращаются к одним и тем же данным и инструкциям. Эта технология присутствует на всех уровнях вычислительных систем. Кэши есть у процессоров, жёстких дисков, серверов, браузеров.
Проблемы котырые решает кэширование: улучшает масштабируемость, снижает нагрузки на сервер, улучшает доступность к данным, уменьшает затраты на обработку данных, уменьшает задержки при доступе к данным.

---

### Задание 2. Memcached

Установите и запустите memcached.

---
### Ответ 2
- Что я делал: 
1. Устанавливаю из стандартного репозитория `memcached` командой: 

```bash
sudo apt install memcached
```
2. Проверяю что процесс запущен:

```bash
sudo systemctl status memcached
```
и получаю вот такой результат:

![memc](https://github.com/Lexacbr/redis-memcached/blob/main/scrsh/memc.png)

---
### Задание 3. Удаление по TTL в Memcached

Запишите в memcached несколько ключей с любыми именами и значениями, для которых выставлен TTL 5. 

*Приведите скриншот, на котором видно, что спустя 5 секунд ключи удалились из базы.*

---

### Задание 4. Запись данных в Redis

Запишите в Redis несколько ключей с любыми именами и значениями. 

*Через redis-cli достаньте все записанные ключи и значения из базы, приведите скриншот этой операции.*


## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже разобраться в материале.

### Задание 5*. Работа с числами 

Запишите в Redis ключ key5 со значением типа "int" равным числу 5. Увеличьте его на 5, чтобы в итоге в значении лежало число 10.  

*Приведите скриншот, где будут проделаны все операции и будет видно, что значение key5 стало равно 10.*