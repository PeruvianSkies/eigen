- ### Definisi DevOps
DevOps berasal dari dua suku kata, Development dan Operations, secara garis besar DevOps adalah serangkaian praktik yang menggabungkan antara Development (Dev) dan Operations (Ops) yang bertujuan untuk memperpendek siklus perubahan dari sebuah system atau pengembangan system serta menyediakan pengiriman berkelanjutan dengan menggunakan software continuous integration seperti Jenkins yang biasa saya gunakan.

- ### Infrastructure as a Code
Saya akan melakukan konsep infrastructure as a code menggunakan tools Terraform yang mana sarana tersebut membuat infrastruktur dengan aman dan efisien menggunakan sebuah baris code yang bisa dipastikan bahwa beberapa server yang didefinisikan memiliki konfigurasi yang sama, kemudian saya akan menggunakan monitoring tools seperti Datadog untuk memantau seluruh infrastruktur server beserta jaringan nya, tools monitoring memberikan pandangan menyeluruh tentang kinerja dari semua server dalam infrastruktur jika terjadi kegagalan pada salah satu server maka bisa ditangani dengan cepat.

- ### Security Topologi
Saya akan mengkonfigurasikan network inbound protocol pada server private agar hanya bisa di akses dari salah satu server. Serta membuka hanya port-port tertentu dan source inbound yang memang di butuhkan oleh server tersebut.

- ### DB Migrate
Modul ORM yang pernah saya gunakan adalah sequelize, langkah pertama pastikan bahwa sequelize sudah terinstall pada server database baru, kemudian jalankan sequelize init untuk membuat 4 direktori konfigurasi, (config, models, migrations, seeders), sebelum melanjutkan proses migrasi database konfigurasikan terlebih dahulu file config.json pada direktori config, untuk menentukan user, DB host, DB name, dan DB yang digunakan. pastikan bahwa user dan nama DB pada file config sama dengan yang ada pada DB server. kemudian konfigurasikan sesuai kebutuhan migrasi pada file migration di dalam direktori migration. Pastikan file models pada direktori models sudah dibuat. Jalankan migrasi pada server baru dengan perintah sequelize db:migrate, cek kembali migrasi yang sudah dijalankan, jika terdapat kegagalan lakukan undo migration dengan perintah sequelize db:migrate:undo atau jika memang ingin undo dengan file yang spesifik bisa menggunakan perintah db:migrate:undo --to path/to/migration/file.js (contoh migrasi MySQL yang pernah saya lakukan https://github.com/PeruvianSkies/Devops-week2/tree/master/Backend-Server).

- ### [CI/CD Gitlab](cicd-gitlab)

- ### [Migration Services](migration-service)