1. **Rota Görüntüleme** (Ayşenur Laklak)
    - **API Metodu:** `GET /route/:routeId`
    - **Açıklama:** Kullanıcının oluşturduğu belirli bir rota kaydının detaylarını görüntülemesini sağlar. Rota içerisinde başlangıç ve varış noktaları, duraklar, önerilen mekanlar, aktivite sıralaması ve varsa zaman planı bilgileri vs. yer alabilir. Kullanıcı yalnızca kendi rota kayıtlarının detaylarına erişebilir.

2. **Rota Oluşturma** (Ayşenur Laklak)
    - **API Metodu:** `POST /route`
    - **Açıklama:** Kullanıcının seçtiği şehir ve gezi tercihleri doğrultusunda yeni bir rota oluşturmasını sağlar. Rota kaydı; mekanlar, durak sırası, aktiviteler, tahmini süreler ve notlar gibi bilgileri içerebilir. Bu özellik sayesinde kullanıcı seyahat planını daha düzenli ve takip edilebilir bir yapı içerisinde oluşturabilir.

3. **Rota Güncelleme** (Ayşenur Laklak)
    - **API Metodu:** `PUT /route/:routeId`
    - **Açıklama:** Kullanıcının daha önce oluşturduğu rota kaydını güncellemesini sağlar. Kullanıcı rota üzerindeki durakları, mekan sıralamasını, aktivite bilgilerini, zaman planını, notlarını vs. değiştirebilir. Güvenlik açısından kullanıcı yalnızca kendi oluşturduğu rota kayıtlarını düzenleyebilir.

4. **Rota Silme** (Ayşenur Laklak)
    - **API Metodu:** `DELETE /route/:routeId`
    - **Açıklama:** Kullanıcının oluşturduğu rota kayıtlarından birini silmesini sağlar. Silinen rota kaydı kullanıcının rota listesinden kaldırılır ve ilgili planlama ekranlarında artık görüntülenmez. Kullanıcı yalnızca kendi rota kayıtlarını silebilir.

5. **Rotaları Listeleme** (Ayşenur Laklak)
    - **API Metodu:** `GET /route`
    - **Açıklama:** Kullanıcının oluşturduğu tüm rota kayıtlarını liste halinde görüntülemesini sağlar. Liste üzerinden kullanıcı mevcut rotalarını inceleyebilir ve ilgili rota detayına erişebilir. Bu işlem için kullanıcının giriş yapmış olması gerekir ve yalnızca kendi rota verileri görüntülenir.

6. **Bildirimleri Görüntüleme** (Ayşenur Laklak)
    - **API Metodu:** `GET /notifications`
    - **Açıklama:** Kullanıcıya ait bildirimlerin listesini görüntülemesini sağlar. Bildirimler; plan hatırlatmaları, yaklaşan etkinlikler, rota değişiklikleri veya sistem bilgilendirmeleri gibi içerikleri kapsayabilir. Kullanıcı yalnızca kendi hesabına ait bildirimleri görüntüleyebilir.

7. **Bildirim Düzenleme** (Ayşenur Laklak)
    - **API Metodu:** `PUT /notifications/:notifId`
    - **Açıklama:** Kullanıcının mevcut bir bildirim kaydı üzerinde düzenleme yapmasını sağlar. Bildirim içeriği, hatırlatma zamanı, bildirim durumu veya bildirim tercihleri güncellenebilir. Güvenlik açısından kullanıcı yalnızca kendi bildirim kayıtlarını düzenleyebilir.

8. **Bildirim Silme** (Ayşenur Laklak)
    - **API Metodu:** `DELETE /notifications/:notifId`
    - **Açıklama:** Kullanıcının bildirim listesindeki bir bildirimi kaldırmasını sağlar. Silinen bildirim kullanıcı arayüzünde artık görüntülenmez ve bildirim listesi güncellenir. Kullanıcı yalnızca kendi bildirim kayıtlarını silebilir.

9. **Bildirim Ekleme** (Ayşenur Laklak)
    - **API Metodu:** `POST /notifications`
    - **Açıklama:** Kullanıcıya ait yeni bir bildirim kaydı oluşturulmasını sağlar. Bildirim; başlık, içerik, tarih-saat, hatırlatma türü ve ilgili plan/rota bağlantısı gibi bilgiler içerebilir. Bu özellik, kullanıcıya seyahat planı ile ilgili önemli hatırlatmaların zamanında iletilmesini destekler.

10. **Bildirim Detayı Görüntüleme** (Ayşenur Laklak)
    - **API Metodu:** `GET /notifications/:notifId`
    - **Açıklama:** Kullanıcının seçtiği bir bildirimin detaylarını görüntülemesini sağlar. Bildirim detayında başlık, içerik, oluşturulma zamanı, hatırlatma zamanı ve ilgili plan/rota bağlantısı gibi bilgiler yer alabilir. Kullanıcı yalnızca kendi bildirim kayıtlarının detaylarına erişebilir.