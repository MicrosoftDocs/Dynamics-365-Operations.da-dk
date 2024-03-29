---
title: Importér remburs
description: Denne procedure fører dig gennem processen med at importere en remburs.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a79b3c391c15099aee0a8d34419e1cf48fafbc
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803985"
---
# <a name="import-letter-of-credit"></a>Importér remburs

[!include [banner](../../includes/banner.md)]

Denne procedure fører dig gennem processen med at importere en remburs. Følgende skal være konfigureret, før du udfører denne procedure: bankfaciliteter, posteringsprofiler, en bankfacilitetsaftale og oplysninger om kreditorbank.

Denne procedure bruger demofirmaet USMF.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Oprette en indkøbsordre med remburs
1. Gå til **Kreditorer > Indkøbsordrer > Alle indkøbsordrer**.
2. Klik på **Ny**.
3. Indtast eller vælg en værdi i feltet **Kreditorkonto**.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Udvid sektionen **Generelt**.
7. Indtast eller vælg en værdi i feltet **Sted**.
8. Klik op linket i den valgte række på listen.
9. Indtast eller vælg en værdi i feltet **Lokation**.
10. Klik op linket i den valgte række på listen.
11. Angiv en dato i feltet **Regnskabsdato**.
12. Angiv en dato i feltet **Leveringsdato**.

>[!Note] 
>Vælg **Remburs** som værdi i feltet **Bankdokumenttype**.  

13. Klik på **OK**.
14. Indtast eller vælg en værdi i feltet **Varenummer**.
15. Find og vælg den ønskede post på listen.
16. Klik op linket i den valgte række på listen.
17. Vis eller skjul sektionen **Linjedetaljer**.
18. Klik på fanen **Levering**.
19. Angiv en dato i feltet **Leveringsdato**.
20. Angiv en dato i feltet **Bekræftet leveringsdato**.
21. Angiv et tal i feltet **Enhedspris**.
    * Definer oplysninger om rembursen.  
22. Klik på **Administrer** i Handlingsrude.
23. Klik på **Remburs/importindsamling**.
24. Angiv en dato og et klokkeslæt i feltet **Ansøgningsdato**.
    * Kontroller, at feltet **Bankkonto** har den aktive standardbankkonto, der er baseret på ansøgningsdatoen.  
25. Skriv en værdi i feltet **Bankdokumentnummer**.
26. Angiv en dato og et klokkeslæt i feltet **Modtagelsesdato**.
27. Udvid sektionen **Bankdokument**.
28. Angiv dato og klokkeslæt i feltet **Udløbsdato**.
29. Udvid sektionen **Bankoplysninger**.
30. Indtast eller vælg en værdi i feltet **Adviserende bank**.
31. Klik op linket i den valgte række på listen.
32. Klik på **Gem**.
33. Klik på **Hent indkøbsordreforsendelser**.
34. Luk siden.
35. Klik på **Køb** i handlingsruden.
36. Klik på **Bekræft**.
37. Klik på **Administrer** i Handlingsrude.
38. Klik på **Remburs/importindsamling**.
39. Klik på **Behandl**.
40. Klik på **Bekræft**.
    * Kontroller, at facilitetssaldoen reducerer beløbet på indkøbsordren. I dette eksempel er Købsbeløb = 500,00 Facilitetsgrænse = 10000,00, og derfor er Facilitetssaldo = 9500,00.  
41. Luk siden.
42. Angiv et tal i feltet **Enhedspris**.
43. Klik på **Gem**.
44. Klik på **Køb** i handlingsruden.
45. Klik på **Bekræft**.
    * Rediger rembursen på grund af ændring i enhedsprisen.  
46. Klik på **Administrer** i Handlingsrude.
47. Klik på **Remburs/importindsamling**.
    * Rediger rembursen på grund af ændring i Købsenhedspris.  
48. Klik på **Behandl**.
49. Klik på **Rediger**.
50. Klik på **Fjern**.
51. Klik på **Ja**.
52. Klik på **Hent indkøbsordreforsendelser**.
53. Klik på **Behandl**.
54. Klik på **Bekræft**.
    * Kontroller, at facilitetssaldoen reducerer beløbet på indkøbsordren. I dette eksempel er redigeret Købsbeløb = 600,00 Facilitetsgrænse = 10000,00, og derfor er Facilitetssaldo = 9400,00.  
55. Luk siden.

## <a name="post-packing-slip"></a>Bogføre følgeseddel
1. Klik på **Modtag** i handlingsruden.
2. Klik på **Produktkvittering**.
3. Skriv en værdi i feltet **PurchParmTable_Num**.
    * Vælg det **Forsendelsesnummer**, der blev oprettet med reference til rembursen.  
4. Klik op linket i den valgte række på listen.
5. Angiv en dato i feltet **Produktkvittering**.
6. Klik på **OK**.
7. Luk siden.
8. Luk siden.

## <a name="verify-import-letter-of-credit-status"></a>Bekræfte status for importremburs
1. Gå til **Likviditets- og bankstyring > Remburser > Importremburs og importinkasso**.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
    * Bekræft **Status for importrembursen**.     
4. Luk siden.
5. Luk siden.

## <a name="post-purchase-invoice"></a>Bogføre købsfaktura
1. Gå til **Kreditorer > Indkøbsordrer > Alle indkøbsordrer**.
    * Vælg den indkøbsordre, der blev oprettet med remburs.  
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Klik på **Faktura** i handlingsruden.
5. Klik på **Faktura**.
6. Skriv en værdi i feltet **Nummer**.
7. Indtast eller vælg en værdi i feltet **Forsendelsesnummer**.
8. Klik op linket i den valgte række på listen.
9. Indtast en dato i feltet **Fakturadato**.
10. Klik på **Opdater status for match**.
11. Klik på **Bogfør**.
12. Luk siden.
13. Luk siden.

## <a name="verify-import-letter-of-credit-status-and-printing"></a>Bekræfte kreditstatus for importremburs og udskrivning

1. Gå til **Likviditets- og bankstyring > Remburser > Importremburs og importinkasso**.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
    * Bekræft importrembursen2.  
    * Valider:  **Forsendelsesstatus** = **Faktureret**  Oplysninger om bankfacilitet  
4. Klik på **Vis**.
5. Klik på **Udskriv ansøgning**.
6. Klik på **OK**.
    * Kontroller, at rembursansøgningen bliver udskrevet.  
7. Luk siden.
8. Luk siden.
9. Luk siden.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Bogføre kreditorbetalingskladde for indkøbsordre, der er oprettet med remburs
1. Gå til **Kreditor > Betalinger > Betalingskladde**.
2. Klik på **Ny**.
3. Indtast eller vælg en værdi i feltet **Navn**.
4. Klik op linket i den valgte række på listen.
5. Klik på **Linjer**.
6. Indtast en dato i feltet **Dato**.
7. I feltet **Konto** skal du angive de ønskede værdier.
8. Klik på **Udlign transaktioner**.
9. Udvid afsnittet **Totaler**.
10. Vælg en indstilling i feltet **Vis**.
    * Kontroller, at felterne **Bankdokumentnummer** og **Forsendelsesnummer** er blevet opdateret.  
11. Markér afkrydsningsfeltet **Markér**.
12. Klik på **OK**.
13. Klik på fanen Betaling.
    * Kontroller, at felterne **Bankdokumentnummer** og **Forsendelsesnummer** er blevet opdateret.  
14. Klik på **Bogfør**.
15. Luk siden.
16. Luk siden.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Bekræfte status for importremburs, når fakturaen er betalt
1. Gå til **Likviditets- og bankstyring > Remburser > Importremburs og importinkasso**.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
    * Bekræft **Status for importrembursen**.   
4. Luk siden.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Kontrollere rapport om bankfacilitetsgrænse og udnyttelse
1. Gå til **Likviditets- og bankstyring > Forespørgsler og rapporter > Remburser eller garanti > Bankfaciliteter og udnyttelse, rapport**.
2. Udvid sektionen **Poster, der skal indgå**.
3. Klik på **Filtrér**.
    * Definer feltet **Kriterier** med den ønskede bankkonto.  
4. Indtast eller vælg en værdi i feltet **Kriterier**.
5. Klik op linket i den valgte række på listen.
6. Klik på **OK**.
7. Klik på **OK**.
    * Kontroller den rapport, som viser posteringerne.  
    * Kontrol af rapporten viser posteringerne med bankdokumentnummer, facilitetsgrænse, udnyttet beløb og facilitetssaldobeløb.  
8. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
