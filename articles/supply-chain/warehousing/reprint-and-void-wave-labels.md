---
title: Genudskrive og annullere bølgeetiketter
description: I dette emne forklares, hvordan du kan annullere og udskrive eksisterende bølgeetiketter.
author: GarmMSFT
manager: PJacobse
ms.date: 07/09/2020
ms.topic: reprint-and-void-wave-labels
ms.service: dynamics-ax-applications
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: af92334af28824b3fcebde5f046bd7c6da459885
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016648"
---
# <a name="reprint-and-void-wave-labels"></a>Genudskrive og annullere bølgeetiketter

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du håndterer etiketter, der genereres af bølgebehandling. (Du kan finde en detaljeret beskrivelse og konfigurationsvejledning i [Konfigurere udskrivning af bølgeetiketter](../warehousing/configure-wave-label-printing.md).)

Du kan til enhver tid udskrive bølgeetiketter igen. Det kan f.eks. være nødvendigt at udskrive en enkelt etiket, hvis en eksisterende etiket er gået tabt eller beskadiget. Alternativt kan en lagermedarbejder eller en leder have behov for at genudskrive en hel række etiketter, hvis antallet og/eller sammensætningen af en hel serie bølgeetiketter er blevet ændret (f.eks. på grund af manglende lager eller andre årsager). Ofte, selv om antallet af kartoner kun er ændret, skal hele rullen genudskrives for at holde det samlede antal nøjagtigt i afsnittet "Karton X af Y" i hver etiket.

Funktionen til genudskrivning af bølgeetiketter understøtter følgende funktioner:

- Genudskriv etiketter både fra lagerstedsappen og den detaljerede klient.
- Annuller etiketter og udskriv dem igen på samme tid. (Muligheden for at annullere etiketter er f.eks. integreret i korte plukscenarier).
- Rydde op i historikken over bølgeetiketter.

Dette emne indeholder en samling scenarier, der viser eksempler på, hvordan du kan arbejde med funktionen til genudskrivning af bølgeetiketter.

> [!IMPORTANT]
> Hvis du vil arbejde gennem de scenarier, der vises i dette emne, skal du først aktivere og konfigurere de relevante bølgeudskrivningsfunktioner som beskrevet under [Konfigurere udskrivning af bølgeetiketter](../warehousing/configure-wave-label-printing.md). Flere af scenarierne i dette emne kræver også, at du først arbejder i scenarierne i dette emne for at oprette de nødvendige eksempeldata.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>Scenarie 1: Genudskrive etiketter fra webklienten

Du kan få vist og udskrive bølgeetiketter fra følgende sider. Gå til handlingsruden på enhver side, og vælg **Bølgeetiketter** i gruppen **Relaterede oplysninger** under fanen **Forsendelser**.

- Alle forsendelser \> Forsendelsesoplysninger
- Alle laster \> Lastdetaljer
- Alle bølger
- Bølgelabels
- Historik for bølgelabel

Udfør følgende trin for at udskrive en bølgeetiket fra webklienten igen.

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Vælg den bølge, der skal udskrives etiketter fra.
1. I handlingsruden under fanen **Bølge** i gruppen **Udskriv** skal du vælge **Bølgeetiketter**.
1. Benyt en eller begge af følgende fremgangsmåder:

    - Hvis du vil genudskrive etiketten skal du vælge en printer i feltet **Printernavn**. (Lad feltet være tomt, hvis du blot vil opdatere oplysningerne om bølgeetiketter uden at genudskrives etiketten).
    - Hvis du vil opdatere etiketten, skal du markere afkrydsningsfeltet **Opdater bølgeetiketdetaljer**. (Undlad at markere dette afkrydsningsfelt, hvis du blot vil udskrive den forrige etiket igen.)

    > [!NOTE]
    > Hver gang der udskrives eller genudskrives en bølgeetiket, konverteres dens data via det relevante bølgeetiketlayout, og alle pladsholdere erstattes med faktiske værdier. Den resulterende streng lagres i en post i historikken over bølgeetiketter. Hvis afkrydsningsfeltet **Opdater bølgeetiketdetaljer** er markeret, bruges de lagrede ZPL-data (Zebra Programming Language), når en etiket udskrives igen. Hvis afkrydsningsfeltet **Opdater bølgeetiketdetaljer** er markeret, genereres en ny streng. De eksisterende bølgeetiketter genberegnes også, og eventuelle overskydende etiketter (f.eks. hvis de relaterede arbejdslinjer er blevet annulleret eller ændret) markeres som **Annulleret** og udskrives ikke igen.

1. Vælg **OK** for at bekræfte valget.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>Scenarie 2: Genudskrive etiketter fra lagerstedsappen

Dette scenarie anvendes typisk, hvis en etiketrulle er blevet væk eller beskadiget. Det indeholder et eksempel, der viser, hvordan du kan konfigurere menupunkter i mobilenheder, som gør det muligt for arbejdere at udskrive enkelte og flere etiketter igen. Derefter vises det, hvordan du bruger disse nye menupunkter, mens du arbejder på en mobilenhed.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>Konfigurere de nødvendige menupunkter og menuer for mobilenheden

Før arbejdere kan genudskrive etiketter fra en mobil enhed, skal du konfigurere menupunkterne for at angive denne funktionalitet og derefter føje disse elementer til menuen i lagerstedsappen.

#### <a name="create-new-mobile-device-menu-items"></a>Oprette nye menupunkter på en mobilenhed

Udfør følgende trin for at oprette en ny samling menupunkter til genudskrivning af etiketter fra lagerstedsappen.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Opret et menupunkt, og angiv følgende værdier for det:

    - **Navn på menupunkt:** *Udskriv en enkelt bølgeetiket igen*
    - **Titel:** *Udskriv en enkelt bølgeetiket igen*
    - **Tilstand:** *Indirekte*
    - **Aktivitetskode:** *Udskriv en enkelt bølgeetiket igen*

1. Opret et andet menupunkt, og angiv følgende værdier for det:

    - **Navn på menupunkt:** *Udskriv etiketter (vare) igen*
    - **Titel:** *Udskriv bølgeetiketter (vare) igen*
    - **Tilstand:** *Indirekte*
    - **Aktivitetskode:** *Udskriv flere bølgeetiketter igen*
    - **Vis filter for gruppering af arbejdsliste:** *Ja*
    - **Systemgrupperingsfelt:** *Forsendelses-id*
    - **Systemgrupperingsetiket:** *Forsendelses-id*
    - **Udskrivningstilstand:** *Produkt*

1. I handlingsruden skal du vælge **Feltliste** for at åbne en side, hvor du kan vælge de felter, der skal vises for at hjælpe arbejdere med at identificere den korrekte etiketrulle.
1. Du kan få vist op til syv felter. Brug rullelisterne til at vælge det felt, der vises på de enkelte tilgængelige positioner. Lad de felter være, som du ikke behøver at udfylde. 

    Her er et eksempel:

    - **Visningsfelt:** *EtiketVareId*
    - **Visningsfelt 2:** *EtiketVareNavn*
    - **Visningsfelt 3:** *LagerAntal*
    - **Visningsfelt 4:** *EtiketEnhedId*

1. Luk siden.
1. Opret et tredje menupunkt, og angiv følgende værdier for det:

    - **Navn på menupunkt:** *Udskriv etiketter (fasttekst) igen*
    - **Titel:** *Udskriv bølgeetiketter (fasttekst) igen*
    - **Tilstand:** *Indirekte**
    - **Aktivitetskode:** *Udskriv flere bølgeetiketter igen*
    - **Vis filter for gruppering af arbejdsliste:** *Ja*
    - **Systemgrupperingsfelt:** *Forsendelses-id*
    - **Systemgrupperingsetiket:** *Forsendelses-id*
    - **Udskrivningstilstand:** *Optælling*

1. I handlingsruden skal du vælge **Feltliste** og derefter bruge rullelisterne til at vælge de felter, der skal vises for at hjælpe arbejderne med at identificere den korrekte etiketrulle (for eksempel *EtiketVareId* , *EtiketVareNavn* , *LagerAntal* , *EtiketEnhedId* og *AntalEtiketter* ).
1. Luk siden.
1. Opret et fjerde menupunkt, og angiv følgende værdier for det:

    - **Navn på menupunkt:** *Udskriv etiketter (efter sidste) igen*
    - **Titel:** *Udskriv bølgeetiketter (efter sidste) igen*
    - **Tilstand:** *Indirekte*
    - **Aktivitetskode:** *Udskriv flere bølgeetiketter igen*
    - **Vis filter for gruppering af arbejdsliste:** *Ja*
    - **Systemgrupperingsfelt:** *Forsendelses-id*
    - **Systemgrupperingsetiket:** *Forsendelses-id*
    - **Udskrivningstilstand:** *Sidste gode bølgeetiket-id*

1. I handlingsruden skal du vælge **Feltliste** og derefter bruge rullelisterne til at vælge de felter, der skal vises for at hjælpe arbejderne med at identificere den korrekte etiketrulle (for eksempel *EtiketVareId* , *EtiketVareNavn* , *LagerAntal* , *EtiketEnhedId* og *AntalEtiketter* ).
1. Luk siden.

#### <a name="set-up-the-mobile-device-menu"></a>Konfigurere mobilenhedsmenuen

Udfør følgende trin for at føje de nye menupunkter til menuen i lagerstedsappen.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Vælg en eksisterende menu for **Udgående**.
1. På listen til venstre kan du finde de menupunkter til genudskrivning, som du netop har oprettet, og derefter bruge den højre pileknap til at føje dem til listen til højre.
1. Luk siden.

### <a name="use-cases"></a>Brugseksempler

De brugseksempler, der angives her, giver eksempler på, hvordan du kan bruge de forskellige menupunkter i mobilenheder, som du konfigurerer, så arbejderne kan udskrive bølgeetiketter igen.

Før du kan arbejde dig gennem med disse brugseksempler, skal følgende forudsætninger være gældende:

- Demonstrationsdata skal være installeret, og du skal vælge den juridiske enhed **USMF**.
- Udskrivning af bølgeetiketter skal konfigureres, og nogle etiketter skal genereres, som beskrevet under [Konfigurere udskrivning af bølgeetiketter](../warehousing/configure-wave-label-printing.md).

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Brugseksempel 2.1: en enkelt bølgeetiket er ridset og skal udskrives igen.

1. Log på lagerstedsappen som en bruger, der har adgang til lagersted *62*. (I standarddemodataene kan du logge på ved at bruge bruger-id'et *62* og adgangskoden *1*.)
1. Gå til **Udgående \> Udskriv af enkelt bølgeetiket igen**.
1. Angiv eller scan bølgeetiket-id'et.
1. Vælg den printer, der skal genudskrives på.
1. Vælg **OK** for at bekræfte handlingen.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Brugseksempel 2.2: Flere etiketter til æsker af samme vare blev beskadiget og skal udskrives igen. Hver etiket har en produktstregkode, men ikke en fasttekst eller et SSCC-nummer.

1. Log på lagerstedsappen som en bruger, der har adgang til lagersted *62*. (I standarddemodataene kan du logge på ved at bruge bruger-id'et *62* og adgangskoden *1*.)
1. Gå til **Udgående \> Udskriv etiketter (vare) igen**.
1. Angiv eller scan forsendelses-id'et.
1. Vælg det felt, som har den korrekte etiketrulle at genudskrive fra.
1. Scan produktstregkoden fra en eksisterende label for at bekræfte, at den rette linje er valgt.
1. Angiv antallet af etiketter, der skal genudskrives.
1. Vælg den printer, der skal genudskrives på.
1. Vælg **OK** for at bekræfte handlingen.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Brugseksempel 2.3: Flere etiketter til æsker blev ikke udskrevet på grund af papirstop i printer. Da etiketterne har fasttekster, kan du definere, at kartonintervallet skal udskrives igen.

1. Log på lagerstedsappen som en bruger, der har adgang til lagersted *62*. (I standarddemodataene kan du logge på ved at bruge bruger-id'et *62* og adgangskoden *1*.)
1. Gå til **Udgående \> Udskriv etiketter (fasttekst) igen**.
1. Angiv eller scan forsendelses-id'et.
1. Vælg det felt, som har den korrekte etiketrulle at genudskrive fra.
1. Angiv den første karton for at udskrive en etiket igen.
1. Angiv den sidste karton for at udskrive en etiket igen. Du kan også lade dette felt være tomt for at udskrive etiketter for alle kartoner efter den angivne første karton.
1. Vælg den printer, der skal genudskrives på.
1. Vælg **OK** for at bekræfte handlingen.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Brugseksempel 2.4: Flere etiketter til æsker blev ikke udskrevet på grund af papirstop i printer. Den sidste gode etiket har et bølgeetiket-id, der udskrives som stregkode.

1. Log på lagerstedsappen som en bruger, der har adgang til lagersted *62*. (I standarddemodataene kan du logge på ved at bruge bruger-id'et *62* og adgangskoden *1*.)
1. Gå til **Udgående \> Udskriv etiketter (efter sidste) igen**.
1. Angiv eller scan forsendelses-id'et.
1. Vælg det felt, som har den korrekte etiketrulle at genudskrive fra.
1. Angiv eller scan bølgeetiket-id'et for den sidste gode bølgeetiket. Appen identificerer den næste etiket i serien som den første karton, som en etiket skal udskrives for igen.
1. Angiv den sidste karton for at udskrive en etiket igen. Du kan også lade dette felt være tomt for at udskrive etiketter for alle kartoner efter den angivne første karton.
1. Vælg den printer, der skal genudskrives på.
1. Vælg **OK** for at bekræfte handlingen.

## <a name="scenario-3-short-pick-and-reprint"></a>Scenarie 3: Kort pluk, og udskriv igen

Før du kan arbejde dig gennem dette scenarie, skal følgende forudsætninger være gældende:

- Demonstrationsdata skal være installeret, og du skal vælge den juridiske enhed **USMF**.
- Udskrivning af bølgeetiketter skal konfigureres, og nogle etiketter skal genereres, som beskrevet under [Konfigurere udskrivning af bølgeetiketter](../warehousing/configure-wave-label-printing.md).

### <a name="set-up-work-exceptions"></a>Konfigurer arbejdsundtagelser

Arbejdsundtagelser styrer funktionsmåden ved kort plukning. Følg disse trin for at konfigurere en arbejdsundtagelse:

1. Gå til **Lokationsstyring \> Konfiguration \> Arbejde \> Arbejdsundtagelser**.
1. Opret en post, der har følgende indstillinger:

    - **Arbejdsundtagelseskode:** *Kort pluk og udskrivning*
    - **Undtagelsestype:** *Kort pluk*
    - **Foreslå genudskrivning af bølgeetiket:** *Ja*

### <a name="void-and-reprint-after-a-short-pick"></a>Annuller og genudskriv efter et kort pluk

1. Log på lagerstedsappen som en bruger, der har adgang til lagersted *62*. (I standarddemodataene kan du logge på ved at bruge bruger-id'et *62* og adgangskoden *1*.)
1. Åbn en arbejdsbehandlingsproces for det salgsordrearbejde, der blev oprettet, da der oprindeligt blev udskrevet bølgeetiketter.
1. Vælg **Kort pluk**.
1. Vælg den arbejdsundtagelseskode, som du har oprettet til dette scenarie.
1. Hvis du valgte den korrekte undtagelse, skal afkrydsningsfeltet **Annuller og udskriv igen** være tilgængeligt. Markér dette afkrydsningsfelt, og bekræft. Når det er bekræftet, genberegnes serien for etiketrulle, der er identificeret af feltet **Etiket-build-id** , på basis af det ændrede antal på arbejdslinje. Derefter udskrives den på den angivne printer.
