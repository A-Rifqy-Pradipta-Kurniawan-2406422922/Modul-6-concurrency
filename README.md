# Reflection 1
Pertama function pass parameter yang diambil dari tcpstream dan assign sebagai mutable, sehingga dapat ada perubahan data pada stream yang didapat selama proses mengolah data.
lalu assign stream ke BufReader, pada dokumentasi, BufReader dapat meningkatkan kecepeatan program yang menggunakan small dan repeated read calls di network socket yang sama.
lalu parse stream yang yang dibaca BufReader ke variable http_request yang berupa dynamic vector(vector dapat berisi data type apa saja namun hanya 1 data type saja). lalu hasil stream akan diolah dan jadi variable akhir http_request. dan print hasil request dari http_request.

## Commit 2
![Commit 2 screen capture](/assets/images/commit2.png)

# Reflection 3
disini kita perlu mengecek header request html, jika path ke root, maka assign ke hello html dengan status OK, namun jika path lain terlibat seperti /bad maka akan mereturn 404 NOT FOUND.

## Commit 3
![Commit 3 SS](/assets/images/commit3.png)

# Reflection 4
saat load, browser menjadi berada dalam state load karena keberadaan sleep di code. kita assign sleep 10 detik sebelum broswer benar-benar load ke hello.html. dalam kasus banyak user, ini dapat digunakan untuk kasus dimana concurrency terjadi, biasanya pada war tiket dimana pengguna akan loading terlebih dahulu dan ditempatkan pada antrian.

# Reflection 5
ThreadPool bekerja dengan melakukan spawn beberapa worker(pool), dengan itu backend dapat menerima beberapa request sekaligus, membuat jika ada stall/user yang melakukan sleep backend tidak stuck di process tersebut dan worker lain yang akan menerima request dari orang lain tanpa menunggu sleep.

# Bonus
build digunakan untuk menambahkan aturan tambahan validasi, pada kasus ini digunakan untuk memastikan bahwa pool yang di buat harus lebih dari 0 dan akan ada fallback jika tidak memenuhi aturan instead of langsung error di programnya.
