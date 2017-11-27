---
title: Importere og vedligeholde kreditkorttransaktioner
description: "Dette emne forklarer, hvordan du importerer og vedligeholder udgiftsrelaterede kreditkorttransaktioner. Disse transaktioner kan konfigureres, så de automatisk importeres efter en gentaget plan, eller du kan importere transaktionerne manuelt efter behov."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e640c9e44add5599be4a2e381b4ffd81f212889c
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a>Importere og vedligeholde kreditkorttransaktioner

[!include[banner](../includes/banner.md)]

Udgiftsrelaterede kreditkorttransaktioner kan konfigureres, så de automatisk importeres efter en tilbagevendende tidsplan. Du kan også importere posteringerne manuelt, når det er påkrævet. Kreditkorttransaktionerne importeres via dataenheden Kreditkorttransaktioner.

Du kan finde flere oplysninger om dataenheder under [Dataenheder](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Importér kreditkorttransaktioner

1. På siden **Kreditkorttransaktioner** skal du vælge **Importer transaktioner**. Hvis du åbner datastyring for første gang, skal systemet opdatere listen over dataenheder, før du kan fortsætte.
2. Indtast en entydig beskrivelse af importjobbet i feltet **Navn**.
3. I feltet **Kildedataformat** skal du vælge formatet på den fil, der indeholder kreditkorttransaktionerne, der skal importeres.
4. Vælg **Overfør**, og søg derefter og vælg den fil, der skal importeres.
5. Når filen er blevet overført, skal du validere tilknytningen af kreditkorttransaktionsfilen og kolonnerne i dataenheden Kreditkorttransaktioner ved at vælge linket **Vis tilknytning** i feltet. Hvis der er tilknytningsfejl, eller hvis du skal ændre tilknytningen, kan du foretage ændringerne af tilknytningen enten under fanen **Visualisering af tilknytning** eller fanen **Oplysninger om tilknytning** under fanen.
6. Hvis du vil automatisere kreditkorttransaktionerne, skal du vælge **Opret tilbagevendende datajob**. Du kan derefter angive gentagelsen, der definerer, hvor ofte kreditkorttransaktioner skal importeres. Vælg **OK**, når du er færdig.
7. Vælg **Importer** for at importere den valgte fil.
8. Hvis der opstår fejl under importen, kan du se logfilen for udførelsen eller midlertidige data for at få vist de fejl, der skal rettes for at sikre en vellykket import.

> [!NOTE]
> Hvis du skal importere mere end ét filformat, skal du oprette separate importjob for hver formattype.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Omfordele fratrådte medarbejderes kreditkorttransaktioner

Når en medarbejderpost er afsluttet, deaktiveres medarbejderens Active Directory-domænetjenester (AD DS)-konto. Der kan dog være aktive kreditkorttransaktioner, der stadig skal udgiftsføres og godtgøres. Fra siden **Kreditkorttransaktioner** kan du igen tildele medarbejderen enhver kreditkorttransaktion, hvor den tilknyttede medarbejder er fratrådt.

Vælg en eller flere kreditkorttransaktioner, og vælg derefter **Omfordel transaktioner**. Du kan derefter vælge en anden medarbejder, som kreditkorttransaktionerne skal tildeles til. Når kreditkorttransaktionerne er blevet tildelt igen, kan de vælges til en udgiftsrapport og betales gennem den normale proces for refusion af udgiftsrapport.

