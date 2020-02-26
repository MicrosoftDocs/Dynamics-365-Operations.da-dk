---
title: Konfigurere Common Data Service-integration
description: Du kan slå integration mellem Common Data Service og en forekomst af Microsoft Dynamics 365 Human Resources til eller fra. Du kan også få vist synkroniseringsdetaljerne, rydde sporingsdata og synkronisere en enhed som hjælp til fejlfinding af dataproblemer mellem de to miljøer.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008460"
---
# <a name="configure-common-data-service-integration"></a>Konfigurere Common Data Service-integration

Du kan slå integration mellem Common Data Service og en forekomst af Microsoft Dynamics 365 Human Resources til eller fra. Du kan også få vist synkroniseringsdetaljerne, rydde sporingsdata og synkronisere en enhed som hjælp til fejlfinding af dataproblemer mellem de to miljøer.

Når du deaktiverer integration, kan brugere foretage ændringer i Personale eller Common Data Service, men disse ændringer synkroniseres ikke mellem de to miljøer.

Integration mellem Personale og Common Data Service er som standard slået fra eller til, afhængigt af tilstedeværelsen af demodata i miljøerne:

- **Fra** for nye miljøer, der ikke indeholder demodata
- **Til** for nye miljøer, der indeholder demodata

Nye miljøer, der indeholder demodata, vil starte med at synkronisere data, når de er klargjort.

Du kan eventuelt deaktivere integration i følgende situationer:

- Du er ved at udfylde data via Data Management Framework og skal importere dataene flere gange for at få dem i korrekt tilstand.

- Der er problemer med dataene i enten Personale eller Common Data Service. Hvis du deaktiverer integration, kan du slette en post i ét miljø uden at slette den i det andet. Når du slår integrationen til igen, vil posten i det miljø, hvor den ikke blev slettet, blive synkroniseret tilbage til det miljø, hvor den blev slettet. Synkroniseringen starter, næste gang batchjobbet **Common Data Service-integration mistet anmodningssynk.** køres.

> [!WARNING]
> Når du slår dataintegration fra, skal du sørge for ikke at redigere den samme post i begge miljøer. Når du slår integration til igen, vil den post, du senest har redigeret, blive synkroniseret. Hvis du derfor ikke har foretaget de samme ændringer i posten i begge miljøer, kan der opstå datatab.

## <a name="access-the-common-data-service-integration-page"></a>Adgang til siden Common Data Service-integration

1. I den Personale-forekomst, hvor du vil se eller konfigurere indstillinger for integrationen med Common Data Service, skal du vælge feltet **Systemadministration**.

    [![Feltet Systemadministration](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Vælg fanen **Links**.

    [![Fanen Links](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Under **Integrationer** skal du vælge **Common Data Service-konfiguration**.

    [![Common Data Service-konfigurationslink](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Slå dataintegration mellem Personale og Common Data Service til eller fra

- Hvis du vil aktivere integration, skal du angive indstillingen **Aktivér integration med Common Data Service** til **Ja**.

    > [!NOTE]
    > Når du slår integration til, synkroniseres data, næste gang batchjobbet **Common Data Service-integration mistet anmodningssynk** køres. Alle data bør være tilgængelige, når batchjobbet er fuldført.

- Hvis du vil deaktivere integration, skal du angive indstillingen til **Nej**.

[![Slå Common Data Service-integration til eller fra](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>Vis dataintegrationsdetaljer

I oversigtspanelet **Administration** på siden **Common Data Service-integration** kan du se, hvordan poster er sammenkædet mellem Personale og Common Data Service.

- Hvis du vil have vist posterne for en enhed, skal du vælge enheden i feltet **CDS-enhedsnavn**. Gitteret viser alle de poster, der er knyttet til den valgte enhed.

[![Visning af posterne for en enhed](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Ikke alle Common Data Service-enheder er angivet i øjeblikket. Kun enheder, der understøtter brugen af brugerdefinerede felter, vises i gitteret. Nye enheder bliver tilgængelige via løbende frigivelser af Personale.

Gitteret indeholder følgende felter:

- **CDS-enhedsnavn** – Navnet på enheden i Common Data Service.
- **CD-enhedsreference** – den identifikator, som Common Data Service bruges til at identificere en post. Denne værdi svarer til en **RecId**-værdi i Personale. Du kan finde identifikatoren, når du åbner Common Data Service-enheden i Microsoft Excel.
- **Personaleenhedsnavn** – Den enhed, der sidst synkroniserede data til Common Data Service. Enheden kan enten have Common Data Service-præfikset eller et andet præfiks.
- **Personale-reference** – Den **RecId**-værdi, der er tilknyttet posten i Personale.
- **Blev slettet fra CDS** – En værdi, der angiver, om posten blev slettet fra Common Data Service.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Fjern tilknytningen af en post i Personale fra Common Data Service

Hvis du får problemer under datasynkronisering mellem Personale og Common Data Service, kan du muligvis løse dem ved at rydde sporingen og lade sporingstabellen blive synkroniseret igen. Hvis du fjerner tilknytningen og derefter ændrer eller sletter en post i Common Data Service, synkroniseres ændringerne ikke med Personale. Hvis du foretager ændringer i Personale, oprettes der en ny sporingspost, og posten opdateres i Common Data Service.

- Hvis du vil fjerne tilknytningen af en post mellem Personale og Common Data Service, skal du vælge enheden i **CDS-enhedsnavn** og derefter vælge **Ryd sporingsoplysninger**.

[![Rydning af sporingsoplysninger](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Se den næste procedure, hvis du vil køre en fuld synkronisering af enheden, når du har ryddet sporingen.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Synkronisere en enhed mellem Personale og Common Data Service

Brug denne fremgangsmåde, hvis det tager for lang tid, før ændringer fra Common Data Service vises i Personale, eller hvis du skal opdatere sporingstabellen, efter at du har ryddet sporingen.

- Hvis du vil køre fuld synkronisering på en enhed mellem Personale og Common Data Service skal du vælge enheden i feltet **CDS-enhedsnavn** og derefter vælge **Synkroniser nu**.

[![Køre en fuld synkronisering](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


