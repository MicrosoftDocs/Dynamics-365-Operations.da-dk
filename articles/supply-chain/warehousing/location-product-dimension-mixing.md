---
title: Blanding af produktdimension for lokation
description: Dette emne indeholder oplysninger om blanding af produktdimensioner på lokation. Denne lokationsprofilfunktion hjælper med at forbedre lokationsstyringen, når der bruges produktvarianter eller produkter med dimensioner, f.eks. i modebranchen. Den giver dig mulighed for at bestemme, om konfigurationer, farver, stilarter og størrelser kan blandes for en bestemt lokationsprofil, eller om kun en af disse dimensioner eller en kombination af dem kan placeres på samme lokation.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c4e42864bfde9ed0650a88961b5a71b33b34c89d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004596"
---
# <a name="location-product-dimension-mixing"></a>Blanding af produktdimension for lokation

[!include [banner](../includes/banner.md)]

Blanding af produktdimensioner på lokation er en lokationsprofilfunktion, der forbedrer lokationsstyringen, når der bruges produktvarianter eller produkter med dimensioner, f.eks. i modebranchen. Den giver dig mulighed for at bestemme, om konfigurationer, farver, stilarter og størrelser kan blandes for en bestemt lokationsprofil, eller om kun en af disse dimensioner eller en kombination af dem kan placeres på samme lokation.

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a>Slå funktionen til blanding af produktdimensioner på lokation til

Før du kan bruge funktionen til blanding af produktdimensioner for sted, skal den være aktiveret i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Blanding af produktdimensioner på lokation*

## <a name="setup"></a>Konfiguration

Hver lokalitet på lagerstedet skal have tilknyttet en lokalitetsprofil, der beskriver egenskaberne for lokaliteten. Derfor vil alle lokationer, der bruger samme lokationsprofil, kunne tillade kombinationen af produktdimensioner, efter at den er konfigureret.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Konfigurer lokationsprofiler, der tillader blanding af produktdimensioner

1. Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.
1. Vælg **MASSE** på listen over lokationsprofiler.
1. Vælg **Rediger** i handlingsruden.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Aktivér specifik blanding af produktdimensioner på lokation** til *Ja*.

    > [!NOTE]
    > Du kan kun angive denne indstilling til *Ja*, hvis indstillingen **Tillad blandede varer** er angivet til *Nej*.

1. I oversigtspanelet **Tilladt blanding af produktdimensioner** skal du angive **Størrelse** til *Ja*. I det scenarie, der beskrives i dette emne, kan der kun foretages blanding for produkter med forskellige **størrelsesdimensioner**. Der findes dog også andre indstillinger.
1. Vælg **Gem**.

### <a name="create-a-new-product-master-and-product-variants"></a>Opret en ny produktmaster og produktvarianter

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktmastere**.
1. Vælg **Ny** i handlingsruden for at oprette en produktmaster.
1. Angiv følgende værdier i dialogboksen **Nyt produkt**:

    - **Produkttype:** *Vare*
    - **Produktundertype:** *Produktmaster*
    - **Produktnummer:** *B0001*
    - **Produktnavn:** *B0001-størrelse*
    - **Produktdimensionsgruppe:** *Størrelse*
    - **Konfigurationsteknologi:** *Foruddefineret variant*

1. Vælg **OK**.
1. Gå til siden **Produktdetaljer** i oversigtspanelet **Generelt**, og angiv følgende værdier:

    - **Generér varianter automatisk:** *Ja*
    - **Størrelsesgruppe:** *CASUALDHIR*

1. Hvis du vil have vist de foruddefinerede varianter, skal du vælge **Produktvarianter** i handlingsruden.

    Siden **Produktvarianter** vises og angiver en liste over varianter fra konfigurationen af størrelsesgruppen.

### <a name="release-products-to-the-usmf-company"></a>Frigive produkter til USMF-firmaet

1. Vælg **Frigiv produkter** i handlingsruden.
1. På siden **Vælg produkter, der skal frigives**, skal du bekræfte, at produktnummeret *B0001* er på listen og derefter vælge **Næste**.
1. Vælg **Næste** for at bekræfte de produktvarianter, der skal frigives.
1. På siden **Vælg firmaer, der skal frigives til**, skal du vælge *USMF* og derefter vælge **Næste** for at bekræfte valget.
1. Klik på **Bekræft valg** skal du vælge **Udfør** for at fuldføre frigivelsen.

    Du får vist meddelelsen "Operationen er udført".

### <a name="update-a-released-product-in-the-usmf-company"></a>Opdatere et frigivet produkt i USMF-firmaet

1. Kontroller, at du er logget på **USMF**-firmaet.
1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter** for at færdiggøre oprettelse af det frigivne produkt.
1. Find og vælg varenummer *B0001* for at åbne siden **Frigivne produktdetaljer**.
1. Vælg **Rediger** i handlingsruden.
1. I oversigtspanelet **Generelt** skal du kontrollere, at feltet **Varemodelgruppe** er angivet til *FIFO*.
1. Gå til handlingsruden, og vælg **Dimensionsgrupper** i gruppen **Opsætning** under fanen **Produkt**.
1. Angiv følgende værdier:

    - **Lagringsdimensionsgruppe:** *Ware*
    - **Sporingsdimensionsgruppe:** *Ingen*

1. Vælg **OK**.
1. Gå til handlingsruden, og vælg **Reservationshierarki** i gruppen **Opsætning** under fanen **Produkt**.
1. Angiv feltet **Reservationshierarki** til *Standard*, og vælg derefter **OK**.
1. I oversigtspanelet **Generelt** skal du i sektionen **Administration** bemærke, at dine valg er blevet opdateret.
1. Angiv **10** i feltet **Pris** i oversigtspanelet *Køb*.
1. På oversigtspanelet **Administrer omkostninger** skal du i feltet **Varegruppe** angive *Lyd*.
1. Angiv **10** i feltet **Pris** i oversigtspanelet *Køb*.
1. I oversigtspanelet **Lager** skal du i feltet **Enhedsseriegruppe-id** angive *ea*.
1. Vælg **Gem**.

### <a name="create-a-location-directive"></a>Oprette en lokalitetsvejledning

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I den venstre rude skal du i feltet **Arbejdsordretype** vælge *Indkøbsordrer*.
1. Vælg den lokationsvejledning, der hedder *24 PO Direct*, på listen.
1. Gå til oversigtspanelet **Handlinger i lokationsvejledning** og vælg **Ny** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Løbenummer:** *1*

        Den nye linje skal være foran den tidligere eksisterende linje. Hvis du vil foretage ændringen, skal du bruge knapperne **Flyt op** og **Flyt ned** på værktøjslinjen eller ændre **Løbenummerværdi** til *2*.

    - **Navn:** *Læg på lager for MASSE-lokationsprofil*
    - **Anvendelse af fast lokation:** *Faste og ikke-faste lokationer*
    - **Tillad negativ lagerbeholdning:** *Fjern markeringen i dette afkrydsningsfelt (= Nej)*
    - **Batch aktiveret:** *Fjern markeringen i dette afkrydsningsfelt (= Nej)*
    - **Strategi:** *Ingen*

1. Mens den nye linje stadig er markeret, skal du vælge **Rediger forespørgsel** over gitteret.
1. Vælg forespørgselsdialogboksen skal du under fanen **Interval** vælge **Tilføj** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Tabel:** *Lokationer*
    - **Afledt tabel:** *Lokationer*
    - **Felt:** *Lokationsprofil-id*
    - **Kriterier:** *BULK*

1. Vælg **OK**.
1. Vælg **Gem** i handlingsruden på siden **Lokationsvejledninger**.

> [!NOTE]
> Hvis du i feltet **Strategi** i oversigtspanelet **Handlinger i lokationsvejledning** bruger lokationsstrategien *Konsolider*, vil opsætningen af oversigtspanelet **Tilladt blanding af produktdimensioner** på **Lokationsprofiler** blive tilsidesat, og varer lægges på lager på samme lokation, også selvom denne virkemåde ikke er tilladt af opsætningen.

### <a name="create-a-mobile-device-menu-item"></a>Oprette et menupunkt på en mobilenhed

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg **Ny** i handlingsruden for at oprette et menupunkt, der skal bruges til sortering.
1. Angiv følgende værdier i overskriften:

    - **Navn på menupunkt:** *Modtagelse af indkøbsordrelinje*
    - **Titel:** *Modtagelse af indkøbsordrelinje*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Nej*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Arbejdsoprettelsesproces:** *Modtagelse og læg på lager for ordrelinje*
    - **Generer nummerplade:** *Ja*

1. Vælg **Gem**.

### <a name="configure-the-mobile-device-menu"></a>Konfigurer mobilenhedsmenuen

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Vælg **Indgående** på listen over menuer.
1. Vælg **Rediger** i handlingsruden.
1. På listen **Tilgængelig menuer og menupunkter** skal du finde og vælge menupunktet **Modtagelse af indkøbsordrelinje**.
1. Vælg den højre pileknap for at flytte menupunktet **Modtagelse af indkøbsordrelinje** til listen **Menustruktur**. På denne måde føjer du det nye menupunkt til den valgte menu.
1. Vælg **Gem**.

## <a name="scenario"></a>Scenario

Dette demonstrationsscenarie viser, hvordan to forskellige produktvarianter kan anbringes på samme lokation, når lokationsprofilen ikke tillader blandede varer, men funktionen *Blanding af produktdimensioner på lokation* er aktiveret. I dette tilfælde skal du bruge varianten **Størrelse** som kriterium.

Før du går i gang, skal du sikre dig, at der er tomme lokationer på lagerstedet *24*, der bruger *MASSE*-lokationsprofilen.

### <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

Du skal oprette en indkøbsordre, der indeholder tre linjer: to linjer for samme produktnummer, men med forskellige varianter af **Størrelse**, og en tredje linje for et andet produkt, der ikke har nogen varianter.

1. Gå til **Kreditor \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret indkøbsordre**:

    - **Kreditorkonto:** *1001*
    - **Lagersted:** *24*

1. Vælg **OK**.
1. Indkøbsordren oprettes, og der tilføjes en ny linje i oversigtspanelet **Indkøbsordrelinjer**. Notér dig købsordrenummeret.
1. Angiv følgende værdier på den nye linje:

    - **Varenummer:** *B0001*
    - **Størrelse** *L*
    - **Antal:** *2*

1. Vælg **Tilføj linje** over gitteret for at tilføje en anden indkøbsordrelinje, og angiv følgende værdier:

    - **Varenummer:** *B0001*
    - **Størrelse** *XL*
    - **Antal:** *2*

1. Vælg **Tilføj linje** for at tilføje en tredje indkøbsordrelinje, og angiv følgende værdier:

    - **Varenummer:** *A0001*
    - **Antal:** *1*

1. Vælg **Gem**.

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a>Modtage indkøbsordrelinjer i lagerstedsappen

1. Log på lagerstedsappen som en bruger, der er aktiveret til lagersted *24*.
1. Vælg menuen **Indgående**.
1. Vælg **Modtagelse af indkøbsordrelinje**.
1. Vælg feltet **IO-num**, angiv derefter indkøbsordrenummeret.
1. Bekræft angivelsen ved at vælge knappen Bekræft (✔) nederst på siden.
1. Angiv linjenummeret fra den indkøbsordre, der modtages. Marker feltet **LINJENUM**, og brug derefter det numeriske tastatur til at angive *1*.
1. Bekræft indtastningen.
1. Angiv det antal, der skal modtages. Vælg knappen plustegn (**+**) to gange for at øge værdien i feltet **Antal** til *2*.
1. Registrer din indtastning ved at vælge knappen (✔) nederst på siden, og bekræft derefter angivelsen ved at vælge knappen (✔) igen.
1. Få vist oplysningerne på siden **Indkøbsordrer: Læg på lager**. Denne side viser det arbejde, der er oprettet for læg på lager-handlingen (arbejde 1).

    Den lokation, hvor den modtagne vare skal lægges på lager, nummerpladen, varen, størrelsen og antallet på den linje i opgaven **Modtagelse indkøbsordrelinje**, som modtager den opgave, du netop har udført, vises.

1. Bekræft læg på lager-arbejdet.
1. Gentag trin 4 til 11 for indkøbsordrelinje 2. I trin 8 skal du dog angive et antal på *1*.

    Der oprettes et nyt læg på lager-arbejde (arbejde 2) for samme lokation som arbejde 1.

1. Gentag trin 4 til 11 igen for indkøbsordrelinje 2. I trin 8 skal du angive et resterende antal på *1*.

    Der oprettes et nyt læg på lager-arbejde (arbejde 3) for samme lokation som arbejde 1 og 2. Dette virkemåde opstår, fordi lokationsvejledningen *Konsolider* bruges, og oversigtspanelet **Tilladt blanding af produktdimensioner** i *Masse*-opsætningen af **Lokationsprofiler** tillader, at varianten **Størrelse** kan blandes på en lokation.

1. Gentag trin 4 til 11 for indkøbsordrelinje 3. I trin 8 skal du angive et antal på *1* for varenummer *A0001*.

    Der oprettes et nyt læg på lager-arbejde (arbejde 4) for en anden lokation end den lokation, der bruges til indkøbsordrelinje nr. 1 og 2. Denne virkemåde opstår, fordi lokationsprofilen ikke tillader blandede produkter, men den giver mulighed for blandede dimensioner af samme produktmaster.

1. Vælg menuknappen øverst på siden (kaldes også hamburger eller hamburgerknappen), og vælg derefter **Annuller** for at afslutte **Modtagelse af indkøbsordrelinjer**.

> [!TIP]
> Du kan gentage dette scenarie, men denne gang skal du angive **Størrelse** - *Nej* under oversigtspanelet **Tillad blanding af produktdimensioner** på *Masse* **Lokationsprofiler**, så ingen af produktdimensionerne kan blandes. Hvis du i dette tilfælde modtager indkøbsordren, vil de enkelte produktvarianter blive lagt på lager på en ny lokation.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]