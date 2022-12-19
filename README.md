# Ujian Akhir Semester 
<br>Mata Kuliah 	: Dasar Pemograman
<br> Nama		: Riza Anwar Fadil
<br>NIM		:	1227050116
<br>Jurusan		:[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
<br> Pada Source code kali ini terdapat 2 program. program pertama yaitu transpose matriks. pada program kedua yaitu menentukan nilai yang bisa dibagi 3 5 dan 7.

## Source Code
	#include <iostream>
	using namespace std;

	int main()
	{

		int i, j, m, n, matriks[10][10], transpose[10][10];
		cout<<"---------------------------------------"<<endl;
		cout<<" Nama : Riza Anwar Fadil "<<endl;
		cout<<"---------------------------------------"<<endl;

		cout<<" No 1. Program transpose Matrik "<<endl;

		cout << "Masukkan jumlah baris matriks: ";
		cin >> m;
		cout << "Masukkan jumlah kolom matriks: ";
		cin >> n;
		cout<<endl;
		cout << "Masukkan elemen matriks\n";
		for (i = 0; i < m; i++){
			for (j = 0; j < n; j++){
				 cout <<"baris ke-"<<i+1<<", kolom ke-"<<j+1<<" : ";
				cin  >> matriks[i][j];
			}
		}
		cout << endl;

		cout<<" Hasil matrik : "<<endl;
		for (i = 0; i < m; i++){
			for (j = 0; j < n; j++){
				cout << matriks[i][j] << "  ";
			}
			cout << endl;
		}
		cout << endl;

		for (i = 0; i < m; i++){
			for (j = 0; j < n; j++){
				transpose[j][i] = matriks[i][j];
			}
		}

		cout << "Hasil Transpose Matriks: \n";
		for (i = 0; i < n; i++){
			for (j = 0; j < m; j++){
				cout << transpose[i][j] << "\t";
			}
			cout << endl;
		}

		cout<<endl<<endl;
		cout<<" No 2 Program mengecek nilai yang habis dibagi 3,5, dan 7 "<<endl;
		int data[10][10];

		cout << "Masukkan jumlah baris : ";
		cin >> m;
		cout << "Masukkan jumlah kolom : ";
		cin >> n;
		cout<<endl;
		cout << "Masukkan elemen array\n";
		for (i = 0; i < m; i++){
			for (j = 0; j < n; j++){
				 cout <<"baris ke-"<<i+1<<", kolom ke-"<<j+1<<" : ";
				cin  >> data[i][j];
			}
		}
		cout << endl;
		cout<<" Nilai yang di inputkan : "<<endl;
		for (i = 0; i < m; i++){
			for (j = 0; j < n; j++){
				cout << data[i][j] << "\t";
			}
			cout << endl;
		}
		cout << endl;

		bool kondisi= true;
		cout<<" Nilai yang habis dibagi 3, 5 dan 7 dari array diatas : "<<endl;
		for (int i=0; i<m; i++ ) {
			for (int j=0; j<n; j++) {
				if (data[i][j]%3==0 && data[i][j]%5==0 && data[i][j]%7==0) {
					cout<<data[i][j];
					cout<<endl;
					kondisi= false;
				}

			}
		}

		if (kondisi) {
			cout<<" tidak ada bilangan yang habis dibagi 3, 5 dan 7. "<<endl;
		}

		return 0;
	}

## Output
<br>---------------------------------------
<br> Nama : Riza Anwar Fadil
<br>---------------------------------------
<br> No 1. Program transpose Matrik
<br>Masukkan jumlah baris matriks: 2
<br>Masukkan jumlah kolom matriks: 3
<br>
<br>Masukkan elemen matriks
<br>baris ke-1, kolom ke-1 : 5
<br>baris ke-1, kolom ke-2 : 3
<br>baris ke-1, kolom ke-3 : 6
<br>baris ke-2, kolom ke-1 : 3
<br>baris ke-2, kolom ke-2 : 2
<br>baris ke-2, kolom ke-3 : 8
<br>
<br> Hasil matrik :
<br>5  3  6
<br>3  2  8
<br>
<br>Hasil Transpose Matriks:
<br>5       3
<br>3       2
<br>6       8
<br>
<br>
<br> No 2 Program mengecek nilai yang habis dibagi 3,5, dan 7
<br>Masukkan jumlah baris : 2
<br>Masukkan jumlah kolom : 3
<br>
<br>Masukkan elemen array
<br>baris ke-1, kolom ke-1 : 105
<br>baris ke-1, kolom ke-2 : 23
<br>baris ke-1, kolom ke-3 : 56
<br>baris ke-2, kolom ke-1 : 210
<br>baris ke-2, kolom ke-2 : 34
<br>baris ke-2, kolom ke-3 : 23
<br>
<br> Nilai yang di inputkan :
<br>105     23      56
<br>210     34      23
<br>
<br> Nilai yang habis dibagi 3, 5 dan 7 dari array diatas :
<br>105
<br>210
