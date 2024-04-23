# Tutorial 8 Publisher Reflection Notes

a. How many data will your publisher program send to the message broker in one run?

Mengacu kepada programnya, akan ada 5 data yang dikirimkan program dalam sekali jalan dengan data berupa user id dari 1 sampai 5 dan nama yang berbeda-beda.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

Artinya, server RabbitMQ yang disambungkan dengan protokol AMQP pada package subscriber digunakan juga pada program ini (server yang sama). Oleh karena itu, interaksi antara dua program ini bisa saja terlihat menjadi satu.

### Foto RabbitMQ sedang berjalan

![Foto RabbitMQ](running_rabbitmq.png)

### Foto Console saat menjalankan `cargo run` Publisher

![Foto console](console_ss.png)

Ketika publisher di run, publisher mengirimkan 5 data ke server RabbitMQ. Karena subscriber melakukan listen atas aktivitas di server RabbitMQ, maka ketika data dari publisher datang, subscriber mendeteksi bahwa ada data yang datang sehingga menampilkan data tersebut sesuai format.

### Foto Spike pada Message Rate

![Foto spike pada message rate](message_rate_spike.png)

Graf yang kedua (yang bawah) adalah graf untuk message rate. Untuk setiap message yang masuk, message akan dikalkulasikan untuk dihitung rate-nya -- seberapa banyak message dikirim setiap detiknya. Dalam contoh di atas, saya mencoba menjalankan kode publisher kira-kira 3 kali, dimana yang kali pertama saya menjalankan langsung 3 kali sekaligus, lalu yang kedua dan ketiga masing-masing 1 kali diberi jarak. Makanya untuk graf yang kiri lebih tinggi dibandingkan graf yang di kanan.
