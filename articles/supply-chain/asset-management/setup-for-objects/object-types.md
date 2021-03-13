---
title: Aktivtyper
description: Dette emne beskriver, hvordan du opretter aktivtyper i Styring af aktiver. Det beskriver også de elementer, der er relateret til aktivtyper.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectJobType, EntAssetObjectType, EntAssetObjectTypeDefaultSparePart, EntAssetObjectTypeDefaultSparePartApprove, EntAssetObjectTypeDefaultCreateCombinations, EntAssetObjectTypeDefault, EntAssetObjectTypeDefaultCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 295840c12f89bc6c6a4d53023985259ac761d6b2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017411"
---
# <a name="asset-types"></a>Aktivtyper

[!include [banner](../../includes/banner.md)]



Dette emner beskriver, hvordan du opretter aktivtyper. Det beskriver også de elementer, der er relateret til aktivtyper. Aktivtyper bruges som generelle kategorier for aktiver. Eksempelvis kan nævnes CNC-maskiner, måleudstyr og lastvognsmotorer. Aktivtyper bruges til at administrere vedligeholdelsesjobtyperne (vedligeholdelsesopgaver), aktivers livscyklustilstande, tællere, aktivattributter, skabeloner til tilstandsvurdering og de aktivmodeller, der kan vælges for et aktiv. Når du opretter et aktiv, skal du angive aktivtypen.

For hver aktivtype kan der oprettes variationer af aktivtypens opsætning. Hvis du for eksempel har en aktivtype, der hedder **Lastbiler**, kan du oprette variationer af den pågældende aktivtype for forskellige aktivproducenter og aktivmodeller. Til hver opsætning af aktivtyperne kan du tilføje de påkrævede reservedele og vedligeholdelsesplaner.

Først skal du oprette de påkrævede aktivtyper. Derefter opretter du de aktivmodeller, der skal relateres til aktivtyperne. Endelig skal du på siden **Standarder for aktivtype** oprette alle de varianter af aktivtyper, der kræves til dit udstyr.

## <a name="create-an-asset-type"></a>Opret en aktivtype

1. Vælg **Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Aktivtyper**.
2. Vælg **Ny** for at oprette en aktivtype.
3. Angiv et ID for aktivtypen i feltet **Aktivtype**.
4. Indtast et navn i feltet **Navn**.
5. Vælg en aktivlivscyklusmodel for i feltet **Aktivlivscyklusmodel**. Du finder flere oplysninger om livscyklustilstande og livscyklusmodeller for aktiver i [Aktivlivscykjlustilstande](object-stages.md).
6. Angiv indstillingen **Total** til **Ja**, hvis de sammenlagte KPI-værdier skal beregnes for aktiver, der har denne aktivtype.
7. Vælg **Gem**.
8. I oversigtspanelet **Vedligeholdelsesjobtyper** skal du vælge de vedligeholdelsesjobtyper, der skal relateres til aktivtypen:

    - Hvis du vil vælge en vedligeholdelsesjobtype, skal du vælge den i feltet **Resterende vedligeholdelsesjobtyper** og derefter vælge højre pileknap ![Højre pileknap](media/29-setup-for-objects.png) for at flytte den til sektionen **Valgte vedligeholdelsesjobtyper**.
    - Hvis du vil vælge alle tilgængelige vedligeholdelsesjobtyper, skal du vælge pileknappen ![Fremsend alle](media/30-setup-for-objects.png). Alle vedligeholdelsesjobtyper overføres fra feltet **Resterende vedligeholdelsesjobtyper** til feltet **Valgte vedligeholdelsesjobtyper**.
    - Hvis du vil annullere den valgte vedligeholdelsesjobtype, skal du vælge den i feltet **Valgte vedligeholdelsesjobtyper** og derefter vælge venstre pileknap ![Venstre pileknap](media/31-setup-for-objects.png) for at flytte den til feltet **Resterende vedligeholdelsesjobtyper**.

9. Du kan også vælge de tællere, som skal relateres til aktivtypen. Foretag dine valg i oversigtspanelet **Tællere** ved hjælp af de metoder, der er beskrevet for vedligeholdelsesjobtyper i trin 8. Du kan finde flere oplysninger om, hvordan du konfigurerer tællere, i [Tællere](counters.md).
10. Du kan også vælge de attributtyper, som skal relateres til aktivtyperne. Foretag dine valg i oversigtspanelet **Attributtyper** ved hjælp af de metoder, der er beskrevet for vedligeholdelsesjobtyper i trin 8. Hvis du derefter vil oprette den foretrukne rækkefølge af attributtyper, skal du i feltet **Valgte attributtyper** vælge en attributtype og bruge knapperne pil op og pil ned til at flytte det. Rækkefølgen af attributtyper vises på aktiver, der bruger denne aktivtype. Du finder flere oplysninger om aktivattributter under [Vedligeholdelsesattributtyper](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Når du tilføjer nye attributtyper i oversigtspanelet **Attributtyper**, opdateres eksisterende aktiver automatisk med disse oplysninger.

11. Du kan også vælge de skabeloner for tilstandsvurderinger, som skal relateres til aktivtyperne. Foretag dine valg i oversigtspanelet **Tilstandsvurderinger** ved hjælp af de metoder, der er beskrevet for vedligeholdelsesjobtyper i trin 8. Du finder flere oplysninger om skabeloner for og registreringer af tilstandsvurderinger i [Tilstandsvurdering](../setup-for-objects/condition-assessment.md).
12. I oversigtspanelet **Aktivmodel** vises alle kombinationer af aktivproducenter og -modeller, der er konfigureret på den valgte aktivtype. Hvis du vil se de kombinationer, som er inddelt efter producent, skal du vælge **Aktivmodel** for at åbne siden **Aktivmodel**.

    På siden **Aktivmodel** kan du tilføje aktivmodel–aktivtyperelationer. Derudover kan du på siden **Aktivtyper** tilføje aktivproducent–akti modelrelationer direkte til en aktivtype. Slutteligt kan du på siden **Aktivmodel** (**Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Aktivmodel**) oprette nye aktivproducent–aktivmodel–aktivtyperelationer. Der er derfor tre måder at oprette og redigere aktivproducent–aktivmodel–aktivtyperelationer på. Alle tilgængelige kombinationer vises fra forskellige perspektiver, og du kan vælge dit foretrukne indgangspunkt, når du arbejder med opsætningen.

> [!NOTE]
> - Hvis du vælger tællere på en aktivtype, opdateres valgene automatisk på siden **Tællere** (**Styring af aktiver** > **Opsætning** > **Aktiver** > **Aktivtyper** > **Tællere**).
> - Felterne i sektionen **Detaljer** i oversigtspanelet **Generelt** viser antallet af vedligeholdelsesjobtyper, tællere, attributter osv., der er konfigureret på den valgte aktivtype.

Arbejdsordrer, der oprettes manuelt, er typisk relateret til korrigerende vedligeholdelse, hvorimod arbejdsordrer, der oprettes automatisk, er relateret til forebyggende vedligeholdelse. Når du opretter arbejdsordrer manuelt, er det kun de vedligeholdelsesjobtyper, der er valgt i oversigtspanelet **Vedligeholdelsesjobtyper** på siden **Aktivtyper**, der kan bruges. Dog kan automatisk oprettede arbejdsordrer bruge alle de vedligeholdelsesjobtyper, du opretter på siden **Vedligeholdelsesjobtyper** (**Styring af aktiver** \> **Opsætning** \> **Job** \> **Vedligeholdelsesjobtyper**).

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

