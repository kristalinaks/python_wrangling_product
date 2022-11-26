# Wrangling &amp; Viz: Product Analysis

Report and Explanation: https://medium.com/@kristalinaks/wrangling-analisis-produk-di-suatu-toko-aaefd7f6162e

---

# Objektif Analisis: Analisis Produk

Perusahaan ingin mengetahui total penjualan dari tiap kategori produk.

Perusahaan ingin mengetahui kategori produk yang paling banyak dipesan.

Perusahaan ingin mengetahui pertumbuhan pemesanan 10 produk yang paling diminati.

---
# Data Overview

Data yang adalah digunakan diambil dari database olist yang berisikan 9 tabel: Olist Customers, Olist Geolocation, Olist Order Items, Olist Order Payment, Olist Order Review, Olist Orders, Olist Products, Olist Seller, dan Product Category Name Translation.
Dalam analisis ini, digunakan 4 tabel yaitu Tabel Order (Olist Orders), Tabel Items (Olist Order Items), Tabel Product (Olist Products), dan Tabel Translation (Product Category Name Translation).

## 1. Tabel Order (Olist Orders)

order_id : unique identifier of the order

customer_id : key to the customer dataset. Each order has a unique customer_id

order_status: reference to the order status

order_purchase_timestamp: shows the purchase timestamp

order_approved_at: shows the payment approval timestamp

order_delivered_carrier_date: shows the order posting timestamp. When it was handled to the logistic partner.

order_delivered_customer_date: shows the actual order delivery date to the customer

order_estimated_delivery_date: shows the estimated delivery date that was informed to customer at the purchase moment


## 2. Tabel Items (Olist Order Items)

order_id: order unique identifier

order_item_id: sequential number identifying number of items included in the same order

product_id: product unique identifier

seller_id: seller unique identifier

shipping_limit_date: shows the seller shipping limit date for handling the order over to the logistic partner

price: item price

freight_value: item freight value item (if an order has more than one tiem the freight value is splitted between items)


## 3. Tabel Product (Olist Products)

product_id: unique product identifier

product_category_name: root category of product, in Portuguese

product_name_lenght: number of characters extracted from the product name

product_description_lenght: number of characters extracted from the product description

product_photos_qty: number of product published photos

product_weight_g: product weight measured in grams

product_length_cm: product length measured in centimeters

product_height_cm: product height measured in centimeters

product_width_cm: product width measured in centimeters


## 4. Tabel Translation (Product Category Name Translation)

product_category_name: category name in Portuguese

product_category_name_english: category name in English


---

# Hasil Pengecekan Data
1. Tabel order: terdapat missing value di beberapa kolom dengan missing value terbanyak sebanyak 2965 value, namun tidak pada kolom yang akan kita gunakan.
2. Tabel items: tidak terdapat missing value maupun duplikasi data
3. Tabel products: terdapat missing value di beberapa kolom dengan missing value terbanyak sebanyak 610 value. Terdapat juga inkonsistensi di kolom product_category_name.
4. Tabel translation: Terdapat inkonsistensi data.

---

# Hasil Analisis dan Pembahasan
## Objektif 1: Total penjualan dari tiap kategori produk

Dari pemrosesan data pada objektif 1, didapatkan bahwa 5 kategori produk dengan penjualan terbanyak adalah kategori health_beauty, watches_gifts, bed_bath_table, sport_leisure, dan computers_accesories. Sedangkan 5 kategori produk dengan penjualan paling sedikit adalah security_and_services, fashion_childrens_clothes, cds_dvds_musicals, flowers, pc_gamer.

Strategi yang bisa diambil management adalah:

Menaikkan harga dari produk yang penjualannya tinggi untuk mendatangkan nilai penjualan yang lebih besar lagi.

Memberikan diskon untuk produk yang penjualannya rendah supaya pelanggan lebih tertarik membeli.

## Objektif 2: Kategori Produk yang Paling Banyak Dipesan

Dari pemrosesan data pada objektif 2, didapatkan bahwa 5 kategori produk yang paling banyak dipesan adalah kategori bed_bath_table, health_beauty, sport_leisure, furniture_decor, dan computers_accesories. Sedangkan 5 kategori produk dengan pemesanan paling sedikit adalah security_and_services, fashion_childrens_clothes, pc_gamer, la_cuisine, dan cds_dvds_musicals.

Strategi yang bisa diambil management adalah:

Melakukan bundling antara produk yang jarang dipesan dengan produk yang sering dipesan untuk lebih mengenalkan produk-produk yang jarang dipesan ke pelanggan.

Mengurangi stok atau memberhentikan penjualan produk yang sangat jarang dipesan dan dianggap kurang menguntungkan.

## Objektif 3: Pertumbuhan Pemesanan 10 Produk yang Paling Diminati di Tahun 2018

Dari pemrosesan data pada objektif 3, didapatkan produk auto memiliki kenaikan pemesanan pada bulan 2 kemudian terus-menerus turun. Sedangkan produk health_beauty cukup konsisten naik.

Hal yang dapat dilakukan management:

Menyelidiki penyebab lonjakan pemesanan produk tertentu pada bulan tertentu, maupun penyebab kenaikan konsisten dari produk tertentu. Strategi yang diterapkan pada momen tersebut dapat diulangi untuk periode selanjutnya.

Menyelidiki penyebab penurunan pemesanan produk tertentu pada bulan tertentu, maupun penyebab penurunan konsisten dari produk tertentu. Strategi dari produk yang mengalami kenaikan pemesanan dapat diterapkan pada produk yang mengalami penurunan pemesanan.

---

# Penutup
Tentunya analisis masih bisa diperdalam lagi untuk mendapatkan insight yang lebih jelas. Misalnya, menganalisis apakah produk yang dipesan ini pasti sampai ke pelanggan, lokasi toko yang paling laris menjual produk tertentu, dsb. Hal ini bisa dieksplorasi di analisis berikutnya.
