# Aritmatika

Aritmatika adalah package Python yang berfungsi untuk menyelesaikan masalah aritmatika sosial seperti untung dan rugi, bunga, pajak, diskon dan rabat, serta bruto, netto, dan tara.

Aritmatika is a Python Package for dealing with social arithmetic problems such as profit and loss, interest, tax, discount and rebate, and also gross, net, and tare.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install aritmatika.

```bash
pip install aritmatika
```

## Penggunaan
#### 1. Fungsi Gaji

```python
from aritmatika import gaji

# Menghitung gaji pokok
gaji_pokok = gaji.hitung_gaji_pokok(50000, 40)
print(f"Gaji pokok: {gaji_pokok}")

# Menghitung gaji bersih
gaji_bersih = gaji.hitung_gaji_bersih(2000000, 500000, 300000)
print(f"Gaji bersih: {gaji_bersih}")

# Menghitung gaji lembur
gaji_lembur = gaji.hitung_gaji_lembur(5, 75000)
print(f"Gaji lembur: {gaji_lembur}")

# Menghitung total gaji
total_gaji = hitung_total_gaji(1000000, 200000, 500000)
print(f"Total gaji karyawan: {total_gaji}")

# Menghitung rata-rata gaji
list_gaji = [5000000, 6000000, 4500000, 5500000]
rata_rata_gaji = hitung_rata_rata_gaji(list_gaji)
print(f"Rata-rata gaji karyawan: {rata_rata_gaji}")
```

#### 2. Fungsi Bruto-Tara-Netto

```python
from aritmatika import bruto_tara_netto

# Menghitung bruto
bruto = bruto_tara_netto.hitung_bruto(500, 50)
print(f"Bruto: {bruto}")

# Menghitung netto
netto = bruto_tara_netto.hitung_netto(550, 50)
print(f"Netto: {netto}")
```

#### 3. Fungsi Pajak

```python
from aritmatika import pajak

# Menghitung PPN
ppn = pajak.ppn(1000000)
print(f"PPN: {ppn}")

# Menghitung PPH
pph = pajak.hitung_pph(120000000, 'lajang', 0)
print(f"PPH: {pph}")
```

#### 4. Fungsi Bunga

```python
from aritmatika import bunga

# Menghitung bunga tunggal
bunga_tunggal = bunga.bunga_tunggal(1000000, 0.05, 2)
print(f"Bunga tunggal: {bunga_tunggal}")

# Menghitung bunga majemuk
bunga_majemuk = bunga.bunga_majemuk(1000000, 0.05, 12, 2)
print(f"Bunga majemuk: {bunga_majemuk}")
```

#### 5. Fungsi Rabat dan Diskon

```python
from aritmatika import rabat_diskon

# Menghitung harga setelah diskon
harga_diskon = rabat_diskon.hitung_diskon(200000, 10)
print(f"Harga setelah diskon: {harga_diskon}")

# Menghitung rabat
total_setelah_rabat = rabat_diskon.hitung_rabat(50000, 10, 5)
print(f"Total setelah rabat: {total_setelah_rabat}")
```

#### 6. Fungsi Untung dan Rugi

```python
from aritmatika import untung_rugi

# Menghitung untung
untung = untung_rugi.hitung_untung(10000, 15000)
print(f"Keuntungan: {untung}")

# Menghitung persentase keuntungan
persen_untung = untung_rugi.persentase_untung(10000, 15000)
print(f"Persentase keuntungan: {persen_untung}%")
```
## Dokumentasi Fungsi

#### 1. Fungsi Gaji

##### `hitung_gaji_pokok(gaji_per_jam, jam_kerja)`
- **Deskripsi**: Menghitung gaji pokok berdasarkan jam kerja.
- **Parameter**:
  - `gaji_per_jam` (*float*): Gaji per jam.
  - `jam_kerja` (*float*): Total jam kerja.
- **Return**: Gaji pokok yang dihasilkan.

##### `hitung_gaji_bersih(gaji_pokok, potongan_pajak, potongan_bpjs, potongan_lain=None)`
- **Deskripsi**: Menghitung gaji bersih setelah potongan pajak, BPJS, dan potongan lainnya.
- **Parameter**:
  - `gaji_pokok` (*float*): Gaji pokok.
  - `potongan_pajak` (*float*): Potongan pajak.
  - `potongan_bpjs` (*float*): Potongan BPJS.
  - `potongan_lain` (*float*, opsional): Potongan lain-lain.
- **Return**: Gaji bersih setelah potongan.

##### `hitung_gaji_lembur(jam_lembur, tarif_lembur)`
- **Deskripsi**: Menghitung gaji lembur berdasarkan jam lembur dan tarif lembur per jam.
- **Parameter**:
  - `jam_lembur` (*float*): Jumlah jam lembur.
  - `tarif_lembur` (*float*): Tarif lembur per jam.
- **Return**: Total gaji lembur.

##### `hitung_total_gaji(gaji_pokok: float, gaji_lembur: float, tunjangan: float)`
- **Deskripsi**: Menghitung total gaji berdasarkan gaji pokok, gaji lembur, dan tunjangan.
- **Parameter**:
  - `gaji_pokok` (*float*): Gaji pokok.
  - `gaji_lembur` (*float*): Gaji lembur.
  - `tunjangan` (*float*): Tunjangan.
- **Return**: Total gaji.

##### `hitung_rata_rata_gaji(list_gaji: list)`
- **Deskripsi**: Menghitung rata-rata gaji berdasarkan list gaji.
- **Parameter**:
  - `list_gaji` (*list*): List gaji.
- **Return**: Rata-rata gaji.

#### 2. Fungsi Bruto-Tara-Netto

##### `hitung_bruto(netto, tara)`
- **Deskripsi**: Menghitung bruto berdasarkan netto dan tara.
- **Parameter**:
  - `netto` (*float*): Berat bersih suatu barang.
  - `tara` (*float*): Berat kemasan barang.
- **Return**: Berat bruto barang.

##### `hitung_netto(bruto, tara)`
- **Deskripsi**: Menghitung netto dari bruto dan tara.
- **Parameter**:
  - `bruto` (*float*): Berat kotor suatu barang.
  - `tara` (*float*): Berat kemasan barang.
- **Return**: Berat netto barang.

#### 3. Fungsi Pajak

##### `ppn(transaksi, tarif_ppn=0.11)`
- **Deskripsi**: Menghitung Pajak Pertambahan Nilai (PPN) berdasarkan nilai transaksi.
- **Parameter**:
  - `transaksi` (*float*): Nilai transaksi.
  - `tarif_ppn` (*float*, opsional): Tarif PPN (default 11% atau 0.11).
- **Return**: Nilai PPN.

##### `hitung_pph(gaji_tahunan, status, tanggungan)`
- **Deskripsi**: Menghitung Pajak Penghasilan (PPH) berdasarkan gaji tahunan, status, dan tanggungan.
- **Parameter**:
  - `gaji_tahunan` (*float*): Total gaji tahunan.
  - `status` (*str*): Status wajib pajak (contoh: 'lajang', 'kawin').
  - `tanggungan` (*int*): Jumlah tanggungan.
- **Return**: Jumlah PPH yang harus dibayar.

#### 4. Fungsi Bunga

##### `bunga_tunggal(p, r, t)`
- **Deskripsi**: Menghitung bunga tunggal berdasarkan pokok, suku bunga, dan periode waktu.
- **Parameter**:
  - `p` (*float*): Pokok pinjaman.
  - `r` (*float*): Suku bunga per periode (dalam desimal, contoh 5% ditulis 0.05).
  - `t` (*float*): Waktu (periode dalam tahun).
- **Return**: Nilai bunga yang dihasilkan.

##### `bunga_majemuk(p, r, n, t)`
- **Deskripsi**: Menghitung bunga majemuk dengan penggabungan bunga setiap periode.
- **Parameter**:
  - `p` (*float*): Pokok pinjaman.
  - `r` (*float*): Suku bunga per periode (dalam desimal).
  - `n` (*int*): Frekuensi penggabungan bunga per periode.
  - `t` (*float*): Waktu (periode dalam tahun).
- **Return**: Total (pokok + bunga) yang dihasilkan.

#### 5. Fungsi Rabat & Diskon

##### `hitung_diskon(harga_awal, diskon_persen)`
- **Deskripsi**: Menghitung harga setelah diskon.
- **Parameter**:
  - `harga_awal` (*float*): Harga sebelum diskon.
  - `diskon_persen` (*float*): Persentase diskon.
- **Return**: Harga setelah diskon.

##### `hitung_rabat(harga_per_barang, jumlah_barang, rabat_persen)`
- **Deskripsi**: Menghitung harga total setelah rabat.
- **Parameter**:
  - `harga_per_barang` (*float*): Harga per barang.
  - `jumlah_barang` (*int*): Jumlah barang.
  - `rabat_persen` (*float*): Persentase rabat.
- **Return**: Total harga setelah rabat.

#### 6. Fungsi Untung & Rugi

##### `hitung_untung(harga_beli, harga_jual)`
- **Deskripsi**: Menghitung keuntungan dari transaksi jual beli.
- **Parameter**:
  - `harga_beli` (*float*): Harga beli barang.
  - `harga_jual` (*float*): Harga jual barang.
- **Return**: Keuntungan yang diperoleh.

##### `persentase_untung(harga_beli, harga_jual)`
- **Deskripsi**: Menghitung persentase keuntungan.
- **Parameter**:
  - `harga_beli` (*float*): Harga beli barang.
  - `harga_jual` (*float*): Harga jual barang.
- **Return**: Persentase keuntungan.

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)

