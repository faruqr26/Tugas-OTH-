# LAPORANTUGAS OTH (CATUR)

2.CATUR : 

SS CODE : 

  ![Cuplikan layar 2024-03-19 223258](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/1c66b499-693c-4fbd-adcb-aae8438e4904)
  ![Cuplikan layar 2024-03-19 223311](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/8f772a1f-6957-4885-a11c-a0ac7415daab)


SS OUTPUT : 
  ![Cuplikan layar 2024-03-19 223238](https://github.com/faruqr26/Tugas-OTH-/assets/163359023/ac39a90f-cdc5-4fc2-9bf3-7ea3534813ef)


  PENJELASAN CODE : 
1. #include <stdio.h> // Library standar input-output

2. // Fungsi untuk mengecek apakah posisi (x, y) valid pada papan catur 
    int isValid(int x, int y) 

3.return (x >= 0 && x < 8 && y >= 0 && y < 8); // Mengembalikan 1 jika posisi valid, 0 jika tidak

4.// Fungsi untuk menandai semua langkah yang mungkin dilakukan oleh kuda pada papan catur
    void koboImaginaryChess(int i, int j, int size, int *chessBoard) 

5.// Langkah-langkah yang mungkin dilakukan oleh kuda
    int movesX[] = {2, 1, -1, -2, -2, -1, 1, 2};
    int movesY[] = {1, 2, 2, 1, -1, -2, -2, -1};

6.// Menandai setiap langkah yang mungkin dilakukan oleh kuda
   for (int k = 0; k < 8; k++) 
   int nextX = i + movesX[k];
   int nextY = j + movesY[k];
   if (isValid(nextX, nextY)) 
   
7.*(chessBoard + nextX * size + nextY) = 1; // Menandai langkah kuda dengan nilai 1
    int main() {
    int i, j;
    
8. scanf("%d %d", &i, &j); // Membaca input posisi i dan j

9.int size = 8; // Ukuran papan catur
    
10.int chessBoard[size][size]; // Array 2D untuk papan catur

11.// Inisialisasi papan catur dengan nilai awal 0
    for (int x = 0; x < size; x++) {
    for (int y = 0; y < size; y++) {
    chessBoard[x][y] = 0;
        
12.koboImaginaryChess(i, j, size, (int *)chessBoard); // Memanggil fungsi untuk menandai langkah kuda

13.// Menampilkan papan catur setelah langkah kuda ditandai
    for (int x = 0; x < size; x++) 
    for (int y = 0; y < size; y++) 
    
14.printf("%d ", chessBoard[x][y]); // Mencetak nilai pada posisi (x, y) papan catur
    
15.printf("\n"); // Pindah baris
    
16.return 0; // Mengembalikan 0 sebagai kode keluaran yang menandakan program berakhir tanpa kesalahan




  


 
