---
title: "Lagermærkatoptælling"
description: "Denne artikel indeholder oplysninger om mærkatoptælling, som du kan bruge til at sammenligne det faktiske indhold af et lagersted med den disponible lagerbeholdning."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 61a48a61963f643c8969e9090c2e84b5499b716a
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-tag-counting"></a>Lagermærkatoptælling

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om mærkatoptælling, som du kan bruge til at sammenligne det faktiske indhold af et lagersted med den disponible lagerbeholdning. 

Ved at oprette linjer på siden **Mærkatoptælling** placerer du et mærkatnummer på hver lagervare, som et tal mellem 1 og 500. Under optællingen skal du angive varenummeret og antallet på et tilsvarende mærkat. Denne mærkat kan derefter bruges som grundlag for input i kladden til mærkatoptælling. Når du bogfører mærkatoptællingskladden, oprettes en ny optællingskladde på siden **Optælling**. Den nye kladde er baseret på de kladdelinjer til mærkatoptælling, du har oprettet Når du vil mærkatoptælle elementer efter en bestemt lagerdimension, kan du vælge dimensionen på siden **Vis dimension**, som vises, når du opretter kladden til mærkatoptælling. Hvis du f.eks. vil tælle varer på et bestemt lagersted, skal du markere afkrydsningsfeltet **Lagersted**. Hvis slideren **Lås varer under optælling** på siden **Parametre til lager- og lokationsstyring** er valgt på siden, kan varer ikke opdateres fysisk under optælling. Dog låses varer i mærkatoptællingskladder ikke under optælling. Der oprettes ikke lagertransaktioner, før mærkatoptællingslinjerne er bogført og overført til en optællingskladde. Hvis mærkaterne angives i vilkårlig rækkefølge, og du vil identificere de manglende mærkater, skal du klikke på kolonneoverskriften **Mærkat**.

<a name="see-also"></a>Se også
--------

[Cyklusoptælling](../warehousing/cycle-counting.md)




