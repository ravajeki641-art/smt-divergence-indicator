# SMT Divergence Reversal & Continuation Indicator

Indikator TradingView Pine Script untuk mengidentifikasi **SMT (Swing Point Momentum Trading) Divergence** berdasarkan Model Fraktal yang mirip dengan metodologi **TTraders_edu**.

## 📌 Deskripsi

Indikator ini hanya menampilkan sinyal ketika ada **Bias Pembalikan (Reversal)** atau **Bias Kelanjutan (Continuation)** yang jelas, berdasarkan urutan pembentukan swing point antara:
- **Aset Utama** (yang sedang Anda perdagangkan)
- **Aset Korelasi** (pasangan atau instrumen yang bergerak bersama)

**Tidak ada sinyal random** — hanya sinyal yang memiliki struktur valid.

## 🎯 Logika Indikator

### Bullish Reversal SMT
- Aset utama membentuk **swing low BARU** yang lebih rendah
- Aset korelasi **sudah membuat swing low duluan** (lebih awal)
- Ini menunjukkan potensi **pembalikan bullish** karena belum ada konfirmasi penuh dari aset korelasi

### Bullish Continuation SMT
- Aset korelasi membuat **swing low DULUAN** terlebih dahulu
- Aset utama **kemudian membuat swing low** juga dengan arah yang sama
- Ini menunjukkan potensi **kelanjutan bullish** karena mengikuti arah aset korelasi

### Bearish Reversal SMT
- Aset utama membentuk **swing high BARU** yang lebih tinggi
- Aset korelasi **sudah membuat swing high duluan** (lebih awal)
- Ini menunjukkan potensi **pembalikan bearish**

### Bearish Continuation SMT
- Aset korelasi membuat **swing high DULUAN**
- Aset utama **kemudian membuat swing high** dengan arah yang sama
- Ini menunjukkan potensi **kelanjutan bearish**

## ⚙️ Parameter Input

| Parameter | Default | Keterangan |
|-----------|---------|-----------|
| **Swing Length** | 5 | Jumlah bar kiri dan kanan untuk deteksi pivot |
| **Correlated Asset** | NQ1! | Simbol aset korelasi (misal: ES1!, EURUSD, BTCUSD) |
| **Min Bars Between Pivots** | 10 | Bar minimum antara pivot events |
| **Show Labels** | true | Tampilkan label sinyal di chart |
| **Highlight Background** | true | Warna background saat sinyal aktif |

## 🎨 Warna Sinyal

- 🟢 **Hijau (Lime)** = Bullish Reversal
- 🔵 **Biru** = Bullish Continuation
- 🔴 **Merah** = Bearish Reversal
- 🟠 **Orange** = Bearish Continuation

## 📊 Contoh Penggunaan

### Setup 1: Futures Correlation
- **Main Chart:** ES1! (E-mini S&P 500)
- **Correlated Asset:** NQ1! (E-mini Nasdaq 100)
- **Timeframe:** 15M - 1H

### Setup 2: Forex Correlation
- **Main Chart:** EURUSD
- **Correlated Asset:** GBPUSD
- **Timeframe:** 5M - 30M

### Setup 3: Crypto Correlation
- **Main Chart:** BTCUSD
- **Correlated Asset:** ETHUSD
- **Timeframe:** 1M - 15M

## 🚀 Cara Menggunakan

1. **Copy code** dari file `smt_divergence_indicator.pine`
2. **Buka TradingView** → Chart → Pine Script Editor → New Script
3. **Paste code** dan klik "Add to Chart"
4. **Sesuaikan Parameter:**
   - Ganti simbol korelasi sesuai kebutuhan
   - Atur swing length sesuai timeframe
   - Aktifkan/nonaktifkan labels dan background
5. **Set Alert** untuk notifikasi real-time

## ⚡ Alert Notifications

Indikator ini memiliki 4 jenis alert:
- ⬆️ Bullish Reversal SMT
- ⬆️ Bullish Continuation SMT
- ⬇️ Bearish Reversal SMT
- ⬇️ Bearish Continuation SMT

## 📖 TTraders_edu Methodology

Metodologi ini terinspirasi dari **TTraders_edu** — sebuah educational platform yang fokus pada:
- **Fractal Model Analysis** — mengidentifikasi pola fraktal di pasar
- **Multi-Asset Correlation** — membandingkan aset yang bergerak bersama
- **Swing Point Structure** — menganalisis pembentukan swing point untuk prediksi arah
- **Confluence Trading** — menggunakan multiple confluence untuk sinyal yang lebih kuat

## 💡 Tips Trading

1. **Gunakan dengan Timeframe yang Konsisten** — jangan ganti timeframe tiba-tiba
2. **Konfirmasi dengan Volume & Price Action** — jangan hanya mengandalkan indikator
3. **Pair yang Tepat Penting** — pilih aset yang benar-benar berkorelasi tinggi
4. **Gabungkan dengan Supply/Demand Zone** — untuk entry yang lebih presisi
5. **Manajemen Risiko** — selalu gunakan stop loss yang ketat

## ⚠️ Disclaimer

Indikator ini adalah alat bantu analisis teknis dan **bukan rekomendasi trading**. Selalu lakukan:
- Backtesting sebelum trading live
- Risk management yang ketat
- Analisis fundamental & teknis yang menyeluruh

## 📝 License

Bebas digunakan untuk keperluan trading personal. Tidak boleh dijual kembali tanpa izin.

## 🔗 Resources

- [TradingView Pine Script Documentation](https://www.tradingview.com/pine-script-docs/)
- [Understanding Swing Points](https://en.wikipedia.org/wiki/Swing_(finance))
- [Fractal Analysis](https://www.investopedia.com/terms/f/fractal.asp)

---

**Dibuat untuk:** Trading dengan logika Fractal & Multi-Asset Correlation  
**Update Terakhir:** October 2026
