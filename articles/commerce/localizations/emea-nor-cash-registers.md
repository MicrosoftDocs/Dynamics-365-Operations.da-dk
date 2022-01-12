---
title: Kasseapparatfunktionalitet til Norge
description: Dette emne indeholder en oversigt over kasseapparatfunktionaliteten, der er tilgængelig for Norge i Microsoft Dynamics 365 Commerce, og indeholder retningslinjer for opsætning af funktionen.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: bb87b3a7405ef3d8435748813fa66db74b8f0971
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944934"
---
# <a name="cash-register-functionality-for-norway"></a>Kasseapparatfunktionalitet til Norge

[!include[banner](../includes/banner.md)]

Dette emne indeholder en oversigt over kasseapparatfunktionaliteten, der er tilgængelig for Norge i Dynamics 365 Commerce. Det indeholder også retningslinjer for opsætning af funktionen. Funktionaliteten består af følgende dele:

- Almindelige POS-funktioner, der er tilgængelige for kunder i alle lande eller områder. Af eksempler kan nævnes en indstilling, der giver dig mulighed for at forhindre, at en kopi af en kvittering udskrives mere end én gang.
- Norgesspecifikke funktioner som f.eks. digitale signaturer for salgstransaktioner.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Oversigt over kasseapparatfunktionalitet til Norge

### <a name="common-pos-features"></a>Almindelige POS-funktioner

Du kan få mere at vide om POS-funktioner, der er tilgængelige for kunder i alle lande eller områder, i [Hjælp-ressourcer til Dynamics 365 Retail](../index.md).

Følgende funktioner til POS-lokalisering, der tidligere blev implementeret og gjort tilgængelige for kunder i alle lande eller områder, kan nu bruges specifikt til Norge:

- **Udskriv tekstfelter på en kvittering med en stor skriftstørrelse.** Du kan bruge parameteren **Skriftstørrelse** i designeren til kvitteringsformat til at angive, at den store skriftstørrelse skal bruges til et felt i kvitteringsformatet. (Den store skriftstørrelse er ca. det dobbelte af den normale skriftstørrelse). Du kan f.eks. bruge denne parameter til at udskrive indikatoren "Kopi" på en kopi af en kvittering med store bogstaver.
- **Registrer udskrivningen af kvitteringskopier i POS-revisionslog.** Du kan bruge parameteren **Revision** i POS-funktionsprofilen til at aktivere udskrivning af kvitteringskopier og andre POS-revisionshændelser, der skal registreres. Revisionshændelser registreres i kanaldatabasen og i Headquarters. Du kan få vist revisionshændelser på siden **Revisionshændelser**.
- **Undgå, at en kopi af en kvittering udskrives mere end én gang.** Når parameteren **Revision** i POS-funktionsprofilen er aktiveret, styrer POS-tilladelsen **Tillad udskrivning af kvitteringskopier**, om kopier af kvitteringer kan udskrives. Der findes også en indstilling, der giver dig mulighed for at forhindre, at en kopi af en kvittering udskrives mere end én gang.

Desuden er følgende POS-funktion implementeret for Norge, men den er tilgængelig for kunder i alle lande eller områder:

- **Registrer yderligere hændelser i POS-revisionsloggen.** Hvis parameteren **Revision** i POS-funktionsprofilen er aktiveret, registreres følgende hændelser i POS-revisionsloggen:

    - Pristjek
    - Momsændringer
    - Rettelser af linjeantal
    - Fjernelse af transaktioner fra kanaldatabasen

### <a name="norway-specific-pos-features"></a>Norgesspecifikke POS-funktioner

Følgende POS-funktioner, der er specifikke for Norge, aktiveres, når parameteren **ISO-kode** i POS-funktionsprofilen angives til **Nej**.

#### <a name="digital-signing-of-sales-transactions"></a>Digital signering af salgstransaktioner

Alle salgstransaktioner signeres digitalt. Signaturen oprettes og registreres i POS-transaktionskladden samtidig med, at transaktionen færdiggøres. Signaturen er også tilgængelig i den kladde, der eksporteres til revisionsbrug.

Kun transaktioner for kontantsalg signeres. Her er nogle eksempler på transaktioner, der er udeladt fra signeringsprocessen:

- Forudbetalinger (indbetaling på kundekonto)
- Forudbetalinger for salgsordrer (indbetaling for kundeordre)
- Udstedelse af et gavekort
- Ikke-salgstransaktioner (kassebeholdning, fjernelse af betalingsmiddel osv.)

De data, der signeres, er en tekststreng, der består af følgende datafelter. Datafelterne er adskilt af semikolon.

1. Tidligere signatur for samme POS (Et nul \[**0**\] bruges til den første transaktion).
2. Transaktionsdato
3. Posteringsklokkeslæt
4. Fortløbende signeret transaktionsnummer
5. Transaktionsbeløb inklusive moms
6. Transaktionsbeløb eksklusive moms

Ved den digitale signeringsproces bruges en RSA 1024-bit nøgle, der har hash-funktionen SHA-1 (RSA-SHA1-1024). Et certifikat, der er installeret på Commerce Scale Unit, bruges til signering. Det entydige id for certifikatet (fodaftryk) registreres sammen med signaturen.

Signaturen gemmes i butiksdatabasen og hovedkontorets database (HQ) sammen med transaktionsdataene. I oversigtspanelet **Regnskabstransaktioner** på siden **Butikstransaktioner** kan du se transaktionssignaturen sammen med de transaktionsdata, der blev brugt til at generere den.

#### <a name="receipts"></a>Kvitteringer

Kvitteringer for Norge kan omfatte yderligere oplysninger, der er implementeret ved hjælp af brugerdefinerede felter:

- **Kvitteringstitel** – Du kan føje et felt til layoutet for kvitteringsformatet for at identificere kvitteringstypen. En salgskvittering indeholder f.eks. teksten "Salgskvittering".
- **Signeret transaktionsserienummer** – Det fortløbende nummer på en signeret transaktion kan vises på kvitteringen for at knytte en trykt kvittering til en digital signatur i databasen.
- **Kvitteringstotaler** – Brugerdefinerede felter for kvitteringstotaler uden ikke-salgsbeløb fra samlede transaktionsbeløb. Ikke-salgsbeløb inkluderer beløb for følgende operationer:

    - Forudbetalinger (indbetaling på kundekonto)
    - Forudbetalinger for salgsordrer (indbetaling for kundeordre)
    - Udstedelse af et gavekort
    - Tilføjelse af midler på et gavekort

#### <a name="x-and-z-reports"></a>X- og Z-rapporter

De oplysninger, der er medtaget i X- og Z-rapporter, er baseret på norske krav. **Samlede kontantsalgsbeløb** omfatter f.eks. kun beløb for kontantsalgstransaktioner og udelader udstedelse af gavekorthandlinger og forudbetalinger. Det samlede kontantsalg angives også for hver varegruppe og betalingsmetode. Akkumulerede **Samlede salg** og **Samlede returneringer** vil desuden blive vedligeholdt og udskrevet.

#### <a name="saf-t-cash-register-audit-file"></a>Revisionsfil til SAF-T_kasseapparatet

Du kan eksportere POS-transaktionskladden i det foruddefinerede SAF-T-format (Standard Audit File – Tax) til kasseapparater. Revisionsfilen indeholder oplysninger om organisationen, relevante masterdata (f.eks. varegrupper, varer og momskoder), data om kontantsalgstransaktioner sammen med signaturer for disse transaktioner, rapportdata, der ikke er salgshændelser, og slutdatorapportdata.

Revisionsfilen kan eksporteres til følgende scenarier:

- Pr. butik
- Alle butikker
- Pr. terminal
- Alle terminaler

Du kan også sende en rapport fra én juridisk enhed på vegne af en anden juridisk enhed. I dette tilfælde skal du køre eksporten fra den juridiske driftsenhed og angive den juridiske rapporteringsenhed som afsender af rapporten.

SAF-T-kasseapparatformatet implementeres i Headquarters ved hjælp af [elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md). 

## <a name="setting-up-commerce-for-norway"></a>Konfigurere Commerce for Norge

I dette afsnit beskrives de indstillinger, der er specifikke for og anbefales for Norge. Du kan finde flere oplysninger i [Hjælp-ressourcer for Dynamics 365 Retail](../index.md).

Hvis du vil bruge den Norgesspecifikke funktion, skal du udføre disse opgaver:

- Angiv feltet **Land/område** til **NOR** (Norge) i den juridiske enheds primære adresse.
- I ISO-funktionalitetsprofilen for alle butikker i Norge skal du angive feltet **POS-kode** til **NO** (Norge).

Du skal også angive følgende indstillinger for Norge.

### <a name="set-up-the-legal-entity"></a>Konfigurere den juridiske enhed

Kontrollér, at navnet på den juridiske enhed er angivet. Dette navn udskrives på X- og Z-rapporter.

Angiv også organisationsnummeret i oversigtspanelet **Bankkontooplysninger** i feltet **Registreringsnummer**.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Konfigurere moms pr. norske krav


Du skal oprette momskoder, momsgrupper og varemomsgrupper. Du skal også angive momsoplysninger for produkter og tjenester. Du kan finde flere oplysninger om opsætning og brug af moms under [Momsoversigt](../../finance/general-ledger/indirect-taxes-overview.md).

Du skal også angive momsgrupper og aktivere indstillingen **Priserne inkluderer moms** for butikker, der ligger i Norge.

### <a name="set-up-functionality-profiles"></a>Konfigurere funktionalitetsprofiler

Du skal aktivere revision og konfigurere kvitteringsnummerering.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>Opdatere POS-rettighedsgrupper og individuelle rettighedsindstillinger for butiksmedarbejdere

Angiv rettigheden **Tillad udskrivning af kvitteringskopi** til en relevant værdi:

- **Tillad altid** – Operatøren kan udskrive en kopi af en kvittering flere gange.
- **Tillad kun én gang** – Operatøren kan kun udskrive en kopi af en kvittering én gang.
- **Tillad kun én gang, og kun hvis HQ DB er tilgængelig** – Operatøren kan kun udskrive en kopi af en kvittering én gang, og kun hvis HQ-databasen er tilgængelig via Commerce Data Exchange: Realtidsservice, så systemet kan kontrollere, at der tidligere ikke er udskrevet kopier af kvitteringen i en butik.
- **Aldrig** – Operatøren kan ikke udskrive en kopi af en kvittering.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurere brugerdefinerede felter, så de kan bruges i kvitteringsformater for salgskvittering

På siden **Sprogtekst** kan du tilføje følgende poster for etiketterne i de brugerdefinerede felter til kvitteringslayout. Bemærk, at værdierne for **Sprog-id**, **Tekst-id** og **Tekst**, der vises i tabellen, kun er eksempler. Du kan nemt ændre dem, så de opfylder dine behov.

| Sprog-id | Tekst                   | Tekst-id |
|-------------|------------------------|---------|
| en-US       | Titel på kvittering          | 900011  |
| en-US       | Er gavekort           | 900012  |
| en-US       | I alt (salg)          | 900013  |
| en-US       | Moms i alt (salg)      | 900014  |
| en-US       | I alt inkl. moms (salg) | 900015  |
| en-US       | Momsbeløb (salg)     | 900016  |
| en-US       | Kontanttransaktions-id    | 900017  |

På siden **Brugerdefinerede felter** kan du tilføje følgende poster for de brugerdefinerede felter til kvitteringslayout. Bemærk, at værdier for **Tekst-id for billedtekst** skal svare til de værdier for **Tekst-id**, som du har angivet på siden **Sprogtekst**.

| Navn                            | Type    | Tekst-id for billedtekst |
|---------------------------------|---------|-----------------|
| ReceiptTitle                    | Kvittering | 900011          |
| IsGiftCard                      | Kvittering | 900012          |
| SalesTotalExt                   | Kvittering | 900013          |
| TaxTotalExt                     | Kvittering | 900014          |
| TotalWithTaxExt                 | Kvittering | 900015          |
| AmountPerTaxExt                 | Kvittering | 900016          |
| CashTransactionSequentialNumber | Kvittering | 900017          |

> [!NOTE]
> Det er vigtigt, at du angiver korrekte brugerdefinerede feltnavne, som vist i ovenstående tabel. Et forkert felt medfører, at der mangler data ved i kvitteringer.

### <a name="configure-receipt-formats"></a>Konfigurere kvitteringsformater

For hvert påkrævet kvitteringsformat skal du ændre værdien i feltet **Udskriftsfunktion** til **Udskriv altid**.

I designeren til kvitteringsformater skal du føje følgende brugerdefinerede felter til de relevante kvitteringssektioner. Bemærk, at feltnavnene svarer til de sprogtekster, du har defineret i forrige afsnit.

1. Sidehoved:

    - **Kvitteringstitel** – I dette felt identificeres typen af kvittering.
    - **Kontanttransaktions-id** – Dette felt udskriver løbenummeret på den signerede kontanttransaktion.

2. Linjer:

    - **Er gavekort** – Dette felt markerer kvitteringslinjen som relateret til udstedelse af gavekort eller tilføjelse på gavekort.

3. Sidefod:

    - **Total (salg)** – Dette felt udskriver kvitteringens samlede kontantsalgsbeløb. Beløbet er uden moms. Forudbetalinger og gavekorthandlinger er ikke medtaget.
    - **Samlet moms (salg)** – Dette felt udskriver kvitteringens samlede momsbeløb for kontantsalg. Forudbetalinger og gavekorthandlinger er ikke medtaget.
    - **Total med moms (salg)** – Dette felt udskriver kvitteringens samlede kontantsalgsbeløb. Beløbet inkluderer moms. Forudbetalinger og gavekorthandlinger er ikke medtaget.
    - **Momsbeløb (salg)** – Dette felt udskriver kvitteringens momsbeløb for kontantsalg pr. momskode. Forudbetalinger og gavekorthandlinger er ikke medtaget.

Du kan finde flere oplysninger om, hvordan du arbejder med kvitteringsformater, i [Konfigurere og designe kvitteringsformater](../receipt-templates-printing.md).

### <a name="configure-the-saf-t-cash-register-export-format"></a>Konfigurere eksportformatet for SAF-T-kasseapparatet

Konfigurationen af SAF-T-kasseapparatet kan hentes fra Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger under [Importere konfigurationer for elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md). Download følgende konfigurationer:

- **Retail-kanaldata.version.1** – Konfiguration af datamodellen.
- **DMM Retail-kanaldata.version.1.14** – Konfiguration af datamodeltilknytning.
- **NO SAF T-kasseapparatet.version.1.20** – Formatkonfigurationen.

Når du har importeret konfigurationerne, skal du vælge navnet på den formatkonfiguration, der blev importeret, i feltet **Eksportformat for SAF-T-kasseapparat** på siden **Commerce-parametre** under fanen **Elektroniske dokumenter**.

Du skal også knytte påkrævede masterdata til foruddefinerede SAF-T-standardkoder. Yderligere oplysninger finder du i dokumentationen til SAF-T-kasseapparatet fra den norske skattemyndighed. Hvis du vil oprette tilknytningen, skal du angive det nye felt **SAF-T-kasseapparatkode** på følgende sider:

- Varegrupper
- Betalingsmetoder
- Momskoder

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

Hvis du vil aktivere den Norgesspecifikke funktionalitet, skal du konfigurere kanalkomponenter. Yderligere oplysninger finder du i [Retningslinjer for installation](emea-nor-fi-deployment.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
