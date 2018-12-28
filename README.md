# Access Hastane Veri Tabanı
## By Alperen AKKAYA

Access Hastane Veri Tabanı İlişkiler:

![Preview](https://i.imgur.com/AQKExgl.png)


İller
------
IlId - PK <br>
IlAdı <br>
IlPlaka <br>

İlceler
--------
IlceId - PK <br>
IlceAdi <br>
IlId (IlId) <br>

Kangrubu
---------
KanGrubuId - PK <br>
KangrubuAdi <br>

Ilaclar
--------
Barkod - PK <br>
IlacAdi <br>
İçerikBilgi <br>
Fiyat <br>

Hastaneler
-----------
HastaneId - PK <br>
HastaneAdi <br>
Telefon -- 05000000000 / 02120000000 => 11 Hane <br>
IlceId (IlceId) <br>

Polikinlikler
--------------
PolikinlikId - PK <br>
PolikinlikAdi <br>
RandevuSure <br>
HastaneId (HastaneId) <br>
 
Kurumlar
---------
KurumId - PK <br>
KurumAdi <br>
Iskonto <br>

OdemeTurleri
------------
OdemeTuruId - PK <br>
OdemeTuru <br>

Unvanlar
---------
UnvanId - PK <br>
UnvanAdi <br>
PersonelTuru <br>

Personel
---------
PersonelId - PK <br>
SicilNo <br>
Ad <br>
Soyad <br>
DiplomaNo <br>
Adres <br>
Cinsiyet <br>
EvTel -- 05000000000 / 02120000000 11 Hane <br>
CepTel <br>
Email <br>
DogumTarihi <br>
DogumYeri <br>
UnvanId (UnvanId) <br>
KlinikId (PolikinlikId) <br>
HastaneId (HastaneId) <br>

TestGruplari
-------------
TestGrupId - PK <br>
TestGrupAdi <br>

Test
-----
TestId <br>
TestAdi <br>
Ucret <br>
TestGrupAdi (TestGrupId) <br>

Hastalar
---------
HastaId - PK <br>
Ad <br>
Soyad <br>
SicilNo <br>
AdresEvTel -- 05000000000 / 02120000000 => 11 Hane <br>
IsTel <br>
CepTel <br>
TCKimlikNo  -- 11111111111 =>11 hane <br>
DogumTarihi <br>
Cinsiyet <br>
MedeniHali <br>
Meslek <br>
OncekiSoyad <br>
VergiNo <br>
KayitTarihi <br>
KurumId (KurumId) <br>
KanGrubuId (KanGrubuId) <br>
Kayitilid (IlId) <br>
KayitliIlceId (IlceId) <br>
DogumYeriId (IlId) <br>

hastagecmisi
-------------
GecmisId - PK <br>
Tarih <br>
Aciklama <br>
SurekliKullanilanIlaclar <br>
GecirdigiHastaliklar <br>
GecirdigiAmeliyatlar <br>
SahipOlduguAlerjiler <br>
HastaId (HastaId) <br>

randevular
-----------
RandevuId - PK <br>
Tarih <br>
Saat <br>
Dakika <br>
Geldimi <br>
HastaId (HastaId) <br>
DoktorId (PersonelId) <br>
PolikinlikId (PolikinlikId) <br>

hastakabul
-----------
HastaKabulId - PK <br>
GelisTarihi <br>
Sikayet <br>
Durum <br>
CikisTarihi <br>
HastaId (HastaId) <br>
DoktorId (PersonelId) <br>
PolikinlikId (PolikinlikId) <br>
RandevuId (RandevuId)  -- Randevusuz => randevusuzda gelebilirler <br>

hastasikayetleri
-----------------
HastaSikayetId - PK <br>
Tarih <br>
HastaSikayeti <br>
HastaKabulId (HastaKabulId) <br>
HastaId (HastaId) <br> 

muayeneler
-----------
MuayeneId - PK <br>
Tarih <br>
HastaKabulId (HastaKabulId) <br>
DoktorId (PersonelId) <br>
HastaSikayetId (HastaSikayetId) <br>

Odemeler
---------
OdemeId - PK <br>
Tarih <br>
OdemeTuruId (OdemeTuruId) <br>
Aciklama <br>
Net <br>
Indirim <br> 
Toplam <br>

tahliler
----------
TahlilId - PK <br>
TahlilAdi <br>

muayenesonuc
-------------
MuayeneSonucId - PK <br>
MuayeneId (MuayeneId) <br>
Aciklama <br>
IstenenTahlilId (TahlilId) <br>

tahlilersonuc
--------------
TahlilSonucId <br>
Aciklama <br>
Durum <br> 
Sonuc <br>
Miktar <br>
Toplam <br>
TahlilId (TahlilId) <br>
TestId (TestId) <br>

teshisler
----------
TeshisId - PK <br>
Tarih <br>
Teshis <br>
DoktorId (PersonelId) <br>
MuayeneId (MuayeneId) <br>

receteler
----------
ReceteNo - PK <br>
Tarih <br>
KurumId (KurumId) <br>
DoktorId (PersonelId) <br>
HastaId (HastaId) <br>

recetelersatirlari
-------------------
SatirId - PK <br>
IlacAdi <br>
Dozu <br>
KullanimSekli <br>
Adet <br>
Fiyat <br>
Toplam <br>
ReceteNo (ReceteNo) <br>
Barkod (Barkod) <br>
