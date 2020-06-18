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

* Letakkan gambar di direktori [gambar](gambar/) sesuai dengan bab yang anda buat. Jika belum ada direktori untuk bab, silahkan dibuat dengan ketentuan penamaan `xx-yy` dengan `xx` adalah angka bagian dan `yy` adalah angka bab (misal `01-01` jika untuk `Bagian 1 - Bab 1`).
* Pada dokumen Asciidoc, gunakan potongan `asciidoctor` berikut ini untuk menampilkan gambar.

```asciidoc
[#gbr-web-rust]
.Web Peranti Pengembangan Rust
[link=https://www.rust-lang.org]
image::bab-01/web-rust-lang-org.png[]
```

* Jika akan membuat link *cross reference* yang mengacu ke gambar tersebut:

```asciidoc
... Informasi tentang Rust bisa diperoleh di <<#gbr-web-rust>> ...
```

### Jika kontribusi anda mengandung *source code*

* letakkan *source code* tersebut di direktori [src](src/) sesuai dengan bab yang anda buat. JIka belum ada direktori untuk bab, silahkan dibuat dengan ketentuan penamaan `xx-yy` dengan `xx` adalah angka bagian dan `nn` adalah angka bab ke nn pada bagian tersebut (lihat pola penamaan file asciidoc dari [isi](isi/) - misal `01-01` jika untuk `Bagian 1 - Bab ke 1 pada bagian tersebut`. Nama proyek sebaiknya sesuai dengan tujuan proyek.
* Pada dokumen Asciidoc, gunakan *source code* berikut:

```
[source,rust]
----
include::../{sourcedir}/01-01/ferris/src/main.rs[]
----
<1> Penjelasan 1
<2> Penjelasan 2
```

**Catatan**: 

1.  Bagian yang penting di atas adalah `/01-01/ferris/src/main.rs` yang menunjukkan letak dari *source code* yang anda acu.
2.  Asciidoc memungkinkan adanya *callout*, gunakan jika anda ingin menjelaskan baris tertentu.
3.  Usahakan setiap satu *source code* yang cukup kompleks, dibuat lengkap menggunakan `cargo`. Pada saat mengirimkan *pull request*, `cargo clean` lebih dulu setelah anda pastikan bisa berjalan dengan baik atau sertakan [.gitignore](https://github.com/github/gitignore/blob/master/Rust.gitignore). Direktori yang anda kirimkan tersebut bukan direktori yang ada di GitHub - konsekuensinya, tidak ada direktori `.git`.


