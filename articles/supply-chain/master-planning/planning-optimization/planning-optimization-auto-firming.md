---
title: Automatisk autorisation med Planlægningsoptimering
description: Dette emne beskriver, hvordan du bruger automatisk autorisation med Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: e412ccbc7c44d41e0a70ef8b5436901e01c671e6
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383682"
---
# <a name="auto-firming-with-planning-optimization"></a>Automatisk autorisation med Planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Ved automatisk autorisation kan du autorisere (dvs. frigive) ordreforslag som del af varedisponeringsprocessen. Når ordreforslag autoriseres, omdannes de til faktiske indkøbsordrer, overførelsesordrer eller produktionsordrer. Når der bruges Planlægningsoptimering, autoriseres ordreforslag under en varedisponeringskørsel, når ordredatoen (dvs. startdatoen) ligger inden for tidshorisonten til autorisation.

> [!NOTE]
> Auto-autorisation af et indkøbsordreforslag kan kun forekomme, hvis varen er knyttet til en kreditor.

## <a name="turn-on-auto-firming"></a>Aktiver automatisk autorisation

Udfør følgende trin for at aktivere automatisk autorisation:

1. I arbejdsområdet **Funktionsstyring** på fanen **Ny** skal du vælge **Auto-autorisering for Planlægningsoptimering** fra listen. Hvis funktionen ikke vises under den fanen **Ny**, skal du se på fanerne **Ikke aktiverede** og **Alle**.
1. Vælg **Aktiver nu**. Du kan også vælge **Planlæg** og derefter vælge det tidspunkt, hvor funktionen skal aktiveres.

## <a name="set-up-the-firming-time-fence"></a>Konfigurer autorisationens tidshorisont

Autorisationstidshorisonten beregnes fremad fra datoen for kørslen af varedisponering. Den defineres af det af dig indtastede antal af dage. Du kan styre tidshorisonten for autorisationen på følgende måder:

- Hvis du vil definere standardautorisationstidshorisonten for en disponeringsgruppe, skal du gå til **Varedisponering** \> **Opsætning** \> **Disponering** \> **Disponeringsgrupper** og vælge en disponeringsgruppe. Derefter skal du angive antallet af dage i oversigtspanelet **Andet** i feltet **Automatisk autorisationstidshorisont (dage)**.
- Hvis du vil overskrive den autorisationstidshorisont, der er defineret for disponeringsgruppen for en bestemt vare, skal du gå til **Administration af produktinformation** \> **Frigivne produkter**, og dernæst i handlingsruden vælge **Plan** og derefter vælge **Varedisponering**. I fanen **Generelt** skal du vælge **Overskriv tidshorisont** og i feltet **Automatisk autorisationstidshorisont (dage)** skal du angive antallet af dage.
- Hvis du vil overskrive den autorisationstidshorisont, der er defineret for disponeringsgruppen og varedisponeringen for en bestemt behovsplan, skal du gå til **Varedisponering** \> **Opsætning** \> **Behovsplan** og dernæst vælge en behovsplan. Derefter skal du i oversigtspanelet **Tidshorisont i dage** angive **Frys** til **Ja** samt angivet antallet af dage.

Hvis automatisk autorisation er aktiveret for en varedisponeringskørsel, der bruger Planlægningsoptimering, udføres den automatiske autorisationsproces i henhold til den automatiske autorisationsopsætning. Hvis automatisk autorisation ikke er slået til, eller hvis planlægningen startes fra siden **Nettokrav**, springes den automatiske autorisationsproces over.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>Planlægsningsoptimering i forhold til det indbyggede planlægningsprogram for Supply Chain Management

Både Planlægningsoptimering og planlægningsprogrammet, der er indbygget i Microsoft Dynamics 365 Supply Chain Management, kan bruges til auto-autorisation af ordreforslag. Der er dog nogle vigtige forskelle. I Planlægningsoptimering bruges ordredatoen (dvs. startdatoen) til at bestemme, hvilke ordreforslag der skal autoriseres, ved hjælp af behovsdatoen (dvs. slutdatoen) for det indbyggede planlægningsprogram for Supply Chain Management. Her vises en oversigt over forskellene.

**Planlægningsoptimering**

- Automatisk autorisation er baseret på ordredatoen (startdato).
- Da ordredatoen (startdato) udløser en autorisation, behøver du ikke at overveje leveringstiden som en del af autorisations tidshorisonten.
- Hvis du vil autorisere alle ordrer, der skal starte i løbet af den aktuelle uge, skal autorisationstidshorisonten være én uge.

**Indbygget planlægningsprogram for Supply Chain Management**

- Automatisk autorisation er baseret på behovsdatoen (slutdatoen).
- For at sikre, at ordrer autoriseres rettidigt, skal autorisationstidshorisonten være længere end leveringstiden.
- Hvis du vil autorisere alle ordrer, der skal starte i løbet af den aktuelle uge, skal autorisationstidshorisonten være leveringstiden plus én uge.
