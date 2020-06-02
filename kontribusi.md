# Kontribusi Penulisan Buku

Buku ini akan bisa terwujud jika komunitas berpartisipasi dan bergotong royong untuk menyelesaikan
pembuatan buku ini. Oleh karena itu, kami mendorong anda untuk berkontribusi. Dokumen ini
menjelaskan berbagai hal yang terkait dengan kontribusi tersebut.

## Lisensi

Anda harus paham bahwa jika anda berkontribusi, berarti kontribusi anda akan masuk dalam buku dengan
lisensi CC-BY-SA Internasional 4.0. Implikasinya bisa dilihat pada bagian [README.md](README.md).

## Persiapan

Untuk berkontribusi, setidaknya anda harus paham:
1.  Rust (tentu saja)
2.  Git. Semua kontribusi dilakukan dengan mengirimkan *Pull Request*
3.  AsciiDoc - khususnya dengan menggunakan [Asciidoctor](https://asciidoctor.org).

## Kontribusi

Semua isi teks Asciidoc ada di direktori [isi](isi/). Sesuaikan dengan nama file yang di *include* pada file [pemrograman-rust.adoc](pemrograman-rust.adoc). Selain itu, ada beberapa hal yang perlu dipahami.

### Jika kontribusi anda mengandung gambar

* Letakkan gambar di direktori [gambar](gambar/) sesuai dengan bab yang anda buat. Jika belum ada direktori untuk bab, silahkan dibuat dengan ketentuan penamaan `bab-nn` dengan `nn` adalah angka bab (misal `bab-01` jika untuk `Bab 1`).
* Pada dokumen Asciidoc, gunakan `image::bab-01/web-rust-lang-org.png[]` untuk menampilkan gambar.

### Jika kontribusi anda mengandung kode sumber

* letakkan kode sumber tersebut di direktori [src](src/) sesuai dengan bab yang anda buat. JIka belum ada direktori untuk bab, silahkan dibuat dengan ketentuan penamaan `bab-nn` dengan `nn` adalah angka bab (misal `bab-01` jika untuk `Bab 1`).
* Pada dokumen Asciidoc, gunakan kode sumber berikut:

```
[source,rust]
----
include::../{sourcedir}/bab-01/ferris/src/main.rs[]
----
<1> Penjelasan 1
<2> Penjelasan 2
```

**Catatan**: 

1.  Bagian yang penting di atas adalah `/bab-01/ferris/src/main.rs` yang menunjukkan letak dari kode sumber yang anda acu.
2.  Asciidoc memungkinkan adanya *callout*, gunakan jika anda ingin menjelaskan baris tertentu.
3.  Usahakan setiap satu kode sumber yang cukup kompleks, dibuat lengkap menggunakan `cargo`. Pada saat mengirimkan *pull request*, `cargo clean` lebih dulu setelah anda pastikan bisa berjalan dengan baik. Hapus direktori `.git` pada proyek cargo tersebut.

