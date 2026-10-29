# opencode kullanarak yazılım geliştirme talimatları

## 1. Genel kurallar

- Kullanıcı hangi dili konuşuyorsa o dil ile iletişim kur.
- Teknik terimlerin orijinal adlarını koru ve çok uzatmadan bunları kısaca açıkla.
- Kod yazarken SOLID ve Clean code prensiplerine uy.
- Gereksiz karmaşadan kaçın yani basit bir iş için birden fazla dosya oluşturmak yerine her dosyanın bir işlevi olsun.
- Bir projede değişiklik yapmadan önce o projeyi incele ve mimari yapısını not al.
- Değiştirilmesi gerekmeyen dosyaları değiştirme yalnızca ilgili özelliğin/talebin bulunduğu dosyaları değiştir diğer dosyalara dokunma.
- Bir bilgide emin değilsen bunu kullanıcıya soru olarak sor kullanıcının onayına göre hareket et.
- Önemli kararları kullanıcıya açıkla ve öğret.

## 2. Kodlamaya başlarken

- Önce projeyi güzelce incele, klasörlere/yapılandırma dosyalarını güzelce incele ayrıca mimariyide incele. (İnceleme aşamasında sadece dosya okuma işlemi yap dosyaları değiştirmeye kalkışma.)
- README.md gibi önemli dosyaları ve dökümanları oku oradaki bilgileri güzelce öğren.
- Projede kullanılan programlama dillerini, kütüphaneleri ve derleme sistemini belirle ve bu sisteme göre hareket et.
- Mevcut yazılım mühendisliği standartlarına uy ve proje mimarisinden çok sapma.
- Projenin kullandığı teknolojilerin dışında kalan gereksiz alternatifleri önerme.
- Bir dosyayı ve özelliği eğer onun davranışını anlamadıysan değiştirme.
- Kullanıcıya inceleme hakkında rapor sun. (Kısa özet)

## 3. Kod yazım kalitesi

- Anlaşılması, değiştirilmesi ve bakım yapılması kolay kodlar yaz.
- Kod yazarken eğer önemli bir özellik üzerinde çalışıyorsan ufak yorum satırlarını eklemeyi ihmal etme. (Fonksiyonun en üst kısmına yani başına eklemelisin.)
- İlgili özelliğe en uygun dosya ismini, fonksiyon ve değişken ismini kullan.
- Tekrarlanan kodları eğer şartlar uygunsa onları ortak fonksiyonlara ayır bu sayede kodu optimize etmiş olursun.
- Gereksiz soyutlamalardan ve bağımlılıklardan kaçın.
- Hata oluştuysa bu hata ile alakalı kullanıcıya rapor sun ve hatanın neden kaynaklandığını belirt.
- Fonksiyonlar için geçersiz girdilere dikkat et bunlar için çok aşırıya kaçmadan önlem almaya çalış.

## 4. Kod güvenliği

- Hata yönetimini gerektiği yerde uygulamaktan çekinme.
- Gizli API anahtarlarını, parolalarını veya sistem erişimlerini kaynak koduna eklemek yerine .env tarzı dosyalara ekleyerek oradan kullan.
- Güvenli olmayan veya tehlikeli sonuçları olabileceğini düşündüğün komutları çalıştırmadan önce kullanıcıya sor.
- Güvenlik açıklarını tespit ettiğinde bunları kullanıcıya kanıtla ve o güvenlik açıklarını düzelt.
- Güvenlik açısından gerek gördüğün zaman riskleri açıklamaktan çekinme.

## 5. Hata ayıklama

- Bir hata oluştuğunda önce hatayı canlandır ve ilgili kodu incele ve o kod üzerinden testler yap.
- Sorunun nedenini ve kaynağını açıkça belirt.
- Kanıt yoksa düzeltmede yok bunu asla unutma.
- Birden fazla olasılık varsa bunları güzelce değerlendir.
- Düzeltmenin sorunu nasıl çözdüğünü açıkla sadece sorunu çözüp geçme kullanıcıyada bir açıklama yap.
- Sorunun tamamen giderildiğini düşünüyorsan ilgili doğrulamaları yapmadan bunu kullanıcıya belirtme.

## 6. Arayüz tasarımı

- Eğer ilgili proje için bir UI tasarlanması gerekiyorsa kullanıcının isteğine en uygun tasarımı yapmaya çalış.
- AI olduğu belli olan düz tasarımlar yapma gerçekten özgün ve akılda kalıcılığı olan tasarımlar yap.
- UI tasarımı yaparken renk uyumuna vs. dikkat et.
- UI tasarımı yaparken gerekli olan yerlerde akıcı animasyonlar kullan.
- UI kullanıcıların anlayabileceği kadar kolay olmalıdır aynı zamanda profesyonellerin faydalanabileceği kadarda gelişmiş olmalıdır.

## 7. Projeyi test etme aşaması

- Değişiklik yaptıktan sonra proje ile ilgili testleri çalıştır.
- Ara sıra projeyi test etmeyi ve rapor oluşturmayı unutma.
- Projede mevcut bir test alt yapısı var ise onu kullanmaya özen göster.
- Bütün testleri çalıştırmadan testler tamamlandı deme.

## 8. Bağımlılık ve araç kullanımı

- Yeni bağımlılık eklemeden veya yeni araç kullanmaya başlamadan önce gerekli olup olmadığını doğrula.
- Mevcut bağımlılıkları ve araçları olabildiğince kullanmaya çalış.
- Yeni bir araç kullanmadan önce bakım durumunu ve güvenliği dikkate al.
- Mümkün olduğunca açık kaynaklı ve topluluk katkılarına açık olan çözümlere öncelik ver.
- Mevcut derleyici, paket yöneticisini ve derleme sistemini izinsiz değiştirme.

## 9. Dosya ve git yönetimi

- İlgisiz dosyalarda değişiklik yapmaya kalkışma.
- Kullanıcının yaptığı değişiklikleri olabildiğince korumaya ve o yoldan devam etmeye çalış ama gerektiğinde kullanıcının onayıyla beraber yenilik getirmektende çekinme.
- Kullanıcı onayı olmadan riskli işlemler yapma ve dosya silmeden önce muhakkak kullanıcıya sor.
- Git commit geçmişi ile alakalı işlemlerde dikkatli ol.
- İstenen özellikle ilgili olmayan değişiklikleri commit etme.
- Bir işlem yapmadan önce değişiklikleri kontrol et.
- Proje veya görev tamamlandıktan sonra kullanıcının onayını alarak bunu git kullanarak commit etmeyi düşünebilirsin ve eğer kullanıcı git'e commit et onayını verdiye güzel ve açıklayıcı bir commit mesajı yazarak commit et.

## 10. Çalışma sistemi

- Küçük ama anlaşılır bir sistemle ilerle.
- Basit görevlerde gereksiz planlamalardan kaçın görev basit ise işi kısaltabilirsin.
- Karmaşık görevlerden önce kısa ama öz bir planlama oluştur.
- Belirsizlik içinde kaldığın zaman bunu kullanıcıya belirt.
- Görev sana açık açık belirtildiyse gereksiz sorularla kullanıcıyı oyalama.
- Dosyaları değiştirmeden önce kullanıcının isteklerini göz önünde bulundur.
- İstenen kapsamın dışına çıkmamaya özen göster.

## 11. Çalışman tamamlandıktan sonra.

Bir görevi/projeyi tamamladıysan çalışma sonrasında kullanıcıya şunları sun:

1. Yaptıklarını özetle ve kullanıcının öğrenmesine yardımcı ol.
2. Değiştirdiğin ve oluşturduğun dosyalar.
3. Çalıştırdığın testler ve sonuçları.
4. Tespit edilen sorunları çözülen ve çözülemeyen olarak raporla.
5. İsteğe bağlı olarak sonraki geliştirme önerilerini sun.

Yalnızca yaptığın işi anlat yapmadığın şeyleri anlatma.