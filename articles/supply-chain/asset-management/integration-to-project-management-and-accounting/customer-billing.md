---
title: Fakturere for vedligeholdelse af aktiver, der ejes af kunder
description: Denne artikel indeholder en forklaring på, hvordan du kan oprette, behandle og fakturere vedligeholdelsesarbejde, der udføres på aktiver, som dine kunder ejer.
author: johanhoffmann
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b7c2c07f3e3eb76ff20e37e8d5d485dc08232c7a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220416"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Fakturere for vedligeholdelse af aktiver, der ejes af kunder

[!include [banner](../../includes/banner.md)]

Med funktionen *Fakturering af arbejdsordre* kan du oprette, behandle og fakturere vedligeholdelsesarbejde på aktiver, som dine kunder ejer. Du kan udføre følgende opgaver med denne funktion:

- Knytte kunder til de aktiver, de ejer.
- Vælg en kunde, og se de aktiver, som kunden ejer, når du opretter en arbejdsordre.
- Konfigurer et overordnet projekt for hver kunde.
- Registrer timer, varer, udgifter og gebyrer på arbejdsordren, og opret derefter et fakturaforslag til kunden senere.

Funktionen har desuden følgende egenskaber:

- Projektkontrakten fra en kundes overordnede projekt kopieres automatisk til det relevante arbejdsordreprojekt.
- Aktivstyring kan nu bruge projekttransaktionstypen *Gebyr* i både prognoser for arbejdsordrer og arbejdsordrekladder.

## <a name="turn-on-the-customer-billing-feature"></a>Slå funktionen for kundefakturering til

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Projektstyring og regnskab*
- **Funktionsnavn:** *Fakturering af arbejdsordre*

## <a name="example-scenario"></a>Eksempelscenario

Du kan få mere at vide om, hvordan funktionen fungerer, ved at følge nedenstående eksempelscenarie.

Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret. Du skal vælge den juridiske enhed **USMF**, før du starter.

Du kan også bruge dette scenarie som vejledning til brug af funktionen, når du arbejder i et produktionssystem. Du skal dog i det tilfælde erstatte dine egne værdier, og du mangler muligvis nogle typer påkrævede poster, som standarddemodataene giver.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>Trin 1: Opret en ny projektkontrakt for kunden

1. Gå til **Projektstyring og regnskab \> Projekter \> Projektkontrakter**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Ny projektkontrakt**:

    - **Navn:** *Pelican Wholesales*
    - **Finansieringstype:** *Kunde*
    - **Finansieringskilde:** *US-013* (*Pelican Wholesales*)

1. Vælg **OK**.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>Trin 2: Opret et nyt overordnet projekt for kunden

Det overordnede projekt, som du opretter her, bruges, når der oprettes arbejdsordrer for kunden.

1. Gå til **Projektstyring og regnskab \> Projekter \> Alle projekter**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Nyt projekt**:

    - **Projekttype:** *Tid og materialer*
    - **Projektnavn:** *Pelican Wholesales-arbejdsordrer*
    - **Projektgruppe:** *TM*
    - **Projektkontrakt-id:** *Pelican Wholesales* (den kontrakt, du oprettede tidligere)
    - **Startdato:** Vælg dags dato.

1. Vælg **Opret projekt**.
1. Det nye projekt åbnes. Notér dig værdien af **Projekt-id**. Du skal angive det senere.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>Trin 3: Opret en ny arbejdsordretype i Aktivstyring

1. Gå til **Styring af aktiver \> Opsætning \> Arbejdsordre \> Arbejdsordretyper**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Der føjes en ny post til listen. Angiv følgende værdier for den:

    - **Arbejdsordretype:** *Service*
    - **Navn:** *Servicearbejdsordrer*
    - **Livscyklustilstand for arbejdsordre:** *Standard*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>Trin 4: Knyt kundekontoen til det overordnede projekt

Du skal nu knytte kundekontoen til det overordnede projekt i projektopsætningen i Aktivstyring.

1. Gå til **Styring af aktiver \> Opsætning \> Arbejdsordrer \> Opsætning af projekt**.
1. På fanen **Overordnet projekt** skal du vælge **Tilføj** for at tilføje en ny linje.
1. Angiv følgende værdier på den nye linje:

    - **Debitorkonto:** *US-013* (*Pelican Wholesales*)
    - **Projekt-id:** Angiv det projekt-id, du har noteret tidligere.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>Trin 5: Knyt projektgruppen og typen til arbejdsordreprojektet

Du bør stadig være på siden **Opsætning af Projekt** (**Styring af aktiver \> Opsætning \> Arbejdsordrer \> Opsætning af Projekt**).

1. På fanen **Projektgruppe** skal du vælge **Tilføj** for at tilføje en ny linje.
1. Angiv følgende værdier på den nye linje:

    - **Arbejdsordretype:** *Service* (den arbejdsordretype, du oprettede tidligere)
    - **Projektgruppe:** *TM*

> [!NOTE]
> Projektkontrakten på arbejdsordreprojektet nedarves altid fra det overordnede projekt.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>Trin 6: Knyt et aktiv til kunde-id'et

1. Gå til **Styring af aktiver \> Aktiver \> Alle aktiver**.
1. Angiv **VE-102** i feltet *Filter*, og vælg at filtrere efter **Aktiv**.
1. Vælg aktivet for at åbne dets indstillinger.
1. Gå til oversigtspanelet **Kunde**, og angiv feltet **Debitorkonto** til *US-013* (*Pelican Wholesales*).

    Feltet **Navn** opdateres automatisk til *Pelican Wholesales*.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>Trin 7: Opret en ny arbejdsordre på aktivet

1. Gå til **Styring af aktiver \> Arbejdsordrer \> Aktive arbejdsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret arbejdsordre**:

    - **Arbejdsordretype:** *Service*
    - **Beskrivelse:** *Reparer lastvogn*
    - **Debitorkonto:** *US-013* (*Pelican Wholesales*)
    - **Aktiv:** *VE-102*

        > [!NOTE]
        > Opslaget viser kun aktiver, der er knyttet til den valgte kundekonto.

    - **Vedligeholdelsesjobtype:** *Reparation*
    - **Branche:** *Mekanik*
    - **Serviceniveau:** *4*

1. Vælg **OK**.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>Trin 8: Gennemse arbejdsordren, og begynd at arbejde på den

I dette afsnit arbejder du med den arbejdsordre, du oprettede i forrige afsnit.

1. Benyt følgende fremgangsmåde for at kontrollere, at det overordnede projekt er *Pelican Wholesales-arbejdsordrer*:

    1. Vælg en linje i sektionen **Vedligeholdelsesjob for arbejdsordre**.
    1. Kontrollér værdien af **Projekt-id** i oversigtspanelet **Linjedetaljer**. Det skal være et nummer med bindestreg i formatet *\<Parent-Project-ID\>-\<Project-ID\>*. Denne værdi er et link.
    1. Vælg linket til projekt-id'et for at åbne en side, hvor du kan se det overordnede projekt og projektnavnene.

1. Vælg **Opdatere tilstand for arbejdsordre** i gruppen **Livscyklustilstand** under fanen **Arbejdsordre** i handlingsruden.
1. I dialogboksen **Opdatere tilstand for arbejdsordre** skal du i kolonnen **Vælg** markere afkrydsningsfeltet for den række, hvor feltet **Livscyklustilstand** er angivet til *I gang*.
1. Vælg **OK**.
1. I dialogboksen **Livscyklustilstand: I gang** skal du vælge **OK**.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>Trin 9: Bogfør de timer, der er brugt på arbejdsordren, og opret et nyt fakturaforslag

I dette afsnit arbejder du fortsat med den arbejdsordre, du arbejdede på i forrige afsnit.

1. Vælg **Kladder** i gruppen **Projekt** under fanen **Arbejdsordre** i handlingsruden.

    Siden **Arbejdsordrekladder** vises. Her kan du registrere den tid, du har brugt på arbejdsordren.

1. Vælg **Tilføj linje** i oversigtspanelet **Timer**.
1. Angiv feltet **Timer** til *4* på den nye linje.
1. Vælg **Bogfør kladder** i handlingsruden.
1. Luk siden **Arbejdsordrekladder** for at vende tilbage til arbejdsordren.
1. I handlingsruden skal du under fanen **Fakturering** vælge **Nyt fakturaforslag**.
1. Markér afkrydsningsfeltet **Vælg** ud for hver linje, du vil fakturere, i sektionen **Projekttransaktioner** i dialogboksen **Opret fakturaforslag**.
1. Vælg **OK** for at lukke dialogboksen og se fakturaforslaget.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]