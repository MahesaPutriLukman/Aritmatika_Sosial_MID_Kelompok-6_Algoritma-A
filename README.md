# Aritmatika

Aritmatika adalah package Python yang berfungsi untuk menyelesaikan masalah aritmatika sosial seperti untung dan rugi, bunga, pajak, diskon dan rabat, serta bruto, netto, dan tara. 


Aritmatika is a Python Package for dealing with social arithmetic problems such as profit and loss, interest, tax, discount and rebate, and also gross, net, and tare. 

## Installation

Gunakan package manager [pip](https://pip.pypa.io/en/stable/) untuk menginstall aritmatika.

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install aritmatika.

bash
pip install aritmatika


## Usage

'''python

from aritmatika.gaji import (
    hitung_gaji_pokok,
    hitung_gaji_bersih,
    hitung_gaji_lembur,
    hitung_total_gaji,
    hitung_rata_rata_gaji
)

'''return gaji_per_jam * jam_kerja'''

gaji_pokok = hitung_gaji_pokok(gaji_per_jam, jam_kerja)

'''return gaji_pokok - potongan_pajak - potongan_bpjs - potongan_lain'''

gaji_lembur = hitung_gaji_lembur(jam_lembur, tarif_lembur)

'''return jam_lembur * tarif_lembur'''

gaji_bersih = hitung_gaji_bersih(gaji_pokok, potongan_pajak, potongan_bpjs)

'''gaji_pokok + gaji_lembur + tunjangan'''

total_gaji = hitung_total_gaji(gaji_pokok, gaji_lembur, tunjangan)

'''

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/
