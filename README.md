# Data Uji Penerjemahan Mesin Bahasa Indonesia

Ini adalah gudang penyimpanan data yang dikhususkan untuk proyek penelitian dan pengembangan teknologi penerjemahan mesin dari dan ke bahasa Indonesia (GARENG). Hanya data uji yang tersimpan di sini. Data latih yang digunakan masih bersifat privat dan belum dapat dibuat publik dengan alasan perizinan.

Proyek penelitian dan pengembangan sistem penerjemahan mesin GARENG adalah kerjasama antara [Rekanalar](http://rekanalar.com) dan [Beritagar](https://beritagar.id).

### Isi

Data uji yang terdapat dalam gudang penyimpanan ini diperoleh dari transkripsi TED Talks dan sejumlah sumber pemberitaan daring nasional dan internasional. Saat ini data yang disediakan adalah pasangan paralel kalimat berbahasa Inggris dan Indonesia. Untuk bahasa-bahasa lain akan ditambahkan seiring pengembangan lanjutan sistem.

Data uji sebanyak 10.000 pasang kalimat tersebut bertopik umum seperti pemberitaan nasional dan internasional, politik, ekonomi, olah raga, hiburan, kesehatan, dan teknologi.

Semua data yang ada di sini berformat teks dan bersifat mentah. Dalam direktori `outputs` adalah hasil sejumlah sistem penerjemahan mesin terhadap data yang terdapat di direktori `data`. Data dalam sub-direktori `gareng` adalah hasil sistem penerjemahan mesin GARENG dan sebagai pembanding data pada sub-direktori `gnmt` adalah hasil sistem penerjemahan mesin Google Neural Machine Translation.

### Penilaian

Penilaian terhadap hasil penerjemahan mesin dilakukan dengan menggunakan program `multi-bleu.pl` yang juga disertakan dalam direktori `scripts`. Informasi lebih lanjut mengenai penilaian BLEU dapat dibaca pada [laman ini](https://en.wikipedia.org/wiki/BLEU).

Program tokenisasi sederhana `tokenizer.py` juga disertakan dalam direktori `scripts` untuk memecah kalimat menjadi sejumlah token (unit yang lebih kecil).

#### Bahasa Inggris ke Bahasa Indonesia

| Sistem   | campur     | huruf kecil |
| -------- |:---------- |:----------- |
| GNMT     | 59.14      | 59.99       |
| GARENG   | **61.48**  | **62.35**   |

#### Bahasa Indonesia ke Bahasa Inggris

| Sistem   | campur     | huruf kecil |
| -------- |:---------- |:----------- |
| GNMT     | 66.90      | 67.43       |
| GARENG   | **68.50**  | **69.00**   |

