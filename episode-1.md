# TTV React native 101

[![N|Solid](https://www.manhattanmobile.com/wp-content/uploads/2018/08/react-native-workshop.jpg)](https://nodesource.com/products/nsolid)



### Eepisode satu

  - Menginstall lingkungan untuk pengembangan menggunakan react native
  - Menjalankan Project react native

Pada tahap ini, kami memberikan cara untuk meyiapkan lingkungan pengembangan react native pada sistem operasi windows 10. dan menjalankan project sederhana

### Bahan

Berikut adalah bahan yang dibutuhkan untuk Menginstall react native:

* [React native](https://reactnative.dev/)
* [Visual studio Code](https://code.visualstudio.com/) - awesome  text editor
* [postman](https://www.postman.com/downloads/) - Digunakan untuk membaca dan membuat request 
* [Chocolatey](https://chocolatey.org/) -  Install dan upgrade program lebih sederhana hanya dengan beberapa perintah.
* [Yarn](https://classic.yarnpkg.com/en/) - Yarn adalah dependency manager untuk javascript yang juga berkompetisi dengan NPM
* [Android Studio](https://developer.android.com/studio/?gclid=CjwKCAjw8MD7BRArEiwAGZsrBYMAhEWXwKwhqS9XqcRUGJ9zxFWKZrwLuNDtRxUnOg3wd8cLma3tMxoC8ioQAvD_BwE&gclsrc=aw.ds) - aplikasi khusus yang digunakan oleh Developer dalam pengembangan Aplikasi Android


### Installation

Berikut adalah beberapa langkah yang harus anda lakukan untuk mengistall [React native](https://reactnative.dev/docs/0.61/getting-started) pada sistem operasi windows 10

__Pertama__, install chocolatey dengan menjalankan powershell dengan akses administrator, dan jalankan kode berikut :

[![installchoco](https://i.ibb.co/26ZNM2m/Chocolatey-install.png)](https://nodesource.com/products/nsolid)
```sh
$ Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

```

**Kedua**, Setelah Chocolatey terinstall, kemudian install node.Js, python, Jdk, dan yarn.
Jalankan terminal dengan akses administrator, dan jalankan command berikut

```sh
$ choco install -y nodejs.install python2 jdk8 yarn
```
[![installchoco](https://i.ibb.co/q1Yqbf6/chocolatey-jdk.png)](https://nodesource.com/products/nsolid)

proses installasi ke tiga item ini akan memakan waktu dan membutuhkan internet yang cukup stabil. jika terjadi error ditengah proses installasi, jalankan kembali command tersebut.


**Ketiga**, Download dan install [Android Studio](https://developer.android.com/studio) . sekelah terinstall, buka android studio dan pilih configure pada pojok kanan bawah untuk mensetting SDK android. 

[![installchoco](https://i.ibb.co/w7Njdzg/ads-1.png)](https://nodesource.com/products/nsolid)

Lalu pastikan SDK __Android 9 (Pie)__ terinstall, dan beberapa item ini terceklis

```sh
- Android SDK Platform 28
- Intel x86 Atom_64 System Image or Google APIs Intel x86 Atom System Image
```
[![installchoco](https://i.ibb.co/mcfLH5M/android-install.png)](https://nodesource.com/products/nsolid)


**Ke Empat**, Install Emulator android . dengan cara membuat sample project dan buka AVD manager dan tambahkan device virtual (disini saya menginstall device android 8.0)

[![installchoco](https://i.ibb.co/DbDG41v/AVD1.png)](https://nodesource.com/products/nsolid)
[![installchoco](https://i.ibb.co/d0Cy1kc/AVD2.png)](https://nodesource.com/products/nsolid)
[![installchoco](https://i.ibb.co/GdNqznx/AVD3.png)](https://nodesource.com/products/nsolid)


**Ke Lima**, Menambahkan variable ANDORID_HOME pada environment variable windows. 


[![installchoco](https://i.ibb.co/HpDSKLk/env.png)](https://nodesource.com/products/nsolid)

[![installchoco](https://reactnative.dev/docs/assets/GettingStartedAndroidEnvironmentVariableANDROID_HOME.png)](https://nodesource.com/products/nsolid)

lokasi default SDK yang terinstal biasanya di sini :
```sh
c:\Users\YOUR_USERNAME\AppData\Local\Android\Sdk
```


**Ke Lima**, menambahkan __platform-tools to Path__ pada environment variable windows:
masih sama pada tab yang sama, cari variable bernama __path__ dan click 2 kali -> __click new__

[![installchoco](https://i.ibb.co/ZKXjm7s/path1.png)](https://nodesource.com/products/nsolid)
[![installchoco](https://i.ibb.co/SwpqwTc/path2.png)](https://nodesource.com/products/nsolid)
tambahkan lokasi platform tools. biasanya berada pada  :
```sh
c:\Users\YOUR_USERNAME\AppData\Local\Android\Sdk\platform-tools
```

### Start New Project 
Setelah semua bahan terinstall, maka kita akan melakukan inisialisasi project pertama dengan cara : __Buka terminal pada lokasi yang diinginkan -> jalankan command berikut__
npx react-native init AwesomeProject


```sh
$ npx react-native init AwesomeProject
```
*ganti `AwesomeProject` dengan nama project yang anda inginkan*
Setelah proses inisialisasi selesai, masuk kedalam folder project tersebut dan jalankan terminal pada directori project tersebut. 

```sh
$ cd AwesomeProject
```
dan lakukan installasi package.json menggunakan yarn . proses ini akan memakan waktu, karena yarn akan mendownload seluruh library yang dibutuhkan

```sh
$ yarn add this
```
setelah proses Selesai, jalankan project react native anda

```sh
$ npx react-native run-android
```

[![installchoco](https://i.ibb.co/QHRMphf/init1.png)](https://nodesource.com/products/nsolid)
[![installchoco](https://i.ibb.co/1rYvZqt/init2.png)](https://nodesource.com/products/nsolid)
[![installchoco](https://i.ibb.co/M87x1pQ/init3.png)](https://nodesource.com/products/nsolid)
[![installchoco](https://i.ibb.co/ZhGFjf6/init4.png)](https://nodesource.com/products/nsolid)


### Next episode
  - Memahami life-cycle react native
  - memahami kode dasar reactt native
  - Melakukan layouting screen menggunakan react native, dan mengetahui dasar flexing layout
  - Mempelajari beberapa elemendasar dalam react native


### Android error troubleshoot
__hipotesis 1:__ 
buka android studio dan buka project react native yang telah di init 

[![installchoco](https://i.ibb.co/LYsxw20/trbland1.png)](https://nodesource.com/products/nsolid)

setelah terbuka tunggu hingga proses pembukaan project selesai. Ketika proses sudah selesai, click logo gajah yang ada di pojok kanan atas, action ini akan melakukan download depedency. kemudian tunggu hingga proses selesai.

[![installchoco](https://i.ibb.co/516wvqM/trbland2.png)](https://nodesource.com/products/nsolid)

setelah proses download depedency di androidstudio Selesai -> jalankan terminal di directory project react native anda -> dan jalankan kembali command ini

```sh
$ npx react-native run-android
```
[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

__hipotesis 2: kesalahan pada pengaturan path dan platform tools__ 
error message : 
[![installchoco](https://i.ibb.co/bd78pcj/error2.png)](https://nodesource.com/products/nsolid)

Sesuaikan lokasi platform tools berdasarkann environmet anda. biasanya berada pada  :
```sh
c:\Users\YOUR_USERNAME\AppData\Local\Android\Sdk\platform-tools
```
ganti `YOUR_USERNAME` Sesuai dengan user andda dan pastikan bahwa lokasi platformtools sesuai yang ada pada device anda .

jika android emulator sudah muncul, jangan lupa approve __USB Debuging__ :
[![installchoco](https://i.ibb.co/mTMr6cX/Emulator1.png)](https://nodesource.com/products/nsolid)


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
