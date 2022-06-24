---
title: Vis feriesaldi i grænsefladen til produktionsudførelse
description: Denne artikel indeholder et eksempelscenario, der viser, hvordan Microsoft Dynamics 365 Supply Chain Management konfigureres, så programmet bruger lønstatistik for at give arbejdere et overblik over deres feriesaldo for det indeværende år.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: 2a6b6f52bfa7539b7c9bb5841536b0d564d0274c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852267"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Vis feriesaldi i grænsefladen til produktionsudførelse

[!include [banner](../includes/banner.md)]

Denne artikel indeholder et eksempelscenario, der viser, hvordan Microsoft Dynamics 365 Supply Chain Management konfigureres, så programmet bruger lønstatistik for at give hver arbejder et overblik over deres feriesaldo for det indeværende år. Arbejdere vil kunne se deres feriesaldo i dialogboksen **Min dag** i brugergrænsefladen til produktionsudførelse.

I dette scenario bruges den danske ferielov, hvor ferieåret går fra 1. september til og med 31. august. I dette scenario har dit firma ansat en ny arbejder og vil tildele denne arbejder en saldo på 10 feriedage resten af det indeværende ferieår.

## <a name="turn-on-the-required-features"></a>Slå de påkrævede funktioner til

Hvis du vil køre dette scenario, skal du aktivere visningen *Visningen "Min dag" til grænsefladen til produktionsudførelse*-funktionen i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Yderligere oplysninger om aktivering af denne og andre funktioner i brugergrænsefladen til produktionsudførelse finder du i [Konfigurere brugergrænsefladen til produktionsudførelse](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

## <a name="create-a-new-pay-type"></a>Oprette en ny lønart

Start med at oprette en ny *lønart*, der sporer arbejdernes feriedage (kaldes også deres *feriesaldo*). Lønarter bruges typisk til at beregne arbejderes løn. Den lønart, du opretter her, bruges dog til at beregne en saldo.

1. Gå til **Tid og fremmøde \> Opsætning \> Løn \> Lønarter**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Lønart:** *5151-1*
    - **Beskrivelse:** *Tæller for arbejderens feriedage*
    - **Medtag i eksport:** *Nej*

## <a name="update-the-pay-agreement"></a>Opdater lønaftale

I dette afsnit kan du redigere en eksisterende *lønaftale* ved at tilføje den nye lønart og angive de regler, der definerer, hvordan den enkelte arbejders feriesaldo justeres, når feriedage registreres.

1. Gå til **Tid og fremmøde \> Opsætning \> Løn \> Lønaftaler**.
1. Vælg den lønaftale, du vil definere feriepolitikken for. (Hvis du arbejder med standardeksempeldata i USMF, findes der kun én lønaftale. *Man*.)
1. Kontroller, at den valgte lønaftale er gyldig for den aktuelle dato. Hvis du arbejder med standardeksempeldata i USMF, kan feltet **Til dato** i *Man*-lønaftalen angives til en dato, der ligger tidligere. Rediger værdien, så det er et år eller to senere efter behov.
1. Klik på **Aftalelinjer** i handlingsruden.
1. På siden **Lønaftalelinjer** i oversigtspanelet **Oversigt** kan du angive følgende værdier på værktøjslinjen:

    - Vælg **Mandag** på den første rulleliste.
    - Vælg **Fravær** på den anden rulleliste.

1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.
1. I den nye række skal du indstille feltet **Lønart** til den lønart, du har oprettet for dette scenario (*5151-1*). Lad de øvrige felter være indstillet med standardværdierne.
1. Mens den nye række stadig er valgt, skal du angive følgende værdier i oversigtspanelet **Generelt**:

    - **Fraværskode:** *Ferie*
    - **Brug fast antal:** *Ja*
    - **Konstant:** *-1*

1. Vælg **Kopiér dag** i handlingsruden.
1. I dialogboksen **Kopier dag** skal du angive følgende værdier:

    - **Tirsdag**, **Onsdag**, **Torsdag** og **Fredag:** *Ja*
    - **Overskriv:** *Ja*
    - **Fravær:** *Ja*

1. Vælg **OK**.

## <a name="create-a-payroll-statistic-group"></a>Oprette lønstatistikgruppe

*Lønstatistikgrupper* bruges til at konfigurere statistikker for arbejderregistreringer i en periode. I dette scenario vil du bruge en lønstatistikgruppe til at beregne antallet af feriedage, som arbejdere optjener i løbet af en ferieperiode. I Danmark løber ferieperioden fra 1. september til og med 31. august.

1. Gå til **Tid og fremmøde \> Opsætning \> Løn \> Lønstatistikgrupper**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Lønstatistikgruppe:** *VAC*
    - **Beskrivelse:** *Feriesaldo*
    - **Overførsel:** *Nej*

1. Mens den nye række stadig er markeret, skal du vælge **Konfiguration** i handlingsruden.
1. Vælg **Ny** på siden **Konfiguration** i handlingsruden for at føje en række til gitteret.
1. Angiv feltet **Lønart** til *5151-1* i den nye række.
1. Du kan også vælge og holde (eller højreklikke) i feltet **Periodekode** og derefter vælge **Vis detaljer**. Du kan nu definere den periodekode, du vil tildele til dette felt senere.
1. På siden **Periodetyper** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Periodetyper:** *VacYear*
    - **Beskrivelse:** *Ferieår*
    - **Hyppighed:** *År*

1. Mens den nye række stadig er markeret, skal du vælge **Generer perioder** i handlingsruden.
1. Angiv følgende værdier i dialogboksen **Generer perioder**:

    - **Angiv startdato for perioden:** *1 september 2021*
    - **Periodelængde:** *5*

1. Vælg **OK**.
1. Luk siden **Periodetyper** for at vende tilbage til siden **Lønstatistikgrupper**.
1. Angiv feltet **Periodekode** til den periodetype, du lige har oprettet (*VacYear*).

## <a name="create-a-statistical-balance-setup"></a>Opret konfiguration af statistisk saldo

I dette afsnit kan du oprette en opsætning for *statistisk saldo*, der er knyttet til den lønstatistikgruppe, som du oprettede i forrige afsnit. Du kan senere sammenkæde denne opsætning af statistiske saldi med visningen **Min dag** i brugergrænsefladen for produktionsudførelse. I visningen **Min dag** kan du derefter få vist feriesaldi for den lønart, der er tildelt den tilknyttede lønstatistikgruppe.

1. Gå til **Tid og fremmøde \> Opsætning \> Løn \> Opsætning af statistisk saldo**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Lønstatistikgruppe:** *VAC*
    - **Eksternt navn:** *Feriesaldo*
    - **Fleks:** *Nej*

## <a name="create-a-manual-premium"></a>Oprette manuelt løntillæg

*Manuelle løntillæg* bruges typisk til at give arbejdere ekstra løn for ekstra arbejde. I dette scenario opretter du et manuelt løntillæg, som du kan bruge til at angive den første feriesaldo for hver arbejder.

1. Gå til **Tid og fremmøde \> Opsætning \> Løn \> Manuelle løntillæg**.
1. Vælg **Ny** i handlingsruden for at tilføje en post.
1. Angiv følgende værdier i den nye post:

    - **Læntillæg:** *VAC*
    - **Beskrivelse:** *Justeringer af arbejderes feriesaldo*
    - **Lønart:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Angive en arbejders første feriesaldo og justere den med én dag

Lønadministratorer bruger siden **Godkend** til at gennemse og godkende arbejderes daglige registreringer. I dette scenario påtager du dig rollen som administrator, så du kan angive den første feriesaldo for en arbejder og registrere arbejderens feriedage.

1. Gå til **Tid og fremmøde \> Gennemse og godkend \> Godkend**.
1. I dialogboksen **Godkend** skal du angive følgende felter.

    - **Godkendelsesgruppe** – Vælg den godkendelsesgruppe, du tilhører. (Hvis du arbejder med standardeksempeldata i USMF, findes der kun én godkendelsesgruppe. *AdmMan*.)
    - **Få vist hele gruppen 1 dag** – Vælg indstillingen, og indstil derefter feltet til dags dato.

1. Vælg **OK**.
1. På siden **Godkend** vises en liste over poster, der svarer til dine kriterier. Vælg den arbejder, du vil godkende. Hvis du arbejder med standardeksempeldata i USMF, skal du vælge *000496* (*Christina Portra*).
1. Giv den valgte arbejder 10 feriedage:

    1. Mens arbejderen stadig er markeret, skal du vælge **Løntillægslinjer** i handlingsruden.
    1. På siden **Læntillægslinjer** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret.
    1. Angiv følgende værdier i den nye række:

        - **Læntillæg:** *VAC*
        - **Antal:** *10*

    1. Luk siden **Løntillægslinjer**.

1. På siden **Godkend** skal du registrere, at arbejderen brugte en af sine feriedage på dags dato:

    1. Under fanen **Oversigt** nederst på siden skal du vælge **Ny** på værktøjslinjen for at føje en række til gitteret.
    1. Angiv følgende værdier i den nye række:

        - **Kladder til registrering:** *Fravær*
        - **Reference:** *Ferie*

    1. I øverste del af siden skal du vælge **Overfør** på værktøjslinjen for at anvende feriesaldoen og beregne fradraget.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Konfigurere brugergrænsefladen til produktionsudførelse, så den indeholder dialogboksen Min dag

I dette afsnit vil du tilføje en knap for **Min dag** til brugergrænsefladen for produktionsudførelse. Arbejderne kan derefter bruge denne knap til at åbne dialogboksen **Min dag**.

1. Gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurer kørsel af produktionsudstyr**.
1. Vælg en konfigurationsudbyder som *Standard*.
1. Vælg **Designfaner** i handlingsruden.
1. På siden **Designfaner** skal du vælge *Alle job* i listeruden for at få vist indstillingerne for den pågældende fane. Feltet **Hovedvisning** skal nu vise værdien for *Alle job*.
1. Vælg **Rediger** i handlingsruden.
1. I kolonnen **Tilgængelige handlinger** i oversigtspanelet **Sekundær værktøjslinje** skal du vælge **Min dag**. Vælg knappen tilføj (højre pil) for at flytte den valgte række til kolonnen **Valgte metoder**.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Kontroller saldoen i grænsefladen til kørsel af produktion

I dette afsnit skal du logge på brugergrænsefladen til produktionsudførelse som den arbejder, hvis ferietid du konfigurerede tidligere. Du åbner derefter dialogboksen **Min dag** for at få vist din feriesaldo.

1. Gå til **Produktionsstyring \> Konfiguration \> Produktionsudførelse \> Kørsel af produktionsudstyr**.
1. Hvis du bliver bedt om at vælge en konfiguration, skal du vælge den konfiguration, du konfigurerede tidligere i dette scenario (*standard*).
1. Log på som den bruger, du konfigurerede tidligere i dette scenario. Hvis du arbejder med standard-USMF-eksempeldata, skal du kunne logge på ved at angive *123* i feltet **Kort-id**. Dette kort-id svarer til Christina Portra.
1. Vælg **Min dag** på værktøjslinjen til venstre.
1. Kontrollere sektionen **Saldi** i dialogboksen. Dette afsnit skal nu vise, at du har en saldo på ni feriedage.
