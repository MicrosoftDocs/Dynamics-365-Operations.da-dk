---
title: Gennemgang af funktioner for styring af tekniske ændringer
description: Dette emne indeholder en total gennemgang, der viser, hvordan du kan arbejde med styring af tekniske ændringer.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 91b19598075871dcfaed3ad9978aa8fe8181aa6f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836656"
---
# <a name="engineering-change-management-feature-walkthrough"></a>Gennemgang af funktioner for styring af tekniske ændringer

[!include [banner](../includes/banner.md)]

Dette emne indeholder en total gennemgang, der viser, hvordan du kan arbejde med styring af tekniske ændringer. Det gennemgår hvert af de vigtigste scenarier:

- Grundlæggende konfiguration af funktioner
- Sådan opretter et teknisk firma et nyt teknisk produkt
- Sådan frigiver et teknisk firma et teknisk produkt til et lokalt firma
- Sådan kan en lokal virksomhed gennemgå og acceptere et produkt, der er frigivet til det af et teknisk firma
- Sådan kan en lokal virksomhed bruge et teknisk produkt i standardtransaktioner
- Sådan føjer du et teknisk produkt til en salgsordre
- Sådan anmoder du om ændringer af et teknisk produkt ved at oprette en anmodning om teknisk ændring
- Sådan planlægger og implementerer du de ønskede ændringer ved at oprette en teknisk ændringsordre
- Sådan frigiver du et produkt, der er ændret

Alle øvelserne i dette emne bruger standardeksempeldataene, der er leveret til Microsoft Dynamics 365 Supply Chain Management. Desuden bygger hver øvelse på den forrige øvelse. Vi anbefaler derfor, at du arbejder gennem øvelserne i rækkefølge fra start til slut, især hvis du aldrig har brugt funktionen til teknisk ændringsstyring før. På denne måde får du en komplet forståelse af funktionen.

## <a name="set-up-for-the-sample-scenario"></a>Konfigurere eksempelscenariet

Hvis du vil følge eksempelscenariet i dette emne, skal du først forberede funktionen ved at gøre demodata tilgængelige og tilføje nogle få brugerdefinerede poster.

Før du forsøger at udføre øvelserne i resten af dette emne, skal du følge instruktionerne i alle følgende underafsnit. Disse underafsnit introducerer også flere vigtige indstillingssider, som du kan bruge, når du konfigurerer styring af tekniske ændringer for din egen organisation.

### <a name="make-standard-demo-data-available"></a>Gøre standarddemodata tilgængelige

Arbejde på et system, hvor [standarddemodataene er installeret](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Standarddemodataene tilføjer data for flere juridiske enheder i demoen (firmaer og organisationer). Efterhånden som du arbejder dig gennem øvelserne, skal du bruge firmavælgeren til højre på navigationslinjen til at skifte mellem et firma (*DEMF*), der er konfigureret som en *teknisk organisation*, og et andet firma (*USMF*), der er konfigureret som en *driftsorganisation*.

### <a name="set-up-an-engineering-organization"></a>Konfigurere en teknisk organisation

En teknisk organisation ejer de tekniske data og er ansvarlig for produktdesign og produktændringer. Benyt følgende fremgangsmåde for at konfigurere dine tekniske organisationer.

1. Gå til **Teknisk ændringsstyring &gt; Konfiguration &gt; Tekniske organisationer**.
1. Vælg **Ny** for at tilføje en række i gitteret, og angiv derefter følgende værdier for den:

    - **Teknisk organisation:** *DEMF*
    - **Organisationsnavn:** *Contoso Entertainment System Germany*

    ![Tilføje en teknisk organisation](media/engineering-org.png "Tilføje en teknisk organisation")

### <a name="set-up-the-version-product-dimension-group"></a>Konfigurere dimensionsgruppen for versionsprodukt

1. Gå til **Administration af produktoplysninger &gt; Konfiguration &gt; Dimensioner og variantgrupper &gt; Produktdimensionsgrupper**.
1. Vælg **Ny** for at oprette en produktdimensionsgruppe.
1. Angiv feltet **Navn** til *Version*.
1. Vælg **Gem** for at gemme de nye dimensions- og lastværdier i oversigtspanelet **Produktdimensioner**.
1. I oversigtspanelet **Produktdimensioner** skal du angive **Version** som en aktiv produktdimension.

    ![Tilføje en produktdimensionsgruppe](media/product-dimension-groups.png "Tilføje en produktdimensionsgruppe")

### <a name="set-up-product-lifecycle-states"></a>Konfigurere produktlivscyklusser

Når et teknisk produkt går gennem dets livscyklus, er det vigtigt, at du kan styre, hvilke transaktioner der er tilladt for hver enkelt livscyklustilstand. Benyt følgende fremgangsmåde for at konfigurere produktlivscyklusser.

1. Gå til **Teknisk ændringsstyring &gt; Konfiguration &gt; Tilstand for produktlivscyklus**.
1. Vælg **Ny** for at tilføje en livscyklustilstand, og angiv derefter følgende værdier for den:

    - **Tilstand:** *Operationel*
    - **Beskrivelse:** *Operationel*

1. Vælg **Gem** for at gemme den nye livscyklustilstand og lastværdier i oversigtspanelet **Aktiverede forretningsprocesser**.
1. Vælg de forretningsprocesser, der skal være tilgængelige, i oversigtspanelet **Aktiverede forretningsprocesser**. I dette eksempel skal du lade **Politik**-feltet være angivet til *Aktiveret* for alle forretningsprocesser.

    ![Aktivere forretningsprocesser for en livscyklustilstand](media/product-lifecycle-states-1.png "Aktivere forretningsprocesser for en livscyklustilstand")

1. Vælg **Ny** for at tilføje en ny livscyklustilstand, og angiv derefter følgende værdier for den:

    - **Tilstand:** *Prototype*
    - **Beskrivelse:** *prototype*

1. Vælg **Gem** for at gemme den nye livscyklustilstand og lastværdier i oversigtspanelet **Aktiverede forretningsprocesser**.
1. Vælg de forretningsprocesser, der skal være tilgængelige, i oversigtspanelet **Aktiverede forretningsprocesser**. I dette eksempel skal du angive **Politik**-feltet til *Aktiveret med advarsel* for alle forretningsprocesser.

    ![Aktivere (med advarsler) forretningsprocesser for en livscyklustilstand](media/product-lifecycle-states-2.png "Aktivere (med advarsler) forretningsprocesser for en livscyklustilstand")

### <a name="set-up-a-version-number-rule"></a>Oprette en regel for versionsnummer

1. Gå til **Teknisk ændringsstyring &gt; Konfiguration &gt; Versionsnummerregel for produkt**.
1. Vælg **Ny** for at tilføje en regel, og angiv derefter følgende værdier for den:

    - **Navn:** *Automatisk*
    - **Nummerregel:** *Automatisk*
    - **Format:** *V-\#\#*

    ![Tilføje en versionsnummerregel for et produkt](media/version-number-rule.png "Tilføje en versionsnummerregel for et produkt")

### <a name="set-up-a-product-release-policy"></a>Konfigurere en produktfrigivelsespolitik

1. Gå til **Teknisk ændringsstyring &gt; Konfiguration &gt; Produktfrigivelsespolitikker**.
1. Vælg **Ny** for at tilføje en frigivelsespolitik, og angiv derefter følgende værdier for den:

    - **Navn:** *Komponenter*
    - **Beskrivelse:** *Komponenter*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Produkttype:** *Vare*
    - **Anvend skabeloner:** *Altid*
    - **Aktiv:** *Ja*

1. I oversigtspanelet **Alle produkter** skal du vælge **Tilføj** for at tilføje en linje, og indstil derefter følgende værdier for den:

    - **Firma:** *DEMF*
    - **Frigivet skabelonprodukt:** *D0006*

1. Vælg **Tilføj** for at tilføje en ny linje, og angiv følgende værdier for den:

    - **Regnskabs-id:** *USMF*
    - **Frigivet skabelonprodukt:** *D0006*
    - **Modtag stykliste:** Markér dette afkrydsningsfelt.
    - **Kopiér godkendelse af stykliste:** Markér dette afkrydsningsfelt.
    - **Kopiér aktivering af stykliste:** Markér dette afkrydsningsfelt.
    - **Modtag rute:** Markér dette afkrydsningsfelt.
    - **Kopiér rutegodkendelse:** Markér dette afkrydsningsfelt.
    - **Kopiér ruteaktivering:** Markér dette afkrydsningsfelt.

    ![Tilføje en produktfrigivelsespolitik](media/product-release-policy.png "Tilføje en produktfrigivelsespolitik")

### <a name="set-up-an-engineering-product-category"></a>Konfigurere en teknisk produktkategori 

Tekniske produktkategorier udgør grundlaget for oprettelse af tekniske produkter (dvs. produkter, der er versionsstyret og kontrolleret via styring af tekniske ændringer). Benyt følgende fremgangsmåde for at konfigurere tekniske produktkategorier.

1. Gå til **Teknisk ændringsstyring &gt; Detaljer om teknisk produktkategori**.
1. Vælg **Ny** for at oprette en ny kategori.
1. I oversigtspanelet **Detaljer** skal du angive følgende værdier:

    - **Navn:** *Komponenter*
    - **Teknisk organisation:** *DEMF*
    - **Produkttype:** *Vare*
    - **Spor version i transaktioner:** *Ja*
    - **Produktdimensionsgruppe:** *Version*
    - **Produktets livscyklustilstand ved oprettelse:** *Operationel*
    - **Versionsnummerregel:** *Automatisk*
    - **Gennemtving gyldighed:** *Nej*
    - **Brug nummerregelnomenklatur:** *Nej*
    - **Brug navneregelnomenklatur:** *Nej*
    - **Brug regelnomenklatur for beskrivelse:** *Nej*

1. I oversigtspanelet **Frigivelsespolitik** skal du angive feltet **Produktfrigivelsespolitik** til *Komponenter*.
1. Vælg **Gem**.

    ![Tilføje en teknisk produktkategori](media/product-category-details.png "Tilføje en teknisk produktkategori")

### <a name="set-up-product-acceptance-conditions"></a>Konfigurere betingelser for accept af produkt

1. Brug firmavælgeren i højre side af navigationslinjen til at skifte til den juridiske enhed (firma) *USMF*.
1. Gå til **Teknisk ændringsstyring &gt; Konfiguration &gt; Parametre for styring af tekniske ændringer**.
1. Under fanen **Frigivelseskontrol** skal du i sektionen **Accept af produkt** angive, feltet **Accept af produkt** til *Manuel*.

    ![Konfigurere betingelser for accept af produkt](media/engineering-change-management-parameters.png "Konfigurere betingelser for accept af produkt")

## <a name="create-a-new-engineering-product"></a>Oprette et nyt teknisk produkt

Et teknisk produkt er et produkt, der versionsnummereret og kontrolleret via styring af tekniske ændringer. Du kan med andre ord styre ændringerne under dets levetid, og ændringsoplysningerne vil blive gemt ved hjælp af tekniske ændringsordrer. Følg disse trin for at oprette tekniske produkter.

1. Sørg for, at du befinder dig i den juridiske enhed for din tekniske organisation (*DEMF* i dette eksempel). Brug firmavælgeren i højre side af navigationslinjen som ønsket.
1. Åbn siden **Frigivne produkter** ved at følge en af disse fremgangsmåder:

    - Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.
    - Gå til **Teknisk ændringsstyring &gt; Fælles &gt; Frigivne produkter**.

1. Vælg **Teknisk produkt** i gruppen **Nyt** under fanen **Produkt** i handlingsruden.
1. Angiv følgende værdier i dialogboksen **Nyt produkt**:

    - **Teknisk produktkategori:** *Komponenter*
    - **Produktnummer:** *Z0001*
    - **Produktnavn:** *Højttalersæt*

    ![Tilføje et teknisk produkt](media/new-product-dialog.png "Tilføje et teknisk produkt")

    Bemærk, at **Version**-feltet automatisk angives ved hjælp af den regel for produktversionsnummer, som du oprettede tidligere.

1. Vælg **OK** for at oprette produktet og lukke dialogboksen.
1. Siden med detaljer for det nye produkt åbnes. Bemærk, at værdier allerede er udfyldt for nogle felter, f.eks. **Lagringsdimensionsgruppe**, **Sporingsdimensionsgruppe** og/eller **Varemodelgruppe**. Disse felter blev automatisk angivet, fordi produktet frigives i den juridiske enhed *DEMF* og bruger *Komponenter* som produktfrigivelsespolitik, der er knyttet til den tekniske produktkategori *Komponenter*. Da du tidligere brugte vare *D0006* som skabelon til oprettelse af en linje til den juridiske enhed *DEMF*, blev de værdier, der blev udfyldt, hentet fra vare *D0006*.

    ![Frigivne produktdetaljer](media/product-details.png "Frigivne produktdetaljer")

1. Vælg **Tekniske versioner** i gruppen **Teknisk ændringsstyring** i handlingsruden under fanen **Tekniker** for at få vist versionerne af produktet.

    ![Tekniske versioner](media/engineering-versions-list.png "Tekniske versioner")

1. Læg mærke til, at der kun er én version til produktet på siden **Tekniske versioner**, og at den er aktiv.
1. Vælg versionen for at få vist detaljerne.

    ![Oplysninger om teknisk version](media/engineering-version-details.png "Oplysninger om teknisk version")

1. Vælg **Opret stykliste** i oversigtspanelet **Stykliste** på siden **Teknisk version**.
1. I dialogboksen **Opret stykliste** skal du angive følgende værdier:

    - **Styklistenummer:** Z0001
    - **Navn:** Højttalersæt
    - **Lokation:** 1

    ![Oprettelse af en BOM](media/create-bom.png "Oprettelse af en BOM")

1. Vælg **OK** for at tilføje styklisten og lukke dialogboksen.
1. Vælg **Stykliste** i oversigtspanelet **Stykliste**.
1. På siden **Styklister** i oversigtspanelet **Styklistelinjer** kan du tilføje tre linjer – én hver for varenummer *D0001*, *D0003* og *D0006*.

    ![Tilføje styklistelinjer](media/bom.png "Tilføje styklistelinjer")

1. Vælg **Gem**.
1. Luk siden.
1. Vælg **Godkend** i oversigtspanelet **Stykliste** på siden **Teknisk version**.
1. Vælg **OK** i dialogboksen, der vises.

    ![Godkende styklisten](media/approve-dialog.png "Godkende styklisten")

1. Vælg **Aktivér** i oversigtspanelet **Stykliste** på siden **Teknisk version**.
1. Bemærk, at afkrydsningsfelterne **Aktiv** og **Godkendt** er markeret for styklisten.

    ![Aktiv og godkendt stykliste](media/approved-bom.png "Aktiv og godkendt stykliste")

1. Luk siden.

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>Frigive et teknisk produkt til et lokalt firma

Produktet er nu designet af den tekniske afdeling. I dette eksempel er produktet en prototype, som teknikeren har designet til en kunde. Da kunden er kunde i den juridiske enhed *USMF*, skal produktet frigives til den juridiske enhed.

1. Bevar den juridiske enhed angivet til *DEMF*. (Brug firmavælgeren i højre side af navigationslinjen som ønsket).
1. Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.
1. Vælg produkt *Z0001*.
1. Vælg **Frigiv produktstruktur** i gruppen **Vedligehold** under fanen **Produkt** i handlingsruden for at åbne guiden **Frigiv produkter**.
1. Markér afkrydsningsfeltet **Vælg** for produkt **Z0001** på siden *Vælg tekniske produkter, der skal frigives*.

    ![Vælge de tekniske produkter, der skal frigives](media/select-eng-product-to-release.png "Vælge de tekniske produkter, der skal frigives")

1. Vælg **Frigiv detaljer**.
1. Siden **Detaljer om produktfrigivelse** vises, hvor du kan gennemse detaljerne om det produkt, der skal frigives, og dets produktstruktur. Bemærk, at indstillingen **Send stykliste** er indstillet til *Ja*. Derfor vil både produkt *Z0001* og alle dets underordnede varer blive frigivet fra styklisten.

    Du kan vælge enhver underordnet vare i venstre rude for at gennemse oplysningerne. Hvis en underordnet vare har en stykliste, kan du også vælge at frigive styklisten for den pågældende underordnede vare.

    ![Gennemse oplysninger om produktfrigivelse](media/product-release-details.png "Gennemse oplysninger om produktfrigivelse")

1. Luk siden for at vende tilbage til guiden **Frigiv produkter**.
1. Vælg **Næste** for at åbne siden **Vælg produkter, der skal frigives**. Hvis du har valgt standardprodukter (der ikke er tekniske), vil de blive vist på denne side. Bemærk, at når du frigiver et standardprodukt ved at vælge **Frigiv produktstruktur**, frigives stykliste og rute også.

    ![Vælge standardprodukter, der skal frigives](media/select-std-product-to-release.png "Vælge standardprodukter, der skal frigives")

1. Vælg **Næste** for at åbne siden **Vælg produktvarianter, der skal frigives**. I dette eksempel er der ikke nogen varianter.
1. Vælg **Næste** for at åbne siden **Vælg firmaer**.
1. Vælg de firmaer, som produktet skal frigives til. I dette eksempel skal du markere afkrydsningsfeltet **USMF**.

    ![Vælge firmaer, der skal frigives til](media/select-release-companies.png "Vælge firmaer, der skal frigives til")

1. Vælg **Næste** for at åbne siden **Bekræft valg**.
1. Vælg **Udfør**.

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>Gennemse og acceptere produktet, før du frigiver det i det lokale firma

Den tekniske afdeling har nu frigivet oplysningerne til de lokale virksomheder, hvor produktet vil blive brugt. I dette eksempel er det lokale firma *USMF*.

Da du har angivet feltet **Accept af produkt** til *Manuel* på siden **Parametre for teknisk ændringsstyring** for *USMF*-firmaet, skal produkterne accepteres manuelt, før de frigives til det pågældende firma. De skal med andre ord gennemses og accepteres, før de bliver til frigivne produkter.

Udfør følgende trin for at gennemse produktet og frigive det i firmaet *USMF*.

1. Angiv den juridiske enhed til *USMF*. (Brug firmavælgeren i højre side af navigationslinjen).
1. Gå til **Teknisk ændringsstyring &gt; Fælles &gt; Produktfrigivelser &gt; Åbn produktfrigivelser**.

    På siden **Åbn produktfrigivelser** vises produkt *Z0001*, som har status af *Afventer accept*.

    ![Åbn produktfrigivelser](media/open-product-releases.png "Åbn produktfrigivelser")

1. Vælg værdien i kolonnen **Produktnummer** for at åbne siden **Detaljer om produktfrigivelse**. Bemærk følgende oplysninger:

    - I oversigtspanelet **Generelt** vises oplysninger om produktfrigivelsen, f.eks. frigivelsesfirmaet (*DEMF* for dette eksempel), frigivelsesstedet (*1*) og den modtagerstedet (*1*). Da du ikke har angivet et modtagersted i guiden **Frigiv produkter**, kopieres værdien af frigivelsesstedet til modtagerstedet.
    - Oversigtspanelet **Frigivelsesdetaljer** indeholder oplysninger om produktet og den version, der er frigivet. Her kan du redigere indstillinger, f.eks. gyldighedsdatoer.
    - Oversigtspanelet **Rute** viser produktets rute. I dette eksempel har du dog ikke frigivet nogen ruter.

    ![Detaljer om produktfrigivelse](media/product-release-details-2.png "Detaljer om produktfrigivelse")

1. Når du er færdig med at gennemse oplysningerne, er du klar til at acceptere produktet og på denne måde frigive det i *USMF*-firmaet. Vælg **Handlinger &gt; Acceptér** i handlingsruden.
1. Produktet er nu frigivet i *USMF*-firmaet. Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Du kan se vare *Z0001*.

## <a name="use-the-product-in-transactions-in-the-local-company"></a>Bruge produktet i transaktioner i det lokale firma

Masterdatastyringen for *USMF*-firmaet vil sikre, at produktet er i en *Prototype*-tilstand for at sikre, at brugerne bliver advaret, hvis de ved et uheld kommer til at tilføje dem i processer, de arbejder på.

1. Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.
1. Vælg produkt *Z0001* for at åbne siden med dets detaljer. (Du kan bruge filteret til at finde produktet).
1. Vælg **Tekniske versioner** i gruppen **Teknisk ændringsstyring** i handlingsruden under fanen **Tekniker**.
1. På siden **Tekniske versioner** skal du vælge versionsnummer *V-01* for at åbne siden med detaljer.
1. Vælg **Skift livscyklustilstand** i gruppen **Livscyklustilstand** under fanen **Produkt** i handlingsruden.
1. Angiv feltet **Tilstand** til **Prototype** på dialogboksrullelisten *Skift livscyklustilstand*, og vælg derefter **OK**.

    ![Ændre livscyklustilstand](media/change-lifecycle-state.png "Ændre livscyklustilstand")

## <a name="add-the-engineering-product-to-a-sales-order"></a>Tilføje det tekniske produkt i en salgsordre

Produktet kan nu sælges til en kunde. Hvis du vil tilføje produktet i en salgsordre, skal du følge disse trin.

1. Gå til **Salg og marketing &gt; Salgsordrer &gt; Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I dialogboksen **Opret salgsordre** skal du angive **US-0002** i feltet *Debitorkonto* og vælge **OK**.
1. Den nye indkøbsordre åbnes. Tilføj en række i oversigtspanelet **Salgsordrelinjer**, og angiv feltet **Varenummer** til *Z000* for den.
1. Vælg **Gem** i handlingsruden.

    Du får vist en advarselsmeddelelse om, at varen har status af *Prototype*. Men da meddelelsen kun er en advarsel, er salgsordren stadig oprettet.

    ![Det tekniske produkts salgsordre](media/sales-order-eng-product.png "Det tekniske produkts salgsordre")

## <a name="request-changes-in-the-engineering-product"></a>Anmode om ændringer i det tekniske produkt

Produktet er sendt til en kunde, men kunden er ikke helt tilfreds og giver feedback, der indeholder forslag til forbedring. Mens kunden taler med en salgsmedarbejder på telefonen, kan salgsassistenten anmode om de ændringer, som kunden beskriver.

1. Gå til **Salg og marketing &gt; Salgsordrer &gt; Alle salgsordrer**.
1. Find og åbn den salgsordre, du oprettede i den forrige øvelse.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Teknisk ændringsstyring &gt; Ny teknisk ændringsanmodning**.

    ![Oprette en anmodning om en teknisk ændring fra en salgsordre](media/sales-order-eng-change-request.png "Oprette en anmodning om en teknisk ændring fra en salgsordre")

1. Udfyld anmodningen om teknisk ændring på baggrund af kundens feedback. Angiv følgende værdier for dette eksempel:

    - **Ændringsanmodning:** *555*
    - **Titel:** *Z0001-kundeændring*
    - **Prioritet:** *lav*
    - **Kategori:** Angiv ændring
    - **Alvorsgrad:** *Mellem*

1. I oversigtspanelet **Oplysninger** skal du vælge **Ny &gt; Note** for at føje en note til gitteret.
1. I feltet **Beskrivelse** for den nye note skal du angive, at varen *D0003* skal slettes fra styklisten. Hvis du skal tilføje flere oplysninger for noten, kan du skrive tekst i feltet **Noter**.

    ![Teknisk ændringsanmodning](media/eng-change-request.png "Teknisk ændringsanmodning")

1. Vælg **Gem** i handlingsruden.
1. Bemærk, at varen automatisk er tilføjet i oversigtspanelet **Produkter**, og at kilden til anmodningen om teknisk ændring (salgsordren) er blevet tilføjet i oversigtspanelet **Kilde**.

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>Foretage ændringer af produktet ved at bruge en teknisk ændringsordre

Salgsassistenten ved, at produktet er vigtigt og er udviklet specielt til kunden. Derfor tilkalder salgsassistenten en tekniker i *DEMF*-firmaet for at give besked om ændringsanmodningen. På denne måde kan teknikeren gøre processen hurtigere.

Teknikeren gennemgår nu anmodningen fra kunden og opretter en ændringsordre for produktet.

1. Da teknikeren arbejder i *DEMF*-firmaet, skal du angive den juridiske enhed til *DEMF*. (Brug firmavælgeren i højre side af navigationslinjen).
1. Gå til **Teknisk ændringsstyring &gt; Fælles &gt; Tekniske ændringsanmodninger**.
1. Åbn ændringsanmodning *555*.
1. Gennemgå oplysningerne, og godkend derefter ændringen. Vælg **Godkend** i gruppen **Skift status** under fanen **Ændringsanmodning** i handlingsruden.
1. Gå til **Teknisk ændringsstyring &gt; Fælles &gt; Tekniske ændringsordrer**.
1. Vælg **Ny** i handlingsruden for at oprette en ændringsordre, og angiv følgende værdier for den:

    - **Ændringsordre:** *555*
    - **Titel:** *Z0001-kundeændring*
    - **Kategori:** *Kundeændring*
    - **Prioritet:** *Lav*
    - **Alvorsgrad:** *Mellem*

1. I oversigtspanelet **Berørte produkter** skal du vælge **Nyt &gt; Tilføj eksisterende produkt** for at føje en række til gitteret, og angiv derefter følgende værdier for den:

    - **Produkt:** *Z0001*
    - **Virkning:** *Ny version*

    ![Oprette en teknisk ændringsordre](media/eng-change-order.png "Oprette en teknisk ændringsordre")

1. Bemærk, at fordi du angiver feltet **Virkning** til *Ny version*, vises feltet **Ny version** under fanen **Detaljer** i oversigtspanelet **Produktdetaljer**, hvad det nye versionsnummer vil være (*V-02* for dette eksempel).

    ![Produktdetaljer for en teknisk ændringsordre](media/eng-change-order-product-details.png "Produktdetaljer for en teknisk ændringsordre")

1. Vælg **Gem** i handlingsruden.
1. I oversigtspanelet **Produktdetaljer** under fanen **Stykliste** skal du vælge **Linjer** for at åbne styklisten for version *V-01* af produkt *Z0001*.

    ![Teknisk produkts styklistelinjer](media/eng-product-bom-lines.png "Teknisk produkts styklistelinjer")

1. Vælg linjen for varenummer *D0003*, og vælg derefter **Slet** i handlingsruden. Værdien i feltet **Ændringstype** for denne linje ændres til *Slettet*.
1. Vælg **Gem** i handlingsruden.

    ![Ændret teknisk produkts styklistelinjer](media/eng-product-bom-lines-modified.png "Ændret teknisk produkts styklistelinjer")

1. Luk siden **Styklistelinje** for at vende tilbage til siden **Teknisk ændringsordre**.
1. I oversigtspanelet **Produktdetaljer** skal du under fanen **Stykliste** bemærkr, at værdien i feltet **Ændringstype** for stykliste *Z0001* nu er *Ændret*.

    ![Teknisk ændringsordre, der indeholder en ændret stykliste](media/eng-change-order-changed-bom.png "Teknisk ændringsordre, der indeholder en ændret stykliste")

    Ordren skal nu godkendes, før ændringerne kan behandles. Når ændringerne er behandlet, opdateres produkterne med de ændringer, der er inkluderet i den tekniske ændringsordre. I dette eksempel er den person, der opretter den tekniske ændringsordre, angivet som godkender.

1. Vælg **Godkend** i gruppen **Skift status** under fanen **Ændringsordre** i handlingsruden.
1. Vælg **Proces** for at opdatere oplysningerne om produktet.

## <a name="release-the-changed-product"></a>Frigive det ændrede produkt

Produktet kan nu frigives igen til firmaet *USMF* og derefter sendes til kunden. Udfør følgende trin for at frigive produktet direkte fra den tekniske ændringsordre.

1. Åbn den tekniske ændringsordre, du oprettede i den forrige øvelse, hvis den ikke allerede er åben.
1. Vælg **Søg** i gruppen **Produktfrigivelser** under fanen **Ændringsordre** i handlingsruden.
1. Søgeresultaterne viser, hvilke firmaer de berørte produkter er frigivet til. Luk søgeresultaterne.
1. I handlingsruden skal du under **Ændringsordre** i gruppen **Produktfrigivelser** vælge **Vis** for at åbne dialogboksen **Frigivelser**, hvor du kan få vist resultaterne af den forrige søgning.
1. Vælg hvert af de firmaer, du vil frigive produkter til.
1. Vælg **OK** for at lukke dialogboksen **Frigivelser** og vende tilbage til ændringsordren.
1. Vælg **Proces** i gruppen **Produktfrigivelser** under fanen **Ændringsordre** i handlingsruden for at frigive de berørte produkter til de valgte firmaer. Du kan også vælge **Frigiv produktstruktur** for at starte frigivelsesprocessen.

## <a name="complete-the-change-order"></a>Fuldføre ændringsrækkefølgen

Hvis du vil markere ændringsordren som fuldført, hvilket angiver, at der ikke længere er flere handlinger, skal du vælge **Fuldført** i handlingsruden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
