---
title: Reparationsstyring
description: Du kan gruppere problemer systematisk, så det bliver muligt at foreslå løsninger, der tidligere har vist sig at fungere.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ebb9833be5e51fe59e9895e67cd8e55058078aa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001337"
---
# <a name="repair-management"></a>Reparationsstyring       

[!include [banner](../includes/banner.md)]


I forbindelse med reparationsstyring kan du gruppere problemer systematisk. På denne måde er det nemmere at foreslå løsninger, der tidligere har vist sig at fungere.

Du kan angive indstillinger for symptomer, diagnoser og løsninger. Du kan så bruge disse senere, når du modtager en lignende vare til reparation. Du kan også oprette reparationsstadier, der følger hvad der sker med en bestemt reparation.

## <a name="setting-up-repair-management"></a>Konfigurere reparationsstyring

Brug følgende forms til at angive oplysninger, der skal bruges til at angive symptomer, diagnose og løsning i forbindelse med en reparation.

1.  Klik på **Servicestyring** \> **Opsætning** \> **Reparation** \> **Betingelser**.

2.  Klik på **Servicestyring** \> **Opsætning** \> **Reparation** \> **Symptomområder**.

3.  Klik på **Servicestyring** \> **Opsætning** \> **Reparation** \> **Diagnoseområder**.

4.  Klik på **Servicestyring** \> **Opsætning** \> **Reparation** \> **Løsninger**.

5.  Klik på **Servicestyring** \> **Opsætning** \> **Reparation** \> **Reparationsstadier**.

## <a name="symptoms-and-conditions"></a>Symptomer og betingelser

Symptomer er den måde, som kunden beskriver problemet. Symptomer omfatter kundens observationer, der henleder til behovet for reparation.

Du kan bruge symptomområder, -koder og -betingelser. Symptomområdet er området for funktionsfejl, og symptomkoden dækker fejlsymptomet. Betingelsen beskriver den situation, hvori problemet udløses.

**Eksempel**

En computer sendes til reparation, fordi der opstår fejl på harddisken efter længere tids brug. Harddiskfejlen forårsager blå skærm. Den tekniker, der modtager computeren, angiver følgende symptomer og betingelser:

1.  Symptomområdet er harddisken.

2.  Symptomkoden er fejlen med blå skærm.

3.  Betingelsen er, at der opstår fejl på harddisken efter længere tids brug.

## <a name="diagnosis-and-resolutions"></a>Diagnose og løsninger

Felterne til diagnose og løsning afspejler reparationen. Det er det, en tekniker har gjort for at finde årsagen til problemet.

Diagnoseområdet omfatter, det der skal udføres for at løse problemet. Diagnosekoden er, hvordan problemet er blevet håndteret, og løsningskoden kan være, at varen er repareret, udskiftet, eller at kunden har annulleret ordren. Hvis computeren f.eks. er blevet repareret, kan diagnoseområdet værd 'defekt del', diagnosekoden kan være 'nyt skærmkort installeret', og løsningskoden kan være 'udskiftet'.

## <a name="repair-stages"></a>Reparationsstadier

Reparationsstadier angiver, hvordan reparationsprocessen skrider frem. Reparationsstadiet har en afmeldingsparameter, **Fuldført**, der viser, at en reparationslinje er fuldført, og at der er registreret en dato og et tidspunkt for færdiggørelsen.

## <a name="applying-repair-management"></a>Anvende reparationsstyring

Hvis du vil anvende reparationsstyring på en vare, skal varen være oprettet med en serviceobjektrelation på en serviceordre. Fra serviceordren kan du derefter oprette en reparationslinje med oplysninger om det aktuelle problem. På reparationslinjen angiver du det serviceobjekt, der skal repareres, sammen med oplysninger om symptomer, diagnose og udførelse. Du kan også oprette en bemærkning til reparationslinjen.

Du kan oprette reparationslinjer for hvert trin i reparationsprocessen.

## <a name="create-a-repair-line-on-a-service-order"></a>Oprette en reparationslinje på en serviceordre

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.

2.  Vælg serviceordren med det serviceobjekt, der skal repareres.

3.  Klik på **Reparation** \> **Reparationslinjer** for at åbne formularen **Reparationslinjer**.

4.  Tryk på Ctrl+N for at oprette en ny linje.

5.  Vælg et serviceobjekt. Du kan vælge et hvilket som helst serviceobjekt, der er oprettet med en objektrelation på serviceordren.

6.  Vælg en eller flere af de foruddefinerede værdier for symptomer, diagnoser og udførelser, der er relevante på reparationslinjen, og klik om nødvendigt på fanen **Bemærkning** for at oprette en bemærkning på reparationslinjen.

7.  Tryk på Ctrl+S for at gemme den nye reparationslinje. Feltet **Dato og klokkeslæt for oprettelse** under fanen **Generelt** i formularen **Reparationslinjer** opdateres med tidspunktet for lagring.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Spore og afslutte et reparationsforløb

Du kan angive reparationsstadierne til en reparationslinje, så du kan spore reparationsforløbet.

Når et reparationsproblem er blevet løst, kan du lukke reparationslinjen. Indstil reparationsstatus med egenskaben **Fuldført** aktiveret. Dato og klokkeslæt registreres som afslutningstidspunkt på linjen.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Afslutte en reparationslinje, når et problem er løst

1.  Åbn formularen **Reparationslinjer**. Følg fremgangsmåden tidligere i dette emne for at oprette en reparationslinje.

2.  Vælg reparationslinjen med det reparationsproblem, du vil afslutte.

3.  I feltet **Reparationsstadie** skal du vælge et stadie, hvor egenskaben **Fuldført** er aktiveret.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]