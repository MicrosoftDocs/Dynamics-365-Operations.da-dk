---
title: Eksportér remburs
description: Denne procedure fører dig gennem processen med at eksportrembursen.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf06a73bf7665059658c7884a0b9f973929d647c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779548"
---
# <a name="export-letter-of-credit"></a>Eksportér remburs

[!include [banner](../../includes/banner.md)]

Denne procedure fører dig gennem processen med at eksportrembursen.

En remburs er en aftale, der udfærdiges af en bank, hvor banken accepterer at sikre betaling på vegne af køberen, hvis vilkårene i aftalen mellem køberen og sælgeren overholdes.



Kør proceduren **Konfigurere bankfaciliteter og posteringsprofiler** og **Remburs_Oprette en bankfacilitetsaftale** inden denne procedure. USMF-demovirksomheden skal være valgt for at køre denne procedure.


## <a name="create-sales-order-for-export-letter-of-credit"></a>Oprette salgsordre for remburs
1. Gå til **Debitor > Ordrer > Alle salgsordrer**.
2. Klik på **Ny**.
3. Klik på rullelisten i feltet **Kundekonto** for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Udvis eller skjul sektionen **Generelt**.
7. Klik på rullelisten i feltet **Sted** for at åbne opslaget.
    * Vælg den **Lokation**, hvor varen, som skal udleveres, opbevares.  
8. Klik op linket i den valgte række på listen.
9. Klik på rullelisten i feltet **Lagersted** for at åbne opslaget.
    * Vælg det **lagersted**, hvor varen, som skal udleveres, opbevares.  
10. Klik op linket i den valgte række på listen.
    * Bemærk! Vælg **Remburs** som værdi i feltet **Bankdokumenttype**.  
11. Vælg **Remburs** i feltet **Bankdokumenttype**.
12. Udvid eller skjul sektionen **Levering**.
    * Vælg **leveringsdatokontrol** = **Ingen**.  
13. Angiv en dato i feltet **Ønsket modtagelsesdato** .
14. Klik på **OK**.
15. Klik på rullelisten i feltet **Varenummer** for at åbne opslaget.
    * Vælg den ønskede vare, som skal være udleveres/sælges.  
16. Find og vælg den ønskede post på listen.
17. Klik op linket i den valgte række på listen.
18. Angiv et tal i feltet **Enhedspris**.
19. Udvid eller skjul sektionen **Linjedetaljer**.
20. Klik på fanen **Levering**.
21. Angiv en dato i feltet **Ønsket afsendelsesdato**.
22. Angiv en dato i feltet **Bekræftet afsendelsesdato**.
23. Klik på **Administrer** i Handlingsrude.
24. Klik på **Remburs**.
25. Skriv en værdi i feltet **Bankdokumentnummer**.
26. Angiv dato og klokkeslæt i feltet **Udløbsdato**.
27. Udvid eller skjul sektionen **Bankoplysninger**.
28. Klik på rullelisten i feltet **Udstedende bank** for at åbne opslaget.
29. Klik op linket i den valgte række på listen.
30. Klik på rullelisten i feltet **Adviserende bank** for at åbne opslaget.
31. Find og vælg den ønskede post på listen.
32. Klik op linket i den valgte række på listen.
33. Klik på **Hent salgsordreforsendelser**.
34. Klik på **Udsted bankdokument**.
35. Luk siden.

## <a name="post-packing-slip"></a>Bogføre følgeseddel
1. Klik på **Pluk og pak** i handlingsruden.
2. Klik på **Bogfør følgeseddel**.
3. Udvid eller skjul sektionen **Parametre**.
4. Vælg **Alle**" i feltet **Antal**.
5. Udvid eller skjul sektionen **Konfiguration**.
6. Angiv en dato i feltet **Følgeseddeldato**.
7. Vælg Forsendelsesnummer.
8. Klik op linket i den valgte række på listen.
9. Klik på **OK**.
10. Klik på **OK**.

## <a name="post-sales-invoice"></a>Bogføre salgsfaktura
1. Klik på **Faktura** i handlingsruden.
2. Klik på **Faktura**.
3. Udvid eller skjul sektionen **Oversigt**.
4. Vælg **Forsendelsesnummer**.
5. Klik op linket i den valgte række på listen.
6. Udvid eller skjul sektionen **Konfiguration**.
7. Indtast en dato i feltet **Fakturadato**.
8. Klik på **OK**.
9. Klik på **OK**.

## <a name="shipment-document-submitted-status"></a>Afsendelsesstatus for forsendelsesdokument
1. Klik på **Administrer** i Handlingsrude.
2. Klik på **Remburs**.
3. Udvid eller skjul sektionen **Linjer**.
    * Bemærk! Feltet **Dokument sendt** skal indstilles til **Ja**.  

## <a name="verify-export-letter-of-credit"></a>Kontrollere remburs
1. Gå til **Likviditets- og bankstyring > Remburser > Eksportremburs og importinkasso**.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
    * Kontroller, at **forsendelsesstatus** for **eksportrembursenstatus** er **Faktureret**.  

## <a name="customer-payment"></a>Debitorbetaling
1. Gå til **Kreditor > Betalinger > Betalingskladde**.
2. Klik på **Ny**.
3. Markér den valgte række på listen.
4. Klik på rullelisten i feltet **Navn** for at åbne opslaget.
5. Klik op linket i den valgte række på listen.
6. Klik på **Linjer**.
7. Indtast en dato i feltet **Dato**.
8. I feltet **Konto** skal du angive de ønskede værdier.
9. Klik på **Udligning**.
10. Markér afkrydsningsfeltet på overskriften til Totaler.
    * Bemærk! Indstil feltet **Vis** til **Remburs**.  
11. Find og vælg den ønskede post på listen.
12. Markér eller fjern markeringen i afkrydsningsfeltet **Markér**.
13. Klik på **OK**.
14. Klik på fanen **Betaling**.
    * Kontroller oplysningerne om bankdokumentnummer og forsendelsesnummer  
15. Klik på **Bogfør**.

## <a name="verify-export-letter-of-credit-after-payment"></a>Kontrollere eksportrembursen efter betaling
1. Gå til **Likviditets- og bankstyring > Remburser > Eksportremburs og importinkasso**.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
    * Kontroller **Forsendelsesstatus** = **Betaling modtaget** og **Saldobeløb** = **0,00**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
