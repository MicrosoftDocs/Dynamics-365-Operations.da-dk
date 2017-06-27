---
title: "Produktionsbogføring"
description: Denne artikel indeholder oplysninger om forskellige typer af posteringer i produktionsprocessen.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f1d46b7eba42640de09d85fbc18969ee2a85f280
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="production-posting"></a>Produktionsbogføring

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om forskellige typer af posteringer i produktionsprocessen.

Produktionsbogføringsaktiviteter følger produktionsprocesser, der er beskrevet i afsnittene nedenfor.

## <a name="material-consumption"></a>Materialeforbrug
Materialer registreres som forbrugt under produktionen, når produktionspluklistekladden bogføres. Denne proces opretter afgangsposteringer, der fratrækker den disponible lagerbeholdning. I produktionsparametrene kan du angive, om værdien af råvarer, der er igangværende (igangværende forarbejdning \[IGVA\]), skal bogføres i finans. Værdien af råvarer, der er igangværende (IGVA), bogføres derefter til en dedikeret pluklistekonto og en dedikeret pluklistemodkonto.

## <a name="time-consumption"></a>Tidsforbrug
Den tid, medarbejdere bruger på produktionsjob registreres i rutekortkladden eller jobkortkladden. Når disse kladder bogføres, behandles finanskontering på en dedikeret konto for ressourcer, der er igangværende (IGVA). Denne bogføring repræsenterer værdien af den tid, der bruges på produktionsordren. Når produktionsordren er registreret som afsluttet, udlignes IGVA-konti.

## <a name="reporting-finished-goods-and-error-quantities"></a>Rapportering af færdigvarer og mængden af fejl
Når en produktionsordre meldes færdig, opdateres mængden af færdigvarer, der er fuldført i Lagerstyring gennem rapporten som en færdigmeldingskladde. Hvis du bruger IGVA-regnskab, der kan konfigureres i produktionsparametrene, oprettes en finanskladde for at reducere IGVA-kontiene og øge lageret af færdigvarer. Kladden bruger de standardomkostninger, der er defineret for produktet.

## <a name="ending-the-production-order"></a>Afslutte produktionsordrer
Inden en produktionsordre afsluttes, beregnes de faktiske omkostninger for den mængde, der er produceret. Alle estimerede omkostninger til materialer, løn og indirekte omkostninger tilbageføres og erstattes med faktiske omkostninger. Den overordnede omkostning for færdigvaren debiteres på lagertilgangskontoen og krediteres på lagerafgangskontoen. Hvis du markerer afkrydsningsfeltet **Slutkørsel**, når du udfører omkostningsberegningen, ændres produktionsordrens status til **Afsluttet**. Denne status forhindrer, at ekstra omkostninger ved en fejltagelse bogføres på en færdigmeldt produktionsordre. Du kan angive, at værdien for mængder med fejl, der er færdigmeldt under rapportering, skal tildeles de gode mængder, der er færdigmeldt. Du kan også angive, at værdien for antal fejl skal bogføres på en dedikeret spildkonto.

## <a name="controlling-the-level-of-ledger-posting"></a>Styre finanskonteringsniveauet
I **Produktionsstyringsparametre** kan du bruge feltet **Finanskontering** til at angive niveauet for finanskontering for produktionsprocesser. Følgende værdier er tilgængelige:

-   **Vare og ressource** – Brug finanskontiene, der er angivet på varegrupper for råmaterialer og færdigvarer. IGVA for tidsforbrug er taget fra ressource eller ressourcegruppe fra ruteoperationer.
-   **Vare og art** – Brug finanskontiene, der er angivet på varegrupper for råmaterialer og færdigvarer. IGVA for tidsforbrug er hentet fra de omkostningskategorier, der er knyttet til ruteoperationer.
-   **Produktionsgrupper** – Brug finanskontiene, der er angivet på produktionsgrupper for både materiale- og tidsforbrug. Produktionsgrupper er knyttet til de frigivne produkter og kopieres til produktionsordrerne, når disse ordrer oprettes. Bogføring på produktionsordrer følger derefter de produktionsgrupper, som er knyttet til produktionsordren.

**Bemærk:** Hvis standardmetoden til beregning af omkostningen for færdigvaren er brugt, afspejles dette også i den endelige postering. Hvis der er en difference mellem de faktiske omkostninger og de omkostninger, der er beregnet ved hjælp af standardmetoden, bogføres differencen på kontoen, der viser avance og tab.




