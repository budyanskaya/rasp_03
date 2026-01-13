# Практическое задание №3. Асинхронное взаимодействие через RabbitMQ
## Разработайте систему обработки заказов с асинхронным взаимодействием через брокер сообщений.
### Требуется реализовать:
* Producer для отправки заказов в очередь RabbitMQ
* Consumer для обработки заказов из очереди (имитация обработки: sleep 2 сек)
* Docker Compose конфигурацию для запуска RabbitMQ
* Структуру JSON сообщения: order_id, customer, amount, status
### Проанализировать:
* Время обработки 5 заказов
* Надежность доставки (роль basic_ack)
* Преимущества асинхронности над синхронными вызовами
### Формат сдачи: producer.py, consumer.py, docker-compose.yml 

## Ход работы
В docker-compose.yml появятся в файле кнопки плей, которые надо нажать для запуска файла
<img width="660" height="337" alt="image" src="https://github.com/user-attachments/assets/71a511d8-a045-4f57-80fa-54af9c784ae0" />

### Далее по шагам в терминале выполняем команды
```
pip install pika
```
```
docker-compose up -d
```
### В одном терминале делаем запуск consumer
```
python consumer.py
```
### А в другом отправка заказов
python producer.py
