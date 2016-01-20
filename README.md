# gcm
Android Client Google Cloud Message

## Step
> Aplikasi ini di buat menggunakan android studio

- Lanjutan dari kode sebelumnya [gcm-server](https://github.com/pwcahyo/gcm-server)
- Download `google-services.json` yang API SERVER KEY nya digunakan pada sisi server gcm-server sebelumnya
- Masukan `google-services.json` kedalam folder ROOT_ANDROID/app/
- Top dependencies `build.gradle(Module:app)` 
```javascript
dependencies {
compile fileTree(dir: 'libs', include: ['*.jar'])
compile "com.google.android.gms:play-services:8.4.0"
compile 'com.android.support:appcompat-v7:23.0.0'
}
apply plugin: 'com.google.gms.google-services'
```
- Project dependencies `build.gradle(Module:GCM)`
```javacript
classpath 'com.android.tools.build:gradle:1.3.0'
classpath 'com.google.gms:google-services:2.0.0-alpha3'
```
- Kemudian Syncrhonize Gradle

- MainActivity.java Replace :
```javascript
private static final String GCM_SENDER_ID = "SENDER ID dari API GCM"; //apabila lupa bisa dilihat [disini](https://console.developers.google.com/project)
private static final String WEB_SERVER_URL = "URL SERVER";
```
- Apabila aplikasi android sudah berjalan klik tombol register ke server untuk melakukan registerDeviceID terhadap API GCM dan phpserver (server pihak ke tiga)
- Untuk melakukan pengiriman notifikasi dari server, aplikasi client harus dalam posisi idle
- Contoh aplikasi [APK](https://drive.google.com/open?id=0ByeKmxCX2t93Tnd0TzFMTHhOVWs "Android GCM Client")
