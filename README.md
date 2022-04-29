# Machine-Learning-Dimension-Reduction
BTK AKADEMY Training eğitimleri kapsamında hazırlanan jupyter Notebooklar bulunmaktadır.

İŞLENEN KONULAR :

1. 202200501_Boyut İndirgeme Analizi (PCA-LDA).ipynb çalışmasında ;
   A. STANDART SACALING İLE ÖLÇEKLEME 
   B. PCA İLE BOYUT KÜÇÜLTME
   C. LDA İLE BOYUT KÜÇÜLTME
   D. LOGISTIC REGRESYON İLE LDA VE PCA SINIFLANDIRMA
   E. CONFUSION MATRIX İLE KARMAŞIKLIK MATRİSİ

#                     BOYUT İNDİRGEME  / DIMENSION REDUCTION                 :
------------------------------------------------------------------------------
1. BOYUT DÖNÜŞTÜRME GEREKSİZ BOYUTLARDAN KURTULMA VEYA BAZILARINI BİRLEŞTİRME 
2. DEĞİŞKENLER ARASINDAKİ BAĞLANTI (KORELASYONLARI ORTAYA ÇIKARMA)
3. EIGEN VALUE : ÖZ DEĞER (SKALAR),
4. EIGEN VECTOR : ÖZ YÖNEY (VEKTÖR)
        
+1 2 +0      1       3 (1*1 +2*1+0*1)           1
+0 1 +2   *  1   =   3                  =    3  1
-1 0 -2      0       0                          0

BURADA ;

ÇARPAN +3 ÖZ DEĞER,
VEKTOR [1,1,0] ÖZ YÖNEY

1. PCA (PRINCIPAL COMPANANT ANALYSIS- BİRİNCİL BİLEŞEN ANALİZİ) ALGORİTMASI    :
-----------------------------------------------------------------------------
UNSUPERVISED GÖZETİMSİZ YAPIDADIR. CLUSTERING VARDIR. SINIF ETİKETLERİ IGNORE EDİLMEKTEDİR.

1. İNDİRGENECEK BOYUT : K OLSUN
2. VERİ STANDARTLAŞTIRMASI YAP
3. KOVARYANS VE KORELASYON MATRİSİNDEN ÖZ DEĞER VE ÖZ YÖNEY ELDE ET.
4. ÖZ DEĞERLERİ AZALARAK SIRALA VE K TANESİNİ AL.
5. K ÖZDEĞERDEN W PROJESİ MATRIX OLUŞTUR.
6. ORJİNAL VERİ KUMESİ [X] ; W KULLANARAK DÖÜŞTÜR VE K-BOYUT UZAY ELDE ET.

2. LDA (LINEAR DISCRIMINANT ANALYSİS- DOĞRUSAL AYRIŞMA ANALİZİ) ALGORİTMASI    :
-----------------------------------------------------------------------------
SUPERVISED GÖZETİMLİ YAPIDADIR. ETİKETLİ VERİLER OLUR. VERİLERİN SINIFLARINI AYRIŞTIRIR.
sebastianraschka.com sayfasında detaylı LDA makalesi mevcuttur.

VERİ SINIFLARININ AYRIŞTIRILMASI HARİÇ PCA İLE AYNIDIR. 

NEREDE KULLANILACAK                                                          :
------------------------------------------------------------------------------
1. GÜRÜLTÜ FİLTERELEME : ANOMALİYE KAŞI DERENÇ OLUŞTURUR.
2. GÖRSELLEŞTİRME
3. ÖZ NİTELİK ÇIKARIMI : FEATURE EXTRACTION
4. ÖZ NİTELİK NİTELİK ELEME YADA DÖNÜŞTÜRME : GEREKSİZ FEATURE VARSA ELEME YAPILIR.
5. BORSA ANALİZİ
6. SAĞLIK VE GENETİK VERİLER 
7. YER BİLİMİ GEO SCIENCE VB....
