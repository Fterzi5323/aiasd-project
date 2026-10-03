# Yapay zekâ bir mühendislik aracı olarak — değerlendirme disiplini

*AIASD · Atlas Üniversitesi · 2026–27 Güz · Prof. Dr. Vedat Coşkun*
*`AI_Doc4`'ün (araçlar nedir, nasıl harcanır) devamı. Bu belge, araçların size verdiğiyle
ne yaptığınız hakkında. Sınav kapsamındadır: final sınavında bu belgeden soru çıkar.*

---

## 0. Tek cümle

Bu ders asistanın ne ürettiğini notlamaz. Üretileni sizin ne kadar iyi **tarif ettiğinizi,
kontrol ettiğinizi, düzelttiğinizi ve hesabını verdiğinizi** notlar. Bir asistan bir ödevin
istediği her dosyayı on dakikada yazabilir; haftalık `ai_log`'unuzun iki puanı, onu yanlış
yaparken yakaladığınız an için ödenir — kanıtı yapıştırılmış ve ne yaptığınız yazılmış
olarak.

Aşağıdakilerin her biri, o anı beklemek yerine bilerek üretmenin adlandırılmış bir
tekniğidir. Her haftanın ödevi beklediği tekniği adlandırır; §10'daki tablo bütün dönemi
gösterir. Hepsini her hafta kullanabilirsiniz — biri zorunludur.

---

## 1. Önce kabul ölçütü

**Ne.** Bir şey istemeden önce, cevabın doğru olduğunu nasıl anlayacağınızı yazın. İki üç
satır, kendi sözlerinizle, istemden *önce* — sonra istemin içine koyun.

**Neden.** Testi olmayan bir istek, makul görünen bir şey isteğidir. Modeller makul
görünende çok iyidir. "StudyRoom için bir veri modeli yaz" içinde `Payment` tablosu olan
derli toplu bir diyagram döndürür; "StudyRoom için veri modeli: en çok beş varlık, hiçbir
yerde para yok, bir rezervasyon kimin ne zaman check-in yaptığını bilmeli" satır satır
kontrol edebileceğiniz bir şey döndürür — ve kontrol zaten yazılmıştır.

**Zayıf.** *"Claude'dan veri modelini istedim, iyi görünüyordu, kullandım."*

**Güçlü.** *"Sormadan önceki ölçütler: ≤5 varlık, ödeme yok, check-in zamanı rezervasyonda.
İlk cevapta 7 varlık vardı, `Invoice` dahil. Ölçütleri yapıştırarak ikinci istem: 5
varlık, ama check-in `Reservation`'da değil `User`'daydı — yanlış, bir kullanıcının çok
rezervasyonu olur. Elle düzelttim; son model `docs/data_model.md`'de."*

**Günlükte.** Önce yazdığınız ölçütler, cevabın onlara karşı durumu, neyin takıldığı.

---

## 2. Okuyarak değil, çalıştırarak doğrulayın

**Ne.** Çalıştırılabilen her şey çalıştırılarak doğrulanır: kodu çalıştırın, isteği
gönderin, sayfayı telefonda açın, Mermaid'i önizlemeye yapıştırın. Okuyup başını sallamak
doğrulama değildir.

**Neden.** Üretilen kod, doğru çalıştığından çok daha sık doğru okunur. Asistan da onu hiç
çalıştırmamıştır; ona benzeyen çok kod görmüştür.

**Zayıf.** *"Copilot OTP endpoint'ini üretti. Kod doğru görünüyor."*

**Güçlü.** *"Endpoint'i çalıştırdım: aynı e-postayla 60 sn içinde ikinci istek reddetmek
yerine yeni kod döndürdü. Spesifikasyon (REQ-006) dakikada bir kod diyor. Traceback ve iki
yanıt aşağıda. Zaman damgası kontrolüyle düzelttim; test eklendi."*

**Günlükte.** Çalıştırdığınız komut, çıktı (yapıştırılmış, kırpılmış), düzeltme.

---

## 3. Düşman gözden geçiren

**Ne.** Asistana kendi işinizi ve bir rol verin: hayır demek isteyen yatırımcı, reddetmek
isteyen mağaza incelemecisi, kırmak isteyen testçi. En güçlü üç itirazı numaralı isteyin.
Sonra **birini belgede yanıtlayın** ve **birinin yanlış olduğunu kanıtla gösterin**.

**Neden.** "Bu iyi mi?" diye sorulan model evet der. "Bu neden başarısız olur?" diye
sorulan model bir liste üretir — ve her üç maddeden biri görmediğiniz gerçek bir sorundur.
Diğer ikisi, onunla gerekçeli olarak aynı fikirde olmamayı öğrendiğiniz yerdir.

**Zayıf.** *"ChatGPT'den teklifimi incelemesini istedim, yararlı geri bildirim verdi,
uyguladım."*

**Güçlü.** *"İtiraz 2: 'Kimse rezervasyonu elle girmez; içeri girer geçer.' Zemin kat
odaları için doğru — §4'e QR ile check-in ekledim. İtiraz 3: 'Kütüphanenin zaten bir
rezervasyon sistemi var.' Kontrol ettim: Atlas kütüphanesinde yok (bankoda sordum,
2026-10-07). Projeyi korudum; kontrolü §9'a yazdım."*

**Günlükte.** Üç itiraz aynen, hangisini nerede yanıtladığınız, hangisini hangi kanıtla
çürüttüğünüz.

---

## 4. Çapraz sorgu — iki asistan, tek istem

**Ne.** İki farklı asistana tam olarak aynı istemi ve aynı kaynak metninizi verin. İki
cevabı birbiriyle ve zaten bildiklerinizle karşılaştırın.

**Neden.** İki modelin uyuştuğu yerde bir adayınız vardır — bir gerçek değil. Ayrıştıkları
yerde en az biri yanlıştır; hangisinin yanlış olduğunu bulmak, gerçek kanıtlı gerçek bir
hataya giden en hızlı yoldur. Bu 2. Hafta'nın tekniğidir; bütün dönem işe yarar.

**Zayıf.** *"İkisi de benzer gereksinimler verdi, birleştirdim."*

**Güçlü.** *"Claude: 'rezervasyon check-in olmadan 15 dk sonra düşer'. Gemini: '2 saat
sonra'. İkisi de bana sormadı. Doğru sayı benim §3'ümde: sorun, giden insanların bütün
öğleden sonra tuttuğu odalar — 15 dk; kendi kabul testimle REQ-004 yaptım."*

**Günlükte.** İstem bir kez, iki cevap yan yana (kırpılmış), karar.

---

## 5. Kaynak gösterttirin — ve "bilmiyorum" demesine izin verin

**Ne.** Her olgusal iddianın kaynağını isteyin: bir belge, bir sayfa, kendi kodunuzdan bir
satır. "Bilmiyorum"un kabul edilebilir bir cevap olduğunu açıkça söyleyin. Sonra **kaynağı
açın**.

**Neden.** Modeller kaynakları da her şey kadar akıcı üretir; bir kısmı yoktur. Sizin
sohbet botunuz da (6. Hafta) kullandığı parçayı alıntılamasını sağlamazsanız kendi
belgeleriniz üzerinde aynısını yapar. Kontrol etmediğiniz bir olgu bildiğiniz bir olgu
değildir.

**Zayıf.** *"Yapay zekâya göre Google Play incelemesi 1–3 gün sürüyor."*

**Güçlü.** *"'1–3 gün'ün kaynağını istedim. Bir Play Console yardım sayfası verdi; açtım
(2026-10-08): sayfa 'yeni geliştirici hesapları için 7 güne kadar ya da daha uzun
sürebilir' diyor. §12 artık 7 gün diyor ve sayfayı kaynak gösteriyor. Aynısını Gemini'ye
sordum: güncel bir rakamı olmadığını söyledi — daha iyi cevap."*

**Günlükte.** İddia, verdiği kaynak, kaynağın gerçekte ne dediği.

---

## 6. Küçük diff'ler — bir seferde bir değişiklik, ve okuyun

**Ne.** Yeniden yazım değil, tek bir değişiklik isteyin. Kabul etmeden önce diff'i okuyun —
tamamını, değiştirilmesini istemediğiniz satırlar dahil. Kabul ettiğiniz her değişikliği
kendi başına commit edin.

**Neden.** "Bu dosyayı yeniden düzenle" istemediğiniz üç şeyin değiştiği, birinin sessizce
değiştiği bir dosya döndürür. İki dakikada okuyabildiğiniz bir diff sorumluluğunu
alabildiğiniz bir diff'tir; 5. Hafta incelemesinde commit geçmişinizi okunur kılan da budur.

**Zayıf.** *"Copilot'tan `app.py`'yi temizlemesini istedim, kabul ettim, push ettim."*

**Güçlü.** *"Yalnızca kullanılmayan import'ların gitmesini istedim. Diff ayrıca OTP
uzunluğunu 6'dan 4 haneye değiştirmişti — istenmemiş, söylenmemiş. O parçayı reddettim,
import'ları aldım. `ruff` doğruluyor; `e41c…` commit'i yalnızca import'lar."*

**Günlükte.** İstediğiniz değişiklik, aldığınız değişiklik, reddettiğiniz.

---

## 7. Üç katman arasında tutarlılık

**Ne.** Aynı özellik sunucuda, web istemcisinde ve mobil istemcide varsa, üçünü de asistana
verin ve tutarsızlığı bulmasını isteyin. Sonra bulduğunu doğrulayın ve kaçırdığını arayın.

**Neden.** Üretilmiş üç parça kendi içinde tutarlı, birbiriyle değildir: sunucuda
`room_id`, uygulamada `roomId`; sunucunun döndürebildiği ama hiçbir istemcinin ele almadığı
bir durum. Modeller istenince bunları iyi bulur, istenmeyince hiç bulmaz.

**Zayıf.** *"Üçünde de her şey çalışıyor."*

**Güçlü.** *"`server/api.py`, `web/app.js`, `mobile/api.dart` arasında uyumsuzluk istedim.
`checked_in` / `checkedIn`'i buldu — gerçek, düzeltildi. Sunucunun çifte rezervasyonda
`409 Conflict` döndürdüğünü ve mobil istemcinin 200 dışı her şeyi 'ağ hatası' saydığını
kaçırdı. Onu test ederek buldum (teknik 2); ele alma eklendi."*

**Günlükte.** Ne buldu, neyi doğruladınız, neyi kaçırdı ve nasıl buldunuz.

---

## 8. Tahmin ile gözlem

**Ne.** İnsanlarla yapılacak bir testten önce (9. Hafta beta, 10. Hafta UAT) asistana neyin
ters gideceğini sorun. Tahmini yazın. Testten sonra testçilerin gerçek hata listesini yanına
koyun.

**Neden.** Bir modelin kullanıcılarınız hakkında ne bildiğinin bu dersteki en temiz ölçümü
budur: genellikle bir şeyler, asla her şey. Aradaki fark, insan testinin isteğe bağlı
olmadığının kanıtıdır — ve test raporunuzu okunur kılan paragraftır.

**Zayıf.** *"Testçiler bazı hatalar buldu, düzelttim."*

**Güçlü.** *"Tahmin (5 madde): giriş kodunun gelmemesi, yavaş liste, …. Gözlem (5 testçiden
7 madde): tahmin edilen 5'ten 2'si; en büyük şikâyet — 'haritada hangi odanın benim
olduğunu anlayamıyorum' — kimsenin tahmininde yoktu. Tablo `docs/test_report.md`'de."*

**Günlükte.** Tahmin (tarihli, testten önce), gözlem listesi, örtüşme.

---

## 9. Karar kaydı — günlük ne içindir

`weekNN/ai_log_NN.md` dosyanız **bir sohbet dökümü değildir** ve yapay zekâyı ne kadar
kullandığınızın günlüğü de değildir. Haftada bir kararın mühendislik kaydıdır, dört parçayla:

| Parça | Yanıtladığı soru | Takıldığı yer |
|---|---|---|
| **Ne için kullandım** | Hangi asistan, hangi istem, hangi dosyanız üzerinde? | "Teklif için ChatGPT kullandım." |
| **Doğru yaptığı** | Neyi tuttunuz, neden doğruydu? | "Yardımcı oldu." |
| **Yanlış yaptığı** | Somut bir hata — haftanın tekniği onu üretti | "Bazı şeyler alakasızdı." |
| **Kanıt + düzeltme** | Yapıştırılmış çıktı ve elle yaptığınız değişiklik | Hiçbir şey yapıştırılmamış; "düzelttim." |

**Kanıt** bloğu, bir insanın ilk okuduğu kısımdır. Yapıştırılmıştır, önemli satırlara
kırpılmıştır ve hatayı gösterir — hatanın tarifini değil. Kanıtı olmayan bir günlük ne
kadar uzun olursa olsun hiçbir şey kazandırmaz.

Günlüğün taşıdığı iki kural daha:

- **Değişen plan yazılır.** Bıraktığınız bir gereksinim, sadeleştirdiğiniz bir katman,
  değiştirdiğiniz bir mağaza — `PROPOSAL.md`'nin değişiklik günlüğünde tarihli bir satır ya
  da günlükte bir satır, gerekçesiyle. Fikir değiştirmek mühendisliktir; sessizce
  değiştirmek değildir.
- **Bazı şeyler asistanla hiç yapılmaz.** Pitch'iniz (`PITCH_03.md`), sorunun en son
  başınıza geldiği an, ürününüzü test edecek beş kişi, değerlendirenlerinizin yazdığı
  cümleler ve onlar hakkında verdiğiniz kararlar. Bunlar sizin hayatınız ve sizin
  insanlarınızla ilgilidir; bir asistan bunları bilemez ve ben soracağım.

---

## 10. Dönem, teknik teknik

| Hafta | Tekniğin hizmet ettiği teslim | Zorunlu teknik |
|---|---|---|
| 2 | Teklif Bölüm A, gereksinimler | §4 Çapraz sorgu |
| 3 | Teklif Bölüm B | §3 Düşman gözden geçiren (yatırımcı) |
| 4 | Tasarım, veri modeli, prototip | §1 Önce kabul ölçütü |
| 5 | Sunucu iskeleti, OTP ile giriş | §2 Çalıştırarak doğrulama |
| 6 | Kendi belgeleriniz üzerinde sohbet botu motoru | §5 Kaynak gösterttirme |
| 7 | İstemcilerde sohbet botu, testler, CI | §6 Küçük diff'ler |
| 8 | Üç katmanda çekirdek özellik | §7 Katmanlar arası tutarlılık |
| 9 | Beta test, hata listesi, test raporu | §8 Tahmin ile gözlem |
| 10 | UAT raporu, gönderim | §5 Kaynak gösterttirme, kendi iddialarınız üzerinde |
| 11 | Yayın, inceleme düzeltmeleri | §3 Düşman gözden geçiren (mağaza incelemecisi) |
| 12 | Kapanış, poster | §9 Dönemin günlüğüne geriye bakış: en pahalıya mal olan hata |

Herhangi bir hafta ek olarak başka bir teknik de kullanılabilir. Haftanın `ai_log_NN.md`
iskeleti tekniğini en üstte adlandırır.

---

## 11. Kısa sürüm

Testi istemden önce yazın. Çalıştırılabileni çalıştırın. İyi mi diye değil, neden
başarısız olur diye sorun. İkisini birbirine düşürün. Kaynak gösterttirin ve kaynağı açın.
Bir şeyi değiştirin, diff'i okuyun. Tahmini sonucun yanına koyun. Kararı yazın, kanıtı
yapıştırın ve kendi hayatınızı asistanın elinden uzak tutun.

Hiç yanlış yaparken yakalanmamış bir asistan iyi bir asistan değildir; kimsenin kontrol
etmediği bir asistandır.
