# Synchronous-vs-Asynchronous
1. Penjelasan Synchronous

Synchronous adalah situasi di mana dua atau lebih kegiatan atau proses terjadi secara bersamaan dalam waktu yang sama atau secara real-time.

2. Asynchronous

Asynchronous adalah komunikasi yang secara tertunda atau online tidak langsung dengan memakai media, seperti e-mail, forum dan membaca atau menulis dokumen online melalui WWW (World Wide Web). Asynchronous juga merupakan proses komunikasi data yang tak terikat waktu tetap dan proses transformasi data kecepatan yang cukup relatif serta tidak tetap.

3. Perbedaan Synchronous dan Asynchronous

Metode pembelajaran sinkron (synchronous) dan asinkron (asynchronous) terutama berbeda dalam hal cara informasi disampaikan, interaksi siswa-guru, dan fleksibilitas waktu.


 

1. Waktu Interaksi

   - Synchronous: Memerlukan waktu interaksi yang langsung antara guru dan peserta didik dalam waktu yang sama. Bisa berupa kuliah langsung, diskusi video secara real-time, atau juga kelas virtual.

   - Asynchronous: Memungkinkan peserta didik untuk mengakses materi pembelajaran, tugas dan diskusi kapan saja sesuai dengan kebutuhan dan ketersediaan mereka sendiri.

 

2. Waktu dan Tempat

   - Synchronous: Terjadi pada waktu dan tempat yang sudah ditentukan sebelumnya. Peserta didik harus hadir tepat waktu dan mungkin memerlukan akses internet yang stabil untuk mengikuti sesi pembelajaran.

   - Asynchronous: Memberikan fleksibilitas waktu dan tempat kepada peserta didik. Mereka dapat mengakses materi pembelajaran dan berpartisipasi dalam diskusi kapan saja dan di mana saja selama mereka memiliki akses ke platform pembelajaran yang sesuai.

 

3. Interaksi dan Respon

   - Synchronous: Interaksi antara peserta didik dan guru terjadi secara langsung dan respon cepat bisa didapatkan, diskusi dan pertanyaan dijawab secara real-time.


   - Asynchronous: Memungkinkan peserta didik untuk memproses materi dan berpartisipasi dalam diskusi sesuai dengan kecepatan dan jadwal mereka sendiri. Respon mungkin tidak segera didapatkan, tetapi peserta didik meiliki lebih banyak waktu untuk merenungkan materi dan merumuskan tanggapan yang baik.


 

4. Tingkat keterlibatan

- Synchronous : Dapat meningkatkan Tingkat keterlibatan karena interaksi langsung antara

guru dan peserta didik, diskusi yang terjadi secara langsung juga

meningkatkan keterlibatan.

-Asynchronous : Memerlukan lebih banyak inisiatif dari peserta didik untuk tetap terlibat dalam

pembelajaran. Namun, fleksibilitas waktu yang lebih besar dapat membantu peserta didik mengatur waktu mereka dengan lebih baik agar fokus ke pembelajaran.


4. Berikan contoh 

1. Synchronous (Sinkron / Waktu Nyata)
Interaksi dilakukan pada waktu yang bersamaan atau real-time, meskipun peserta berada di tempat yang berbeda.
• Contoh dalam komunikasi/pembelajaran:
	• Rapat daring menggunakan Zoom atau Google Meet.
	• Panggilan telepon langsung.
	• Mengobrol lewat pesan instan secara langsung (live chat).
	• Kelas tatap muka di dalam kelas fisik.
• Kelebihan: Respon didapat seketika (instant feedback) dan diskusi berjalan hidup.
• Kekurangan: Terikat jadwal yang ketat dan butuh koneksi internet stabil.

2. Asynchronous (Asinkron / Tidak Serempak)
Interaksi dilakukan secara tertunda; pemberi pesan dan penerima pesan tidak harus berada di waktu yang sama.
• Contoh dalam komunikasi/pembelajaran:
	• Mengirim dan membalas E-mail.
	• Mengakses modul PDF, slide materi, atau video rekaman pembelajaran di LMS (Learning Management System).
	• Berdiskusi melalui forum komentar atau bulletin board.
	• Menitipkan pesan lewat project management software (seperti Trello/Notion).
• Kelebihan: Waktu lebih fleksibel dan bisa belajar/bekerja mandiri sesuai kecepatan masing-masing.
• Kekurangan: Respon terhadap pertanyaan bisa tertunda dan butuh kemandirian tinggi.

5. Tiga Cara Menulis Kode Asynchronous di JavaScript

Ada tiga cara untuk mencapai hal ini: callback, Promise, dan async/await.

1.Panggilan balik
Cara pertama dan tertua untuk menulis kode JavaScript asinkron adalah dengan menggunakan callback. Callback adalah fungsi asinkron yang diteruskan sebagai argumen ke fungsi lain saat Anda memanggilnya. Ketika fungsi yang Anda panggil selesai dieksekusi, fungsi tersebut akan "memanggil kembali" fungsi callback.

function ambilData(callback) {
  setTimeout(() => {
    callback("Data berhasil diambil");
  }, 2000);
}

ambilData(function(data) {
  console.log(data);
});

2.Janji
Cara kedua untuk menulis kode JavaScript asinkron adalah dengan Promises. Promises adalah fitur yang lebih baru, diperkenalkan ke JavaScript dengan spesifikasi ES6 . Fitur ini menyediakan cara yang sangat mudah untuk menangani kode JavaScript asinkron. Inilah salah satu alasan mengapa banyak pengembang JavaScript, jika bukan hampir semua, mulai menggunakannya sebagai pengganti callback.

const data = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve("Data berhasil diambil");
  }, 2000);
});

data
  .then((hasil) => {
    console.log(hasil);
  })
  .catch((error) => {
    console.log(error);
  });


3.Asinkron/tunggu
Opsi terakhir untuk menulis kode JavaScript asinkron adalah dengan menggunakan async/await. Async/await diperkenalkan di ES8. Async/await terdiri dari dua bagian. Bagian pertama adalah sebuah asyncfungsi. Fungsi async ini dieksekusi secara asinkron secara default. Nilai yang dikembalikannya adalah Promise baru.

function ambilData() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Data berhasil diambil");
    }, 2000);
  });
}

async function tampilkanData() {
  const hasil = await ambilData();
  console.log(hasil);
}

tampilkanData();