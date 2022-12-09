---
title: Sporing af regnskabskilde
description: Denne artikel indeholder oplysninger om siden Sporing af regnskabskilde, som du kan bruge til detaljeret analyse af kildeoplysninger bag regnskabsposter i finansmodulet.
author: RyanCCarlson2
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: kfend
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd5580dc0be37ec89e6c7934b47c7d5593d8716
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806427"
---
# <a name="accounting-source-explorer"></a>Sporing af regnskabskilde

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om siden **Sporing af regnskabskilde**, som du kan bruge til detaljeret analyse af kildeoplysninger bag regnskabsposter i finansmodulet.

Siden **Sporing af regnskabskilde** viser kildeoplysninger. Du kan bruge den enten som et separat værktøj eller til at analysere detaljerne bag regnskabsposter i finansmodulet. Du kan eksempelvis bruge siden til at få de mest detaljerede kildeoplysninger til en saldo i råbalancen eller til en bilagstransaktion. Du kan derefter bruge funktionen **Eksportér til Microsoft Excel** til at inddele oplysningerne i Microsoft Excel yderligere (for eksempel i en pivottabel eller i en pivottabelrapport).

Siden **Sporing af regnskabskilde** viser altid det samme samlede beløb pr. finanskonto som Finans viser (for eksempel i råbalancen). Som med råbalancen kan du få vist segmenter i separate kolonner. Du skal blot vælge det relevante sæt økonomiske dimensioner. 

Du kan bruge parametre til at definere et datointerval for analysen. Denne funktionalitet minder også om funktionerne i råbalance.

Siden **Sporing af regnskabskilde** viser yderligere oplysninger, der er baseret på regnskabsfordelinger, og eventuelt projektregnskabsfordelinger for alle dokumenter, der bruger kildedokumentstrukturen. Disse oplysninger omfatter værdierne **Type af pengebeløb**, **Projekt**, **Aktivitet**, **Kategori** og **Linjeegenskab**. Her er nogle eksempler på den analyse, du kan foretage:

- Afvigelser mellem indkøbsordrer og kreditorfakturaer, da hver afvigelse er repræsenteret af typen pengebeløb, som f.eks. gebyrafvigelse
- Fakturerbare og ikke-fakturerbare timer og udgifter pr. projekt, virksomhedsenhed og hovedkonto

Til kildedokumenter, der anvender begrebet reference-id'er til kildedokumenter, viser siden **Sporing af regnskabskilde** endnu flere detaljer som f.eks. **Debitor**, **Kreditor**, **Arbejder**, **Produkt**, **Antal**, **Enhedstekst** og **Beskrivelse**. Her er nogle eksempler på den analyse, du kan foretage:

- Hoteludgifter pr. virksomhedsenhed og hotelmærke for en regnskabsperiode baseret på udgiftsrapporter
- Rabatter pr. leverandør, produkt, afdeling

For disse dokumenter kan du også navigere til det faktiske kildedokument fra siden **Sporing af regnskabskilde**.

> [!NOTE]
> Pr. version 10.0.31 er den nye funktion **Avanceret filtrering af sporing af regnskabskilde** tilgængelig i Funktionsstyring. Denne funktion erstatter knappen **Opdater** for at give en mere robust avanceret forespørgselsoplevelse, der ligner den, der er tilgængelig på siden **Bilagstransaktioner**. Med det avancerede filter kan du filtrere på lignende felter som det, du finder på forespørgselssiden **Bilagstransaktioner**, f.eks. **Finanskonto**, **Forretningsenhed**, **Bærer** og **Afdeling**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
