---
title: ER-destinationstype for email
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer en emaildestination for de enkelte MAPPE- eller FIL-komponenter i et ER-format (elektronisk rapportering).
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2248b8a35b076eb778a50bbbc67d083380ceee62
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324002"
---
# <a name="email-er-destination-type"></a>ER-destinationstype for email

[!include [banner](../includes/banner.md)]

Når der køres et elektronisk rapporteringsformat (ER-format), kan der genereres et eller flere udgående dokumenter. Komponenter i formatet **Mappe** eller **Fil** bruges i ER-formater til at angive strukturen i udgående dokumenter. Du kan konfigurere en emaildestination for disse typer komponenter for at sende udgående dokumenter som vedhæftede filer i emails.

Du kan konfigurere en emaildestination for alle **mappe-** eller **fil** komponenter i et ER-format. I dette tilfælde **sendes de enkelte udgående dokumenter enkeltvist via email**. På baggrund af denne destinationsindstilling leveres et genereret dokument som en vedhæftet fil til en email. 

> [!NOTE]
> Hvis der ikke genereres et dokument, fordi det **aktiverede** udtryk for den relevante **fil** komponent er konfigureret til at returnere en **falsk** boolesk værdi, sendes der ingen email, heller ikke selvom der er konfigureret og aktiveret en emaildestination for komponenten.

Du kan også [gruppere](#grouping) flere **mappe**- eller **fil** komponenter sammen og derefter konfigurere en emaildestination for alle komponenterne i gruppen. I dette tilfælde sendes alle udgående dokumenter, der er genereret af komponenter, og som tilhører gruppen, **som flere vedhæftede filer i en enkelt email**. På baggrund af denne destinationsindstilling leveres alle genererede dokumenter som en vedhæftet fil til en enkelt email.

> [!NOTE]
> Hvis der genereres mindst ét dokument af en **fil** komponent i en gruppe af komponenter, sendes der en email. Hvis der ikke genereres et dokument af grupperede komponenter, fordi det **aktiverede** udtryk for de enkelte **fil** komponenter er konfigureret til at returnere en **falsk** boolesk værdi, sendes der ingen email, heller ikke selvom der er konfigureret og aktiveret en emaildestination for gruppen af komponter.
>
> **Mail** er den eneste destination, der kan konfigureres for en gruppe af komponenter. Hvis du vil levere et dokument, der er baseret på email, på indstillingen for emaildestinationen for en gruppe, skal du tilføje en flere destinationsposter, vælge den ønskede komponent og derefter konfigurere en anden destination for denne post.

Der kan konfigureres flere grupper af komponenter for en enkelt ER-formatkonfiguration. På denne måde kan du konfigurere en emaildestination for hver gruppe af komponenter og en emaildestination for hver enkelt komponent.

## <a name="enable-an-email-destination"></a>Aktivere en emaildestination

Hvis du vil sende en eller flere outputfiler via email, skal du følge disse trin.

1. På til siden **Destination for elektronisk rapportering** skal du i oversigtspanelet **Fildestination** vælge en komponent eller gruppe ag komponenter i gitteret.
2. Vælg **Indstillinger**, og i dialogboksen **Indstillinger for destination**, der vises, skal du angive indstillingen **Aktiveret** til **Ja** under fanen **Mail**.

[![Angive indstillingen Aktiveret til Ja for en emaildestination.](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="configure-an-email-destination"></a>Konfigurere en emaildestination

### <a name="email-content"></a>Mailindhold

Du kan redigere emnet og teksten i emailen.

I feltet **Emne** skal du indtaste teksten til det emailemne, der skal vises i emnefeltet i en elektronisk meddelelse, der genereres under kørslen. I feltet **Tekst** skal du indtaste den tekst til emailen, som skal vises i feltet for brødteksten i en elektronisk meddelelse. Du kan konfigurere en konstant tekst til emailens emne og indhold, eller du kan bruge ER-[formler](er-formula-language.md) til at oprette dynamiske emailtekster under kørslen. Den konfigurerede formel skal returnere en værdi for typen [Streng](er-formula-supported-data-types-primitive.md#string).

Brødteksten i emailen er i TEXT- eller HTML-format, afhængigt af emailklienten. Du kan bruge ethvert layout, alle tilpasninger og mærkninger, som HTML og integrerede overlappende typografiark (CSS) tillader.

> [!NOTE]
> E-mail-klienter pålægger layout- og typografibegrænsninger, der kan kræver justeringer af HTML-koden, og CSS, som du bruger til meddelelsesbrødteksten. Det anbefales, at du sætter dig ind i de bedste metoder til at oprette HTML-tekst, der understøttes af de mest populære emailklienter.
>
> Brug den rette kodning for at indsætte et linjeskift, afhængigt af tekstens formatering. Yderligere oplysninger finder du i definitionen af datatypen [Streng](er-formula-supported-data-types-primitive.md#string).

### <a name="email-addresses"></a>E-mail-adresser

Du kan angive emailens afsender og modtagere. Som standard sendes email på vegne af den aktuelle bruger. Hvis du vil angive en anden emailafsender, skal du konfigurere feltet **Fra**.

> [!NOTE]
> Når der konfigureres en emaildestination, er feltet **Fra** kun synligt for brugere, der har `ERFormatDestinationSenderEmailConfigure`-sikkerhedsrettigheden **Konfigurer afsendermailadressen til ER-formatdestinationer**.
>
> Når en emaildestination vises til redigering ved [kørsel](electronic-reporting-destinations.md#security-considerations), er feltet **Fra** kun synligt for brugere, der har `ERFormatDestinationSenderEmailMaintain`-sikkerhedsrettigheden **Vedligehold afsendermailadressen til ER-formatdestinationer**.
>
> Når feltet **Fra** er konfigureret til at bruge en anden emailadresse end den aktuelle brugers, skal enten tilladelsen **Send som** eller **Send på vegne af** være [angivet](/microsoft-365/solutions/allow-members-to-send-as-or-send-on-behalf-of-group) korrekt i forvejen. Ellers gælder følgende undtagelse ved kørsel: "Ikke i stand til at sende email som \<from email account\> fra kontoen \<current user account\>. Kontrollér tilladelserne 'Send som' på \<from email account\>."

Du kan konfigurere feltet **Fra** til at returnere mere end én emailadresse. I dette tilfælde bruges den første adresse på listen som emailafsenderadresse.

Hvis du vil angive emailmodtagere, skal du konfigurere felterne **Til** og **Cc** (valgfrit).

Du kan konfigurere emailadresser for ER på to måder. Konfigurationen kan fuldføres på samme måde som funktionen Udskriftsstyring, eller du kan fortolke en emailadresse ved at bruge en direkte reference til ER-konfigurationen via en formel.

## <a name="email-address-types"></a>E-mailadressetyper

Hvis du vælger **Rediger** ud for feltet **Fra**, **Til** eller **Cc** i dialogboksen **Indstillinger for destination**, åbnes dialogboksen **Mail fra**, **Mail til** eller **Mail cc**. Her kan du konfigurere emailafsenderen og emailmodtagere. Vælg **Tilføj**, og vælg derefter typen af emailadresse, du vil bruge. I øjeblikket understøttes to typer: **Udskriftsstyringsmail** og **Konfigurationsmail**.

[![Vælg typen af emailadresse.](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Mail for udskriftsstyring

Hvis du vælger **Udskriftsstyringsmail** som emailadressetype, kan du angive faste emailadresser i dialogboksen **Mail fra**, **Mail til** eller **Mail cc** ved at angive følgende felter:

- Vælg **Ingen** i feltet **Mailkilde**.
- Angiv de faste emailadresser i feltet **Yderligere emailadresser, adskilt af ";"**.

Du kan også hente emailadresser fra kontaktoplysningerne for den part, du opretter et udgående dokument for. Hvis du vil bruge emailadresser, der ikke er faste, skal du gå til feltet **Mailkilde** og vælge [rollen](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles) for parten for en fildestination. Følgende roller understøttes:

- Kunde
- Leverandør
- Kundeemne
- Kontaktperson
- Konkurrent
- Arbejdstråd
- Ansøger
- Mulig kreditor
- Ikke-godkendt kreditor
- Juridisk enhed

Hvis du f.eks. vil konfigurere en emaildestination for et ER-format, der bruges til at behandle kreditorbetalinger, skal du vælge rollen **Kreditor**.

Når du har valgt den ønskede rolle, skal du vælge knappen **Bind** (kædesymbolet) ud for feltet **Mailkildekonto** for at åbne siden [Formeldesigner](general-electronic-reporting-formula-designer.md). Du kan derefter bruge denne side til at konfigurere en formel, der under kørsel returnerer kontonummeret på den part, der er tildelt den konfigurerede rolle, fra det behandlede dokument til emaildestinationen.

> [!NOTE]
> Formler er specifikke for ER-konfigurationen.

I feltet **Formel** på siden **Formeldesigner** skal du angive en dokumentspecifik reference til en understøttet rolle. I stedet for at skrive referencen i ruden **Datakilde** skal du finde og vælge den datakildenode, der repræsenterer en konto i den konfigurerede rolle, og derefter vælge **Tilføj datakilde** for at opdatere formlen. Hvis du f.eks. konfigurerer emaildestinationen for konfigurationen af **ISO 20022 Kreditoverførsel**, der bruges til at behandle kreditorbetalinger, er den node, der repræsenterer en kreditorkonto, `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

![Konfigurere emailens kildekonto.](./media/er_destinations-emaildefineaddresssource.gif)

Hvis kontonumrene for den konfigurerede rolle er entydige for hele forekomsten af Microsoft Dynamics 365 Finance, kan feltet **Firma for emailkilde** i dialogboksen **Mail to** være tomt.

Alternativt kan du have en situation, hvor forskellige parter i det [globale adressekartotek](../../fin-ops/organization-administration/overview-global-address-book.md) er blevet registreret i forskellige firmaer ([juridiske enheder](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) på en sådan måde, at de alle bruger det samme kontonummer til at udfylde den konfigurerede rolle. I dette tilfælde er kontonumrene for den konfigurerede rolle ikke entydige for hele Finans-forekomsten. Hvis du udtrykkeligt vil vælge en part, kan du derfor ikke kun angive et kontonummer. Du skal også angive det regnskab, som parten er blevet registreret i for at kunne udfylde den konfigurerede rolle. Vælg knappen **Bind** (kædesymbolet) ud for feltet **Firma for emailkilde** i dialogboksen **Mail til** for at åbne siden [Formeldesigner](general-electronic-reporting-formula-designer.md). Du kan derefter bruge denne side til at konfigurere en formel, der under kørsel returnerer koden for det firma, som den ønskede kilde skal findes inden for.

> [!TIP]
> Hvis du skal bruge firmakoden til at køre et ER-format, men ER-formatet ikke indeholder nogen datakilde, som firmakoden kan hentes fra, skal du konfigurere `GetCurrentCompany()`-formlen ved hjælp af den indbyggede ER-funktion [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md).

> [!NOTE]
> Formler er specifikke for ER-konfigurationen.

Hvis du vil angive, hvilken type emailadresser der skal bruges på kørselstidspunktet, skal du vælge **Rediger** ud for feltet **Til** i dialogboksen **Mail til** for at åbne rullelisten **Tildel emailadresse**. Angiv derefter følgende felter:

- Vælg det ønskede formål i feltet **Formål**. Der bruges kun emailadresser til de valgte formål fra kontaktpersoner for den fundne part.
- Angiv indstillingen **Primær kontakt** til **Ja** for at bruge en emailadresse, der er konfigureret for den fundne part som den primære emailadresse.

> [!NOTE]
> Hvis der er valgt formål i feltet **Formål**, og indstillingen **Primær kontakt** er angivet til **Ja** på samme tid, vil alle emails, der opfylder mindst ét konfigureret kriterie, blive brugt under kørsel.

### <a name="configuration-email"></a>Konfigurationsmail

Vælg **Konfigurationsmail** som emailadressetype, hvis den konfiguration, du bruger, har en node i datakilderne, der returnerer enten en enkelt emailadresse eller flere emailadresser, der er adskilt af semikolon (;). Du kan bruge datakilder og [funktioner](er-formula-language.md#Functions) i formeldesigneren til at få en korrekt formateret mailadresse eller korrekt formaterede mailadresser, der er adskilt af semikolon. Hvis du f.eks. bruger konfigurationen **ISO 20022 Kreditoverførsel**, er den node, der repræsenterer den primære emailadresse for en kreditor fra leverandørens kontaktoplysninger, som følgeskrivelsen skal sendes til, `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Konfigurere en emailadressekilde.](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Gruppere formatkomponenter

Hvis du vil gruppere formatkomponenter, skal du gå til siden **Destination for elektronisk rapportering**, gå til oversigtspanelet **Fildestination**, vælge komponenterne i gitteret og derefter vælge **Gruppe**.

**Mail** er den eneste tidligere konfigurerede destination, der stadig er tilgængelig for de valgte komponenter. Der er ingen andre tidligere konfigurerede destinationer tilgængelige, fordi de betragtes som ikke-understøttede for en gruppe af komponenter. Du bliver informeret om disse ændringer efter behov.

Den post, du tidligere har tilføjet, betragtes som overskrift for den gruppe, der oprettes. Denne overskriftspost indeholder indstillingerne for emaildestinationen for gruppen. Andre poster er gruppemedlemmer, der vil bruge indstillingerne for emaildestinationen i gruppens overskriftspost.

Hvis du vil fjerne grupperingen af formatkomponenter, skal du gå til oversigtspanelet **Fildestination**, vælge en post, der tilhører gruppen, og derefter vælge **Opdel gruppe**.

- Hvis du vælger en overskriftspost, opdeles hele gruppen.
- Hvis du vælger en medlemspost, og det er den sidste medlemspost i en gruppe, opdeles hele gruppen.
- Hvis du vælger en medlemspost, der ikke er den sidste medlemspost i en gruppe, udelades posten fra den aktuelle gruppe.

I følgende illustration vises strukturen af et ER-format, der er konfigureret til at frembringe en komprimeret udgående fil, der indeholder en rykker og de relevante debitorfakturaer i PDF-format.

[![Struktur af et ER-format, der genererer udgående dokumenter.](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

I følgende illustration vises processen, som beskrevet i dette emne, til gruppering af de enkelte komponenter og aktivering af **mail** destinationen for den nye gruppe, så der sendes en rykker sammen med de relevante debitorfakturaer som vedhæftede filer i emails.

[![Gruppere de enkelte komponenter og aktivere emaildestinationen.](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
- [Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
