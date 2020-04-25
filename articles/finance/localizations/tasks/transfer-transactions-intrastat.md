---
title: Overføre posteringer til Intrastat
description: Denne procedure viser dig, hvordan du kan konfigurere Intrastat-parametre og overføre transaktioner til Intrastat.
author: Anasyash
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fa397eb8dbce9418ca3da010e64165e0d399502
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139078"
---
# <a name="transfer-transactions-to-the-intrastat"></a>Overføre posteringer til Intrastat

[!include [banner](../../includes/banner.md)]

Denne procedure viser dig, hvordan du kan konfigurere Intrastat-parametre og overføre transaktioner til Intrastat. Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.


## <a name="create-new-and-update-existing-commodity-code"></a>Oprette en ny og opdatere en eksisterende varekode
1. Gå til **Moduler > Administration af produktoplysninger > Opsætning > Kategorier og attributter > Kategorihierarkier** i navigationsruden.
2. Søg på listen eller vælg posten **Koder for Intrastat-goder**.
3. Klik op linket i den valgte række på listen.
4. Vælg en post i træet. Vælg for eksempel **Intrastat\Speaker**.  
5. Klik på **Rediger**.
6. Udvid oversigtspanelet **Udenrigshandel**.
7. Indtast eller vælg en værdi i feltet **Supplerende enheder**. Vælg for eksempel **styk**.  
8. Vælg **Ja** i feltet **Vægt ikke gældende**.
9. Vælg **Intrastat** i træet.
10. Klik på **Ny kategorinode**.
11. Indtast navnet på godet i feltet **Navn**. Skriv for eksempel **Andet gode**.  
12. Indtast koden for godet i feltet **Kode**. Skriv for eksempel **995 00 00**.  
13. Indtast en værdi i feltet Brugervenligt navn. Skriv for eksempel **Andet**.  
14. Klik på **Gem**.
15. Luk siden.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Tildele varekode til et produkthierarki og et frigivet produkt
1. Brug quick-filteret til at finde poster. Du kan for eksempel filtrere på feltet **Navn** med værdien **salg**.
2. Klik op linket i den valgte række på listen.
3. Udvid **en kategorinode** i træet. Udvid for eksempel **Sales hierarchy\Home audio**.  
4. Vælg den **kategori, som skal tildeles koden for godet** i træet. Vælg for eksempel **Sales hierarchy\Home audio\Speakers.  
5. Udvid oversigtspanelet **Koder for gode**.
6. Klik på **Tilføj**.
7. I feltet **Vælg hierarki** skal du vælge **Intrastat**.
8. Find og vælg koden for godet på listen. Vælg for eksempel **920 20 34 Speaker**.  
9. Klik på pilen til højre for at vælge koden.
10. Klik på **OK**.
11. I navigationsruden skal du gå til **Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.
12. Vælg det frigivne produkt på listen, som du vil tildele til varekoden. Vælg for eksempel **D0001**.  
13. Klik på **Rediger**.
14. Udvid oversigtspanelet **Udenrigshandel**.
15. Indtast koden for godet i feltet **Gode**. Vælg for eksempel værdien **920 20 34 Speaker**.    
16. Indtast et tal i feltet **Gebyrprocent**. Indtast for eksempel **3**.  
17. Indtaste eller vælge et land eller område i feltet **Land/område**. Vælg for eksempel **AUT**.  
18. Udvid **Styr lager** på oversigtspanelet.
19. Indtast en vægt i kg i feltet **Nettovægt**. Indtast for eksempel **2,5**.  
20. Klik på **Gem**.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Oprette Intrastat-transaktionkoder og udenrigshandelsparametre
1. I navigationsruden skal du gå til **Moduler > Moms > Opsætning > Udenrigshandel > Transaktionskoder**.
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Transaktionskode**. Indtast for eksempel **21** for den transaktionkode, der anvendes som returværdi.  
4. Skriv navnet på transaktionskoden i feltet **Navn**. Indtast for eksempel **Returner**.  
5. Vælg en indstilling i feltet **Statistisk beløb**. Vælg for eksempel **Tom** for at angive, at den statistiske værdi, der skal rapporteres for transaktioner med transaktionskoden **21**, altid vil være nul.  
6. I navigationsruden skal du gå til **Moduler > Moms > Opsætning > Udenrigshandel > Parametre for udenrigshandel**.
7. Indtast eller vælg en værdi i feltet **Transaktionskode**. Vælg for eksempel **11**.  
8. Indtast eller vælg en værdi i feltet **Kreditnota**. Denne værdi identificerer også fysisk returnering. Kreditnotaen for den fysiske returnering overføres i Intrastat-kladden med modsat retning. Returneringen af modtagede varer overføres f.eks. som en forsendelse.   Ellers betragtes kreditnotaen som en rettelse, og den overføres med samme retning og modsat fortegn. Korrektion af varemodtagelse overføres f.eks. som en modtagelse med et negativt beløb og det aktive flag er indstillet til **Korrektion**.  
9. Udvid oversigtspanelet **Overførelse**.
10. Vælg **Ja** i feltet **Varer med varekode**. Vælg denne indstilling for at overføre transaktionerne med en tildelt varekode. Transaktioner uden en varekode bliver ikke** overført til Intrastat.  
11. Vælg en indstilling i feltet **Overfør ved opfyldelse af kriterium på**. Vælg for eksempel **En af de valgte**.  
12. Udvid sektionen **Varekodehieraki**.
13. Klik på fanen **Egenskaber for land/område**.
14. Klik på **Ny**.
15. Indtast eller vælg en værdi i feltet **Land/område**. Vælg for eksempel værdien **FRA**.  
16. I feltet **Intrastat-kode** skal du angive ISO-koden for landet/området.  Skriv for eksempel **FR**.  
17. Vælg **EU**i feltet **Lande-/områdetype**.
18. Klik på fanen Nummerserier.

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Konfigurere leveringsmåder og regler for at medtage gebyrer i Intrastat
1. I navigationsruden skal du gå til **Moduler > Salg og marketing > Opsætning > Distribution > Leveringsmetode**.
2. Find og vælg den ønskede post på listen. Vælg for eksempel **20 Air**.  
3. Udvid oversigtspanelet **Udenrigshandel**.
4. Klik på **Rediger**.
5. Indtast eller vælg en værdi i feltet **Transport**. Vælg for eksempel **02**.  
6. I navigationsruden skal du gå til **Moduler > Debitor > Konfiguration af gebyrer > Gebyrkoder**.
7. Brug quick-filteret til at finde poster. Filtrer for eksempel feltet Gebyrkode ud fra værdien **fragt**.
8. Udvid oversigtspanelet **Udenrigshandel**.
9. Klik på **Rediger**.
10. Vælg **Ja** i feltet **Intrastat-fakturaværdi**. Beløbet vil blive overført til feltet **Fakturagebyrer** og lægges til det beløb, der er overført i feltet Fakturabeløb. Vælg **Ja** i feltet **Værdi af Intrastat-statistik**, hvis antallet af ændringer skal overføres til feltet **Statistiske gebyrbeløb** og lægges til i feltet **Statistisk beløb**.  

## <a name="sell-products-for-eu-customers"></a>Sælge produkter til EU-debitorer
1. I navigationsruden skal du gå til **Moduler > Debitor > Ordrer > Alle salgsordrer**.
2. Klik på **Ny**.
3. Vælg en EU-kunde i feltet **Debitorkonto**. Vælg for eksempel **DE-012 Litware Retail**.  
4. Udvid oversigtspanelet **Levering**.
5. Indtast eller vælg en værdi i feltet **Leveringsmetode**. Vælg for eksempel **20 Air**.  
6. Klik på **OK**.
7. Vælg den første række af salgsordrelinjer.
8. Indtast eller vælg en værdi i feltet **Varenummer**. Vælg for eksempel **D001**.  
9. Vis eller skjul oversigtspanelet **Linjedetaljer**.
10. Klik på fanen **Udenrigshandel**. Transporten udfyldes automatisk fra den valgte leveringsmetode.  
11. Indtast eller vælg en værdi i feltet **Havn**.
12. Klik på **Finanser**. I henhold til indstillingerne skal dette beløb medtages i **Intrastat-fakturaværdi**.  
13. Klik på **Fasthold gebyrer**.
14. Indtast eller vælg en værdi i feltet **Gebyrkode**. Vælg for eksempel **FRAGT**.  
15. Vælg **Behold** i afkrydsningsfeltet.
16. Indtast et tal i feltet **Gebyrværdi**. Indtast for eksempel **10**.  
17. Klik på **Gem**.
18. Luk siden.
19. Klik på **Faktura** i handlingsruden.
20. Klik på **Faktura**.
21. Udvid sektionen **Parametre**.
22. Vælg **Alle**" i feltet **Antal**.
23. Udvid oversigtspanelet **Opsætning**.
24. Indtast en dato i feltet **Fakturadato**. Indtast for eksempel **31-01-2015**.  
25. Klik på **OK**.
26. Klik på **OK**.
27. Luk siden.
28. Klik på **Ny**.
29. Vælg en EU-kunde i feltet **Debitorkonto**. Vælg for eksempel **DE-013 Trey Wholesales**.
30. Klik på **OK**.
31. Indtast eller vælg en værdi i feltet **Varenummer**. Vælg for eksempel **D0001**.  
32. Klik på **Gem**.
33. Klik på **Faktura**.
34. Indtast en dato i feltet **Fakturadato**. Indtast for eksempel datoen **31-01-2015**.  
35. Klik på **OK**.
36. Klik på **OK**.

## <a name="transfer-transactions-to-the-intrastat"></a>Overføre transaktioner til Intrastat
1. I navigationsruden skal du gå til **Moduler > Moms > Deklareringer > Udenrigshandel > Intrastat**.
2. Klik på **Overfør**.
3. Vælg **Ja** i feltet **Debitorfaktura**.
4. Klik på **Filtrér**.
5. Markér rækken **Dato** på listen.
6. Skriv en værdi i feltet **Kriterier**. Angiv for eksempel filteret for perioden januar 2015 (den nøjagtige værdi afhænger af dit datoformat): 1/1/2015..31/1/2015  
7. Klik på **OK**.
8. Klik på **OK**.
9. Find og vælg den overførte post på listen.
10. Klik på fanen **Generelt**.
    
Gennemse overførte data, herunder land/område for destination/afsendelse, oprindelsesland/område, vægt, antal, antal i supplerende enheder, varekode, transaktionskode, fakturabeløb og statistiske beløb. Du kan ændre data, hvis det er nødvendigt.  

