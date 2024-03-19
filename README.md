# laporanTugas-OTH-

kartu :

SS CODE : 
![image](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/d1ba40bd-ed85-4129-b120-d432576ea081)
![image](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/2f7c5e17-5a3e-4587-8740-e12cbe8affe0)
![image](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/6d378a47-de7a-4631-8dc6-9eda1f29afef)

SS OUTPUT : 
![image](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/bdfec2ea-ac74-4831-b18e-132669a1532a)

PENJELASAN CODE : 
#include <stdio.h> // Library standar input-output
#include <stdlib.h> // Library standar untuk alokasi memori dinamis
#include <string.h> // Library standar untuk operasi string
// Fungsi untuk mendapatkan nilai angka dari kartu
int getCardValue(char card) 
if (card == 'J') return 11; // Kartu Jack memiliki nilai 11
else if (card == 'Q') return 12; // Kartu Queen memiliki nilai 12
else if (card == 'K') return 13; // Kartu King memiliki nilai 13
else if (card == '1') return 10; // Kartu 10 memiliki nilai 10
else return (int)(card - '0'); // Konversi karakter angka ke nilai integer
// Fungsi untuk menampilkan urutan kartu
void printCards(char *cards, int length) 
for (int i = 0; i < length; i++) 
printf("%c ", cards[i]); // Mencetak kartu ke layar
printf("\n"); // Pindah baris
// Fungsi untuk mengurutkan kartu
int sortCards(char *cards, int length) 
int swaps = 0; // Jumlah pertukaran kartu
for (int i = 0; i < length - 1; i++) 
int min_idx = i; // Indeks kartu minimum
for (int j = i; j < length; j++) 
// Konversi kartu ke nilai angka untuk membandingkan
if (getCardValue(cards[j]) < getCardValue(cards[min_idx])) 
min_idx = j; // Update indeks kartu minimum
if (min_idx != i)
char temp = cards[i];
cards[i] = cards[min_idx]; // Tukar kartu
cards[min_idx] = temp;
swaps++; // Tambah jumlah pertukaran
printf("Pertukaran %d : ", swaps);
printCards(cards, length); // Cetak urutan kartu setelah pertukaran
return swaps; // Mengembalikan jumlah pertukaran
int main() {
int n;
printf("Masukkan jumlah kartu: "); // Menampilkan pesan untuk pengguna
scanf("%d", &n); // Meminta jumlah kartu dari pengguna
char cards[n]; // Deklarasi array kartu
printf("Masukkan nilai kartu (1-10, J, Q, K): ");
for (int i = 0; i < n; i++) {
scanf(" %c", &cards[i]); // Meminta nilai kartu dari pengguna
int swaps = sortCards(cards, n); // Mengurutkan kartu dan mendapatkan jumlah pertukaran
printf("\nJumlah minimal langkah pertukaran: %d\n", swaps); // Menampilkan jumlah pertukaran minimal
free(cards); // Melepaskan memori yang dialokasikan untuk array kartu
return 0; // Mengembalikan 0 sebagai kode keluaran yang menandakan program berakhir tanpa kesalahan


    





    


