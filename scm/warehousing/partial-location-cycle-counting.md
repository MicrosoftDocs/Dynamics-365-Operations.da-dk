---
title: "Delvis cyklusoptælling for sted"
description: "Cyklusoptællingsplaner guider de faktiske optællingshandlinger. Du kan anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på en lokalitet."
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 856ac2a61bc06a772b586a0cf77496fc360db623
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---

# <a name="partial-location-cycle-counting"></a>Delvis cyklusoptælling for sted

[!include[banner](../includes/banner.md)]


Cyklusoptællingsplaner guider de faktiske optællingshandlinger. Du kan anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på en lokalitet.

Ved at bruge cyklusoptællingsplaner til at oprette optællingsarbejde kan du styre de faktiske optællingshandlinger. Du kan anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på en lokalitet. Ved at filtrere på bestemte produkter kan lagerchefen reducere evalueringsomkostninger, undgå konsolideringsfejl og spare tid.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Sådan konfigureres delvis cyklusoptælling for sted
Når du bruger lagerstedsarbejdsprocesser til optællingshandlinger, oprettes der en opgaveoverskrift for hvert sted. Når du definerer cyklusoptællingsplanen, kan du bruge forespørgslen **Vælg lokationer** for at begrænse det cyklusoptællingsarbejde, der oprettes. Når du vælger produkter til cyklusoptællingsplanen, kan du vælge både produkt- og produktvariantforespørgsler for at præcisere, hvad der skal optælles. 

Du kan knytte en **arbejdsskabelon** til en cyklusoptællingsplan for at definere, hvordan cyklusoptællingsarbejdet skal oprettes. Der henvises direkte til arbejdsskabelonen til cyklusoptællingshandlinger fra cyklusoptællingsplanen. 

Når du definerer oplysningerne i arbejdsskabelonen, kan du bruge indstillingen **Arbejdslinjeskift** til at angive, om optællingsarbejdslinjerne skal grupperes efter varenummer eller produktvariantnummer. Denne opsætning er påkrævet, hvis der kun skal optælles disponible lagerbeholdninger for bestemte produkter på en lokalitet. De cyklusoptællingsarbejdslinjer, der oprettes, har det oplysningsniveau, du angiver her, og den styrede optællingshandlingen håndteres baseret på dette niveau. 

Hvis du knytter cyklusoptællingsplaner til arbejdsskabeloner ved hjælp af indstillingen **Arbejdslinjeskift**, markeres feltet **Delvis cyklusoptælling** for det cyklusoptællingsarbejde, der oprettes, og flere cyklusoptællingsarbejdslinjer oprettes på baggrund af definitionen af arbejdsskabelonen. 

Før delvis cyklusoptællingsarbejde kan behandles, skal du som minimum vælge **Vis varenummer** for menupunktet på mobilenheden som et led i opsætningen af cyklusoptællingen. Operatøren på lagerstedet bliver bedt om kun at registrere kun optællingsoplysninger, der er relateret til optællingslinjerne (varenumre og produktdimensioner). Alle andre disponible lagerbeholdninger bliver ignoreret for denne optællingsproces. 

For den delvise cyklusoptællingsproces bliver dato og klokkeslæt for **Seneste optællingscyklus** ikke opdateret for lokationen.

## <a name="example"></a>Eksempel
I dette eksempel skal kun varenummer A0001 optælles på lagersted 61.

1.  Der oprettes en ny arbejdsskabelon for cyklusoptælling. Indstillingen **Arbejdslinjeskift** bruges til at gruppere optællingsarbejdslinjer efter varenummer. Derfor har det cyklusoptællingsarbejde, der oprettes, linjer pr. varenummer. Du kan også gruppere linjerne efter produktvariantnummer.
2.  Der oprettes en ny cyklusoptællingsplan, der refererer til den nyoprettede arbejdsskabelon. Cyklusoptællingsplanen omfatter alle lokationer på lagersted 61 (forespørgslen **Vælg lokationer**), der har en lagerbeholdning for varenummeret A0001. Valget af bestemte produkter defineres i afsnittet **Produktvalg for cyklusoptælling**.
3.  Du kan vælge produkter for cyklusoptællingsplaner ved at indstille feltet **Tomme lokationer** til **Udeluk tomme**. Når cyklusoptællingsplanen behandles, oprettes delvis cyklusoptællingsarbejde for varenummer A0001. Den faktiske optællingsproces kan udføres ved hjælp af menupunktet for cyklusoptælling på mobilenheden.



<a name="see-also"></a>Se også
--------

[Cyklusoptælling](cycle-counting.md)


