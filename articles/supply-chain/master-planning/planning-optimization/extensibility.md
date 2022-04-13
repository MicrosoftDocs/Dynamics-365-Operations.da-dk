---
title: Udvidelse til planlægningsoptimering
description: I dette emne beskrives de scenarier med udvidelsesmuligheder, der understøttes i planlægningsoptimering.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: d7e39c9ecd1dc1a101e219764e8f4457bb06ff7a
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468882"
---
# <a name="planning-optimization-extensibility"></a>Udvidelse til planlægningsoptimering

[!include [banner](../../includes/banner.md)]

I dette emne beskrives de scenarier med udvidelsesmuligheder, der er relateret til varedisponering og understøttes i planlægningsoptimering. Disse funktioner er tilgængelige fra og med Microsoft Dynamics 365 Supply Chain Management version 10.0.13.

## <a name="custom-processing-when-master-planning-is-completed"></a>Brugerdefineret behandling, når varedisponering er fuldført

I det mest almindelige scenarie med udvidelsesmuligheder i Planlægningsoptimering udføres brugerdefineret behandling, når planen er blevet opdateret. Du kan f.eks. føje en kolonne til tabellen med ordreforslag (`ReqPO`), eller du vil måske aflede statistiske oplysninger fra den oprettede plan. Det vigtigste udvidelsespunkt, der muliggør disse scenarier, er `jobCompletedSuccessfully`-metoden i `MpsMasterPlanningEvents`-klassen.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Her er et eksempel på en udvidelse, der angiver et brugerdefineret `CstmOrderPriority`-felt i ordreforslaget.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Når du tilføjer brugerdefineret logik, skal du overveje følgende begrænsninger og bedste fremgangsmåder:

- Metoden `jobCompletedSuccessfully` kaldes uden for posteringsområdet. Derfor er planen allerede synlig for brugeren, når den brugerdefinerede logik begynder at køre. Hvis tilpasningen indstiller flere felter i ordreforslag, er det vigtigt, at du giver brugerne besked om, at værdierne i disse felter i den sidste ende vil være ensartede (med andre ord kan de være forældede umiddelbart efter, at et planlægningsjob er udført).
- Et andet varedisponeringsjob kan starte, når metoden `jobCompletedSuccessfully` kaldes. Det nye job kan påvirke den fulde plan eller dele af planen. Det nye job kan opdatere eller slette de samme ordreforslag eller behovsposteringer, som blev oprettet eller opdateret som en del af det planlægningsjob, der blev håndteret i `jobCompletedSuccessfully`. Opdatering af konfliktundtagelser skal håndteres, når denne hændelse udvides.
- Undgå at bruge enkelt posteringsområde, når du udvider denne metode. En enkelt kørsel af varedisponering kan producere millioner af behovsposteringer og flere hundrede tusind ordreforslag. Hvis alle disse posteringer og ordreforslag behandles inden for området af en enkelt postering, vil der forekomme mange SQL-låse, som spærrer andre planlægningsprocesser. Hvis transaktionen desuden opbevares i længere tid, vil der blive oprettet "spøgelsesposter" i SQL-databasen. Spøgelsesposter påvirker alle processer i systemet negativt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]