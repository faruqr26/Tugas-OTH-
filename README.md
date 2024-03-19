# laporanTugas-OTH- (KARTU)

kartu :

SS CODE : 
![image](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/d1ba40bd-ed85-4129-b120-d432576ea081)
![image](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/2f7c5e17-5a3e-4587-8740-e12cbe8affe0)
![image](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/6d378a47-de7a-4631-8dc6-9eda1f29afef)

SS OUTPUT : 
![image](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/bdfec2ea-ac74-4831-b18e-132669a1532a)

PENJELASAN CODE : 
1.#include <stdio.h> // Library standar input-output

2.#include <stdlib.h> // Library standar untuk alokasi memori dinamis

3.#include <string.h> // Library standar untuk operasi string

4.// Fungsi untuk mendapatkan nilai angka dari kartu
  int getCardValue(char card) 
5.if (card == 'J') return 11; // Kartu Jack memiliki nilai 11

6.else if (card == 'Q') return 12; // Kartu Queen memiliki nilai 12

7.else if (card == 'K') return 13; // Kartu King memiliki nilai 13

8.else if (card == '1') return 10; // Kartu 10 memiliki nilai 10

9.else return (int)(card - '0'); // Konversi karakter angka ke nilai integer

10.// Fungsi untuk menampilkan urutan kartu
 void printCards(char *cards, int length) 
 for (int i = 0; i < length; i++) 
11.printf("%c ", cards[i]); // Mencetak kartu ke layar

12,printf("\n"); // Pindah baris

13.// Fungsi untuk mengurutkan kartu
 int sortCards(char *cards, int length) 
 
14.int swaps = 0; // Jumlah pertukaran kartu
 for (int i = 0; i < length - 1; i++) 
 
15.int min_idx = i; // Indeks kartu minimum
 for (int j = i; j < length; j++) 
 
16.// Konversi kartu ke nilai angka untuk membandingkan
 if (getCardValue(cards[j]) < getCardValue(cards[min_idx])) 
 
17.min_idx = j; // Update indeks kartu minimum
 if (min_idx != i)
 char temp = cards[i];
 cards[i] = cards[min_idx]; // Tukar kartu
 cards[min_idx] = temp;
 
18.swaps++; // Tambah jumlah pertukaran
 printf("Pertukaran %d : ", swaps);
 
19.printCards(cards, length); // Cetak urutan kartu setelah pertukaran

20.return swaps; // Mengembalikan jumlah pertukaran
 int main() {
 int n;
 
21.printf("Masukkan jumlah kartu: "); // Menampilkan pesan untuk pengguna

22.scanf("%d", &n); // Meminta jumlah kartu dari pengguna

23.char cards[n]; // Deklarasi array kartu
 printf("Masukkan nilai kartu (1-10, J, Q, K): ");
 for (int i = 0; i < n; i++) 
 
24.scanf(" %c", &cards[i]); // Meminta nilai kartu dari pengguna

25.int swaps = sortCards(cards, n); // Mengurutkan kartu dan mendapatkan jumlah pertukaran

26.printf("\nJumlah minimal langkah pertukaran: %d\n", swaps); // Menampilkan jumlah pertukaran minimal

27.free(cards); // Melepaskan memori yang dialokasikan untuk array kartu

28.return 0; // Mengembalikan 0 sebagai kode keluaran yang menandakan program berakhir tanpa kesalahan


    





    


