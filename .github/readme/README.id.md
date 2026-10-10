<p align="center">
  <img src="../../logo.png" alt="i-have-adhd" width="140" />
</p>
<p align="center">
  <strong align="center">Respons yang ramah bagi kamu yang memiliki ADHD. Tanpa perlu diagnosis!</strong>
</p>
<p align="center">
  <a href="../../LICENSE"><img src="https://img.shields.io/github/license/ayghri/i-have-adhd?style=flat" alt="Lisensi"></a>
</p>

<p align="center">
  <a href="../../README.md" title="English" aria-label="English">🇬🇧</a> ·
  <a href="README.zh-CN.md" title="简体中文" aria-label="简体中文">🇨🇳</a> ·
  <strong title="Bahasa Indonesia" aria-label="Bahasa Indonesia">🇮🇩</strong> ·
  <a href="README.ja.md" title="日本語" aria-label="日本語">🇯🇵</a> ·
  <a href="README.vi.md" title="Tiếng Việt" aria-label="Tiếng Việt">🇻🇳</a> ·
  <a href="README.ko.md" title="한국어" aria-label="한국어">🇰🇷</a> ·
  <a href="README.fa.md" title="فارسی" aria-label="فارسی">🇮🇷</a> ·
  <a href="README.th.md" title="ภาษาไทย" aria-label="ภาษาไทย">🇹🇭</a>
</p>


## Instalasi

🔗 [Panduan Instalasi](../install/INSTALL.id.md)

## Apa Fungsinya Sii?

Sebuah skill untuk asisten coding-mu yang mencegahnya mengubur jawaban di tengah teks. Aksi di awal. Langkah bernomor. Tanpa basa-basi seperti "Semoga membantu!"


## Apa yang Berubah??


<table>
<tr>
<td width="50%">

## Sebelumnya

> Pertanyaan bagus! Biarkan saya memikirkan ini. Alur autentikasi Anda memiliki beberapa bagian yang terlibat: middleware, verifikasi token, dan penanganan cookie. Melihat `src/auth.ts`, fungsi `verifyToken` (sekitar baris 42-58) sepertinya menggunakan API lama dari `jsonwebtoken`. Salah satu pendekatannya adalah memperbarui paket dan menulis ulang fungsi tersebut. Setelah perubahan, Anda perlu menjalankan tes autentikasi untuk memastikan tidak ada yang rusak. Ngomong-ngomong, mungkin ada baiknya meninjau ulang versi dependensi Anda secara keseluruhan. Semoga membantu! Beri tahu saya jika Anda ingin mendalami lebih lanjut.

</td>
<td width="50%">

## Sesudahnya

> Validasi token di `src/auth.ts:42` sudah diperbaiki dan tes autentikasi sudah dijalankan.
>
> Terverifikasi: 18 tes lulus. Dependensi lama diparkir; hal itu tidak menghalangi perbaikan ini.

</td>
</tr>
</table>


## Perilakunya

Teks lengkap ada di [SKILL.md](../../skills/i-have-adhd/SKILL.md).

1. Kerjakan tugas yang dapat dilakukan agen dengan aman, bukan mengembalikannya sebagai daftar instruksi.
2. Tampilkan jawaban, hasil, rekomendasi, atau hambatan terlebih dahulu.
3. Buat tindakan pertama yang harus dilakukan pengguna menjadi kecil dan konkret.
4. Pertahankan satu set kerja yang terlihat: sekarang, berikutnya, dan diparkir.
5. Pulihkan konteks setelah interupsi tanpa mengulang seluruh riwayat.
6. Rekomendasikan satu pilihan bawaan sebelum menampilkan alternatif.
7. Bedakan kemajuan terverifikasi, kegagalan, dan hal yang belum diketahui.
8. Perkirakan waktu hanya jika membantu keputusan dan jelaskan ketidakpastiannya.
9. Akhiri dengan satu langkah berikutnya hanya jika benar-benar diperlukan.

## Sesuaikan (Kustomisasi)

Lakukan fork, edit `skills/i-have-adhd/SKILL.md`, dan ganti dengan salinan Anda sendiri:

```bash
claude plugin uninstall i-have-adhd            # hapus salinan upstream terlebih dahulu:
claude plugin marketplace remove i-have-adhd   # fork dan upstream menggunakan nama yang sama
claude plugin marketplace add <username-anda>/i-have-adhd
claude plugin install i-have-adhd@i-have-adhd
```

Mulai ulang Claude Code dan panggil `/i-have-adhd` lagi.

## Kredit

Terinspirasi secara bebas dari *The Adult ADHD Tool Kit* karya J. Russell Ramsay dan Anthony L. Rostain. Diadaptasi untuk cara LLM seharusnya merespons, bukan untuk cara seseorang mengatur harinya.

## Lisensi

MIT.

Beri ⭐ jika ini menyelamatkanmu dari harus menggulir layar melewati satu lagi "Pertanyaan bagus!"
