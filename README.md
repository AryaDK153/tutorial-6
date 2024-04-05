# Tutorial 6 - Main Menu and GUI
## Tutorial Mandiri: Fitur Tambahan
### Tombol Kembali ke Menu Utama dari Scene Game Over
Untuk menunjukkan bahwa pemain kalah, kita perlu menunjukkan scene Game Over. Pada umumnya, setelah kalah, kita ingin dapat memulai kembali permainan, sehingga dibutuhkan tombol untuk kembali ke menu utama yang berisi tombol New Game. Tombol kembali kali ini dibuat sebagai berikut:

1. Menambahkan LinkButton dan menyesuaikan text, color, font, serta ukuran;
2. Refactor script yang digunakan untuk tombol New Game yang telah dibuat sebelumnya. Pada tiap signal yang menggunakan script tersebut, diubah receivernya menjadi "_on_LinkButton_pressed," sehingga tidak perlu membuat script baru tiap membuat node LinkButton;
3. Cantumkan script pada LinkButton untuk kembali ke main menu yang telah dibuat, atur signal agar menunjuk "_on_LinkButton_pressed," dan masukkan "MainMenu" pada exported variable "Scene to Load."

### Stage Select Scene
Ide yang digunakan adalah apabila memasuki level melalui pilihan ini, nyawa ketika mulai pasti ulang dari 3. Dari ide tersebut juga muncul kesadaran bahwa belum ada mekanisme reset untuk jumlah life yang dimiliki player. Maka langkah pembuatan fitur ini adalah sebagai berikut:

1. Refactor mekanisme life untuk selalu reset menjadi 3 ketika memasuki scene main menu;
2. Membuat scene baru yang berisi LinkButton bertuliskan angka-angka yang merepresentasikan level-level yang dapat dipilih. Tidak lupa LinkButton untuk kembali ke main menu;
3. Cantumkan script dan masukkan nama "Scene to Load" yang bersesuaian, misal untuk LinkButton yang bertuliskan "1" maka "Scene to Load" bernama "Level 1"