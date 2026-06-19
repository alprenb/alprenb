 dsPIC33EP128GP502 Ultrasonic Radar Eşzamanlı Bilgisayar Ekranında İzleme

Bu proje, Microchip ailesinden dsPIC33EP128GP502 mikrodenetleyicisi kullanılarak donanım (register) seviyesinde geliştirilmiş bir ultrasonik radar sistemidir. Sistem, bir servo motor(SG-90) üzerine entegre edilmiş ultrasonik sensör(HC-SR04) ile çevreyi tarar ve engellerin mesafe/açı verilerini işler.

 🚀 Proje Özeti
Projenin temel amacı, gömülü sistemlerde donanımsal zamanlayıcıları (Timers) ve kesmeleri (Interrupts) kullanarak gerçek zamanlı (real-time) ve bloklanmayan  bir sensör okuma mimarisi kurmaktır. 

 🛠 Donanım Mimarisi
 Mikrodenetleyici: Microchip dsPIC33EP128GP502
 Sensör:   HC-SR04 Ultrasonik Mesafe Sensörü
 Aktüatör: Servo Motor (SG90)
 Lojik Seviye Dönüştürücü (Level Shifter): 3.3V mikrodenetleyici sinyallerini 5V motor ve sensör lojiğine kararlı bir şekilde aktarmak için harici transistör (BJT/MOSFET) tabanlı donanımsal seviye dönüştürücü devresi tasarlandı.

💻 Yazılım ve Geliştirme Ortamı
 Uygulama : MPLAB X IDE
 Derleyici: XC16
 Programlama Dili: C / Assembly (Register seviyesinde donanım konfigürasyonları)
 Bootloader: BullyCPP (Firmware yükleme ve test süreçleri için)

 ⚙️ Temel Sistem Özellikleri
1. Hassas PWM Kontrolü: Servo motorun yumuşak ve kararlı tarama hareketi  yapabilmesi için donanımsal Timer kesmeleri kullanılarak özel yazılımsal PWM  dizileri oluşturuldu.
2. FSM (Finite State Machine) Mimarisi: Sensörden gelen 'Echo' sinyallerini beklerken işlemcinin kilitlenmemesi (blocking delay kullanılmaması) için durum makinesi tasarımı uygulandı.
3. Register Seviyesinde Konfigürasyon: G/Ç pinleri, osilatör ayarları ve kesme bayrakları doğrudan register manipülasyonu ile yönetilerek maksimum performans hedeflendi.

📂 Kurulum ve Kullanım
1. Depoyu klonlayın: https://github.com/alpren.b/dspic33-ultrasonic-radar.git
2. Projeyi MPLAB X IDE ile açın.
3. BullyCPP veya tercih ettiğiniz bir programlayıcı/debugger (örn. PICkit 3/4) ile kodu derleyip dsPIC33'e yükleyin .

📸 Görseller ve Şemalar


