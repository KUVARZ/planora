1. **Kullanıcı Tercihi Ekleme**
    - **API Metodu:** `POST /preferences`
    - **Açıklama:** Kullanıcının seyahat planlamasında kullanılmak üzere kişisel tercih bilgilerini sisteme eklemesini sağlar. Tercihler; bütçe aralığı, ilgi alanları, ulaşım tercihi, yemek tercihleri, aktivite türleri veya konaklama beklentileri gibi bilgileri içerebilir. Bu bilgiler, yapay zeka destekli önerilerin kullanıcıya daha uygun şekilde sunulmasına yardımcı olur.

2. **Kullanıcı Tercihi Güncelleme**
   - **API Metodu:** `PUT /preferences/:prefId`
   - **Açıklama:** Kullanıcının daha önce kaydettiği tercih bilgilerinde değişiklik yapmasını sağlar. Kullanıcı bütçe, ilgi alanı, ulaşım, yemek veya aktivite tercihlerini güncelleyerek öneri sonuçlarını kendi ihtiyaçlarına göre yeniden şekillendirebilir. Güvenlik açısından kullanıcı yalnızca kendi tercih kayıtlarını düzenleyebilir.

3. **Kullanıcı Tercihi Silme**
   - **API Metodu:** `DELETE /preferences/:prefId`
   - **Açıklama:** Kullanıcının kayıtlı tercih bilgilerinden birini sistemden kaldırmasını sağlar. Silinen tercih kaydı artık öneri oluşturma sürecinde dikkate alınmaz ve kullanıcı tercih listesinde görüntülenmez. Kullanıcı yalnızca kendi tercih kayıtlarını silebilir.

4. **Kullanıcı Tercihleri Görüntüleme**
   - **API Metodu:** `GET /preferences`
   - **Açıklama:** Kullanıcının sisteme kaydettiği tüm tercih bilgilerini liste halinde görüntülemesini sağlar. Kullanıcı bu ekran üzerinden mevcut tercihlerini inceleyebilir ve ihtiyaç duyduğunda güncelleme veya silme işlemlerine erişebilir. Bu işlem için kullanıcının giriş yapmış olması gerekir ve yalnızca kendi tercih verileri görüntülenir.

5. **Gezi Noktası Ekleme**
   - **API Metodu:** `POST /route/:routeId/places`
   - **Açıklama:** Kullanıcının mevcut bir rota içerisine yeni bir gezi noktası eklemesini sağlar. Gezi noktası kaydı; mekan adı, konum bilgisi, ziyaret sırası, tahmini süre, kategori ve notlar gibi bilgileri içerebilir. Bu özellik sayesinde kullanıcı rotasını daha detaylı ve kişiselleştirilmiş şekilde düzenleyebilir.

6. **Gezi Noktası Güncelleme**
   - **API Metodu:** `PUT /route/:routeId/places/:placeId`
   - **Açıklama:** Kullanıcının rota içerisinde yer alan bir gezi noktasının bilgilerini güncellemesini sağlar. Kullanıcı gezi noktasının adını, konumunu, sırasını, tahmini ziyaret süresini veya notlarını vs. değiştirebilir. Güvenlik açısından kullanıcı yalnızca kendi rotalarına ait gezi noktalarını düzenleyebilir.

7. **Gezi Noktası Silme**
   - **API Metodu:** `DELETE /route/:routeId/places/:placeId`
   - **Açıklama:** Kullanıcının rota içerisinde bulunan bir gezi noktasını kaldırmasını sağlar. Silinen gezi noktası rota planından çıkarılır ve rota sıralaması gerekli durumlarda güncellenir. Kullanıcı yalnızca kendi rotalarına ait gezi noktalarını silebilir.

8. **Gezi Noktası Görüntüleme**
   - **API Metodu:** `GET /route/:routeId/places/:placeId`
   - **Açıklama:** Kullanıcının rota içindeki belirli bir gezi noktasının detaylarını görüntülemesini sağlar. Gezi noktası detayında mekan adı, konum bilgisi, kategori, ziyaret süresi, sıra bilgisi ve kullanıcı notları gibi bilgiler yer alabilir. Kullanıcı yalnızca kendi rotalarına ait gezi noktalarının detaylarına erişebilir.

9. **Yapay Zeka Destekli Gezi Raporu Özeti Oluşturma**
   - **API Metodu:** `POST /ai/trip-summary`
   - **Açıklama:** Kullanıcının tamamladığı veya planladığı geziye ait rota, ziyaret edilen yerler, aktiviteler, süreler ve kullanıcı notları gibi verileri analiz ederek özet bir gezi raporu oluşturur. Yapay zeka; gezi boyunca yapılan aktiviteleri kronolojik olarak özetleyebilir, öne çıkan deneyimleri vurgulayabilir ve kullanıcıya paylaşılabilir bir metin sunabilir. Bu özellik, kullanıcıların seyahat deneyimlerini kaydetmesine ve başkalarıyla paylaşmasına yardımcı olur.