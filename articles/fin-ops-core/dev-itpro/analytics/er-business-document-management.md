---
title: Oversigt over styring af forretningsdokumenter
description: Denne artikel indeholder oplysninger om, hvordan du kan bruge funktionen til styring af forretningsdokumenter i ER-strukturen.
author: kfend
ms.date: 04/23/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.assetid: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
ms.openlocfilehash: 0fab7e1a36d9b4092cf4353533704859e83bed26
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288282"
---
# <a name="business-document-management-overview"></a>Oversigt over styring af forretningsdokumenter

[!include [banner](../includes/banner.md)]

Forretningsbrugere benytter strukturen til [Elektronisk rapportering (ER)](general-electronic-reporting.md) til at konfigurere formater for udgående elektroniske dokumenter i overensstemmelse med de lovgivningsmæssige krav i forskellige lande/områder. Brugerne kan også definere dataflow for at angive, hvilke programdata der skal placeres i genererede dokumenter. ER-strukturen genererer udgående dokumenter i Microsoft Office-formater (Excel-projektmapper eller Word-dokumenter) ved hjælp af foruddefinerede skabeloner. Skabelonerne udfyldes med de påkrævede data i overensstemmelse med det konfigurerede dataflow, mens de nødvendige dokumenter genereres. Hvert konfigurerede format kan udgives som en del af en ER-løsning til generering af specifikke udgående dokumenter. Dette repræsenteres ved en ER-formatkonfiguration, der kan indeholde skabeloner, som du kan bruge til at generere forskellige udgående dokumenter. Erhvervsbrugere kan benytte denne struktur til at administrere nødvendige forretningsdokumenter.

**Styring af forretningsdokumenter** er bygget oven på ER-strukturen og gør det muligt for erhvervsbrugere at redigere forretningsdokumentskabeloner i Microsoft 365-tjenesten eller Microsoft Office-skrivebordsprogrammet. Ændringer i dokumenterne kan omfatte ændring af forretningsdokumentdesign og tilføjelse af pladsholdere til yderligere data uden ændringer af kildekode og nye installationer. Det er ikke nødvendigt at have kendskab til ER-strukturen for at opdatere skabeloner til forretningsdokumenter.

> [!NOTE]
> Vær opmærksom på, at styring af forretningsdokumenter giver dig mulighed for at redigere skabeloner, der bruges til at fremstille forretningsdokumenter som f.eks. ordrer, fakturaer osv. Mens en skabelon er ændret, og der er udgivet en ny version af den, bruges denne version til at oprette nødvendige forretningsdokumenter. Styring af forretningsdokumenter kan ikke bruges til at redigere allerede genererede forretningsdokumenter.

## <a name="supported-deployments"></a>Understøttede installationer

I øjeblikket er funktionen til styring af forretningsdokumenter kun implementeret i skyinstallationer. Hvis denne funktion er vigtig for din lokale installation, skal du give os besked via feedback på webstedet [Idéer](https://experience.dynamics.com/ideas/).

## <a name="supported-microsoft-office-applications"></a>Understøttede Microsoft Office-applikationer

Hvis du vil bruge styring af forretningsdokumenter til redigering af skabeloner i Excel eller Word ved hjælp af Microsoft Office-skrivebordsprogrammer, skal du have Microsoft Office 2010 eller nyere installeret. Dette understøttes i skyinstallationen og installationer i det lokale miljø.

Hvis du vil bruge styring af forretningsdokumenter til redigering af skabeloner i Excel eller Word ved hjælp af Microsoft 365-programmer, skal du have Microsoft 365 Office til webabonnementet. Dette understøttes af implementering i skyen.

## <a name="business-document-availability"></a>Tilgængelighed af forretningsdokument

En komplet liste over alle rapporter, der er planlagt for udgaven i oktober 2019, findes i [Konfigurerbar rapportering af forretningsdokumenter i Word og Excel](/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

En komplet liste over alle rapporter, der er planlagt for udgaven i oktober 2020, findes i [Konfigurerbare forretningsdokumenter – Word-skabeloner](/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates).

Der vil være flere tilgængelige rapporter i fremtidige versioner. Der vil blive udsendt særlige beskeder om flere rapporter separat. Du kan få mere at vide om, hvordan du gennemser listen over aktuelt tilgængelige rapporter, i afsnittet [Liste over ER-konfigurationer, der er udgivet i Finans for at understøtte konfigurerbare forretningsdokumenter](#list-of-configurations-cbd) nedenfor.

Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet i denne artikel.

## <a name="configure-er-parameters"></a>Konfigurere ER-parametre

Da styring af forretningsdokumenter er bygget oven på ER-strukturen, skal du konfigurere ER-parametrene for at begynde at arbejde med styring af forretningsdokumenter. Hvis du vil gøre dette, skal du konfigurere ER-parametrene som beskrevet i [Konfigurere strukturen for Elektronisk rapportering (ER)](electronic-reporting-er-configure-parameters.md). Du skal også tilføje en ny konfigurationsudbyder som beskrevet under [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER-arbejdsområde.](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>Importere ER-løsninger

Eksempel på ER-konfigurationer bruges i eksemplet med denne procedure. Du skal til din aktuelle forekomst af Dynamics 365 Finance importere de ER-konfigurationer, der indeholder de skabeloner for forretningsdokumenter, der kan redigeres ved hjælp af Styring af forretningsdokumenter. Download og gem derefter lokalt følgende filer for at fuldføre denne procedure.

**Eksempelløsning til ER-debitorfakturering**

| Filer                                      | Indhold |
|-------------------------------------------|---------|
| Debitorfaktureringsmodel.version.2.xml    | [ER-datamodelkonfiguration](https://download.microsoft.com/download/b/f/a/bfa5cb52-e6e2-42bc-a4c0-77014a4c54e6/Customerinvoicingmodel.version.2.xml) |
| FTI-debitorrapport (GER).version.2.3.xml | [Konfiguration af ER-format til fritekstfaktura](https://download.microsoft.com/download/3/c/2/3c2e58f2-6e56-43d9-85ea-4c97252a108d/CustomerFTIreportGER.version.2.3.xml) |

**Eksempelløsning til ER-betalingscheck**

| Filer                                     | Indhold |
|------------------------------------------|---------|
| Model for checks.version.10.xml         | [ER-datamodelkonfiguration](https://download.microsoft.com/download/3/7/6/376cb0f6-181a-4895-a432-390ffca64162/Modelforcheques.version.10.xml) |
| Checkudskrivningsformat.version.10.9.xml | [ER-konfigurationsformat for betalingscheck](https://download.microsoft.com/download/6/d/6/6d61bfff-3d89-4377-9e34-2e3ee6d6df91/Chequesprintingformat.version.10.9.xml) |

**Eksempelløsning til ER-udenrigshandel**

| Filer                             | Indhold |
|----------------------------------|---------|
| Intrastat-model.version.1.xml    | [ER-datamodelkonfiguration](https://download.microsoft.com/download/2/0/0/200d6ed1-eff8-48ec-ab75-175a4acf9714/Intrastatmodel.version.1.xml) |
| Intrastat-rapport.version.1.9.xml | [ER-formatkonfiguration af Intrastat-kontrolrapport](https://download.microsoft.com/download/7/a/2/7a2a27c3-a8a5-42a1-9d04-f0a8e1ec1707/Intrastatreport.version.1.9.xml) |

Benyt følgende fremgangsmåde for at importere de enkelte filer. Importér ER-konfigurationen af *datamodellen* for hver ER-løsning i tabellerne ovenfor, før du importerer den tilsvarende ER-*format*-konfiguration.

1. Åbn siden **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Vælg **Udveksling** øverst på siden.
3. Vælg **Indlæs fra XML-fil**.
4. Vælg **Gennemse** for at indlæse den påkrævede XML-fil.
5. Vælg **OK** for at bekræfte konfigurationens import.

![Bekræftelse af konfigurationsimport på siden ER-konfigurationer.](./media/BDM-Overview-ERSolutions.png)

Du kan også importere de officielt publicerede ER-formatkonfigurationer fra Microsoft Dynamics Lifecycle service (LCS). Hvis du f.eks. vil fuldføre denne procedure, kan du importere den seneste version af ER-formatkonfigurationen **Fritekstfaktura (Excel)**. Varianter af den tilsvarende ER-datamodel og konfigurationer af ER-modeltilknytninger importeres automatisk.

![Indholdssiden for delt LCS-aktivbibliotek.](./media/BDM-Overview-SharedAssetLibrary.png)

Du kan finde flere oplysninger om import af ER-konfigurationer under [Administrere livscyklus for ER-konfiguration](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>Aktivere styring af forretningsdokumenter

Hvis du vil starte styring af forretningsdokumenter, skal du åbne arbejdsområdet **Administration af funktioner** og aktivere funktionen **Styring af forretningsdokumenter**.

Benyt følgende fremgangsmåde for at aktivere funktionen til styring af forretningsdokumenter for alle juridiske enheder.

1. Åbn arbejdsområdet **Administration af funktioner**.
2. Vælg funktionen **Styring af forretningsdokumenter** på listen under fanen **Ny**.
3. Vælg **Aktivér nu** for at aktivere den valgte funktion.
4. Opdater siden for at få adgang til den nye funktion.

> [!NOTE]
> Yderligere oplysninger om brug af den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter finder du i [Ny brugergrænseflade i dokumenter i Styring af forretningsdokumenter](er-business-document-management-new-template-ui.md).

![Arbejdsområdet Administration af funktioner.](./media/BDM-Overview-FMEnabling.png)

Du kan finde flere oplysninger om aktivering af nye funktioner under [Oversigt over funktionsstyring](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Konfigurere parametre

Brug oplysningerne i følgende afsnit til at konfigurere de grundlæggende parametre for styring af forretningsdokumenter.

### <a name="prerequisites-for-parameter-setup"></a>Forudsætninger for parameteropsætning

Før du kan konfigurere styring af forretningsdokumenter, skal du konfigurere den ønskede dokumenttype i dokumentstyringsstrukturen. Denne dokumenttype bruges til at angive en midlertidig lagring af dokumenter i Office-formater (Excel og Word), der bruges som skabeloner for ER-rapporter. Skabelonen til midlertidig lagring kan redigeres ved hjælp af Office-skrivebordsprogrammer.

For denne dokumenttype skal følgende attributværdier vælges.

| Attributnavn | Attributværdi |
|----------------|-----------------|
| Klasse          | Vedlæg fil     |
| Multi          | Fil            |
| Adresse       | SharePoint      |

Du kan finde oplysninger om, hvordan du konfigurerer de påkrævede dokumentstyringsparametre og dokumenttyper, i [Konfigurere dokumentstyring](../../fin-ops/organization-administration/configure-document-management.md).

![Konfigurere dokumenttype til dokumentstyring.](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><a name="SetupBdmParameters"></a>Konfigurere parametre

De grundlæggende parametre til styring af forretningsdokumenter kan konfigureres på siden **Parametre for forretningsdokument**. Det er kun specifikke brugere, der har adgang til siden. Det omfatter:

- Brugere, der er tildelt rollen **Systemadministrator**.
- Brugere, der er tildelt en hvilken som helst rolle, der er konfigureret til at udføre opgaven **Vedligeholde parametre for styring af forretningsdokumenter** (AOT-navn **ERBDMaintainParameters**).

Benyt følgende fremgangsmåde til at konfigurere grundlæggende parametre for alle juridiske enheder.

1. Log på som bruger med adgang til siden **Parametre for forretningsdokument**.
2. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Styring af forretningsdokumenter** \> **Parametre for forretningsdokument**.
3. På siden **Parametre for forretningsdokument** skal du under fanen **Vedhæftede filer** i feltet **SharePoint-dokumenttype** definere den dokumenttype, der skal bruges til midlertidig lagring af skabeloner i Office-formater, mens de redigeres ved hjælp af Office-skrivebordsprogrammer. 

> [!NOTE]
> Det er kun de dokumenttyper, der er konfigureret ved hjælp af et SharePoint-sted, der er tilgængelige for denne parameter.

![Konfigurere parametre til styring af forretningsdokumenter.](./media/BDM-Overview-BDMSetting.png)

Den valgte dokumenttype er firmaspecifik og vil blive brugt, når brugeren arbejder med styring af forretningsdokumenter i det firma, som den valgte dokumenttype er konfigureret til. Når brugeren arbejder med styring af forretningsdokumenter i et andet firma, bruges den samme valgte dokumenttype, hvis der ikke er konfigureret nogen for dette firma. Når en dokumenttype er konfigureret, bruges den i stedet for den, der er valgt i feltet **SharePoint-dokumenttype**.

> [!NOTE]
> Parameteren **SharePoint-dokumenttype** definerer en SharePoint-mappe som et midlertidigt lagringssted til skabeloner, der kan redigeres ved hjælp af enten Microsoft Excel eller Word. Du skal konfigurere denne parameter, hvis du planlægger at bruge disse Office-skrivebordsprogrammer til redigering af skabeloner. Du kan finde flere oplysninger i [Redigere en skabelon i Office-skrivebordsprogrammet](#EditInOfficeDesktopApp). Du kan sørge for, at denne parameter er tom, hvis du planlægger at redigere skabelonen udelukkende ved hjælp af funktionaliteten i Microsoft 365. Du kan finde flere oplysninger i [Redigere en skabelon i Microsoft 365](#EditInOffice365).

## <a name="configure-access-permissions"></a>Konfigurere adgangstilladelser

Når adgangsrettigheder til forretningsdokumentstyring ikke er aktiveret, kan alle brugere med adgang til arbejdsområdet for forretningsdokumentstyring som standard se alle de ER-løsningsskabeloner, der er tilgængelige. Arbejdsområdet til styring af forretningsdokumenter viser kun de skabeloner, der er placeret i ER-formatkonfigurationer, og som er markeret som **Forretningsdokumenttype**.

![Siden ER-konfigurationer med tag til forretningsdokumenttype.](./media/BDM-Overview-ERFormatTags.png)

Listen over skabeloner, der er tilgængelige i arbejdsområdet for styring af forretningsdokumenter, kan begrænses ved at konfigurere adgangsrettigheder. Det kan være vigtigt, når der bruges forskellige skabeloner til at fremstille forretningsdokumenter for forskellige virksomhedsdomæner (funktionsområder), og du vil give bestemte brugere adgang til forskellige skabeloner til redigering i arbejdsområdet for styring af forretningsdokumenter.

Adgangstilladelser til forretningsdokumentstyring kan angives i **Konfigurator for adgangstilladelser**. Det er kun følgende brugere, der har adgang til siden:

- Brugere, der er tildelt rollen **Systemadministrator**.
- Brugere, der er tildelt en hvilken som helst anden rolle, der er konfigureret til at udføre opgaven **Konfigurere adgangstilladelser til redigering af skabeloner til forretningsdokumenter** (AOT-navn **ERBDTemplatesSecurity**).

Benyt følgende fremgangsmåde til at konfigurere adgangstilladelser til styring af forretningsdokumenter for alle juridiske enheder.

1. Log på som bruger med adgang til siden **Konfigurator for adgangstilladelser**.
2. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Styring af forretningsdokumenter** \> **Administrer adgangsrettigheder**.

    Vær opmærksom på beskeden om, at brugen af adgangsrettigheder til forretningsdokumentstyring ikke er aktiveret i øjeblikket.

    ![Konfiguratorside for adgangsrettigheder til forretningsdokumentstyring.](./media/BDM-Overview-TemplatesAccess1.png)

    Med denne indstilling kan alle brugere, der har fået tildelt en sikkerhedsrolle, der er konfigureret til at udføre opgaven **Administrer forretningsdokumentskabeloner** (AOT-navn **ERBDManageTemplates**), åbne forretningsdokumentstyringens arbejdsområde og kan redigere alle tilgængelige skabeloner.

    I følgende illustration vises, hvad der er tilgængeligt i arbejdsområdet til forretningsdokumentstyring for brugere, der er tildelt rollen **Debitorassistent**. Med de aktuelle indstillinger af adgangsrettigheder kan brugeren redigere forretningsdokumentskabeloner fra forskellige funktionsområder, herunder fakturering, lovpligtig rapportering og betalinger.

    ![Side med arbejdsområde til forretningsdokumentstyring for debitorassistent.](./media/BDM-Overview-TemplatesForAlice1.png)

3. Vælg **Indstillinger for adgangsrettigheder** på siden **Konfigurator for adgangstilladelser**.
4. I dialogboksen **Indstillinger for adgangsrettigheder til redigering af skabeloner** skal du aktivere indstillingen **Anvend konfigurerede adgangsrettigheder**.
5. Vælg **OK** for at bekræfte, at der er aktiveret adgangstilladelser til forretningsdokumentstyring.

    ![Bekræfte adgangsrettigheder til forretningsdokumentstyring.](./media/BDM-Overview-TemplatesAccess2.png)

6. Vælg **Tilføj** for at angive en ny forretningsrolle, der skal have konfigureret adgangsrettigheder til skabeloner for forretningsdokumentstyring.
7. I dialogboksen **Sikkerhedsroller** skal du vælge rollen **Debitorassistent** og derefter vælge **OK** for at bekræfte valget af rollen.
8. Vælg **Ny** under fanen **Adgangsrettigheder pr. konfigurationsmærkater**.
9. Vælg **Funktionsområde** i feltet **Mærkattype**, og vælg **Fakturering** i feltet **Id**.
10. Vælg **Gem** for at gemme de konfigurerede adgangsrettigheder for den valgte rolle.

    Den aktuelle indstilling betyder, at for en hvilken som helst bruger, der er tildelt rollen **Debitorassistent** og udfører pligten **Administrer forretningsdokumentskabeloner** (AOT-navn **ERBDManageTemplates**), vil ER-formatkonfigurationsskabeloner, der har værdien **Fakturering** for mærkatet **Funktionsområde**, kunne redigeres i arbejdsområdet for styring af forretningsdokumenter.

11. Skift til ruden **Relaterede oplysninger** fra højre side af den aktuelle side. I ruden **Relaterede oplysninger** kan du se, hvordan de konfigurerede adgangsrettigheder anvendes, herunder hvilke ER-konfigurationsskabeloner der er tilgængelige for brugere, der er tildelt rollen **Debitorassistent**.

    ![Ruden Relaterede oplysninger på siden Konfigurator for adgangstilladelser.](./media/BDM-Overview-TemplatesAccess3.png)

12. Vælg **Tilføj** under fanen **Adgangsrettigheder pr. konfigurationer**.
13. I dialogboksen **Vælg konfiguration** skal du markere **Intrastat-rapporten** som ER-formatkonfiguration.
14. Vælg **OK** for at bekræfte indtastningen af de valgte konfigurationer, og vælg **Gem** for at gemme de konfigurerede adgangsrettigheder for den valgte rolle.

Den aktuelle indstilling betyder, at for en hvilken som helst bruger, der er tildelt rollen **Debitorassistent** og udfører pligten **Administrer forretningsdokumentskabeloner** (AOT-navn **ERBDManageTemplates**), vil følgende skabeloner kunne redigeres i arbejdsområdet for styring af forretningsdokumenter:

- Skabeloner med værdien **Fakturering** for mærkatet **Funktionsområde**.
- Skabeloner fra ER-formatkonfigurationer, der vises under fanen **Adgangsrettigheder pr. konfigurationer** (skabeloner fra formatkonfigurationen **Intrastat-rapport** for domænet **Lovpligtig rapportering** i dette eksempel).

![Oversigtspaneler for adgangsrettigheder på siden Konfigurator for adgangstilladelser.](./media/BDM-Overview-TemplatesAccess4.png)

I følgende illustration vises, hvad der er tilgængeligt i arbejdsområdet til forretningsdokumentstyring for en bruger, der er tildelt rollen **Debitorassistent**. Med den aktuelle indstilling af adgangsrettigheder til forretningsdokumentstyring kan brugeren redigere forretningsdokumentskabeloner fra **Fakturering**-domænet og **Intrastat-rapporten** som ER-formatkonfiguration. Skabeloner fra domænet **Betalinger** er ikke tilgængelige for rollen **Debitorassistent**.

![Redigering af skabeloner til forretningsdokumenter i arbejdsområdet Styring af forretningsdokumenter.](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> Reglerne **Adgangsrettigheder pr. konfigurationer** gemmes ved hjælp af det entydige identifikations-id for en ER-formatkonfiguration. Dette betyder, at disse regler ikke slettes, når en ER-konfiguration, der refererer til dem, slettes. Når du importerer slettede konfigurationer tilbage til denne forekomst, refererer disse regler til dem igen. Det er ikke nødvendigt at konfigurere reglerne igen, når de slettede konfigurationer importeres igen.

## <a name="use-business-document-management-to-edit-templates"></a>Bruge styring af forretningsdokumenter til at redigere skabeloner

Forretningsbrugere kan få adgang til forretningsdokumentskabeloner til redigering i arbejdsområdet til styring af forretningsdokumenter. Det er kun følgende brugere, som kan få adgang til arbejdsområdet for forretningsdokumentstyring:

- Brugere, der er tildelt rollen **Systemadministrator**.
- Brugere, der er tildelt en hvilken som helst rolle, der er konfigureret til at udføre pligten **Administrer forretningsdokumentskabeloner** (AOT-navn **ERBDManageTemplates**).

Benyt følgende fremgangsmåde for at redigere skabeloner til fritekstfakturaer i arbejdsområdet til styring af forretningsdokumenter. Før du udfører denne procedure, skal du have fuldført alle de foregående procedurer i denne artikel.

1. Log på som bruger med adgang til arbejdsområdet til styring af forretningsdokumenter.
2. Åbn arbejdsområdet til styring af forretningsdokumenter.

Når funktionen **Office-lignende brugergrænsefladeoplevelse for styring af forretningsdokumenter** er slået fra i arbejdsområdet **Funktionsstyring**, viser hovedgitteret i arbejdsområdet **Styring af forretningsdokumenter** følgende skabeloner:

- Skabeloner, som ejes af din ER-konfigurationsleverandør (dvs. den udbyder, der aktuelt er markeret som aktiv i arbejdsområdet **Elektronisk rapportering**). Når du har valgt en af disse skabeloner, kan du vælge **Rediger skabelon** for at starte eller fortsætte med at redigere den.
- Skabeloner, der ejes af andre ER-konfigurationsudbydere. Når du har valgt en af disse skabeloner, kan du vælge **Nyt dokument** for at oprette en kopi af det, der ejes af din ER-konfigurationsudbyder, og derefter begynde at redigere kopien.

![Skabelonliste på siden i arbejdsområdet Styring af forretningsdokument.](./media/BDM-Overview-EditingTemplate1.png)

Fanen **Skabelon** viser indholdet af den valgte skabelon. Vælg fanen **Detaljer** for at få vist oplysninger om den valgte skabelon samt detaljer om en ER-formatkonfiguration, som denne skabelon er placeret i. Bemærk, at alle skabelonerne har statussen **Udgivet** og ikke indeholder nogen detaljer i kolonnen **Revision**. Det betyder, at disse skabeloner ikke redigeres i øjeblikket.

Når funktionen **Office-lignende brugergrænsefladeoplevelse for styring af forretningsdokumenter** er slået til i **Funktionsstyring**, viser hovedgitteret i arbejdsområdet **Styring af forretningsdokumenter** skabeloner, der ejes af din ER-konfigurationsudbyder (dvs. den udbyder, der aktuelt er markeret som aktiv i arbejdsområdet **Elektronisk rapportering**). Når du har valgt en af disse skabeloner, kan du vælge **Rediger skabelon** for at starte eller fortsætte med at redigere den.

Hvis du vil arbejde med skabeloner, der ejes af andre ER-konfigurationsudbydere, skal du vælge **Nyt dokument** for at oprette en kopi af den skabelon, der ejes af din ER-udbyder. Du kan derefter starte med at redigere kopier. Du kan få flere oplysninger i [Brugergrænseflade for nyt dokument i styring af forretningsdokumenter](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Starte redigering af skabeloner, der ejes af din konfigurationsudbyder

1. I arbejdsområdet til styring af forretningsdokumenter skal du vælge skabelonen **Checkudskrivningsformat** på listen.
2. Vælg fanen **Detaljer**.

![Side med arbejdsområde til styring af forretningsdokumenter, fanen Detaljer.](./media/BDM-Overview-EditingTemplate2.png)

Indstillingen **Rediger skabelon** er tilgængelig for den valgte skabelon. Denne indstilling er altid tilgængelig for en skabelon i en ER-formatkonfiguration, der ejes af den aktive ER-konfigurationsudbyder **(Litware, Inc.** i dette eksempel). Når du vælger **Rediger skabelon**, vil den eksisterende skabelon fra kladdeversionen af den underliggende ER-formatkonfiguration være tilgængelig for redigering.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Starte redigering af skabeloner, der ejes af andre udbydere

1. Vælg det dokument, du vil bruge som skabelon, i arbejdsområdet til Styring af forretningsdokumenter.

    ![Vælge et dokument på siden i arbejdsområdet Styring af forretningsdokumenter.](./media/BDM-Overview-EditingTemplate3.png)

2. Vælg **Nyt dokument**, og rediger titlen på den redigerbare skabelon i feltet **Titel**, hvis det er nødvendigt. Teksten vil blive brugt til at navngive den ER-formatkonfiguration, der oprettes automatisk. Bemærk, at kladdeversionen af denne konfiguration (**FTI-debitorrapport (GER) Kopi**), der vil indeholde den redigerede skabelon, automatisk markeres til at køre dette ER-format for den aktuelle bruger. Samtidig bruges den ikke-redigerede oprindelige skabelon fra ER-basisformatkonfigurationen til at køre dette ER-format for enhver anden bruger.
3. I feltet **Navn** skal du ændre navnet på den første revision af den redigerbare skabelon, der oprettes automatisk.
4. I feltet **Kommentar** skal du ændre kommentaren til den automatisk oprettede revision af den redigerbare skabelon.
5. Vælg **OK** for at bekræfte starten af redigeringsprocessen.

![Bekræfte starten af redigeringsprocessen for at oprette en ny skabelon.](./media/BDM-Overview-EditingTemplate4.png)

Hvis der ikke er nogen udbyder, vil den blive tilbudt at oprette. Hvis der ikke er nogen aktiv udbyder, vil den blive tilbudt at vælge den til aktivering.

Hvis du vil oprette en udbyder, skal du ændre navnet på udbyderen i feltet **Navn**, opdatere den nye udbyders internetadresse i feltet **Internetadresse** og vælge **OK** for at bekræfte.

   ![Oprette en ny udbyder i BDM.](./media/bdm_create_provider.png)

Hvis du vil aktivere en eksisterende udbyder, skal du vælge navnet på udbyderen i feltet **Konfigurationsudbyder** og vælge **OK** for at indstille udbyderen til aktiv.

   ![Aktivere udbyder i BDM.](./media/bdm_choose_provider.png)

> [!NOTE]
> Hver BDM-skabelon refererer til udbyderen som konfigurations forfatter. Derfor kræves der en aktiv udbyder for skabelonen.


Indstillingen **Nyt dokument** er altid tilgængelig for en skabelon i en ER-formatkonfiguration, der er leveret af den aktuelle udbyder og en anden udbyder (Microsoft i dette eksempel), som ikke har nogen revision. Den redigerede skabelon gemmes derefter i en ny ER-formatkonfiguration, der genereres automatisk.



### <a name="start-editing-a-template"></a>Starte redigering af en skabelon

1. I den valgte skabelon skal du vælge **Rediger dokument**.
2. I feltet **Navn** skal du ændre navnet på den første revision af den redigerbare skabelon, der oprettes automatisk.
3. I feltet **Kommentar** skal du ændre bemærkningen til den automatisk oprettede revision af den redigerbare skabelon.

    ![Redigering af en skabelon på siden i arbejdsområdet Styring af forretningsdokument.](./media/BDM-Overview-EditingTemplate5.png)

4. Vælg **OK** for at bekræfte starten af redigeringsprocessen.

Siden **BDM-skabeloneditor** åbnes. Den valgte skabelon er tilgængelig for online redigering ved hjælp af Microsoft 365.

![Side med skabeloneditor til styring af forretningsdokumenter.](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-microsoft-365"></a><a name="EditInOffice365"></a>Redigere en skabelon i Microsoft 365

Du kan redigere skabelonen ved hjælp af Microsoft 365. I Office Online kan du f.eks. ændre skrifttypen i feltprompterne i skabelonoverskriften fra **Normal** til **Fed**. Disse ændringer gemmes automatisk i den redigerbare skabelon, der er gemt i den primære skabelons lager (som standard Azure Blob Storage). Dette er konfigureret for ER-strukturen.

![Ændring af skrifttypen til fed i skabelonhovedet på siden til skabeloneditoren til Forretningsdokumentstyring.](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><a name="EditInOfficeDesktopApp"></a>Redigere en skabelon i Office-skrivebordsprogrammet

> [!NOTE]
> Denne funktion er kun tilgængelig, når parameteren **SharePoint-dokumenttype** er konfigureret korrekt. Du kan finde flere oplysninger i [Konfigurere parametre](#SetupBdmParameters).

1. Vælg indstillingen **Åbn i skrivebordsapp** for at ændre skabelonen ved hjælp af funktionerne i Office-skrivebordsprogrammet (Excel i dette eksempel). Den redigerbare skabelon kopieres fra det permanente lager til det midlertidige lager, der er konfigureret i parametrene for forretningsdokumentstyring, som en SharePoint-mappe.
2. Bekræft, at du vil åbne skabelonen fra det midlertidige fillager i Office-skrivebordsprogrammet Excel.

    ![Skabelon, der åbnes i et Excel-skrivebordsprogram.](./media/BDM-Overview-EditingLayout3.png)

3. Rediger skabelonen. Du kan du f.eks. ændre skrifttypen i feltprompterne i skabelonoverskriften ved at opdatere farven fra **Sort** til **Blå**.

    ![Redigere skriftfarven i skabelonhovedet ved hjælp af Excel-skrivebordsprogrammet.](./media/BDM-Overview-EditingLayout4.png)

4. Vælg **Gem** i Excel-skrivebordsprogrammet for at gemme skabelonændringerne i det midlertidige lager.

    ![Gemme ændringer på siden til skabeloneditoren til Forretningsdokumentstyring ved hjælp af Excel-programmet.](./media/BDM-Overview-EditingLayout5.png)

5. Luk Excel-skrivebordsprogrammet.
6. Vælg **Synkroniser gemt kopi** for at synkronisere det midlertidige skabelonlager med det permanente skabelonlager.

> [!NOTE]
> Kopien af den redigerbare skabelon i det midlertidige fillager opbevares kun for den aktuelle session med skabelonredigering. Når du afslutter denne session ved at lukke siden **BDM-skabeloneditor**, slettes denne kopi. Hvis du har justeret skabelonen i det midlertidige fillager, og du ikke vælger **Synkroniser gemt kopi**, når du forsøger at lukke siden med **BDM-skabeloneditoren**, bliver du spurgt, om du vil gemme de indsatte ændringer. Vælg **Ja**, hvis du vil gemme ændringerne af skabelonen på den permanente filplacering.

### <a name="validate-a-template"></a>Validere en skabelon

1. På siden **BDM-skabeloneditor** skal du vælge **Søg efter fejl** for at validere den ændrede skabelon i forhold til den underliggende ER-formatkonfiguration. Følg anbefalingerne, hvis det er relevant, for at justere skabelonen med formatstrukturen fra ER-basisformatkonfigurationen.
2. Vælg **Vis format** for at få vist formatets aktuelle struktur fra den ER-basisformatkonfigurationen, der skal justeres i forhold til den redigerbare skabelon. 
3. Vælg **Skjul format** for at lukke ruden.

    ![Siden med BDM-skabeloneditor.](./media/BDM-Overview-EditingTemplate6.png)

4. Luk siden **BDM-skabeloneditor**.

Den opdaterede skabelon vises under fanen **Skabelon**. Bemærk, at status for den redigerede skabelon nu er **Kladde**, og at den aktuelle revision ikke længere er tom. Det betyder, at processen for redigering af denne skabelon er startet.

![Se den opdaterede skabelon på siden i arbejdsområdet Styring af forretningsdokument.](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Teste den ændrede skabelon 

1. I programmet skal du skifte til firmaet, **USMF.**
2. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
3. Vælg fakturaen **FTI-00000002**, og vælg derefter **Udskriftsstyring**.
4. Vælg **Modul - debitor** \> **Dokumenter** \> **Fritekstfaktura** \> **Originaldokument** som niveau for at angive omfanget af fakturaer til behandling.
5. I feltet **Rapportformat** skal du vælge **FTI-debitorrapport (GER) Kopi** som ER-formatet for det angivne dokumentniveau.

    ![Side med indstillinger for udskriftsstyring.](./media/BDM-Overview-TestRun1.png)

6. Tryk på **Escape** for at lukke den aktuelle side.
7. Vælg **Udskriv**, og vælg derefter **Valgt**.
8. Download dokumentet, og åbn det i Excel-skrivebordsprogrammet.

![Siden med fritekstfakturaer.](./media/BDM-Overview-TestRun2.png)

Den ændrede skabelon bruges til at generere rapporten med fritekstfaktura for den valgte vare. Hvis du vil analysere, hvordan denne rapport påvirkes af de ændringer, du har introduceret i skabelonen, kan du køre denne rapport i én programsession direkte, efter at du har ændret skabelonen i en anden programsession.

### <a name="create-an-alternative-template-revision"></a>Oprette en alternativ skabelonrevision

1. Åbn siden **BDM-skabeloneditor**, og vælg skabelonen **FTI-debitorrapport (GER) Kopi** .
2. Vælg **Ny** under fanen **Revisioner**.
3. Hvis det er nødvendigt, skal du ændre navnet på den anden revision i feltet **Navn** og basere den på den aktuelt aktive første revision.
4. I feltet **Kommentar** skal du efter behov ændre bemærkningen til den automatisk oprettede revision af den redigerbare skabelon.

    ![Oprette revideringer af skabelonen på siden i arbejdsområdet Styring af forretningsdokument.](./media/BDM-Overview-AddRevision.png)

    Du har oprettet en ny revision af skabelonen, der er gemt i den permanente skabelons lager. Nu kan du fortsætte med at redigere skabelonen for den anden revision, der aktuelt er valgt som aktiv.

5. Vælg den første revision, og vælg derefter **Angiv som aktiv**. Du kan vælge en anden revision som aktiv, hvis du på et tidspunkt vil vende tilbage til denne revision af skabelonen.
6. Vælg den anden revision, og vælge derefter **Slet**.
7. Vælg **OK** for at bekræfte, at du vil slette den valgte revision. Du kan slette alle de ikke-aktive revisioner, når der ikke længere er brug for dem.

### <a name="delete-a-modified-template"></a>Slette en ændret skabelon

1. Vælg fanen **Skabelon** på siden **BDM-skabeloneditor**.
2. Vælg **Slet**.
3. Hvis du vælger **OK** for at bekræfte sletningen, slettes ER-formatet **FTI-debitorrapport (GER) Kopi** sammen med den ændrede skabelon. Vælg **Annuller** for at se andre indstillinger.

### <a name="revoke-changes-of-template"></a>Tilbagekalde ændringer af skabelon

Når du redigerer skabelonen fra et ER-format, der ejes af den aktuelle aktive udbyder, får du mulighed for at tilbagekalde ændringer, der er introduceret i skabelonen.

![Afvise ændringer af skabelonen på siden i arbejdsområdet Styring af forretningsdokument.](./media/BDM-Overview-RevokeChanges.png)

1. Vælg fanen **Skabelon** på siden **BDM-skabeloneditor**.
2. Vælg **Fortryd**.
3. Hvis du vælger **OK** for at annullere de ændringer, der er introduceret for skabelonen, erstattes den ændrede skabelon med den oprindelige skabelon, og alle ændringer fjernes. Når du tilbagekalder ændringer til skabelonen, kan du slette skabelonen. Vælg **Annuller** for at se andre indstillinger.

### <a name="publish-a-modified-template"></a>Udgive en ændret skabelon

1. Vælg fanen **Udgiv** under fanen **Skabelon** på siden **BDM-skabeloneditor**.
2. Hvis du vælger **OK** for at bekræfte udgivelsen, markeres kladdeversionen af det afledte **FTI-debitorrapport (GER) Kopi**-ER-format, som indeholder den ændrede skabelon, som fuldført. Den ændrede skabelon bliver tilgængelig for andre brugere. De fuldførte versioner af dette ER-format bevarer kun den sidst aktive revision af skabelonen. Andre revisioner vil blive slettet. Vælg **Annuller** for at se andre indstillinger.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="i-selected-edit-document-but-instead-of-going-to-the-bdm-template-editor-page-in-finance-i-was-sent-to-the-microsoft-365-webpage"></a>Jeg valgte Rediger dokument, men i stedet for at åbne siden BDM-skabeloneditor i Finans, blev jeg sendt til Microsoft 365-websiden.

Dette er et kendt problem i Microsoft 365-omdirigeringen. Dette sker, når du logger på Microsoft 365 for første gang. Du kan løse dette problem ved at vælge **Tilbage** i browseren for at vende tilbage til forrige side.

### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-and-adjust-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-use-the-office-desktop-application-in-the-same-way"></a>Jeg forstår, hvordan jeg kan redigere en skabelon ved at bruge Microsoft 365 i den første programsession, og hvordan jeg kan bruge skabelonen i den anden programsession og justere skabelonen for at se, hvordan mine ændringer påvirker det genererede forretningsdokument. Kan jeg bruge Office-skrivebordsapplikationen på samme måde?

Ja, det kan du. Vælg **Åbn i skrivebordsapp** i den første programsession. Skabelonen gemmes i det midlertidige fillager og åbnes i Office-skrivebordsprogrammet. Udfør derefter følgende trin for at se dine skabelonændringer i det genererede forretningsdokument:

1. Foretag ændringer i skabelonen ved hjælp af Office-skrivebordsprogrammet.
2. Vælg **Gem** i Office-skrivebordsprogrammet.
3. Vælg **Synkroniser gemt kopi** på siden **BDM-skabeloneditor** i den første programsession.
4. Udfør dette skabelon-ER-format i den anden programsession.

### <a name="when-i-select-open-in-desktop-app-i-receive-the-following-error-message-value-cannot-be-null-parameter-name-externalid-how-do-i-work-around-this-issue"></a>Når jeg vælger Åbn i skrivebordsapp, modtager jeg følgende fejlmeddelelse: "Værdien kan ikke være null. Parameternavn: externalId." Hvordan retter jeg denne fejl?

Du har højst sandsynligt logget på den aktuelle forekomst af appen i et Azure AD-domæne, der er forskelligt fra det Azure AD-domæne, der blev brugt til at installere denne forekomst. Da SharePoint-tjenesten, der bruges til at gemme skabeloner for at gøre dem tilgængelige for redigering ved hjælp af Office-skrivebordsprogrammer, tilhører det samme domæne, har vi ingen adgangsrettigheder til SharePoint-tjenesten. Du kan løse dette problem ved at logge på den aktuelle forekomst ved hjælp af legitimationsoplysningerne for en bruger med det korrekte Azure AD-domæne.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Designe en ER-konfiguration til generering af rapporter i OPENXML-format (november 2016)](tasks/er-design-reports-openxml-2016-11.md)

[Designe ER-konfigurationer til at generere rapporter i Word-format](tasks/er-design-configuration-word-2016-11.md)

[Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md)

[Konfigurere elektronisk rapportering (ER) for at trække data ind i Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)

## <a name="list-of-er-configurations-that-have-been-released-in-finance-to-support-configurable-business-documents"></a><a name="list-of-configurations-cbd"></a>Liste over ER-konfigurationer, der er udgivet i Finans for at understøtte konfigurerbare forretningsdokumenter

[Listen](general-electronic-reporting.md#list-of-configurations) over ER-konfigurationer for Finans opdateres konstant. Åbn det [globale lager](er-download-configurations-global-repo.md) for at gennemgå listen over ER-konfigurationer, der understøttes i øjeblikket. Du kan [filtrere](../../../finance/localizations/enhanced-filtering-global-repo.md) det globale lager for at gennemgå listen over ER-konfigurationer, der bruges til at understøtte forretningsdokumenter, der kan konfigureres.

![Filtrering af indholdet af det globale lager på siden Konfigurationslager.](./media/bdm-overview-filterglobalrepo.gif)

Følgende tabel viser listen over ER-konfigurationer, der understøtter konfigurerbare forretningsdokumenter, og som er frigivet i Finans indtil december 2020.

| Datamodelkonfiguration    | Formatkonfigurationer                           |
|-----------------------------|-------------------------------------------------|
| Fragtseddelmodel        | Fragtseddel (Excel)                          |
|                             | Fragtseddel (Word)                           |
| Model for oprindelsescertifikat | Oprindelsescertifikat (Excel)                   |
|                             | Oprindelsescertifikat (Word)                    |
| Fakturamodel               | Kundedebetnota og kreditnota (Excel)          |
|                             | Kundedebetnota og kreditnota (Word)           |
|                             | Fritekstfaktura (Excel)                       |
|                             | Fritekstfaktura (Excel) (BH)                  |
|                             | Fritekstfaktura (FR) (Excel)                  |
|                             | Fritekstfaktura (LT) (Excel)                  |
|                             | Fritekstfaktura (LV) (Excel)                  |
|                             | Fritekstfaktura (PL) (Excel)                  |
|                             | Fritekstfaktura (CZ) (Excel)                  |
|                             | Fritekstfaktura (EE) (Excel)                  |
|                             | Fritekstfaktura (HU) (Excel)                  |
|                             | Fritekstfaktura (TH) (Excel)                  |
|                             | Fritekstfaktura (Word)                        |
|                             | Linjeelementer i projektkontrakt (Excel)             |
|                             | Linjeelementer i projektkontrakt (CZ) (Excel)        |
|                             | Linjeelementer i projektkontrakt (Excel) (BH)        |
|                             | Linjeelementer i projektkontrakt (HU) (Excel)        |
|                             | Linjeelementer i projektkontrakt (LT) (Excel)        |
|                             | Linjeelementer i projektkontrakt (PL) (Excel)        |
|                             | Linjeelementer i projektkontrakt (Word)              |
|                             | Frigivelse af tilbageholdelse af projektkunde (Excel)      |
|                             | Frigivelse af tilbageholdelse af projektkunde (CZ) (Excel) |
|                             | Frigivelse af tilbageholdelse af projektkunde (HU) (Excel) |
|                             | Frigivelse af tilbageholdelse af projektkunde (LT) (Excel) |
|                             | Frigivelse af tilbageholdelse af projektkunde (PL) (Excel) |
|                             | Frigivelse af tilbageholdelse af projektkunde (TH) (Excel) |
|                             | Frigivelse af tilbageholdelse af projektkunde (Word)       |
|                             | Projektfaktura (Excel)                         |
|                             | Projektfaktura (Word)                          |
|                             | Projektfaktura (AE) (Excel)                    |
|                             | Projektfaktura (CZ) (Excel)                    |
|                             | Projektfaktura (Excel) (BH)                    |
|                             | Projektfaktura (HU) (Excel)                    |
|                             | Projektfaktura (JP) (Excel)                    |
|                             | Projektfaktura (LT) (Excel)                    |
|                             | Projektfaktura (PL) (Excel)                    |
|                             | Projektfaktura (TH) (Excel)                    |
|                             | Fuld projektfaktura (MY) (Excel)               |
|                             | Simpel projektfaktura (MY) (Excel)             |
|                             | Projektstyringsfaktura (Excel)                  |
|                             | Projektstyringsfaktura (CZ) (Excel)             |
|                             | Projektstyringsfaktura (Excel) (BH)             |
|                             | Projektstyringsfaktura (HU) (Excel)             |
|                             | Projektstyringsfaktura (JP) (Excel)             |
|                             | Projektstyringsfaktura (LT) (Excel)             |
|                             | Projektstyringsfaktura (PL) (Excel)             |
|                             | Projektstyringsfaktura (Word)                   |
|                             | Indkøbsforskudsfaktura (Excel)                |
|                             | Indkøbsforskudsfaktura (Word)                 |
|                             | Faktura for salgsforskud (Excel)                   |
|                             | Faktura for salgsforskud (Word)                    |
|                             | Faktura for salgsforskud (PL) (Excel)              |
|                             | Salgsfaktura (Excel)                           |
|                             | Salgsfaktura (Excel) (BH)                      |
|                             | Salgsfaktura (Excel) (CZ)                      |
|                             | Salgsfaktura (Excel) (EE)                      |
|                             | Salgsfaktura (Excel) (FR)                      |
|                             | Salgsfaktura (Excel) (HU)                      |
|                             | Salgsfaktura (Excel) (IN)                      |
|                             | Salgsfaktura (Excel) (LT)                      |
|                             | Salgsfaktura (Excel) (LV)                      |
|                             | Salgsfaktura (Excel) (PL)                      |
|                             | Salgsfaktura (Excel) (TH)                      |
|                             | Salgsfaktura (Word)                            |
|                             | TMS-handelsfaktura (Excel)                  |
|                             | TMS-handelsfaktura (Word)                   |
|                             | Dokument til kreditorfaktura (Excel)                 |
|                             | Dokument til kreditorfaktura (CZ) (Excel)            |
|                             | Dokument til kreditorfaktura (HU) (Excel)            |
|                             | Dokument til kreditorfaktura (IN) (Excel)            |
|                             | Dokument til kreditorfaktura (LT) (Excel)            |
|                             | Dokument til kreditorfaktura (LV) (Excel)            |
|                             | Dokument til kreditorfaktura (MY) (Excel)            |
|                             | Dokument til kreditorfaktura (Word)                  |
| Ordremodel                 | Aftalebekræftelse (Excel)                  |
|                             | Aftalebekræftelse (Word)                   |
|                             | Købsaftalebekræftelse (Excel)         |
|                             | Købsaftalebekræftelse (Word)          |
|                             | Indkøbsordre (Excel)                          |
|                             | Indkøbsordre (CZ) (Excel)                     |
|                             | Forespørgsel på indkøbsordre (CZ) (Excel)             |
|                             | Indkøbsordre (HU) (Excel)                     |
|                             | Forespørgsel på indkøbsordre (HU) (Excel)             |
|                             | Indkøbsordre (Word)                           |
|                             | Forespørgsel på indkøbsordre (Excel)                  |
|                             | Forespørgsel på indkøbsordre (Word)                   |
|                             | Salgsordrebekræftelse (Excel)                |
|                             | Salgsordrebekræftelse (CZ) (Excel)           |
|                             | Salgsordrebekræftelse (HU) (Excel)           |
|                             | Salgsordrebekræftelse (Word)                 |
| Pakkelistemodel          | Containerindhold (Excel)                      |
|                             | Containerindhold (Word)                       |
|                             | Lastliste (Excel)                               |
|                             | Lastliste (Word)                                |
|                             | Plukliste (Excel)                            |
|                             | Plukliste (CZ) (Excel)                       |
|                             | Plukliste (Word)                             |
|                             | Produktionsplukliste (Excel)                    |
|                             | Produktionsplukliste (Word)                     |
|                             | Plukliste til forsendelse af last (Excel)             |
|                             | Plukliste til forsendelse af last (Word)              |
|                             | Plukliste til forsendelse (Excel)         |
|                             | Plukliste til forsendelse (Word)          |
|                             | Plukliste til forsendelse af bølge (Excel)             |
|                             | Plukliste til forsendelse af bølge (Word)              |
| Betalingsmodel               | Debitorbetalingsvejledning (Excel)                 |
|                             | Debitorbetalingsvejledning (Word)                  |
|                             | Kreditorbetalingsvejledning (Excel)                   |
|                             | Kreditorbetalingsvejledning (Word)                    |
| Tilbudsmodel             | Projekttilbud (Excel)                       |
|                             | Projekttilbud (Word)                        |
|                             | Tilbudsanmodning (Excel)                   |
|                             | Tilbudsanmodning (acceptér) (Excel)          |
|                             | Tilbudsanmodning (acceptér) (Word)           |
|                             | Tilbudsanmodning (afvis) (Excel)          |
|                             | Tilbudsanmodning (afvis) (Word)           |
|                             | Tilbudsanmodning (returner) (Excel)          |
|                             | Tilbudsanmodning (returner) (Word)           |
|                             | Tilbudsanmodning (Word)                    |
|                             | Salgstilbud (Excel)                         |
|                             | Salgstilbud (CZ) (Excel)                    |
|                             | Salgstilbud (HU) (Excel)                    |
|                             | Salgstilbud (Word)                          |
|                             | Bekræftelse af salgstilbud (Excel)            |
|                             | Bekræftelse af salgstilbud (Word)             |
| Afstemningsmodel        | Kundekontoudtog, eksternt (Excel)             |
|                             | Kundekontoudtog, eksternt (CN) (Excel)        |
|                             | Kundekontoudtog, eksternt (Word)              |
|                             | Kundekontoudtog, Frankrig (Excel)          |
| Påmindelsesmodel              | Rykkernota (Excel)                  |
|                             | Rykkernota (CN) (Excel)             |
|                             | Rykkernota (Word)                   |
|                             | Debitorrentenota (Excel)                  |
|                             | Debitorrentenota (Word)                   |
| Fragtbrevmodel               | Lasttilbud (Excel)                             |
|                             | Lasttilbud (Word)                              |
|                             | Følgeseddel til indkøbsordre (Excel)             |
|                             | Følgeseddel til indkøbsordre (CZ) (Excel)        |
|                             | Følgeseddel til indkøbsordre (Word)              |
|                             | Rute (Excel)                                   |
|                             | Rute (Word)                                    |
|                             | Salgsordrefølgeseddel (Excel)                |
|                             | Salgsordrefølgeseddel (CZ) (Excel)           |
|                             | Salgsordrefølgeseddel (LT) (Excel)           |
|                             | Salgsordrefølgeseddel (PL) (Excel)           |
|                             | Salgsordrefølgeseddel (Word)                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
