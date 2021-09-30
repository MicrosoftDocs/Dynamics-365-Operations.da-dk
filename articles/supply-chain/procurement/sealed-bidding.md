---
title: Forseglet bud på tilbudsanmodninger
description: I dette emne beskrives, hvordan du kan konfigurere forseglede bud, der kan holde leverandørers budsvar hemmelige, indtil indkøbsmedarbejdere bryder forseglingen.
author: yanansong
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 02cbe9d6a6d157208d73ed756efae24df2a082de
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500628"
---
# <a name="sealed-bidding-for-rfqs"></a>Forseglet bud på tilbudsanmodninger

[!include [banner](../includes/banner.md)]

Forseglede bud holder leverandørers budsvar hemmelige, indtil indkøbsmedarbejdere bryder forseglingen. Alle de bud, der er relateret til en tilbudsanmodning, kan først få brudt forseglingen ved udløb af bud. Før et bud får brudt forseglingen, er det kun brugere, der har dedikerede brugerroller, og som repræsenterer leverandøren, der kan få adgang til det.

> [!IMPORTANT]
> Redigering eller udvidelse af formularer eller oprettelse af nye formularer eller forretningslogik kan ødelægge den beskyttelse, som Microsoft leverer til forseglede bud. Du bærer selv risikoen for at bruge ændringer, udvidelser, nye formularer eller forretningslogik eller manglende evne til at bruge den forseglede budfunktion pga. sådanne ændringer, udvidelser, nye formularer eller forretningslogik.  Microsoft er ikke ansvarlig for eventuelle skader, der måtte opstå som følge af eventuelle ændringer eller udvidelser til formularer eller nye formularer eller forretningslogik, som du opretter, eller som en tredjepart opretter for dig. Microsoft yder ikke teknisk support eller anden support til eventuelle ændringer, udvidelser, nye formularer eller forretningslogik, der er foretaget af dig eller en tredjepart på dine vegne. Det er dit eneansvar at overholde alle gældende love eller regulativer vedrørende forseglede bud.

## <a name="how-bids-are-kept-secure"></a>Hvordan bud kan beskyttes

Forseglede bud bruger asymmetrisk kryptering til at kryptere budkrypteringsnøglen og symmetrisk kryptering til at kryptere det faktiske bud. Systemet integreres med Microsoft Azure Key Vault for at generere og administrere de krypteringsnøgler, der bruges til at kryptere forseglede bud. Hvert bud har sin egen krypteringsnøgle. Denne kryptering holdes sikker i en key vault, der ejes af den organisation, der kører Dynamics 365 Supply Chain Management. Systemet får adgang til key vault efter behov, når kryptering og dekryptering er påkrævet.

## <a name="setup-and-configuration"></a>Installation og konfiguration

I dette afsnit beskrives de forudsætninger, der skal være på plads, før du kan udsende tilbudsanmodninger, der kræver forseglede bud.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>Trin 1: Konfigurer brugeradgang til forseglet bud

Når du bruger forseglet bud, er det kun brugere, der er angivet som kontaktperson for en leverandør, som kan se, redigere og afgive bud for den pågældende leverandør, indtil budperioden er udløbet. Disse brugere skal have rollen **Kreditor (ekstern)**, og de skal angives som kontaktperson for kreditorkontoen. Kontaktpersonen skal også have tilladelse til at udføre kreditorsamarbejde som beskrevet i [Konfigurere og vedligeholde kreditorsamarbejde](set-up-maintain-vendor-collaboration.md).

Da brugere, der har de relevante tilladelser, og som er konfigureret som leverandørkontaktpersoner, kan få adgang til de forseglede bud for en leverandør, er det vigtigt at registrere, hvem disse brugere er. Den systemadministrator, der konfigurerer brugere og sikkerhedsroller, er ansvarlig for at begrænse adgangen til forseglede bud til de brugere, der reelt har tilladelse til at se dem.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>Trin 2: Aktivér funktionen for forseglet bud

Før du begynder at konfigurere eller bruge denne funktion, skal du sørge for, at den er tilgængelig i systemet. Administratorer kan bruge arbejdsområdet **[Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Indkøb og forsyning*
- **Funktionsnavn:** *Forseglet bud for tilbudsanmodning*

### <a name="step-3-set-up-azure-key-vault"></a>Trin3: Konfigurer Azure Key Vault

Supply Chain Management bruger krypteringsnøgler til at beskytte alle forseglede bud og hemmeligholde dem indtil det rigtige tidspunkt. Det gør brug af funktionerne i Key Vault til at generere og administrere de nødvendige nøgler. Du skal derfor konfigurere en forbindelse fra Supply Chain Management til en Key Vault for at aktivere systemet.

> [!IMPORTANT]
> Key Vault skal oprettes i et Azure-abonnement, der ejes af din organisation (ikke det abonnement, hvor du kører Supply Chain Management).

Hvert bud henter sin egen hemmelige nøgle. Denne nøgle bruges, hver gang en bruger skal se, opdatere eller bryde forseglingen af buddet.

Key Vault genererer den nøgle, der bruges til at hente hemmeligheden, når leverandøren vælger **Bud** i brugergrænsefladen for leverandørsamarbejde. Nøglen udløber derefter efter et bestemt tidspunkt, som indkøbschefen angiver på siden **Indkøbs- og forsyningsparametre** i Supply Chain Management. Når nøglen udløber, kan du se, redigere eller bryde forseglingen af buddet. Det er derfor vigtigt at konfigurere udløb af nøgler, så der er tilstrækkelig tid til, at processen kan fuldføres.

I de næste tre trin skal du konfigurere forbindelsen til Key Vault. Du skal først konfigurere en Key Vault, der skal bruges til forseglede bud. Derefter skal du konfigurere Supply Chain Management til at kommunikere med Key Vault. Endelig angiver du udløbstiden for nøglen.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>Trin 4: Konfigurer en Key Vault, der skal bruges til forseglede bud

Benyt følgende fremgangsmåde for at konfigurere din Key Vault. Rækkefølgen af trinnene er vigtig.

1. Hvis du ikke allerede har oprettet et Azure-abonnement, der er adskilt fra det abonnement, hvor du kører Supply Chain Management, skal du konfigurere det.
1. Konfigurer en Key Vault i dit separate Azure-lager. Du kan finde flere oplysninger i [Vedligeholde et Azure Key Vault-lager](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage).
1. Konfigurer din Supply Chain Management-app, så den fungerer som klient til din Key Vault. Du kan finde flere oplysninger i [Konfigurere en Azure Key Vault-klient](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>Trin 5: Konfigurere Key Vault-parametre i Supply Chain Management

Hvis du vil konfigurere Supply Chain Management til at kommunikere med Key Vault under forseglede bud, skal du følge disse trin.

1. Log på Supply Chain Management, og gå til **Systemadministration \> Konfiguration \> Key Vault-parametre**.
1. Vælg **Ny** for at oprette en post, og angiv følgende felter til den:

    - **Navn** – Angiv et navn.
    - **Beskrivelse** – Indtast en beskrivelse.
    - **URL-adresse til Key Vault** – Angiv standard-URL-adressen til din Key Vault.
    - **Key Vault-klient** – Angiv det interaktive klient-id for det Active Directory-program, der er tilknyttet en Key Vault til godkendelse.
    - **Key Vault-hemmelig nøgle** – Angiv den hemmelige reference til certifikatet.
    - **Aktiveret for forseglet bud** – Angiv denne indstilling til *Ja*.

![Siden Key Vault-parametre](media/sealed-bidding-key-vault-param.png "Siden Key Vault-parametre")

> [!NOTE]
> Du kan kun aktivere én Key Vault-konfiguration til forseglede bud ad gangen. Før du deaktiverer en eksisterende konfiguration af Key Vault, skal du sikre dig, at alle de forseglede bud, der bruger den, ikke er forseglet. Kontrollér alle tilbudsanmodningstilfælde af typen *Forseglet*, og sørg for, at alle svar på den ikke er forseglet.

### <a name="step-6-set-the-key-expiration-time"></a>Trin 6: Angiv udløbstiden for nøglen

Hvis du vil angive det udløbstidspunkt, der anvendes på den nøgle, der genereres for hvert nye bud, skal du følge disse trin.

1. Gå til **Indkøbs- og forsyningsparametre \> Konfiguration \> Indkøbs- og forsyningsparametre**.
1. Angiv det antal dage, som perioden for tilbudsanmodningen skal vare, i feltet **Modregnede dage** under fanen **Tilbudsanmodning**. Når der oprettes en tilbudsanmodning, føjes det antal dage, du angiver her, til systemdatoen for at definere standardudløbsdatoen for tilbudsanmodningen.
1. I feltet **Forskydning af udløbsdag for krypteringsnøgle** skal du angive det antal dage, hver krypteringsnøgle skal være gyldig, efter at den er udstedt. Når krypteringsnøglen udløber, kan ingen se, redigere eller bryde forseglingen af buddet, som bruger den.

> [!TIP]
> Værdien i feltet **Forskydning af udløbsdag for krypteringsnøgle** bør ikke være mindre end værdien i feltet **Modregnede dage**.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>Trin 7: Angiv standardbudtypen

Hver tilbudsanmodningssag har en budtype. Budtypen definerer, om den pågældende tilbudsanmodningssag har åben eller lukket budafgivning.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>Sager om tilbudsanmodning, der ikke har en anmodningstype

Hvis du vil angive den standardbudtype, der er knyttet til nye tilbudsanmodningssager, som ikke tildeles en anmodningstype, når de oprettes, skal du følge disse trin.

1. Gå til **Indkøbs- og forsyningsparametre \> Konfiguration \> Indkøbs- og forsyningsparametre**.
1. Angiv feltet **Budtype** til **Forseglet** under fanen *Tilbudsanmodning.*

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>Sager om tilbudsanmodning, der har en anmodningstype

Hvis du vil angive den standardbudtype, der er knyttet til nye tilbudsanmodningssager, som tildeles en anmodningstype, når de oprettes, skal du følge disse trin.

1. Gå til **Indkøb og forsyning \> Konfiguration \> Tilbudsanmodning \> Anmodningstype**.
1. Opret en ny anmodningstype, eller vælg en eksisterende anmodningstype, hvor du vil bruge budtypen *Forseglet*.
1. Indstil feltet **Budtype** til *Forseglet*.
1. Gentag disse trin for hver ekstra anmodningstype, hvor du vil implementere forseglet bud.

> [!TIP]
> En anmodningstype behøver ikke at blive tildelt, når der oprettes en ny tilbudsanmodning. Hvis der er tildelt en anmodningstype, kan standardbudtypen for en tilbudsanmodning hente den. Ellers kan den standardanmodningstype, der er defineret i parametre for indkøb og forsyning, bruges.

## <a name="the-sealed-bidding-process"></a>Processen for forseglede bud

Forseglet bud følger stort set den samme proces, som beskrives i [Oversigt over tilbudsanmodninger](request-quotations.md). Den væsentligste forskel er, at buddataene og de vedhæftede filer bevares krypteret, indtil forsegling af buddet brydes.

> [!IMPORTANT]
> [Spørgeskemaer](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) er ikke krypterede og bør ikke bruges til indsamling af følsomme oplysninger

Her er en oversigt over processen:

1. Du opretter og sender en tilbudsanmodning til en eller flere leverandører.
1. Leverandører svarer ved at indsende deres forseglede bud.
1. Du bryder forseglingen af buddene, når budposten er udløbet.
1. Buddene vises, og du kan evaluere og sammenligne dem.
1. Når et bud er accepteret, kan du generere en indkøbsordre, generere en købsaftale eller opdatere en indkøbsrekvisition.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Oprette en tilbudsanmodningssag, der bruger forseglede bud

Processen til oprettelse af en tilbudsanmodningssag til forseglede bud er stort set den samme som processen for ikke-forseglede bud. Du kan finde flere oplysninger om oprettelse af begge typer tilbudsanmodningssager under [Oprette en tilbudsanmodning](tasks/create-request-quotation.md). I dette afsnit fremhæves nogle få vigtige overvejelser, når du opretter en tilbudsanmodning til forseglede bud.

Tilbudsanmodningssager for forseglede bud skal have **Budtypen** *Forseglet*. Du kan tildele denne værdi til en tilbudsanmodningssag på tre måder:

- Angiv værdien direkte i tilbudsanmodningssagen, når du har oprettet den.
- Definer forseglet bud som standardbudtype for alle sager med tilbudsanmodninger i Indkøbs- og forsyningsparametre. (Se afsnittet [Angiv standardbudtypen](#set-default-bid-type) tidligere i dette emne).
- Når du opretter en ny tilbudsanmodningssag, skal du vælge en anmodningstype, der er konfigureret til forseglede bud. (Se afsnittet [Angiv standardbudtypen](#set-default-bid-type)).

Til forseglede bud fastlægger tilbudsanmodningssagens **Udløbsdato og -klokkeslæt**, hvornår de indsendte bud kan få brudt forseglingen. Værdien for **Udløbsdato og -klokkeslæt** på hver linje svarer til værdien i overskriften.

Du kan ikke ændre budtypen, efter at en tilbudsanmodningssag er afsendt.

### <a name="vendors-respond-to-an-rfq"></a>Leverandører reagerer på en tilbudsanmodning

Leverandører, der svarer på et forseglet bud, anvender samme procedure, som de bruger til at svare på åbne bud, som det er beskrevet i [Arbejde med tilbudsanmodninger i arbejdsområdet Kreditorbud](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace). Du kan finde detaljerede instruktioner til, hvordan du både kan arbejde med åbne bud og forseglede bud, i [Angive og sammenligne bud på tilbudsanmodninger og tildele kontrakter](tasks/enter-compare-rfq-bids-award-contracts.md). Den eneste forskel mellem behandling af forseglede bud og behandling af åbne bud er, at indkøbsmedarbejderne ikke kan åbne en leverandørs forseglede bud, før budperioden er udløbet. Kun en kontaktperson for leverandøren kan åbne denne leverandørs forseglede bud.

> [!IMPORTANT]
> For forseglede bud kan leverandører kun uploade vedhæftede filer i PDF-format. Ingen andre formater accepteres.

Når en registreret leverandørbruger har valgt **Bud** på en tilbudsanmodning med forseglet bud, kan de angive deres buddata, som vil blive opbevaret sikkert. Leverandører kan gemme deres arbejde, mens de forbereder et bud, vende tilbage til det så ofte som nødvendigt og derefter sende det, når det er klar. Leverandører kan også se deres bud, når de har indsendt det. Hvis leverandører skal ændre deres bud, når de har indsendt det, kan de tilbagekalde det, opdatere det og sende det igen når som helst, indtil budperioden udløber.

Følgende betingelser gælder for forseglede bud:

- Under forseglede bud opretter systemet en *Tilbudsanmodning*-kladde.
- Når en leverandør sender et bud, oprettes der tilbudsanmodningskladder uden linjer, som har en forseglet pris.
- Når sagens forsegling er brudt, oprettes der tilbudsanmodningskladder med en pris og et beløb. Du kan åbne denne kladde ved at vælge **Kladder til tilbudsanmodninger** på siden **Alle tilbudsanmodninger**.
- Systemet gemmer en log over hver af de handlinger, som brugerne udfører på et forseglet bud. Disse handlinger omfatter visning, redigering og lagring af bud. Loggen kan både ses af leverandøren og de indkøbsmedarbejdere, der har adgang til buddet.
- Efterhånden som buddet skrider frem, kan indkøbsmedarbejderne se dets status. Status er enten *Leverandør opdaterer* eller *Sendt af leverandør*.
- Statussen for linjerne i et forseglet bud forbliver *Sendt*, indtil buddets forsegling brydes.
- Hvis leverandøren vælger at afvise et bud, er buddets **Svarstatus** *Afvist af leverandør*. Denne status kan ses af indkøbsmedarbejdere.
- Besvarelser i spørgeskemaer gemmes **ikke** i krypteret form i databasen. De er derfor ikke forseglet. De vil dog ikke være synlige i brugergrænsefladen til tilbudsanmodningen, før sagens forsegling er brudt.

### <a name="all-sealed-bid-activities-are-logged"></a>Alle forseglede budaktiviteter logføres

En detaljeret log registrerer alle brugeraktiviteter og handlinger for et bud. Aktivitetsloggen sætter organisationer i stand til at bestemme, hvem der har opdateret et bud i løbet af levetiden, og hvilke opdateringer der var. Den giver også organisationer mulighed for at bekræfte, at det kun er godkendte personer, der har adgang til et forseglet bud. Aktivitetsloggen er tilgængelig på hvert buds **Aktivitetsside**.

### <a name="review-rfq-activity"></a>Gennemse aktivitet i tilbudsanmodning

Alle interaktioner med buddet logføres og kan ses på siden **Aktivitet**. Følgende illustration viser et eksempel.

![Eksempel på siden Aktivitet](media/sealed-bidding-rfq-activity.png "Eksempel på siden Aktivitet")

Leverandører kan få adgang til siden **Aktivitet** ved at vælge **Aktivitet** på siden **Forseglet bud for tilbudsanmodning**. Indkøbspersonalet har adgang til den ved at vælge **Aktivitet** på siden **Tilbudsanmodning**. Aktivitetsloggen giver fuld synlighed for leverandører og for de indkøbsmedarbejdere, der har adgang til buddet. Den kan derfor afsløre enhver uautoriseret adgang.

### <a name="unseal-sealed-bids"></a>Bryde forseglingen af bud

Når den værdi for **Udløbsdato og -klokkeslæt**, der blev konfigureret for et forseglet bud i tilbudsanmodningssag, er overskredet, bliver knappen **Bryd forsegling** tilgængelig. Vælg **Bryd forsegling** for at bryde forseglingen af alle bud på den valgte tilbudsanmodningssag. Derefter kan alle buddata og vedhæftede filer ses, så svarene på sagen kan administreres. Derudover oprettes der kladder, der indeholder de indsendte buddata.

Brydning af forsegling logføres og kan ses på siden **Aktivitet**.

### <a name="process-accepted-bids"></a>Behandle accepterede bud

Processen til sammenligning og godkendelse af tidligere forseglede bud er den samme som processen for åbne bud. Du kan finde oplysninger om, hvordan du scorer, sammenligner, afviser og accepterer ikke-forseglede bud i [Angive og sammenligne bud på tilbudsanmodninger og tildele kontrakter](tasks/enter-compare-rfq-bids-award-contracts.md).

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>Aktivitetsloggen med tilbudsanmodninger kan aldrig slettes

Ingen, ikke engang administratorer og Microsoft Support, kan redigere eller slette aktivitetsloggen for tilbudsanmodninger. Denne restriktion er med til at sikre, at den forseglede budproces er retfærdig. Det er også med til at sikre, at et præcist revisionsspor vedligeholdes.
