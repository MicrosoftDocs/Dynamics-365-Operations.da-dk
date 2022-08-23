---
title: Momsopgørelse (Danmark)
description: Denne artikel beskriver, hvordan du kan konfigurere og generere en forudgående momsopgørelse for Danmark.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: a47b2b98d86daf50876c783f879362ec1addb579
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272134"
---
# <a name="vat-declaration-denmark"></a>Momsopgørelse (Danmark)

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du kan konfigurere momsopgørelsen for Danmark og gennemgå den i Microsoft Excel.

Hvis rapporten skal genereres automatisk, skal du først oprette nok momskoder til at føre et separat momsregnskab for hvert felt i den forudgående momsopgørelse. Derudover skal du i de applikationsspecifikke parametre i ER-formatet for den forudgående momsopgørelse knytte momskoder til opslagsresultatet af opslagene i felterne i momsopgørelsen.

For Danmark skal du konfigurere **Opslag i rapportfelt**. Du kan finde flere oplysninger om, hvordan du konfigurerer programspecifikke parametre, i afsnittet [Konfigurere programspecifikke parametre for momsopgørelsesfelter](#set-up-application-specific-parameters) senere i denne artikel.

I tabellen nedenfor viser kolonnen "Opslagsresultat" det opslagsresultat, der er forudkonfigureret til en bestemt momsopgørelsesrække i momsopgørelsesformatet. Brug disse oplysninger til korrekt at knytte momskoder til opslagsresultatet og derefter med rækken i momsopgørelsen.

### <a name="vat-declaration-overview"></a>Oversigt over momsopgørelse

Den forudgående momsopgørelse i Danmark indeholder følgende oplysninger.

**Skyldig moms**

| Beskrivelse                                                  | Momsgrundlag/Momsbeløb | Opslagsresultat/Total                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Udgående moms                                                   | Momsbeløb          | **OutputVAT**</br> **DomesticVATUseTax** (indberettes også i feltet "Indgående moms")                                                                                                                                                                                                                                                                       |
| Moms på varer osv. købt i udlandet                           | Momsbeløb          | **PurchaseGoodsAbroad**</br>**PurchaseGoodsAbroadUseTax** (indberettes også i feltet "Indgående moms")</br>**PurchaseGoodsEU** (momsgrundlaget indberettes i "Felt A - anskaffelse af varer.")</br>**PurchaseGoodsEUUseTax** (momsbeløbet indberettes også i feltet "Indgående moms". Momsgrundlaget indberettes i "Felt A - anskaffelse af varer.")                   |
| Moms på tjenester, der er købt i udlandet, som er omfattet af modtagermoms | Momsbeløb          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax** (indberettes også i feltet "Indgående moms")</br>**PurchaseServicesEU** (momsgrundlaget indberettes i "Felt A - anskaffelse af tjenester.")</br>**PurchaseServicesEUUseTax** (momsbeløbet indberettes også i feltet "Indgående moms". Momsgrundlaget indberettes i "Felt A - anskaffelse af tjenester.") |
| I alt til betaling                                                | Momsbeløb          | Total for de foregående tre felter                                                                                                                                                                                                                                                                                                            |

**Fradrag**

| Beskrivelse                                                                               | Momsgrundlag/Momsbeløb | Opslagsresultat/Total                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indgående moms                                                                                 | Momsbeløb          | **InputVAT**</br> **DomesticVATUseTax** (indberettes også i feltet "Udgående moms")</br>**PurchaseGoodsAbroadUseTax** (indberettes også i feltet "Moms på varer osv. købt i udlandet")</br>**PurchaseServicesAbroadUseTax** (indberettes også i feltet "Moms af ydelseskøb i udlandet med omvendt betalingspligt")</br>**PurchaseGoodsEUUseTax** (indberettes også i feltet "Moms på varer osv. købt i udlandet")</br> **PurchaseServicesEUUseTax** (indberettes også i feltet "Moms af ydelseskøb i udlandet med omvendt betalingspligt") |
| Afgift på olie og flaskegas                                                                  | Momsbeløb          | **OilGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Afgift på naturgas og bygas                                                             | Momsbeløb          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Kulafgift                                                                               | Momsbeløb          | **CarbonDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2Duty                                                                                   | Momsbeløb          | **CO2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Vandafgift                                                                              | Momsbeløb          | **WaterCharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Samlede fradrag                                                                          | Momsbeløb          | Total for de foregående seks felter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Samlet momsbeløb (positivt beløb = foretag betaling, negativt beløb = modtag refusion) | Momsbeløb          | "I alt til betaling" – "Samlede fradrag"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Supplerende oplysninger**

| Beskrivelse                                                                                                                                                                                                                                | Momsgrundlag/Momsbeløb | Opslagsresultat/Total                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| Felt A – anskaffelse af varer. Værdien uden moms af anskaffelse af varer inden for EU.                                                                                                                                                   | Momsgrundlag            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| Felt A – anskaffelse af ydelser. Værdien uden moms af anskaffelse af ydelser inden for EU.                                                                                                                                             | Momsgrundlag            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| Felt B - levering af varer - skal indberettes i "EU-salg uden moms"/DK VIES. Værdien uden moms af varelevering inden for EU                                                                                                           | Momsgrundlag            | **SalesGoodsEU**                                |
| Felt B - anskaffelser - skal ikke indberettes i "EU-salg uden moms"/DK VIES. Værdien uden moms af visse leverancer inden for EU, f.eks. installation, samling, fjernsalg og ny transportform til ikke-momspligtige personer. | Momsgrundlag            | **SalesInstallationAssemblyEtcEU**              |
| Felt B – levering af ydelser. Den værdi uden moms af serviceydelser inden for EU, hvor køberen skal betale momsen som modtagermoms, skal også indberettes til "EU-salg uden moms"/DK VIES.                          | Momsgrundlag            | **SalesServicesEU**                             |
| Felt C – andre leverancer. Værdi af levering af andre varer og tjenester, der leveres uden moms i Danmark, til andre EU-medlemslande og til tredjeparter eller tredjeområder.                                     | Momsgrundlag            | **OtherSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Modtagermoms

Hvis du konfigurerer momskoder til at bogføre indgående modtagermoms ved hjælp af use tax, skal du knytte momskoderne til opslagsresultatet i **rapportfeltopslag**, der indeholder "UseTax" i navnet.

Du kan også konfigurere to separate momskoder: en til skyldige momsbeløb og en til momsfradrag. Knyt derefter hver kode til det tilsvarende opslagsresultat for **opslag i rapportfeltet**.

Hvis der f.eks. skal foretages skattepligtig anskaffelse inden for EU til en standardsats, kan du konfigurere momskode **UT_S_EU** sammen med importmoms og knytte den til opslagsresultatet **PurchaseGoodsEUUseTax** for **opslag i rapportfeltet**. I dette tilfælde afspejles momsbeløb, der bruger **UT_S_EU**-momskoden, i felterne "Moms på varer osv. købt i udlandet" og "Indgående moms". Momsgrundlaget afspejles i "Felt A - anskaffelse af varer."

Du kan også konfigurere to momskoder:

- **VAT_S_EU**, som har momssatsværdien -25 %
- **InVAT_S_EU**, som har momssatsværdien 25 %

Tilknyt derefter hver kode til det tilsvarende opslagsresultat for **opslag i rapportfeltet** således:

- Knyt **VAT_S_EU** til opslagsresultatet **PurchaseGoodsEU**.
- Knyt **InVAT_S_EU** til opslagsresultatet **InputVAT**.

I dette tilfælde afspejles beløb, der bruger **VAT_S_EU**-momskoden, i felterne "Moms på varer osv. købt i udlandet" og "Felt A - anskaffelse af varer". De beløb, der bruger momskoden **InVAT_S_EU**, vises i feltet "Indgående moms".

Få flere oplysninger om, hvordan du kan konfigurere modtagermoms, i [Tilbageføre gebyrer](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfigurere systemparametre

Hvis du vil generere en momsopgørelse, skal du konfigurere momsnummeret.

1. Gå til **Organisationsadministration** > **Organisationer** > **Juridiske enheder**.
2. Vælg den juridiske enhed, og vælg derefter **Registrerings-id**.
3. Vælg eller opret adressen i Danmark, og vælg derefter **Tilføj** i oversigtspanelet **Registrerings-id**.
4. I feltet **Registreringstype** skal du vælge den registreringstype, der er dedikeret til Danmark, og som bruger registreringskategorien **Moms-id**.
5. Angiv momsnummeret i feltet **Registreringsnummer**.
6. Angiv den dato, nummeret gælder fra, i feltet **Gældende** under fanen **Generelt**.

Du kan finde flere oplysninger om, hvordan du konfigurerer registreringskategorier og registreringstyper, i [Registrerings-id'er](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Konfigurere eksempelvisning af momsangivelse for Danmark

### <a name="import-er-configurations"></a>Importér ER-konfigurationer

Åbn arbejdsområdet **Elektronisk rapportering**, og importér ER-formatet **Momsopgørelse Excel (DK)**.

Du kan finde flere oplysninger under [Downloade ER-konfigurationer fra det globale lager i konfigurationstjeneste](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a>Konfigurere programspecifikke parametre for momsopgørelsesfelter

> [!NOTE]
> Vi anbefaler, at du aktiverer funktionen **Brug programspecifikke parametre fra tidligere versioner af ER-formater** i arbejdsområdet **Funktionsstyring**. Når denne funktion er aktiveret, anvendes parametre, der er konfigureret for den tidligere version af et ER-format, automatisk for den senere version af samme format. Hvis denne funktion ikke er aktiveret, skal du udtrykkeligt konfigurere programspecifikke parametre for hver enkelt formatversion. Funktionen **Brug programspecifikke parametre fra tidligere versioner af ER-formater** er tilgængelig i arbejdsområdet **Funktionsstyring** fra og med Finans version 10.0.23. Du kan finde flere oplysninger om, hvordan du konfigurerer parametrene for et ER-format for hver juridiske enhed, i [Konfigurere parametrene for et ER-format pr. juridisk enhed](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Hvis der automatisk skal oprettes en momsopgørelse, skal du knytte momskoder i programmet og opslaget resulterer i ER-konfigurationen.

Benyt følgende fremgangsmåde for at definere, hvilke momskoder der genererer hvilke felter i momsopgørelsen.

1. Gå til **Arbejdsområder** > **Elektronisk rapportering**, og vælg **Rapporteringskonfigurationer**.
2. Vælg konfigurationen **Momsopgørelse Excel (DK)**, og vælg derefter **Konfigurationer \> Konfiguration af programspecifikke parametre**.
3. Vælg **opslag** i **rapportfeltet i oversigtspanelet Opslag** på siden **Applikationsspecifikke parametre**.
4. I oversigtspanelet **Betingelser** kan du angive følgende felter for at tilknytte momskoder og rapportfelter.

    | Felt                  | Beskrivelse                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Opslagsresultat          | Vælg værdien i rapportfeltet. Du kan finde flere oplysninger om værdierne og deres tilknytning til momsopgørelsesrækker i [oversigtsafsnittet for momsopgørelse](#vat-declaration-overview) tidligere i denne artikel.                                                                                               |
    | Skattekode               | Vælg den momskode, der skal tilknyttes rapportfeltet. Bogførte momsposteringer, der bruger den valgte momskode, samles i det relevante momsfelt. Det anbefales, at du adskille momskoder på en sådan måde, at en momskode kun genererer beløb i én opgørelsesboks. |
    | Transaktionsklasse | Hvis du har oprettet nok momskoder til at bestemme et opgørelsesfelt, skal du vælge **\*Ikke tom\***. Hvis du ikke har oprettet nok momskoder, så en momskode kun genererer beløb i ét opgørelsesfelt, kan du konfigurere en transaktionsklassifikator. Følgende transaktionsklassificeringer er tilgængelige:</br>-   **Køb**</br>-   **PurchaseExempt** (køb fritaget for moms)</br>-   **PurchaseReverseCharge** (Moms, der skal modtages fra køb med modtagermoms)</br>-   **Sales**</br>-   **SalesExempt** (momsfrit salg)</br>-   **SalesReverseCharge** (moms, der skal betales fra en modtager af køb eller modtagerbetaling)</br>-   **Brug moms**. </br>Der findes også en klassificering for hver transaktionsklasse for kreditnotaen. En af disse klassificeringer er f.eks. **PurchaseCreditNote** (købskreditnota).</br>Sørg for at oprette to linjer for hver momskode: En med transaktionsklasseværdien, og en med transaktionsklasse for kreditnotaværdien. |


    > [!NOTE]
    > Knyt alle momskoder til opslagsresultater. Hvis momskoderne ikke skal generere værdier i momsopgørelsen, skal du knytte dem til opslagsresultatet **Andet**.

    ![Side med ansøgningsspecifikke parametre.](media/7db74920fad66a0db7fad60758698cc0.png)


5. I feltet **Tilstand** skal du ændre værdien til **Fuldført**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Konfigurere momsrapporteringsformatet for eksempelbeløb i Excel

1. Find og vælg funktionen **Rapporter med format for momsindberetning** i arbejdsområdet **Funktionsstyring**. Vælg funktionen på listen, og vælg derefter **Aktivér nu**.
2. Gå til **Finans** > **Opsætning** > **Finansparametre**.
3. På fanen **Moms** i oversigtspanelet **Momsindstillinger** i feltet **Tilknytningsformat for momsindberetning** skal du vælge **Momsopgørelse Excel (DK)** som ER-format.

   Dette format udskrives, når du kører rapporten **Rapport over moms for afregningsperiode**. Den udskrives også, når du vælger **Udskriv** på **momsbetalingssiden**.

4. Vælg skattemyndighederne på siden **Momsmyndighederne**, og vælg derefter **Standard** i feltet **Rapportlayout**.

Hvis du konfigurerer momsopgørelsen i en juridisk enhed, der har [flere momsregistreringer](emea-reporting-for-multiple-vat-registrations.md), skal du følge disse trin.

1. Gå til **Finans** \> **Konfiguration** \> **Finansparametre**.
2. Under fanen **Moms** i oversigtspanelet **Elektronisk rapportering for lande/områder** på linjen til **DNK** skal du vælge ER-formatet **Momsopgørelse Excel (DK)**.

## <a name="set-up-electronic-messages"></a>Konfigurere elektroniske meddelelser

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Hente og importere den datapakke, der indeholder eksempelindstillinger for elektroniske meddelelser

Datapakken indeholder indstillinger for elektroniske meddelelser, der bruges til eksempelvisning af momsopgørelsen i Excel. Du kan forlænge disse indstillinger eller oprette dine egne. Du kan finde flere oplysninger om, hvordan du arbejder med elektroniske meddelelser og opretter dine egne indstillinger, i [Elektronisk meddelelse](../general-ledger/electronic-messaging.md).

1. I [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) skal du vælge **Datapakke** som aktivtype i biblioteket Delte aktiver og derefter hente **DK-momsopgørelsespakken**. Det hentede filnavn er **DK VAT declaration package.zip**.
2. I Finans skal du vælge **Importér** i arbejdsområdet **Datastyring**.
3. Indtast et navn for gruppen i feltet **Gruppenavn** i oversigtspanelet **Importér**.
4. Vælg **Tilføj fil** i oversigtspanelet **Valgte enheder**.
5. I dialogboksen **Tilføj fil** skal du kontrollere, at feltet **Kildedataformat** er angivet til **Pakke**, vælge **Overfør og tilføj**, og vælg derefter den zip-fil, du har hentet tidligere.
6. Vælg **Luk**.
7. Når dataenhederne er overført, skal du vælge **Import** i handlingsruden.
8. Gå til **Moms** > **Forespørgsler og rapporter** > **Elektroniske meddelelser** > **Elektroniske meddelelser**, og valider den behandling af elektroniske meddelelser, som du har importeret (**DK-momsopgørelse**).

### <a name="configure-electronic-messages"></a>Konfigurer elektroniske meddelelser

1. Gå til **Moms** > **Konfiguration** > **Elektroniske meddelelser** > **Handlingerne Udfyld poster**.
2. Marker linjen for **DK-udfyld momsreturposter**, og vælg derefter **Rediger forespørgsel**.
3. Brug filteret til at angive de afregningsperioder, der skal medtages i rapporten.
4. Hvis du skal rapportere momsposteringer fra andre afregningsperioder i en anden opgørelse, skal du oprette en ny handling for **Udfyld poster** og vælge de relevante afregningsperioder.

## <a name="preview-the-vat-declaration-in-excel"></a>Få vist momsopgørelsen i Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a>Få vist momsopgørelsen i Excel fra den periodiske opgave for rapportmoms til afregningsperiode

1. Gå til **Moms** > **Periodiske opgaver** > **Erklæringer** > **Moms** > **Rapporter moms for afregningsperioden**.
2. Vælg en værdi i feltet **Afregningsperiode**.
3. Vælg en af følgende værdier i feltet **Momsafregningsversion**:

    - **Original**: Opret en rapport over momstransaktionerne for den oprindelige momsbetaling, eller før momsbetalingen genereres.
    - **Rettelser**: Opret en rapport over momstransaktioner for alle efterfølgende momsbetalinger for perioden.
    - **Liste over totaler**: Opret en rapport over alle momstransaktioner for perioden, herunder de originale og alle rettelser.

4. Vælg startdatoen for rapporteringsperioden i feltet **Fra-dato**.
5. Vælg **OK**, og gennemse Excel-rapporten.

### <a name="settle-and-post-sales-tax"></a>Afregn og bogfør moms

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
> Rapporten genereres kun for den valgte linje i momsbetalingen. Hvis du skal generere en korrigerende opgørelse, der indeholder alle rettelserne for perioden, eller en erstatningsrapport, der indeholder de oprindelige data og alle rettelser, skal du bruge den periodiske opgave **Indberet moms for afregningsperioden**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Generere en momsopgørelse fra elektroniske meddelelser

Når du bruger elektroniske meddelelser til generering af rapporten, kan du indsamle momsdata fra flere juridiske enheder. Du kan finde flere oplysninger i afsnittet [Køre en momsopgørelse for flere juridiske enheder](#run-vat-declaration) senere i denne artikel.

Følgende procedure gælder for eksemplet på behandling af elektroniske meddelelser, som du tidligere har importeret fra LCS-biblioteket til delte aktiver.

1. Gå til **Moms \> Forespørgsler og rapporter \> Elektroniske meddelelser \> Elektroniske meddelelser**.
2. Vælg **DK-momsopgørelse** i venstre rude.
3. Vælg **Ny** i oversigtspanelet **Meddelelser**, og vælg derefter **OK** i dialogboksen **Kør behandling**.
4. Vælg den meddelelseslinje, der er oprettet, angiv en beskrivelse, og angiv derefter start- og slutdatoer for opgørelsen.

   > [!NOTE]
   > Trin 5 til 7 er valgfrie.

5. Valgfrit: Vælg **Indsamlingsdata** i oversigtspanelet **Meddelelser**, og vælg derefter **OK**. De momsbetalinger, der er genereret tidligere, føjes til meddelelsen. Du kan finde flere oplysninger i afsnittet [Afregn og bogfør moms](#settle-and-post-sales-tax) tidligere i denne artikel. Hvis du springer dette trin over, kan du stadig generere en momsopgørelse ved hjælp af feltet **Momsopgørelsesversion** i dialogboksen **Momsopgørelse**.
6. Valgfrit: Gennemse de momsbetalinger, der er overført til behandling, i oversigtspanelet **Meddelelseselementer**. Alle momsbetalinger i den valgte periode, som ikke er inkluderet i andre meddelelser i samme behandling, inkluderes som standard.
7. Valgfrit: Vælg det **Originaldokument**, du vil gennemse momsafbetalingerne for, eller vælg **Slet** for at udelukke momsbetalinger fra behandling. Hvis du springer dette trin over, kan du stadig generere en momsopgørelse ved hjælp af feltet **Momsopgørelsesversion** i dialogboksen **Momsopgørelse**.
8. I oversigtspanelet **Meddelelser** skal du vælge **Opdater status**. Vælg **Klar til generering** i dialogboksen **Opdater status**, og vælg derefter **OK**. Kontroller, at meddelelsens status er ændret til **Klar til generering**.
9. Vælg **Generer rapport**. Hvis du vil have vist momsopgørelsesbeløbene, skal du vælge **Forhåndsversionsrapport** i dialogboksen **Kør behandling** og derefter vælge **OK**.
10. I dialogboksen **Parametre for elektronisk rapportering** skal du angive felterne som beskrevet i sektionen [Få vist momsopgørelsen i Excel fra den periodiske opgave for rapportmoms til afregningsperiode](#preview-vat-excel) tidligere i denne artikel og derefter vælge **OK**.
11. Vælg knappen **Vedhæftede filer** (papirklipssymbolet) øverst til højre på siden, og vælg derefter **Åbn** for at åbne filen. Gennemgå beløbene i Excel-dokumentet.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a>Kør en momserklæring for flere juridiske enheder

Hvis du vil bruge formaterne til indberetning af momsopgørelsen for en gruppe juridiske enheder, skal du først konfigurere programspecifikke parametre for ER-formater for momskoder fra alle nødvendige juridiske enheder.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Oprette elektroniske meddelelser til indsamling af momsdata fra flere juridiske enheder

Følg disse trin for at konfigurere elektroniske meddelelser, der indsamler data fra flere juridiske enheder.

1. Gå til **Arbejdsområder** > **Funktionsstyring**.
2. Find og vælg **forespørgsler på tværs af virksomheder** for funktionen til handling af poster på listen, og vælg **Aktiver nu**.
3. Gå til **Moms** > **Konfiguration** > **Elektroniske meddelelser** > **Handlingerne Udfyld poster**.
4. Vælg linjen for **DK-udfyld momsreturposter** på handlingssiden **Udfyld poster**.

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
