1. **Üye Olma**
    - **API Metodu:** `POST /auth/register`
    - **Açıklama:** Kullanıcıların yeni hesaplar oluşturarak sisteme kayıt olmasını sağlar. Kişisel bilgilerin toplanmasını ve hesap oluşturma işlemlerini içerir. Kullanıcılar kullanıcı adı, email adresi ve şifre belirleyerek hesap oluşturur.

2. **Kullanıcı Bilgilerini Düzenleme**
    - **API Metodu:** `PUT /profile`
    - **Açıklama:** Kullanıcının profil bilgilerini güncellemesini sağlar. Kullanıcılar ad, soyad, email, doğum tarihi gibi kişisel bilgilerini değiştirebilir. Güvenlik için giriş yapmış olmak gerekir ve kullanıcılar yalnızca kendi bilgilerini güncelleyebilir.

3. **Kullanıcı Bilgisi Görüntüleme**
    - **API Metodu:** `GET /profile`
    - **Açıklama:** Kullanıcının kendi profil bilgilerini görüntülemesini sağlar. Ad, soyad, kullanıcı adı, email adresi, doğum tarihi gibi hesap bilgileri güvenli şekilde listelenir. Bu işlem için kullanıcının sisteme giriş yapmış olması gerekir ve yalnızca kendi profil verilerine erişebilir.

4. **Kimlik Doğrulama Metodu Oluşturma**
    - **API Metodu:** `POST /auth/2fa`
    - **Açıklama:** Kullanıcı hesabı için ek güvenlik amacıyla iki aşamalı kimlik doğrulama (2FA) yönteminin tanımlanmasını sağlar. Kullanıcı, doğrulama uygulaması veya benzeri bir doğrulama yöntemi ekleyerek hesabını daha güvenli hale getirebilir. Bu işlem yalnızca giriş yapmış kullanıcılar tarafından gerçekleştirilebilir.

5. **Kimlik Doğrulama Metodu Güncelleme**
    - **API Metodu:** `PUT /auth/2fa`
    - **Açıklama:** Kullanıcının daha önce tanımladığı iki aşamalı kimlik doğrulama (2FA) yöntemini güncellemesini sağlar. Kullanıcı mevcut doğrulama yöntemini değiştirebilir, yeniden yapılandırabilir veya yeni bir yöntem ile değiştirebilir. Güvenlik nedeniyle işlem sırasında kullanıcının kimliği tekrar doğrulanabilir.

6. **Favori Ekle**
    - **API Metodu:** `POST /favorites`
    - **Açıklama:** Kullanıcının beğendiği mekan, aktivite, gezi planı vs. favorilerine eklemesini sağlar. Böylece kullanıcı daha sonra bu içeriklere kolayca erişebilir ve kişisel bir favori listesi oluşturabilir. İşlem için kullanıcının giriş yapmış olması gerekir.

7. **Favori Silme**
    - **API Metodu:** `DELETE /favorites/:favoriteId`
    - **Açıklama:** Kullanıcının favori listesinde bulunan bir öğeyi kaldırmasını sağlar. Silinen favori kayıt, kullanıcının favori listesinden çıkarılır ve ilgili öğe artık favoriler ekranında görüntülenmez. Güvenlik için kullanıcı yalnızca kendi favori kayıtlarını silebilir.

8. **Favorileri Görüntüleme**
    - **API Metodu:** `GET /favorites`
    - **Açıklama:** Kullanıcının favori olarak kaydettiği mekan, aktivite, gezi planı vs. listesini görüntülemesini sağlar. Favoriler, kullanıcının daha sonra hızlı erişim sağlayabilmesi için tek bir liste halinde sunulur. Kullanıcı yalnızca kendi favori listesini görüntüleyebilir.

9. **Yapay Zeka Destekli Gezi Önerileri Sunma**
   - **API Metodu:** `POST /ai/trip-recommendations`
   - **Açıklama:** Kullanıcının tercihleri, seyahat amacı, bütçesi, süresi ve seçtiği destinasyon doğrultusunda kapsamlı gezi önerileri sunar. Yapay zeka; önerilen mekanlar, günlük plan taslakları, rota fikirleri, yapılabilecek aktiviteler ve dikkat edilmesi gereken noktalar gibi bilgileri içerebilir. Bu özellik, kullanıcıya seyahat planlamasının başlangıç aşamasında rehberlik eder ve hızlı bir plan oluşturmasına yardımcı olur.