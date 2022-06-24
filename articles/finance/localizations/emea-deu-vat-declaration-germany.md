---
title: Momsangivelse (Tyskland)
description: Denne artikel beskriver, hvordan du kan konfigurere og generere en forudgående momsopgørelse for Tyskland i det officielle XML-format.
author: anasyash
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: ff52963c03ec2eb662eb0c20ef2a960e3b999167
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879526"
---
# <a name="vat-declaration-germany"></a>Momsangivelse (Tyskland)

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du kan konfigurere og generere en forudgående momsopgørelse for Tyskland i det officielle XML-format. Denne artikel beskriver også, hvordan du kan få vist en forhåndsversion af momsopgørelsen i Microsoft Excel.

Hvis rapporten skal genereres automatisk, skal du oprette nok momskoder til at føre et separat momsregnskab for hvert felt i den forudgående momsopgørelse. Derudover skal du i de applikationsspecifikke parametre i ER-formatet for den forudgående momsopgørelse knytte momskoder til opslagsresultatet af opslagene i felterne i momsopgørelsen.

For Tyskland skal du konfigurere **opslag i rapportfelt**. Du kan finde flere oplysninger om, hvordan du konfigurerer programspecifikke parametre, i afsnittet [Konfigurere programspecifikke parametre for momsopgørelsesfelter](#set-up-application-specific-parameters-for-vat-declaration-fields) senere i denne artikel.

I tabellen nedenfor viser kolonnen "Opslagsresultat" det opslagsresultat, der er forudkonfigureret til en bestemt momsopgørelsesrække i momsopgørelsesformatet. Brug disse oplysninger til korrekt at knytte momskoder til opslagsresultatet og derefter med rækken i momsopgørelsen.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a>Oversigt over momsopgørelse

Den forudgående momsopgørelse i Tyskland indeholder følgende oplysninger.

**AFSNIT – LEVERANCER OG ANDRE TJENESTER**

**Momspligtigt salg**

| Række | Felt - momsbasis | Felt - momsbeløb | Beskrivelse                                                                                                                                      | Opslagsresultat                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Uden kode     | Momspligtigt salg til en momssats på 19 procent.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – med minusfortegn             |
| 21  | 86             | Uden kode     | Momspligtigt salg til en momssats på 7 procent.                                                                                                        | 21-TaxableSalesReduced</br>73-BadDebtsWriteOffReduced (86/50) – med minusfortegn               |
| 22  | 35             | 36               | Momspligtigt salg til andre momssatser.                                                                                                                | 22-TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – med minusfortegn      |
| 23  | 77             | *Intet momsbeløb*  | Leveringer fra landbrugs- og skovvirksomheder i overensstemmelse med §24 i lov om tysk moms (UStG) til kunder, der har et moms-id-nummer. | 23-EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – med minusfortegn |
| 24  | 76             | 80               | Salg, som skat og moms skal betales for ifølge §24 af UStG (varer, pengeprodukter, pengeprodukter og likvide midler).                                | 24-SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Momsfrit salg med indgående momsfradrag**

| Række | Felt - momsbasis | Felt - momsbeløb | Beskrivelse                                                                       | Opslagsresultat                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Intet momsbeløb*  | Leveringer inden for EU til kunder, der har et moms-id.                       | 26-EUSales                          |
| 27  | 44             | *Intet momsbeløb*  | Leveringer inden for EU af nye køretøjer til købere, der ikke har et moms-id.    | 27-EUSalesNewVehicles               |
| 28  | 49             | *Intet momsbeløb*  | Leveringer inden for EU af nye køretøjer uden for et firma.                     | 28-EUSalesNewVehiclesOutsideCompany |
| 29  | 43             | *Intet momsbeløb*  | Andre momsfrit salg med indgående momsfradrag, f.eks. eksportleverancer. | 29-ExportOtherTaxFreeSales          |

**Momsfrit salg uden indgående momsfradrag**

| Række | Felt - momsbasis | Felt - momsbeløb | Beskrivelse                                            | Opslagsresultat                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Intet momsbeløb*  | Skattefrit salg uden indgående momsfradrag. | 30-TaxFreeSalesWithoutInputTaxDeduction |

**Fællesskabsanskaffelser**

| Række | Felt - momsbasis | Felt - momsbeløb | Beskrivelse                                                                                                                   | Opslagsresultat                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Intet momsbeløb*  | Skattefrit anskaffelse af visse objekter og investeringsguld.                                                    | 33-TaxFreeEUPurchase                                             |
| 34  | 89             | Uden kode     | Skattepligtig anskaffelse inden for EU til en momssats på 19 %.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Uden kode     | Skattepligtig anskaffelse inden for EU til en momssats på 7 %.                                                              | 35-EUPurchaseReduced</br>35-UseTaxEUPurchaseReduced (93/61)          |
| 36  | 95             | 98               | Skattepligtig anskaffelse inden for EU til en anden momssats.                                                                      | 36-EUPurchaseOtherRates</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Momspligtig anskaffelse af nye køretøjer fra leverandører uden et moms-id-nummer til den generelle momssats. | 37-EUPurchaseVehicles</br>37-UseTaxEUPurchaseVehicles (94/96/61)     |

**SEKTION – MODTAGER SOM MOMSDEBITOR**

| Række | Felt - momsbasis | Felt - momsbeløb | Beskrivelse                                                                        | Opslagsresultat                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Andre tjenester, der er baseret på resten af community-området.        | 40-BeneficiaryTaxDebtor</br>40-UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Salg, der falder under section 13b (2) nr. 3 af UStG.                               | 41-BeneficiaryTaxDebtorRealEstateTransfer</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Øvrige salg, der falder under section 13b (2) nr. 1, 2 og 4 til og med 12 af UStG. | 42-BeneficiaryTaxDebtorOther</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**SEKTION – SUPPLERENDE OPLYSNINGER OM SALG**

| Række | Felt - momsbasis  | Felt - momsbeløb | Beskrivelse                                                                                                | Opslagsresultat                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Intet momsbeløb*  | Leveringer fra den første kunde i tilfælde af trekantstransaktioner inden for EU.                   | 48-DeliveriesFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Intet momsbeløb*  | Momspligtigt salg af den ydelse, som modtageren af tjenesten skylder momsen for. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Intet momsbeløb*  | Andre ikke-momspligtige ydelser.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Intet momsbeløb*  | Andet ikke-momspligtigt salg, når performance-stedet ikke er i Tyskland.                                    | 51-OtherSalesNonTaxable                                                                          |
| 52  | *Intet momsbeløb* | *Intet momsbeløb*  | Moms.                                                                                                       | Række 20 + række 21 + række 22 + række 24 + række 34 + række 35 + række 36 + række 37 + række 40 + række 41 + række 42 |

**SEKTION – FRADRAGSBERETTIGET INDGÅENDE MOMS**

| Række | Felt - momsbeløb | Beskrivelse                                                                                                | Opslagsresultat                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Indtast fakturaafgiftsbeløb fra andre firmaer, tjenester og trekantstransaktioner.     | 55-InputTax 40-UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – med minustegn                                                                   |
| 56  | 61               | Indgående momsbeløb fra anskaffelse af varer inden for EU.                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35-UseTaxEUPurchaseReduced (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37-UseTaxEUPurchaseVehicles (94/96/61) |
| 57  | 62               | Påløbne import moms.                                                                                 | 57-InputTaxImport                                                                                                                                                            |
| 58  | 67               | Indgående momsbeløb fra tjenester i betydningen §13b af UStG".                                        | 58-InputTaxServices</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Indgående momsbeløb, der beregnes i henhold til generelle gennemsnitssatser.                                  | 59-InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – med minusfortegn                                                                                    |
| 60  | 59               | Indgående momsfradrag for leveringer inden for EU af nye køretøjer uden for et firma og mindre virksomheder. | 60-InputTaxEUPurchaseNewVehicles</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37) – med minusfortegn                                                                  |
| 61  | 64               | Korrektion af indgående momsfradrag.                                                                     | 61-InputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Resterende beløb.                                                                                      | Række 52 – Række 55 – række 56 – række 57 – række 58 – række 50 – række 60 – række 61                                                                                                        |

**SEKTION – ANDRE MOMSBELØB**

| Række | Felt - momsbeløb | Beskrivelse                                                                                                                                                                                                                                                         | Opslagsresultat                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Moms på grund af en ændring i form af moms og yderligere moms på skattebetalinger på grund af ændring af momssatsen.                                                                                                                                        | 64-AdditionalTaxDueChangeTaxRate              |
| 65  | 69               | Ugyldige eller tilladte momsbeløb, der er vist på fakturaer, samt momsbeløb, der skyldes i henhold til section 6a (4) sætning 2, section 17 (1) sætning 7 eller section 25b (2) i UStG, eller som skyldes af et outsourcet firma eller lagerchef. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Fradrag for den faste særlige forskudsbetaling for permanent forlængelse. Denne række er normalt kun udfyldt med den sidste besked om forskud for momsperioden.                                                                                                  | Brugerinputparameter i rapportdialogboksen |
| 68  | 83               | Den resterende forudbetaling af moms og resterende overskydende beløb. Medtag en minuslog foran beløbet.                                                                                                                                                          | Række 62 + række 64 – række 65 – række 66             |

**SEKTION – SUPPLERENDE OPLYSNINGER OM REDUKTIONER**

| Række | Felt - momsbasis | Felt - momsbeløb | Beskrivelse                                                            | Opslagsresultat                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Reduktion af momsgrundlaget på linje 20 til og med 24.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffReduced (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Reduktion af de fradragsberettigede indgående momsbeløb på linje 55, 59 og 60. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Modtagermoms

Hvis du konfigurerer momskoder til at bogføre indgående modtagermoms ved hjælp af use tax, skal du knytte momskoderne til opslagsresultatet i **rapportfeltopslag**, der indeholder "UseTax" i navnet.

Du kan også konfigurere to separate momskoder: en til skyldige momsbeløb og en til momsfradrag. Knyt derefter hver kode til det tilsvarende opslagsresultat for **opslag i rapportfeltet**.

Hvis der f.eks. skal foretages skattepligtig anskaffelse inden for EU til en standardsats, kan du konfigurere momskode **UT_S_EU** sammen med use tax og knytte den til opslagsresultatet **34-UseTaxEUPurchaseStandard** for **opslag i rapportfeltet**. I dette tilfælde afspejles beløb, der bruger den **UT_S_EU** momskode, i felterne 089 og 061 (række 34 og 56).

Du kan også konfigurere to momskoder:

  - **VAT_S_EU**, som har momssatsværdien -19 %
  - **InVAT_S_EU**, som har momssatsværdien 19 %

Tilknyt derefter hver kode til det tilsvarende opslagsresultat for **opslag i rapportfeltet** således:

  - Tilknyt **VAT_S_EU** med opslagsresultatet **34-EUPurchaseStandard**.
  - Tilknyt **InVAT_S_EU** med opslagsresultatet **56-InputTaxEUPurchase**.

I dette tilfælde afspejles beløb, der bruger momskoden **VAT_S_EU**, i felterne 089 (række 34). De beløb, der bruger momskoden **InVAT_S_EU**, vises i felterne 061 (række 56).

Få flere oplysninger om, hvordan du kan konfigurere modtagermoms, i [Tilbageføre gebyrer](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfigurere systemparametre

Hvis du vil oprette en momsopgørelse, skal du konfigurere organisationens (Steuernummer) momsnummer.

1. Gå til **Organisationsadministration** > **Organisationer** > **Juridiske enheder**.
2. Vælg den juridiske enhed, og vælg derefter **Registrerings-id**.
3. Vælg eller opret adressen i Tyskland, og vælg derefter **Tilføj** i oversigtspanelet **Registrerings-id**.
4. I feltet **Registreringstype** skal du vælge den registreringstype, der er dedikeret Tyskland, og som bruger **COID-registreringskategorien (Enterprise-id)**.
5. Angiv momsnummeret i feltet **Registreringsnummer**.
6. Angiv den dato, nummeret gælder fra, i feltet **Gældende** under fanen **Generelt**.

Du kan finde flere oplysninger om, hvordan du konfigurerer registreringskategorier og registreringstyper, i [Registrerings-id'er](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-for-germany"></a>Konfigurere momsangivelse for Tyskland

### <a name="import-er-configurations"></a>Importér ER-konfigurationer

Åbn arbejdsområdet til **elektronisk rapportering**, og importer følgende versioner eller senere af disse ER-formater:

   - Momsopgørelse Excel (DE).version.101.16.12.xml
   - Momsopgørelse XML (DE).version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a>Konfigurere programspecifikke parametre for momsopgørelsesfelter

Hvis der automatisk skal oprettes en momsopgørelse, skal du knytte momskoder i programmet og opslaget resulterer i ER-konfigurationen.

> [!NOTE]
> Vi anbefaler, at du aktiverer funktionen **Brug programspecifikke parametre fra tidligere versioner af ER-formater** i arbejdsområdet **Funktionsstyring**. Når denne funktion er aktiveret, anvendes parametre, der er konfigureret for den tidligere version af et ER-format, automatisk for den senere version af samme format. Hvis denne funktion ikke er aktiveret, skal du udtrykkeligt konfigurere programspecifikke parametre for hver enkelt formatversion. Funktionen **Brug programspecifikke parametre fra tidligere versioner af ER-formater** er tilgængelig i arbejdsområdet **Funktionsstyring** fra og med Finans version 10.0.23. Du kan finde flere oplysninger om, hvordan du konfigurerer parametrene for et ER-format for hver juridiske enhed, i [Konfigurere parametrene for et ER-format pr. juridisk enhed](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Benyt følgende fremgangsmåde for at definere, hvilke momskoder der genererer hvilke felter i momsopgørelsen.

1. Gå til **Arbejdsområder** > **Elektronisk rapportering**, og vælg **Rapporteringskonfigurationer**.
2. Vælg konfigurationen af **Momsopgørelsen (DE)**, og vælg derefter **Konfigurationer \> Konfiguration af Programspecifikke parametre**.
3. Vælg **opslag** i **rapportfeltet i oversigtspanelet Opslag** på siden **Applikationsspecifikke parametre**.
4. I oversigtspanelet **Betingelser** kan du angive følgende felter for at tilknytte momskoder og rapportfelter.

    | Felt                  | Beskrivelse                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Opslagsresultat          | Vælg værdien i rapportfeltet. Du kan finde flere oplysninger om værdierne og deres tilknytning til momsopgørelsesrækker i [oversigtsafsnittet for momsopgørelse](#vat-declaration-overview) tidligere i denne artikel.                                                                                               |
    | Skattekode               | Vælg den momskode, der skal tilknyttes rapportfeltet. Bogførte momsposteringer, der bruger den valgte momskode, samles i det relevante momsfelt. Det anbefales, at du adskille momskoder på en sådan måde, at en momskode kun genererer beløb i én opgørelsesboks. |
    | Transaktionsklasse | Hvis du har oprettet nok momskoder til at bestemme et opgørelsesfelt, skal du vælge **\*Ikke tom\***. Hvis du ikke har oprettet nok momskoder, så en momskode kun genererer beløb i ét opgørelsesfelt, kan du konfigurere en transaktionsklassifikator. Følgende transaktionsklassificeringer er tilgængelige:</br>-   **Køb**</br>-   **PurchaseExempt** (køb fritaget for moms)</br>-   **PurchaseReverseCharge** (Moms, der skal modtages fra køb med modtagermoms)</br>-   **Sales**</br>-   **SalesExempt** (momsfrit salg)</br>-   **SalesReverseCharge** (moms, der skal betales fra en modtager af køb eller modtagerbetaling)</br>-   **Brug moms**. </br>Der findes også en klassificering for hver transaktionsklasse for kreditnotaen. En af disse klassificeringer er f.eks. **PurchaseCreditNote** (købskreditnota).</br>Sørg for at oprette to linjer for hver momskode: En med transaktionsklasseværdien, og en med transaktionsklasse for kreditnotaværdien. |

    > [!NOTE]
    > Knyt alle momskoder til opslagsresultater. Hvis momskoderne ikke skal generere værdier i momsopgørelsen, skal du knytte dem til opslagsresultatet **Andet**.

    ![Side med ansøgningsspecifikke parametre](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. I feltet **Tilstand** skal du ændre værdien til **Fuldført**.
6. I handlingsruden skal du vælge **Eksporter** for at eksportere indstillingerne for de programspecifikke parametre.
7. Vælg konfigurationen af **momsopgørelsen Excel (DE)**, og vælg derefter **Import** i handlingsruden for at importere de parametre, du har konfigureret til **Momsopgørelse XML (DE)**.
8. I feltet **Tilstand** skal du vælge **Fuldført**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Konfigurere momsrapporteringsformatet for eksempelbeløb i Excel

1. Find, og aktiver funktionen **Rapporter med format for momsindberetning** i arbejdsområdet **Funktionsstyring**, og vælg aktivér den.
2. Gå til **Finans** > **Opsætning** > **Finansparametre**.
3. På fanen **Moms** i oversigtspanelet **Momsindstillinger** i feltet **Tilknytningsformat for momsindberetning** skal du vælge **Momsopgørelse Excel (DE)**.

   Dette format udskrives, når du kører rapporten **Rapport over moms for afregningsperiode**. Den udskrives også, når du vælger **Udskriv** på **momsbetalingssiden**.

4. Vælg skattemyndighederne på siden **Momsmyndighederne**, og vælg derefter **Standard** i feltet **Rapportlayout**.

Hvis du konfigurerer momsopgørelsen i en juridisk enhed, der har [flere momsregistreringer](emea-reporting-for-multiple-vat-registrations.md). skal du følge disse trin:

1. Gå til **Finans** > **Opsætning** > **Finansparametre**.
2. Under fanen **Moms** i oversigtspanelet **Elektronisk rapportering for lande/regioner** på linjen til **DEU** skal du vælge ER-formatet **Momsopgørelse Excel (DE)**.

## <a name="set-up-electronic-messages"></a>Konfigurere elektroniske meddelelser

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Hente og importere den datapakke, der indeholder eksempelindstillinger for elektroniske meddelelser

Datapakken indeholder indstillinger for elektroniske meddelelser, der bruges til at generere momsopgørelsen i XML-format og derefter få vist den i Excel. Du kan forlænge disse indstillinger eller oprette dine egne. Du kan finde flere oplysninger om, hvordan du arbejder med elektroniske meddelelser og opretter dine egne indstillinger, i [Elektronisk meddelelse](../general-ledger/electronic-messaging.md).

1. I [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) skal du vælge **Data-pakken** som aktivtype i biblioteket Delte aktiver og derefter hente **DE-momsopgørelsespakken EM**. Det hentede filnavn er **DE VAT declaration EM-pakke.zip**.
2. I Dynamics 365 Finance skal du vælge **Importér** i arbejdsområdet **Datastyring**.
3. Indtast et navn for gruppen i feltet **Gruppenavn** i oversigtspanelet **Importér**.
4. Vælg **Tilføj fil** i oversigtspanelet **Valgte enheder**.
5. I dialogboksen **Tilføj fil** skal du kontrollere, at feltet **Kildedataformat** er angivet til **Pakke**, vælge **Overfør og tilføj**, og vælg derefter den zip-fil, du har hentet tidligere.
6. Vælg **Luk**.
7. Når dataenhederne er overført, skal du vælge **Import** i handlingsruden.
8. Gå til **Moms** > **Momsforespørgsler og rapporter** > **Elektroniske meddelelser** > **Elektroniske meddelelser**, og valider den behandling af elektroniske meddelelser, som du har importeret.

### <a name="configure-electronic-messages"></a>Konfigurer elektroniske meddelelser

1. Gå til **Moms** > **Konfiguration** > **Elektroniske meddelelser** > **Handlingerne Udfyld poster**.
2. Marker linjen for **DE-udfyld momsreturposter**, og vælg derefter **Rediger forespørgsel**.
3. Brug filteret til at angive de afregningsperioder, der skal medtages i rapporten.
4. Hvis du skal rapportere momsposteringer fra andre afregningsperioder i en anden opgørelse, skal du oprette en ny handling for **Udfyld poster** og vælge de relevante afregningsperioder.

## <a name="preview-the-vat-declaration-in-excel"></a>Få vist momsopgørelsen i Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Få vist momsopgørelsen i Excel fra den periodiske opgave for rapportmoms til afregningsperiode

1. Gå til **Moms** > **Periodiske opgaver** > **Erklæringer** > **Moms** > **Rapporter moms for afregningsperioden**.
2. Vælg en værdi i feltet **Afregningsperiode**.
3. Vælg en af følgende værdier i feltet **Momsafregningsversion**:

    - **Original**: Opret en rapport over momstransaktionerne for den oprindelige momsbetaling, eller før momsbetalingen genereres.
    - **Rettelser**: Opret en rapport over momstransaktioner for alle efterfølgende momsbetalinger for perioden.
    - **Liste over totaler**: Opret en rapport over alle momstransaktioner for perioden, herunder de originale og alle rettelser.

4. Vælg startdatoen for rapporteringsperioden i feltet **Fra-dato**.
5. Vælg **OK**, og gennemse Excel-rapporten.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Afregn og bogfør moms

1. Gå til **Moms** > **Periodiske opgaver** > **Erklæringer** > **Moms** > **Afregn og bogfør moms**.
2. Vælg en værdi i feltet **Afregningsperiode**.
3. Vælg en af følgende værdier i feltet **Momsafregningsversion**:

    - **Original**: Generér den oprindelige momsafregning for afregningsperioden.
    - **Seneste korrektioner**: Opret en momsafregning for rettelsen, efter at den oprindelige momsafregning for afregningsperioden blev oprettet.

4. Vælg startdatoen for rapporteringsperioden i feltet **Fra-dato**.
5. Vælg **OK**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Få vist momsopgørelsen i Excel fra en momsbetaling

1. Gå til **Moms** > **Forespørgsler og rapporter** > **Momsforespørgsler** > **Momsafregninger**, og vælg en momsbetalingslinje.
2. Vælg **Udskriv rapport**, og vælg derefter **OK**.
3. Gennemse den Excel-fil, der er genereret for den valgte momsbetalingslinje.

    > [!NOTE]
    > Rapporten genereres kun for den valgte linje i momsbetalingen. Hvis du f.eks. vil generere en korrigerende opgørelse, der indeholder alle rettelserne for perioden, eller en erstatningsrapport, der indeholder de oprindelige data og alle rettelser, skal du bruge **rapporten moms til den periodiske opgave for afregningsperioden**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Generere en momsopgørelse fra elektroniske meddelelser

Når du bruger elektroniske meddelelser til generering af rapporten, kan du indsamle momsdata fra flere juridiske enheder. Du kan finde flere oplysninger i afsnittet [Køre en momsopgørelse for flere juridiske enheder](#run-a-vat-declaration-for-multiple-legal-entities) senere i denne artikel.

Følgende procedure gælder for eksemplet på behandling af elektroniske meddelelser, som du har importeret fra LCS-biblioteket til delte aktiver.

1. Gå til **Moms** > **Forespørgsler og rapporter** > **Elektroniske meddelelser** > **Elektroniske meddelelser**.
2. Vælg **DE-momsopgørelse** i venstre rude.
3. Vælg **Ny** i oversigtspanelet **Meddelelser**, og vælg derefter **OK** i dialogboksen **Kør behandling**.
4. Vælg den meddelelseslinje, der er oprettet, angiv en beskrivelse, og angiv derefter start- og slutdatoer for opgørelsen.

    > [!NOTE]
    > Trin 5 til 7 er valgfrie.

5. Valgfrit: Vælg **Indsamlingsdata** i oversigtspanelet **Meddelelser**, og vælg derefter **OK**. De momsbetalinger, der er genereret tidligere, føjes til meddelelsen. Du kan finde flere oplysninger i afsnittet [Afregn og bogfør moms](#settle-and-post-sales-tax) tidligere i denne artikel. Hvis du springer dette trin over, kan du stadig generere en momsopgørelse ved hjælp af feltet **Momsopgørelsesversion** i dialogboksen **Momsopgørelse**.
6. Valgfrit: Gennemse de momsbetalinger, der er overført til behandling, i oversigtspanelet **Meddelelseselementer**. Alle momsbetalinger i den valgte periode, som ikke er inkluderet i andre meddelelser i samme behandling, inkluderes som standard.
7. Valgfrit: Vælg det **originaldokument**, du vil gennemse momsafbetalingerne for, eller vælg **Slet** for at udelukke momsbetalinger fra behandling. Hvis du springer dette trin over, kan du stadig generere en momsopgørelse ved hjælp af feltet **Momsopgørelsesversion** i dialogboksen **Momsopgørelse**.
8. I oversigtspanelet **Meddelelser** skal du vælge **Opdater status**. Vælg **Klar til generering** i dialogboksen **Opdater status**, og vælg derefter **OK**. Kontroller, at meddelelsens status er ændret til **Klar til generering**.
9. Vælg **Generer rapport**. Hvis du vil have vist momsopgørelsesbeløbene, skal du vælge **Forhåndsversionsrapport** i dialogboksen **Kør behandling** og derefter vælge **OK**.
10. Vælg **OK** i dialogboksen **Elektroniske rapportparametre**, og angiv følgende felter.

    | **Felt**                                   | **Beskrivelse**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Afregningsperiode                           | Vælg afregningsperiode. Hvis du valgte **Indsamling af data** i trin 5, kan du lade dette felt stå tomt. Rapporten genereres for de momstransaktioner, der inkluderes i inkasseret momsbetaling. |
    | Momsopgørelse                     | Vælg en af følgende værdier:</br>-   **Original** - Opret en rapport over momstransaktionerne for den oprindelige momsbetaling, eller før momsbetalingen genereres.</br>-   **Rettelser** - Opret en rapport over momstransaktioner for alle efterfølgende momsbetalinger for perioden.</br>-   **Liste over totaler** - Opret en rapport over alle momstransaktioner for perioden, herunder de originale og alle rettelser.|
    | Momspligtig repræsentant | Vælg den part, der er momsrepræsentant for momsopgørelsen, hvis det er relevant. Oplysninger om den valgte part eksporteres til **DatenLieferant** XML-elementet. |
    | Kontaktperson | Vælg en person i organisationen, som er dataleverandør. Oplysninger om den valgte person eksporteres til **DatenLieferant** XML-elementet. |
    | Korrigerende returnering | Vælg **Ja**, hvis dette er en rettelse af momsopgørelsen. I dette tilfælde har XML-elementet KZ10 en værdi på **1**.|
    | Understøttende dokumenter | Vælg **Ja**, hvis du også sender supplerende dokumenter. I dette tilfælde har XML-elementet KZ22 en værdi på **1**.|
    | SEPA Direct Debit-bemyndigelsen tilbagekaldes som en undtagelse| Vælg **Ja**, hvis SEPA-bemyndigelsen til direkte debitering tilbagekaldes som en undtagelse for denne periode før registrering. F.eks. på grund af modregning af anmodninger. Eventuel restsaldo skal betales separat. I dette tilfælde har XML-elementet KZ26 en værdi på **1**. |
    | Modpostering af det ønskede refunderingsbeløb | Vælg **Ja**, hvis det ønskede refusionsbeløb modposteres, eller hvis refusionsbeløbet er tildelt. I dette tilfælde har XML-elementet KZ29 en værdi på **1**. |
    | Permanent forlængelse af særlig forudbetaling | Angiv fradrag for den faste særlige forskudsbetaling for permanent forlængelse. Dette fradragsbeløb udfyldes normalt kun ved den seneste forudregistrering af momsperioden. Beløbet eksporteres i række 67 (felt 39) og XML-elementet KZ39 i momsopgørelsen. |

11. Vælg **Vedhæftede filer** i øverste højre hjørne af siden, og vælg derefter **Åbn**.
12. Gennemse beløbene i Excel-dokumentet, og vælg derefter **Generer rapport**.
13. Hvis du vil generere en momsopgørelse i XML-format, skal du vælge **Generer rapport** i dialogboksen **Kør behandling** og derefter vælge **OK**.
14. I dialogboksen **Parametre for elektronisk rapportering** skal du angive felterne som beskrevet i trin 10.
15. Vælg **Vedhæftede filer** øverst til højre på siden, hent filen, og brug den til overførsel til momsmyndigheden.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a>Kør en momserklæring for flere juridiske enheder

Hvis du vil bruge formaterne til indberetning af momsopgørelsen for en gruppe juridiske enheder, skal du først konfigurere programspecifikke parametre for ER-formater for momskoder fra alle nødvendige juridiske enheder.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Oprette elektroniske meddelelser til indsamling af momsdata fra flere juridiske enheder

Følg disse trin for at konfigurere elektroniske meddelelser, der indsamler data fra flere juridiske enheder.

1. Gå til **Arbejdsområder** > **Funktionsstyring**.
2. Find og vælg **forespørgsler på tværs af virksomheder** for funktionen til handling af poster på listen, og vælg **Aktiver nu**.
3. Gå til **Moms** > **Konfiguration** > **Elektroniske meddelelser \> Udfyld poster**.
4. Marker linjen for **DE-udfyld momsreturposter** på siden **Udfyld poster**.

   I gitteret til **opsætning af datakilder** vises et nyt **regnskab**. For eksisterende poster viser dette felt id'et for den aktuelle juridiske enhed.

5. I gitteret til **opsætning af datakilder** skal du tilføje en linje for hver yderligere juridisk enhed, der skal medtages i rapporteringen. For hver ny linje skal du angive følgende felter.

    | Felt                  | Beskrivelse                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Navn                   | Angiv en værdi, der kan hjælpe dig med at forstå, hvor denne post stammer fra. Du kan f.eks. angive **momsbetaling for Datterselskab 1**. |
    | Typen af meddelelseselement      | Vælg **momsretur**. Denne værdi er den eneste værdi, der er tilgængelig for alle poster.                                    |
    | Kontotype           | Markér **Alt**.                                                                                                               |
    | Navn på overordnet tabel      | Angiv **TaxReportVoucher** for alle poster.                                                                             |
    | Feltet dokumentnummer  | Angiv **Bilag** for alle poster.                                                                                      |
    | Feltet Dokumentdato    | Angiv **TransDate** for alle poster.                                                                                    |
    | Feltet Dokumentkonto | Angiv **TaxPeriod** for alle poster.                                                                                    |
    | Virksomhed                | Vælg id'et for den juridiske enhed.                                                                                            |
    | Brugerforespørgsel             | Dette afkrydsningsfelt markeres automatisk, når du definerer kriterier ved at vælge **Rediger forespørgsel**.                                 |

6. For hver ny linje skal du vælge **Rediger forespørgsel** og angive et relateret afregningsperiode, der er specifikt for den juridiske enhed, som er angivet i feltet **Firma** på linjen.

Når opsætningen er fuldført, indsamler funktionen **Indsamling af data** på siden **Elektroniske meddelelser** momsbetalinger fra alle de juridiske enheder, du har defineret.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
