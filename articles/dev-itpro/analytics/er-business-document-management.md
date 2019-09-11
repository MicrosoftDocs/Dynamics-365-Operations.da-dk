---
title: Oversigt over styring af forretningsdokumenter
description: Dette emne indeholder oplysninger om, hvordan du kan bruge funktionen til styring af forretningsdokumenter i ER-strukturen.
author: NickSelin
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d756436373b10f9538788a3292135a73c9c45d04
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873147"
---
# <a name="business-document-management-overview"></a>Oversigt over styring af forretningsdokumenter

Forretningsbrugere benytter det [elektroniske rapporteringsværktøjs struktur (ER)](general-electronic-reporting.md) til at konfigurere formater for udgående elektroniske dokumenter i overensstemmelse med de lovgivningsmæssige krav i forskellige lande/områder. Brugerne kan også definere dataflow for at angive, hvilke programdata der skal placeres i genererede dokumenter. ER-strukturen genererer udgående dokumenter i Microsoft Office-formater (Excel-projektmapper eller Word-dokumenter) ved hjælp af foruddefinerede skabeloner. Skabelonerne udfyldes med de påkrævede data i overensstemmelse med det konfigurerede dataflow, mens de nødvendige dokumenter genereres. Hvert konfigurerede format kan udgives som en del af en ER-løsning til generering af specifikke udgående dokumenter. Dette repræsenteres ved en ER-formatkonfiguration, der kan indeholde skabeloner, som du kan bruge til at generere forskellige udgående dokumenter. Erhvervsbrugere kan benytte denne struktur til at administrere nødvendige forretningsdokumenter.

**Styring af forretningsdokumenter** er bygget oven på ER-strukturen og gør det muligt for erhvervsbrugere at redigere forretningsdokumentskabeloner i Microsoft Office 365-tjenesten eller Microsoft Office-skrivebordsprogrammet. Ændringer i dokumenterne kan omfatte ændring af forretningsdokumentdesign og tilføjelse af pladsholdere til yderligere data inde fra Dynamics 365 for Finance and Operations uden ændringer af kildekode og nye installationer. Det er ikke nødvendigt at have kendskab til ER-strukturen for at opdatere skabeloner til forretningsdokumenter.

> [!NOTE]
> Vær opmærksom på, at styring af forretningsdokumenter giver dig mulighed for at redigere skabeloner, der bruges til at fremstille forretningsdokumenter som f.eks. ordrer, fakturaer osv. Mens en skabelon er ændret, og der er udgivet en ny version af den, bruges denne version til at oprette nødvendige forretningsdokumenter. Styring af forretningsdokumenter kan ikke bruges til at redigere allerede genererede forretningsdokumenter.

## <a name="supported-deployments"></a>Understøttede installationer

I øjeblikket er funktionen til styring af forretningsdokumenter kun implementeret i skyinstallationer. Hvis denne funktion er vigtig for din lokale installation, skal du give os besked via feedback på webstedet [Idéer](https://experience.dynamics.com/ideas/).

## <a name="supported-microsoft-office-applications"></a>Understøttede Microsoft Office-applikationer

Hvis du vil bruge styring af forretningsdokumenter til redigering af skabeloner i Excel eller Word ved hjælp af Microsoft Office-skrivebordsprogrammer, skal du have Microsoft Office 2010 eller nyere installeret. Dette understøttes i skyinstallationer og lokale installationer af Finance and Operations.

## <a name="business-document-availability"></a>Tilgængelighed af forretningsdokument

Følgende rapporter vil blive tilgængelige med Excel-baserede skabeloner med udgivelsen af den offentlige prøveversion:

**Debitor** (august 2019)

- Faktura for salgsforskud
- Salgsordrefølgeseddel

**Kreditor** (august 2019)

- Indkøbsforskudsfaktura
- Indkøbsordre
- Følgeseddel til indkøbsordre

Flere rapporter vil blive tilgængelige. Der vil blive udsendt særlige beskeder om flere rapporter separat. 

En komplet liste over alle rapporter, der er planlagt for udgaven i oktober 2019, findes i [Konfigurerbar rapportering af forretningsdokumenter i Word og Excel](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

# <a name="example-enable-configure-and-use-business-document-management"></a>Eksempel: aktivere, konfigurere og bruge styring af forretningsdokumenter

Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet i dette emne.

## <a name="configure-er-parameters"></a>Konfigurere ER-parametre

Da styring af forretningsdokumenter er bygget oven på ER-strukturen, skal du konfigurere ER-parametrene for at begynde at arbejde med styring af forretningsdokumenter. Hvis du vil gøre dette, skal du konfigurere ER-parametrene som beskrevet i [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md). Du skal også tilføje en ny konfigurationsudbyder som beskrevet under [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER-arbejdsområde](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>Importere ER-løsninger

Du skal importere ER-konfigurationer, der indeholder skabeloner for forretningsdokumenter, til den aktuelle forekomst af Finance and Operations. Download og gem lokalt følgende filer for at fuldføre denne procedure.

**Eksempelløsning til ER-debitorfakturering**

| **Filer**                                  | **Indhold**                                |
|-------------------------------------------|--------------------------------------------|
| Debitorfaktureringsmodel.version.2.xml    | [ER-datamodelkonfiguration](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| FTI-debitorrapport (GER).version.2.3.xml | [Konfiguration af ER-format til fritekstfaktura](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Eksempelløsning til ER-betalingscheck**

| **Filer**                                  | **Indhold**                                |
|-------------------------------------------|--------------------------------------------|
| Model for checks.version.10.xml          | [ER-datamodelkonfiguration](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Checkudskrivningsformat.version.10.9.xml  | [ER-konfigurationsformat for betalingscheck](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Eksempelløsning til ER-udenrigshandel**

| **Filer**                                  | **Indhold**                                |
|-------------------------------------------|--------------------------------------------|
| Intrastat-model.version.1.xml             | [ER-datamodelkonfiguration](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Intrastat-rapport.version.1.9.xml          | [ER-formatkonfiguration af Intrastat-kontrolrapport](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Benyt følgende fremgangsmåde for at importere de enkelte filer. Importér ER-konfigurationen af *datamodellen* for hver ER-løsning i tabellerne ovenfor, før du importerer den tilsvarende ER-*format*konfiguration.

1. Åbn siden **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Vælg **Udveksling** øverst på siden.
3. Vælg **Indlæs fra XML-fil**.
4. Vælg **Gennemse** for at indlæse den påkrævede XML-fil.
5. Vælg **OK** for at bekræfte konfigurationsimporten.

![Siden ER-konfigurationer](./media/BDM-Overview-ERSolutions.png)

Du kan finde flere oplysninger om import af ER-konfigurationer under [Administrere livscyklus for ER-konfiguration](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>Aktivere styring af forretningsdokumenter

Hvis du vil starte styring af forretningsdokumenter, skal du åbne arbejdsområdet **Administration af funktioner** og aktivere funktionen **Styring af forretningsdokumenter**.

Benyt følgende fremgangsmåde for at aktivere funktionen til styring af forretningsdokumenter for alle juridiske enheder.

1. Åbn arbejdsområdet **Administration af funktioner**.
2. Vælg funktionen **Styring af forretningsdokumenter** på listen under fanen **Ny**.
3. Vælg **Aktivér nu** for at aktivere den valgte funktion.
4. Opdater siden for at få adgang til den nye funktion.

![Arbejdsområdet Administration af funktioner](./media/BDM-Overview-FMEnabling.png)

Du kan finde flere oplysninger om aktivering af nye funktioner under [Oversigt over funktionsstyring](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Konfigurere parametre

Brug oplysningerne i følgende afsnit til at konfigurere de grundlæggende parametre for styring af forretningsdokumenter.

### <a name="prerequisites-for-parameter-setup"></a>Forudsætninger for parameteropsætning
Før du kan konfigurere styring af forretningsdokumenter, skal du konfigurere den ønskede dokumenttype i dokumentstyringsstrukturen. Denne dokumenttype bruges til at angive en midlertidig lagring af dokumenter i Office-formater (Excel og Word), der bruges som skabeloner for ER-rapporter. Skabelonen til midlertidig lagring kan redigeres ved hjælp af Office-skrivebordsprogrammer.

For denne dokumenttype skal følgende attributværdier vælges.

| **Attributnavn**  | **Attributværdi**   |
|---------------------|-----------------------|
| Klasse               | Vedlæg fil           |
| Multi               | Fil                  |
| Adresse            | SharePoint            |

Du kan finde oplysninger om, hvordan du konfigurerer de påkrævede dokumentstyringsparametre og dokumenttyper, i [Konfigurere dokumentstyring](../../fin-and-ops/organization-administration/configure-document-management.md).

![Konfigurere dokumenttype til dokumentstyring](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a>Konfigurere parametre

De grundlæggende parametre til styring af forretningsdokumenter kan konfigureres på siden **Parametre for forretningsdokument**. Det er kun specifikke brugere, der har adgang til siden. Det omfatter:

- Brugere, der er tildelt rollen **Systemadministrator**.
- Brugere, der er tildelt en hvilken som helst rolle, der er konfigureret til at udføre opgaven **Vedligeholde parametre for styring af forretningsdokumenter** (AOT-navn **ERBDMaintainParameters**).

Benyt følgende fremgangsmåde til at konfigurere grundlæggende parametre for alle juridiske enheder.

1. Log på Finance and Operations som bruger med adgang til siden **Parametre for forretningsdokument**.
2. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Styring af forretningsdokumenter** \> **Parametre for forretningsdokument**.
3.  På siden **Parametre for forretningsdokument** skal du under fanen **Vedhæftede filer** i feltet **SharePoint-dokumenttype** definere den dokumenttype, der skal bruges til midlertidig lagring af skabeloner i Office-formater, mens de redigeres ved hjælp af Office-skrivebordsprogrammer. 

> [!NOTE]
> Det er kun de dokumenttyper, der er konfigureret ved hjælp af et SharePoint-sted, der er tilgængelige for denne parameter.

![Konfigurere parametre til styring af forretningsdokumenter](./media/BDM-Overview-BDMSetting.png)

Den valgte dokumenttype er firmaspecifik og vil blive brugt, når brugeren arbejder med styring af forretningsdokumenter i det firma, som den valgte dokumenttype er konfigureret til. Når brugeren arbejder med styring af forretningsdokumenter i et andet firma, bruges den samme valgte dokumenttype, hvis der ikke er konfigureret nogen for dette firma. Når en dokumenttype er konfigureret, bruges den i stedet for den, der er valgt i feltet **SharePoint-dokumenttype**.

## <a name="configure-access-permissions"></a>Konfigurere adgangstilladelser

Når adgangsrettigheder til forretningsdokumentstyring ikke er aktiveret, kan alle brugere med adgang til arbejdsområdet for forretningsdokumentstyring som standard se alle de ER-løsningsskabeloner, der er tilgængelige i Finance and Operations. Arbejdsområdet til styring af forretningsdokumenter viser kun de skabeloner, der er placeret i ER-formatkonfigurationer, og som er markeret som **Forretningsdokumenttype**.

![Siden ER-konfigurationer](./media/BDM-Overview-ERFormatTags.png)

Listen over skabeloner, der er tilgængelige i arbejdsområdet for styring af forretningsdokumenter, kan begrænses ved at konfigurere adgangsrettigheder. Det kan være vigtigt, når der bruges forskellige skabeloner til at fremstille forretningsdokumenter for forskellige virksomhedsdomæner (funktionsområder), og du vil give bestemte brugere adgang til forskellige skabeloner til redigering i arbejdsområdet for styring af forretningsdokumenter.

Adgangstilladelser til forretningsdokumentstyring kan angives i **Konfigurator for adgangstilladelser**. Det er kun følgende brugere, der har adgang til siden:

- Brugere, der er tildelt rollen **Systemadministrator**.
- Brugere, der er tildelt en hvilken som helst anden rolle, der er konfigureret til at udføre opgaven **Konfigurere adgangstilladelser til redigering af skabeloner til forretningsdokumenter** (AOT-navn **ERBDTemplatesSecurity**).

Benyt følgende fremgangsmåde til at konfigurere adgangstilladelser til styring af forretningsdokumenter for alle juridiske enheder.

1. Log på Finance and Operations som bruger med adgang til siden **Konfigurator for adgangstilladelser**.
2. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Styring af forretningsdokumenter** \> **Administrer adgangsrettigheder**.

Vær opmærksom på beskeden om, at brugen af adgangsrettigheder til forretningsdokumentstyring ikke er aktiveret i øjeblikket.

![Konfiguratorside for adgangsrettigheder til forretningsdokumentstyring](./media/BDM-Overview-TemplatesAccess1.png)

Med denne indstilling kan alle brugere, der har fået tildelt en sikkerhedsrolle, der er konfigureret til at udføre opgaven **Administrer forretningsdokumentskabeloner** (AOT-navn **ERBDManageTemplates**), åbne forretningsdokumentstyringens arbejdsområde og kan redigere alle skabeloner, der er tilgængelige i Finance and Operations.

I følgende illustration vises, hvad der er tilgængeligt i arbejdsområdet til forretningsdokumentstyring for brugere, der er tildelt rollen **Debitorassistent**. Med de aktuelle indstillinger af adgangsrettigheder kan brugeren redigere forretningsdokumentskabeloner fra forskellige funktionsområder, herunder fakturering, lovpligtig rapportering og betalinger.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-TemplatesForAlice1.png)

3. Vælg **Indstillinger for adgangsrettigheder** på siden **Konfigurator for adgangstilladelser**.
4. I dialogboksen **Indstillinger for adgangsrettigheder til redigering af skabeloner** skal du aktivere indstillingen **Anvend konfigurerede adgangsrettigheder**.
5. Vælg **OK** for at bekræfte, at der er aktiveret adgangstilladelser til forretningsdokumentstyring.

![Konfigurationsside for adgangsrettigheder til forretningsdokumentstyring](./media/BDM-Overview-TemplatesAccess2.png)

6. Vælg **Tilføj** for at angive en ny forretningsrolle, der skal have konfigureret adgangsrettigheder til skabeloner for forretningsdokumentstyring.
7. I dialogboksen **Sikkerhedsroller** skal du vælge rollen **Debitorassistent** og derefter vælge **OK** for at bekræfte valget af rollen.
8. Vælg **Ny** under fanen **Adgangsrettigheder pr. konfigurationsmærkater**.
9. Vælg **Funktionsområde** i feltet **Mærkattype**, og vælg **Fakturering** i feltet **Id**.
10. Vælg **Gem** for at gemme de konfigurerede adgangsrettigheder for den valgte rolle.

  Den aktuelle indstilling betyder, at for en hvilken som helst bruger, der er tildelt rollen **Debitorassistent** og udfører pligten **Administrer forretningsdokumentskabeloner** (AOT-navn **ERBDManageTemplates**), vil ER-formatkonfigurationsskabeloner, der har værdien **Fakturering** for mærkatet **Funktionsområde**, kunne redigeres i arbejdsområdet for styring af forretningsdokumenter.

11. Skift til ruden **Relaterede oplysninger** fra højre side af den aktuelle side. I ruden **Relaterede oplysninger** kan du se, hvordan de konfigurerede adgangsrettigheder anvendes, herunder hvilke ER-konfigurationsskabeloner der er tilgængelige for brugere, der er tildelt rollen **Debitorassistent**.

![Konfigurationsside for adgangsrettigheder til forretningsdokumentstyring](./media/BDM-Overview-TemplatesAccess3.png)

12. Vælg **Tilføj** under fanen **Adgangsrettigheder pr. konfigurationer**.
13. I dialogboksen **Vælg konfiguration** skal du markere **Intrastat-rapporten** som ER-formatkonfiguration.
14. Vælg **OK** for at bekræfte indtastningen af de valgte konfigurationer, og vælg **Gem** for at gemme de konfigurerede adgangsrettigheder for den valgte rolle.

Den aktuelle indstilling betyder, at for en hvilken som helst bruger, der er tildelt rollen **Debitorassistent** og udfører pligten **Administrer forretningsdokumentskabeloner** (AOT-navn **ERBDManageTemplates**), vil følgende skabeloner kunne redigeres i arbejdsområdet for styring af forretningsdokumenter:

- Skabeloner med værdien **Fakturering** for mærkatet **Funktionsområde**.
- Skabeloner fra ER-formatkonfigurationer, der vises under fanen **Adgangsrettigheder pr. konfigurationer** (skabeloner fra formatkonfigurationen **Intrastat-rapport** for domænet **Lovpligtig rapportering** i dette eksempel).

![Konfigurationsside for adgangsrettigheder til forretningsdokumentstyring](./media/BDM-Overview-TemplatesAccess4.png)

I følgende illustration vises, hvad der er tilgængeligt i arbejdsområdet til forretningsdokumentstyring for en bruger, der er tildelt rollen **Debitorassistent**. Med den aktuelle indstilling af adgangsrettigheder til forretningsdokumentstyring kan brugeren redigere forretningsdokumentskabeloner fra **Fakturering**-domænet og **Intrastat-rapporten** som ER-formatkonfiguration. Skabeloner fra domænet **Betalinger** er ikke tilgængelige for rollen **Debitorassistent**.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> Reglerne **Adgangsrettigheder pr. konfigurationer** gemmes ved hjælp af det entydige identifikations-id for en ER-formatkonfiguration. Dette betyder, at disse regler ikke slettes, når en ER-konfiguration, der refererer til dem, slettes. Når du importerer slettede konfigurationer tilbage til denne forekomst af Finance and Operations, refererer disse regler til dem igen. Det er ikke nødvendigt at konfigurere reglerne igen, når de slettede konfigurationer importeres igen.

## <a name="use-business-document-management-to-edit-templates"></a>Bruge styring af forretningsdokumenter til at redigere skabeloner

Forretningsbrugere kan få adgang til forretningsdokumentskabeloner til redigering i arbejdsområdet til styring af forretningsdokumenter. Det er kun følgende brugere, som kan få adgang til arbejdsområdet for forretningsdokumentstyring:

- Brugere, der er tildelt rollen **Systemadministrator**.
- Brugere, der er tildelt en hvilken som helst rolle, der er konfigureret til at udføre pligten **Administrer forretningsdokumentskabeloner** (AOT-navn **ERBDManageTemplates**).

Benyt følgende fremgangsmåde for at redigere skabeloner til fritekstfakturaer i arbejdsområdet til styring af forretningsdokumenter. Før du udfører denne procedure, skal du have fuldført alle de foregående procedurer i dette emne.

1. Log på Finance and Operations som bruger med adgang til arbejdsområdet til styring af forretningsdokumenter.
2. Åbn arbejdsområdet til styring af forretningsdokumenter.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-EditingTemplate1.png)

Fanen **Skabelon** viser indholdet af den valgte skabelon. Vælg fanen **Detaljer** for at få vist oplysninger om den valgte skabelon samt detaljer om en ER-formatkonfiguration, som denne skabelon er placeret i. Bemærk, at alle skabelonerne har statussen **Udgivet**og ikke indeholder nogen detaljer i kolonnen **Revision**. Det betyder, at disse skabeloner ikke redigeres i øjeblikket.

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Starte redigering af skabeloner, der ejes af din konfigurationsudbyder

1. I arbejdsområdet til styring af forretningsdokumenter skal du vælge skabelonen **Checkudskrivningsformat** på listen.
2. Vælg fanen **Detaljer**.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-EditingTemplate2.png)

Indstillingen **Rediger skabelon** er tilgængelig for den valgte skabelon. Denne indstilling er altid tilgængelig for en skabelon i en ER-formatkonfiguration, der ejes af den aktive ER-konfigurationsudbyder **(Litware, Inc.** i dette eksempel). Når du vælger **Rediger skabelon**, vil den eksisterende skabelon fra kladdeversionen af den underliggende ER-formatkonfiguration være tilgængelig for redigering.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Starte redigering af skabeloner, der ejes af andre udbydere

1. I arbejdsområdet til styring af forretningsdokumenter skal du vælge skabelonen **FTI-debitorrapport (GER)** på listen.
2. Vælg fanen **Detaljer**.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-EditingTemplate3.png)

Indstillingen **Nyt dokument** er tilgængelig for den valgte skabelon. Denne indstilling er altid tilgængelig for en skabelon i en ER-formatkonfiguration, der er leveret af en anden udbyder (**Microsoft** i dette eksempel). Når **Nyt dokument** er valgt, kan en ny skabelon redigeres. Den redigerede skabelon gemmes derefter i en ny ER-formatkonfiguration, der genereres automatisk.

### <a name="start-editing-a-template"></a>Starte redigering af en skabelon

1. Vælg **Nyt dokument** i den valgte skabelon.
2. Rediger feltet **Titel** på den redigerbare skabelon, hvis det er nødvendigt. Teksten vil blive brugt til at navngive den ER-formatkonfiguration, der oprettes automatisk. Bemærk, at kladdeversionen af denne konfiguration (**FTI-debitorrapport (GER) Kopi**), der vil indeholde den redigerede skabelon, automatisk markeres til at køre dette ER-format for den aktuelle bruger. Samtidig bruges den ikke-redigerede oprindelige skabelon fra ER-basisformatkonfigurationen til at køre dette ER-format for enhver anden bruger.
3. I feltet **Navn** skal du ændre navnet på den første revision af den redigerbare skabelon, der oprettes automatisk.
4. I feltet **Kommentar** skal du ændre bemærkningen til den automatisk oprettede revision af den redigerbare skabelon.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-EditingTemplate4.png)

5. Vælg **OK** for at bekræfte starten af redigeringsprocessen.

Siden **BDM-skabeloneditor** i Finance and Operations åbnes. Den valgte skabelon er tilgængelig for online redigering ved hjælp af Office 365.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-office-365"></a>Redigere en skabelon i Office 365

Rediger skabelonen ved hjælp af funktionerne i Office 365. I Office Online kan du f.eks. ændre skrifttypen i feltprompterne i skabelonoverskriften fra **Normal** til **Fed**. Disse ændringer gemmes automatisk i den redigerbare skabelon, der er gemt i den primære skabelons lager (som standard er det Azure-blob-lageret), der er konfigureret til ER-strukturen.

![Side med skabeloneditor til styring af forretningsdokumenter](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a>Redigere en skabelon i Office-skrivebordsprogrammet

1. Vælg indstillingen **Åbn i skrivebordsapp** for at ændre skabelonen ved hjælp af funktionerne i Office-skrivebordsprogrammet (Excel i dette eksempel). Den redigerbare skabelon kopieres fra det permanente lager til det midlertidige lager, der er konfigureret i parametrene for forretningsdokumentstyring, som en SharePoint-mappe.
2. Bekræft, at du vil åbne skabelonen fra det midlertidige fillager i Office-skrivebordsprogrammet Excel.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-EditingLayout3.png)

3. Rediger skabelonen. Du kan du f.eks. ændre skrifttypen i feltprompterne i skabelonoverskriften ved at opdatere farven fra **Sort** til **Blå**.

![Side med skabeloneditor til styring af forretningsdokumenter](./media/BDM-Overview-EditingLayout4.png)

4. Vælg **Gem** i Excel-skrivebordsprogrammet for at gemme skabelonændringerne i det midlertidige lager.

![Side med skabeloneditor til styring af forretningsdokumenter](./media/BDM-Overview-EditingLayout5.png)

5. Luk Excel-skrivebordsprogrammet.
6. Vælg **Synkroniser gemt kopi** for at synkronisere det midlertidige skabelonlager med det permanente skabelonlager.

> [!NOTE]
> Kopien af den redigerbare skabelon i det midlertidige fillager opbevares kun for den aktuelle session med skabelonredigering. Når du afslutter denne session ved at lukke siden **BDM-skabeloneditor**, slettes denne kopi. Hvis du har justeret skabelonen i det midlertidige fillager, og du ikke vælger **Synkroniser gemt kopi**, når du forsøger at lukke siden med **BDM-skabeloneditoren**, bliver du spurgt, om du vil gemme de indsatte ændringer. Vælg **Ja**, hvis du vil gemme ændringerne af skabelonen på den permanente filplacering.

### <a name="validate-a-template"></a>Validere en skabelon

1. På siden **BDM-skabeloneditor** skal du vælge **Søg efter fejl** for at validere den ændrede skabelon i forhold til den underliggende ER-formatkonfiguration. Følg anbefalingerne, hvis det er relevant, for at justere skabelonen med formatstrukturen fra ER-basisformatkonfigurationen.
2. Vælg **Vis format** for at få vist formatets aktuelle struktur fra den ER-basisformatkonfigurationen, der skal justeres i forhold til den redigerbare skabelon. 
3. Vælg **Skjul format** for at lukke ruden.

![Siden med BDM-skabeloneditor](./media/BDM-Overview-EditingTemplate6.png)

4. Luk siden **BDM-skabeloneditor**.

Den opdaterede skabelon vises under fanen **Skabelon**. Bemærk, at status for den redigerede skabelon nu er **Kladde**, og at den aktuelle revision ikke længere er tom. Det betyder, at processen for redigering af denne skabelon er startet.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Teste den ændrede skabelon 

1. I Finance and Operations skal du skifte til firmaet **USMF**.
2. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
3. Vælg fakturaen **FTI-00000002**, og vælg derefter **Udskriftsstyring**.
4. Vælg **Modul - debitor** \> **Dokumenter** \> **Fritekstfaktura** \> **Originaldokument** som niveau for at angive omfanget af fakturaer til behandling.
5. I feltet **Rapportformat** skal du vælge **FTI-debitorrapport (GER) Kopi** som ER-formatet for det angivne dokumentniveau.

![Side med indstillinger for udskriftsstyring](./media/BDM-Overview-TestRun1.png)

6. Tryk på **Escape** for at lukke den aktuelle side.
7. Vælg **Udskriv**, og klik derefter på **Valgt**.
8. Download dokumentet, og åbn det i Excel-skrivebordsprogrammet.

![Siden med fritekstfakturaer](./media/BDM-Overview-TestRun2.png)

Den ændrede skabelon bruges til at generere rapporten med fritekstfaktura for den valgte vare. Hvis du vil analysere, hvordan denne rapport påvirkes af de ændringer, du har introduceret i skabelonen, kan du køre denne rapport i én programsession direkte, efter at du har ændret skabelonen i en anden programsession.

### <a name="create-an-alternative-template-revision"></a>Oprette en alternativ skabelonrevision

1. Åbn siden **BDM-skabeloneditor**, og vælg skabelonen **FTI-debitorrapport (GER) Kopi** .
2. Vælg **Ny** under fanen **Revisioner**.
3. Hvis det er nødvendigt, skal du ændre navnet på den anden revision i feltet **Navn** og basere den på den aktuelt aktive første revision.
4. I feltet **Kommentar** skal du efter behov ændre bemærkningen til den automatisk oprettede revision af den redigerbare skabelon.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-AddRevision.png)

Du har oprettet en ny revision af skabelonen, der er gemt i det permanente skabelonlager. Nu kan du fortsætte med at redigere skabelonen for den anden revision, der aktuelt er valgt som aktiv.

5. Vælg den første revision, og vælg derefter **Angiv som aktiv**. Du kan vælge en anden revision som aktiv, hvis du på et tidspunkt vil vende tilbage til denne revision af skabelonen.
6. Vælg den anden revision, og vælge derefter **Slet**.
7. Vælg **OK** for at bekræfte, at du vil slette den valgte revision. Du kan slette alle de ikke-aktive revisioner, når der ikke længere er brug for dem.

### <a name="delete-a-modified-template"></a>Slette en ændret skabelon

1. Vælg fanen **Skabelon** på siden **BDM-skabeloneditor**.
2. Vælg **Slet**.
3. Hvis du vælger **OK** for at bekræfte sletningen, slettes ER-formatet **FTI-debitorrapport (GER) Kopi** sammen med den ændrede skabelon. Vælg **Annuller** for at se andre indstillinger.

### <a name="revoke-changes-of-template"></a>Tilbagekalde ændringer af skabelon

Når du redigerer skabelonen fra et ER-format, der ejes af den aktuelle aktive udbyder, får du mulighed for at tilbagekalde ændringer, der er introduceret i skabelonen.

![Side med arbejdsområde til styring af forretningsdokumenter](./media/BDM-Overview-RevokeChanges.png)

1. Vælg fanen **Skabelon** på siden **BDM-skabeloneditor**.
2. Vælg **Fortryd**.
3. Hvis du vælger **OK** for at annullere de ændringer, der er introduceret for skabelonen, erstattes den ændrede skabelon med den oprindelige skabelon, og alle ændringer fjernes. Når du tilbagekalder ændringer til skabelonen, kan du slette skabelonen. Vælg **Annuller** for at se andre indstillinger.

### <a name="publish-a-modified-template"></a>Udgive en ændret skabelon
1. Vælg fanen **Udgiv** under fanen **Skabelon** på siden **BDM-skabeloneditor**.
2. Hvis du vælger **OK** for at bekræfte udgivelsen, markeres kladdeversionen af det afledte **FTI-debitorrapport (GER) Kopi**-ER-format, som indeholder den ændrede skabelon, som fuldført. Den ændrede skabelon bliver tilgængelig for andre brugere af Finance and Operations. De fuldførte versioner af dette ER-format bevarer kun den sidst aktive revision af skabelonen. Andre revisioner vil blive slettet. Vælg **Annuller** for at se andre indstillinger.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

#### <a name="i-selected-new-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-office-365-web-page"></a>Jeg har valgt **Nyt dokument**, men i stedet for at åbne siden **BDM-skabeloneditor** i Finance and Operations er jeg blevet sendt til Office 365-websiden.
Dette er et kendt problem med Office 365-omdirigeringen tilbage til Finance and Operations. Dette sker, når du logger på Office 365 første gang. Du kan løse dette problem ved at vælge knappen **Tilbage** i din browser for at gå tilbage til Finance and Operations.

#### <a name="i-understand-how-to-edit-a-template-by-using-office-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a>Jeg forstår, hvordan jeg kan redigere en skabelon ved at bruge Office 365 i den første programsession, og hvordan jeg kan bruge skabelonen i den anden programsession, der justerer skabelonen, for at se, hvordan mine ændringer påvirker det genererede forretningsdokument. Kan jeg gøre dette ved hjælp af Office-skrivebordsprogrammet?
Ja, det kan du. Vælg **Åbn i skrivebordsapp** i den første programsession. Skabelonen gemmes i det midlertidige fillager og åbnes i Office-skrivebordsprogrammet. Udfør derefter følgende trin for at se dine skabelonændringer i det genererede forretningsdokument:

1. Foretag ændringer i skabelonen ved hjælp af Office-skrivebordsprogrammet.
2. Vælg **Gem** i Office-skrivebordsprogrammet.
3. Vælg **Synkroniser gemt kopi** på siden **BDM-skabeloneditor** i den første programsession.
4. Udfør dette skabelon-ER-format i den anden programsession.

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a>Jeg får vist fejlen 'Værdi kan ikke være nul. Parameternavn: externalId', når jeg vælger **Åbn i skrivebordsapp**. Hvordan kan jeg undgå dette? 
Du har højst sandsynligt logget på den aktuelle forekomst af Finance and Operations i et Azure AD-domæne, der er forskelligt fra det Azure AD-domæne, der blev brugt til at implementere denne forekomst af Finance and Operations. Da SharePoint-tjenesten, der bruges til at gemme skabeloner for at gøre dem tilgængelige for redigering ved hjælp af Office-skrivebordsprogrammer, tilhører det samme domæne som Finance and Operations, har vi ingen adgangsrettigheder til SharePoint-tjenesten. Du kan løse dette problem ved at logge på den aktuelle forekomst af Finance and Operations ved hjælp af legitimationsoplysningerne for en bruger med det korrekte Azure AD-domæne.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Designe en konfiguration til generering af rapporter i OPENXML-format](tasks/er-design-reports-openxml-2016-11.md)

[Designe ER-konfigurationer til at generere rapporter i Word-format](tasks/er-design-configuration-word-2016-11.md)

[Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md)

[Konfigurere elektronisk rapportering for at trække data ind i Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)
