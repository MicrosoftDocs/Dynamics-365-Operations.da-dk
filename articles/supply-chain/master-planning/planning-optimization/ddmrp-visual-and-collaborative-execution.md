---
title: Udførelse af visuel grafik og samarbejde
description: I denne artikel beskrives, hvordan du kan overvåge DDMRP-punkterne (Demand Driven Material Requirements Planning), bufferzoner, ordreforslag og historik.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: ce32a4449da8e85f958f212f2c2dfd2841ca6887
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740817"
---
# <a name="visual-and-collaborative-execution"></a>Udførelse af visuel grafik og samarbejde

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

I denne artikel beskrives, hvordan du kan overvåge DDMRP-punkterne (Demand Driven Material Requirements Planning), bufferzoner, ordreforslag og historik.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Spore buffere og antal visuelt for en valgt vare

I Microsoft Dynamics 365 Supply Chain Management kan du visuelt spore, hvordan buffers, disponible antal og nettoflowniveauer ændres over tid for alle valgte, frigivne produkter. Følg disse trin for at åbne og gennemse resultaterne af diagrammerne.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg en frigivet vare, der er konfigureret som et afkoblingspunkt. (Du finder flere oplysninger under [Lagerpositionering](ddmrp-inventory-positioning.md).)
1. Vælg **Plan** i handlingsruden, og vælg derefter **Varedisponering**.
1. Vælg en varedisponeringspost, der opretter et disponeringspunkt på siden **Varedisponering**. (Denne post viser navnet på en disponeringsgruppe, der er konfigureret til at oprette disponeringspunkter).
1. Vælg fanen **Disponibel**. Denne fane indeholder et diagram, der viser, hvordan disponible antal er ændret over tid, sammen med værdien af det disponible niveau, der er registreret for en bestemt periode, hver gang varedisponering køres. Fanen indeholder også en tabel, der viser, hvilke af følgende kategorier hver af de registrerede sikkerhedsniveau falder i:

    - **Kritisk lav** – Mindre end halvdelen af minimum for perioden.
    - **Lav** – Mellem halv minimum og minimum.
    - **Gennemsnitlig disponibel** - Mellem minimum og minimum plus den grønne zone.
    - **Højere end gennemsnittet** – Højere end gennemsnittet.

    ![Historiske historikniveauer under fanen Disponibel.](media/ddmrp-on-hand-graph.png "Historiske disponible niveauer på fanen Disponibel")

    > [!NOTE]
    > De farver, der bruges under fanen **Disponibel**, repræsenterer forskellige områder end de lignende farver, der bruges under fanen **Bufferværdier**.

1. Hvis du vil have vist, hvordan bufferværdierne er ændret over tid, og hvordan de sammenlignes med lager- og nettoflowniveauer, skal du vælge fanen **Bufferværdier**.

    ![Historiske historikniveauer for lager og nettoflow under fanen Bufferværdier.](media/ddmrp-buffer-values-graph.png "Historiske disponible og net-flow-niveauer på fanen Bufferværdier")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Spore status og ordreforslag for alle tilbagemeldte point

Arbejdsområdet i **efterspørgselsbaseret MRP** indeholder flere værktøjer sammen med nøgletal (KPI'er) og oversigter over status for dine varer og relaterede ordreforslag. Du kan åbne den ved at gå til **Varedisponering \> Arbejdsområder \> Efterspørgselsstyret MRP**.

![Efterspørgselsstyret MRP-arbejdsområde.](media/ddmrp-workspace.png "Efterspørgselsstyret MRP-arbejdsområde")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Få oversigter over afkoblingspoint og ordreforslag

Udover det **efterspørgselsbaserede MRP-arbejdsområde** findes der adskillige sider i Supply Chain Management, hvor du kan få vist oplysninger om din DDMRP-opsætning, deling point og ordreforslag. Nogle af disse sider indeholder også praktiske knapper i handlingsruden, som kan bruges til at administrere buffers, køre behovsplanlægning og åbne andre relaterede visninger.

- Hvis du vil have vist status for delingspunkt efter nettoflowniveau, **Varedisponering \> Varedisponering \> DDMRP \> Status for afkoblingspunkter efter nettoflow**.
- Hvis du vil have vist afkoblingspointstatus for disponibel lagerbeholdning, skal du gå til **Varedisponering \> Varedisponering \> DDMRP \> Status for disponible afkoblingspunkter**.
- Hvis du vil have vist ordreforslag til afkoblingspoint, skal du gå til **Varedisponering \> Varedisponering \> DDMRP \> Planlagte ordrer til afkoblingspoint**.
- Hvis du vil vise afkoblede gennemløbstider, skal du gå til **Varedisponering \> Varedisponering \> DDMRP \> Afkoblet gennemløbstid**.

## <a name="clean-up-decoupling-point-buffer-values"></a>Ryd op i bufferværdier for afkoblingspunkt

Systemet vil med tiden opbygge en stor mængde historikdata, der er knyttet til igangværende bufferberegninger. Denne historikdata medfører, at datavolumen øges, og kan senere påvirke systemets ydeevne. Det anbefales derfor, at du rydder op fra tid til anden de gamle bufferværdier til afkoblingspunkt.

> [!WARNING]
> Oprydningsjobbet fjerner indstillinger for historiske bufferværdier og oplysninger om historisk lager/nettoflow. Det kan ikke tilbageføres.

Benyt følgende fremgangsmåde for at rydde op i bufferværdier for et afkoblingspunkt.

1. Gå til **Varedisponering \> Varedisponering \> DDMRP \> Ryd op i bufferværdier til afkoblingspunkt**.
1. Angiv følgende felter i dialogboksen **Ryd op i bufferværdier til afkoblingspunkt**:

    - **Slet poster, der er ældre end (dage)** – Angiv alder for de poster, der skal beholdes, i dage. Alle bufferværdiposter til afkoblingspunkter, der er ældre end denne værdi, slettes.
    - **Varedisponering** – Vælg en varedisponering, der omfatter de varer, der påvirkes af oprydningen. Oprydningen gælder for alle varerne i planen, når de indstillinger for **Filter**, du angiver i denne dialogboks, er anvendt.

1. Hvis du vil begrænse, hvilke poster der skal medtages i batchjobbet, skal du vælge **Filter** i oversigtspanelet **Poster, der skal medtages** for at åbne dialogboksen **Forespørgsel**. Denne dialogboks fungerer på samme måde som for andre typer af [baggrundsjob](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Angiv, hvordan, hvornår og hvor ofte oprydningen skal genereres, i oversigtspanelet **Kør i baggrunden**. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Vælg **OK** for at tilføje det nye job til udførelse i batchkøen.
