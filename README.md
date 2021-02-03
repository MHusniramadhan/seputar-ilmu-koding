# seputar-ilmu-koding
c++

#include<time.h>
#include<iostream>
#include<conio.h>
#include<windows.h>

using namespace std;
int main() {
 
 int pil;
cout << "======= NAMA : MUHAMAD HUSNI RAMADHAN =========="<<endl<<endl;
cout << "======= NIM  : 191011400011           =========="<<endl<<endl;
cout << "======= (PROGRAM SORTING DATA ARRAY) =========="<<endl<<endl;
cout << "1. INSERT DATA ARRAY" <<endl;
cout << "2. INSERTION SORT" <<endl;
cout << "3. SELECTION SORT" <<endl;
cout << "4. BUBBLE SORT" <<endl;
cout << "5. EXIT" <<endl<<endl;
cout << "==============================="<<endl<<endl;

cout << "Masukan pilihan anda = "; cin >> pil;

switch(pil) {
	case 1:
 system("cls");
 cout << "INSERT DATA ARRAY";
 cout <<endl<<"============="<<endl;
 cout<<endl;
 
 
 int arr[5], i, elem, pos, tot;
    cout<<"JUMLAH DATA ARRAY: ";
    cin>>tot;
    cout<<"MASUKAN "<<tot<<" DATA Array : "<<endl;
    for(i=0; i<tot; i++)
        cin>>arr[i];
    cout<<"\nSUSUNAN ARRAY:\n";
    for(i=0; i<tot; i++)
        cout<<arr[i]<<"  ";
   
	
 cout<<endl;
break;
//////////////////////////////////////////////////////////

///////     Insertion start               /////////

////////////////////////////////////////////////


 
 case 2:
 system("cls");
 cout << "INSERTION SORT";
 cout <<endl<<"============="<<endl;
 cout<<endl;
 int t3,t4;
 
 int Key;
 int array1[5];

 cout<<"Masukan 5 angka : "<<endl;

for(int i=0; i<5; i++)  {
 cout << "  angka ke " <<i+1 <<" = ";cin>>array1[i];
}

cout<<endl;
t3=GetTickCount();
cout<<"Angka sebelum di sortir = ";

for(int j=0; j<5; j++) {
 cout<<array1[j]<<"  ";
 
}

cout<<endl;
cout<<endl<< "Data proses "<<endl;
for(int j=1 ; j < 5 ; j++) {
 Key = array1[j];              
 int i = j-1;                  
 while(i >= 0 && array1[i] < Key) {
  array1[i + 1] = array1[i];
  i = i - 1;
 }
 array1[i + 1] = Key;
 
 for(int l=0; l<5; l++) {
  cout<<array1[l]<<"  ";
  
 }
 cout<<endl;
}
cout<<endl<<"Angka setelah disortir = ";

for(int i=0; i<5; i++) {
 cout<<array1[i]<<"  ";
 
}
t4=GetTickCount();
cout << endl<<endl <<"Lama proses = " << (int)(t4 - t3) << " ms";
 cout<<endl;

 break;
 
 
 
////////////////////////////////////////////////////////

//////////////   Selection start /////////////////////

///////////////////////////////////// 
 
 
 case 3:
 system("cls");
 cout << "SELECTION SORT";
 cout <<endl<< "================="<<endl<<endl;
 int t5,t6;
int mini,temp;

cout<<"masukan 5 angka ="<<endl;

for(int i=0; i<5; i++) {
 cout << "  angka ke " <<i+1 <<" = ";cin>>arr[i];
}
t5=GetTickCount();
cout<<endl;
cout<<"Angka sebelum di sortir = ";

for(int j=0; j<5; j++) {
 cout<<arr[j]<<"  ";
 
}

for(int r1=0;r1<4;r1++) {
 mini=r1;
 for(int r2=r1+1; r2<5; r2++)
   if(arr[r2]>arr[mini])
   mini=r2;
    if(mini !=r1) {
     temp=arr[r1];
     arr[r1]=arr[mini];
     arr[mini]=temp;
    }
}
cout<<endl;
cout<<endl;
cout<<"Setelah di sortir = ";
for(int q=0; q<5; q++) {
 cout<<arr[q]<< "  " ;
 
}
t6=GetTickCount();
cout << endl<<endl <<"Lama proses = " << (int)(t6 - t5) << " ms";
 cout<<endl;
 break;
 
 ////////////////////////////////////

 ////  Buble start /////////////

 ////////////////////////

 case 4:
 system("cls");
 cout << endl;
 cout << "BUBBLE SORT"<<endl;
 cout << "=============="<<endl;
 
 int t7,t8;
 
    int hold;
 int array[5];

 cout<<"Masukan 5 angka :"<<endl;

 for(int i=0; i<5; i++) {
  cout << "  angka ke " <<i+1 <<" = ";cin>>array[i];
 }
 cout<<endl;
 cout<<endl;
 t7=GetTickCount();
 cout<<"Sebelum di sortir = ";

 for(int j=0; j<5; j++) {
 cout<<array[j];
 cout<<"  ";
 }
 
 cout<<endl;
 
 cout <<endl<< "Urutan program"<<endl;
 for(int i=0; i<4; i++) {
  for(int j=0; j<4; j++) {
   if(array[j]<array[j+1]) {
    hold=array[j];
    array[j]=array[j+1];
    array[j+1]=hold;
    
    for(int i=0; i<5; i++) {
  cout<<array[i]<<"  ";
  }
  cout<<endl;
   }
  
  
  }
  
 }
cout<<endl;
 cout<<"Setelah di sortir = ";

 for(int i=0; i<5; i++) {
  cout<<array[i]<<"  ";
 }
    cout<<endl;
 t8=GetTickCount();
 cout << endl <<"Lama proses = " << (int)(t8 - t7) << " ms";
 cout<<endl;
 
 break;


 


//////////////////////////////////////////

//////          EXIT   /////////

////////////////////////////////////////// 
 default:
 system("cls");
 cout << "EXIT";
 break;
 
}   
 
 
 
 getch();
}
