# Menyunting dokumen

Dokumen boleh disunting terus di dalam pemapar. Skrin penyuntingan mempunyai "paparan visual", iaitu anda menyunting apa yang anda lihat, dan "paparan sumber Markdown"; satu butang menukar antara keduanya.

## Mula menyunting

Tekan salah satu daripada yang berikut. Kesemuanya membuka skrin penyuntingan yang sama.

- [Edit] di bahagian bawah kanan teks
- [⋯] (Tindakan lain) di bahagian atas kanan teks → [Edit]
- Menu item INDEX → [Edit]

## Menyunting

1. Sunting teks secara terus.
   Pada bar alat di bahagian atas skrin penyuntingan, anda boleh menggunakan format perenggan (teks badan, tajuk 1–4, petikan, kod), [Tebal], [Condong], [Senarai berbulet], [Senarai bernombor], [Pautan], [Sisip jadual], [Saiz imej], [Buat asal] dan [Buat semula].
2. Apabila anda mahu menyunting sumber Markdown secara terus, tekan [Markdown].
   Tekan sekali lagi untuk kembali ke paparan visual. Paparan yang digunakan kali terakhir akan diingati dan dipulihkan apabila anda menekan [Edit] pada kali berikutnya.
3. Tekan [Simpan].
   Fail Markdown ditulis dan paparan kembali ke mod bacaan. Tekan [Batal] apabila anda mahu berhenti.

> **Nota**
>
> - Menyimpan hanya menulis ke fail sahaja. Pementasan dan komit Git tidak dilakukan secara automatik.
> - Rumus matematik dan rajah seperti Mermaid, TikZ dan Vega-Lite dipaparkan sebagai hasil lakaran dalam paparan visual. Untuk menukar kandungannya, beralih ke [Markdown].
> - Dokumen yang mengandungi sintaks khusus MDX (komponen, `import` dan sebagainya) disunting dalam paparan Markdown sahaja, bagi mengekalkan sintaks tersebut.
> - Front matter (tetapan yang diapit oleh `---` di bahagian atas) dikekalkan walaupun disunting dalam paparan visual.

> **Petua**
>
> - Apabila anda menekan [Buka dalam VS Code], fail dibuka dalam editor teks biasa. Apabila anda menyimpan dalam editor teks, paparan pemapar turut dikemas kini secara automatik.
> - Apabila anda tidak mahu butang [Edit] dipaparkan, matikan [Butang edit] dalam [Tetapan paparan]. Untuk menyembunyikannya bagi keseluruhan projek, tetapkan `editor.showEditButton` dalam `lunascape-docs.json` kepada `false`.
> - Paparan lalai yang dibuka pada mulanya (visual atau Markdown) boleh ditukar melalui tetapan `lunascapeDocEditor.editor.defaultMode` atau `editor.defaultMode` dalam `lunascape-docs.json`.

## Topik berkaitan

- [Mencipta dan menyusun dokumen dan folder](organize.md)
- [Melaraskan saiz imej](images.md)
- [Menulis rumus matematik](math.md)
- [Menulis rajah dan carta](diagrams.md)
