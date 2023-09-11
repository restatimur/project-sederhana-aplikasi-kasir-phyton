# project-sederhana-aplikasi-kasir-phyton
Project Sederhana Pembuatan Aplikasi Kasir Sederhan Pyhton

Adapun Penjelasan Detail aplikasi adalah sebagai berikut:

## class Transaction
Kelas adalah sebuah blueprint atau cetak biru untuk menciptakan objek. 
Ketika mendefinisikan sebuah kelas, sebenarnya mendefinisikan tipe data baru yang dapat digunakan untuk membuat objek-objek.
Dalam konteks ini kita buat terlebih dahulu class Transaction.
```sh
class Transaction:
```

## __init__(self)
Konstruktor adalah metode khusus yang dipanggil saat objek dari kelas tersebut dibuat (diinisialisasi).
Dalam konteks yang Anda berikan, def __init__(self): adalah konstruktor untuk kelas Transaction. Fungsi ini memiliki satu parameter, yaitu self, yang merujuk pada objek yang akan dibuat.
```sh
def __init__(self):
        self.transaction_data = []
        self.discount = 0
```

## add_item
Dari sini kita akan mulai membuat methode untuk menambahkan nama item, jumlah item dan harga item.
```sh
    def add_item(self, item_name, item_qty, item_price):
        item_total_price = item_qty * item_price
        self.transaction_data.append([item_name, item_qty, item_price, item_total_price])
```

## update_item
Ini merupakan methode untuk mengubah item yang dibagi menjadi 3 yaitu 

Update Nama Item
```sh
    def update_item_name(self, old_name, new_name):
        for item in self.transaction_data:
            if item[0] == old_name:
                item[0] = new_name
```

Update Jumlah Item
```sh
    def update_item_qty(self, item_name, new_qty):
        for item in self.transaction_data:
            if item[0] == item_name:
                item[1] = new_qty
                item[3] = new_qty * item[2]
```

Update Harga Item
```sh
    def update_item_price(self, item_name, new_price):
        for item in self.transaction_data:
            if item[0] == item_name:
                item[2] = new_price
                item[3] = item[1] * new_price
```

## delete_item
ini merupakan methode untuk menghapus item 
```sh
    def delete_item(self, item_name):
        self.transaction_data = [item for item in self.transaction_data if item[0] != item_name]
```

## reset_transaction
ini merupakan methode untuk mereset transaksi 
```sh
    def reset_transaction(self):
        self.transaction_data = []
```




# Cara Menjalakan Aplikasi
Dengan menjalankan script .......... di [JUPYTER](https://jupyter.org/try-jupyter/lab/index.html)


