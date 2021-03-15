---
title: Konfigurere og administrere databaselogning
description: Du kan spore ændringer af tabeller og felter i Dynamics 365 Human Resources med databaselogning.
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50346cc495fe08f49137dba59dbcbb3f7f838c7b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129273"
---
# <a name="configure-and-manage-database-logging"></a>Konfigurere og administrere databaselogning

Du kan spore ændringer af tabeller og felter i Dynamics 365 Human Resources med databaselogning. I dette emne beskrives, hvordan du kan:

- Administrere sikkerhed og ydeevne til databaselogning
- Opret databaselogføring
- Rydde op i databaselogfiler

## <a name="overview-of-database-logging"></a>Oversigt over databaselogning

Databaselogning sporer specifikke ændringer af tabeller og felter i Microsoft Dynamics 365 Human Resources. Disse ændringer omfatter indsættelse, opdatering eller sletning. Databaselogning gemmer en post over ændringer af tabeller eller felter i databaseloggens tabel.

Forretningsbrug af databaselogning omfatter:

- Oprette en revisionspost med ændringer af bestemte tabeller, der indeholder følsomme oplysninger.
- Sporing af enkelte transaktioner. Databaselogning er ikke beregnet til sporing af automatiske transaktioner, der kører i batchjob.

## <a name="security-for-database-logging"></a>Sikkerhed for databaselogning

Databaselogge kan indeholde følsomme data. Begræns adgangen, så den kun omfatter sikkerhedsroller, der skal have adgang til logdata.

## <a name="database-logging-and-performance"></a>Databaselogning og ydeevne

Selvom databaselogning er værdifuld ud fra et forretningsmæssigt perspektiv, kan det være dyrt i ressourceforbrug og administration. Påvirkninger af ydeevne fra databaselogning omfatter:

- Tabellen i databaselog kan hurtigt vokse og forårsage en forøgelse af størrelsen på databasen. Væksten afhænger af mængden af logførte data, du beslutter at beholde. Tabellen i databaseloggen bevarer som standard kun 30 dages logdata. 

- Databaselogning kan påvirke lange automatiserede processer negativt, f.eks. en langvarig dataimport.

### <a name="best-practices"></a>Bedste fremgangsmåder

Du kan forbedre ydeevnen ved at udvælge bestemte felter til loggen i stedet for hele tabeller. Databaselogning er begrænset til 20 tabeller for at hjælpe med at opretholde den overordnede ydeevne.

> [!NOTE]
> Det er kun muligt at logføre opdateringer for individuelle felter.

## <a name="set-up-database-logging"></a>Opret databaselogføring

Du kan bruge guiden **Registrering af databaseændringer** til at konfigurere databaselogning. Guiden giver en fleksibel måde at konfigurere logføring for tabeller eller felter.

1. Gå til **Systemadministration > Links > Database > Opsætning af databaselog**. Vælg **Ny** for at starte guiden **Registrering af databaseændringer**.
2. Fuldfør guiden.

## <a name="clean-up-database-logs"></a>Rydde op i databaselogfiler

Du kan slette alle eller en del af databaseloggene ved hjælp af følgende indstillinger:

- Vælg alle logge for en bestemt tabel.
- Vælg bestemte typer af databaselog.
- Vælg en dato og et klokkeslæt for oprettelse af en log.

Benyt følgende fremgangsmåde for at konfigurere oprydning af databaselog: 

1. Gå til **Systemadministration > Links > Database > Databaselog**. Vælg **Oprydning i log**.

2. Vælg en metode til valg af logge, der skal slettes, ved at angive en af følgende indstillinger:

   - Tabel-ID
   - Logtype
   - Dato og klokkeslæt for oprettelse

3. Brug fanen **Oprydning i databaselog** til at bestemme, hvornår du vil køre oprydningsopgaven for log. Databaselogge er som standard tilgængelige i 30 dage.


[!INCLUDE[footer-include](../includes/footer-banner.md)]