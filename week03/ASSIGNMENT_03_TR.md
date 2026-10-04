# 3. Hafta Ödevi — Sunum, Akran İncelemesi, Teklif Bölüm B

**Teslim:** ders içi bölüm dersin son push'una kadar (11:50) · kalanı Cumartesi 23:59 · Proje reponuza commit edin

> **Dersten önce:** `PITCH_03.md` dosyanız yazılmış ve push edilmiş olmalı. Dersin ilk
> saati onu sunmakla geçer — o sırada yazacak zaman yok. Bilgisayarınızı şarjı dolu
> getirin; sunumu ondan yapacaksınız.

Geçen hafta ne yapacağınıza karar verdiniz. Bu hafta üç sınıf arkadaşınız bu karar
hakkında ne düşündüğünü söyler, siz neyi değiştireceğinize karar verirsiniz ve teklifin
ikinci yarısını yazarsınız — neden yapmaya değer olduğunu ve sizi neyin durdurabileceğini
anlatan yarısını.

---

## Bu hafta gelenler

Denetleyiciyi bir kez çalıştırın:

```bash
python .github/check_deliverables.py
```

`week03/PITCH_03.md`, `week03/contributors_03.json` ve `week03/ai_log_03.md` gelir.
`PROPOSAL.md` zaten sizde; Bölüm B (§8–§12) ve Değişiklik günlüğü onun içinde, sizi
bekliyor.

---

## Dersten önce — `week03/PITCH_03.md`

Beş dakikalık sunumunuz, altı slayt, Markdown olarak: dosya sunumun **kendisidir**, her
`---` yeni bir slayttır. VS Code'da açın; **Marp for VS Code** eklentisi onu slayt olarak
gösterir (sağ üstte önizleme düğmesi) ve isterseniz PDF ya da PPTX'e aktarır. Eklenti
olmadan VS Code'un normal Markdown önizlemesi de sunum için yeterlidir.

Altı slayt, her birinin yönergesi dosyanın içinde:

1. ürün tek cümleyle;
2. **sorun en son ne zaman oldu** — size ya da gözünüzün önünde — tarih, yer, kim, onun yerine ne yaptı;
3. **9. haftada test edecek beş gerçek kişi** — ad, nereden tanıdığınız;
4. yaptığı üç şey, yapmadığı bir şey;
5. ana ekran, **elle çizilmiş** (fotoğraf `week03/` içinde) ya da metinle;
6. emin olmadığınız tek şey.

7. slayt sabittir: değerlendirenlerinizin cevaplayacağı üç soru.

**Kendiniz yazın — bu dosyada yapay zekâ yok.** Ne metin, ne yapı. Bu slaytlardaki her
şey sizin hayatınız ve sizin çevreniz hakkında; bir asistan bunu bilemez ve ben grupta ya
da derste herhangi bir slaytı sorabilirim. Haftanın geri kalanı farklı: orada yapay zekâ
her zamanki gibi bir araçtır ve `ai_log_03.md` onu kullanmanızı ister.

2. ve 3. slaytların arkasında iki kural var ve dönem boyunca geçerli: **proje sizin bir
sorununuzu çözer — kendinizin, üniversitedeki arkadaşlarınızın ya da sosyal çevrenizin**
ve **çevrenizdeki gerçek kişiler tarafından kullanılabilir** — Atlas'ta, ailenizde, bir
kulüpte — çünkü 9. haftada o kişiler test edecek ve onlara ihtiyacınız olacak. Sorunun en
son ne zaman olduğunu ya da ürünü kullanacak beş kişiyi
söyleyemiyorsanız sorun slaytta değil projededir: projeyi şimdi değiştirin, bunun ucuz
olduğu son hafta bu.

---

## Derste — 11:50'ye kadar push

### 1. İnceleme turu — dörtlü gruplar, ilk saat

Dört kişilik grubunuzu dersin başında kendiniz kurarsınız; reposu henüz olmayan bir öğrenci üç kişilik bir gruba katılır. Herkes kendi bilgisayarından beş dakika sunar;
diğer üçü dinler, sonra 7. slayttaki üç sorunun her biri için birer cümle **yazar** —
kâğıda ya da bir metin dosyasına — ve sunana verir. Dört tur, yaklaşık 45 dakika. Ne
düşünüyorsanız söyleyin; nazik bir "iyi olmuş" kimseye yardım etmez, kimseye puan
getirmez.

**Bu grup, dönemin geri kalanında sizin grubunuzdur.** 4. Hafta'dan itibaren dördünüz
**her hafta, ders ile Cumartesi arasında, bir saatlik bir çevrimiçi toplantı** yaparsınız
— Teams, Meet, Discord, ne isterseniz — ve her biriniz o hafta projesinde neyin değiştiğini
anlatır; diğer üçü ne düşündüğünü söyler. O andan sonra `weekNN/contributors_NN.json`
içindeki üç kayıt bu toplantıdan gelir: kim ne dedi, alıntıyla, ve siz ne yaptınız.
Toplantıda olmayan biri için kimse o üç kaydı yazamaz; toplantıyı kaçırmak kendiliğinden
görünür. İlkini bu hafta yapabilirsiniz.

### 2. `week03/contributors_03.json` — üç değerlendiren

Üç değerlendireniniz, rol `reviewer`, öğrenci numaraları ve her biri için **yazdığı en
yararlı cümle** — özetlenmiş değil, alıntılanmış. Sonra `accepted: true` ya da `false`
ve `why`. Bir öneriyi gerekçeyle reddetmek olur; her şeyi kabul edip neyin değiştiğinin
izi olmaması olmaz. Adını yazdığınız her değerlendiren geçen haftaki gibi katkı bonusu
kazanır.

### 3. `PROPOSAL.md` — Bölüm A gözden geçirilmiş, Değişiklik günlüğü başlamış

Üç cevap önünüzdeyken §1–§7'yi yeniden okuyun ve incelemenin değiştirdiğini değiştirin.
Her değişiklik dosyanın sonundaki Değişiklik günlüğüne **tarihli bir satır**: ne değişti,
hangi bölümde, neden — "2026-10-08 — §4: grup sohbeti çıkarıldı; iki değerlendiren
WhatsApp'ın yanında kimsenin kullanmayacağını söyledi". Teklif değişebilir; sessizce
değişemez.

`requirements.json` bu hafta da değişebilir — ekleyin, çıkarın (id kalır, `"dropped":
true`), yeniden yazın. **Cumartesiden itibaren bir id'nin anlamı hiç değişmez**; listenin
kendisi 5. Hafta sonuna kadar açık kalır ve prototip incelemesinden sonra taban çizginiz
(baseline) olur.

### 4. Push

```bash
python .github/check_deliverables.py
git add .
git commit -m "week03: pitch, review, proposal revised"
git push
```

İnceleme turundan sonra ve dersin son push'unda, **11:50**'de bir kez daha push edin — her zamanki 10:00 / 11:00 / 11:50. Hemen ardından her repoyu donduruyorum. Push edilmeyen yoktur.

---

## Cumartesi 23:59'a kadar

### 5. `PROPOSAL.md` — Bölüm B, §8–§12

Neden yapmaya değer olduğunu söyleyen yarı. Her bölümün dosya içinde NEDEN'i, NE'si ve
zayıf/güçlü örneği var; StudyRoom örnekleri devam ediyor.

- **§8 Pazar ve hedef kullanıcılar** — kim, kaç kişi, nereden biliyorsunuz. 3. slayttaki
  beş test kullanıcınız bu bölümün ilk satırı.
- **§9 Rakipler** — sorunu bugün çözen üç şey; kâğıt liste de sayılır.
- **§10 Karşılaştırma ve üstünlüğünüz** — küçük bir tablo, kullanıcının ölçütleri, tek cümle.
- **§11 Ticari potansiyel** — kendini nasıl finanse eder; "ticari niyet yok, değeri X"
  gerekçelendirirseniz dürüst bir cevaptır.
- **§12 Teknik riskler** — 11. haftaya kadar sizi durdurması en olası üç şey, her biri
  için plan ve yedek. **Seçtiğiniz mağaza (S0)** burada adıyla, ücretiyle, inceleme ya da
  test süresiyle yazılır: karar vermeden `AI_PLATFORMS_AND_STORES_TR.md` dosyasını okuyun.

### 6. Yapay zekâyı düşman gözüyle okutun — `week03/ai_log_03.md`

Bu hafta asistan, hayır demek isteyen yatırımcıyı oynar. Bölüm B'nizi verin ve en güçlü
üç itirazı isteyin. Sonra **birini teklifte cevaplayın** ve **birinin yanlış olduğunu
gösterin** — kanıtla: bir sayı, bir kaynak, kontrol ettiğiniz bir şey. Yazışmayı
yapıştırın. "Yararlı geri bildirim verdi" diyen bir günlük puan getirmez.

### 7. Yeniden push, kontroller yeşil

Haftaya yayılmış commit'ler, ne değiştiğini söyleyen mesajlar. Denetleyicinin istediği
her şey aşağıda.

---

## Teslim listesi

**Dersten önce**
- [ ] `week03/PITCH_03.md` — altı slayt dolu, sizin yazdığınız, push edilmiş

**Derste, 11:50'ye kadar**
- [ ] `week03/contributors_03.json` — üç değerlendiren, her birinden alıntı bir cümle, accepted/why
- [ ] `PROPOSAL.md` §1–§7 incelemenin değiştirdiği yerlerde gözden geçirilmiş
- [ ] `PROPOSAL.md` Değişiklik günlüğü — en az bir tarihli satır

**Cumartesiye kadar**
- [ ] `PROPOSAL.md` §8–§12 dolu; §12 mağazayı, ücretini ve inceleme süresini adlandırıyor
- [ ] `week03/ai_log_03.md` — üç itiraz, biri teklifte cevaplanmış, birinin yanlışlığı gösterilmiş, yazışma yapıştırılmış
- [ ] `requirements.json` güncel — bundan sonra bir id'nin anlamı değişmez
- [ ] GitHub'da kontroller yeşil; 1. ve 2. hafta hâlâ geçiyor

---

## Bu hafta değil

Kod yok, tasarım belgeleri henüz yok (4. hafta), ortam kurulumu yok. Mağaza hesabı
açmayın; §12'de mağazayı adlandırmak yeter.

---

## Bu hafta nasıl notlanıyor

**Ders sonu — 5 puan.** Sunum push edilmiş ve tam, üç değerlendiren gerçek cümlelerle,
Değişiklik günlüğü başlamış — 11:50 push'undaki reponuzdan okunur.

**Cumartesi 23:59 — 5 puan.** Son durumda kontroller yeşil: **2**. İnsan katkısı: **2** —
kanıtıyla `ai_log_03.md` ve arkasında gerçek cümleler, gerçek kararlar olan incelemeler.
Commit disiplini: **1** — haftaya yayılmış, aralarında gerçek ilerleme olan commit'ler.

**Katkı bonusu.** Adını yazdığınız her değerlendiren haftalık notunuzun %10'unu kazanır;
siz de verdiğiniz incelemeler için aynısını kazanırsınız. 4. Hafta'dan itibaren isimler grubunuzdur.

**Bir öğrenci, bir bilgisayar, bir GitHub hesabı.** Arkadaşınızın bilgisayarında ya da
onun oturumunda yapılan iş ders için puan getirmez.
