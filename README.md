# AWS-Latihan
Membuat S3

*Create New Bucket

-Buat Nama Bucket (unik diseluruh dunia, sesuai nama domain),region

-Object ownership (ACLs Enabled)

-Unthick block all public access

*Klik Nama bucket

-1. bagian object

-upload file | permission - grant public permission access

-2. bagian properties

-Pilih  Static web hosting |edit |enabled

-isi index.html

ROute 53

-DNS Management (created hosted zone)

-Domain name (sesuai nama domain dan bucket s3)

-public hosted zone

-create record | aktifkan alias | pilih s3 endpoint | region | s3 endpoint

Lambda

-Create function | Use blueprint | microservice-http-endpoint

-Function Name |Role Name| REST API|Security-open| Create Function

DynamoDB

-Create table | table name |primary key |create table

-Klik Nama table |Action|Create item

-Explore items|cek hasil

Lambda+DynamoDB

-lambda function |test

-test |create event name |template (hello-world)|save &test |cek status 200

-cek dynamodb | table | explore item

API Gateway

-Klik nama API | klik ANY | Klik TEST

-Isi method POST | Request body - pakai file API-Gateway-POST-Test

-Klik Test |Cek status 200

-cek dynamodb | table | explore item


Akses API dari luar

-API Gateway |Klik nama API | Action |Deploy API

-Deployment Stage - New | Stage name -test|Stage description |Deployment description -versi 1 inisialisasi |Deploy

-expand bagian Stage -test |pilih POST | copy invoke URL

-dari commandline pakai file cURL-command-line-POST-test

-Tambahkan diakhir baris invoke URL

-paste dan jalankan di command prompt

-cek dynamodb | table | explore item

Menyambungkan API dengan Aplikasi Web

-API Gateway |stages | test|post |invoke URL

-edit index.html |tambahkan di bagian form-action dengan invoke URL

-upload index.html bersama bundle.js ke S3

-buka website |masih ada eror TypeError: Failed to fetch (karena mengaktifkan CORES, dan browser menolak cross-origin), solusi membolehkan cross-origin

-ke lambda |pilih function |code |bagian headers tambahkan "Access-Control-Allow-Origin : '*'"

-Cek aplikasi web

