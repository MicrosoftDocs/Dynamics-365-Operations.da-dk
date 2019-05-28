---
title: Sende salgsordrer uden lagerstyring
description: Denne vejledning viser, hvordan du opdaterer en salgsordre, når varerne er afsendt til kunden.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae70e09dbc4da90b7d1802d076384eae2d00da0e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555787"
---
# <a name="ship-sales-orders-without-warehousing"></a>Sende salgsordrer uden lagerstyring

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne vejledning viser, hvordan du opdaterer en salgsordre, når varerne er afsendt til kunden. Vejledningen gælder for den opfyldelsesstrøm, der ikke er konfigureret for lagerstedsstyring (hverken grundlæggende eller avancerede lagerfunktioner) og derfor ikke kræver, at produktplukning registreres før afsendelse. Du kan køre procedure på dine egne data eller i demofirmaet USMF. I begge tilfælde skal du, før du starter denne opgave, oprette en salgsordre for et lagerført produkt med et antal større end 1. For at undgå en bogføringsfejl skal du kontrollere, at produktets disponible antal i lokationen og på lagerstedet, som du har valgt i ordren, dækker ordreantallet.


## <a name="post-packing-slip-for-an-order"></a>Bogføre følgeseddel for en ordre
1. Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.
2. Find og vælg den ordre på listen, du har oprettet til denne opgave.
3. Klik op linket i den valgte række på listen.
4. Klik på fanen Pluk og pak i handlingsruden.
5. Klik på Bogfør følgeseddel.
6. Udvid eller skjul sektionen Parametre.
7. Vælg "Alle" i feltet Antal.
    * Andre muligheder omfatter Levér nu og Plukket. Hvis ordrelinjen er delvist leveret og feltet Levér nu på ordrelinjen indeholder en mængde, skal du vælge Levér nu. Hvis din organisations opfyldelsesstrøm indeholder pluk som en separat proces, der styres af og registreres i en plukliste, skal du vælge Plukket.  
    * Kontroller, at indstillingen Bogføring er indstillet til Ja.  
8. Sæt indstillingen Udskriv følgeseddel til Ja.
    * Fanen Oversigt indeholder en liste over følgesedler, der skal genereres i denne postering. Hvis du leverer en enkelt ordre, vil der typisk være én følgeseddel. Men hvis denne ordres linjer skal leveres fra forskellige steder, opdeles bogføringen automatisk i det rette antal dokumenter. Dette er en obligatorisk betingelse, der ikke kan ændres. På samme måde opdeles bogføringen også i flere dokumenter, hvis ordrelinjerne skal leveres til forskellige leveringsadresser, og politikken for levering er indstillet til at kræve en opdeling.  
9. Vælg rækken for ordrelinjen, der skal sendes, under fanen Linjer.
10. Skriv et tal, der er lavere end den oprindelige mængde, i feltet Opdater.
11. Klik på OK.
12. Klik på Ja.
13. Luk siden.
14. Klik på Indstillinger i handlingsruden.
15. Klik på Skift visning.
16. Klik på Overskriftsvisning.
    * Hvis alle linjer i ordren er fuldt leveret, ændres ordrestatus fra åben til leveret.  
    * I dette eksempel er ordrelinjen leveret delvist. Det er grunden til, at ordrestatus forbliver åben.     
    * Feltet Dokumentstatus er indstillet til Følgeseddel, fordi mindst én af ordrelinjerne er blevet leveret.  
17. Klik på Generelt i handlingsruden.
18. Klik på Linjeantal.
19. Luk siden.
20. Klik på fanen Pluk og pak i handlingsruden.
21. Klik på følgeseddel.
    * Siden Følgeseddelkladde indeholder alle følgeseddeldokumenter, der oprettes for din ordre. Du kan gennemse detaljerne for hvert dokument og udskrive dem, hvis du ønsker.  

