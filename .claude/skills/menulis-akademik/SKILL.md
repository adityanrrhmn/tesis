---
name: menulis-akademik
description: Panduan gaya menulis akademik Bahasa Indonesia yang manusiawi & bebas pola AI (anti AI-slop) untuk naskah tesis. WAJIB dibaca sebelum menulis atau menyunting teks naskah apa pun (.tex atau markdown) — berisi daftar frasa terlarang, pola struktur terlarang, dan uji cepat sebelum menyerahkan tulisan.
---

# Gaya Menulis Akademik Manusiawi (Anti AI-Slop)

Tujuan: teks yang terbaca seperti ditulis peneliti manusia — punya sudut pandang, ritme bervariasi, dan presisi — bukan keluaran generatif generik. Naskah tesis berbahasa Indonesia baku (PUEBI), nada akademis, sitasi natbib.

## 1. Frasa TERLARANG (penanda khas AI)

- Pembuka klise: "Dalam era digital yang terus berkembang", "Seiring dengan pesatnya perkembangan teknologi", "Di zaman modern ini", "Dewasa ini" sebagai pembuka bab/paragraf.
- Pengisi kosong: "penting untuk dicatat bahwa", "tidak dapat dipungkiri bahwa", "tentunya", "pada dasarnya" (tanpa fungsi), "sejatinya", "yang mana".
- Superlatif tanpa data: "sangat signifikan", "revolusioner", "luar biasa", "berkembang sangat pesat" — ganti dengan angka/bukti bersitasi atau netralkan.
- Pola terjemahan Inggris: "Bukan hanya X, tetapi juga Y" berulang-ulang; "Mari kita telusuri"; "Bayangkan sebuah dunia di mana...".
- Penutup kosong: "demikianlah pembahasan...", kalimat rangkuman yang hanya mengulang kalimat topik.

## 2. Pola struktur TERLARANG

- Tiga poin simetris terus-menerus (rule of three di hampir tiap paragraf).
- Rantai transisi formula: "Selain itu... Selanjutnya... Di sisi lain... Kemudian..." — transisi harus lahir dari logika argumen (sebab, kontras, konsesi), bukan stok kata.
- Bullet/numbering untuk hal yang seharusnya prosa argumentatif. Di naskah tesis, daftar berbutir hanya untuk enumerasi sejati (langkah prosedur, spesifikasi).
- Panjang kalimat seragam. Variasikan dengan sengaja: kalimat pendek menekankan. Kalimat panjang dipakai ketika hubungan sebab-akibat antara beberapa konsep memang perlu dirangkai dalam satu tarikan napas.
- Paragraf 1–2 kalimat beruntun (gaya blog). Paragraf akademik utuh: kalimat topik → pengembangan/bukti bersitasi → kaitan ke argumen besar.
- Bolak-balik "Pertama, ... Kedua, ... Ketiga, ..." di luar konteks yang benar-benar enumeratif.

## 3. Yang HARUS ada

- Setiap klaim faktual → `\citep{}`; setiap angka → sumber atau hasil sendiri (rujuk bab/tabel/gambar).
- Pola argumen: klaim → bukti → implikasi ke penelitian INI. Jangan berhenti di "banyak peneliti telah meneliti X" — katakan apa artinya bagi rumusan masalah kita.
- Sudut pandang: posisikan penelitian terhadap literatur ("Berbeda dengan X yang berfokus pada..., penelitian ini...").
- Istilah teknis konsisten: ikuti GLOSARIUM.tex; istilah asing `\textit{}` atau `\gls{}`; satu konsep satu istilah.
- Kata baku: analisis (bukan analisa), metode (bukan metoda), praktik, risiko, sistem, teknik, objek, subjek; "memengaruhi" (bukan mempengaruhi), "mengubah" (bukan merubah).

## 4. Uji cepat sebelum selesai (jalankan selalu)

1. **Uji portabilitas**: adakah kalimat yang bisa dipindahkan ke tesis orang lain tanpa terasa janggal? → terlalu generik; tulis ulang dengan konteks spesifik penelitian ini.
2. **Uji pembuka paragraf**: adakah ≥2 paragraf berdekatan dibuka kata/frasa sama? → variasikan.
3. **Uji sitasi**: adakah klaim faktual yang 2 kalimat terakhirnya tanpa \citep dan bukan hasil sendiri? → tambah sitasi atau `% TODO: butuh sitasi`.
4. **Uji ritme**: baca dalam hati; monoton = tanda slop; pecah/gabung kalimat.
5. **Uji daftar**: setiap bullet yang bisa dijadikan kalimat mengalir → jadikan prosa.
