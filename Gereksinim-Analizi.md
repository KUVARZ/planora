# Tüm Gereksinimler

1. **Üye Olma** (Ramazan Bodur)
    - **API Metodu:** `POST /auth/register`
    - **Açıklama:** Kullanıcıların yeni hesaplar oluşturarak sisteme kayıt olmasını sağlar. Kişisel bilgilerin toplanmasını ve hesap oluşturma işlemlerini içerir. Kullanıcılar kullanıcı adı, email adresi ve şifre belirleyerek hesap oluşturur.

2. **Kullanıcı Bilgilerini Düzenleme** (Ramazan Bodur)
    - **API Metodu:** `PUT /profile`
    - **Açıklama:** Kullanıcının profil bilgilerini güncellemesini sağlar. Kullanıcılar ad, soyad, email, doğum tarihi gibi kişisel bilgilerini değiştirebilir. Güvenlik için giriş yapmış olmak gerekir ve kullanıcılar yalnızca kendi bilgilerini güncelleyebilir.

3. **Kullanıcı Bilgisi Görüntüleme** (Ramazan Bodur)
    - **API Metodu:** `GET /profile`
    - **Açıklama:** Kullanıcının kendi profil bilgilerini görüntülemesini sağlar. Ad, soyad, kullanıcı adı, email adresi, doğum tarihi gibi hesap bilgileri güvenli şekilde listelenir. Bu işlem için kullanıcının sisteme giriş yapmış olması gerekir ve yalnızca kendi profil verilerine erişebilir.

4. **Kimlik Doğrulama Metodu Oluşturma** (Ramazan Bodur)
    - **API Metodu:** `POST /auth/2fa`
    - **Açıklama:** Kullanıcı hesabı için ek güvenlik amacıyla iki aşamalı kimlik doğrulama (2FA) yönteminin tanımlanmasını sağlar. Kullanıcı, doğrulama uygulaması veya benzeri bir doğrulama yöntemi ekleyerek hesabını daha güvenli hale getirebilir. Bu işlem yalnızca giriş yapmış kullanıcılar tarafından gerçekleştirilebilir.

5. **Kimlik Doğrulama Metodu Güncelleme** (Ramazan Bodur)
    - **API Metodu:** `PUT /auth/2fa`
    - **Açıklama:** Kullanıcının daha önce tanımladığı iki aşamalı kimlik doğrulama (2FA) yöntemini güncellemesini sağlar. Kullanıcı mevcut doğrulama yöntemini değiştirebilir, yeniden yapılandırabilir veya yeni bir yöntem ile değiştirebilir. Güvenlik nedeniyle işlem sırasında kullanıcının kimliği tekrar doğrulanabilir.

6. **Favori Ekle** (Ramazan Bodur)
    - **API Metodu:** `POST /favorites`
    - **Açıklama:** Kullanıcının beğendiği mekan, aktivite, gezi planı vs. favorilerine eklemesini sağlar. Böylece kullanıcı daha sonra bu içeriklere kolayca erişebilir ve kişisel bir favori listesi oluşturabilir. İşlem için kullanıcının giriş yapmış olması gerekir.

7. **Favori Silme** (Ramazan Bodur)
    - **API Metodu:** `DELETE /favorites/:favoriteId`
    - **Açıklama:** Kullanıcının favori listesinde bulunan bir öğeyi kaldırmasını sağlar. Silinen favori kayıt, kullanıcının favori listesinden çıkarılır ve ilgili öğe artık favoriler ekranında görüntülenmez. Güvenlik için kullanıcı yalnızca kendi favori kayıtlarını silebilir.

8. **Favorileri Görüntüleme** (Ramazan Bodur)
    - **API Metodu:** `GET /favorites`
    - **Açıklama:** Kullanıcının favori olarak kaydettiği mekan, aktivite, gezi planı vs. listesini görüntülemesini sağlar. Favoriler, kullanıcının daha sonra hızlı erişim sağlayabilmesi için tek bir liste halinde sunulur. Kullanıcı yalnızca kendi favori listesini görüntüleyebilir.

9. **Giriş Yapma** (Sümeyye Zişan Abdan)
   - **API Metodu:** `POST /auth/login`
   - **Açıklama:** Kullanıcıların sisteme giriş yaparak hizmetlere erişmesini sağlar. Email adresi, şifre ve 2FA ile kimlik doğrulama yapılır. Başarılı giriş sonrası kullanıcıya erişim izni verilir ve kişisel verilerin güvenliği sağlanır.

10. **Şifre Sıfırlama** (Sümeyye Zişan Abdan)
    - **API Metodu:** `POST /password-reset`
    - **Açıklama:** Şifresini unutan veya değiştirmek isteyen kullanıcıların şifre sıfırlama işlemini başlatmasını sağlar. Kullanıcı email adresini girerek sıfırlama talebi oluşturur ve doğrulama adımlarını tamamladıktan sonra yeni bir şifre belirleyebilir. Bu süreç, hesap güvenliğini koruyacak şekilde güvenli doğrulama mekanizmaları ile yürütülür.

11. **Kullanıcı Adı Doğrulama** (Sümeyye Zişan Abdan)
    - **API Metodu:** `GET /username-check`
    - **Açıklama:** Kullanıcının seçtiği kullanıcı adının sistemde kullanılabilir olup olmadığını kontrol eder. Kayıt veya profil güncelleme sırasında aynı kullanıcı adının birden fazla kişi tarafından kullanılmasını engellemeye yardımcı olur. Uygunluk durumuna göre kullanıcıya geçerli veya kullanımda bilgisi döndürülür.

12. **Takvim Planı Oluşturma** (Sümeyye Zişan Abdan)
    - **API Metodu:** `POST /calendar`
    - **Açıklama:** Kullanıcının seyahat planı kapsamında belirli bir gün ve saat için takvim kaydı oluşturmasını sağlar. Plan içerisinde mekan, aktivite, saat aralığı, notlar ve ilgili öneriler gibi bilgiler yer alabilir. Bu özellik sayesinde kullanıcı seyahat programını gün bazlı ve düzenli şekilde planlayabilir.

13. **Takvim Planı Düzenleme** (Sümeyye Zişan Abdan)
    - **API Metodu:** `PUT /calendar/:planId`
    - **Açıklama:** Kullanıcının oluşturduğu takvim planı kayıtlarını güncellemesini sağlar. Kullanıcı planın tarihini, saatini, aktivite bilgisini, mekan bilgisini veya notlarını değiştirebilir. Güvenlik açısından kullanıcı yalnızca kendi oluşturduğu plan kayıtlarını düzenleyebilir.

14. **Takvim Planı Silme** (Sümeyye Zişan Abdan)
    - **API Metodu:** `DELETE /calendar/:planId`
    - **Açıklama:** Kullanıcının oluşturduğu takvim planı kayıtlarından birini silmesini sağlar. Silinen plan kaydı takvim görünümünden kaldırılır ve ilgili günün programı güncellenmiş şekilde gösterilir. Kullanıcı yalnızca kendi takvim planlarını silebilir.

15. **Takvim Planı Görüntüleme** (Sümeyye Zişan Abdan)
    - **API Metodu:** `GET /calendar/:planId`
    - **Açıklama:** Kullanıcının belirli bir takvim planı kaydının detaylarını görüntülemesini sağlar. Plan kaydında tarih, saat, mekan, aktivite, notlar ve varsa yapay zeka tarafından önerilen içeriklere ait bilgiler gösterilebilir. Kullanıcı yalnızca kendi plan kayıtlarının detaylarına erişebilir.

16. **Takvim Görüntüleme** (Sümeyye Zişan Abdan)
    - **API Metodu:** `GET /calendar`
    - **Açıklama:** Kullanıcının oluşturduğu tüm takvim planlarını gün, hafta veya ay bazında görüntülemesini sağlar. Takvim üzerinde hangi günlerde hangi etkinliklerin planlandığı listelenir ve kullanıcı seyahat programını bütüncül olarak takip edebilir. Bu işlem için kullanıcının giriş yapmış olması gerekir ve yalnızca kendi takvim verileri görüntülenir.

17. **Rota Görüntüleme** (Ayşenur Laklak)
    - **API Metodu:** `GET /route/:routeId`
    - **Açıklama:** Kullanıcının oluşturduğu belirli bir rota kaydının detaylarını görüntülemesini sağlar. Rota içerisinde başlangıç ve varış noktaları, duraklar, önerilen mekanlar, aktivite sıralaması ve varsa zaman planı bilgileri vs. yer alabilir. Kullanıcı yalnızca kendi rota kayıtlarının detaylarına erişebilir.

18. **Rota Oluşturma** (Ayşenur Laklak)
    - **API Metodu:** `POST /route`
    - **Açıklama:** Kullanıcının seçtiği şehir ve gezi tercihleri doğrultusunda yeni bir rota oluşturmasını sağlar. Rota kaydı; mekanlar, durak sırası, aktiviteler, tahmini süreler ve notlar gibi bilgileri içerebilir. Bu özellik sayesinde kullanıcı seyahat planını daha düzenli ve takip edilebilir bir yapı içerisinde oluşturabilir.

19. **Rota Güncelleme** (Ayşenur Laklak)
    - **API Metodu:** `PUT /route/:routeId`
    - **Açıklama:** Kullanıcının daha önce oluşturduğu rota kaydını güncellemesini sağlar. Kullanıcı rota üzerindeki durakları, mekan sıralamasını, aktivite bilgilerini, zaman planını, notlarını vs. değiştirebilir. Güvenlik açısından kullanıcı yalnızca kendi oluşturduğu rota kayıtlarını düzenleyebilir.

20. **Rota Silme** (Ayşenur Laklak)
    - **API Metodu:** `DELETE /route/:routeId`
    - **Açıklama:** Kullanıcının oluşturduğu rota kayıtlarından birini silmesini sağlar. Silinen rota kaydı kullanıcının rota listesinden kaldırılır ve ilgili planlama ekranlarında artık görüntülenmez. Kullanıcı yalnızca kendi rota kayıtlarını silebilir.

21. **Rotaları Listeleme** (Ayşenur Laklak)
    - **API Metodu:** `GET /route`
    - **Açıklama:** Kullanıcının oluşturduğu tüm rota kayıtlarını liste halinde görüntülemesini sağlar. Liste üzerinden kullanıcı mevcut rotalarını inceleyebilir ve ilgili rota detayına erişebilir. Bu işlem için kullanıcının giriş yapmış olması gerekir ve yalnızca kendi rota verileri görüntülenir.

22. **Bildirimleri Görüntüleme** (Ayşenur Laklak)
    - **API Metodu:** `GET /notifications`
    - **Açıklama:** Kullanıcıya ait bildirimlerin listesini görüntülemesini sağlar. Bildirimler; plan hatırlatmaları, yaklaşan etkinlikler, rota değişiklikleri veya sistem bilgilendirmeleri gibi içerikleri kapsayabilir. Kullanıcı yalnızca kendi hesabına ait bildirimleri görüntüleyebilir.

23. **Bildirim Düzenleme** (Ayşenur Laklak)
    - **API Metodu:** `PUT /notifications/:notifId`
    - **Açıklama:** Kullanıcının mevcut bir bildirim kaydı üzerinde düzenleme yapmasını sağlar. Bildirim içeriği, hatırlatma zamanı, bildirim durumu veya bildirim tercihleri güncellenebilir. Güvenlik açısından kullanıcı yalnızca kendi bildirim kayıtlarını düzenleyebilir.

24. **Bildirim Silme** (Ayşenur Laklak)
    - **API Metodu:** `DELETE /notifications/:notifId`
    - **Açıklama:** Kullanıcının bildirim listesindeki bir bildirimi kaldırmasını sağlar. Silinen bildirim kullanıcı arayüzünde artık görüntülenmez ve bildirim listesi güncellenir. Kullanıcı yalnızca kendi bildirim kayıtlarını silebilir.

25. **Bildirim Ekleme** (Ayşenur Laklak)
    - **API Metodu:** `POST /notifications`
    - **Açıklama:** Kullanıcıya ait yeni bir bildirim kaydı oluşturulmasını sağlar. Bildirim; başlık, içerik, tarih-saat, hatırlatma türü ve ilgili plan/rota bağlantısı gibi bilgiler içerebilir. Bu özellik, kullanıcıya seyahat planı ile ilgili önemli hatırlatmaların zamanında iletilmesini destekler.

26. **Bildirim Detayı Görüntüleme** (Ayşenur Laklak)
    - **API Metodu:** `GET /notifications/:notifId`
    - **Açıklama:** Kullanıcının seçtiği bir bildirimin detaylarını görüntülemesini sağlar. Bildirim detayında başlık, içerik, oluşturulma zamanı, hatırlatma zamanı ve ilgili plan/rota bağlantısı gibi bilgiler yer alabilir. Kullanıcı yalnızca kendi bildirim kayıtlarının detaylarına erişebilir.

27. **Kullanıcı Tercihi Ekleme** (Volkan Avcı)
    - **API Metodu:** `POST /preferences`
    - **Açıklama:** Kullanıcının seyahat planlamasında kullanılmak üzere kişisel tercih bilgilerini sisteme eklemesini sağlar. Tercihler; bütçe aralığı, ilgi alanları, ulaşım tercihi, yemek tercihleri, aktivite türleri veya konaklama beklentileri gibi bilgileri içerebilir. Bu bilgiler, yapay zeka destekli önerilerin kullanıcıya daha uygun şekilde sunulmasına yardımcı olur.

28. **Kullanıcı Tercihi Güncelleme** (Volkan Avcı)
    - **API Metodu:** `PUT /preferences/:prefId`
    - **Açıklama:** Kullanıcının daha önce kaydettiği tercih bilgilerinde değişiklik yapmasını sağlar. Kullanıcı bütçe, ilgi alanı, ulaşım, yemek veya aktivite tercihlerini güncelleyerek öneri sonuçlarını kendi ihtiyaçlarına göre yeniden şekillendirebilir. Güvenlik açısından kullanıcı yalnızca kendi tercih kayıtlarını düzenleyebilir.

29. **Kullanıcı Tercihi Silme** (Volkan Avcı)
    - **API Metodu:** `DELETE /preferences/:prefId`
    - **Açıklama:** Kullanıcının kayıtlı tercih bilgilerinden birini sistemden kaldırmasını sağlar. Silinen tercih kaydı artık öneri oluşturma sürecinde dikkate alınmaz ve kullanıcı tercih listesinde görüntülenmez. Kullanıcı yalnızca kendi tercih kayıtlarını silebilir.

30. **Kullanıcı Tercihleri Görüntüleme** (Volkan Avcı)
    - **API Metodu:** `GET /preferences`
    - **Açıklama:** Kullanıcının sisteme kaydettiği tüm tercih bilgilerini liste halinde görüntülemesini sağlar. Kullanıcı bu ekran üzerinden mevcut tercihlerini inceleyebilir ve ihtiyaç duyduğunda güncelleme veya silme işlemlerine erişebilir. Bu işlem için kullanıcının giriş yapmış olması gerekir ve yalnızca kendi tercih verileri görüntülenir.

31. **Gezi Noktası Ekleme** (Volkan Avcı)
    - **API Metodu:** `POST /route/:routeId/places`
    - **Açıklama:** Kullanıcının mevcut bir rota içerisine yeni bir gezi noktası eklemesini sağlar. Gezi noktası kaydı; mekan adı, konum bilgisi, ziyaret sırası, tahmini süre, kategori ve notlar gibi bilgileri içerebilir. Bu özellik sayesinde kullanıcı rotasını daha detaylı ve kişiselleştirilmiş şekilde düzenleyebilir.

32. **Gezi Noktası Güncelleme** (Volkan Avcı)
    - **API Metodu:** `PUT /route/:routeId/places/:placeId`
    - **Açıklama:** Kullanıcının rota içerisinde yer alan bir gezi noktasının bilgilerini güncellemesini sağlar. Kullanıcı gezi noktasının adını, konumunu, sırasını, tahmini ziyaret süresini veya notlarını vs. değiştirebilir. Güvenlik açısından kullanıcı yalnızca kendi rotalarına ait gezi noktalarını düzenleyebilir.

33. **Gezi Noktası Silme** (Volkan Avcı)
    - **API Metodu:** `DELETE /route/:routeId/places/:placeId`
    - **Açıklama:** Kullanıcının rota içerisinde bulunan bir gezi noktasını kaldırmasını sağlar. Silinen gezi noktası rota planından çıkarılır ve rota sıralaması gerekli durumlarda güncellenir. Kullanıcı yalnızca kendi rotalarına ait gezi noktalarını silebilir.

34. **Gezi Noktası Görüntüleme** (Volkan Avcı)
    - **API Metodu:** `GET /route/:routeId/places/:placeId`
    - **Açıklama:** Kullanıcının rota içindeki belirli bir gezi noktasının detaylarını görüntülemesini sağlar. Gezi noktası detayında mekan adı, konum bilgisi, kategori, ziyaret süresi, sıra bilgisi ve kullanıcı notları gibi bilgiler yer alabilir. Kullanıcı yalnızca kendi rotalarına ait gezi noktalarının detaylarına erişebilir.

# Gereksinim Dağılımları

1. [Ramazan Bodur'un Gereksinimleri](Ramazan-Bodur/Ramazan-Bodur-Gereksinimler.md)
2. [Sümeyye Zişan Abdan'ın Gereksinimleri](Sumeyye-Zisan-Abdan/Zisan-Abdan-Gereksinimler.md)
3. [Ayşenur Laklak'ın Gereksinimleri](Aysenur-Laklak/Aysenur-Laklak-Gereksinimler.md)
4. [Volkan Avcı'nın Gereksinimleri](Volkan-Avci/Volkan-Avci-Gereksinimler.md)