---
title: Arkivere lagertransaktioner
description: Dette emne beskriver, hvordan du arkiverer lagertransaktionsdata for at forbedre systemets ydeevne.
author: yufeihuang
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 99a7b61d9bd5e1e2bd8d2c7df34882646bb51270
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567457"
---
# <a name="archive-inventory-transactions"></a>Arkivere lagertransaktioner

[!include [banner](../../includes/banner.md)]

Med tiden fortsætter tabellen med lagertransaktioner (`InventTrans`) med at stige og forbruge mere databaseplads. Derfor bliver de forespørgsler, der foretages mod tabellen, efterhånden langsommere. Dette emne beskriver, hvordan du kan bruge funktionen *Arkivér lagertransaktioner* til at arkivere data om lagertransaktioner for at forbedre systemets ydeevne.

> [!NOTE]
> Det er kun økonomisk opdaterede lagertransaktioner, der kan arkiveres i en valgt lukket finansperiode. Hvis du vil arkivere, skal økonomisk opdaterede udgående lagertransaktioner have afgangsstatussen *Solgt*, og indgående lagertransaktioner skal have tilgangsstatussen *Købt*.

Når du arkiverer lagertransaktioner, flyttes alle relaterede transaktioner til tabellen `InventTransArchive`. Lagerafgangstransaktioner og lagertilgangstransaktioner arkiveres separat baseret på kombinationen af vare-id (`itemId`) og lagerdimensions-id (`inventDimId`), og de indgår i de opsummerede afgangs- og opsummerede tilgangstransaktioner.

Hvis en kombination af `itemId` og `inventDimId` kun indeholder én tilgangs- eller afgangstransaktion, arkiveres transaktionen ikke.

## <a name="turn-on-the-feature-in-your-system"></a>Aktivere funktionen i systemet

Hvis systemet ikke allerede indeholder de funktioner, der er beskrevet i dette emne, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Arkivér lagertransaktioner*. Bemærk, at denne funktion ikke kan deaktiveres, når den først er aktiveret.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Ting, der skal overvejes, før du arkiverer lagertransaktioner

Før du arkiverer lagertransaktioner, skal du overveje følgende forretningsscenarier, da de påvirkes af operationen:

- Når du overvåger lagertransaktioner fra relaterede dokumenter som f.eks. indkøbsordrelinjer, vises de som arkiverede. Du kan gennemse de arkiverede transaktioner ved at gå til **Lagerstyring \> Periodiske opgaver \> Oprydning \> Arkivér lagertransaktioner**.
- Lagerlukning kan ikke annulleres i arkiverede perioder. Før du kan annullere en lagerlukning, skal du tilbageføre lagertransaktionsarkivet for den relevante periode.
- Standardomkostningskonvertering kan ikke udføres for arkiverede perioder. Før du kan udføre standardomkostningskonvertering, skal du tilbageføre lagertransaktionsarkivet for den relevante periode.
- Lagerrapporter, der er hentet fra lagertransaktioner, påvirkes, når du arkiverer lagertransaktioner. Disse rapporter omfatter rapport over aldersfordelt lager og rapport over lagerværdier.
- Lagerbudgetter kan påvirkes, hvis de køres i tidshorisonten for arkiverede perioder.

## <a name="prerequisites"></a>Forudsætninger

Lagertransaktioner kan kun arkiveres i perioder, hvor følgende betingelser er opfyldt:

- Finansperioden skal være lukket.
- Lagerlukning skal køres på eller efter til-periodedatoen for arkivet.
- Perioden skal være mindst ét år før fra-periodedatoen for arkivet.
- Der må ikke være eksisterende genberegninger af lager.

## <a name="archive-inventory-transactions"></a>Arkivere lagertransaktioner

Benyt følgende trin for at arkivere lagertransaktioner.

1. Gå til **Lagerstyring** \> **Periodiske opgaver** \> **Oprydning** \> **Arkivér lagertransaktioner**.

    Siden **Arkivér lagertransaktioner** vises med en liste over arkiverede procesposter.

    ![Siden Arkivér lagertransaktioner.](media/archive-inventory-empty.png "Siden Arkivér lagertransaktioner")

1. Vælg **Arkivér lagertransaktioner** i handlingsruden for at oprette et lagerposteringsarkiv.
1. Angiv følgende felter i oversigtspanelet **Parametre** i dialogboksen **Arkivér lagertransaktioner**:

    - **Fra dato i lukket finansperiode** – Vælg den tidligste transaktionsdato, der skal medtages i arkivet.
    - **Til dato i lukket finansperiode** – Vælg den seneste transaktionsdato, der skal medtages i arkivet.

    ![Dialogboksen Arkivér lagertransaktioner.](media/archive-inventory-dates.png "Dialogboksen Arkivér lagertransaktioner")

    > [!NOTE]
    > Det er kun perioder, der opfylder [forudsætningerne](#prerequisites), som kan vælges.

1. Konfigurer batchafviklingsdetaljer efter behov i oversigtspanelet **Kør i baggrunden**. Følg de normale trin for batchjob i Microsoft Dynamics 365 Supply Chain Management.
1. Vælg **OK**.
1. Du modtager en meddelelse, hvor du bliver bedt om at bekræfte, at du vil fortsætte. Læs meddelelsen omhyggeligt, og vælg derefter **Ja**, hvis du vil fortsætte.

    Du modtager en meddelelse om, at lagertransaktionernes arkivjob er føjet til batchkøen. Jobbet vil nu begynde at arkivere lagertransaktioner fra den valgte periode.

## <a name="view-archived-inventory-transactions"></a>Vis arkiverede lagertransaktioner

Siden **Arkivér lagertransaktioner** viser hele din arkiveringshistorik. Hver række i gitteret indeholder oplysninger som f.eks. den dato, hvor arkivet blev oprettet, den bruger, der oprettede det, og statussen.

![Arkiveringshistorik på siden Arkivér lagertransaktioner.](media/archive-inventory-full.png "Arkiveringshistorik på siden Arkivér lagertransaktioner")

Vælg en af følgende værdier på rullelisten øverst på siden for at filtrere de arkiver, der vises i gitteret:

- **Aktiv** – Vis kun aktive arkiver, ikke tilbageførte arkiver.
- **Alle** – Vis alle arkiver, både aktive og tilbageførte.

For hvert arkiv i gitteret gives følgende oplysninger:

- **Aktiv** – En markering angiver, at arkivet er aktivt.
- **Fra dato** – Datoen på den ældste transaktion, der kan medtages i arkivet.
- **Til dato** – Datoen på den seneste transaktion, der kan medtages i arkivet.
- **Planlagt af** – Den brugerkonto, der oprettede arkivet.
- **Udført** – Datoen for oprettelsen af arkivet.
- **Tilbageført** – En markering angiver, at arkivet er tilbageført.
- **Stop aktuel opdatering** – En markering angiver, at arkivering er i gang, men det er blevet sat på pause.
- **Tilstand** – Behandlingsstatus for arkivet. De mulige værdier er *Venter*, *I gang* og *Udført*.

Værktøjslinjen over gitteret indeholder følgende knapper, du kan bruge til at arbejde med et valgt arkiv:

- **Arkiverede transaktioner** – Få vist alle detaljer i det valgte arkiv. Siden **Arkiverede transaktioner** viser alle transaktionerne i arkivet.

    ![Siden Arkiverede transaktioner.](media/archive-inventory-transactions.png "Siden Arkiverede transaktioner")

    Hvis du vil have vist flere oplysninger om en bestemt transaktion på siden **Arkiverede transaktioner**, skal du vælge den i gitteret og derefter vælge **Arkiverede transaktionsdetaljer** i handlingsruden. Siden **Arkiverede transaktionsdetaljer** viser oplysninger som f.eks. finanspostering, referencer til relateret reskontro og økonomiske dimensioner.

- **Afbryd arkivering midlertidigt** – Afbryd et valgt arkiv midlertidigt, som er ved at blive behandlet. Denne pause træder først i kraft, når arkiveringsopgaven er oprettet. Derfor kan der være en kort forsinkelse, før pausen træder i kraft. Hvis et arkiv er blevet afbrudt midlertidigt, vises der en markering i feltet **Stop aktuel opdatering**.
- **Fortsæt arkivering** – Fortsæt behandlingen af et valgt arkiv, som er afbrudt midlertidigt.
- **Tilbagefør** – Tilbagefør det valgte arkiv. Du kan kun tilbageføre et arkiv, hvis feltet **Tilstand** er angivet til *Udført*. Hvis et arkiv er blevet tilbageført, vises der en markering i feltet **Tilbageført**.
