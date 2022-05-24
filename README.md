# 🌊TUGAS AKHIR KELOMPOK PEMOS TEAM 20🌊
_Repository_ ini dibuat untuk memenuhi Tugas Akhir Kelompok Praktikum Pemodelan Oseanografi 2022. _Repository_ ini memuat file berupa _script python_ (py) yang digunakan untuk memproses beberapa pemodelan oseanografi seperti Adveksi-Difusi dan Hidrodinamika. Pengerjaan _repository_ ini menggunakan bahasa pemrograman _python_ yang dapat dilakukan pada beberapa _platform_ seperti _Google Collaboratory_ atau _Jupyter Notebook_. _Mandatory library_ yang digunakan kali ini adalah _Numpy, Matplotlib, Python, Sys, Siphon_ dan _Pprint_. Seluruh _script_ yang dibuat adalah hasil Team 20 Oseanografi 2020. Semoga dapat bermanfaat!

## 🙋🏼‍♀️1. AUTHORS (TEAM 20)🙋🏼‍♂️
1. Doding Akka Damanik 26050120120027 A
2. Azalya Besari Noerazzahra Tilaar 26050120130098 A
3. Umar Abdul Aziz 26050120140163 B
4. Clarisa Wulandari 26050120120030 A
5. Ananda Annisa Fitriani 26050120140063 B
6. M. Zanugera Alamsyah 26050120120015 A
7. Olivia Rebeka Vera Wati Sinaga 26050120120028 A

## 🗒️2. CARA PENGGUNAAN SCRIPT🗒️
1. Pengguna dapat membuka folder _Kumpulan Script_ pada _repository_ ini. Di dalamnya terdapat 3 _script_, bisa dibuka salah satu.

   ![1](https://user-images.githubusercontent.com/105897134/169439922-6bd9c427-5733-41fc-80cb-f50c3f0425c6.png)

2. Tampilan _script_ akan muncul seperti gambar di bawah ini. 

   ![2](https://user-images.githubusercontent.com/105897134/169441338-d7256c02-e782-4407-aea9-a395260713d6.png)

3. Script dapat di-_copy_ untuk nantinya dipergunakan dan disesuaikan di _Jupyter Notebook_ maupun _Google Collaboratory._

## 📝3. METODE PENGERJAAN📝
1. Modul 2: Adveksi-Difusi 2 Dimensi
2. Modul 3: Model Hidrodinamika 1 Dimensi Sederhana
3. Modul 4: Model Hidrodinamika 2 Dimensi

### 📒**3.1. Modul 2: Adveksi-Difusi 2 Dimensi**📒

#### 📌Definisi dan Persamaan📌
Adveksi 2 dimensi adalah proses pergerakan substansi atau materi oleh fluida akibat dipengaruhi gaya-gaya tertentu dalam arah vertikal dan horizontal.

![Adveksi 2D](https://user-images.githubusercontent.com/105897134/169457375-a9fa82d8-3b9d-4328-9fe2-c178e3d62e2d.png)

Difusi 2 dimensi adalah proses penyebaran substansi atau materi oleh fluida akibat dipengaruhi gaya-gaya tertentu dalam arah vertikal dan horizontal.

![Difusi 2D](https://user-images.githubusercontent.com/105897134/169457501-c4c608fa-3f05-459d-86ee-3362975ba08c.png)

Persamaan adveksi-difusi merupakan persamaan matematis yang dirancang untuk mempelajari fenomena transpor polutan. Persamaan adveksi-difusi dua dimensi merupakan model matematika yang menggambarkan proses transportasi suatu zat yang dipengaruhi gaya dalam dua dimensi. Persamaannya secara umum sebagai berikut:

![Adveksi-Difusi 2D](https://user-images.githubusercontent.com/105897134/169457432-c04c6964-4144-4fba-8312-d8f416b24cff.png)

#### 📌Metode Diskritisasi Beserta Hasilnya📌
Diskritisasi persamaan adveksi-difusi 2 dimensi menggunakan metode eksplisit upstream dimana persamaan beda hingga dengan metode ini menggunakan pendekatan beda maju untuk turunan waktu, sedangkan untuk turunan ruang dilakukan dengan melihat arah kecepatan _u_.
Jika _u_ > 0, turunan ruang menggunakan beda mundur. Jika _u_ < 0, digunakan pendekatan beda maju. Berikut adalah hasil diskritisasi untuk persamaan adveksi 2 dimensi.

![Diskritisasi Adveksi 2D](https://user-images.githubusercontent.com/105897134/169457504-4f6cd76c-eaed-4a65-8408-53f57042fc0a.png)

Model 2 dimensi untuk mekanisme transpor difusi dapat menggunakan pendekatan beda maju untuk turunan waktu dan beda pusat untuk turunan ruang. Berikut adalah hasil diskritisasi untuk persamaan difusi 2 dimensi.

![Diskritisasi Difusi 2D](https://user-images.githubusercontent.com/105897134/169457506-9fbe396c-701e-44b4-b9c9-5eb6394e468b.png)

Indeks _n_ untuk waktu, indeks _i_ untuk ruang dan koefisien difusi AD dianggap konstan terhadap ruang dan waktu. Berikut ini adalah hasil diskritisasi persamaan adveksi-difusi 2 dimensi.

![Diskritisasi Adveksi-Difusi 2D](https://user-images.githubusercontent.com/105897134/169457505-80ee0398-73f8-4c15-9d86-0d7bbfce05ad.png)

#### 📌Penentuan Nilai Batas dan Syarat Batas📌
Syarat batas merupakan suatu kondisi yang menggambarkan kondisi di batas (ruang maupun waktu) dari model yang dibangun. Syarat batas dari metode eksplisit upstream diberikan pada nilai awal (hulu) dan nilai akhir (hilir).

![Syarat Batas](https://user-images.githubusercontent.com/105897134/169457513-581f12b3-d391-4310-b1a1-71a25c1ec425.png)

#### 📌Saat Iterasi Dihentikan📌
Syarat awal yang digunakan dalam skenario model 2D adveksi-difusi ini adalah dengan memberikan harga 0 di semua titik konsentrasi polutan kecuali di titik-titik sumber yang tersebar dan sumber bersifat tidak kontinu.

![Iterasi](https://user-images.githubusercontent.com/105897134/169457510-64116b16-bf28-4cf3-99eb-7804c56fba14.png)

#### 📌Kriteria Kestabilan📌
Suatu metode untuk menentukan seberapa besar nilai stabilitas dari model yang digunakan.

![Kriteria Kestabilan](https://user-images.githubusercontent.com/105897134/169457512-b6746147-ed68-48e3-bd10-2db4965b62ab.png)

#### 📌Pengerjaan Script📌
1. Memasukkan _mandatory library python matploblib_ untuk memberikan efek visual pada grafik, _numpy_ untuk perhitungan numerik dan _sys_ untuk mengakses konfigurasi interpreter pada saat _runtime_. Memasukkan juga pendefinisian.
```
import matplotlib.pyplot as plt
import numpy as np
import sys
 
def percentage(part, whole):
        percentage = 100 * float(part)/float(whole)
        return str(round(percentage,2)) + "X"

```
2. Selanjutnya, memasukkan parameter perhitungan polutan yang akan digunakan.
```
#Memasukkan Parameter Awal
C = 1.51    #Kecepatan Aliran
ad = 1.51   #Koefisien Difusi
#Arah Arus (Berdasarkan Geographic Convention)
theta = 0  #Skenario I, II, III atau IV
#Parameter Lanjutan
q = 0.95    #Kriteria Kestabilan
x = 500     #Jumlah Grid Horizontal (x)
y = 500     #Jumlah Grid Vertikal (y)
dx = 5      
dy = 5
Tend = 105   #Lama Simulasi
#Tend = 1
dt = 0.5
#Polutan
px = 250   #Polutan pada grid x
py = 235   #Polutan pada grid y
Ic = 1051   #Jumlah Polutan
 
```
3. Kemudian, _script_ perhitungan dibuat untuk mengetahui persebaran polutan.
```
#Perhitungan U dan V ()
u = C * np.sin(theta*np.pi/180)
v = C * np.cos(theta*np.pi/180)
dt_count = 1/((abs(u)/(q*dx))+(abs(v)/(q*dy))+(2*ad/(q*dx*2))+(2*ad/(q*dy*2)))
 
Nx = int(x/dx)      #number of mesh in x direction
Ny = int(y/dy)      #number of mesh in y direction
Nt = int(Tend/dt)   #number of timesteps
#Perhitungan Titik Polutan di Buang
px1 = int(px/dx)
py1 = int(py/dy)
 
#Fungsi disederhanakan
lx = u*dt/dx
ly = v*dt/dy
ax = ad*dt/dx**2
ay = ad*dt/dy**2
cfl = (2*ax + 2*ay + abs(lx) + abs(ly))     #Syarat Kestabilan CFL
#Perhitungan CFL
if cfl >= q:
    print('CFL Violated, Please use dt :'+str(round(dt_count,4)))
    sys.exit()
#%%

```
4. Setelah itu, _script_ pembuatan grid dibuat sebagai alat bantu untuk menyusun atau mengatur hasil _running_ polutan.
```
#Pembuatan Grid
x_grid = np.linspace(0-dx, x+dx, Nx+2)      #Ghostnode pada boundary
y_grid = np.linspace(0-dx, y+dy, Ny+2)      #Ghostnode pada boundary
t = np.linspace(0, Tend, Nt+1)
x_mesh,y_mesh = np.meshgrid(x_grid,y_grid)
F = np.zeros((Nt+1, Ny+2, Nx+2))
 
```
5. Selanjutnya, iterasi dilakukan sampai semua syarat batas terpenuhi.
```
#Kondisi Awal(Initial Condition)
F[0,py1,px1] = Ic
#%%
#Iterasi
for n in range (0, Nt):
    for i in range (1,Ny+1):
        for j in range(1,Nx+1):
            F[n+1,i,j]=((F[n,i,j]*(1-abs(lx)-abs(ly)))  + \
                        (0.5*(F[n,i-1,j]*(ly+abs(ly)))) + \
                        (0.5*(F[n,i+1,j]*(abs(ly)-ly))) + \
                        (0.5*(F[n,i,j-1]*(lx+abs(lx)))) + \
                        (0.5*(F[n,i,j+1]*(abs(lx)-lx))) + \
                        (ay*(F[n,i+1,j]-2*(F[n,i,j])+F[n,i-1,j])) + \
                        (ax*(F[n,i,j+1]-2*(F[n,i,j])+F[n,i,j-1]))) #Diskritisasi
    #Syarat Batas (Dirichlet Boundary Condition)
    F[n+1,0,:] = 0 #BC Bawah
    F[n+1,:,0] = 0 #BC Kiri
    F[n+1,Ny+1,:] = 0 #BC Atas
    F[n+1,:,Nx+1] = 0 #BC Kanan
 
``` 
6. Langkah berikutnya membuat _script_ untuk _output_ gambar penyebaran polutan. _Script_ siap dijalankan.
```
    #Output Gambar
    plt.clf()
    plt.pcolor(x_mesh, y_mesh, F[n+1,:,:],cmap = 'jet',shading ='auto',edgecolors = 'k')
    cbar = plt.colorbar(orientation = 'vertical', shrink = 0.95, extend = 'both')
    cbar.set_label(label='Concentration', size = 8)
    #plt.clim(0,100)
    plt.title('Nama Lengkap_NIM \n t='+str(round(dt*(n+1),3))+', Initial Condition='+str(Ic),fontsize=10)
    plt.xlabel('x_grid',fontsize=9)
    plt.ylabel('y_grid',fontsize=9)
    plt.axis([0, x, 0, y])
    #plt.pause(0.01)
    plt.savefig(str(n+1)+'.jpg', dpi = 300)
    plt.pause(0.01)
    plt.close()
    print('running timestep ke:' +str(n+1) + ' dari:' +str(Nt) + '('+ percentage(n+1,Nt)+')')
    #print('Nilai CFL:' +str(cfl) + ' dengan arah:' +str(theta))
```
#### 📌Hasil Running📌
![Hasil Running](https://user-images.githubusercontent.com/105897134/169520897-cfb19073-7f57-4191-bd03-d8373ffd2e26.png)

### 📒**3.2. Modul 3: Hidrodinamika 1 Dimensi**📒

#### 📌Definisi dan Persamaan📌
Hidrodinamika 1 dimensi sangat penting untuk mensimulasikan pola gerak air laut secara global. Model Hidrodinamika dalam air laut dapat digunakan untuk mengkaji pergerakan polutan, disipasi panas di laut, sebaran radionuklida yang terlepas ke badan air laut serta untuk pengkajian klimatologi laut.

Pemodelan Hidrodinamika 1D:
- Model yang dibangun dari adanya proses yang mempengaruhi massa air.
- Penampang melintang diambil tegak lurus terhadap aliran sungai (x).
- Ketinggian air dan kecepatan yang dihasilkan seragam saat melintasi penampang.
- Model 1D lebih cocok diterapkan pada kemiringan yang rendah atau landai.
- Mensimulasikan elevasi muka air laut dan kecepatan arus yang dipengaruhi oleh beberapa parameter.

Hidrodinamika 1 dimensi memiliki persamaan utama, yaitu :

![Momentum]![image](https://user-images.githubusercontent.com/105913443/169557409-fd3160df-0310-417d-b09b-86f8fc54d27c.png)



![Kontinuitas]![image](https://user-images.githubusercontent.com/105913443/169557846-4c4f3fbb-0c72-424c-9a55-7b491b9115ea.png)


Hidrodinamika 1 dimensi memiliki persamaan pembangunan, yaitu :

![image](https://user-images.githubusercontent.com/105913443/169557999-73b93686-afe0-4687-b030-7ee6b2cd68bc.png)
![image](https://user-images.githubusercontent.com/105913443/169558103-0ec690f7-7c99-40f2-a8c6-4ec4970a9e51.png)

#### 📌Metode Diskritisasi Beserta Hasilnya📌
Diskritisasi persamaan hidrodinamika 1 dimensi dapat dilakukan menggunakan metode eksplisit.

![image](https://user-images.githubusercontent.com/105913443/169558510-0ce98473-a3da-429c-b738-7bd364699a07.png)

Dengan syarat :

![image](https://user-images.githubusercontent.com/105913443/169558609-e3b0b0c0-db4a-4934-a8ec-e3607acc7cf9.png)

#### 📌Pengaplikasian Hidrodinamika 1 Dimensi dalam Oseanografi📌
- Analisis pendangkalan jalur pelayaran

- Penentuan tipe pengaman pantai

- Pemodelan transpor sedimen untuk membuktikan adanya sedimentasi dan kekeruhan

#### 📌Kekurangan Hidrodinamika 1 Dimensi📌
- Datanya terlalu banyak

- Rawan eror ketika terdapat perhitungan aliran kritis

- Simulasi lama

#### 📌Pengerjaan Script📌
1. Memasukkan _mandatory library python matploblib_ untuk memberikan efek visual pada grafik, _numpy_ untuk perhitungan numerik dan _sys_ untuk mengakses konfigurasi interpreter pada saat _runtime_. 
```
import matplotlib.pyplot as plt
import numpy as np
 
```
2. Selanjutnya, memasukkan parameter perhitungan polutan yang akan digunakan.
```
#Proses Awal
p = 5000 #Panjang Grid
T = 1200 #Waktu Simulasi
A = 0.5  #Amplitudo
D = 15   #Depth/Kedalaman
dt = 2   
To = 300 #Periode
dx = 100

g = 9.8
pi = np.pi
C = np.sqrt(g*D) #Kecepatan Arus
s = 2*pi/To      #Kecepatan Sudut Gelombang
L = C*To         #Panjang Gelombang
k = 2*pi/L       #Koefisien Panjang Gelombang
Mmax = int(p//dx)
Nmax = int(T//dt)

zo = [None for _ in range(Mmax)]
uo = [None for _ in range (Mmax)]

hasilu = [None for _ in range (Nmax)]
hasilz = [None for _ in range (Nmax)]

```
3. Kemudian, _script_ perhitungan dibuat.
```
for i in range(1, Mmax+1):
    zo[i-1] = A*np.cos(k*(i)*dx)
    uo[i-1] = A*C*np.cos(k*((i)*dx+(0.5)*dx))/(D+zo[i-1])
for i in range(1, Nmax+1):
    zb = [None for _ in range (Mmax)]
    ub = [None for _ in range (Mmax)]
    zb[0] = A*np.cos(s*(i)*dt)
    ub[-1] = A*C*np.cos(k*L-s*(i)*dt)/(D+zo[-1])
    for j in range(1, Mmax):
        ub[j-1] = uo[j-1]-g*(dt/dx)*(zo[j]-zo[j-1])
    for k in range(2, Mmax+1):
        zb[k-1] = zo[k-1]-(D+zo[k-1])*(dt/dx)*(ub[k-1]-ub[k-2])
        hasilu[i-1] = ub
        hasilz[i-1] = zb
    for p in range(0, Mmax):
        uo[p] = ub[p]
        zo[p] = zb[p]
        
```
4. Setelah itu, _script_ grafik dan grid dibuat. 
```
#Pembuatan Grafik
def rand_col_hex_string():
    return f'#{format(np.random.randint(0,16777215), "#08x")[2:]}'

hasilu_np = np.array(hasilu)
hasilz_np = np.array(hasilz)

fig0, ax0 = plt.subplots(figsize=(12,8))
for i in range(1, 16):
    col0 = rand_col_hex_string()
    line, = ax0.plot(hasilu_np[:,i-1], c=col0, label=f'n={i}')
    ax0.legend()
    
    ax0.set(xlabel='Waktu', ylabel='Kecepatan Arus',
           title='''Nama_NIM
           Perubahan Kecepatan Arus dalam Grid Tertentu di Sepanjang Waktu''')
    ax0.grid()
    
fig1, ax1 = plt.subplots(figsize=(12,8))
for i in range(1, 16):
    col1 = rand_col_hex_string()
    line, = ax1.plot(hasilz_np[:,i-1], c=col1, label=f'n={i}')
    ax1.legend()
    
    ax1.set(xlabel='Waktu', ylabel='Elevasi Muka Air',
           title='''Nama_NIM
           Perubahan Elevasi Permukaan Air dalam Grid Tertentu di Sepanjang Waktu''')
    ax1.grid()
    
fig2, ax2 = plt.subplots(figsize=(12,8))
for i in range(1, 16):
    col2 = rand_col_hex_string()
    line, = ax2.plot(hasilu_np[i-1], c=col2, label=f't={i}')
    ax2.legend()
    
    ax2.set(xlabel='Grid', ylabel='Kecepatan Arus',
           title='''Nama_NIM
           Perubahan Kecepatan Arus dalam Waktu Tertentu di Sepanjang Grid''')
    ax2.grid()

fig3, ax3 = plt.subplots(figsize=(12,8))
for i in range(1, 16):
    col3 = rand_col_hex_string()
    line, = ax3.plot(hasilz_np[i-1], c=col3, label=f't={i}')
    ax3.legend()
    
    ax3.set(xlabel='Grid', ylabel='Elevasi Muka Air',
           title='''Nama_NIM
           Perubahan Elevasi Permukaan Air dalam Waktu Tertentu di Sepanjang Grid''')
    ax3.grid()
    
plt.show()
```
#### 📌Hasil Running📌
![image](https://user-images.githubusercontent.com/105913443/169561223-6562a9b8-8d17-4ebb-9d96-ae5a9fb2034f.png)

### 📒**3.3. Modul 4: Model Hidrodinamika 2 Dimensi**📒

#### 📌Definisi📌
Hidrodinamika adalah cabang dari mekanika fluida, khususnya zat cair incompressible yang dipengaruhi oleh gaya internal dan eksternal. Dalam hidrodinamika laut, gaya-gaya yang terpenting adalah gaya gravitasi, gaya gesekan, dan gaya coriolis. Model Hidrodinamika dalam air laut dapat digunakan untuk mengkaji pergerakan polutan, disipasi panas di laut, sebaran radionuklida yang terlepas ke badan air laut serta untuk pengkajian klimatologi laut. Fenomena arus, gelombang, dan pasang surut adalah bagian dari hidrodinamika laut. Parameter hidrodinamika laut tersebut merupakan bagian dari keseluruhan komponen oseangrafi yang saling mengadakan interaksi atau saling mempengaruhi satu sama lain yang cukup kompleks. 

Dalam pemodelan Hidrodinamika 2D, terdapat beberapa hasil pemodelan yang berbeda dengan pemodelan Hidrodinamika 1D, yaitu:
- Kecepatan arus dan gelombang yang dihasilkan tidak seragam, pasti berbeda-beda di setiap daerah penelitian.
- Daerah atau medan direpresentasikan sebagai permukaan kontinu, tidak hanya ada medan X, tetapi ada medan (X, Y) atau medan (X, Z).
- Model 2D lebih cocok diterapkan pada kemiringan yang curam atau tinggi.
- Kedalaman air tidak dianggap seragam.

#### 📌Pengaplikasian Hidrodinamika 2 Dimensi dalam Oseanografi📌
- Pemodelan Gelombang karena Angin
- Pemodelan Gaya Pembangkit Arus karena Angin
- Pemodelan Sampah Plastik di Laut
- Pemodelan _Coastal Dynamics_ dan Sedimentasi Pantai
- Pemodelan Tumpahan Minyak di Laut
- Pemodelan _Longshore Current_ Beserta Proses Sedimentasinya
- Pemodelan untuk Mengestimasi Potensi Energi Arus Laut

   Arus laut adalah gerakan massa air laut yang memiliki energi kinetik untuk digunakan sebagai penggerak rotor atau turbin pembangkit tenaga listrik. Salah satu teknologi yang dapat digunakan untuk mengkonversi gerakan turbin menjadi energi listrik adalah _Marine Current Turbin_ yang bekerja menyerupai pembangkit listrik tenaga angin, namun ditempatkan di dalam air.

   Salah satu asumsi dasar yaitu dengan menggunakan rumus Frankel, maka arus dengan kecepatan 1 m/s yang melewati penampang vertikal sebesar 1 m^2, dapat menghasilka rapat daya maksimum sekitar:
   
   ![image](https://user-images.githubusercontent.com/105908002/169751354-f4e2b7aa-903e-48a6-8e1a-7348c7a538a1.png)

   Kecepatan arus maksimum terjadi saat pasang purnama pada kondisi peralihan pasang menuju surut atau surut menuju pasang. Kecepatan arus mencapai minimum pada saat elevasi muka air pasang maksimum atau surut minimum.

   Pemodelan yang dilakukan biasanya hanya mengkaji potensi energi arus untuk satu nilai arus yang besarnya merupakan hasil perata-rataan terhadap kedalaman (2 dimensi horizontal). Untuk pengkajian lebih lanjut potensi energi arus yang terdapat pada selat-selat di Indonesia, perlu dilakukan pemodelan secara 3 dimensi, sehingga dapat diketahui potensi yang tersimpan pada setiap kedalaman.

#### 📌Pengerjaan Script📌
1. Memasukkan _mandatory library python matploblib_ untuk memberikan efek visual pada grafik, import _NDBC_ dari _siphon.simplewebservice.ndbc._ yang mana NDBC menyimpan file bergulir terbaru selama 45 hari untuk setiap _buoy_. 
```
import matplotlib.pyplot as plt
from siphon.simplewebservice.ndbc import NDBC
```
2. Selanjutnya, _Station ID_ yang ingin diamati dimasukkan
```
df = NDBC.realtime_observations('STATION ID')
df.head()
```
3. Setelah itu, _script_ grafik _time series_ sederhana _Pressure, Wind speed, gust, direction, Water temperature_ dibuat 
```
fig, (ax1, ax2, ax3) = plt.subplots(3, 1, figsize=(12, 10))
ax2b = ax2.twinx()

# Pressure
ax1.plot(df['time'], df['pressure'], color='black')
ax1.set_ylabel('Pressure [hPa]')
fig.subtitle('Nama_NIM_Kelas', fontsize=18)

# Wind speed, gust, direction
ax2.plot(df['time'], df['wind_speed'], color='tab:orange')
ax2.plot(df['time'], df['wind_gust'], color='tab:olive', linestyle='--')
ax2b.plot(df['time'], df['wind_direction'], color='tab:blue', linestyle='-')
ax2.set_ylabel('Wind Speed [m/s]')
ax2b.set_ylabel('Wind Direction')

# Water temperature
ax3.plot(df['time'], df['water_temperature'], color='tab:brown')
ax3.set_ylabel('Water Temperature [degC]')

plt.show()
```
#### 📌Hasil Running📌
![modul 4](https://user-images.githubusercontent.com/90039747/169631215-dec32e37-ea73-46ba-8b54-186da2acc6c1.png)

4. Selanjutnya, masuk ke website NDBC-NOAA (https://www.ndbc.noaa.gov/obs.shtml), pada bagian _search Station ID_, cari _Station ID_ pada kolom pencarian
![fghm](https://user-images.githubusercontent.com/90039747/169631375-60590fb0-0e03-4150-a525-2056f53854cf.png)

5. Kemudian Lokasi _buoy_ diidentifikasi
![image](https://user-images.githubusercontent.com/90039747/169631429-fd64c9f6-37d1-48c4-b9e6-45b50443d6b1.png)

## 🗒️4. SARAN PENGEMBANGAN🗒️
1. Tipe pembuatan grafik dapat dikreasikan dengan mengacu pada _Style sheets reference_. (https://matplotlib.org/stable/gallery/style_sheets/style_sheets_reference.html)
2. Tipe garis dan warna pada grafik dapat dikreasikan dengan mengacu pada _Line and Color style_. (https://matplotlib.org/2.1.1/api/_as_gen/matplotlib.pyplot.plot.html)
3. Persamaan untuk setiap metode dapat _customizable_



## 🙏5. UCAPAN TERIMA KASIH🙏
Demikianlah tugas akhir praktikum pemodelan oseanografi ini kami buat. Authors memohon maaf apabila terdapat kesalahan dalam tugas akhir kelompok ini. Team 20 selaku author dari repository kali ini juga mengucapkan terima kasih kepada:
1. Dr. Aris Ismanto, S.Si, M.Si. selaku dosen pengampu mata kuliah Pemodelan Oseanografi.
2. Prof. Dr. Denny Nugroho Sugianto, S.T., M.Si. selaku dosen pengampu mata kuliah Pemodelan Oseanografi.
3. Dr. Elis Indrayanti, S.T., M.Si. selaku dosen pengampu mata kuliah Pemodelan Oseanografi.
4. Rikha Widiaratih, S.Si, M.Si. selaku dosen pengampu mata kuliah Pemodelan Oseanografi.
5. Tim asisten Praktikum Pemodelan Oseanografi tahun 2022 yang selalu mendampingi dalam pengerjaan tugas akhir kelompok ini.
6. Seluruh rekan-rekan Oseanografi 2020 yang turut mendukung tersusunnya repository ini.

