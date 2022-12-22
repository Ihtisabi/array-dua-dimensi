# Ujian Akhir Semester 
<pre>Mata Kuliah :Dasar Pemograman
<br>Nama        :Suci Ihtisabi Hida Nursyifa
<br>NIM         :1227050129
<br>Jurusan     :Teknik Informatika</pre>
<br>[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/)</pre>

## Matriks (Array 2 Dimensi)
Array dua dimensi terdiri dari beberapa baris dan kolom elemen yang bertipe variabel sama. Bentuk dari array ini seperi matriks atau tabel. Penomoran indeks dari array dua dimensi ini menggunakan dua buah angka yang disimpan dalam tanda kurung siku.
<pre>
int A[2][3] = ( {1,2,3} 
                {4,5,6} )
</pre>
<table>
  <tr>
    <td>        </td>
    <td>indeks 0</td>
    <td>indeks 1</td>
    <td>indeks 2</td>
  </tr>
    <td>indeks 0</td>
    <td>1</td>
    <td>2</td>
    <td>3</td>
  <tr>
    <td>indeks 1</td>
    <td>4</td>
    <td>5</td>
    <td>6</td>
  </tr>
</table>
Array dua dimensi A memiliki 2 elemen baris dan 3 dengan total seluruh elemennya adalah 6 (2*3). Dalam array dua dimensi, penomoran indeks yang pertama adalah elemen baris dan yang kedua adalah kolom. Angka yang berada pada penomoran indeks menunjukkan kepada jumlah elemennya, yaitu nilai indeks+1. Untuk mengakses setiap element array, penulisan indeks juga harus ditulis 2 kali, seperti contoh berikut:
<pre>
indeks (0,0) = 1
indeks (0,1) = 2
indeks (0,2) = 3
indeks (1,0) = 4
indeks (1,1) = 5
indeks (1,2) = 6
</pre>



## Source Code
Input nilai array, merubah dimensi array, elemen array dan nilai array habis dibagi 3,5,7
```c++
//PROGRAM INPUT JUMLAH DIMENSI DAN NILAI ARRAY
#include <iostream>
#include <conio.h>
using namespace std;

int main () {
	int array[100][100];
	int baris, kolom, i, j;
 
	cout << "Input jumlah baris array: ";
	cin >> baris;
 
	cout << "Input jumlah kolom array: ";
	cin >> kolom;
	cout << endl;
 
	for(i = 0; i < baris ; i++){
    	for(j = 0; j < kolom; j++){
      	cout << "Baris " <<i+1<<", kolom "<<j+1<< " = ";
      	cin >> array[i][j];//menginput nilai elemen pada indeks array
    	}
    cout << endl;
  	}
 
  	cout << "Hasil array: \n";
  	for(i = 0; i < baris ; i++){
    	for(j = 0; j < kolom; j++){
      	cout << array[i][j] << "\t";
    	}
    cout << endl;
  	}
	cout<<endl;


//PROGRAM MENUKAR DIMENSI ARRAY
	cout<<"Hasil tukar kolom dan baris: \n";
	for (i=0;i<baris;i++) {
		for (j=0;j<kolom;j++) {
			cout<<array[j][i]<<"\t";//merubah kolom menjadi baris dan sebaliknya
		}
	cout<<endl;
	}
	
  
 //PROGRAM MEMANGGIL ELEMEN ARRAY
	int k=0;
	int array2[100];
	for (int i=0; i<baris; i++) {
		for (int j=0; j<kolom; j++) {
			array2[k]= array[i][j];//merubah array dua dimensi menjadi satu dimensi
			k++;
		}
	}
	
	int s=baris*kolom;//proses untuk menghilangkan duplikasi nilai elemen
	for(k=0;k<s-1;k++) {
		for(int y=k+1;y<s;y++) {
			if(array2[k]==array2[y]) {
				for(int z=y;z<s;z++) {
					array2[z]=array2[z+1];
				}
			s--;
			y--;
			}
		}
	}
	
	cout<<"\nElemen array:";
 	for(k=0;k<s;k++) {
        cout<<array2[k]<<" ";//memanggil setiap satu elemen array yang berbeda (bilangan yang bernilai sama hanya di tampilkan salah satunya) 
	}
  
  
 //PROGRAM BILANGAN ARRAY HABIS DIBAGI 3, 5, DAN 7
	cout<<"\n\nBilangan yang habis dibagi 3,5, dan 7:";
	cout<<"\nBilangan habis dibagi (3) :  ";
	for (k=0;k<s;k++) {
		if (array2[k]%3==0) {
			cout<<array2[k]<<" ";
		}
	}
	
	cout<<"\nBilangan habis dibagi (5) :  ";
	for (k=0;k<s;k++) {
		if (array2[k]%5==0) {
			cout<<array2[k]<<" ";
		}
	}
	
	cout<<"\nBilangan habis dibagi (7) :  ";
	for (k=0;k<s;k++) {
		if (array2[k]%7==0) {
			cout<<array2[k]<<" ";
		}
	}
	
	getch ();
}
```
## Output
 ![UAS no 1 cpp - Executing - Dev-C++ 12_22_2022 4_38_38 AM](https://user-images.githubusercontent.com/118999021/209021360-5aff2278-70bb-4ede-85a3-72df2a5506de.png) 
 ![array2](https://user-images.githubusercontent.com/118999021/209021389-85386bb0-7984-470a-a8c3-2b62f6dd76ee.png)
