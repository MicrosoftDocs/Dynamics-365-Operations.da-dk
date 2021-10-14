---
title: Lagermærkatoptælling
description: Dette emne indeholder oplysninger om mærkatoptælling, som du kan bruge til at sammenligne det faktiske indhold af et lagersted med den disponible lagerbeholdning.
author: yufeihuang
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64315b8c5f0be1dbd19239a8b07746e90aebb0d4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567361"
---
# <a name="inventory-tag-counting"></a>Lagermærkatoptælling

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om mærkatoptælling, som du kan bruge til at sammenligne det faktiske indhold af et lagersted med den disponible lagerbeholdning.

Ved at oprette linjer på siden **Mærkatoptælling** placerer du et mærkatnummer på hver lagervare, som et tal mellem 1 og 500. Under optællingen skal du angive varenummeret og antallet på et tilsvarende mærkat. Denne mærkat kan derefter bruges som grundlag for input i kladden til mærkatoptælling. Når du bogfører mærkatoptællingskladden, oprettes en ny optællingskladde på siden **Optælling**. Den nye kladde er baseret på de kladdelinjer til mærkatoptælling, du har oprettet Når du vil mærkatoptælle elementer efter en bestemt lagerdimension, kan du vælge dimensionen på siden **Vis dimension**, som vises, når du opretter kladden til mærkatoptælling. Hvis du f.eks. vil tælle varer på et bestemt lagersted, skal du markere afkrydsningsfeltet **Lagersted**. Hvis slideren **Lås varer under optælling** på siden **Parametre til lager- og lokationsstyring** er valgt på siden, kan varer ikke opdateres fysisk under optælling. Dog låses varer i mærkatoptællingskladder ikke under optælling. Der oprettes ikke lagertransaktioner, før mærkatoptællingslinjerne er bogført og overført til en optællingskladde. Hvis mærkaterne angives i vilkårlig rækkefølge, og du vil identificere de manglende mærkater, skal du klikke på kolonneoverskriften **Mærkat**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Cyklusoptælling](../warehousing/cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]