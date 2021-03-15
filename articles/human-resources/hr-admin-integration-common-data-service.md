---
title: Konfigurere Dataverse-integration
description: Du kan slå integration mellem Microsoft Dataverse og Dynamics 365 Human Resources til eller fra. Du kan også få vist synkroniseringsdetaljer, rydde sporingsdata og synkronisere en tabel som hjælp til fejlfinding af dataproblemer mellem de to miljøer.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111974"
---
# <a name="configure-dataverse-integration"></a>Konfigurere Dataverse-integration

Du kan slå integration mellem Microsoft Dataverse og Dynamics 365 Human Resources til eller fra. Du kan også få vist synkroniseringsdetaljer, rydde sporingsdata og synkronisere en tabel som hjælp til fejlfinding af dataproblemer mellem de to miljøer.

> [!NOTE]
> Yderligere oplysninger om Dataverse (tidligere Common Data Service) og terminologiopdateringer finder du i [Hvad er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)

Når du deaktiverer integration, kan brugere foretage ændringer i Human Resources eller Dataverse, men disse ændringer synkroniseres ikke mellem de to miljøer.

Som standard er dataintegration mellem Human Resources og Dataverse slået fra.

Du kan eventuelt deaktivere integration i følgende situationer:

- Du er ved at udfylde data via Data Management Framework og skal importere dataene flere gange for at få dem i korrekt tilstand.

- Der er problemer med dataene i enten Human Resources eller Dataverse. Hvis du deaktiverer integration, kan du slette en post i ét miljø uden at slette den i det andet. Når du slår integrationen til igen, vil posten i det miljø, hvor den ikke blev slettet, blive synkroniseret til det miljø, hvor den blev slettet. Synkroniseringen starter, næste gang batchjobbet **Dataverse-integration mistet anmodningssynk.** køres.

> [!WARNING]
> Når du slår dataintegration fra, skal du sørge for ikke at redigere den samme post i begge miljøer. Når du slår integration til igen, vil den post, du senest har redigeret, blive synkroniseret. Hvis du derfor ikke har foretaget de samme ændringer i posten i begge miljøer, kan der opstå datatab.

## <a name="access-the-dataverse-integration-page"></a>Adgang til siden Dataverse-integration

1. I den Human Resources-forekomst, hvor du vil se eller konfigurere indstillinger for integrationen med Dataverse, skal du vælge feltet **Systemadministration**.

    [![Feltet Systemadministration](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Vælg fanen **Links**.

    [![Fanen Links](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Under **Integrationer** skal du vælge **Dataverse-konfiguration**.

    [![Dataverse-konfigurationslink](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Slå dataintegration mellem Human Resources og Dataverse til eller fra

- Hvis du vil aktivere integration, skal du angive indstillingen **Aktivere Dataverse-integration** til **Ja** på siden **Microsoft Dataverse-integration**.

    > [!NOTE]
    > Når du slår integration til, synkroniseres data, næste gang batchjobbet **Dataverse-integration mistet anmodningssynk** køres. Alle data bør være tilgængelige, når batchjobbet er fuldført.

- Hvis du vil deaktivere integration, skal du angive indstillingen til **Nej**.

[![Slå Dataverse-integration til eller fra](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Det anbefales kraftigt, at du deaktiverer Dataverse-integration, mens du udfører dataoverførselsopgaver. Store dataoverførsler kan påvirke ydeevnen betydeligt. Overførsel af 2000 arbejdere kan f.eks. tage flere timer, når integration er aktiveret, og mindre end en time, når den deaktiveres. De tal, der er i dette eksempel, er udelukkende til demonstrationsformål. Det nøjagtige tidsforbrug med at importere poster kan variere meget afhængigt af mange faktorer.

## <a name="view-data-integration-details"></a>Vis dataintegrationsdetaljer

I oversigtspanelet **Administration** på siden **Microsoft Dataverse-integration** kan du se, hvordan rækkerne er sammenkædet mellem Human Resources og Dataverse.

- Hvis du vil se rækkerne for en tabel, skal du vælge tabellen i feltet **Dataverse-tabel**. Gitteret viser alle de rækker, der er knyttet til den valgte tabel.

> [!NOTE]
> Ikke alle Dataverse-tabeller er angivet i øjeblikket. Kun tabeller, der understøtter brugen af brugerdefinerede felter, vises i gitteret. Nye tabeller bliver tilgængelige via løbende frigivelser af Human Resources.

Gitteret indeholder følgende felter:

- **Dataverse-tabel** – Navn på tabellen i Dataverse.
- **Dataverse-tabelreference** – Den identifikation, som Dataverse bruger til at identificere en post. Denne værdi svarer til en **RecId**-værdi i Human Resources. Du kan finde identifikatoren, når du åbner Dataverse-tabellen i Microsoft Excel.
- **Human Resources-enhedsnavn** – Den Human Resources-enhed, der sidst synkroniserede data til Dataverse. Enheden kan enten have Dataverse-præfikset eller et andet præfiks.
- **Human Resources-reference** – Den **RecId**-værdi, der er tilknyttet posten i Human Resources.
- **Slettet fra Dataverse** – En værdi, der angiver, om rækken blev slettet fra Dataverse.

> [!NOTE]
> Poster i Human Resources svarer til rækker i Dataverse.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Fjerne tilknytningen af en post i Human resources fra en Dataverse-række

Hvis du får problemer under datasynkronisering mellem Human Resources og Dataverse, kan du muligvis løse dem ved at rydde sporingen og lade sporingstabellen blive synkroniseret igen. Hvis du fjerner tilknytningen og derefter ændrer eller sletter en række i Dataverse, synkroniseres ændringerne ikke med Human Resources. Hvis du foretager ændringer i Human Resources, oprettes der en ny sporingspost, og rækken opdateres i Dataverse.

- Hvis du vil fjerne tilknytningen af en post mellem Human Resources og en Dataverse-række, skal du vælge tabellen i feltet **Dataverse-tabel** og derefter vælge **Ryd sporingsoplysninger**.

[![Rydning af sporingsoplysninger](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Se den næste procedure, hvis du vil køre en fuld synkronisering af tabellen, når du har ryddet sporingen.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Synkronisere en tabel mellem Human Resources og Dataverse

Benyt denne fremgangsmåde, når:

- Ændringerne fra Dataverse er for længe om at blive vist i Human Resources.

- Du skal opdatere sporingstabellen, efter at du har ryddet registreringen.

Sådan kører du en fuld synkronisering af en tabel mellem Human Resources og Dataverse:

1. Vælg tabellen i feltet **Dataverse-tabel**.

2. Vælg **Synkroniser nu**.

[![Køre en fuld synkronisering](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Se også

[Dataverse-tabeller](hr-developer-entities.md)<br>
[Konfigurere virtuelle Dataverse-tabeller](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Ofte stillede spørgsmål om Virtuelle tabeller i Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Hvad er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologiopdateringer](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]