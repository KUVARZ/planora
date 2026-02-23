1. **Giriş Yapma** 
   - **API Metodu:** `POST /auth/login`
   - **Açıklama:** Kullanıcıların sisteme giriş yaparak hizmetlere erişmesini sağlar. Email adresi, şifre ve 2FA ile kimlik doğrulama yapılır. Başarılı giriş sonrası kullanıcıya erişim izni verilir ve kişisel verilerin güvenliği sağlanır.

2. **Şifre Sıfırlama** 
    - **API Metodu:** `POST /password-reset`
    - **Açıklama:** Şifresini unutan veya değiştirmek isteyen kullanıcıların şifre sıfırlama işlemini başlatmasını sağlar. Kullanıcı email adresini girerek sıfırlama talebi oluşturur ve doğrulama adımlarını tamamladıktan sonra yeni bir şifre belirleyebilir. Bu süreç, hesap güvenliğini koruyacak şekilde güvenli doğrulama mekanizmaları ile yürütülür.

3. **Kullanıcı Adı Doğrulama** 
    - **API Metodu:** `GET /username-check`
    - **Açıklama:** Kullanıcının seçtiği kullanıcı adının sistemde kullanılabilir olup olmadığını kontrol eder. Kayıt veya profil güncelleme sırasında aynı kullanıcı adının birden fazla kişi tarafından kullanılmasını engellemeye yardımcı olur. Uygunluk durumuna göre kullanıcıya geçerli veya kullanımda bilgisi döndürülür.

4. **Takvim Planı Oluşturma** 
    - **API Metodu:** `POST /calendar`
    - **Açıklama:** Kullanıcının seyahat planı kapsamında belirli bir gün ve saat için takvim kaydı oluşturmasını sağlar. Plan içerisinde mekan, aktivite, saat aralığı, notlar ve ilgili öneriler gibi bilgiler yer alabilir. Bu özellik sayesinde kullanıcı seyahat programını gün bazlı ve düzenli şekilde planlayabilir.

5. **Takvim Planı Düzenleme** 
    - **API Metodu:** `PUT /calendar/:planId`
    - **Açıklama:** Kullanıcının oluşturduğu takvim planı kayıtlarını güncellemesini sağlar. Kullanıcı planın tarihini, saatini, aktivite bilgisini, mekan bilgisini veya notlarını değiştirebilir. Güvenlik açısından kullanıcı yalnızca kendi oluşturduğu plan kayıtlarını düzenleyebilir.

6. **Takvim Planı Silme** 
    - **API Metodu:** `DELETE /calendar/:planId`
    - **Açıklama:** Kullanıcının oluşturduğu takvim planı kayıtlarından birini silmesini sağlar. Silinen plan kaydı takvim görünümünden kaldırılır ve ilgili günün programı güncellenmiş şekilde gösterilir. Kullanıcı yalnızca kendi takvim planlarını silebilir.

7. **Takvim Planı Görüntüleme** 
    - **API Metodu:** `GET /calendar/:planId`
    - **Açıklama:** Kullanıcının belirli bir takvim planı kaydının detaylarını görüntülemesini sağlar. Plan kaydında tarih, saat, mekan, aktivite, notlar ve varsa yapay zeka tarafından önerilen içeriklere ait bilgiler gösterilebilir. Kullanıcı yalnızca kendi plan kayıtlarının detaylarına erişebilir.

8. **Takvim Görüntüleme** 
    - **API Metodu:** `GET /calendar`
    - **Açıklama:** Kullanıcının oluşturduğu tüm takvim planlarını gün, hafta veya ay bazında görüntülemesini sağlar. Takvim üzerinde hangi günlerde hangi etkinliklerin planlandığı listelenir ve kullanıcı seyahat programını bütüncül olarak takip edebilir. Bu işlem için kullanıcının giriş yapmış olması gerekir ve yalnızca kendi takvim verileri görüntülenir.


9. **Yapay Zeka Destekli Aktivite Önerisi Sunma** 
    - **API Metodu:** `POST /ai/activity-recommendations`
    - **Açıklama:** Kullanıcının ilgi alanları, bütçe aralığı, seyahat süresi, konum bilgisi ve geçmiş tercihlerine göre kişiselleştirilmiş aktivite önerileri oluşturur. Yapay zeka; kültürel, eğlence, doğa, gastronomi gibi farklı kategorilerde öneriler sunabilir. Öneriler, kullanıcının mevcut rota ve takvim planları ile uyumlu olacak şekilde hazırlanabilir.