---
title: Aktivtyper
description: Dette emne beskriver, hvordan du opretter aktivtyper i Styring af aktiver. Det beskriver også de elementer, der er relateret til aktivtyper.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288dac77f9d999012ec930ef2bca5c0921c2955f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783158"
---
# <a name="asset-types"></a>Aktivtyper

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emner beskriver, hvordan du opretter aktivtyper. Det beskriver også de elementer, der er relateret til aktivtyper. Aktivtyper bruges som generelle kategorier for aktiver. Eksempelvis kan nævnes CNC-maskiner, måleudstyr og lastvognsmotorer. Aktivtyper bruges til at administrere jobtyperne (vedligeholdelsesopgaver), aktivers livscyklustilstande, aktivmålinger, aktivattributter, skabeloner til tilstandsvurdering og de aktivmodeller, der kan vælges for et aktiv. Når du opretter et aktiv, skal du angive aktivtypen.

For hver aktivtype kan der oprettes variationer af aktivtypens opsætning. Hvis du for eksempel har en aktivtype, der hedder **Lastbiler**, kan du oprette variationer af den pågældende aktivtype for forskellige aktivproducenter og aktivmodeller. Til hver opsætning af aktivtyperne kan du tilføje de påkrævede reservedele og vedligeholdelsesplaner.

Først skal du oprette de påkrævede aktivtyper. Derefter opretter du de aktivmodeller, der skal relateres til aktivtyperne. Endelig skal du på siden **Standarder for aktivtype** oprette alle de varianter af aktivtyper, der kræves til dit udstyr.

## <a name="create-an-asset-type"></a>Opret en aktivtype

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktivtype** \> **Aktivtyper**.
2. Vælg **Ny** for at oprette en aktivtype.
3. Angiv et ID for aktivtypen i feltet **Aktivtype**.
4. Indtast et navn i feltet **Navn**.
5. Vælg en aktivlivscyklusmodel for i feltet **Aktivlivscyklusmodel**. Du finder flere oplysninger om livscyklustilstande og livscyklusmodeller for aktiver i [Aktivlivscykjlustilstande](object-stages.md).
6. Angiv indstillingen **Total** til **Ja**, hvis de sammenlagte KPI-værdier skal beregnes for aktiver, der har denne aktivtype.
7. Vælg **Gem**.
8. I oversigtspanelet **Jobtyper** skal du vælge de jobtyper, der skal relateres til aktivtypen:

    - Hvis du vil vælge en jobtype, skal du vælge den i feltet **Resterende jobtyper** og derefter vælge højre pileknap ![Højre pileknap](media/29-setup-for-objects.png) for at flytte den til sektionen **Valgte jobtyper**.
    - Hvis du vil vælge alle tilgængelige jobtyper, skal du vælge knappen ![Fremsend alle](media/30-setup-for-objects.png). Alle jobtyper overføres fra feltet **Resterende jobtyper** til feltet **Valgte jobtyper**.
    - Hvis du vil annullere den valgte jobtype, skal du vælge den i feltet **Valgte jobtyper** og derefter vælge venstre pileknap ![Venstre pileknap](media/31-setup-for-objects.png) for at flytte den til feltet **Resterende jobtyper**.

9. Du kan også vælge de aktivmålinger, som skal relateres til aktivtyperne. Foretag dine valg i oversigtspanelet **Aktivmålinger** ved hjælp af de metoder, der er beskrevet for jobtyper i trin 8. Du finder flere oplysninger om opsætningen af aktivmålinger i [Vedligeholdelse af aktivmålinger](counters.md).
10. Du kan også vælge de attributtyper, som skal relateres til aktivtyperne. Foretag dine valg i oversigtspanelet **Attributtyper** ved hjælp af de metoder, der er beskrevet for jobtyper i trin 8. Hvis du derefter vil oprette den foretrukne rækkefølge af attributtyper, skal du i feltet **Valgte attributtyper** vælge en attributtype og bruge knapperne pil op og pil ned til at flytte det. Rækkefølgen af attributtyper vises på aktiver, der bruger denne aktivtype. Du finder flere oplysninger om aktivattributter under [Vedligeholdelsesattributtyper](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Når du tilføjer nye attributtyper i oversigtspanelet **Attributtyper**, opdateres eksisterende aktiver automatisk med disse oplysninger.

11. Du kan også vælge de skabeloner for tilstandsvurderinger, som skal relateres til aktivtyperne. Foretag dine valg i oversigtspanelet **Tilstandsvurderinger** ved hjælp af de metoder, der er beskrevet for jobtyper i trin 8. Du finder flere oplysninger om skabeloner for og registreringer af tilstandsvurderinger i [Tilstandsvurdering](../setup-for-objects/condition-assessment.md).
12. I oversigtspanelet **Aktivmodel** vises alle kombinationer af aktivproducenter og -modeller, der er konfigureret på den valgte aktivtype. Hvis du vil se de kombinationer, som er inddelt efter producent, skal du vælge **Aktivmodel** for at åbne siden **Aktivmodel**.

    På siden **Aktivmodel** kan du tilføje aktivmodel–aktivtyperelationer. Derudover kan du på siden **Aktivtyper** tilføje aktivproducent–akti modelrelationer direkte til en aktivtype. Slutteligt kan du på siden **Aktivmodel** (**Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Aktivmodel**) oprette nye aktivproducent–aktivmodel–aktivtyperelationer. Der er derfor tre måder at oprette og redigere aktivproducent–aktivmodel–aktivtyperelationer på. Alle tilgængelige kombinationer vises fra forskellige perspektiver, og du kan vælge dit foretrukne indgangspunkt, når du arbejder med opsætningen.

> [!NOTE]
> - Hvis du vælger aktivmålinger på en aktivtype, bliver valgene automatisk opdateret på siden **Aktivmålinger** (**Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Aktivtyper** \> **Aktivmålinger**).
> - Felterne i sektionen **Detaljer** i oversigtspanelet **Generelt** viser antallet af jobtyper, aktivmålinger, -attributter osv., der er oprettet på den valgte aktivtype.

Arbejdsordrer, der oprettes manuelt, er typisk relateret til korrigerende vedligeholdelse, hvorimod arbejdsordrer, der oprettes automatisk, er relateret til forebyggende vedligeholdelse. Når du opretter arbejdsordrer manuelt, er det kun de jobtyper, der er valgt i oversigtspanelet **Jobtyper** på siden **Aktivtyper**, der kan bruges. Dog kan automatisk oprettede arbejdsordrer bruge alle de jobtyper, du opretter på siden **Jobtyper** (**Styring af aktiver** \> **Opsætning** \> **Job** \> **Jobtyper**).

## <a name="create-asset-type-setup-lines"></a>Opret opsætningslinjer for aktivtype

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Aktivtyper** \> **Opsætning af aktivtyper**. Du kan som alternativ vælge **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Aktivtyper** \> **Aktivtyper**, vælge en aktivtype og dernæst vælge **Opsætning af aktivtype**.
2. Første gang du bruger siden **Opsætning af aktivtype**, vil du med fordel kunne bruge knappen **Opret kombinationer**. Du kan bruge denne knap til hurtigt at oprette alle kombinationer af en aktivmodel på en aktivtype. Vælg **Opret kombinationer**, vælg den aktivtype, du vil oprette kombinationer for, og vælg derefter **OK**.

    > [!NOTE]
    > Hvis du ikke vil bruge alle de opsætningskombinationer af aktivtypen, der blev oprettet automatisk, kan du slette en opsætning ved at markere den og derefter vælge **Slet**.

3. Vælg **Ny** for manuelt at oprette en opsætning for en aktivtype.
4. Afhængigt af, hvor specifik opsætningen af aktivtypen skal være, skal du foretage valg i felterne **Aktivtype**, **Producent** og **Model**.
5. Hvis en garantiaftale er relateret til aktivtypen, skal du vælge aftalen i felterne **Leverandørgaranti** og **Kundegaranti**. 
6. I oversigtspanelet **Reservedele** skal du vælge **Tilføj** for at føje reservedele til den valgte opsætning af aktivtyper.
7. Hvis du vil godkende en reservedel, skal du vælge reservedelslinjen og derefter vælge **Godkend**. Du kan vælge flere linjer til godkendelse.
8. Hvis du vil se, om en reservedel bruges et andet sted i Styring af aktiver (f.eks. i relation til aktiver og arbejdsordrer), skal du vælge reservedelslinjen og derefter vælge **Vare, hvor den bruges** til at åbne siden **Vare, hvor den bruges**. Hvis du vil se alle aktivers reservedele på listen, skal du markere afkrydsningsfeltet **Aktiv**. Hvis du kun vil se godkendte reservedele, skal du markere afkrydsningsfeltet **Godkendt**.
9. I oversigtspanelet **Vedligeholdelsesplaner** skal du vælge **Tilføj** for at føje vedligeholdelsesplaner til den valgte opsætning af aktivtyper.
10. Hvis du vil kopiere opsætningen af en aktivtype til en anden opsætning, kan du bruge kopieringsfunktionen. Vælg opsætningen af den aktivtype, du vil kopiere en opsætning til, vælg **Kopier opsætning**, og vælg den aktivtypeopsætning, du vil kopiere opsætningen fra. Indstillingerne for de forskellige valgmuligheder afgør, hvor mange oplysninger der er inkluderet. Når du er færdig, skal du vælge **OK** for at kopiere opsætningen.

> [!NOTE]
> Hvis du har mange linjer for reservedele og vedligeholdelsesplaner, som du vil gerne vil genbruge, giver kopieringsfunktionen dig mulighed for hurtigt og nemt at konfigurere data for mange kombinationer af aktivtypeopsætninger.

## <a name="spare-parts-on-the-asset-type-setup"></a>Reservedele i opsætningen af aktivtype

Som det blev beskrevet i afsnittet "Opret opsætningslinjer for aktivtype", konfigureres reservedele på aktivmodeller på siden **Opsætning af aktivtype**. Når du åbner siden **Opsætning af aktivtype**, får du derfor kun vist de reservedele, der er relateret til den valgte kombination af en aktivtype, en aktivproducent og en aktivmodel. Hvis du vil se en liste over alle reservedelsposter, skal du åbne siden **Reservedele** (**Styring af aktiver** \> **Forespørgsler** \> **Reservedele**).

På siden **Reservedele** kan du også oprette nye reservedele til eksisterende kombinationer af en aktivtype, en aktivproducent og en aktivmodel. Du kan selv bestemme, om du foretrækker at oprette reservedelsposter på siden **Opsætning af aktivtype** eller siden **Reservedele**. Siden **Opsætning af aktivtype** indeholder en oversigt over data for den valgte kombination af en aktivtype, en aktivproducent og en aktivmodel, hvorimod siden **Reservedele** indeholder en komplet oversigt over alle opsætningslinjer for aktivtyper. Hvis siden **Reservedele** indeholder mange poster, kan siden **Opsætning af aktivtype** give dig et bedre overblik.

Hvis du vil se, om reservedelen på den valgte linje bruges et sted i Styring af aktiver (f.eks. i relation til aktiver og arbejdsordrer), skal du vælge **Vare, hvor den bruges** til at åbne siden **Vare, hvor den bruges**. 

