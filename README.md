# Tutorial 8 Publisher Reflection Notes

a. How many data will your publisher program send to the message broker in one run?

Mengacu kepada programnya, akan ada 5 data yang dikirimkan program dalam sekali jalan dengan data berupa user id dari 1 sampai 5 dan nama yang berbeda-beda.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

Artinya, server RabbitMQ yang disambungkan dengan protokol AMQP pada package subscriber digunakan juga pada program ini (server yang sama). Oleh karena itu, interaksi antara dua program ini bisa saja terlihat menjadi satu.

### Foto RabbitMQ sedang berjalan
![Foto RabbitMQ](running_rabbitmq.png)
