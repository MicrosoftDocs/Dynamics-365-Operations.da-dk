---
title: Garantipostering
description: Denne procedure gennemgår garantiprocessen.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05abad6898c2b97cf66abdff21b30407dacd6488
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141781"
---
# <a name="letter-of-guarantee-transaction"></a>Garantipostering

[!include [banner](../../includes/banner.md)]

Denne procedure gennemgår garantiprocessen.



Følgende opgaver skal være fuldført, før du fuldfører denne procedure:

- Konfigurere bankfaciliteter og posteringsprofiler for en garanti.

- Opret en bankfacilitetsaftale for en garanti.



Denne procedure bruger demofirmaet USMF.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Oprette salgsordre med Garanti
1. Gå til Debitor > Ordrer > Alle salgsordrer.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kundekonto.
4. Udvid afsnittet Generelt.
5. Indtast eller vælg en værdi i feltet Lokation.
6. Klik op linket i den valgte række på listen.
7. Indtast eller vælg en værdi i feltet Lagersted.
8. Klik op linket i den valgte række på listen.
9. Vælg Garanti i feltet Bankdokumenttype.
10. Klik på OK.
11. Indtast eller vælg en værdi i feltet Varenummer.
12. Angiv et tal i feltet Enhedspris.
13. Vis eller skjul sektionen Linjedetaljer.
14. Klik på fanen Levering.
    * Bemærk! Vælg leveringsdatokontrol = Ingen  
15. Angiv en dato i feltet Ønsket afsendelsesdato.
16. Angiv en dato i feltet Bekræftet afsendelsesdato.

## <a name="process-letter-of-guarantee_request"></a>Behandle garanti_Anmodning
1. Klik på Administrer i handlingsruden.
2. Klik på Garanti.
3. I handlingsruden skal du klikke på Garanti.
4. Klik på Anmodning for at åbne dialogboksen.
5. Indtast eller vælg en værdi i feltet Type.
6. Klik op linket i den valgte række på listen.
7. Angiv et tal i feltet Værdi.
8. Angiv dato og klokkeslæt i feltet Udløbsdato.
9. Klik på OK.
10. Luk siden.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Behandle anmodning om garanti_Send til bank
1. Gå til Kontant- og bankstyring > Garantier > Garantier.
2. Find og vælg den ønskede post på listen.
3. Klik på Send til bank for at åbne dialogboksen.
4. Indtast eller vælg en værdi i feltet Bankkonto.
5. Klik op linket i den valgte række på listen.
6. Klik på OK.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Behandle garanti_Modtag fra bank
1. Klik på Modtag fra bank for at åbne dialogboksen.
2. Skriv en værdi i feltet Banknummer.
    * Kontrollér værdierne i de beregnede avance- og udgiftsfelter.  
3. Klik på OK.
4. Udvid afsnittet Handlinger.
    * Kontroller posten "Modtag fra bank".  
5. Klik for at følge linket i feltet Kladdebatchnummer.
6. Klik på Linjer.
    * Kontrollér bogføringen af kladdeposteringer.  
7. Luk siden.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Behandle garanti_Giv til modtager
1. Gå til Debitor > Ordrer > Alle salgsordrer.
2. Klik op linket i den valgte række på listen.
3. Klik på Administrer i handlingsruden.
4. Klik på Garanti.
5. I handlingsruden skal du klikke på Garanti.
6. Klik på Giv til modtager for at åbne dialogboksen.
7. Klik på OK.
8. Gå til Kontant- og bankstyring > Garantier > Garantier.
9. Find og vælg den ønskede post på listen.
10. Klik på Giv til modtager for at åbne dialogboksen.
11. Klik på OK.
12. Udvid afsnittet Handlinger.
    * Valider 'Giv til beneficiant'-posten.  

## <a name="process-letter-of-guarantee_increase-value"></a>Behandle garanti_Opskriv værdi
1. Gå til Debitor > Ordrer > Alle salgsordrer.
2. Klik op linket i den valgte række på listen.
3. Klik på Administrer i handlingsruden.
4. Klik på Garanti.
5. I handlingsruden skal du klikke på Garanti.
6. Klik på Opskriv værdi for at åbne dialogboksen.
7. Indtast et tal i feltet Værdi, der skal tilføjes.
8. Klik på OK.
9. Gå til Kontant- og bankstyring > Garantier > Garantier.
10. Find og vælg den ønskede post på listen.
11. Klik på Opskriv værdi for at åbne dialogboksen.
12. Klik på OK.
13. Udvid afsnittet Handlinger.
    * Kontroller posten 'Opskriv værdi'.  
14. Find og vælg den ønskede post på listen.
15. Klik for at følge linket i feltet Kladdebatchnummer.
16. Klik på Linjer.
    * Kontrollér de bogførte kladdeposteringer.  

## <a name="process-letter-of-guarantee_liquidate"></a>Behandle garanti_Udfør afvikling
1. Gå til Debitor > Ordrer > Alle salgsordrer.
2. Klik op linket i den valgte række på listen.
3. Klik på Administrer i handlingsruden.
4. Klik på Garanti.
5. I handlingsruden skal du klikke på Garanti.
6. Klik på Udfør afvikling for at åbne dialogboksen.
7. Klik på OK.
8. Gå til Kontant- og bankstyring > Garantier > Garantier.
9. Find og vælg den ønskede post på listen.
10. Klik på Udfør afvikling for at åbne dialogboksen.
11. Klik på OK.
12. Udvid afsnittet Handlinger.
    * Kontroller posten 'Udfør afvikling'.  
13. Find og vælg den ønskede post på listen.
14. Klik for at følge linket i feltet Kladdebatchnummer.
15. Klik på Linjer.
    * Kontrollér de bogførte kladdeposteringer.  
16. Luk siden.

