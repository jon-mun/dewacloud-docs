---
sidebar_position: 4
slug: /managing-server-roles-and-features
title: Managing Server Roles & Features
---

# Mengatur Peran dan Fitur Windows melalui Server Manager

[Windows VM](https://docs.dewacloud.com/win-vm/) menyediakan GUI yang kuat dari Windows OS yang dapat diakses melalui [remote desktop protocol](https://docs.dewacloud.com/win-rdp-access/) (RDP). Ini memungkinkan Anda untuk terhubung dan mengelola instance Windows Anda dari jarak jauh, misalnya:

- melalui [Guacamole](https://docs.dewacloud.com/win-rdp-access/#rdp-connection-via-web-client) alat HTML5 langsung di browser Anda
- melalui [klien RD lokal](https://docs.dewacloud.com/win-rdp-access/#rdp-connection-via-local-client) (kredensial yang sesuai untuk pembentukan koneksi dapat ditemukan dalam email yang dikirim setelah pembuatan environment)

Untuk mengkonfigurasi virtual private server Windows via RDP, Server Manager bawaan digunakan. Di bawah ini kami soroti beberapa fungsionalitas dasar yang disediakan:

- [menetapkan peran server](https://docs.dewacloud.com/#set-windows-vm-roles)
- [menambahkan fitur server](https://docs.dewacloud.com/#add-features-to-windows-server-roles)

## Menetapkan Peran Windows VM{#set-windows-vm-roles}

Setelah [terhubung](https://docs.dewacloud.com/win-rdp-access/) ke desktop node yang diperlukan, Anda akan melihat alat **Server Manager** terbuka. Sebagai contoh, mari kita tambahkan peran server baru dengan langkah-langkah berikut.

1. Klik tautan **Add roles and features** yang terletak di halaman utama manager.

![Windows server manager](#)

2. Wizard yang sesuai akan dibuka di window baru dengan beberapa informasi pra-mulai dasar yang ditampilkan, maka periksalah dan klik **Next**.

![Windows add roles](#)

Pada tab _Installation Type_, pilih opsi **Role-based or feature-based installation** dan lanjutkan dengan tombol **Next**.

3. Tab _Server Selection_ akan membantu Anda memilih server yang ingin Anda konfigurasikan (beberapa server dari satu domain Active Directory dapat ditambahkan melalui opsi _Add Servers_ di halaman utama **Server Manager**).

![Windows server select](#)

Pilih yang saat ini dan navigasikan ke tab **Next**.

4. Di dalam tab _Server Roles_, klik pada peran tertentu dari daftar yang tersedia untuk mendapatkan deskripsinya (di bagian kanan jendela) dan centang kotak yang diperlukan untuk mengaktifkan peran yang sesuai.

![Windows server roles](#)

Kami akan menambahkan peran **Web Server (IIS)** sebagai contoh dan melanjutkan dengan mengelola fiturnya di bagian berikutnya.

## Menambahkan Fitur ke Peran Windows Server{#add-features-to-windows-server-roles}

Tergantung pada peran server yang dipilih sebelumnya, Anda dapat mengaktifkan beberapa fitur server tambahan yang melekat padanya.

1. Setelah pemilihan peran, Anda akan ditampilkan jendela pop-up yang berisi daftar alat manajemen peran yang tidak wajib (Anda dapat mengaktifkan atau menonaktifkan instalasi mereka dengan kotak centang di bawah).

![Windows add features](#)

Tekan tombol **Add Features**.

2. Selama beberapa langkah wizard berikutnya (tergantung peran yang dipilih), Anda dapat mengelola beberapa fitur tambahan. Untuk itu, bacalah detail peran yang dipilih dan tentukan layanan yang diperlukan untuk mereka.

![Windows role services](#)

Selesaikan konfigurasi Anda dan klik **Next**.

3. Pada tab _Confirmation_ terakhir, periksa konfigurasi yang telah Anda tentukan sebelumnya dan klik **Install** jika semuanya sudah benar.

![Windows install roles and features](#)

4. Instalasi akan dimulai secara otomatis. Anda dapat menunggu hingga selesai atau menutup jendela saat ini dan melanjutkan pekerjaan lainnya, sementara proses ini akan selesai di latar belakang.

![Windows roles and features installed](#)

5. Setelah instalasi selesai, peran baru akan muncul di dashboard **Server Manager**, di mana mereka dapat dengan mudah diakses untuk pelacakan dan penyesuaian parameter tambahan.

![Windows remove roles and features](#)

Anda juga dapat selalu menghapus peran atau fitur kustom dengan bantuan wizard yang sepenuhnya serupa, tersedia melalui opsi **Remove Roles and Features** dalam daftar drop-down dashboard **Manage**.

:::tip
Jika Anda ingin mempelajari lebih lanjut tentang kemungkinan yang tersedia di Windows VM, lihat dokumentasi resmi Windows Server 2008 R2 dan Windows Server 2012.
:::

## Baca Juga{#whats-next}

- [.NET Core (Beta)](https://docs.dewacloud.com/net-core/)
- [Windows VM](https://docs.dewacloud.com/win-vm/)
- [Windows RD Access](https://docs.dewacloud.com/win-rdp-access/)