---
title: Ændre eller tildele en finanskalender igen
description: I dette emne beskrives, hvordan du kan ændre den kalender, der aktuelt er knyttet til finans, og hvordan du tildeler en ny kalender til finans.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 16000243bc8aa76b04ac56dfb8bfbab7cd644eb3120cc68493ff066598f6cf85
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758071"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Ændre eller tildele en finanskalender igen

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du kan ændre den kalender, der aktuelt er knyttet til finans, og hvordan du tildeler en ny kalender til finans.

## <a name="issue"></a>Emne

Nogen gange skal virksomheder ændre den eksisterende kalender, der er knyttet til finans, eller tildele en ny kalender.

## <a name="resolution"></a>Løsning

Der er to scenarier til at ændre eller knytte en kalender igen til finans. Det første scenario omfatter ændring af en eksisterende kalender, der allerede er tilknyttet finans. Det andet scenario omfatter oprettelse af en ny kalender og tildeling af den til finans. Begge ændringer kan udføres når som helst, også efter at der er bogført transaktioner i finans.

### <a name="change-an-existing-fiscal-calendar"></a>Ændre en eksisterende regnskabskalender

Hvis du vil ændre en eksisterende kalender, der er knyttet til finans, skal du gå til **Finans \> Finansopsætning \> Finans** og vælge linket til regnskabskalenderen for at åbne siden **Finanskalendere**.

Der er grænser for, hvilke ændringer du kan foretage i en kalender. Du kan f.eks. ændre start- og slutdatoerne for *perioderne* i et år, men du kan ikke ændre start- og slutdatoerne for et *år* i kalenderen.

Hvis du vil ændre perioderne i et år, skal du vælge den relevante kalender og det relevante år. Du skal først bruge knappen **Slet periode** til at slette nogle eller alle de eksisterende driftsperioder. Alle driftsperioder undtagen den første kan slettes. Brug derefter knappen **Opdel periode** til at opdele den resterende periode eller perioder i nye perioder ved at angive en korrekt startdato for den næste periode.

Når du har ændret perioderne i en kalender, skal du køre processen **Genberegn finansperioder** i alle juridiske enheder (virksomhed), som kalenderen er tilknyttet. Selvom der ikke vises en advarsel, som minder dig om at udføre dette trin, skal genberegningsprocessen opdatere den periode, der er knyttet til hver bogført transaktion i Finans. Hvis du vil køre genberegningsprocessen, skal du vælge **Genberegn finansperioder** på siden **Finansopsætning** i hvert enkelt regnskab.

Hvis genberegningsprocessen ikke køres, kan transaktionssaldi på en råbalance eller i regnskaber blive medtaget forkert i perioder. I dette tilfælde kan du til enhver tid rette saldi ved at køre genberegningsprocessen.

### <a name="assign-a-new-fiscal-calendar"></a>Tildele en ny regnskabskalender

Hvis du vil tildele en ny regnskabskalender, skal du gå til **Finans \> Finansopsætning \> Finans** og vælge **Rediger** for at sætte siden **Finans** i redigeringstilstand. Vælg derefter en ny regnskabskalender i feltet **Regnskabskalender**.

Når du har ændret regnskabskalenderen for en finans, skal du køre **Genberegn finansperioder**. Når du tildeler en ny regnskabskalender til en finanskonto, vises der en meddelelse, som minder dig om at udføre dette trin. Selvom meddelelsen kan indikere, at genberegningsprocessen er valgfri, er den det ikke. Den skal opdatere den periode, der er knyttet til hver bogført transaktion i Finans. Hvis du vil køre genberegningsprocessen, skal du vælge **Genberegn finansperioder** på siden **Finansopsætning**.

Hvis genberegningsprocessen ikke køres, kan transaktionssaldi på en råbalance eller i regnskaber blive medtaget forkert i perioder. I dette tilfælde kan du til enhver tid rette saldi ved at køre genberegningsprocessen.
