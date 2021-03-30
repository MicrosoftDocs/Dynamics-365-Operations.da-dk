---
title: Sporing af regnskabskilde
description: Denne artikel indeholder oplysninger om Sporing af regnskabskilde, som du kan bruge til detaljeret analyse af kildeoplysninger bag regnskabsposter i finansmodulet.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: roschlom
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f92781a8e1400206f91f91c46c319b928e0010c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250716"
---
# <a name="accounting-source-explorer"></a>Sporing af regnskabskilde

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om Sporing af regnskabskilde, som du kan bruge til detaljeret analyse af kildeoplysninger bag regnskabsposter i finansmodulet.

Sporing af regnskabskilde er en ny side, der viser kildeoplysninger. Du kan bruge Sporing af regnskabskilde enten som et separat værktøj eller til at analysere detaljerne bag regnskabsposter i finansmodulet. Du kan eksempelvis bruge Sporing af regnskabskilde til at få de mest detaljerede kildeoplysninger til en saldo i råbalancen eller til en bilagspostering. Du kan derefter bruge funktionen Eksportér til Microsoft Excel til at inddele oplysningerne i Microsoft Excel yderligere (for eksempel i en pivottabel eller i en pivottabelrapport).

Sporing af regnskabskilde viser altid det samme samlede beløb pr. finanskonto som Finans viser (for eksempel i råbalancen). Som med råbalancen kan du få vist segmenter i separate kolonner. Du skal blot vælge det relevante sæt økonomiske dimensioner. 

Du kan bruge parametre til at definere et datointerval for analysen. Denne funktionalitet minder også om funktionerne i råbalance.

Sporing af regnskabskilde viser yderligere oplysninger, der er baseret på regnskabsfordelinger, og eventuelt projektregnskabsfordelinger for alle dokumenter, der bruger kildedokumentstrukturen. Disse oplysninger omfatter typen af pengebeløb-, projekt-, aktivitets-, kategori- og linjeegenskaben. Her er nogle eksempler på den analyse, du kan foretage:

-   Afvigelser mellem indkøbsordrer og kreditorfakturaer, da hver afvigelse er repræsenteret af typen pengebeløb, som f.eks. gebyrafvigelse
-   Fakturerbare og ikke-fakturerbare timer og udgifter pr. projekt, virksomhedsenhed og hovedkonto

Til kildedokumenter, der anvender begrebet reference-id'er til kildedokumenter, viser Sporing af regnskabskilde endnu flere detaljer, som debitor, kreditor, arbejder, produkt, antal, enhedsteksten og beskrivelser. Her er nogle eksempler på den analyse, du kan foretage:

-   Hoteludgifter pr. virksomhedsenhed og hotelmærke for en regnskabsperiode baseret på udgiftsrapporter
-   Rabatter pr. leverandør, produkt, afdeling

For disse dokumenter kan du også navigere til det faktiske kildedokument fra Sporing af regnskabskilde.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]