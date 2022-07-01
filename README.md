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

-Function Name |Role Name| Security| Create Function

DynamoDB

-Create table | table name |primary key |create table

-Explore items|create item |

Lambda+DynamoDB

-lambda function |test

-test |create event name |template (hello-world)|save &test |cek status 200

-cek dynamodb | table | explore item

API Gateway

-Klik nama API | klik ANY | Klik TEST

-Isi method POST | Request body - pakai file API-Gateway-POST-Test

-Klik Test |Cek status 200

-cek dynamodb | table | explore item

