# Expert System for Animal Classification

Proyek ini merupakan implementasi sistem pakar sederhana untuk mengklasifikasikan hewan berdasarkan karakteristik biologisnya. Sistem ini dibangun menggunakan pendekatan rule-based (berbasis aturan) dengan bantuan pustaka Python `experta` — turunan dari `CLIPS` untuk inference engine berbasis forward chaining.

## Fitur

- Klasifikasi hewan berdasarkan ciri-ciri seperti bertulang belakang, menyusui, memiliki bulu, bernapas dengan paru-paru, dan lainnya.
- Menentukan jenis hewan seperti mamalia, burung, reptil, ikan, dan amfibi menggunakan aturan yang telah didefinisikan oleh pakar.
- Output berupa nama spesifik dari hewan (contoh: **ikan hiu**, **ular**, **ayam**) berdasarkan aturan inferensi.

## Teknologi dan Library

- `Python 3`
- `experta` (Rule engine)
- `IPython.display` untuk tampilan interaktif dalam notebook

## Struktur Sistem

- **Facts**: Menyimpan input atau pengetahuan yang diperoleh dari pengguna.
- **Rules**: Aturan logika if-then yang menentukan keputusan klasifikasi.
- **Engine**: Forward chaining engine untuk menelusuri rule dan mengklasifikasikan hewan.

## Contoh Aturan

```python
@Rule(Animal(menyusui=True, memiliki_bulu=True))
def classify_mamalia(self):
    self.declare(Fact(hewan='mamalia'))
