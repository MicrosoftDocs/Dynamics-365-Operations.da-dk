---
title: Kostprisark
description: Opsætning af efterkalkulationsarket omfatter to målsætninger. Som den første målsætning skal du definere formatet for visning af omkostninger for solgte varer for en produceret vare eller en produktionsordre. Den formaterede visning kaldes et kostprisark. Som den anden målsætning skal du definere udgangspunktet for beregning af indirekte omkostninger. Opsætningen af efterkalkulationsarket bygger på kostprisgruppens funktion for visning af oplysninger og formlerne til beregning af indirekte omkostninger. De to mål for opsætning af efterkalkulationsark er beskrevet i denne artikel.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, CostSheetCalculationFactor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53201
ms.assetid: e7d72b43-3892-49ae-8821-9eede3f4d24a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28597fde8257c6b6518fd52a636354cf2b64b658
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579802"
---
# <a name="costing-sheets"></a>Kostprisark

[!include [banner](../includes/banner.md)]

Opsætning af efterkalkulationsarket omfatter to målsætninger. Som den første målsætning skal du definere formatet for visning af omkostninger for solgte varer for en produceret vare eller en produktionsordre. Den formaterede visning kaldes et kostprisark. Som den anden målsætning skal du definere udgangspunktet for beregning af indirekte omkostninger. Opsætningen af efterkalkulationsarket bygger på kostprisgruppens funktion for visning af oplysninger og formlerne til beregning af indirekte omkostninger. De to mål for opsætning af efterkalkulationsark er beskrevet i denne artikel. 

Et efterkalkulationsark er den formaterede visning af oplysninger om omkostninger for solgte varer for en produceret vare eller en produktionsordre. Når du opretter et efterkalkulationsark, kan du definere formatet for oplysningerne og også definere grundlaget for beregning af indirekte omkostninger. Opsætningen af efterkalkulationsarket bygger på kostprisgruppens funktioner for visning af oplysninger og for de formler, der bruges til beregning af indirekte omkostninger. Her er flere oplysninger om de to målsætninger for opsætningen af efterkalkulationsarket:
-   **Definer formatet af efterkalkulationsarket.** Det brugerdefinerede format for et efterkalkulationsark identificerer segmenteringen af omkostninger, der omfatter en produceret vares vareforbrug. Oplysningerne om en vares vareforbrug kan f.eks. segmenteres i materiale, arbejdskraft og indirekte omkostninger baseret på kostgrupper. Disse kostgrupper er tildelt varer, omkostningsarter for ruteoperationer og formler til beregning af indirekte omkostninger. Formatet for efterkalkulationsarket kræver som regel mellemtotaler, når der er defineret flere kostgrupper. Der kan f.eks. samles flere omkostningsgrupper, der er relateret til materiale. Det er valgfrit, om du vil definere formatet af et efterkalkulationsark, men der skal defineres et format for et efterkalkulationsark, hvis der skal beregnes indirekte omkostninger.
-   **Definer grundlaget for beregning af indirekte omkostninger.** Indirekte omkostninger afspejler indirekte produktionsomkostninger, der er knyttet til fremstilling af en produceret vare. En formel til beregning af indirekte omkostninger kan enten udtrykkes som et tillæg eller en sats. Et tillæg repræsenterer en procentdel af en værdi, mens en sats repræsenterer et beløb i timen for en ruteoperation. En kostprisgruppe definerer grundlaget for beregningsformlen. Det kan f.eks. være et tillæg på 100 % for en kostgruppe med arbejdskraft eller en timesats på DKK 50,00 for en kostgruppe med maskiner. Hvis du vil definere en beregningsformel og dets grundlag for kostgruppe, kræver opsætningen af efterkalkulationsarket, at du identificerer den kostgruppe, der repræsenterer de indirekte omkostninger, og vælger, om der skal bruges tillæg eller sats.

De enkelte beregningsformler skal angives som en kostprispost. Omkostningsposten består af en angivet efterkalkulationsversion, en tillægsprocent (eller et satsbeløb), grundlaget for kostgruppen, en status og en ikrafttrædelsesdato. Når en omkostningspost angives første gang, har den statussen **Afventer** og en ikrafttrædelsesdato. Når du aktiverer omkostningsposten, opdateres statussen til Aktiv, så posten er den aktuelle aktive post, og ikrafttrædelsesdatoen opdateres til aktiveringsdatoen. Omkostningsposten kan også angive et sted for en stedspecifik beregningsformel. Alternativt kan du lade feltet **Sted** stå tomt for at angive, at beregningsformlen er en formel for hele firmaet. Kostprisposten kan bestå af en angivet vare eller varegruppe, når beregningsformlen er markeret som en formel for de enkelte varer. 

De aktuelt aktive omkostningsposter for formler til beregning af indirekte omkostninger bruges til at forkalkulere omkostninger for produktionsordrer. De bruges også til at beregne faktiske omkostninger, der er relateret til faktisk forbrug af tid og materiale. Afventende kostprisposter bruges i styklisteberegninger for en fremtidig dato. 

De to blokeringspolitikker for en efterkalkulationsversion bestemmer, om afventende omkostninger kan vedligeholdes, og om de afventende omkostninger kan startes. Brug blokeringspolitikkerne til at tillade vedligeholdelse af data og derefter til at forhindre vedligeholdelse af omkostningsdata i en efterkalkulationsversion. 

Når du har defineret formatet for efterkalkulationsarket og beregninger for indirekte omkostninger, skal du udføre en særskilt handling for at validere og gemme oplysningerne. Efterkalkulationsarket repræsenterer et format for hele virksomheden, så der opnås en ensartet visning af oplysningerne om omkostningerne for solgte varer. 

Efterkalkulationsarket vises som en del af siden **Beregn varens kostpris**. Efterkalkulationsarket kan vises for en produceret vares beregnede omkostningspost på siden **Varepris** eller for en ordrespecifik beregningspost på siden **Resultater af styklistekalkulation**. Det vises også som del af siden **Prisberegning** for en produktionsordre.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]