---
title: Bruge den elektroniske faktureringsservice til at importere kreditorfakturaer
description: Dette emne indeholder oplysninger om, hvordan du importerer kreditorfakturaer ved hjælp af tjenesten Elektronisk fakturering.
author: gionoder
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c28adbfe532e77a52cab7625b9539d1e8e528bea
ms.sourcegitcommit: 81bc42551e6c9af6ad38908afb606ee1f8d3c44b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473370"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Bruge den elektroniske faktureringsservice til at importere kreditorfakturaer

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med at importere kreditorfakturaer med elektronisk faktureringsservice. Den fører dig gennem konfigurationstrinnene i RCS (Regulatory Configuration Services), Dynamics 365 Finance og Dynamics 365 Supply Chain Management, som du skal følge for at modtage elektroniske kreditorfakturaer fra leverandørerne.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Konfigurere import af kreditorfakturaer i RCS
Benyt følgende fremgangsmåde for at konfigurere import af kreditorfakturaer i RCS:

1. Se oversigten over [generelt tilgængelige funktioner for elektronisk fakturering](e-invoicing-configuration-rcs.md#generally-available-features).
2. Vælg og importér funktionen til elektronisk fakturering. Du kan finde flere oplysninger under [Importere en funktion til elektronisk fakturering fra Microsoft-konfigurationsudbyder](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Opret en funktion til elektronisk fakturering for din organisation. Du kan finde flere oplysninger under [Oprette en funktion til elektronisk fakturering under din organisationsudbyder](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>Konfigurere en mailkontokanal

Konfigurer en mailkontokanal, hvis du med funktionen Elektronisk fakturering har oprettet import af elektroniske kreditorfakturaer fra vedhæftede filer, der modtages via mail.

1. Vælg den funktion til elektronisk fakturering, du har oprettet, i RCS. Sørg for at vælge den version, der har statussen **Kladde**.
2. Vælg en funktionsopsætning i gitteret under fanen **Opsætninger**, og vælg derefter **Rediger**.
3. Angiv navnet på kanalen i fanen **Datakanel** i feltgruppen **Parametre** i feltet **Datakanal**, og angiv navnet på kanalen. Kanalnavnet må ikke være på mere end ti tegn.
4. I feltet **Serveradresse** skal du angive kontoudbyderens e-mailadresse. Serveradressen til **https://outlook.live.com/** er f.eks. **imap-mail.outlook.com**.
5. Vælg **Serverport** i feltet, og angiv den port, der bruges af mailkontoudbyderen. Serverporten for **https://outlook.live.com/** er f.eks. **993**.
6. Vælg **Brugernavnhemmelighed**, og angiv navnet på Key Vault-hemmeligheden, der indeholder id'et for mailbrugerkontoen. Denne konfiguration skal oprettes i Azure-nøgle vault og -konfiguration i dit servicemiljø. 
7. Vælg **Brugeradgangskodehemmelighed**, og angiv navnet på Key Vault-hemmeligheden, der indeholder adgangskoden for mailbrugerkontoen.
8. Valgfrit – Angiv værdier i felterne **Fra filter**, **Emnefilter** og **Datofilter**.
9. Angiv navnene på de mail-mapper, hvor mails skal være:

    - Importeret fra: **Hovedmappe**
    - Gemt efter vellykket behandling: **Arkivmappe**
    - Gemt, efter at behandling af fejlen ikke lykkedes: **fejlmappe** Du behøver ikke oprette disse mapper i e-mailfeltet. Mapperne oprettes automatisk efter den første e-fakturaimport og -behandling. 
   
10. Tilføj oplysningerne om filfiltre i feltgruppen **Vedhæftede filer**. Der behandles kun vedhæftede filer, der opfylder det definerede filter. Du kan f.eks. konfigurere "\*.xml" for vedhæftede filer med xml-filtype. Navnet på den vedhæftede fil bruges i Dynamics 365 Finance eller Dynamics 365 Supply Chain Management under opsætningen. 
11. Gennemse og opdater kriterierne under fanen **Anvendelighedsregler**, hvis det er nødvendigt. Feltet **Kanal** skal være lig med den **datakanal**, der er angivet tidligere. Du kan finde flere oplysninger i [Anvendelighedsregler](e-invoicing-configuration-rcs.md#applicability-rules).
12. Vælg **Gem**, og luk siden.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Konfigurere en Microsoft SharePoint-kanal

Konfigurer en Microsoft SharePoint-kanal, hvis funktionen til elektronisk fakturering importerer elektroniske kreditorfakturaer fra filer, der er placeret i SharePoint-mapper.

1. Vælg den funktion til elektronisk fakturering, du har oprettet, i RCS. Sørg for at vælge den **Version**, der har statussen **Kladde**.
2. Vælg en funktionsopsætning i gitteret under fanen **Opsætninger**, og vælg derefter **Rediger**.
3. Vælg **SharePoint-adresse** under fanen **Datakanal** i feltgruppen **Parametre**, og angiv SharePoint-URL-adressen.
4. Vælg **Serverport**, og angiv den port, der bruges af mailkontoudbyderen.
5. Vælg **Program-id**, og angiv navnet på Key Vault-hemmeligheden, der indeholder id'et for SharePoint-klienten.
6. Vælg **Programhemmelighed**, og angiv navnet på Key Vault-hemmeligheden, der indeholder adgangskoden til SharePoint-klienten.
7. Vælg **Filfilter**. Gennemse og opdater masken for at filtrere de filer, der indeholder den elektroniske kreditorfaktura, der skal importeres.
8. Gennemse og opdater kriterierne under fanen **Anvendelighedsregler**, hvis det er nødvendigt. Du kan finde flere oplysninger i [Anvendelighedsregler](e-invoicing-configuration-rcs.md#applicability-rules).
9. Vælg **Gem**, og luk siden

### <a name="deploy-an-electronic-invoicing-feature"></a>Implementere en funktion til elektronisk fakturering

Hvis du vil implementere funktionen Elektronisk fakturering, skal du se [Implementere funktionen Elektronisk fakturering i servicemiljøet](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-or-supply-chain-management"></a>Konfigurere import af kreditorfakturaer i Finance eller Supply Chain Management
Gennemfør trinnene i følgende to afsnit for at konfigurere forskellige typer import af kreditorfakturaer.

### <a name="import-brazilian-nf-e-from-email"></a>Brasiliansk NF-e import fra e-mail

1. Log på dit Finance- eller Supply Chain Management-miljø, og kontrollér, at du er i den korrekte juridiske enhed.
2. Gå til **Organisationsadministration** > **Konfiguration** > **Elektroniske dokumentparametre**.
3. Under fanen **Funktioner** skal du sørge for, at der er valgt **NF-e Federal - brasiliansk elektronisk faktura**.
4. Under fanen **Eksterne kanaler** i feltgruppen **Kanaler** skal du vælge **Tilføj**.
5. I feltet **Kanal** skal du angive **NFe** (navnet på den kanal, der er angivet i konfigurationen af datakanalen til funktionen Elektronisk fakturering i RCS).
6. Indtast en beskrivelse i feltet **Beskrivelse**. I feltet **Virksomhed** skal du vælge den juridiske enhed.
7. I feltet **Dokumentkontekst** skal du vælge **Kontekstmodel for debitorfaktura – regnskabsdokumentkontekst**.
8. Vælg **Tilføj** i feltgruppen **Importkilder**.
9. I feltet **Navn** skal du angive **XmlFile** (navnet på det **Tilknytningsfilter**, der er angivet i konfigurationen af datakanalen til funktionen Elektronisk fakturering i RCS).
10. Indtast en beskrivelse i feltet **Beskrivelse**, og vælg **Modtagne NF-e XML-dokumenter** i feltet **Navn på dataenhed**.
11. I feltet **Modeltilknytning** skal du vælge **NF-e-mailimport – NF-e-mailimport (BR)** og derefter vælge **Gem**.
12. Under fanen **Elektronisk dokument** i feltgruppen **Elektronisk rapportering** skal du vælge **Tilføj** og vælge **Modtagne NF-e XML-dokument** i feltet **Tabelnavn**.
13. I feltet **Dokumentkontekst** skal du vælge **Kontekstmodel for debitorfaktura – Forespørg på regnskabsdokumentkontekst**.
14. Vælg **Forespørg på tilknytning – Tilknytning af regnskabsdokument** i feltet **Tilknytning af elektronisk dokumentmodel**.
15. Vælg **Svartyper**, og vælg derefter **Ny**.
16. I feltet **Svartype** skal du angive **Svar**. Vælg **Planlagt** i feltet **Indsendelsesstatus**.
17. I feltet **Modeltilknytning** skal du vælge **Modeltilknytning fra svarmeddelelse – Format til import af svarmeddelelse**.
18. Vælg **Gem**, og luk derefter siden.

### <a name="import-peppol-electronic-vendor-invoices"></a>Importere PEPPOL-elektroniske kreditorfakturaer

1. Gå til arbejdsområdet **Elektronisk rapportering** og vælg **Rapporteringskonfigurationer**.
2. Vælg en **kontekstmodel for debitorfaktura**, og vælg derefter **Opret konfiguration** > **Afledt fra navn: Kundefakturakontekstmodel, Microsoft** for at oprette en afledt konfiguration.
3. I **Kladde**-versionen skal du vælge **Designer** og i **Datamodel**-træet skal du vælge **Tilknyt model til datakilde**.
4. Vælg **DataChannel** i træet **Definitioner**, og vælg derefter **Designer**.
5. I træet **Datakilder** udvides containeren **$Context\_Kanal**. Vælg **Rediger**, og angiv navnet på datakanalen i feltet **Værdi**. Det er navnet på den kanal, der er angivet i konfigurationen af datakanalen til funktionen Elektronisk fakturering i RCS. 
7. Vælg **Gem**, og luk siden.
8. Luk siden.
9. Vælg den afledte konfiguration, du netop har oprettet fra **kontekstmodellen for debitorfakturaen**, og vælg **Ændringsstatus**  > **Fuldført** i oversigtspanelet **Versioner**.
10. Gå til **Organisationsadministration** > **Konfiguration** > **Parametre for elektroniske dokumenter**, og under fanen **Funktioner** skal du sørge for, at **PEPPOL - Global elektronisk faktura** er valgt. 
11. Under fanen **Eksterne kanaler** i feltgruppen **Kanaler** skal du vælge **Tilføj**.
12. I feltet **Kanal** angives datakanalnavnet og i feltet **Beskrivelse** angives en beskrivelse.
13. I feltet **Virksomhed** skal du vælge den juridiske enhed. 
14. Vælg den nye afledte konfiguration fra **debitorfakturakontekstmodellen** i feltet **Dokumentkontekst**. Tilknytningsbeskrivelsen skal være en **datakanalkontekst**.
15. Vælg **Tilføj** i feltgruppen **Importkilder**.
16. Angiv filternavnet **Vedhæftede filer** i feltet **Navn**, og vælg **kreditorfakturahoved** i feltet **Navn på dataenhed**.
17. Vælg **import for kreditorfaktura – Importer kreditorfaktura** i feltet **Modeltilknytning**.
18. Klik på **Gem**, og luk derefter siden.


## <a name="receive-electronic-invoices"></a>Modtage elektroniske fakturaer

Tjenesten Elektronisk fakturering udfører to trin under fakturaimport fra datakanalerne:

1. Får adgang til e-mailfeltet og læser e-mailen.
2. Behandler e-mailene. 
    
Hvis du vil udføre disse to trin, skal klienten ringe til tjenesten manuelt for hvert trin. Det anbefales dog, at du konfigurerer et batch til modtagelse af elektroniske dokumenter.

Benyt følgende fremgangsmåde for at modtage elektroniske fakturaer:

1. Gå til **Organisationsadministration** > **Periodisk** > **Elektroniske dokumenter** > **Modtag elektroniske dokumenter**.
2. Vælg **OK**, og luk derefter siden.


## <a name="view-receive-logs-for-electronic-invoices"></a>Se modtagelseslogge for elektroniske fakturaer

Du kan se modtagelseslogfilerne for elektroniske fakturaer ved at gå til **Organisationsadministration** > **Periodisk** > **Elektroniske dokumenter** > **Modtagelseslog for elektroniske dokumenter**.
Hvis du ikke kan se fakturaer, der er behandlet, skal du fjerne tabelfilteret.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
