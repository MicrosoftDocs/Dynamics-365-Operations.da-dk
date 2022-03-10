---
title: Fakturasammenholdelse og interne indkøbsordrer
description: Den juridiske indkøbsenhed, der er involveret i en intern handelstransaktion kan konfigureres til at bruge kreditorfakturasammenholdelse. I dette tilfælde skal behovene for bogføring for både intern handel og kreditorfakturasammenholdelse opfyldes, før de interne kreditorfakturaer kan bogføres.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e884e96e1275f9162b642bbe48c2d891c6434002
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109962"
---
# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Fakturasammenholdelse og interne indkøbsordrer

[!include [banner](../includes/banner.md)]

Den juridiske indkøbsenhed, der er involveret i en intern handelstransaktion kan konfigureres til at bruge kreditorfakturasammenholdelse. Når feltet **Bogfør faktura med uoverensstemmelser** på siden **Kreditorparametre** er angivet til **Kræv godkendelse**, udføres validering af fakturasammenholdelse. I dette tilfælde skal behovene for bogføring for både intern handel og kreditorfakturasammenholdelse opfyldes, før de interne kreditorfakturaer kan bogføres.

I eksemplerne under dette emne benyttes følgende opsætning for intern handel:
-   Fabrikam Purchase er den juridiske indkøbsenhed.
-   Fabrikam Sales er den juridiske salgsenhed.
-   Debitor 4020 findes i Fabrikam Sales.
-   Kreditor 3024 findes i Fabrikam Purchase.
-   I Fabrikam Purchase er der angivet interne oplysninger for kreditor 3024. Fabrikam Sales er angivet som kundefirmaet, og kunde 4020 er angivet som den debitorkonto, der svarer til den juridiske Fabrikam Purchase-enhed.
-   I Fabrikam Sales er der angivet interne oplysninger for kreditor 4020. Fabrikam Purchase er angivet som kreditorfirmaet, og kreditor 3024 er angivet som den kreditorkonto, der svarer til den juridiske Fabrikam Sales-enhed.

I eksemplerne bruges følgende opsætning for kreditorfakturasammenholdelse for Fabrikam Purchase:
-   På siden **Kreditorparametre** er indstillingen **Aktivér validering af fakturasammenholdelse** markeret.
-   På siden **Kreditorparametre** er feltet **Bogfør faktura med uoverensstemmelser** indstillet til **Kræv godkendelse**.
-   Pristolerancen for den juridiske enhed er på 2 procent.

## <a name="example-price-matching-and-intercompany-trade"></a>Eksempel: Prissammenholdelse og intern handel
Nettobeløbene for den interne kreditorfaktura og den interne debitorfaktura skal være ens. Dette krav tilsidesætter de eventuelle godkendelser af fakturasammenholdelse eller pristoleranceprocenter, der måtte gælde. Benyt f.eks. følgende fremgangsmåde.
1.  Opret salgsordre SO888 for debitor 4020 i Fabrikam Purchase. Den interne indkøbsordre ICP0222 oprettes automatisk for kreditor 3024 i Fabrikam Purchase , og salgsordre ICSO888 oprettes automatisk i Fabrikam Sales.
2.  Registrer i Fabrikam Sales, at varerne er modtaget, og bogfør en følgeseddel. Statussen for ICSO888 skifter til Leveret. Statussen for ICP0222 skifter til Modtaget.
3.  Opdater en faktura for ICSO888 i Fabrikam Sales. Enhedsprisen er 0,45, og 100 varer opdateres.
4.  Opret en faktura til ICP0222 i Fabrikam Purchase. Du kommer utilsigtet til at ændre nettoprisen fra 45,00 til 54,00. Der vises et ikon, som angiver, at prisen overstiger den tilladte pristolerance på 2 procent.
5.  på siden **Detaljer om fakturasammenholdelse** skal du vælge indstillingen for at godkende bogføring med matchningsafvigelser. Klik på **OK** på siden **Kreditorfaktura**. Hvis kreditorfakturaen ikke var en intern kreditorfaktura, er bogføring korrekt gennemført. Men fordi du arbejder med en intern kreditorfaktura, er bogføringen ikke udført korrekt. I forbindelse med intern handel skal fakturatotaler på den interne salgsordre være lig med fakturatotaler på den tilsvarende interne indkøbsordre. Du kan løse dette problem ved at rette nettoprisen på fakturaen ved at ændre nettoprisen tilbage til standardbeløbet på 45,00.

## <a name="example-quantity-matching-with-intercompany-trade"></a>Eksempel: Antalssammenholdelse i intern handel
Antallene i den interne indkøbsordre og den interne salgsordre skal være ens. Dette krav tilsidesætter eventuelle godkendelser af fakturasammenholdelse, der måtte gælde. I dette eksempel bruges følgende yderligere opsætning af intern handel:
-   I Fabrikam Purchase er handlingspolitikken i forbindelse med indkøbsordrer for kreditor 3024 konfigureret til automatisk at bogføre både den oprindelige debitorfaktura og den interne indkøbsordrefaktura.

I dette eksempel bruges følgende yderligere opsætning af kreditorfakturasammenholdelse for Fabrikam Purchase:
-   På siden **Varemodelgrupper** for den modelgruppe, der bruges af vare B-R14, er indstillingen **Tilgangskrav** valgt.
-   Det disponible antal for vare B-R14 er 0 (nul).

Benyt f.eks. følgende fremgangsmåde.
1.  Opret salgsordre SO999 for debitor 4020 i Fabrikam Purchase. Ordren indeholder et linjeelement: 100 batterier (vare B-R14) til en enhedspris på 1,00 pr. styk. Den interne indkøbsordre ICPO333 oprettes automatisk i Fabrikam Purchase for kreditor 3024, og salgsordre ICSO999 oprettes automatisk i Fabrikam Sales.
2.  Udfør en fakturaopdatering af ICSO999 in Fabrikam Sales. Bogføringen er ikke lykkedes, fordi varen ikke er på lager og endnu ikke er blevet modtaget. Derfor kan de finansielle oplysninger ikke opdateres.
3.  Registrer, at varerne er modtaget, og bogfør en følgeseddel for ICS0999 i Fabrikam Sales. Der bogføres automatisk en produktkvittering for ICPO333 i Fabrikam Purchase. Det modtagne antal for vare B-R14 skifter til 100 i Fabrikam Purchase.
4.  Udfør en fakturaopdatering af ICSO999 in Fabrikam Sales. Bogføringen er korrekt udført i begge juridiske enheder. Det indkøbte antal af vare B-R14 skifter til 100 i Fabrikam Purchase.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
