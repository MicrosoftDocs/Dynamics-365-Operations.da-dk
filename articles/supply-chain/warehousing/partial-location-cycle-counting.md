---
title: Delvis cyklusoptælling for sted
description: Cyklusoptællingsplaner guider de faktiske optællingshandlinger. Du kan anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på en lokalitet.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f06b39f3c2d2f5a0bdfef1da9395c71686ed46968a1143305b5a10787f7e85f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778428"
---
# <a name="partial-location-cycle-counting"></a>Delvis cyklusoptælling for sted

[!include [banner](../includes/banner.md)]

Cyklusoptællingsplaner guider de faktiske optællingshandlinger. Du kan anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på en lokalitet.

Ved at bruge cyklusoptællingsplaner til at oprette optællingsarbejde kan du styre de faktiske optællingshandlinger. Du kan anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på en lokalitet. Ved at filtrere på bestemte produkter kan lagerchefen reducere evalueringsomkostninger, undgå konsolideringsfejl og spare tid.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Sådan konfigureres delvis cyklusoptælling for sted

Når du bruger lagerstedsarbejdsprocesser til optællingshandlinger, oprettes der en opgaveoverskrift for hvert sted. Når du definerer cyklusoptællingsplanen, kan du bruge forespørgslen **Vælg lokationer** for at begrænse det cyklusoptællingsarbejde, der oprettes. Når du vælger produkter til cyklusoptællingsplanen, kan du vælge både produkt- og produktvariantforespørgsler for at præcisere, hvad der skal optælles.

Du kan knytte en **arbejdsskabelon** til en cyklusoptællingsplan for at definere, hvordan cyklusoptællingsarbejdet skal oprettes. Der henvises direkte til arbejdsskabelonen til cyklusoptællingshandlinger fra cyklusoptællingsplanen.

Når du definerer oplysningerne i arbejdsskabelonen, kan du bruge indstillingen **Arbejdslinjeskift** til at angive, om optællingsarbejdslinjerne skal grupperes efter varenummer eller produktvariantnummer. Denne opsætning er påkrævet, hvis der kun skal optælles disponible lagerbeholdninger for bestemte produkter på en lokalitet. De cyklusoptællingsarbejdslinjer, der oprettes, har det oplysningsniveau, du angiver her, og den styrede optællingshandlingen håndteres baseret på dette niveau.

Hvis du knytter cyklusoptællingsplaner til arbejdsskabeloner ved hjælp af indstillingen **Arbejdslinjeskift**, markeres feltet **Delvis cyklusoptælling** for det cyklusoptællingsarbejde, der oprettes, og flere cyklusoptællingsarbejdslinjer oprettes på baggrund af definitionen af arbejdsskabelonen.

Før delvis cyklusoptællingsarbejde kan behandles, skal du som minimum vælge **Vis varenummer** for menupunktet på mobilenheden som et led i opsætningen af cyklusoptællingen. Operatøren på lagerstedet bliver bedt om kun at registrere kun optællingsoplysninger, der er relateret til optællingslinjerne (varenumre og produktdimensioner). Alle andre disponible lagerbeholdninger bliver ignoreret for denne optællingsproces.

For processen til delvis cyklusoptælling opdateres dato/klokkeslæt for **Seneste cyklusoptælling** ikke for lokationen, selvom alle disponible varer på en bestemt lokation tælles. Den delvise cyklusoptælling tager ikke højde for parameteren **Dage mellem cyklusoptælling**, der er angivet på siden **Cyklusoptællingsplaner**. Delvis cyklusoptælling understøtter ikke samtidig optælling af flere varer på samme lokation. Funktionen for delvis cyklusoptælling kan resultere i, at samme lokation optælles flere gange for en vare, når **Udfør behandling af cyklusoptællingsplan** køres. Hvis du vil undgå dette scenario, skal du angive filtre i feltet **Vælg lokationer**.

> [!NOTE]
> Mobilappen Lokationsstyring har ikke knappen **Tilføj NP eller vare**, når du bruger den delvise cyklusoptællingsproces.

## <a name="example"></a>Eksempel

I dette eksempel skal kun varenummer A0001 optælles på lagersted 61.

1. Der oprettes en ny arbejdsskabelon for cyklusoptælling. Indstillingen **Arbejdslinjeskift** bruges til at gruppere optællingsarbejdslinjer efter varenummer. Derfor har det cyklusoptællingsarbejde, der oprettes, linjer pr. varenummer. Du kan også gruppere linjerne efter produktvariantnummer.
1. Der oprettes en ny cyklusoptællingsplan, der refererer til den nyoprettede arbejdsskabelon. Cyklusoptællingsplanen omfatter alle lokationer på lagersted 61 (forespørgslen **Vælg lokationer**), der har en lagerbeholdning for varenummeret A0001. Valget af bestemte produkter defineres i afsnittet **Produktvalg for cyklusoptælling**.
1. Du kan vælge produkter til cyklusoptællingsplaner ved at angive feltet **Tomme lokationer** til **Udeluk tomme**. Når cyklusoptællingsplanen behandles, oprettes delvist cyklusoptællingsarbejde for varenummer A0001. Den faktiske optællingsproces kan udføres ved hjælp af menupunktet for cyklusoptælling på mobilenheden.

## <a name="additional-resources"></a>Yderligere ressourcer

[Cyklusoptælling](cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]