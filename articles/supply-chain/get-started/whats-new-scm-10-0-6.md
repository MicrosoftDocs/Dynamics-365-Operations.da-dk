---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management (10.0.6. november 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: f253355b3de4f148c11b1d9d3f43b6756e6bd38c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983669"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management (10.0.6. november 2019)

[!include [banner](../includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.6. Denne version har et build-nummer på 10.0.234. Når den generelle tilgængelighedsdato er november, er de nye funktioner tilgængelige til tidlig frigivelse i oktober. Du kan få flere oplysninger om version 10.0.6 i [Yderligere ressourcer](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>V2-dataenhed i produktkonfigurationsmodeller

Der udgives en anden version til dataenheden "produktkonfigurationsmodeller" (kaldet "Produktkonfigurationsmodeller V2 "). Standardskabelonen "418-produktkonfigurationsmodeller" er også nødvendig, så den bruger den nye enhed "produktkonfigurationsmodeller v2"-dataenhed i import/eksport af Framework-skabelonerne. Skabelonen opdateres ikke automatisk, så du skal indlæse skabelonen fra standarden manuelt. V2-enheden eksporterer en række som en separat fil i en vedhæftet fil i stedet for indlejret og løser derfor størrelsesbegrænsningerne for V1-enheden. 
 
Hvad skal du gøre for at foretage denne ændring?
-    Når v1-enheden er blevet udfaset, skal du starte med at overflytte fra V1 til V2. Hvis du bruger skabelonen "418-produktkonfigurationsmodeller", kan du klikke på knappen "Indlæs standardskabeloner" og derefter genindlæse skabelonen "418 – produktkonfigurationsmodeller"
-    Hvis du har brug for at bevare kompatibiliteten med eksisterende systemer, kan du nu fortsætte med at bruge den eksisterende skabelon og den (udfasede) V1-enhed, indtil du flytter integrationerne til den nye skabelon. 

## <a name="feature-management-enhancements"></a>Forbedringer af funktionsstyringen
Med funktionsstyring kan du nu aktivere alle nye funktioner, kræve en bekræftelse for at aktivere en funktion og aktivere alle funktioner, der ikke allerede er aktiveret. 


## <a name="purchase-agreement-responsible-party"></a>Ansvarlig part for købsaftale
Nu har du mulighed for at definere primære og sekundære ansvarlige parter i formularen Købsaftaleklassifikation og de resulterede købsaftaler.  Det giver brugeren adgang til, hvem der har ansvaret for aftalerne.

## <a name="rfq-link-on-the-purchase-order-line"></a>RFO-link på linjen Indkøbsordre
Du kan føje et referencelink fra indkøbsordrelinjerne tilbage til de tilsvarende RFO-linjer, som de stammer fra, så brugeren nemt kan få adgang til det understøttende dokument til anmodning om tilbud.

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="bug-fixes"></a>Fejlrettelser
Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.6, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>Platform update 30
Microsoft Dynamics 365 Supply Chain Management 10.0.6 indeholder platformsopdatering 30. Hvis du vil vide mere om platformsopdatering 30, kan du se [Nyheder eller ændringer i platformsopdatering 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019-frigivelsesplan bølge 2
Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Se [Dynamics 365: 2019-frigivelsesplan bølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Emnet [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i emnet [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.
