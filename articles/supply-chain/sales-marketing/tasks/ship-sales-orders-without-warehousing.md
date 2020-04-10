---
title: Sende salgsordrer uden lagerstyring
description: I dette emne beskrives, hvordan du opdaterer en salgsordre, når varerne er afsendt til kunden.
author: omulvad
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bd90767af741760b1fbd3fd5c2b4cbbae95a477
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146393"
---
# <a name="ship-sales-orders-without-warehousing"></a>Sende salgsordrer uden lagerstyring

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du opdaterer en salgsordre, når varerne er afsendt til kunden. Vejledningen gælder for den opfyldelsesstrøm, der ikke er konfigureret for lagerstedsstyring (hverken grundlæggende eller avancerede lagerfunktioner) og derfor ikke kræver, at produktplukning registreres før afsendelse. Du kan køre procedure på dine egne data eller i demofirmaet USMF. I begge tilfælde skal du, før du starter denne opgave, oprette en salgsordre for et lagerført produkt med et antal større end 1. For at undgå en bogføringsfejl skal du kontrollere, at produktets disponible antal i lokationen og på lagerstedet, som du har valgt i ordren, dækker ordreantallet.

## <a name="post-packing-slip-for-an-order"></a>Bogføre følgeseddel for en ordre
1. Gå til **Moduler > Salg og marketing > Salgsordrer > Alle salgsordrer** i navigationsruden.
2. Find og vælg den ordre på listen, du har oprettet til denne opgave.
3. Vælg **Pluk og pak** i handlingsruden.
4. Vælg **Bogfør følgeseddel**.
5. Udvid eller skjul sektionen **Parametre**.
6. Vælg **Alle**" i feltet **Antal**.
    - Andre muligheder omfatter **Levér nu** og **Plukket**. Hvis ordrelinjen er delvist leveret og feltet **Levér nu** på ordrelinjen indeholder en mængde, skal du vælge **Levér nu**. Hvis din organisations opfyldelsesstrøm indeholder pluk som en separat proces, der styres af og registreres i en plukliste, skal du vælge **Plukket**.  
    - Kontroller, at indstillingen **Bogføring** er indstillet til **Ja**.  
7. Sæt indstillingen **Udskriv følgeseddel** til **Ja**. Fanen **Oversigt** indeholder en liste over følgesedler, der skal genereres i denne postering. Hvis du leverer en enkelt ordre, vil der typisk være én følgeseddel. Men hvis denne ordres linjer skal leveres fra forskellige steder, opdeles bogføringen automatisk i det rette antal dokumenter. Dette er en obligatorisk betingelse, der ikke kan ændres. På samme måde opdeles bogføringen også i flere dokumenter, hvis ordrelinjerne skal leveres til forskellige leveringsadresser, og politikken for levering er indstillet til at kræve en opdeling.  
8. Vælg rækken for ordrelinjen, der skal sendes, under fanen **Linjer**.
9. Skriv et tal, der er lavere end den oprindelige mængde, i feltet **Opdater**.
10. Vælg **OK**.
11. Vælg **Ja**.
12. Luk siden.
13. Vælg **Indstillinger** i handlingsruden.
14. Vælg **Skift visning**.
15. Vælg **Overskriftsvisning**.
    - Hvis alle linjer i ordren er fuldt leveret, ændres ordrestatus fra åben til leveret.  
    - I dette eksempel er ordrelinjen leveret delvist. Det er grunden til, at ordrestatus forbliver åben.     
    - Feltet **Dokumentstatus** er indstillet til Følgeseddel, fordi mindst én af ordrelinjerne er blevet leveret.  
16. Vælg **Generelt** i handlingsruden.
17. Vælg **Linjeantal**.
18. Luk siden.
19. Vælg **Pluk og pak** i handlingsruden.
20. Vælg **Følgeseddel**. Siden **Følgeseddelkladde** indeholder alle følgeseddeldokumenter, der oprettes for din ordre. Du kan gennemse detaljerne for hvert dokument og udskrive dem, hvis du ønsker.  

