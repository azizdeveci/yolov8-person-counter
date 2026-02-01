🚶‍♂️ YOLOv8 ile Gerçek Zamanlı Kişi Sayma Sistemi

Bu proje, YOLOv8 ve ByteTrack kullanarak bir video üzerinde gerçek zamanlı kişi tespiti ve takibi yapar.
Belirlenen dikey bir çizgiden geçen kişileri giren / çıkan olarak sayar.

🎯 Proje özellikle:

AVM girişleri

Turnike sistemleri

Kalabalık analizi

Akıllı şehir uygulamaları

gibi senaryolar için temel bir altyapı sunar.

🛠 Kullanılan Teknolojiler

Python

OpenCV – Video işleme

YOLOv8 (Ultralytics) – Kişi tespiti

ByteTrack – Nesne takibi (ID bazlı)

⚙️ Nasıl Çalışır?

Video dosyası OpenCV ile okunur

YOLOv8 modeli her karede person sınıfını tespit eder

ByteTrack sayesinde her kişiye benzersiz bir ID atanır

Kişilerin X eksenindeki hareketi takip edilir

Dikey çizgiyi:

Soldan sağa geçenler → Giriş

Sağdan sola geçenler → Çıkış
olarak sayılır

Her kişi yalnızca bir kez sayılır.

▶️ Kurulum
git clone https://github.com/azizdeveci/yolov8-person-counter.git
cd yolov8-person-counter
pip install -r requirements.txt

🎥 Kullanım

main.py içindeki şu satırı kendi video yolunla değiştir:

cap = cv2.VideoCapture("video_path")


Sonra çalıştır:

python main.py


Program çalışırken:

Yeşil kutular → Tespit edilen kişiler

ID numarası → Takip edilen kişi

Kırmızı çizgi → Sayım hattı

q tuşu → Çıkış

📊 Ekran Çıktısı

Giriş sayısı sol üstte

Çıkış sayısı sağ üstte gösterilir

(İstersen assets/demo.gif ekleyebilirsin, çok şık durur.)

🔍 Projede Dikkat Edilen Noktalar

Aynı kişinin birden fazla kez sayılması engellenmiştir

Sadece person sınıfı dikkate alınır

Takip işlemi persist=True ile kararlı hale getirilmiştir