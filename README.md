# Module 5

## Reflection
Hasil JMeter GUI sebelum *profiling*:<br>
![/all-studentendpoint](https://media.discordapp.net/attachments/1058012034970681454/1217050818927136779/image.png?ex=66029de6&is=65f028e6&hm=a28f6658181767c1293e4e6024042eda6177d0b31d20721c5ae47a2caa5e8cdf&=&format=webp&quality=lossless&width=835&height=462)
![/all-student-nameendpoint](https://media.discordapp.net/attachments/1058012034970681454/1217115291419672586/image.png?ex=6602d9f2&is=65f064f2&hm=c2deb7243f0a94a3a7dd493f603a8e844212f667f3865a1ccbebd3073c837578&=&format=webp&quality=lossless&width=550&height=306)
![/highest-gpaendpoint](https://media.discordapp.net/attachments/1058012034970681454/1217117037915013131/image.png?ex=6602db92&is=65f06692&hm=356897e61b2baac4a57673a1109329fb8a4466170f081a3c1e754ea44734ce6c&=&format=webp&quality=lossless&width=820&height=462)

Hasil JMeter CLI sebelum *profiling*:<br>
![/all-studentendpoint](https://media.discordapp.net/attachments/1058012034970681454/1217121077507915847/image.png?ex=6602df55&is=65f06a55&hm=c4cff21542d795e91e236de8efc8995be55b046d608fa852bad85f55376b8ce2&=&format=webp&quality=lossless&width=550&height=89)
![/all-student-nameendpoint](https://media.discordapp.net/attachments/1058012034970681454/1217121151281533059/image.png?ex=6602df67&is=65f06a67&hm=df04fb6178b3e651d7e6a9670bb622457516806a5c4314395c8953405adc80f4&=&format=webp&quality=lossless&width=998&height=149)
![/highest-gpaendpoint](https://media.discordapp.net/attachments/1058012034970681454/1217121809305174148/image.png?ex=6602e004&is=65f06b04&hm=dbc1a69298c817ee05d413c6c8f04962332ee6b743587258afd5d1bacf6cdd3f&=&format=webp&quality=lossless&width=998&height=162)

Hasil JMeter CLI setelah *profiling*:<br>
![/all-studentendpoint](https://media.discordapp.net/attachments/1058012034970681454/1217145809704059042/image.png?ex=6602f65e&is=65f0815e&hm=6e92e57cf36f61e8ece255807a8496e255db28395ced284101e297b8afd195d3&=&format=webp&quality=lossless&width=550&height=85)
![/all-student-nameendpoint](https://media.discordapp.net/attachments/1058012034970681454/1217145878867873902/image.png?ex=6602f66e&is=65f0816e&hm=8b1cea0eef319d6427cda651d3e269d152ae9d8c5e738f205619ccb3b0c5eef8&=&format=webp&quality=lossless&width=998&height=160)
![/highest-gpaendpoint](https://media.discordapp.net/attachments/1058012034970681454/1217145951765008454/image.png?ex=6602f680&is=65f08180&hm=3e8299b94cec3b9b91c3892b50a1e8766a67ff3e57593dd9893c8d6d65baf5f8&=&format=webp&quality=lossless&width=998&height=159)

    Berdasarkan foto diatas, terlihat bahwa *profiling* membuat *time elapsed* pada method-method di kode yang awalnya cukup terbilang lama menjadi berkali-kali jauh lebih cepat. Setelah itu, dapat disimpulkan bahwa optimasi terhadap alur program tentu berpengaruh juga terhadap pengujian aplikasi secara *blackbox* dengan memanfaatkan JMeter.

1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?

    Pengujian menggunakan JMeter tidak terlalu fokus pada internal dari aplikasi atau program, sehingga sering dianggap sebagai metode pengujian *blackbox*. Ini karena JMeter hanya bertugas untuk mengirim permintaan ke endpoint yang telah ditentukan, sesuai dengan jumlah yang diminta oleh pengujinya. JMeter bertindak dengan mengevaluasi apakah permintaan tersebut dapat dijalankan dengan sukses dan mendapatkan respons. Di sisi lain, pendekatan *profiling* lebih mendalam dalam memeriksa proses internal program saat menerima suatu permintaan. Melalui *profiling*, saya dapat mengidentifikasi bagian mana dari program yang membutuhkan waktu paling lama untuk dieksekusi dibandingkan dengan bagian lain, memungkinkan optimisasi yang lebih efektif terhadap kode.

2. How does the profiling process help you in identifying and understanding the weak points in your application?

    Melalui profiling, saya dapat mengidentifikasi komponen mana dalam program yang memperlambat performa aplikasi secara umum. Ini memungkinkan saya untuk fokus mengoptimalkan komponen tersebut, yang pada gilirannya akan meningkatkan efisiensi keseluruhan aplikasi tanpa harus mengubah banyak aspek lainnya.

3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?

    Benar, seperti yang dijelaskan dalam tutorial tersebut, dengan menggunakan Intellij profiler, saya dapat mengungkap bahwa bagian program yang paling memboroskan waktu, misalnya metode getAllStudentWithCourse yang memperlukan loop terlalu berlebih. Profiler ini bahkan memungkinkan saya untuk melihat baris kode mana dalam metode tersebut yang paling mempengaruhi efisiensi metode. Dengan informasi tentang berapa lama waktu yang dibutuhkan untuk menjalankan setiap pemanggilan fungsi, saya menjadi lebih mudah untuk mengidentifikasi komponen mana dalam program yang menjadi hambatan utama bagi kinerja aplikasi secara keseluruhan.

4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?

    Kesulitan terbesar yang saya hadapi dalam pengujian performa dan profiling terletak pada kemampuan untuk menginterpretasikan output yang relevan dan mengidentifikasi komponen mana dalam program yang bertindak sebagai penghambat utama. Untuk mengatasi ini, solusinya adalah dengan mempelajari dan memahami hasil output dari JMeter atau profiler secara lebih teliti. Ini mungkin memerlukan waktu untuk terbiasa dengan teknologi baru tersebut agar dapat lebih mudah memahami informasi yang cukup detail.

5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?

    Seperti yang telah dibahas sebelumnya, menggunakan *profiler* dari IntelliJ memungkinkan saya untuk mengidentifikasi komponen program yang mengalami kebuntuan, mengetahui durasi yang dibutuhkan untuk menjalankan sebuah pemanggilan metode, dan menentukan frekuensi pemanggilan metode tersebut. Dengan informasi ini, kita dapat menargetkan area spesifik untuk optimasi dan membedakan mana yang tidak perlu diutak-atik. Penting untuk diingat bahwa "optimasi prematur merupakan sumber segala masalah" karena optimasi yang tergesa-gesa tidak hanya bisa mengurangi keterbacaan kode, tetapi juga dapat menyebabkan komplikasi yang tidak perlu.

6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?

    Setelah mengerjakan sejauh ini, belum terdapat ke tidak konsistenan dalam hasil *performance testing* yang dikeluarkan oleh IntelliJ Profiler dengan JMeter. Ini menunjukkan bahwa kedua aplikasi tersebut telah memberikan pandangan yang konsisten tentang bagaimana performa aplikasi dalam konteks pengujian kode saya.

7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?

    Berdasarkan strategi nomor 2, setelah melakukan tes dan profiling, langkah yang saya ambil adalah mengevaluasi durasi yang dibutuhkan oleh program untuk merespons permintaan melalui JMeter. Bila respons terasa lambat, saya akan menggunakan profiler untuk mengidentifikasi bagian kode mana yang menyebabkan penundaan dan kemudian mencari solusi untuk mempercepat proses tersebut. Untuk memverifikasi keakuratan kode pasca-modifikasi, saya memastikan bahwa outputnya tetap konsisten dengan sebelum dilakukan perubahan. 

    Pendekatan yang lebih efektif adalah dengan membuat unit test, sebagaimana diuraikan dalam tutorial sebelumnya. Dengan menjalankan unit test dan memastikannya berhasil, dapat diasumsikan bahwa kode yang telah direfaktor berfungsi dengan baik, asalkan *unit testnya* dirancang dengan benar dan relevan. Ini memungkinkan fokus perbaikan hanya pada aspek-aspek yang memang memerlukan peningkatan, tanpa perlu mengubah seluruh bagian kode.
