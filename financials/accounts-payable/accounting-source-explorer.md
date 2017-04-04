---
title: Sporing af regnskabskilde
description: Denne artikel indeholder oplysninger om Sporing af regnskabskilde, som du kan bruge til detaljeret analyse af kildeoplysninger bag regnskabsposter i finansmodulet.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 8913e61285d5d180883471991b659ddcb260afe3
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-source-explorer"></a>Sporing af regnskabskilde

Denne artikel indeholder oplysninger om Sporing af regnskabskilde, som du kan bruge til detaljeret analyse af kildeoplysninger bag regnskabsposter i finansmodulet.

Sporing af regnskabskilde er en ny side, der viser kildeoplysninger. Du kan bruge regnskabsmæssige kilde explorer enten som et separat værktøj eller til at analysere detaljerne bag regnskabsposter i finansmodulet. Du kan eksempelvis bruge regnskabsmæssige kilde explorer til at få de mest detaljerede kildeoplysninger til en balance i revisionssporet saldo eller til en bilagspostering. Du kan derefter bruge funktionen Eksportér til Microsoft Excel til at inddele oplysningerne i Microsoft Excel yderligere (for eksempel i en pivottabel eller i en pivottabelrapport).

Sporing af regnskabskilde viser altid det samme samlede beløb pr. finanskonto som Finans viser (for eksempel i råbalancen). Som med råbalancen kan du få vist segmenter i separate kolonner. Du skal blot vælge det relevante sæt økonomiske dimensioner. 

Du kan bruge parametre til at definere et datointerval for analysen. Denne funktionalitet minder også om funktionerne i råbalance.

Explorer Viser yderligere oplysninger, der er baseret på regnskabsfordelinger for alle dokumenter, der bruger kilde dokument framework, regnskabsmæssige kilde og eventuelt projekt regnskabsfordelinger. Disse oplysninger omfatter typen af pengebeløb, projekt, aktivitet, kategori og linjeegenskaben. Her er nogle eksempler på den analyse, du kan foretage:

-   Afvigelser mellem indkøbsordrer og kreditorfakturaer, da hver afvigelse er repræsenteret af typen pengebeløb, som f.eks. gebyrafvigelse
-   Fakturerbare og ikke-fakturerbare timer og udgifter pr. projekt, virksomhedsenhed og hovedkonto

Til kildedokumenter, der anvender begrebet reference-id'er til kildedokumenter, viser Sporing af regnskabskilde endnu flere detaljer, som debitor, kreditor, arbejder, produkt, antal, enhedsteksten og beskrivelser. Her er nogle eksempler på den analyse, du kan foretage:

-   Hoteludgifter pr. virksomhedsenhed og hotelmærke for en regnskabsperiode baseret på udgiftsrapporter
-   Rabatter pr. leverandør, produkt, afdeling

For disse dokumenter kan du også navigere til det faktiske kildedokument fra Sporing af regnskabskilde.


