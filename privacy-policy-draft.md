# Asia Follower — Gizlilik Politikası Taslağı

Durum: YAYINA HAZIR DEĞİL. Sunucu tarafı ve hizmet sağlayıcıları doğrulanmalıdır.
İnceleme tarihi: 30 Ekim 2026
Android paket adı: com.asiafollower.app
İletişim: tokafatma997@gmail.com

## Kapsam

Asia Follower Android uygulaması https://asiafollower.com/ web sitesini WebView
içinde gösterir. Bu taslak, uygulama kaynak kodu ve incelenen ana sayfa betiklerinde
gözlenen davranışları kapsar. Sunucu tarafının tamamı incelenmediğinden eksiksiz
bir gizlilik politikası olarak kullanılamaz.

## Gözlenen veri akışları

- Girilen Instagram kullanıcı adı, profil araması için asiafollower.com üzerindeki
  /get_instagram_profile.php uç noktasına sorgu parametresi olarak gönderilir.
- Giriş alanı en az üç karakter içerdiğinde 1,5 saniyelik beklemeden sonra arama
  otomatik başlayabilir; düğmeye basmak zorunlu değildir.
- Yanıttaki profil adı, fotoğraf URL'si ve varsa takipçi sayısı arayüzde gösterilir.
- Sayfa yüklenince /t.php adresine sayfa yolu, önceki sayfa adresi (referrer) ve
  zaman damgası gönderilir. Bu uç noktanın verileri nasıl kullandığı bilinmiyor.
- Başarılı aramadan sonra üç saniyelik sayaçla goodfollowers.in/user/ adresine
  geçiş yapılır. Kullanıcı adı, zaman damgası ve source=asiafollower bilgisi
  URL parametrelerinde aktarılır. Android uygulaması bu harici HTTPS yönlendirmesini
  sistem tarayıcısında açacak şekilde yapılandırılmıştır.
- Profil fotoğrafı, sunucu yanıtındaki URL üzerinden yüklenir; gerçek sağlayıcı
  ve alan adları bu incelemede doğrulanmadı.
- Ağ isteği yapılması, alıcı sunucunun bağlantı bilgilerini teknik olarak görmesini
  gerektirir; IP ve diğer bilgilerin loglanıp loglanmadığı henüz doğrulanmadı.

## Uygulamanın izinleri ve yerel davranışı

Uygulama internet erişimi kullanır. Kamera, mikrofon, konum veya rehber erişimi
istemek üzere bir özellik eklenmemiştir. JavaScript açıktır; DOM storage,
dosya ve içerik erişimi kapalıdır. Üçüncü taraf çerezleri kapalıdır; bu ayar,
birinci taraf çerezlerinin veya sunucu kayıtlarının bulunmadığı anlamına gelmez.
Native kaynaklarda ayrı reklam veya analiz SDK'sı görülmemiştir; web sitesi
tarafındaki tüm hizmetler hakkında aynı sonuç çıkarılamaz.

## Yayın öncesi tamamlanması gereken bilgiler

1. Gerçek hizmet işletmecisinin / veri sorumlusunun adı ve gerekiyorsa adresi.
2. Hosting, CDN, profil sorgulama ve görsel sağlayıcıları; işlenen veriler,
   alıcılar ve uluslararası aktarım bilgileri.
3. /t.php ve /get_instagram_profile.php dosyalarının davranışı, sunucu logları,
   veritabanı kayıtları ve çerezler; amaçlar ve hukuki dayanaklar.
4. goodfollowers.in işletmecisiyle ilişki, aktarılan verinin amacı ve sonraki akışlar.
5. Her veri türü için saklama süresi veya belirleme ölçütü; silme prosedürü.
6. Destek başvurularının işlenmesi ve saklanması; erişim, düzeltme ve silme talepleri.
7. Uygulamada veya sitede hesap oluşturulabiliyorsa hesap/veri silme yöntemi.
8. Hedef yaş grubu ve çocuk verileri uygulaması; gerçek güvenlik önlemleri.

Bu bilgiler tamamlanmadan bu dosya Play Console gizlilik politikası veya Veri
güvenliği formuna dayanak olarak kullanılmamalıdır. Gizlilik politikası yayımlandığında
herkese açık bir HTML URL'sinden ve uygulama içinden erişilebilir olmalıdır.
