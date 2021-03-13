---
title: ER-destinationstype for e-mail
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer en maildestination for de enkelte MAPPE- eller FIL-komponenter i et ER-format (elektronisk rapportering).
author: NickSelin
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: e2e0da1c724269e0956be2f402b34ff376ed1990
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094098"
---
# <a name="email-er-destination-type"></a>ER-destinationstype for e-mail

[!include [banner](../includes/banner.md)]

Når der køres et elektronisk rapporteringsformat (ER-format), kan der genereres et eller flere udgående dokumenter. Komponenter i formatet **Mappe** eller **Fil** bruges i ER-formater til at angive strukturen i udgående dokumenter. Du kan konfigurere en maildestination for disse typer komponenter for at sende udgående dokumenter som vedhæftede filer i mails.

Du kan konfigurere en maildestination for alle **mappe-** eller **fil** komponenter i et ER-format. I dette tilfælde **sendes de enkelte udgående dokumenter enkeltvist via mail**. På baggrund af denne destinationsindstilling leveres et genereret dokument som en vedhæftet fil til en mail. 

> [!NOTE]
> Hvis der ikke genereres et dokument, fordi det **aktiverede** udtryk for den relevante **fil** komponent er konfigureret til at returnere en **falsk** boolesk værdi, sendes der ingen mail, heller ikke selvom der er konfigureret og aktiveret en maildestination for komponenten.

Du kan også [gruppere](#grouping) flere **mappe**- eller **fil** komponenter sammen og derefter konfigurere en maildestination for alle komponenterne i gruppen. I dette tilfælde sendes alle udgående dokumenter, der er genereret af komponenter, og som tilhører gruppen, **som flere vedhæftede filer i en enkelt mail**. På baggrund af denne destinationsindstilling leveres alle genererede dokumenter som en vedhæftet fil til en enkelt mail.

> [!NOTE]
> Hvis der genereres mindst ét dokument af en **fil** komponent i en gruppe af komponenter, sendes der en mail. Hvis der ikke genereres et dokument af grupperede komponenter, fordi det **aktiverede** udtryk for de enkelte **fil** komponenter er konfigureret til at returnere en **falsk** boolesk værdi, sendes der ingen mail, heller ikke selvom der er konfigureret og aktiveret en maildestination for gruppen af komponter.
>
> **Mail** er den eneste destination, der kan konfigureres for en gruppe af komponenter. Hvis du vil levere et dokument, der er baseret på mail, på indstillingen for maildestinationen for en gruppe, skal du tilføje en flere destinationsposter, vælge den ønskede komponent og derefter konfigurere en anden destination for denne post.

Der kan konfigureres flere grupper af komponenter for en enkelt ER-formatkonfiguration. På denne måde kan du konfigurere en maildestination for hver gruppe af komponenter og en maildestination for hver enkelt komponent.

## <a name="configure-an-email-destination"></a>Konfigurere en maildestination

Hvis du vil sende en outputfil eller flere outputfiler via mail, skal du gå til siden **Destination for elektronisk rapportering**, gå til oversigtspanelet **Fildestination**, vælge en komponent eller en gruppe af komponenter i gitteret og derefter vælge **Indstillinger**. I dialogboksen **Indstillinger for destination**, der vises, skal du angive indstillingen **Aktiveret** til **Ja** under fanen **Mail**. Du kan derefter angive mailmodtagere og redigere mailens emne og brødtekst. Du kan enten konfigurere konstanttekst til mailens emne og brødtekst, eller du kan bruge ER-[formler](er-formula-language.md) til dynamisk at oprette mailtekster.

Du kan konfigurere e-mailadresser for ER på to måder. Konfigurationen kan fuldføres på samme måde, som funktionen Udskriftsstyring fuldfører den, eller du kan fortolke en mailadresse ved at bruge en direkte reference til ER-konfigurationen via en formel.

[![Angive indstillingen Aktiveret til Ja for en maildestination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>E-mailadressetyper

Hvis du vælger **Rediger** ud for feltet **Til** eller **Cc** i dialogboksen **Indstillinger for destination**, åbnes dialogboksen **Mail til**. Vælg **Tilføj**, og vælg derefter typen af mailadresse, du vil bruge. I øjeblikket understøttes to typer: **Udskriftsstyringsmail** og **Konfigurationsmail**.

[![Vælg typen af mailadresse](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Mail for udskriftsstyring

Hvis du vælger **Udskriftsstyringsmail** som mailadressetype, kan du angive faste mailadresser i dialogboksen **Mail til** ved at angive følgende felter:

- Vælg **Ingen** i feltet **Mailkilde**.
- Angiv de faste mailadresser i feltet **Yderligere mailadresser, adskilt af ";"**.

Du kan også hente mailadresser fra kontaktoplysningerne for den part, du opretter et udgående dokument for. Hvis du vil bruge mailadresser, der ikke er faste, skal du gå til feltet **Mailkilde** og vælge [rollen](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles) for parten for en fildestination. Følgende roller understøttes:

- Kunde
- Leverandør
- Kundeemne
- Kontaktperson
- Konkurrent
- Arbejdstråd
- Ansøger
- Mulig kreditor
- Ikke-godkendt kreditor

Hvis du f.eks. vil konfigurere en maildestination for et ER-format, der bruges til at behandle kreditorbetalinger, skal du vælge rollen **Kreditor**.

Når du har valgt den ønskede rolle, skal du vælge knappen **Bind** (kædesymbolet) ud for feltet **Mailkildekonto** for at åbne siden [Formeldesigner](general-electronic-reporting-formula-designer.md). Du kan derefter bruge denne side til at konfigurere en formel, der under kørsel returnerer kontonummeret på den part, der er tildelt den konfigurerede rolle, fra det behandlede dokument til maildestinationen.

> [!NOTE]
> Formler er specifikke for ER-konfigurationen.

I feltet **Formel** på siden **Formeldesigner** skal du angive en dokumentspecifik reference til en understøttet rolle. I stedet for at skrive referencen i ruden **Datakilde** skal du finde og vælge den datakildenode, der repræsenterer en konto i den konfigurerede rolle, og derefter vælge **Tilføj datakilde** for at opdatere formlen. Hvis du f.eks. konfigurerer maildestinationen for konfigurationen af **ISO 20022 Kreditoverførsel**, der bruges til at behandle kreditorbetalinger, er den node, der repræsenterer en kreditorkonto, `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

![Konfigurere mailens kildekonto](./media/er_destinations-emaildefineaddresssource.gif)

Hvis kontonumrene for den konfigurerede rolle er entydige for hele forekomsten af Microsoft Dynamics 365 Finance, kan feltet **Firma for mailkilde** i dialogboksen **Mail to** være tomt.

Alternativt kan du have en situation, hvor forskellige parter i det [globale adressekartotek](../../fin-ops/organization-administration/overview-global-address-book.md) er blevet registreret i forskellige firmaer ([juridiske enheder](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) på en sådan måde, at de alle bruger det samme kontonummer til at udfylde den konfigurerede rolle. I dette tilfælde er kontonumrene for den konfigurerede rolle ikke entydige for hele Finans-forekomsten. Hvis du udtrykkeligt vil vælge en part, kan du derfor ikke kun angive et kontonummer. Du skal også angive det regnskab, som parten er blevet registreret i for at kunne udfylde den konfigurerede rolle. Vælg knappen **Bind** (kædesymbolet) ud for feltet **Firma for mailkilde** i dialogboksen **Mail til** for at åbne siden [Formeldesigner](general-electronic-reporting-formula-designer.md). Du kan derefter bruge denne side til at konfigurere en formel, der under kørsel returnerer koden for det firma, som den ønskede kilde skal findes inden for.

> [!TIP]
> Hvis du skal bruge firmakoden til at køre et ER-format, men ER-formatet ikke indeholder nogen datakilde, som firmakoden kan hentes fra, skal du konfigurere `GetCurrentCompany()`-formlen ved hjælp af den indbyggede ER-funktion [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md).

> [!NOTE]
> Formler er specifikke for ER-konfigurationen.

Hvis du vil angive, hvilken type mailadresser der skal bruges på kørselstidspunktet, skal du vælge **Rediger** ud for feltet **Til** i dialogboksen **Mail til** for at åbne rullelisten **Tildel mailadresse**. Angiv derefter følgende felter:

- Vælg det ønskede formål i feltet **Formål**. Der bruges kun mailadresser til de valgte formål fra kontaktpersoner for den fundne part.
- Angiv indstillingen **Primær kontakt** til **Ja** for at bruge en mailadresse, der er konfigureret for den fundne part som den primære mailadresse.

> [!NOTE]
> Hvis der er valgt formål i feltet **Formål**, og indstillingen **Primær kontakt** er angivet til **Ja** på samme tid, vil alle mails, der opfylder mindst ét konfigureret kriterie, blive brugt under kørsel.

### <a name="configuration-email"></a>Konfigurationsmail

Vælg **Konfigurationsmail** som mailadressetype, hvis den konfiguration, du bruger, har en node i datakilderne, der returnerer enten en enkelt mailadresse eller flere mailadresser, der er adskilt af semikolon (;). Du kan bruge [datakilder](general-electronic-reporting.md#FormatComponentOutbound) og [funktioner](er-formula-language.md#functions) i formeldesigneren til at få en korrekt formateret mailadresse eller korrekt formaterede mailadresser, der er adskilt af semikolon. Hvis du f.eks. bruger konfigurationen **ISO 20022 Kreditoverførsel**, er den node, der repræsenterer den primære mailadresse for en kreditor fra leverandørens kontaktoplysninger, som følgeskrivelsen skal sendes til, `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Konfigurere en mailadressekilde](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Gruppere formatkomponenter

Hvis du vil gruppere formatkomponenter, skal du gå til siden **Destination for elektronisk rapportering**, gå til oversigtspanelet **Fildestination**, vælge komponenterne i gitteret og derefter vælge **Gruppe**.

**Mail** er den eneste tidligere konfigurerede destination, der stadig er tilgængelig for de valgte komponenter. Der er ingen andre tidligere konfigurerede destinationer tilgængelige, fordi de betragtes som ikke-understøttede for en gruppe af komponenter. Du bliver informeret om disse ændringer efter behov.

Den post, du tidligere har tilføjet, betragtes som overskrift for den gruppe, der oprettes. Denne overskriftspost indeholder indstillingerne for maildestinationen for gruppen. Andre poster er gruppemedlemmer, der vil bruge indstillingerne for maildestinationen i gruppens overskriftspost.

Hvis du vil fjerne grupperingen af formatkomponenter, skal du gå til oversigtspanelet **Fildestination**, vælge en post, der tilhører gruppen, og derefter vælge **Opdel gruppe**.

- Hvis du vælger en overskriftspost, opdeles hele gruppen.
- Hvis du vælger en medlemspost, og det er den sidste medlemspost i en gruppe, opdeles hele gruppen.
- Hvis du vælger en medlemspost, der ikke er den sidste medlemspost i en gruppe, udelades posten fra den aktuelle gruppe.

I følgende illustration vises strukturen af et ER-format, der er konfigureret til at frembringe en komprimeret udgående fil, der indeholder en rykker og de relevante debitorfakturaer i PDF-format.

[![Struktur af et ER-format, der genererer udgående dokumenter](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

I følgende illustration vises processen, som beskrevet i dette emne, til gruppering af de enkelte komponenter og aktivering af **mail** destinationen for den nye gruppe, så der sendes en rykker sammen med de relevante debitorfakturaer som vedhæftede filer i mails.

[![Gruppere de enkelte komponenter og aktivere maildestinationen](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
- [Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md)
