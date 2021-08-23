---
title: Konfigurere og administrere databaselogning
description: Du kan spore ændringer af tabeller og felter i Dynamics 365 Human Resources med databaselogning.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fd0f69df4a141e509c8c250f767cbbc3a20ef4ab7ac3dcec2bc6faa15eababb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781651"
---
# <a name="configure-and-manage-database-logging"></a>Konfigurere og administrere databaselogning

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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
2. Vælg **Næste**. 
3. På siden **Tabeller og felter** i guiden skal du vælge de tabeller og felter, hvor du vil aktivere databaselogføring, og vælge **Næste**.

   > [!Note]
   > Databaselogføring er ikke tilgængelig i alle tabeller i Human Resources-databasen. Hvis du vælger **Vis alle tabeller** under listen, udvides listen over tabeller og felter til at vise alle databasetabeller, som databaselogføring er tilgængelig for, men dette vil være en delmængde af den fulde liste over databasetabeller.

4. På siden **Typer af ændringer** i guiden skal du vælge de datahandlinger, du vil spore ændringer for i hver af tabellerne og felterne, og vælge **Næste**. I tabellen nedenfor kan du se en beskrivelse af de datahandlinger, der er tilgængelige til logføring.
5. Gennemse de ændringer, der vil blive foretaget, på siden **Udfør**, og vælg **Udfør**.

| Operation | Betegnelse |
| -- | -- |
| Spor nye transaktioner | Opret en log for nye poster, der er oprettet i tabellen. |
| Opdater | Opret en log for opdateringer af tabelposter eller opdateringer af individuelt valgte felter i tabellen. Hvis du vælger at logføre opdateringer for tabellen, oprettes der en logpost, hver gang der foretages en opdatering af et felt i en vilkårlig post i tabellen. Hvis du vælger at logføre opdateringer for bestemte felter, oprettes der kun en logpost, når der foretages opdateringer af disse felter med tabelposter. |
| Slet | Opret en log for poster, der er slettet fra tabellen. |
| Omdøb nøgle | Opret en logpost, når en tabelnøgle omdøbes. |


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
