---
title: Justere et ER-format for at oprette et brugerdefineret elektronisk dokument
description: Denne artikel forklarer, hvordan du justerer et elektronisk rapporteringsformat (ER) fra Microsoft og opretter et brugerdefineret elektronisk dokument.
author: kfend
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314,  ""intro-internal
ms.assetid: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
ms.openlocfilehash: 8b0bcdbd011c4c04e2693a3dcb8033c3cbe2adc7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283552"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>Justere et ER-format for at oprette et brugerdefineret elektronisk dokument

[!include[banner](../includes/banner.md)]

Procedurerne i denne artikel forklarer, hvordan en bruger med rollen Systemadministrator eller Funktionel konsulent i elektronisk rapportering kan udføre disse opgaver:

- Konfigurer parametre for den [Elektroniske rapporteringsstruktur (ER)](general-electronic-reporting.md).
- Importer ER-konfigurationer, der leveres af Microsoft, og som bruges til at generere en betalingsfil, mens en [kreditorbetaling](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) behandles.
- Opret en brugerdefineret version af en standardkonfiguration af ER-format, der leveres af Microsoft.
- Rediger den brugerdefinerede konfigurationen af ER-format, så det genererer betalingsfiler, der opfylder kravene i en bestemt bank.
- Anvend de ændringer, der er foretaget i konfiguration af standard-ER-formatet, i konfigurationen af det brugerdefinerede ER-format.

Alle de følgende procedurer kan udføres i **GBSI**-virksomheden. Der kræves ingen kodning.

- [Konfigurere ER-strukturen](#ConfigureFramework)

    - [Konfigurere ER-parametre](#ConfigureParameters)
    - [Aktivere en udbyder af ER-konfigurationer](#ActivateProvider)

        - [Gennemse listen over udbydere af ER-konfigurationer](#ReviewProvidersList)
        - [Tilføje en ny udbyder af ER-konfigurationer](#ActivateProvider)
        - [Aktivere en udbyder af ER-konfigurationer](#ActivateAddedProvider)

- [Importere standardkonfigurationer af ER-format](#ImportERSolution1)

    - [Importere standardkonfigurationer af ER](#ImportERFormat1)
    - [Gennemse de importerede ER-konfigurationer](#ReviewImportedERSolution)

- [Klargøre en kreditorbetaling til behandling](#PrepareVendorPayment)

    - [Tilføj bankoplysninger for kreditorkonto](#AddBankAccount)
    - [Angive en kreditorbetaling](#EnterVendorPayment)

- [Behandle kreditorbetaling ved hjælp af standard-ER-formatet](#ProcessVendorPayment1)

    - [Konfigurere den elektroniske betalingsmåde](#ConfigureMethodOfPayment1)
    - [Behandle en kreditorbetaling](#ProcessPayment1)

- [Tilpasse standard-ER-formatet](#CustomizeProvidedFormat)

    - [Oprette et brugerdefineret format](#DeriveProvidedFormat)
    - [Redigere et brugerdefineret format](#ConfigureDerivedFormat)
    - [Markere et brugerdefineret format som kørbart](#MarkFormatRunnable)

- [Behandle kreditorbetaling ved hjælp af det brugerdefinerede ER-format](#ProcessVendorPayment2)

    - [Konfigurere den elektroniske betalingsmåde](#ConfigureMethodOfPayment2)
    - [Behandle en kreditorbetaling](#ProcessPayment2)

- [Importere nye version af standardkonfigurationer af ER-format](#ImportERSolution2)

    - [Importere nye version af standardkonfigurationer af ER](#ImportERFormat2)
    - [Gennemse de importerede ER-formatkonfigurationer](#ReviewImportedERFormat)

- [Anvende ændringerne i den nye version af et importeret format i et brugerdefineret format](#AdoptNewBaseVersion)

    - [Fuldføre den aktuelle kladdeversion af et brugerdefineret format](#CompleteDerivedFormat)
    - [Basere et brugerdefineret format på en ny basisversion](#RebaseDerivedFormat)
    - [Behandle kreditorbetaling ved hjælp af et ER-format med ny base](#ProcessPayment3)

- [Yderligere ressourcer](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>Konfigurere ER-strukturen

Som bruger i rollen Funktionel konsulent i elektronisk rapportering skal du konfigurere det minimale sæt med ER-parametre, før du kan begynde at bruge ER-strukturen til at designe en brugerdefineret version af standard-ER-formatet.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfigurere ER-parametre

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.
3. På siden **Parametre til elektronisk rapportering** under fanen **Generelt** skal du vælge **Ja** i indstillingen **Aktiver designtilstand** .
4. På fanen **Vedhæftede filer** kan du angive følgende parametre:

    - I feltet **Konfigurationer** skal du vælge typen **Fil** for **USMF**-virksomheden.
    - I felterne **Jobarkiv**, **Midlertidig**, **Grundlag** og **Andre** skal du vælge typen **Fil**.

Du kan finde flere oplysninger om ER-parametre under [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivere en udbyder af ER-konfigurationer

Alle ER-konfigurationer, der tilføjes, er markeret som ejet af en udbyder af ER-konfigurationer. Den udbyder af ER-konfigurationer, der aktiveres i arbejdsområdet **Elektronisk rapportering**, bruges til dette formål. Du skal derfor aktivere en udbyder af ER-konfigurationer i arbejdsområdet **Elektronisk rapportering**, før du begynder at tilføje eller redigere ER-konfigurationer.

> [!NOTE]
> Det er kun ejeren af en ER-konfiguration, der kan redigere den. Før du kan redigere en ER-konfiguration, skal den relevante udbyder af ER-konfiguration aktiveres i arbejdsområdet **Elektronisk rapportering**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Gennemse listen over udbydere af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.
3. På siden **Tabel over konfigurationsudbydere** har hver udbyderpost et entydigt navn og en entydig URL-adresse. Gennemse indholdet af denne side. Hvis der allerede findes en post for **Litware, Inc.** (`https://www.litware.com`), skal du springe den næste procedure over, [Tilføje en ny udbyder af ER-konfigurationer](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Tilføje en ny udbyder af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.
3. På siden **Konfigurationsudbydere** skal du vælge **Ny**.
4. I feltet **Navn** skal du angive **Litware, Inc.**
5. I feltet **Internetadresse** skal du angive `https://www.litware.com`.
6. Vælg **Gem**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivere en udbyder af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Gå til siden **Lokaliseringskonkfigurationer**, og vælg feltet **Litware, Inc.** i sektionen **Konfigurationsudbydere**, og vælg derefter **Angiv som aktive**.

Få flere oplysninger om udbydere af ER-konfigurationer under [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Importere standardkonfigurationer af ER-format

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>Importere standardkonfigurationer af ER

Hvis du vil føje ER-standardkonfigurationerne til din aktuelle forekomst af Microsoft Dynamics 365 Finance, skal du importere dem fra det [ER-lager](general-electronic-reporting.md#Repository), der er konfigureret for den pågældende forekomst.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du i sektionen **Konfigurationsudbydere** vælge feltet **Microsoft** og derefter vælge **Lagre** for at få vist listen over lagre for Microsoft-udbyderen.
3. På siden **Konfigurationslagre** skal du vælge lageret for **Global**-typen og derefter vælge **Åbn**. Hvis du bliver bedt om at angive godkendelse for at oprette forbindelse til Regulatory Configuration Service, skal du følge godkendelsesvejledningen.
4. På siden **Konfigurationslager** skal du i konfigurationstræet i venstre rude vælge formatkonfigurationen **BACS (Storbritannien)**.
5. I oversigtspanelet **Versioner** skal du vælge version **1.1** for den valgte ER-formatkonfiguration.
6. Vælg **Importér** for at hente den valgte version fra Global-lageret til den aktuelle Finans-forekomst.

![Siden Konfigurationslager.](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> Hvis du har problemer med at få adgang til det [globale lager](er-download-configurations-global-repo.md), kan du [hente konfigurationer](download-electronic-reporting-configuration-lcs.md) fra Microsoft Dynamics Lifecycle Services (LCS) i stedet.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Gennemse de importerede ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel**.
4. Bemærk, at der ud over det valgte **BACS (Storbritannien)**-format, blev importeret andre krævede ER-konfigurationer. Kontroller, at følgende ER-konfigurationer er tilgængelige i konfigurationstræet:

    - **Betalingsmodel** – Denne konfiguration indeholder den datamodel, der repræsenterer datastrukturen for betalingsforretningsdomænet.
    - **Tilknytning af betalingsmodel 1611** – Denne konfiguration indeholder den modeltilknytning ER-komponent, der beskriver, hvordan datamodellen udfyldes med applikationsdata under kørsel.
    - **BACS (Storbritannien)** – Denne konfiguration indeholder format og formattilknytnings-ER-komponenter. Formatkomponenten angiver rapportlayoutet. Komponenten til formattilknytning indeholder modeldatakilden og angiver, hvordan rapportlayoutet angives ved hjælp af denne datakilde på kørselstidspunktet.

![Siden Konfigurationer med de angivne ER-konfigurationer, der er tilgængelige i træet.](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>Klargøre en kreditorbetaling til behandling

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Tilføje bankoplysninger for kreditorkonto

Du skal tilføje bankoplysninger for en kreditorkonto, som der vil blive henvist til senere i en registreret betaling.

1. Gå til **Kreditor** \> **Kreditorer** \> **Alle kreditorer**.
2. På siden **Alle kreditorer** skal du vælge kreditorkontoen **GB_SI_000001**, og derefter skal du i handlingsruden på fanen **Kreditor** i gruppen **Konfigurer** vælge **Bankkonti**.
3. På siden **Kreditorbankkonti** skal du vælge **Ny** og angive derefter følgende oplysninger:

    1. Angiv **GBP OPER** i feltet **Bankkonto**.
    2. Vælg **BankGBP** i feltet **Bankgrupper**.
    3. Angiv **202015** i feltet **Bankkontonummer**.
    4. I feltet **SWIFT-kode** skal du angive <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.
    5. I feltet **IBAN** skal du angive **GB33BUKB20201555555555**.
    6. I feltet **Registreringsnummer** skal du beholde standardværdien <a id="DefineRoutingNumber"></a>**123456**.

    ![Siden Kreditorbankkonti.](./media/er-quick-start2-bank-account.png)

4. Vælg **Gem**.
5. Luk siden.
6. På siden **Alle kreditorer** skal du åbne kreditorkontoen **GB_SI_000001**.
7. På siden Kreditordetaljer skal du vælge **Rediger** for at gøre siden redigerbare, hvis det er nødvendigt.
8. I oversigtspanelet **Betaling** skal du i feltet **Bankkonto** vælge **GBP OPER**.

    ![Siden Kreditordetaljer.](./media/er-quick-start2-bank-account-reference.png)

9. Vælg **Gem**.
10. Luk siden.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Angive en kreditorbetaling

Du skal angive en ny kreditorbetaling ved hjælp af et [betalingsforslag](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).

1. Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.
2. På siden **Kreditorbetalingskladde** skal du vælge **Ny**.
3. Vælg **VendPay** i feltet **Navn**.
4. Vælg **Linjer**.
5. Vælg **Betalingsforslag** \> **Opret betalingsforslag**.
6. I dialogboksen **Kreditorbetalingsforslag** skal du konfigurere betingelser, der kun filtrerer efter poster for kreditorkontoen **GB_SI_000001**, og derefter vælge **OK**.
7. Marker linjen for fakturaen **00000007_Inv**, og vælg derefter **Opret betaling**.

    ![Dialogboksen Kreditorbetalingsforslag.](./media/er-quick-start2-payment-proposal.png)

8. Kontroller, at den angivne betaling er konfigureret til at bruge den **elektroniske** betalingsmåde.

    ![Side med leverandørbetalinger.](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Behandle kreditorbetaling ved hjælp af standard-ER-formatet

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>Konfigurere den elektroniske betalingsmåde

Du skal konfigurere den elektroniske betalingsmåde, så den bruger den importeret ER-formatkonfiguration.

1. Gå til **Kreditor** \> **Opsætning af betaling** \> **Betalingsmåder**.
2. Gå til siden **Betalingsmetoder – kreditorer**, og vælg den **elektroniske** betalingsmetode i venstre rude.
3. Vælg **Rediger**.
4. I oversigtspanelet **Filformater** til at angive indstillingen **Generelt elektronisk eksportformat** til **Ja**.
5. I feltet **Eksportér formatkonfiguration** skal du vælge formatkonfigurationen **BACS (Storbritannien)**.

    ![Betalingsmåder – kreditorer til opsætning af elektronisk betalingsmåde til behandling af kreditorbetalinger i et standardformat.](./media/er-quick-start2-method-of-payment1.png)

6. Vælg **Gem**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Behandle en kreditorbetaling

1. Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.
2. På siden **Kreditorbetalingskladde** skal du vælge den betalingskladde, du tilføjede tidligere, og derefter vælge **Linjer**.
3. Vælg **Generer betalinger** på siden **Kreditorbetalinger**.
4. I dialogboksen **Opret betalinger** skal du angive følgende oplysninger:

    - Vælg **Elektronisk** i feltet **Betalingsmåde**.
    - Vælg **GBSI OPER** i feltet **Bankkonto**.

5. Vælg **OK**.
6. I dialogboksen **Parametre til elektronisk rapportering** skal du angive indstillingen **Udskriv kontrolrapport** til **Ja** og derefter vælge **OK**.

    ![Siden med dialogboksen Parametre til elektronisk rapportering.](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > Ud over betalingsfilen kan du nu oprette kontrolrapporten.

7. Hent zip-filen, og udtræk derefter følgende filer fra den:

    - Kontrolrapporten i Excel-format
    - Betalingsfilen i TXT-format

        Bemærk, at i overensstemmelse med [strukturen](#PositionRoutingNumber) i det angivne ER-format starter betalingslinjen i den genererede fil med det registreringsnummer, der blev [defineret](#DefineRoutingNumber) for den konfigurerede bankkonto.

        ![Betalingsfil i TXT-format.](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Tilpasse standard-ER-formatet

I eksemplet, der vises i dette afsnit, bruger du de ER-konfigurationer, der leveres af Microsoft, til at generere kreditorbetalingsfiler i BACS-format, men du skal tilføje en tilpasning for at understøtte kravene til en bestemt bank. Det er også en god ide at opgradere det brugerdefinerede format, når nye versioner af ER-konfigurationer bliver tilgængelige. Du vil dog være i stand til at opgradere til den laveste omkostning.

I dette tilfælde skal du som repræsentant for Litware, Inc. oprette (aflede) en ny standard-ER-formatkonfiguration ved at bruge konfigurationen leveret af **BACS (Storbritannien)** Microsoft som basis.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Oprette et brugerdefineret format

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **BACS (Storbritannien)**. Litware, Inc. vil bruge version 1.1 af denne ER-formatkonfiguration som basis for den brugerdefinerede version.
3. Vælg **Opret konfiguration** for at åbne dialogboksen med rullemenu. Du kan bruge denne dialogboks til at oprette en ny konfiguration for et brugerdefineret betalingsformat.
4. I feltet **Ny** skal du vælge indstillingen **Afledt fra navn: BACS (Storbritannien), Microsoft**.
5. Angiv **BACS (UK – brugerdefineret )** i feltet **Navn**.

    ![Dialogboks til rulleliste Opret konfiguration.](./media/er-quick-start2-add-derived-format.png)

6. Vælg **Opret konfiguration**.

Version 1.1.1 af **BACS (UK – brugerdefineret)** ER-formatkonfiguration er oprettet. Denne version har statussen **Kladde** og kan redigeres. Det aktuelle indhold af det brugerdefinerede ER-format svarer til indholdet af det format, der er leveret af Microsoft.

![Konfigurationsside med Version 1.1.1 af BACS (UK – brugerdefineret) ER-formatkonfiguration.](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Redigere et brugerdefineret format

Du skal konfigurere det brugerdefinerede format, så det opfylder de bankspecifikke krav. En bank kan f.eks. kræve, at betalingsfiler, der genereres, omfatter EU-koden til SWIFT-koden (Society for Worldwide Interbank Financial Telecommunication) for den bank, der er tildelt agentrollen i den behandlede kreditorbetaling. SWIFT-koder er internationale bankkoder, der identificerer specifikke banker verden over. De kaldes også BIC'er (Bank Identifier Codes). SWIFT-koden skal indeholde 11 tegn, og den skal angives i begyndelsen af hver betalingslinje i en genereret betalingsfil.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **BACS (UK brugerdefineret)**.
3. I oversigtspanelet **Versioner** skal du vælge version **1.1.1** for den valgte konfiguration.
4. Vælg **Designer**.
5. På siden **Formatdesigner** skal du vælge **Vis detaljer** for at få vist flere oplysninger om formatelementerne.
6. Udvid og gennemse følgende elementer:

    - Elementet **BACSReportsFolder** typen **Mappe**. Dette element bruges til at oprette output i ZIP-format.
    - Elementet **Fil** for typen **Fil**. Dette element bruges til at oprette en betalingsfil i TXT-format.
    - Elementet **Transaktioner** for typen **Rækkefølge**. Dette element bruges til at oprette en enkelt betalingslinje i en betalingsfil.
    - Elementet **Transaktion** for typen **Rækkefølge**. Dette element bruges til at oprette individuelle felter for en enkelt betalingslinje.

7. Vælg elementet **Transaktion**.

    ![Transaktionselementet i ER-operationsdesigneren.](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Den leverede rapport konfigureres, så <a id="PositionRoutingNumber"></a>alle betalingslinjer starter med bankens registreringsnummer. Formatelementet **vendBankRouteNum** bruges til dette formål. 

8. Vælg **Tilføj**, og vælg derefter typen **Tekst\\Streng** for det formatelement, du vil tilføje:

    1. I feltet **Navn** skal du angive **vendBankSWIFT**.
    2. Angiv **11** i feltet **Minimumlængde**.
    3. Angiv **11** i feltet **Maksimumlængde**.
    4. Vælg **OK**.

    > [!NOTE]
    > Elementet **vendBankSWIFT** bruges til at angive SWIFT-koden for en kreditors bank i genererede filer.

9. Vælg **vendBankSWIFT** i formattræstrukturen.
10. Vælg **Flyt op** for at flytte det valgte formatelement et niveau op. Gentag dette trin, indtil elementet **vendBankSWIFT** er det <a id="PositionSWIFTCode"></a>første element under det overordnede element **transaktion**.

    ![VendBankSWIFT som det første element under transaktion i ER-operationsdesigner.](./media/er-quick-start2-derived-format1.png)

11. Mens **vendBankSWIFT** stadig er markeret i formatets strukturtræ, skal du vælge fanen **Tilknytning** og derefter udvide datakilden **model**.
12. Udvid **model.Payment** \> **model.Payment.CreditorAgent**, og vælg datakildefeltet **model.Payment.CreditorAgent.BICFI**. Dette datakildefelt viser SWIFT-koden for en kreditorbank, der er tildelt agentrollen i den behandlede kreditorbetaling.
13. Vælg **Bind**. Formatelementet **VendBankSWIFT** er nu bundet sammen med datakildefeltet **model.Payment.CreditorAgent.BICFI**, så SWIFT-koderne angives i genererede betalingsfiler.

    ![vendBankSWIFT-formatelement, der er bundet til datakildefeltet model.Payment.CreditorAgent.BICFI, er i ER-operationsdesigner.](./media/er-quick-start2-derived-format2.png)

14. Vælg **Gem**.
15. Luk designersiden.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Markere et brugerdefineret format som kørbart

Nu, hvor den første version af det brugerdefinerede format er blevet oprettet og har statussen **Kladde**, kan du køre den til testformål. Hvis du vil køre rapporten, skal du behandle en kreditorbetaling ved hjælp af den betalingsmåde, der refererer til det brugerdefinerede ER-format. Som standard er det kun versioner, der har statussen **Fuldført** eller **Delt**, der tages i betragtning, når du kalder et ER-format fra applikationen. Denne funktionsmåde er med til at forhindre, at ER-formater med uafsluttede design bliver brugt. Men når det gælder dine testkørsler, kan du tvinge programmet til at bruge den version af dit ER-format, der har statussen **Kladde**. På denne måde kan du justere den aktuelle formatversion, hvis der kræves ændringer. Du kan finde flere oplysninger under [Anvendelighed](electronic-reporting-destinations.md#applicability).

Hvis du vil bruge kladdeversionen af et ER-format, skal du eksplicit markere ER-formatet.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. I dialogboksen **Brugerparametre** skal du angive indstillingen **Kørselsindstillinger** til **Ja** og derefter vælge **OK**.
4. Vælg **Rediger** for at gøre den aktuelle side redigerbar efter behov.
5. Vælg **BACS (UK brugerdefineret)** i konfigurationstræet i ruden til venstre.
6. Angiv indstillingen **Kør kladde** til **Ja**.

    ![Indstillingen Kør kladde på siden Konfigurationer.](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Behandle kreditorbetaling ved hjælp af det brugerdefinerede ER-format

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>Konfigurere den elektroniske betalingsmåde

Du skal konfigurere den elektroniske betalingsmåde, så det brugerdefinerede ER-format bruges til at behandle kreditorbetalinger.

1. Gå til **Kreditor** \> **Opsætning af betaling** \> **Betalingsmåder**.
2. Gå til siden **Betalingsmetoder – kreditorer**, og vælg den **elektroniske** betalingsmetode i venstre rude.
3. Vælg **Rediger**.
4. I oversigtspanelet **Filformat** til at angive indstillingen **Generelt elektronisk eksportformat** til **Ja**.
5. I feltet **Eksportér formatkonfiguration** skal du vælge formatkonfigurationen **BACS (UK brugerdefineret)**.

    ![Betalingsmåder – kreditorer til opsætning af elektronisk betalingsmåde til behandling af kreditorbetalinger i et brugerdefineret format.](./media/er-quick-start2-method-of-payment2.png)

6. Vælg **Gem**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Behandle en kreditorbetaling

1. Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.
2. På siden **Kreditorbetalingskladde** skal du vælge den betalingskladde, du oprettede tidligere.
3. Vælg **Linjer**.
4. Gå til siden **Kreditorbetalinger**, og vælg **Betalingsstatus** \> **Ingen** over gitteret.
5. Vælg **Generer betaling**.
6. I dialogboksen **Opret betalinger** skal du angive følgende oplysninger:

    - Vælg **Elektronisk** i feltet **Betalingsmåde**.
    - Vælg **GBSI OPER** i feltet **Bankkonto**.

7. Vælg **OK**.
8. I dialogboksen **Parametre til elektronisk rapportering** skal du angive indstillingen **Udskriv kontrolrapport** til **Ja** og derefter vælge **OK**.

    > [!NOTE]
    > Ud over betalingsfilen kan du kun oprette kontrolrapporten.

9. Hent zip-filen, og udtræk derefter følgende filer fra den:

    - Kontrolrapporten i Excel-format
    - Betalingsfilen i TXT-format

        Bemærk, at betalingslinjen i den genererede fil nu [starter](#PositionSWIFTCode) med den SWIFT-kode, der blev [angivet](#DefineSWIFTCode) for bankkontoen for den kreditor, hvor betalingen er behandlet, i overensstemmelse med strukturen i det brugerdefinerede ER-format.

        ![Den betalingsfil i TXT-format, der bruges til behandling af kreditorbetalingen.](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Importere nye version af standardkonfigurationer af ER-format

I eksemplet, der vises i dette afsnit, modtager du en meddelelse om vidensdatabaseartikel [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046). Denne besked oplyser dig om den nye version af ER-formatet **BACS (Storbritannien)**, der er udgivet af Microsoft. Ud over kontrolrapporten lader denne nye version brugere oprette betalingsadviseringsrapporten og rapporten over mødenotater, mens en kreditorbetaling behandles. Det er en funktion, du vil blive glad for.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Importere nye version af standardkonfigurationer af ER

Hvis du vil tilføje nye versioner af ER-konfigurationerne til den aktuelle Finans-forekomst, skal du importere dem fra ER-[lageret](general-electronic-reporting.md#Repository), som du har konfigureret.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du i sektionen **Konfigurationsudbydere** vælge feltet **Microsoft** og derefter vælge **Lagre** for at få vist listen over lagre for Microsoft-udbyderen.
3. På siden **Konfigurationslagre** skal du vælge lageret for **Global**-typen og derefter vælge **Åbn**. Hvis du bliver bedt om at angive godkendelse for at oprette forbindelse til Regulatory Configuration Service, skal du følge godkendelsesvejledningen.
4. På siden **Konfigurationslager** skal du i konfigurationstræet i venstre rude vælge formatkonfigurationen **BACS (Storbritannien)**.
5. I oversigtspanelet **Versioner** skal du vælge version **3.3** for den valgte ER-formatkonfiguration.
6. Vælg **Importér** for at hente den valgte version fra Global-lageret til den aktuelle Finans-forekomst.

![Siden Konfigurationslager, oversigtspanelet Versioner, knappen Import.](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> Hvis du har problemer med at få adgang til det [globale lager](er-download-configurations-global-repo.md), kan du i stedet [hente konfigurationer](download-electronic-reporting-configuration-lcs.md) fra LCS i stedet.

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>Gennemse de importerede ER-formatkonfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **BACS (Storbritannien)**.
4. I oversigtspanelet **Versioner** skal du vælge version **3.3**.
5. Vælg **Designer**.
6. Gå til siden **Formatdesigner**, udvid formatelementet **BACSReportsFolder**.
7.  Bemærk, at version 3.3 indeholder det formatelementet **PaymentAdviceReport**, der bruges til at generere en betalingsadviseringsrapport, når en kreditorbetaling behandles.

    ![PaymentAdviceReport-formatet i ER-operationsdesigneren.](./media/er-quick-start2-imported-solution2.png)

8. Luk designersiden.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>Anvende ændringerne i den nye version af et importeret format i et brugerdefineret format

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>Fuldføre den aktuelle kladdeversion af et brugerdefineret format

Hvis du vil beholde den aktuelle tilstand for det brugerdefinerede format, skal du fuldføre kladdeversion 1.1.1 ved at ændre dens status fra **Kladde** til **Fuldført**.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **BACS (Storbritannien)** og derefter vælge **BACS (UK brugerdefineret)**.
4. I oversigtspanelet **Versioner** skal du vælge **Skift status** \> **Fuldfør** og derefter vælge **OK**.

Statussen for version 1.1.1 ændres fra **Kladde** til **Fuldført**, og versionen bliver skrivebeskyttet. Der er tilføjet en ny redigerbar version, 1.1.2, som har statussen **Kladde**. Du kan bruge denne version til at foretage yderligere ændringer i det brugerdefinerede ER-format.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Basere et brugerdefineret format på en ny basisversion

Hvis du vil begynde at bruge den nye funktionalitet i version 3.3 af formatet **BACS (Storbritannien)** i tilpasningen, skal du ændre den grundlæggende konfigurationsversion for den brugerdefinerede konfiguration, **BACS (Storbritannien)**. Denne proces kaldes [rebasering](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase). I stedet for version 1.1 af **BACS (Storbritannien)** skal du bruge version 3.3.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **BACS (UK brugerdefineret)**.
3. I oversigtspanelet **Versioner** skal du vælge version **1.1.2** og derefter **Rebasér**.
4. I dialogboksen **Rebasér** skal du i feltet **Målversion** vælge version **3.3** af basiskonfiguration for at anvende den som den ny base og bruge den til at opdatere konfigurationen.

    ![Dialogboksen Rebasér.](./media/er-quick-start2-rebase1.png)

5. Vælg **OK**.
6. Bemærk, at nummeret på kladdeversionen er ændret fra **1.1.2** til **3.3.2**, så den afspejler ændringen i basisversionen.

    Når den brugerdefinerede version og en ny basisversion flettes, kan der blive registreret nogle konflikter på grund af formatændringer, der ikke kan flettes automatisk.

    ![Rebaseret konfiguration med konflikter på siden Konfigurationer.](./media/er-quick-start2-rebase2.png)

    Hvis der registreres konflikter, skal de løses manuelt i formatdesigneren.

7. I oversigtspanelet **Versioner** skal du vælge version **3.3.2**.
8. Vælg **Designer**.
9. Gå til siden **Formatdesigner**, og vælg en post med en rebaseringskonflikt i oversigtspanelet **Detaljer**, og vælg derefter **Anvend basisværdi**.

    ![Rebaserer konfliktpost i ER-operationsdesigner.](./media/er-quick-start2-rebase3.png)

10. Vælg **Gem**.

    Posten for rebaseringskonflikten skal ikke længere vises i oversigtspanelet **Detaljer**.

    ![Konflikt er løst i ER-operationsdesigner.](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > Du har løst konflikten ved at bekræfte, at version 3 af basismodellen skal bruges i dette ER-format.

11. Udvid **BACSReportsFolder** \> **fil** \> **transaktioner** \> **transaktion**.
12. Under fanen **Tilknytning** kan du se, at version 3.3.2 i det brugerdefinerede ER-format indeholder både din tilpasning (formatelementet **vendBankSWIFT** og dets binding) og den nye funktionalitet i version 3.3 af basis-ER-formatet, der blev angivet af Microsoft (elementformatet **PaymentAdviceReport** sammen med de indlejrede elementer og konfigurerede bindinger). Med blot nogle få klik med musen har du indført ændringerne af en ny basisversion ved at flette dem med tilpasningen.

    ![Flettet format i ER-operationsdesigner.](./media/er-quick-start2-rebase5.png)

13. Luk designersiden.

> [!NOTE]
> Rebaseringshandling kan fortrydes. Hvis du vil annullere denne rebasering, skal du vælge version **1.1.1** af formatet **BACS (UK brugerdefineret)** i oversigtspanelet **Versioner** og derefter vælge **Hent denne version**. Version 3.3.2 vil derefter blive omnummereret til 1.1.2, og indholdet af kladdeversion 1.1.2 vil svare til indholdet af version 1.1.1.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Behandle kreditorbetaling ved hjælp af et ER-format med ny base

1. Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.
2. På siden **Kreditorbetalingskladde** skal du vælge den betalingskladde, du oprettede tidligere.
3. Vælg **Linjer**.
4. Gå til siden **Kreditorbetalinger**, og vælg **Betalingsstatus** \> **Ingen** over gitteret.
5. Vælg **Generer betaling**.
6. I dialogboksen **Opret betalinger** skal du angive følgende oplysninger:

    - Vælg **Elektronisk** i feltet **Betalingsmåde**.
    - Vælg **GBSI OPER** i feltet **Bankkonto**.

7. Vælg **OK**.
8. I dialogboksen **Parametre til elektronisk rapportering** skal du angive følgende oplysninger:

    - Angiv indstillingen **Udskriv kontrolrapport** til **Ja**.
    - Angiv indstillingen **Udskriv betalingsadvisering** til **Ja**.

    ![Dialogboksen Parametre til elektronisk rapportering.](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > Ud over betalingsfilen kan du nu generere både kontrolrapporten og betalingsadviseringsrapporten.

9. Vælg **OK**.
10. Hent zip-filen, og udtræk derefter følgende filer fra den:

    - Kontrolrapporten i Excel-format
    - Betalingsadviseringsrapporten i Excel-format

        ![Betalingsadviseringsrapport i Excel-format.](./media/er-quick-start2-payment-advice-report.png)

    - Betalingsfilen i TXT-format

        Bemærk, at betalingslinjen i den genererede fil starter med den SWIFT-kode, der blev angivet for bankkontoen for den kreditor, hvor betalingen er behandlet.

        ![Den betalingsfil i TXT-format, der bruges til behandling af kreditorbetalingen ved hjælp af ER-format i ny base.](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Hente ER-konfigurationer fra Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [Hente ER/konfigurationer fra det globale lager til Konfigurationstjenesten](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
