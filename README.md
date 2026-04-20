# Reflection 1
Pertama function pass parameter yang diambil dari tcpstream dan assign sebagai mutable, sehingga dapat ada perubahan data pada stream yang didapat selama proses mengolah data.
lalu assign stream ke BufReader, pada dokumentasi, BufReader dapat meningkatkan kecepeatan program yang menggunakan small dan repeated read calls di network socket yang sama.
lalu parse stream yang yang dibaca BufReader ke variable http_request yang berupa dynamic vector(vector dapat berisi data type apa saja namun hanya 1 data type saja). lalu hasil stream akan diolah dan jadi variable akhir http_request. dan print hasil request dari http_request.

## Commit 2
![Commit 2 screen capture](/assets/images/commit2.png)
