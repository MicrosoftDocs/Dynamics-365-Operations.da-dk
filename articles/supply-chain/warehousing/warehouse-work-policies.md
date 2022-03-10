---
title: Arbejdspolitikker
description: I dette emne forklares, hvordan du konfigurerer arbejdspolitikker.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1d4ee3f1bffaf00c20758f6a3f399451d3122291
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571155"
---
# <a name="work-policies"></a>Arbejdspolitikker

[!include [banner](../includes/banner.md)]

I dette emne forklares, hvordan du kan konfigurere systemet og mobilappen Lokationsstyring, så de understøtter arbejdspolitikker. Du kan bruge denne funktion til hurtigt at registrere lagerbeholdningen uden at oprette læg på lager-arbejde, når du modtager indkøbs- eller flytteordrer, eller når du fuldfører produktionsprocesser. Dette emne indeholder generelle oplysninger. Du kan finde detaljerede oplysninger, der er relateret til id-modtagelse, under [Modtagelse af id via mobilappen Lokationsstyring](warehousing-mobile-device-app-license-plate-receiving.md).

En arbejdspolitik styrer, om der oprettes lagerstedsarbejde, når en produceret vare færdigmeldes, eller når varer modtages ved hjælp af mobilappen Lokationsstyring. Du konfigurerer hver arbejdspolitik ved at definere de betingelser, der gælder: arbejdsordretyper og processer, lagerlokation og (valgfrit) produkter. En indkøbsordre på produkt *A0001* skal f.eks. modtages på lokation *RECV* på lagersted *24*. Senere forbruges produktet i en anden proces på lokation *RECV*. I dette tilfælde kan du konfigurere en arbejdspolitik for at forhindre, at læg på lager-arbejde oprettes, når en arbejder rapporterer, at produkt *A0001* er modtaget på lokation *RECV*.

> [!NOTE]
> - Hvis en arbejdspolitik skal være aktiv, skal du definere mindst én lokation for den i oversigtspanelet **Lagerlokationer** på siden **Arbejdspolitikker**. 
> - Du kan ikke angive den samme placering for flere arbejdspolitikker.
> - Indstillingen **Udskriv label** til mobilenhedens menupunkter udskriver ikke en id-label, medmindre arbejde er oprettet.

## <a name="activate-the-features-in-your-system"></a>Aktivere funktionerne i systemet

Hvis du vil gøre alle funktioner, der beskrives i dette emne, tilgængelige i systemet, skal du aktivere følgende to funktioner i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Forbedringer af modtagelse af id
- Forbedringer af arbejdspolitikker for indgående arbejde

## <a name="the-work-policies-page"></a>Siden arbejdspolitikker

Hvis du vil konfigurere arbejdspolitikker, skal du gå til **Lokationsstyring \> Konfiguration \> Arbejde \> Arbejdspolitikker**. Derefter skal du i hvert oversigtspanel angive felterne som beskrevet i følgende underafsnit.

### <a name="the-work-order-types-fasttab"></a>Oversigtspanelet Arbejdsordretyper

I oversigtspanelet **Arbejdsordretyper** skal du tilføje alle arbejdsordretyper og de relaterede arbejdsprocesser, som arbejdspolitikken gælder for. Følgende arbejdsordretyper og relaterede arbejdsprocesser understøttes for arbejdspolitikker.

| Arbejdsordretype | Arbejdsproces |
|---|---|
| Råvarepluk| Alle relaterede processer |
| Samprodukt og biprodukt, læg på lager | Alle relaterede processer |
| Færdige varer, læg på lager | Alle relaterede processer |
| Tilgang for overførsel | Modtagelse af id (og læg på lager) |
| Indkøbsordrer | <ul><li>Modtagelse af id (og læg på lager)</li><li>Modtagelse af varelast (og læg på lager)</li><li>Indkøbsordrelinje til modtagelse (og læg på lager)</li><li>Indkøbsordrevare til modtagelse (og læg på lager)</li></ul> |

Hvis du vil oprette en arbejdspolitik, så den gælder for flere arbejdsprocesser med samme arbejdsordretype, skal du føje en separat linje for hver arbejdsproces til gitteret.

For hver linje i gitteret skal du angive feltet **Metode til oprettelse af arbejde** til en af følgende værdier:

- **Aldrig** – Arbejdspolitikken forhindrer lagerstedsarbejde i at blive oprettet for den valgte arbejdsordretype og relaterede arbejdsproces.
- **Cross-docking** – Arbejdspolitikken opretter cross-docking-arbejde ved hjælp af den politik, du vælger i feltet **Navn på politik for cross-docking**.

### <a name="the-inventory-locations-fasttab"></a>Oversigtspanelet Lagerlokationer

Tilføj alle de lokationer, hvor denne arbejdspolitik skal anvendes, i oversigtspanelet **Lagerlokationer**. Hvis ingen lokation er knyttet til en arbejdspolitik, gælder arbejdspolitikken ikke for nogen proces.

Du kan ikke angive den samme placering for flere arbejdspolitikker.

Det er muligt at bruge en lagerlokation, der er tildelt en lokationsprofil, når **Brug nummerpladesporing** er slået fra. I dette tilfælde vil arbejderne direkte registrere den disponible lagerbeholdning.

### <a name="the-products-fasttab"></a>Oversigtspanelet Produkter

Under fanen **Produkter** skal du angive feltet **Produktvalg** for at styre, hvilke produkter politikken skal gælde for:

- **Alle** – Politikken skal gælde for alle produkter.
- **Valgte** – Politikken skal kun gælde for produkter, der er angivet i gitteret. Brug værktøjslinjen i oversigtspanelet **Produkter** til at føje produkter til gitteret eller fjerne dem fra gitteret.

## <a name="default-and-custom-to-locations"></a>Standard- og brugerdefinerede "til"-lokationer

> [!NOTE]
> Hvis du vil gøre den funktionalitet, der er beskrevet i dette afsnit, tilgængelig i systemet, skal du aktivere *Forbedringer af modtagelse af id* og *Forbedringer af arbejdspolitikken, for indgående arbejde* i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tidligere understøttede systemet kun modtagelse på den standardplacering, der er defineret for hvert lagersted. Men menupunkterne i mobilenheder, der bruger følgende processer til oprettelse af arbejdsopgaver, indeholder nu indstillingen **Brug standarddata**. Med denne indstilling kan du tildele en brugerdefineret "til"-lokation til et eller flere menupunkter. (Denne indstilling var allerede tilgængelig for andre typer menupunkter).

- Modtagelse af id (og læg på lager)
- Modtagelse af varelast (og læg på lager)
- Indkøbsordrelinje til modtagelse (og læg på lager)
- Indkøbsordrevare til modtagelse (og læg på lager)

Indstillingen **Til lokation** for et menupunkt tilsidesætter standardplaceringen for modtagelse på lagerstedet for alle ordrer, der behandles ved hjælp af dette menupunkt.

Hvis du vil konfigurere et menupunkt for mobilenheden til at understøtte modtagelse på en brugerdefineret lokation, skal du følge disse trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg eller opret et menupunkt, der bruger en af de processer til oprettelse af arbejde, der er angivet tidligere i dette afsnit.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Brug standarddata** til **Ja**.
1. Vælg **Standarddata** i handlingsruden.
1. På siden **Standarddata** kan du angive følgende værdier:

    - **Feltet Standarddata:** Indstil dette felt til *Til lokation*.
    - **Lagersted:** Vælg det destinationslagersted, der skal bruges til dette menupunkt.
    - **Lokation:** Dette felt viser alle de lokations-id'er, der er tilgængelige for det valgte lagersted. Indstillingen i dette felt har dog ikke nogen virkning. Du kan derfor lade feltet være tomt. Du kan dog bruge listen til at bekræfte det id, du skal angive i feltet **Hardcodet værdi**.
    - **Hardcodet værdi:** Angiv lokalitets-id'et for den modtagende lokation, der gælder for dette menupunkt.

> [!TIP]
> Der kan kun anvendes en arbejdspolitik, hvis alle de modtagende lokationer er angivet i den relevante opsætning af arbejdspolitik. Dette krav gælder, uanset om du bruger standardlokationen for modtagelse på lagersted eller en brugerdefineret "til"-lokation.

## <a name="example-scenario-warehouse-receiving"></a>Eksempelscenario: modtagelse på lagerstedet

Alle produkter, der modtages af processen *Indkøbsordrevare til modtagelse (og læg på lager)*, skal være registreret i lokation *FL-001*, og de skal være tilgængelige på lagersted *24*. Der skal dog ikke oprettes arbejde. Produkter, der modtages af enhver anden proces (dvs. ved hjælp af andre menupunkter i mobilenheder), skal registreres på standardlagerstedets modtagelseslokation (*RECV*), og der skal oprettes arbejde som normalt. (Dette scenarie viser ikke den standardopsætning af modtagelse).

Dette scenario kræver følgende elementer:

- En arbejdspolitik til processen *Indkøbsordrevare til modtagelse (og læg på lager)* i lokation *FL-001* for alle produkter
- Et menupunkt i mobilenheden, der indeholder standarddata, og som angiver feltet **Til lokation** til *FL-001*

### <a name="prerequisites"></a>Forudsætninger

Hvis du vil gøre den funktionalitet, der er beskrevet i dette scenarie, tilgængelig i systemet, skal du aktivere *Forbedringer af modtagelse af id* og *Forbedringer af arbejdspolitikken, for indgående arbejde* i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Dette scenarie bruger standarddemodata. Hvis du vil gennemgå scenariet ved hjælp af de værdier, der vises her, skal du arbejde på et system, hvor demodata er installeret. Derudover skal du vælge den juridiske enhed **USMF**.

### <a name="set-up-a-work-policy"></a>Konfigurere en arbejdspolitik

1. Gå til **Lokationsstyring \> Konfiguration \> Arbejde \> Arbejdspolitikker**.
1. Vælg **Ny**.
1. I feltet **Navn på arbejdspolitik** skal du angive *Intet læg på lager-arbejde for indkøbsvare*.
1. Vælg **Gem**.
1. Vælg **Tilføj** i oversigtspanelet **Arbejdsordretyper** for at føje en række til gitteret, og angiv derefter følgende værdier for den nye række:

    - **Arbejdsordretype:** *Indkøbsordrer*
    - **Arbejdsproces:** *Indkøbsordrevare til modtagelse (og læg på lager)*
    - **Metode til oprettelse af arbejde:** *Aldrig*
    - **Navn på politik for cross-docking:** Lad feltet være tomt.

1. Vælg **Tilføj** i oversigtspanelet **Lagerlokationer** for at føje en række til gitteret, og angiv derefter følgende værdier for den nye række:

    - **Lagersted:** *24*
    - **Lokation:** *FL-001*

1. I oversigtspanelet **Produkter** skal du angive feltet **Produktvalg** til *Alle*.
1. Vælg **Gem**.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Konfigurere et menupunkt for mobilenheden til ændring af modtagelseslokationen

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. I venstre rude skal du vælge det eksisterende menupunkt **Købsmodtagelse**.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Brug standarddata** til *Ja*.
1. Vælg **Gem**.
1. Vælg **Standarddata** i handlingsruden.
1. Vælg **Ny** i handlingsruden på siden **Standarddata** for at føje en række til gitteret, og angiv derefter følgende værdier for den nye række:

    - **Standarddatafelt:** *Til lokation*
    - **Lagersted:** *24*
    - **Lokation:** Lad feltet være tomt.
    - **Hardcodet værdi:** *FL-001*

1. Vælg **Gem**.

### <a name="receive-a-purchase-order-without-creating-work"></a>Modtage en indkøbsordre uden at oprette arbejde

I eksemplet i dette afsnit vises, hvordan du modtager en indkøbsordrevare, men uden at oprette arbejde, på en lokation, der er forskellig fra standardlokationen for modtagelse på lagerstedet. I dette eksempel bruges den arbejdspolitik og det mobilenhedselement, du har oprettet tidligere i dette scenario.

#### <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret indkøbsordre**:

    - **Kreditorkonto:** *US-101*
    - **Lokation:** *2*
    - **Lagersted:** *24*

1. Vælg **OK** for at åbne den nye indkøbsordre og lukke dialogboksen.
1. I oversigtspanelet **Indkøbsordrelinjer** skal du angive følgende værdier for den tomme række:

    - **Varenummer:** *A0001*
    - **Antal:** *1*

1. Vælg **Gem**.
1. Notér dig købsordrenummeret.

#### <a name="receive-a-purchase-order"></a>Modtage en indkøbsordre

1. På mobilenheden skal du logge på lagersted *24* ved hjælp *24* som bruger-id og *1* som adgangskode.
1. Vælg **Indgående**.
1. Vælg **Købsmodtagelse**. Feltet **Lokation** skal indstilles til *FL-001*.
1. Angiv indkøbsordrenummeret for den indkøbsordre, du oprettede i den foregående procedure.
1. Indtast **A0001** i feltet *Varenummer*.
1. Vælg **OK**.
1. Angiv **1** i feltet *Antal*.
1. Vælg **OK**.

Indkøbsordren er nu modtaget, men der er ikke knyttet noget arbejde til den. Den disponible lagerbeholdning er opdateret, og et antal på *1* af vare *A0001* er nu tilgængeligt på lokationen *FL-001*.

## <a name="example-scenario-manufacturing"></a>Eksempelscenario: produktion

I følgende eksempel er der to produktionsordrer, *PRD-001* og *PRD-002*. Produktionsordre *PRD-001* er en handling, der hedder *Samling*, hvor produktet *SC1* færdigmeldes på lokation *001*. Produktionsordre *PRD-002* er en handling, der hedder *Maling* og forbruger produkt *SC1* fra lokation *001*. Produktionsordren *PRD-002* forbruger også råvare *RM1* fra lokation *001*. Råvare *RM1* opbevares på lagerlokation *BULK-001* og vil blive plukket til lokation *001* af lagerstedets arbejde til råvareplukning. Plukkearbejdet genereres, når produktionen *PRD-002* frigives.

[![Politikker for lagerstedsarbejde.](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Når du skal konfigurere lagerstedets arbejdspolitik for dette scenario, skal du overveje følgende oplysninger:

- Lagerstedets arbejde for færdigvarer, der skal lægges på lager, er ikke påkrævet, når du færdigmelder produkt *SC1* fra produktionsordre *PRD-001* til lokation *001*. Dette skyldes, at *Maling*-handlingen for produktionsordre *PRD-002* forbruger produkt *SC1* på samme lokation.
- Lagerstedsarbejde til plukning af råvarer kræves for at flytte råvare *RM1* fra lagerlokation *BULK-001* til lokation *001*.

Her er et eksempel på en politik for arbejde, du har angivet, ud fra disse overvejelser:

- **Navn på arbejdspolitik:** *Intet læg på lager-arbejde*
- **Arbejdsordretyper:** *Færdige varer, læg på lager*, og *Samprodukt og biprodukt, læg på lager*
- **Lagerlokationer:** Lagersted *51* og lokation *001*
- **Produkter:** *SC1*

Følgende eksempelscenario indeholder trinvise instruktioner i, hvordan du konfigurerer arbejdspolitikken for lagersted i dette scenario.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Eksempelscenario: Færdigmelde til en lokation, der ikke er id-kontrolleret

Dette scenarie viser et eksempel på, hvor en produktionsordre færdigmeldes til en lokation, der ikke er id-kontrolleret.

Dette scenarie bruger standarddemodata. Hvis du vil gennemgå scenariet ved hjælp af de værdier, der vises her, skal du arbejde på et system, hvor demodata er installeret. Derudover skal du vælge den juridiske enhed **USMF**.

### <a name="set-up-a-warehouse-work-policy"></a>Konfigurere en arbejdspolitik for lagersted

Lagerstedsprocesser omfatter ikke altid lagerstedsarbejde. Ved at definere en arbejdspolitik kan du forhindre oprettelse af arbejde med pluk af råmaterialer og læg færdigvarer på lager for en række produkter på bestemte lokationer.

1. Gå til **Lokationsstyring \> Konfiguration \> Arbejde \> Arbejdspolitikker**.
1. Vælg **Ny**.
1. I feltet **Navn på arbejdspolitik** skal du angive *Intet læg på lager-arbejde*.
1. Vælg **Gem** i handlingsruden.
1. Vælg **Tilføj** i oversigtspanelet **Arbejdsordretyper** for at føje en række til gitteret, og angiv derefter følgende værdier for den nye række:

    - **Arbejdsordretype:** *Færdige varer, læg på lager*
    - **Arbejdsproces:** *Alle relaterede arbejdsprocesser*
    - **Metode til oprettelse af arbejde:** *Aldrig*
    - **Navn på politik for cross-docking:** Lad feltet være tomt.

1. Vælg **Tilføj** for at tilføje endnu en række i gitteret, og angiv derefter følgende værdier for den nye række:

    - **Arbejdsordretype:** *Samprodukt og biprodukt, læg på lager*
    - **Arbejdsproces:** *Alle relaterede arbejdsprocesser*
    - **Metode til oprettelse af arbejde:** *Aldrig*
    - **Navn på politik for cross-docking:** Lad feltet være tomt.

1. Vælg **Tilføj** i oversigtspanelet **Lagerlokationer** for at føje en række til gitteret, og angiv derefter følgende værdier for den nye række:

    - **Lagersted:** *51*
    - **Lokation:** *001*

1. I oversigtspanelet **Produkter** skal du angive feltet **Produktvalg** til *Valgte*.
1. I oversigtspanelet **Produkter** skal du vælge **Tilføj** for at føje en række til gitteret.
1. Angiv feltet **Varenummer** til *L0101* i den nye række.
1. Vælg **Gem** i handlingsruden.

### <a name="set-up-an-output-location"></a>Konfigurere en outputlokation

1. Gå til **Virksomhedsadministration \> Ressourcer \> Ressourcegrupper**.
1. Vælg ressourcegruppen **5102** i venstre rude.
1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Lagersted for udlagring:** *51*
    - **Udlagringslokation:** *001*

1. Vælg **Gem** i handlingsruden.

> [!NOTE]
> Lokationen *001* er ikke en id-kontrolleret lokation. Du kan kun konfigurere en udlagringslokation uden id-kontrol, hvis der findes en gyldig arbejdspolitik for lokationen.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Oprette en produktionsordre og rapportere den som færdig

1. Gå til **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer**.
1. Vælg **Ny produktionsordre** i handlingsruden.
1. Angiv feltet **Varenummer** til **L0101** i dialogboksen *Opret produktionsordre*.
1. Vælg **Opret** for at oprette ordren og lukke dialogboksen.

    En ny produktionsordre føjes til gitteret på siden **Alle produktionsordrer**.

    Lad den nye produktionsordre forblive valgt.

1. I handlingsruden under fanen **Produktionsordre** skal du i gruppen **Proces** vælge **Estimer**.
1. Læs estimatet i dialogboksen **Estimat**, og vælg derefter **OK** for at lukke dialogboksen.
1. I handlingsruden under fanen **Produktionsordre** skal du i gruppen **Proces** vælge **Start**.
1. I dialogboksen **Start** skal du under fanen **Generelt** angive feltet **Automatisk styklisteforbrug** til *Aldrig*.
1. Vælg **OK** for at gemme indstillingen og lukke dialogboksen.
1. I handlingsruden under fanen **Produktionsordre** skal du i gruppen **Proces** vælge **Færdigmeld**.
1. I dialogboksen **Færdigmeld** under fanen **Generelt** skal du angive indstillingen **Accepter fejl** til *Ja*.
1. Vælg **OK** for at gemme indstillingen og lukke dialogboksen.
1. Vælg **Arbejdsdetaljer** i gruppen **Generelt** under fanen **Lagersted** i handlingsruden.

Når produktionsordren er færdigmeldt, oprettes der intet arbejde for læg på lager. Dette skyldes, at der er defineret en arbejdspolitik, som forhindrer, at der genereres arbejde, når produktet *L0101* færdigmeldes på lokation *001*.

## <a name="more-information"></a>Flere oplysninger

Du kan få flere oplysninger om menupunkter på mobilenheder, i [Konfigurere mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md).

Du kan finde flere oplysninger om id-modtagelse og arbejdspolitikker under [Modtagelse af id via mobilappen Lokationsstyring](warehousing-mobile-device-app-license-plate-receiving.md).

Du finder flere oplysninger om indgående laststyring i [Lagerstedshåndtering af indgående laster til indkøbsordrer](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]