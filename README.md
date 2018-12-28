# Access Hastane Veri Tabanı
## By Alperen AKKAYA

Access Hastane Veri Tabanı İlişkiler:

![Preview](https://i.imgur.com/AQKExgl.png)


İller
------
IlId - PK
IlAdı
IlPlaka

İlceler
--------
IlceId - PK
IlceAdi
IlId (IlId)

Kangrubu
---------
KanGrubuId - PK
KangrubuAdi

Ilaclar
--------
Barkod - PK
IlacAdi
İçerikBilgi
Fiyat

Hastaneler
-----------
HastaneId - PK
HastaneAdi
Telefon -- 05000000000 / 02120000000 => 11 Hane
IlceId (IlceId)

Polikinlikler
--------------
PolikinlikId - PK
PolikinlikAdi
RandevuSure
HastaneId (HastaneId)

Kurumlar
---------
KurumId - PK
KurumAdi
Iskonto

OdemeTurleri
------------
OdemeTuruId - PK
OdemeTuru

Unvanlar
---------
UnvanId - PK
UnvanAdi
PersonelTuru

Personel
---------
PersonelId - PK
SicilNo
Ad
Soyad
DiplomaNo
Adres
Cinsiyet
EvTel -- 05000000000 / 02120000000 11 Hane
CepTel
Email
DogumTarihi
DogumYeri
UnvanId (UnvanId)
KlinikId (PolikinlikId)
HastaneId (HastaneId)

TestGruplari
-------------
TestGrupId - PK
TestGrupAdi

Test
-----
TestId
TestAdi
Ucret
TestGrupAdi (TestGrupId)

Hastalar
---------
HastaId - PK
Ad
Soyad
SicilNo
AdresEvTel -- 05000000000 / 02120000000 => 11 Hane
IsTel
CepTel
TCKimlikNo  -- 11111111111 =>11 hane
DogumTarihi
Cinsiyet
MedeniHali
Meslek
OncekiSoyad
VergiNo
KayitTarihi
KurumId (KurumId)
KanGrubuId (KanGrubuId)
Kayitilid (IlId)
KayitliIlceId (IlceId)
DogumYeriId (IlId)

hastagecmisi
-------------
GecmisId - PK
Tarih
Aciklama
SurekliKullanilanIlaclar
GecirdigiHastaliklar
GecirdigiAmeliyatlar
SahipOlduguAlerjiler
HastaId (HastaId)

randevular
-----------
RandevuId - PK
Tarih
Saat
Dakika
Geldimi
HastaId (HastaId)
DoktorId (PersonelId)
PolikinlikId (PolikinlikId)

hastakabul
-----------
HastaKabulId - PK
GelisTarihi
Sikayet
Durum
CikisTarihi
HastaId (HastaId)
DoktorId (PersonelId)
PolikinlikId (PolikinlikId)
RandevuId (RandevuId)  -- Randevusuz => randevusuzda gelebilirler

hastasikayetleri
-----------------
HastaSikayetId - PK
Tarih
HastaSikayeti
HastaKabulId (HastaKabulId)
HastaId (HastaId)

muayeneler
-----------
MuayeneId - PK
Tarih
HastaKabulId (HastaKabulId)
DoktorId (PersonelId)
HastaSikayetId (HastaSikayetId)

Odemeler
---------
OdemeId - PK
Tarih
OdemeTuruId (OdemeTuruId)
Aciklama
Net
Indirim
Toplam

tahliler
----------
TahlilId - PK
TahlilAdi

muayenesonuc
-------------
MuayeneSonucId - PK
MuayeneId (MuayeneId)
Aciklama
IstenenTahlilId (TahlilId)

tahlilersonuc
--------------
TahlilSonucId
Aciklama
Durum
Sonuc
Miktar
Toplam
TahlilId (TahlilId)
TestId (TestId)

teshisler
----------
TeshisId - PK
Tarih
Teshis
DoktorId (PersonelId)
MuayeneId (MuayeneId)

receteler
----------
ReceteNo - PK
Tarih
KurumId (KurumId)
DoktorId (PersonelId)
HastaId (HastaId)

recetelersatirlari
-------------------
SatirId - PK
IlacAdi
Dozu
KullanimSekli
Adet
Fiyat
Toplam
ReceteNo (ReceteNo)
Barkod (Barkod)

