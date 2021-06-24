---
title: Designe en ny ER-løsning til udskrivning af en brugerdefineret rapport
description: Dette emne forklarer, hvordan du kan designe en elektronisk rapporteringsløsning (ER) til udskrivning af en brugerdefineret rapport.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f5a3ac7cae58d17409ea081ec30f61cecf29ce9
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224028"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Designe en ny ER-løsning til udskrivning af en brugerdefineret rapport

[!include[banner](../includes/banner.md)]

I følgende fremgangsmåde forklares det, hvordan en bruger i rollen Systemadministrator, Udvikler af elektronisk rapportering eller Funktionel konsulent til elektronisk rapportering kan konfigurere parametre for ER-strukturen, designe de krævede konfigurationer af en ny ER-løsning for at få adgang til dataene i et bestemt virksomhedsdomæne og generere en brugerdefineret rapport i Microsoft Office-format. Disse trin kan udføres i **USMF**-virksomheden.

- [Konfigurere ER-strukturen](#ConfigureFramework)

    - [Konfigurere ER-parametre](#ConfigureParameters)
    - [Aktivere en udbyder af ER-konfigurationer](#ActivateProvider)

        - [Gennemse listen over udbydere af ER-konfigurationer](#ReviewProvidersList)
        - [Tilføje en ny udbyder af ER-konfigurationer](#AddProvider)
        - [Aktivere en udbyder af ER-konfigurationer](#ActivateAddedProvider)

- [Designe en domænespecifik datamodel](#DesignModel)

    - [Importere en datamodelkonfiguration](#ImportDataModel)
    - [Opret en ny datamodelkonfiguration](#DesignDataModel)

        - [Navngive datamodellen](#NameDataModel)
        - [Tilføje datamodelfelter](#FieldsEntry)
        - [Fuldføre designet af datamodellen](#CompleteDataModel)

- [Designe en modeltilknytning til den konfigurerede datamodel](#DesignMapping)

    - [Importere en ny konfiguration af modeltilknytning](#ImportModelMapping)
    - [Oprette en ny konfiguration af modeltilknytning](#CreateModelMapping)

        - [Designe en ny komponent til modeltilknytning](#DesignMappingComponent)
        - [Tilføje datakilder for at få adgang til programtabeller](#AddMmDataSource1)
        - [Tilføje datakilder for at få adgang til programoptællinger](#AddMmDataSource2)
        - [Tilføje ER-etiketter for at generere en rapport på et angivet sprog](#AddMmLabels)
        - [Tilføje en datakilde for at transformere resultaterne af sammenligning af optællingsværdier med en tekstværdi](#AddMmDataSource3)
        - [Knytte datakilder til datamodelfelter](#AddMmBindings1)
        - [Fuldføre designet af modeltilknytningen](#CompleteModelMapping)

- [Designe en skabelon til en brugerdefineret rapport](#DesignReportTemplate)
- [Design et format](#DesignFormat)

    - [Importere en designet formatkonfiguration](#FormatImport)
    - [Opret en ny formatkonfiguration](#FormatCreate)

        - [Importere en rapportskabelon](#ImportReportTemplate)
        - [Konfigurere et format](#ConfigureFormat)
        - [Definere databinding for en rapporttitel](#DefineFormatBindings)
        - [Gennemse modeldatakilden](#ReviewModelDataSource)
        - [Binde formatelementer til datakildefelter](#BindFormatElements)

    - [Køre et designet format fra ER](#RunFormatFromER)

- [Finjustere et designet format](#TuneFormat)

    - [Ændre et format for at ændre navnet på et oprettet dokument](#ModifyToChangeName)
    - [Redigere et format for at ændre rækkefølgen af spørgsmål](#ModifyToOrder)
    - [Køre et ændret format fra ER](#RunFormatFromER2)
    - [Fuldføre formatdesignet](#CompleteFormat)

- [Udvikle programartefakter for at kalde den designede rapport](#DevelopCustomCode)

    - [Ændre kildekode](#ModifySourceCode)

        - [Tilføje en datakontraktklasse](#DataContractClass)
        - [Tilføje en klasse for brugergrænsefladegenerator](#UIBuilderClass)
        - [Tilføje en klasse for dataprovider](#DataProviderClass)
        - [Tilføje en etiketfil](#LabelsFile)
        - [Tilføje en rapportserviceklasse](#ServiceClass)
        - [Tilføje en klasse for rapport-controller](#ControllerClass)
        - [Tilføje et menupunkt](#MenuItem)
        - [Tilføje et menupunkt til en menu](#Menu)
        - [Bygge et Visual Studio-projekt](#BuildVSProject)

    - [Køre et format fra applikationen](#RunFormatFromApp)

- [Tilpasse en designet ER-løsning](#TuneSolution)

    - [Redigere en modeltilknytning](#ModifyModelMapping)

        - [Tilføje datakilder for at få adgang til et datakontraktobjekt](#AddDataSource1)
        - [Føje en datakilde for at få adgang til poster for ER-formattilknytning](#AddDataSource2)
        - [Føje en datakilde for at få adgang til en formattilknytningspost for et aktuelt ER-format](#AddDataSource3)
        - [Angive navnet på det aktuelle ER-format i datamodellen](#AddBinding)
        - [Fuldføre designet af modeltilknytningen](#CompleteModelMapping2)

    - [Redigere et format](#ModifyFormat)

        - [Tilføje et nyt formatelement](#AddFormatElement)
        - [Binde det tilføjede formatelement](#BindAddedFormatElement)
        - [Fuldføre formatdesignet](#CompleteFormat2)

    - [Køre et format fra applikationen](#RunFormatFromApp2)
    - [Køre et format fra ER](#RunFormatFromER3)
    - [Konfigurere en formatdestination til visning på skærmen](#ConfigureDestination)
    - [Køre et format fra applikationen for at vise det som et PDF-dokument](#RunFormatFromApp3)

- [Yderligere ressourcer](#References)

I dette eksempel skal du oprette en ny ER-løsning til modulet [Spørgeskema](../../../human-resources/hr-learning-questionnaires.md). Med denne nye ER-løsning kan du oprette en rapport ved at bruge et Microsoft Excel-regneark som skabelon. Du kan derefter generere rapporten for **Spørgeskema** i Excel- eller PDF-format, ud over at generere den eksisterende rapport for SQL Server Reporting Services (SSRS). Du kan også ændre den nye rapport senere og efter anmodning. Der kræves ingen kodning.

1. Hvis du vil køre den eksisterende rapport skal du gå til **Spørgeskema** \> **Design** \> **Rapport for spørgeskemaer**.

    ![Valg af menupunktet Rapport for spørgeskemaer i modulet Spørgeskema for at køre den eksisterende SSRS-rapport](./media/er-quick-start1-application-menu-origin.png)

2. Angiv valgkriterier i dialogboksen **Rapport for spørgeskemaer**. Anvend et filter, så rapporten kun indeholder spørgeskemaet **SBCCrsExam**.

    ![Angivelse af valgkriterier i dialogboksen Rapport for spørgeskemaer](./media/er-quick-start1-ssrs-report-dialog.png)

I følgende illustration vises den genererede version af SSRS-rapporten for spørgeskemaet **SBCCrsExam**.

![Genereret SSRS-rapport](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>Konfigurere ER-strukturen

Som bruger i rollen Udvikler af elektronisk rapportering skal du konfigurere det minimale sæt af ER-parametre, før du kan begynde at bruge ER-strukturen til at designe din nye ER-løsning.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>Konfigurere ER-parametre

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Parametre til elektronisk rapportering**.
3. På siden **Parametre til elektronisk rapportering** under fanen **Generelt** skal du vælge **Ja** i indstillingen **Aktiver designtilstand** .
4. På fanen **Vedhæftede filer** kan du angive følgende parametre:

    - Angiv feltet **Konfigurationer** til **Fil** for **USMF**-virksomheden.
    - Angiv felterne **Jobarkiv**, **Midlertidig**, **Grundlag** og **Andre** skal du vælge typen **Fil**.

Du kan finde flere oplysninger om ER-parametre under [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>Aktivere en udbyder af ER-konfigurationer

Alle ER-konfigurationer er markeret som ejet af en udbyder af ER-konfigurationer. Du skal derfor aktivere en udbyder af ER-konfigurationer i arbejdsområdet **Elektronisk rapportering**, før du begynder at tilføje eller redigere nogen ER-konfigurationer.

> [!NOTE]
> Det er kun ejeren af en ER-konfiguration, der kan redigere den. Før du kan redigere en ER-konfiguration, skal den relevante udbyder af ER-konfiguration aktiveres i arbejdsområdet **Elektronisk rapportering**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>Gennemse listen over udbydere af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Gå til arbejdsområdet **Elektronisk rapportering**, og vælg **Konfigurationsudbydere** i sektionen **Relaterede links**.
3. På siden **Konfigurationsudbydere** har hver udbyderpost et entydigt navn og en entydig URL-adresse. Gennemse indholdet af denne side. Hvis der allerede findes en post for **Litware, Inc.** (`https://www.litware.com`), skal du springe den næste procedure over, [Tilføje en ny udbyder af ER-konfigurationer](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Tilføje en ny udbyder af ER-konfigurationer

1. På siden **Konfigurationsudbydere** skal du vælge **Ny**.
2. I feltet **Navn** skal du angive **Litware, Inc.**
3. I feltet **Internetadresse** skal du angive `https://www.litware.com`.
4. Vælg **Gem**.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>Aktivere en udbyder af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. I arbejdsområdet **Elektronisk rapportering** skal du vælge konfigurationsudbyderen **Litware, Inc.**.
3. Vælg **Angiv aktive**.

Få flere oplysninger om udbydere af ER-konfigurationer under [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Designe en domænespecifik datamodel

Du skal oprette en ny ER-konfiguration, der indeholder en komponent til [datamodellen](general-electronic-reporting.md#data-model-and-model-mapping-components) til forretningsdomænet **Spørgeskema**. Denne datamodel vil senere blive brugt som en datakilde, når du designer et ER-format til at generere rapporten for **Spørgeskema**.

Når du udfører fremgangsmåden i afsnittet [Importere en ny datamodelkonfiguration](#ImportDataModel), kan du importere den ønskede datamodel fra den angivne XML-fil. Du kan også udføre fremgangsmåden i afsnittet [Oprette en ny datamodelkonfiguration](#DesignDataModel) for at designe denne datamodel fra bunden.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Importere en ny datamodelkonfiguration

1. Hent filen [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448), og gem den på din lokale computer.
2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.
4. Vælg **Exchange** \> **Indlæs fra XML-fil** i handlingsruden.
5. Vælg **Gennemse**, og find og vælg derefter filen **Questionnaires model.version.1.xml**.
6. Vælg **OK** for at importere konfigurationen.

Hvis du vil fortsætte, skal du springe over den næste procedure [Oprette en ny datamodelkonfiguration](#DesignDataModel).

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Opret en ny datamodelkonfiguration

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.
3. Vælg **Opret konfiguration**.
4. Åbn **Spørgeskemamodel** i feltet **Navn** i rulledialogboksen.
5. Vælg **Opret konfiguration** for at oprette konfigurationen.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Navngive datamodellen

1. På siden **Konfigurationer** skal du i konfigurationstræet vælge **Spørgeskemamodel**.
2. Vælg **Designer**.
3. Åbn <a name="DataModeName"></a>**Spørgeskemaer** i feltet **Navn** i oversigtspanelet **Generelt** på siden **Datamodeldesigner**.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Tilføje nye datamodelfelter

1. På siden **Datamodeldesigner** skal du vælge **Ny**.
2. Udfør følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:

    1. Vælg **Modelrod** som type for den nye node.
    2. I feltet **Navn** skal du skrive <a name="RootDefinitionName"></a>**Rod**.
    3. Vælg **Tilføj** for at tilføje en ny node.

    Denne rodbeskrivelse bruges til at levere data til rapporten for **Spørgeskema**. En enkelt datamodel kan have flere beskrivelser. Hver beskrivelse kan angives for et enkelt ER-format for at identificere de data, der skal bruges til at generere rapporten.

3. Vælg **Ny** igen, og udfør dernæst følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:

    1. Vælg **Underordnet til en aktiv node** som typen af den nye node.
    2. I feltet **Navn** skal du skrive **CompanyName**.
    3. Vælg **Streng** i feltet **Varetype**.
    4. Vælg **Tilføj** for at tilføje et nyt felt.

    Dette felt skal bruges til at overføre navnet på den aktuelle virksomhed til en ER-rapport, der bruger denne datamodel som datakilde.

4. Vælg **Ny** igen, og udfør dernæst følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:

    1. Vælg **Underordnet til en aktiv node** som typen af den nye node.
    2. I feltet **Navn** skal du skrive **Spørgeskema**.
    3. Vælg **Liste over poster** i feltet **Varetype**.
    4. Vælg **Tilføj** for at tilføje et nyt felt.

    Dette felt skal bruges til at overføre listen over spørgeskemaer til en ER-rapport, der bruger denne datamodel som datakilde.

5. Vælg noden **Spørgeskema**.
6. Fortsæt med at tilføje de krævede felter fra den redigerbare datamodel på samme måde, indtil du har fuldført følgende datamodelstruktur.

    | Feltsti                                                    | Datatype   | Feltbetegnelse/returneret værdi |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Rod                                                          |             | Referencepunktet til anmodning om spørgeskemadata. |
    | Rod\\Firmanavn                                             | Streng      | Navnet på den aktuelle virksomhed. |
    | Rod\\Udførelseskontekst                                        | Optag      | Detaljer om formatudførelse. |
    | Rod\\Udførelseskontekst\\Formatnavn                            | Streng      | Navnet på det ER-format, der køres. |
    | Rod\\Spørgeskema                                           | Liste over poster | Listen over spørgeskemaer |
    | Rod\\Spørgeskema\\Aktiv                                   | Streng      | Statussen for det aktuelle spørgeskema. |
    | Rod\\Spørgeskema\\Kode                                     | Streng      | Koden for det aktuelle spørgeskema. |
    | Rod\\Spørgeskema\\Beskrivelse                              | Streng      | Beskrivelsen for det aktuelle spørgeskema. |
    | Rod\\Spørgeskema\\Spørgeskematype                        | Streng      | Typen af det aktuelle spørgeskema. |
    | Rod\\Spørgeskema\\Spørgsmålsrækkefølge                            | Streng      | Den numeriske rækkefølge for det aktuelle spørgeskema. |
    | Rod\\Spørgeskema\\Resultatgruppe                             | Optag      | Resultatparametre for det aktuelle spørgeskema. |
    | Rod\\Spørgeskema\\Resultatgruppe\\Kode                       | Streng      | Identifikationskoden for den aktuelle resultatgruppe. |
    | Rod\\Spørgeskema\\Resultatgruppe\\Beskrivelse                | Streng      | Beskrivelsen for den aktuelle resultatgruppe. |
    | Rod\\Spørgeskema\\Resultatgruppe\\MaksAntalPoint          | Kommatal        | Det maksimale antal point, der kunne optjenes. |
    | Rod\\Spørgeskema\\Spørgsmål                                 | Liste over poster | Listen over spørgsmål til det aktuelle spørgeskema. |
    | Rod\\Spørgeskema\\Spørgsmål\\SamlingsSekvensnummer       | Heltal     | Sekvensnummeret for den aktuelle svarsamling. |
    | Rod\\Spørgeskema\\Spørgsmål\\Id                             | Streng      | Identifikationskoden for det aktuelle spørgsmål. |
    | Rod\\Spørgeskema\\Spørgsmål\\SkalFuldføres                | Streng      | Et flag, der angiver, om det aktuelle spørgsmål skal besvares. |
    | Rod\\Spørgeskema\\Spørgsmål\\PrimærtSpørgsmål                | Streng      | Et flag, der angiver, om det aktuelle spørgsmål er primært. |
    | Rod\\Spørgeskema\\Spørgsmål\\Sekvensnummer                 | Heltal     | Sekvensnummeret for det aktuelle spørgsmål. |
    | Rod\\Spørgeskema\\Spørgsmål\\Tekst                           | Streng      | Teksten i det aktuelle spørgsmål. |
    | Rod\\Spørgeskema\\Spørgsmål\\Svar                         | Liste over poster | Listen over svar for det aktuelle spørgsmål. |
    | Rod\\Spørgeskema\\Spørgsmål\\Svar\\KorrektSvar          | Streng      | Et flag, der angiver, om det aktuelle svar er korrekt. |
    | Rod\\Spørgeskema\\Spørgsmål\\Svar\\Point                 | Kommatal        | De point, der optjenes, når det aktuelle svar er valgt. |
    | Rod\\Spørgeskema\\Spørgsmål\\Svar\\Sekvensnummer         | Heltal     | Sekvensnummeret for det aktuelle svar. |
    | Rod\\Spørgeskema\\Spørgsmål\\Svar\\Tekst                   | Streng      | Teksten i det aktuelle svar. |

    I følgende illustration vises den fuldførte redigerbare datamodel på siden **Datamodeldesigner**.

    ![Konfigureret datamodel i ER-datamodeldesigneren](./media/er-quick-start1-model2.png)

7. Gem ændringerne.
8. Luk siden **Datamodeldesigner**.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Fuldføre designet af datamodellen

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet vælge **Spørgeskemamodel**.
3. I oversigtspanelet **Versioner** skal du vælge den konfigurationsversion, der har statussen **Kladde**.
4. Vælg **Skift status** \> **Fuldfør**.

Status for version 1 af denne konfiguration ændres fra **Kladde** til **Fuldført**. Version 1 kan ikke længere ændres. Denne version indeholder den konfigurerede datamodel og kan bruges som grundlag for andre ER-konfigurationer. Version 2 af denne konfiguration er oprettet og har statussen **Kladde**. Du kan redigere denne version for at justere datamodellen **Spørgeskema**.

![Versioner af den redigerbare konfiguration på siden Konfigurationer](./media/er-quick-start1-model-configuration.png)

Yderligere oplysninger om versionering for ER-konfigurationer finder du i [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md#component-versioning).

> [!NOTE]
> Den konfigurerede datamodel er din abstrakte repræsentation af forretningsdomæne **Spørgeskema** og indeholder ingen relationer til artefakter, der er specifikke for Microsoft Dynamics 365 Finance.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Designe en modeltilknytning for den konfigurerede datamodel

Som bruger i rollen Udvikler afelektronisk rapportering skal du oprette en ny ER-konfiguration, der indeholder en komponent for [modeltilknytning](general-electronic-reporting.md#data-model-and-model-mapping-components) til datamodellen **Spørgeskema**. Da denne komponent implementerer den konfigurerede datamodel for Finance, er den specifik for Finance. Du skal konfigurere komponenten for modeltilknytning for at angive de applikationsobjekter, der skal bruges til at udfylde den konfigurerede datamodel med applikationsdata under kørsel. For at fuldføre denne opgave skal du være opmærksom på implementeringsoplysningerne om datastrukturen i forretningsdomænet **Spørgeskema** i Finance.

Når du udfører fremgangsmåden i det efterfølgende afsnit [Importere en ny konfiguration af modeltilknytning](#ImportModelMapping), kan du importere den krævede konfiguration af modeltilknytning fra den angivne XML-fil. Du kan også udføre fremgangsmåden i afsnittet [Oprette en ny konfiguration af modeltilknytning](#CreateModelMapping) for at designe denne modeltilknytning fra bunden.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Importere en ny konfiguration af modeltilknytning

1. Hent filen [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448), og gem den på din lokale computer.
2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.
4. Vælg **Exchange** \> **Indlæs fra XML-fil** i handlingsruden.
5. Vælg **Gennemse**, og find og vælg derefter filen **Questionnaires mapping.version.1.1.xml**.
6. Vælg **OK** for at importere konfigurationen.

Hvis du vil fortsætte, skal du springe over den næste procedure [Oprette en ny konfiguration af modeltilknytning](#CreateModelMapping).

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Oprette en ny konfiguration af modeltilknytning

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet vælge **Spørgeskemamodel**.
3. Vælg **Opret konfiguration**.
4. Følg disse trin i rulledialogboksen:

    1. Vælg **Modeltilknytning baseret på datamodellen Spørgeskemaer** i feltet **Ny**.
    2. Skriv **Tilknytning af spørgeskema** i feltet **Navn**.
    3. Vælg definitionen **Rod** i feltet **Definition af datamodel**.
    4. Vælg **Opret konfiguration** for at oprette konfigurationen.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Designe en ny komponent til modeltilknytning

1. På siden **Konfigurationer** skal du i konfigurationstræet vælge **Tilknytning af spørgeskema**.
2. Vælg **Designer** for at åbne listen over tilknytninger.
3. Vælg tilknytningen **Tilknytning af spørgeskemaer**, der automatisk er tilføjet for definitionen **Rod**
4. Vælg **Designer** for at konfigurere den valgte tilknytning.

Der tilføjes automatisk en ny tilknytning for definitionen **Rod**. Denne tilknytning har retningen **Til model**. Denne tilknytning kan derfor bruges til at udfylde en datamodel med de nødvendige data.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Tilføje datakilder for at få adgang til programtabeller

Du skal konfigurere datakilder for at få adgang til de programtabeller, der indeholder spørgeskemaoplysninger.

1. Vælg **Dynamics 365 for Operations\\Tabelposter** på siden **Modeltilknytningsdesigner** i ruden **Datakildetyper**.
2. Tilføj en ny datakilde, der skal bruges til at få adgang til tabellen KMCollection, hvor hver post repræsenterer et enkelt spørgeskema:

    1. Vælg **Tilføj rod** i ruden **Datakilder**.
    2. Åbn **Spørgeskema** i feltet **Navn** i dialogboksen.
    3. Indtast **KMCollection** i feltet **Tabel**.
    4. Angiv indstillingen **Spørg efter forespørgsel** til **Ja**. Du kan derefter angive indstillinger for [filtrering](../../fin-ops/get-started/advanced-filtering-query-options.md) for tabellen i systemets dialogboks under kørsel.
    5. Vælg **OK** for at tilføje den nye datakilde.

3. Vælg **Dynamics 365 for Operations\\Tabelposter** i ruden **Datakildetyper**.
4. Tilføj en ny datakilde, der skal bruges til at få adgang til tabellen KMQuestion, hvor hver post repræsenterer et enkelt spørgsmål i et spørgeskema:

    1. Vælg **Tilføj rod** i ruden **Datakilder**.
    2. I dialogboksen skal du angive **Spørgsmål** i feltet **Navn**.
    3. Indtast **KMQuestion** i feltet **Tabel**.
    4. Vælg **OK** for at tilføje den nye datakilde.

5. Vælg **Dynamics 365 for Operations\\Tabelposter** i ruden **Datakildetyper**.
6. Tilføj en ny datakilde, der skal bruges til at få adgang til tabellen KMAnswer, hvor hver post repræsenterer et enkelt svar på et spørgsmål i et spørgeskema:

    1. Vælg **Tilføj rod** i ruden **Datakilder**.
    2. I feltet **Navn** skal du skrive **Svar**.
    3. Indtast **KMAnswer** i feltet **Tabel**.
    4. Vælg **OK** for at tilføje den nye datakilde.

7. Vælg **Funktioner\\Beregnet felt** i ruden **Datakildetyper**.
8. Tilføj et nyt beregnet felt, der skal bruges til at få adgang til en post i tabellen KMQuestionResultGroup fra alle poster i den overordnede KMCollection-tabel:

    1. Vælg **Spørgeskema** i ruden **Datakilder**.
    2. Vælg **Tilføj**.
    3. I dialogboksen skal du angive **\$Resultatgruppe** i feltet **Navn**.
    4. Vælg **Rediger formel**.
    5. I [ER-formeleditoren](general-electronic-reporting-formula-designer.md) i feltet **Formel** skal du skrive **FIRSTORNULL (\@.'\<Relations'.KMQuestionResultGroup)** for at bruge [stien](er-formula-language.md#paths) til en-til-mange-relationen mellem KMCollection- og KMQuestionResultGroup-tabellerne.
    6. Vælg **Gem**, og luk formeleditoren.
    7. Vælg **OK** for at tilføje det nye beregnede felt.

9. Vælg **Funktioner\\Beregnet felt** i ruden **Datakildetyper**.
10. Tilføj et nyt beregnet felt, der skal bruges til at få adgang til spørgsmålsposter i tabellen KMQuestion fra alle poster i den overordnede KMCollectionQuestion-tabel:

    1. Vælg **Spørgeskema** i ruden **Datakilder**.
    2. Udvid noden **\<Relationer**, der indeholder én til mange-relationer i tabellen KMCollection.
    3. Vælg den relaterede tabel **KMCollectionQuestion**, og vælg derefter **Tilføj**.
    4. I dialogboksen skal du angive **\$Spørgsmål** i feltet **Navn**.
    5. Vælg **Rediger formel**.
    6. I formeleditoren i feltet **Formel** skal du indtaste **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** for gå tilbage til den relevante spørgsmålspost fra tabellen KMQuestion.
    7. Vælg **Gem**, og luk formeleditoren.
    8. Vælg **OK** for at tilføje det nye beregnede felt.

11. Vælg **Funktioner\\Beregnet felt** i ruden **Datakildetyper**.
12. Tilføj et nyt beregnet felt, der skal bruges til at få adgang til svarposter i tabellen KMAnswer fra alle poster i den overordnede KMQuestion-tabel:

    1. I ruden **Datakilder** skal du vælge **Spørgeskema.\<Relationer.KMCollectionQuestion.\$Spørgsmål** og derefter vælge **Tilføj**.
    2. I dialogboksen skal du angive **\$Svar** i feltet **Navn**.
    3. Vælg **Rediger formel**.
    4. I formeleditoren i feltet **Formel** skal du angive **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** for gå tilbage til den relevante spørgsmålspost fra tabellen KMAnswer.
    5. Vælg **Gem**, og luk formeleditoren.
    6. Vælg **OK** for at tilføje det nye beregnede felt.

13. Vælg **Dynamics 365 for Operations\\Tabel** i ruden **Datakildetyper**.
14. Tilføj en ny datakilde, der skal bruges til at få adgang til metoder i tabellen CompanyInfo. Bemærk, at metoden **find()** i denne tabel returnerer en post, der repræsenterer et firma for den aktuelle Finance-forekomst, som denne tilknytning kaldes i forbindelse med.

    1. Vælg **Tilføj rod** i ruden **Datakilder**.
    2. I dialogboksen skal du angive **CompanyInfo** i feltet **Navn**.
    3. Indtast **CompanyInfo** i feltet **Tabel**.
    4. Vælg **OK** for at tilføje den nye datakilde.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Tilføje datakilder for at få adgang til programoptællinger

Du skal konfigurere datakilder for at få adgang til programoptællinger og sammenligne deres værdier med feltværdierne af typen **Optælling** i programtabellerne. Du skal bruge resultatet af sammenligningen til at udfylde de relevante felter i datamodellen.

1. Vælg **Dynamics 365 for Operations\\Optælling** på siden **Modeltilknytningsdesigner** i ruden **Datakildetyper**.
2. Tilføj en ny datakilde, der skal bruges til at få adgang til værdier i optællingen **EnumAppNoYes**.

    1. Vælg **Tilføj rod** i ruden **Datakilder**.
    2. I dialogboksen skal du angive **EnumAppNoYes** i feltet **Navn**.
    3. Angiv **NoYes** i feltet **Optælling**.
    4. Vælg **OK** for at tilføje den nye datakilde.

3. Vælg **Dynamics 365 for Operations\\Optælling** i ruden **Datakildetyper**.
4. Tilføj en ny datakilde, der skal bruges til at få adgang til værdierne i optællingen **KMCollectionQuestionMode**.

    1. Vælg **Tilføj rod** i ruden **Datakilder**.
    2. Gå til dialogboksen, og angiv **EnumAppQuestionOrder** i feltet **Navn**.
    3. Angiv **KMCollectionQuestionMode** i feltet **Optælling**.
    4. Vælg **OK** for at tilføje den nye datakilde.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>Tilføje ER-etiketter for at generere en rapport på et angivet sprog

Du kan tilføje ER-etiketter for at konfigurere nogle af dine datakilder til at returnere værdier, der afhænger af det sprog, der er defineret i sammenhæng med modeltilknytningens kald.

1. På siden **Modeltilknytningsdesigner** skal du i ruden **Datakilder** vælge **Svar** og derefter **Rediger**.
2. Aktivér feltet **Etiket**.
3. Vælg **Oversæt**.
4. Følg disse trin i dialogboksen **Tekstoversættelse**:

    1. Angiv **PositiveAnswer** i feltet **Etiket-id**.
    2. I feltet **Tekst på standardsprog** skal du indtaste **Ja**.
    3. Vælg **Oversæt**.
    4. Angiv **NegativtSvar** i feltet **Etiket-id**.
    5. I feltet **Tekst på standardsprog** skal du indtaste **Nej**.
    6. Vælg **Oversæt**.

5. Luk dialogboksen **Tekstoversættelse**.
6. Vælg **Annuller**.

![Tilføje ER-etiketter til den redigerbare modeltilknytning](./media/er-quick-start1-adding-labels.png)

Du har kun indtastet ER-etiketter for standardsproget. Oplysninger om, hvordan ER-etiketter kan oversættes til andre sprog, finder du i afsnittet [Designe flersprogede rapporter](er-design-multilingual-reports.md).

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Tilføje en datakilde for at transformere resultaterne af sammenligning af optællingsværdier med en tekstværdi

Da du skal transformere resultaterne af sammenligningen mellem optællingsværdier og tekstværdier flere gange for at finde differencekilder, er det en god ide at konfigurere denne logik som en enkelt datakilde. Hvis du vil bruge denne datakilde, skal du dog konfigurere den som parametrized-datakilde. Du kan finde flere oplysninger i [Understøtte parameteriserede opkald om ER-datakilder af typen Beregnet felt](er-calculated-field-type.md)

1. Vælg **Generelt\\Tom container** i ruden **Datakildetyper** på siden **Modeltilknytningsdesigner**.
2. Tilføj en ny containerdatakilde:

    1. Vælg **Tilføj rod** i ruden **Datakilder**.
    2. I dialogboksen skal du angive **Hjælpefunktion** i feltet **Navn**.
    3. Vælg **OK** for at tilføje den nye containerdatakilde.

3. Vælg **Funktioner\\Beregnet felt** i ruden **Datakildetyper**.
4. Tilføj en ny datakilde:

    1. Vælg **Hjælpefunktion** i ruden **Datakilder**.
    2. Vælg **Tilføj**.
    3. Gå til dialogboksen, og angiv **NoYesEnumToString** i feltet **Navn**.
    4. Vælg **Rediger formel**.
    5. Vælg **Parametre** i formeleditoren.
    6. Benyt følgende fremgangsmåde for at angive parametre for det konfigurerede udtryk:

        1. Vælg **Ny**.
        2. I dialogboksen skal du angive **Argument** i feltet **Navn**.
        3. Vælg datatypen **Boolesk** i feltet **Type**.
        4. Vælg **OK**.

    7. I feltet **Formel** skal du angive **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** for at returnere teksten for det relevante ER-navn, afhængigt af sproget i udførelseskonteksten og værdien af den angivne parameter.
    8. Vælg **Gem**, og luk formeleditoren.
    9. Vælg **OK** for at tilføje den nye datakilde.

![Konfigureret modeltilknytning i ER-modeltilknytningsdesigneren](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Binde datakilder til datamodelfelter

Du skal binde de konfigurerede datakilder til felterne i datamodellen for at angive, hvordan datamodellen skal udfyldes med programdata under kørsel.

1. Vælg **Firmanavn** på siden **Modeltilknytningsdesigner** i ruden **Datamodel**.
2. Udvid **Firmainfo** i ruden **Datakilder**, og benyt derefter følgende fremgangsmåde:

    1. Udvid noden **Firmainfo.find()**, der repræsenterer metoden **find()** i tabellen Firmainfo.
    2. Vælg **Firmainfo.find().Navn**.
    3. Vælg **Bind** for at angive navnet på den virksomhed, som den konfigurerede modeltilknytning kaldes i forbindelse med kørsel.

3. Vælg **Spørgeskema** i ruden **Datamodel**.
4. I ruden **Datakilder** skal du vælge **Spørgeskema** og derefter vælge **Bind** for at udfylde spørgeskemaposterne.
5. Udvid **Spørgeskema** i ruden **Datamodel**, og benyt derefter følgende fremgangsmåde:

    1. Vælg **Aktiv** i ruden **Datamodel**.
    2. Vælg **Rediger** i ruden **Datamodel**.
    3. Angiv i feltet **Formel** **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** for at udfylde det tekstafhængige og sprogafhængige resultat af sammenligningen mellem optællingsværdierne.

6. Fortsæt med at binde datakilder til datamodelfelter på samme måde, indtil du opnår følgende resultat.

    | Feltsti                                              | Datatype   | Handling | Bindingsudtryk |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | Firmanavn                                             | Streng      | Bind   | CompanyInfo.'find()'.Name |
    | Spørgeskema                                           | Liste over poster | Bind   | Spørgeskema |
    | Spørgeskema\\Aktiv                                   | Streng      | Edit   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Spørgeskema\\Kode                                     | Streng      | Bind   | \@.kmCollectionId |
    | Spørgeskema\\Beskrivelse                              | Streng      | Bind   | \@.Description |
    | Spørgeskema\\Spørgeskematype                        | Streng      | Bind   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Spørgeskema\\Spørgsmålsrækkefølge                            | Streng      | Edit   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Betinget",<br>EnumAppQuestionOrder.Random, "Tilfældig (procent i spørgeskema)",<br>EnumAppQuestionOrder.RandomGroup, "Tilfældig (procent i resultatgrupper)",<br>EnumAppQuestionOrder.Sequence, "Sekventiel",<br>"") |
    | Spørgeskema\\Resultatgruppe                             | Optag      |        | |
    | Spørgeskema\\Resultatgruppe\\Kode                       | Streng      | Bind   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Spørgeskema\\Resultatgruppe\\Beskrivelse                | Streng      | Bind   | \@.'\$ResultGroup'.description |
    | Spørgeskema\\Resultatgruppe\\MaksAntalPoint          | Kommatal        | Bind   | \@.'\$ResultGroup'.maxPoint |
    | Spørgeskema\\Spørgsmål                                 | Liste over poster | Bind   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Spørgeskema\\Spørgsmål\\SamlingsSekvensnummer       | Heltal     | Bind   | \@.answerCollectionSequenceNumber |
    | Spørgeskema\\Spørgsmål\\Id                             | Streng      | Bind   | \@.kmQuestionId |
    | Spørgeskema\\Spørgsmål\\SkalFuldføres                | Streng      | Edit   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Spørgeskema\\Spørgsmål\\PrimærtSpørgsmål                | Streng      | Bind   | \@.parentQuestionId |
    | Spørgeskema\\Spørgsmål\\Sekvensnummer                 | Heltal     | Bind   | \@.SequenceNumber |
    | Spørgeskema\\Spørgsmål\\Tekst                           | Streng      | Bind   | \@.'\$Question'.text |
    | Spørgeskema\\Spørgsmål\\Svar                         | Liste over poster | Bind   | \@.'\$Question'.'\$Answer' |
    | Spørgeskema\\Spørgsmål\\Svar\\KorrektSvar          | Streng      | Edit   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Spørgeskema\\Spørgsmål\\Svar\\Point                 | Kommatal        | Bind   | \@.point |
    | Spørgeskema\\Spørgsmål\\Svar\\Sekvensnummer         | Heltal     | Bind   | \@.sequenceNumber |
    | Spørgeskema\\Spørgsmål\\Svar\\Tekst                   | Streng      | Bind   | \@.text |

    I følgende illustration vises den endelige tilstand for den konfigurerede modeltilknytning på siden **Modeltilknytningsdesigner**.

    ![Fuldt konfigureret modeltilknytning i ER-modeltilknytningsdesigneren](./media/er-quick-start1-mapping2.png)

7. Gem ændringerne.
8. Luk siden **Modeltilknytningsdesigner**.

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Fuldføre designet af modeltilknytningen

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet vælge **Tilknytning af spørgeskema**.
3. I oversigtspanelet **Versioner** skal du vælge den konfigurationsversion, der har statussen **Kladde**.
4. Vælg **Skift status** \> **Fuldfør**.

Status for version 1.1 af denne konfiguration ændres fra **Kladde** til **Fuldført**. Version 1.1 kan ikke længere ændres. Denne version indeholder den konfigurerede modeltilknytning og kan bruges som grundlag for andre ER-konfigurationer. Version 1.2 af denne konfiguration er oprettet og har statussen **Kladde**. Du kan redigere denne version for at justere konfigurationen **Tilknytning af spørgeskema**.

![Versioner af den redigerbare ER-konfiguration på siden Konfigurationer](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> Den konfigurerede modeltilknytning er den Finance-specifikke implementering af den abstrakte datamodel, der repræsenterer forretningsdomænet **Spørgeskema**.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Designe en skabelon til en brugerdefineret rapport

ER-strukturen bruger foruddefinerede skabeloner til at oprette rapporter i Microsoft Office-formater (Excel-projektmapper eller Word-dokumenter). Mens den påkrævede rapport oprettes, udfyldes en skabelon med de krævede data i henhold til det konfigurerede dataflow. Derfor skal du først designe en skabelon til den brugerdefinerede rapport. Denne skabelon skal være designet som en Excel-projektmappe, og strukturen repræsenterer layoutet for en brugerdefineret rapport. Du skal navngive alle Excel-elementer, som du vil udfylde med de krævede data.

1. Hent filen [Questionnaires report template.xslxl](https://go.microsoft.com/fwlink/?linkid=851448), og gem den på din lokale computer.
2. Åbn filen i Excel, og gennemse projektmappens struktur.

Som følgende illustration viser, er den hentede skabelon designet til at udskrive bestemte spørgeskemaer, der viser et spørgeskemas spørgsmål sammen med relevante svar.

![Excel-skabelon til udskrivning af angivne spørgeskemaer](./media/er-quick-start1-template-layout.png)

Der er føjet Excel-navne til denne skabelon for udfylde spørgeskemaoplysninger. Du kan bruge Navnestyring til at gennemse Excel-navnene.

![Bruge Navnestyring til at gennemse Excel-navne i den viste Excel-skabelon](./media/er-quick-start1-template-names.png)

Rapportetiketter er tilføjet som fasttekst på engelsk. Du kan erstatte rapportetiketterne med nye Excel-navne, der udfylder etiketterne med sprogafhængig tekst, ved at bruge [etiketter](#AddMmLabels) for ER-format, som du gjorde for sprogafhængige udtryk i den konfigurerede modeltilknytning. I dette tilfælde skal der tilføjes-navne i det redigerbare ER-format.

I følgende illustration vises det brugerdefinerede rapporthoved, der gør det muligt at foretage sideinddeling i Excel.

![Brugerdefineret rapporthoved i den tilgængelige Excel-skabelon](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Design et format

Som bruger med rollen Funktionel konsulent i elektronisk rapportering skal du oprette en ny ER-konfiguration, der indeholder en komponent for [format](general-electronic-reporting.md#FormatComponentOutbound). Du skal konfigurere formatkomponenten format for at angive, hvordan en rapportskabelon skal udfyldes med de nødvendige data under kørsel.

Når du udfører fremgangsmåden i afsnittet [Importere en designet formatkonfiguration](#FormatImport), kan du importere det ønskede format fra den angivne XML-fil. Du kan også udføre fremgangsmåden i afsnittet [Oprette en ny formatkonfiguration](#FormatCreate) for at designe dette format fra bunden.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Importere en designet formatkonfiguration

1. Hent filen [Questionnairesformat.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448), og gem den på din lokale computer.
2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.
4. Vælg **Exchange** \> **Indlæs fra XML-fil** i handlingsruden.
5. Vælg **Gennemse**, og find og vælg derefter filen **Questionnaires format.version.1.1.xml**.
6. Vælg **OK** for at importere konfigurationen.

Hvis du vil fortsætte, skal du springe over den næste procedure [Oprette en ny formatkonfiguration](#FormatCreate).

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Opret en ny formatkonfiguration
 
1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet vælge **Spørgeskemamodel**.
3. Vælg **Opret konfiguration**.
4. Følg disse trin i rulledialogboksen:

    1. Vælg **Format baseret på datamodellen Spørgeskemaer** i feltet **Ny**.
    2. Skriv **Spørgeskemarapport** i feltet **Navn**.
    3. Vælg **1** i feltet **Datamodelversion**.

        > [!NOTE]
        > - Hvis du vælger en bestemt version af stamdatamodellen, vises strukturen i den tilsvarende version af datamodellen som strukturen i datakilden **Model** i det format, der oprettes.
        > - Du kan lade feltet stå tomt. Hvis det er tilfældet, vises strukturen i **Kladde**-versionen af datamodellen som strukturen i datakilden **Model** i det format, der oprettes. Du kan derefter justere modellen og straks se disse justeringer i dit format. Denne metode kan forbedre effektiviteten af ER-løsningsdesign, når du konfigurerer datamodellen, modeltilknytningen og formatet samtidigt.
        > - Hvis du vælger en bestemt version af stamdatamodellen, kan du skifte til at bruge **Kladde**-versionen senere, når du begynder at redigere et format.

    4. Vælg definitionen **Rod** i feltet **Definition af datamodel**.

5. Vælg **Opret konfiguration** for at oprette konfigurationen.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Importere en rapportskabelon

1. På siden **Konfigurationer** skal du i konfigurationstræet vælge **Spørgeskemarapport**.
2. Vælg **Designer** for at begynde at konfigurere et brugerdefineret format.
3. I oversigtspanelet på siden **Formatdesigner** skal du vælge **Importér** \> **Importér fra Excel** i handlingsruden.
4. Følg disse trin i dialogboksen:

    1. Vælg **Tilføj skabelon**.
    2. Find og vælg den lokalt gemte filen **Questionnaires report template.xslx**, og vælg derefter **Åbn**.
    3. Vælg **OK** for at importere skabelonen.

    ![Import af en rapportskabelon](./media/er-quick-start1-template-import.png)

Formatelementet **Excel\\Fil** føjes automatisk til det redigerbare format som et rodelement. Derudover tilføjes formatelementet **Excel\\Område** eller **Excel\\Celle** automatisk for hvert genkendeligt Excel-navn i den importerede skabelon. Formatet **Excel\\Overskrift**, der indeholder det indlejrede element **Streng**, tilføjes automatisk for at afspejle overskriftsindstillingerne for den importerede skabelon.

![Formatstruktur, der omfatter automatisk tilføjede elementer i ER-operationsdesigneren](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Konfigurere et format

1. Vælg rodelementet **Excel** i formattræet på siden **Formatdesigner**.
2. Angiv <a name="AddFormatRootElement"></a>**Rapport** i feltet **Navn** under fanen **Format** i højre side af siden.
3. I feltet **Foretrukket sprog** skal du vælge **Brugerindstilling** for at køre rapporten på brugerens foretrukne sprog.
4. I feltet **Foretrukket kultur** skal du vælge **Brugerindstilling** for at køre rapporten på brugerens foretrukne kultur.

    Du kan finde oplysninger om, hvordan du angiver sprog- og kulturkontekster for en ER-proces, under [Designe flersprogede rapporter](er-design-multilingual-reports.md).

    ![Konfigurere indstillinger for sprog og kultur for den designede rapport i ER-operationsdesigneren](./media/er-quick-start1-template-format-structure1.png)

5. Udvid rodnoden i formattræet, og vælg derefter **Resultatgruppe**.
6. Under fanen **Format** i feltet **Replikeringsretning** skal du vælge **Ingen replikering**, da du ikke forventer flere resultatgrupper for et enkelt spørgeskema.

    ![Definere replikeringsretningen for formatelementer af typen Område i ER-operationsdesigneren](./media/er-quick-start1-template-format-structure2.png)

7. Vælg **Gem**.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>Definere databinding for en rapporttitel

Du skal angive en databinding for et formatelement, der bruges til at udfylde titlen på en genereret rapport.

1. Vælg elementet **Rapport\\Rapporttitel** på siden **Formatdesigner** under fanen **Tilknytning** til højre.
2. Vælg **Rediger formel**.
3. Vælg **Oversæt** i formeleditoren.
4. Følg disse trin i dialogboksen **Tekstoversættelse**:

    1. Angiv **Rapporttitel** i feltet **Etiket-id**.
    2. I feltet **Tekst i standardsprog** skal du indtaste **Rapport for spørgeskemaer**.
    3. Vælg **Oversæt**, og vælg derefter **Gem**.
    4. Vælg **Oversæt** for at lukke dialogboksen **Tekstoversættelse**.

5. Luk formeleditoren.

    ![Konfiguration af bindingen for at udfylde titlen på en genereret rapport](./media/er-quick-start1-add-report-title-label.png)

Du kan bruge denne teknik til at gøre alle andre etiketter for den aktuelle skabelon sprogafhængige. Oplysninger om, hvordan de tilføjede etiketter til en enkelt ER-konfiguration kan oversættes til alle understøttede sprog, finder du i [Designe flersprogede rapporter](er-design-multilingual-reports.md).

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>Gennemse modeldatakilden

1. På siden **Formatdesigner** under fanen **Tilknytning** skal du vælge datakilden for <a name="ModelDSName"></a>**modellen**, der repræsenterer basisdatamodellen for dette ER-format.
2. Vælg **Rediger**.
3. Gennemse oplysningerne i dialogboksen **Egenskaber for datakilde**. Denne datakilde repræsenterer version 1 af datamodelkomponenten **Spørge skemaer**, der findes i ER-konfiguraitonen for **Spørgeskemamodel**.

![Egenskaber for modeldatakilden i ER-operationsdesigneren](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Binde formatelementer til datakildefelter

Hvis du vil angive, hvordan en skabelon skal udfyldes på kørselstidspunktet, skal du binde alle formatelementer, der er knyttet til et relevant Excel-navn, til et enkelt felt i dette formats datakilde.

1. Vælg formatelementet **Rapport\\Firmanavn** i formattræet på siden **Formatdesigner**.
2. Under fanen **Tilknytning** skal du vælge datakildefeltet **model.CompanyName** for typen **Streng**.
3. Vælg **Bind** for at angive et firmanavn i en skabelon.
4. Vælg elementet **Rapport\\Spørgeskema** i formattræet.
5. Under fanen **Tilknytning** skal du vælge datakildefeltet **model.Questionnaire** for typen **Postliste**.
6. Vælg **Bind**.
7. Vælg **Vis detaljer** for at få vist flere oplysninger om formatelementer.

    Formatelementet for området for **Spørgeskema** konfigureres som lodret replikeret. Når den er bundet til en datakilde af typen **Postliste**, gentages det relevante område for **Spørgeskema** for Excel-skabelonen for hver post i den bundne datakilde.
 
    ![Binding af formatelementet for spørgeskemaområdet til de relevante postlistedatakilder i ER-operationsdesigneren](./media/er-quick-start1-bindings1.png)

    Da området **Spørgeskema** for Excel-skabelonen er defineret fra række 5 til 14, gentages disse rækker for hvert rapporteret spørgeskema.

    ![Rækker i Excel-skabelonen, der vil blive gentaget i en genereret rapport for hver post på postlistens datakilder](./media/er-quick-start1-template-questionnaire-range.png)

8. Konfigurer lignende bindinger for de resterende formatelementer som beskrevet i følgende tabel.

    > [!NOTE]
    > I denne tabel antager oplysningerne i kolonnen "Sti til datakilde", at ER-funktionen for den [relative sti](relative-path-data-bindings-er-models-format.md) er aktiveret.

    | Formatere elementsti                                      | Datakildesti |
    |----------------------------------------------------------|------------------|
    | Excel\\Rapporttitel                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\Firmanavn                                       | **model.CompanyName** |
    | Excel\\Spørgeskema                                     | **model.Questionnaire** |
    | Excel\\Spørgeskema\\Aktiv                             | **\@.Active**, hvor **\@** er **model.Questionnaire** |
    | Excel\\Spørgeskema\\Kode                               | **\@.Code** |
    | Excel\\Spørgeskema\\Beskrivelse                        | **\@.Description** |
    | Excel\\Spørgeskema\\Spørgeskematype                  | **\@.QuestionnaireType** |
    | Excel\\Spørgeskema\\Spørgsmålsrækkefølge                      | **\@.QuestionOrder** |
    | Excel\\Spørgeskema\\Resultatgruppe\\Kode\_               | **\@.ResultsGroup.Code** |
    | Excel\\Spørgeskema\\Resultatgruppe\\Beskrivelse\_        | **\@.ResultsGroup.Description** |
    | Excel\\Spørgeskema\\Resultatgruppe\\MaksAntalPoint    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Spørgeskema\\Spørgsmål                           | **\@.Question** |
    | Excel\\Spørgeskema\\Spørgsmål\\SamlingsSekvensnummer | **\@.CollectionSequenceNumber**, hvor **\@** er **model.Questionnaire.Question** |
    | Excel\\Spørgeskema\\Spørgsmål\\Id                       | **\@.Id** |
    | Excel\\Spørgeskema\\Spørgsmål\\SkalFuldføres          | **\@.MustBeCompleted** |
    | Excel\\Spørgeskema\\Spørgsmål\\PrimærtSpørgsmål          | **\@.PrimaryQuestion** |
    | Excel\\Spørgeskema\\Spørgsmål\\Sekvensnummer           | **\@.SequenceNumber** |
    | Excel\\Spørgeskema\\Spørgsmål\\Tekst                     | **\@.Text** |
    | Excel\\Spørgeskema\\Spørgsmål\\Svar                   | **\@.Answer** |
    | Excel\\Spørgeskema\\Spørgsmål\\Svar\\KorrektSvar    | **\@.CorrectAnswer**, hvor **\@** er **model.Questionnaire.Answer** |
    | Excel\\Spørgeskema\\Spørgsmål\\Svar\\Point           | **\@.Points** |
    | Excel\\Spørgeskema\\Spørgsmål\\Svar\\Tekst             | **\@.Text** |

9. Vælg **Gem**, når du er færdig.

I følgende illustration vises den endelige tilstand for de konfigurerede databindinger på siden **Formatdesigner**.

![Konfigurerede databindinger i ER-operationsdesigneren](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> Hele samlingen af angivne datakilder og bindinger repræsenterer en komponent til formattilknytning i det konfigurerede format. Denne formattilknytning kaldes, når du kører det konfigurerede format for oprettelse af rapporter.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>Køre et designet format fra ER

Du kan nu køre et designet format til testformål fra siden **Konfigurationer**.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfiguration** i konfigurationstræet skal du udvide **Spørgeskemamodel** og derefter vælge **Spørgeskemarapport**.
3. Vælg **Designer** for den formatversion, der har statussen **Kladde**.
4. På siden **Formatdesigner** skal du vælge **Kør**.
5. Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **ER-parametre**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.
6. Vælg **OK** for at bekræfte filtreringsindstillingen.
7. Vælg **OK** for at køre rapporten.
8. Gennemse den oprettede rapport.

Som [standard](electronic-reporting-destinations.md#default-behavior) leveres en oprettet rapport som en Excel-fil, som du kan hente. I følgende illustrationer vises to sider med den oprettede rapport i Excel-format.

![Eksempel på en oprettet rapport i Excel-format, side 1](./media/er-quick-start1-report1a.png)

![Eksempel på en oprettet rapport i Excel-format, side 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Finjustere et designet format

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Ændre et format for at ændre navnet på et oprettet dokument

Et oprettet dokument navngives som standard ved hjælp af aliasset for den aktuelle bruger. Ved at ændre formatet kan du ændre denne funktionsmåde, så et oprettet dokument navngives på baggrund af din brugerdefinerede logik. Navnet på et oprettet dokument kan f.eks. være baseret på den aktuelle sessionsdato og -klokkeslæt og på rapportens titel.

1. Vælg rodelementet **Rapport** på siden **Formatdesigner**.
2. Vælg **Rediger filnavn** under fanen **Tilknytning**.
3. I feltet **Formel** skal du skrive **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.
4. Vælg **Gem**, og luk formeleditoren.
5. Vælg **Gem**.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Redigere et format for at ændre rækkefølgen af spørgsmål

Spørgsmålene er ikke placeret i korrekt rækkefølge i en oprettet rapport. Du kan ændre rækkefølgen ved at ændre formatet.

1. Vælg rodelementet **Rapport** på siden **Formatdesigner**.
2. Under fanen **Tilknytning** i formattræet skal du udvide **Rapport\\Spørgeskema\\Spørgsmål**.

    ![Spørgsmålsformatelement for intervaltypen i ER-operationsdesigneren](./media/er-quick-start1-bindings3.png)

3. Vælg **model.Questionnaire** under fanen **Tilknytning**.
4. Vælg **Tilføj** \> **Funktioner\\Beregnet felt** og angiv derefter **OrderedQuestions** i feltet **Navn**.
5. Vælg **Rediger formel**.
6. I formeleditoren i feltet **Formel** skal du skrive **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** for at arrangere listen over spørgsmål i det aktuelle spørgeskema efter sekvensrækkefølgenummeret.
7. Vælg **Gem**, og luk formeleditoren.
8. Vælg **OK** for at fuldføre indtastningen af et nyt beregnet felt.
9. Vælg **model.Questionnaire.OrderedQuestions** under fanen **Tilknytning**.
10. Vælg **Excel\\Spørgeskema\\Spørgsmål** i formattræet.
11. Vælg **Bind**, og bekræft derefter, at den aktuelle sti for **model.Questionnaire.Questions** erstattes af den nye sti for **model.Questionnaire.OrderedQuestions** i alle bindinger af indlejrede elementer.
12. Vælg **Gem**.

![Binding af formatelementet Spørgsmål til den konfigurerede datakilde for OrderedQuestions i ER-operationsdesigneren](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>Køre et ændret format fra ER

Du kan nu køre et ændret format til testformål fra ER-strukturen.

1. På siden **Formatdesigner** skal du vælge **Kør**.
2. Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **ER-parametre**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.
3. Vælg **OK** for at bekræfte filtreringsindstillingen.
4. Vælg **OK** for at køre rapporten.
5. Gennemse den oprettede rapport.

I følgende illustration vises en oprettet rapport i Excel-format, hvor spørgsmålene er placeret i korrekt rækkefølge.

![Oprettet rapport i Excel-format, der har placeret spørgsmålene i korrekt rækkefølge](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Fuldføre formatdesignet

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet skal du udvide **Spørgeskemamodel** og derefter vælge **Spørgeskemarapport**.
3. I oversigtspanelet **Versioner** skal du vælge den konfigurationsversion, der har statussen **Kladde**.
4. Vælg **Skift status** \> **Fuldfør**.

Status for version 1.1 af denne konfiguration ændres fra **Kladde** til **Fuldført**. Version 1.1 kan ikke længere ændres. Denne version indeholder det konfigurerede format og kan bruges til at udskrive den brugerdefinerede rapport. Version 1.2 af denne konfiguration er oprettet og har statussen **Kladde**. Du kan redigere denne version for at justere formatet for rapporten for **Spørgeskema**.

![Redigerbar ER-konfiguration på siden Konfigurationer](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> Det konfigurerede format er designet af rapporten for **Spørgeskema** og indeholder ingen relationer til de Finance-specifikke artefakter.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Udvikle programartefakter for at kalde den designede rapport

Som bruger i rollen Systemadministrator skal du udvikle ny logik, så det konfigurerede ER-format kan kaldes fra applikationens brugergrænseflade (UI) for at oprette den brugerdefinerede rapport. I øjeblikket giver ER ikke mulighed for at konfigurere denne type logik. Dette kræver derfor udviklingsarbejde. 

Hvis du vil udvikle den nye logik, skal du installere en topologi, der understøtter fortløbende build. Du kan finde flere oplysninger under [Installere topologier, der understøtter fortløbende build og automatisering af test](../perf-test/continuous-build-test-automation.md). Du skal også have adgang til udviklingsmiljøet for denne topologi. Du kan finde flere oplysninger om den tilgængelige API for ER under [API for ER-struktur](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Ændre kildekode

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Tilføje en datakontraktklasse

Føj den nye klasse **QuestionnairesErReportContract** til dit Microsoft Visual Studio-projekt, og skriv kode, der angiver den datakontrakt, der skal bruges til at køre det konfigurerede ER-format.

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>Tilføje en klasse for brugergrænsefladegenerator

Føj den nye klasse **QuestionnairesErReportUIBuilder** til dit Visual Studio-projekt, og skriv kode for at generere en dialogboks til kørsel, som skal bruges til at søge efter formattilknytnings-id'et for det ER-format, der skal køres. Den leverede kode søger kun efter ER-formater, der indeholder en datakilde af typen **Datamodel**, som refererer til datamodellen for **[Spørgeskemaer](#DataModeName)** ved hjælp af definitionen af **[Rod](#RootDefinitionName)**.

> [!NOTE]
> Du kan også bruge ER-integrationspunkter til at filtrere ER-formater. Du kan finde flere oplysninger under [API til at vise et opslag i formattilknytning](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Tilføje en klasse for dataprovider

Føj den nye klasse **QuestionnairesErReportDP** til dit Microsoft Visual Studio-projekt, og skriv kode, der indsætter den dataprovider, der skal bruges til at køre det konfigurerede ER-format. Den leverede kode omfatter kun datakontrakten for denne dataprovider.

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Tilføje en etiketfil

Føj den nye etiketfil **QuestionnairesErReportLabels\_en-US** til dit Visual Studio-projekt, og angiv følgende etiketter til nye ressourcer til brugergrænsefladen:

- Etiketten **\@QuestionnairesReport** for et nyt menupunkt, der indeholder følgende tekst på amerikansk engelsk (en-US): **Rapport for spørgeskemaer (drevet af ER)**
- Etiketten **\@QuestionnairesReportBatchJobDescription** for en titel på et batchjob, hvis et valgt ER-format er planlagt til udførelse som et batchjob

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Tilføje en rapportserviceklasse

Føj den nye klasse **QuestionnairesErReportService** til dit Visual Studio-projekt, og skriv kode, der kalder et ER-format, identificerer det ud fra formattilknytnings-id'et og angiver en datakontrakt som parameter.

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

Når du skal bruge et ER-format, der kører programdata, skal du konfigurere en datakilde af typen **Datamodel** i formattilknytningen. Denne datakilde refererer til en bestemt del af den angivne datamodel ved hjælp af en enkelt roddefinition. Når ER-formatet er kørt, kalder det denne datakilde for at få adgang til den tilsvarende ER-modeltilknytning, der er konfigureret for en bestemt model og roddefinition.

Alle de oplysninger, du kan forberede i kildekoden og -lageret som en del af datakontrakten, kan overføres til det aktuelle ER-format ved hjælp af en ER-modeltilknytning af denne type. I ER-modeltilknytningen skal du konfigurere en datakilde af typen **Objekt**, der refererer til klassen **[QuestionnairesErReportContract](#DataContractClass)**. Hvis du vil identificere en modeltilknytning, skal du angive en datakilde, der kalder denne modeltilknytning. I den leverede kode specificerede denne datakilde med konstanten **ERModelDataSourceName**, der har værdien for **[model](#ModelDSName)**. For at identificere, hvilken datakilde der skal bruges til at eksponere datakontrakten i modeltilknytningen, skal du angive et datakildenavn. I den leverede kode er dette navn angivet med konstanten **ParametersDataSourceName**, der har værdien <a name="DataContractDSName"></a>**RunTimeParameters**.

> [!NOTE]
> I et nyt miljø skal du muligvis opdatere ER-metadataene, så denne klassetype er tilgængelig i ER-modeltilknytningsdesigneren. Du kan finde flere oplysninger under [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Tilføje en klasse for rapport-controller

Føj den nye klasse **QuestionnairesErReportController** til dit Visual Studio-projekt, og skriv kode, der kører et ER-formatet enten i synkron tilstand eller batchtilstand, som du foretrækker, i den dialogboks, der er bygget på baggrund af logikken i den leverede klasse **QuestionnairesErReportUIBuilder**.

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Tilføje et menupunkt

Føj det nye menupunkt **QuestionnairesErReport** til Visual Studio-projektet. I egenskaben **Object** refererer dette menupunkt til klassen **QuestionnairesErReportController**, og det bruges til at angive en brugerrettighed til at vælge og køre et ER-format. I egenskaben **Etiket** refererer dette menupunkt til etiketten **\@QuestionnairesReport**, du har oprettet tidligere, så der vises en korrekt tekst på applikationens brugergrænseflade.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Tilføje et menupunkt til en menu

Tilføj den eksisterende menu **KM** i Visual Studio-projektet. Du skal føje et nyt element for **QuestionnairesErReport** af typen **Output** til denne menu. Dette element skal henvise til menupunktet **QuestionnairesErReport**, der er beskrevet i forrige afsnit.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Bygge et Visual Studio-projekt

Opbyg dit projekt for at gøre et nyt menupunkt tilgængeligt for brugerne.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Køre et format fra applikationen

1. Gå til **Spørgeskema** \> **Design** \> **Rapport for spørgeskemaer (leveret af ER)**.

    ![Valg af menupunktet Rapport for spørgeskemaer (leveret af ER) i modulet Spørgeskema for at køre det konfigurerede ER-format](./media/er-quick-start1-application-menu-modified.png)

2. Vælg **Rapport for spørgeskemaer** i feltet **Formattilknytning** i dialogboksen.
3. Vælg **OK**.
4. Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **Parametre for elektronisk rapportering**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.
5. Vælg **OK** for at bekræfte filtreringsindstillingen.
6. Vælg **OK** for at køre rapporten.

    ![Angivelse af valgkriterierne i dialogboksen Elektronisk rapportering](./media/er-quick-start1-report-run-dialog-page.png)

7. Gennemse den oprettede rapport.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Tilpasse en designet ER-løsning

Du kan redigere den konfigurerede ER-løsning, så den bruger den dataproviderklasse, du har udviklet til at få adgang til oplysninger om det aktive ER-format, og så den angiver navnet på dette ER-format i en oprettet rapport.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Redigere en modeltilknytning

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Tilføje datakilder for at få adgang til et datakontraktobjekt

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet skal du udvide **Spørgeskemamodel** og derefter vælge **Tilknytning af spørgeskema**.
3. Vælg **Designer** for at åbne siden **Tilknytning af model til datakilde**.
4. Vælg **Designer** for at åbne den valgte tilknytning i modeltilknytningsdesigneren.
5. Vælg **Dynamics 365 for Operations\\Objekt** på siden **Modeltilknytningsdesigner** i ruden **Datakildetyper**.
6. Vælg **Tilføj rod** i ruden **Datakilder**.
7. Angiv **[RunTimeParameters](#DataContractDSName)** i feltet **Navn** i dialogboksen som defineret i kildekoden for klassen **QuestionnairesErReportService**.
8. I feltet **Klasse** skal du angive **[QuestionnairesErReportContract](#DataContractClass)**, som er kodet tidligere.
9. Vælg **OK**.
10. Udvid **RunTimeParameters**.

Den tilføjede datakilde indeholder oplysninger om post-id'et for den aktuelle ER-formattilknytning.

![Tilføjet datakilde i ER-modeltilknytningsdesigneren](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>Føje en datakilde for at få adgang til poster for ER-formattilknytning

Fortsæt med at redigere den valgte modeltilknytning ved at tilføje en datakilde for at få adgang til poster for ER-formattilknytningen.

1. Vælg **Dynamics 365 for Operations\\Tabelposter** på siden **Modeltilknytningsdesigner** i ruden **Datakildetyper**.
2. Vælg **Tilføj rod** i ruden **Datakilder**.
3. I dialogboksen skal du angive **ER1** i feltet **Navn**.
4. Indtast **ERFormatMappingTable** i feltet **Tabel**.
5. Vælg **OK**.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Føje en datakilde for at få adgang til en formattilknytningspost for et aktuelt ER-format

Fortsæt med at redigere den valgte modeltilknytning ved at tilføje en datakilde for at få adgang til posten for formattilknytningen med det aktuelle ER-format.

1. Vælg **Funktioner\\Beregnet felt** i ruden **Datakildetyper** på siden **Modeltilknytningsdesigner**.
2. Vælg **Tilføj rod** i ruden **Datakilder**.
3. I dialogboksen skal du angive **ER2** i feltet **Navn**.
4. Vælg **Rediger formel**.
5. I formeleditoren i feltet **Formel** skal du angive **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.
6. Vælg **Gem**, og luk formeleditoren.
7. Vælg **OK**.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>Angive navnet på det aktuelle ER-format i datamodellen

Fortsæt med at redigere den valgte modeltilknytning, så navnet på det aktuelle ER-format angives i datamodellen.

1. På siden **Modeltilknytningsdesigner** skal du i ruden **Datamodel** skal du udvide **Udførelseskontekst** og derefter vælge **Udførelseskontekst\\Formatnavn**.
2. Vælg **Rediger** i ruden **Datamodel** for at konfigurere en databinding for den valgte datamodels felt.
3. I formeleditoren skal du angive **FIRSTORNULL (ER2.'\>Relations'.Format).Name** i feltet **Formel**.
4. Vælg **Gem**, og luk formeleditoren.

Da du har brugt feltet **Formatnavn**, viser den konfigurerede modeltilknytning nu navnet på et ER-format, der kalder denne modeltilknytning under udførelsen.

![Binding af datamodelfeltet til metoden for den tilføjede datakilde i ER-modeltilknytningsdesigneren](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Fuldføre designet af modeltilknytningen

1. Vælg **Gem** på siden **Modeltilknytningsdesigner**.
2. Luk siden.
3. Luk siden for modeltilknytninger.
4. På siden **Konfigurationer** i konfigurationstræet skal du sikre, at konfigurationen **Tilknytning af spørgeskema** stadig er valgt. Vælg derefter den konfigurationsversion, der har statussen **Kladde** på oversigtspanelet **Versioner**.
5. Vælg **Skift status** \> **Fuldfør**.

Status for version 1.2 af denne konfiguration ændres fra **Kladde** til **Fuldført**. Version 1.2 kan ikke længere ændres. Denne version indeholder den konfigurerede modeltilknytning og kan bruges som grundlag for andre ER-konfigurationer. Version 1.3 af denne konfiguration er oprettet og har statussen **Kladde**. Du kan redigere denne version for at justere datatilknytningen **Spørgeskema**.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Redigere et format

Du kan redigere det konfigurerede ER-format, så navnet vises i sidefoden i en rapport, der oprettes, når ER-formatet køres.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Tilføje et nyt formatelement.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet skal du udvide **Spørgeskemamodel** og derefter vælge **Spørgeskemarapport**.
3. Vælg **Designer**.
4. Vælg rodelementet **Rapport** på siden **Formatdesigner**.
5. Vælg **Tilføj** for at tilføje et nyt indlejret formatelement for det valgte rodelement for **Rapport**.
6. Vælg **Excel\\Sidefod**.
7. I feltet **Navn** skal du skrive **Sidefod**.
8. Vælg **Rapport\Sidefod**, og vælg derefter **Tilføj**.
9. Vælg **Tekst\\Streng**.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Binde det tilføjede formatelement

1. Vælg **Rediger formel** for det aktive element for **Sidefod\\Streng** på siden **Formatdesigner** under fanen **Tilknytning**.
2. Angiv **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))** i feltet **Formel** i formeleditoren.
3. Vælg **Gem**, og luk formeleditoren.
4. Vælg **Gem**.

Det konfigurerede format er nu ændret, så navnet indsættes i sidefoden i en genereret rapport ved hjælp af elementet for **Sidefod\\Streng**.

![Tilføjelse af formatelementet Sidefod til det konfigurerede format i ER-operationsdesigneren](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Fuldføre formatdesignet

1. Luk siden **Formatdesigner**.
2. På siden **Konfigurationer** i konfigurationstræet skal du sikre, at konfigurationen **Spørgeskemarapport** stadig er valgt. Vælg derefter den konfigurationsversion, der har statussen **Kladde** på oversigtspanelet **Versioner**.
3. Vælg **Skift status** \> **Fuldfør**.

Status for version 1.2 af denne konfiguration ændres fra **Kladde** til **Fuldført**. Version 1.2 kan ikke længere ændres. Denne version indeholder det konfigurerede format og kan bruges som grundlag for andre ER-konfigurationer. Version 1.3 af denne konfiguration er oprettet og har statussen **Kladde**. Du kan redigere denne version for at justere rapporten **Spørgeskema**.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Køre et format fra applikationen

1. Gå til **Spørgeskema** \> **Design** \> **Rapport for spørgeskemaer (leveret af ER)**.
2. Vælg **Rapport for spørgeskemaer** i feltet **Formattilknytning** i dialogboksen.
3. Vælg **OK**.
4. Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **ER-parametre**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.
5. Vælg **OK** for at bekræfte filtreringsindstillingen.
6. Vælg **OK** for at køre rapporten.
7. Gennemse den oprettede rapport i Excel-format.

Bemærk, at sidefoden i den oprettede rapport indeholder navnet på det ER-format, der blev brugt til at oprette den.

![Genereret rapport i Excel-format](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>Køre et format fra ER

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet skal du udvide **Spørgeskemamodel** og derefter vælge **Spørgeskemarapport**.
3. Vælg **Kør** i handlingsruden.
4. Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **Parametre for elektronisk rapportering**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.
5. Vælg **OK** for at bekræfte filtreringsindstillingen.
6. Vælg **OK** for at køre rapporten.
7. Gennemse den oprettede rapport i Excel-format.

Bemærk, at sidefoden i den oprettede rapport ikke indeholder navnet på det ER-format, der blev brugt til at generere den, da datakontraktobjektet ikke blev overført til den aktuelle modeltilknytning, da det blev kaldt af det ER-format, der blev kørt fra ER.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Konfigurere en formatdestination til visning på skærmen

1. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Destination for elektronisk rapportering**.
2. På siden **Destination for elektronisk rapportering** skal du tilføje en destinationspost for det konfigurerede ER-format for **Spørgeskemarapport**.
3. Konfigurer [destinationen](er-destination-type-screen.md) for **Skærm** for den formatkomponent for **Rapport**, der er [tilføjet](#AddFormatRootElement) som rodelementet for det konfigurerede ER-format for **Spørgeskemarapport**, i oversigtspanelet **Fildestination**.
4. I oversigtspanelet **PDF-konverteringsindstillinger** kan du konfigurere destinationen til at konvertere en rapport til [PDF-format](electronic-reporting-destinations.md#OutputConversionToPDF), som bruger **Liggende** sideretning.

![Konfiguration af den brugerdefinerede skærmdestination til ER-formatet på siden Destination for elektronisk rapportering](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>Køre et format fra applikationen for at vise det som et PDF-dokument

1. Gå til **Spørgeskema** \> **Design** \> **Rapport for spørgeskemaer (leveret af ER)**.
2. Vælg **Rapport for spørgeskemaer** i feltet **Formattilknytning** i dialogboksen.
3. Vælg **OK**.
4. Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **Parametre for elektronisk rapportering**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.
5. Vælg **OK** for at bekræfte filtreringsindstillingen.

    Bemærk, at feltet **Output** i oversigtspanelet **Destinationer** er indstillet til **Skærm**. Hvis du vil ændre den konfigurerede destination, skal du vælge **Skift**.

    ![Dialogboks for ER-rapportens kørsel, hvor du kan ændre den konfigurerede destination](./media/er-quick-start1-run-settings.png)

6. Vælg **OK** for at køre rapporten.
7. Gennemse den oprettede rapport i PDF-format.

    ![Eksempel på skærmen af den oprettede rapport i PDF-format.](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Formelsprog i elektronisk rapportering](er-formula-language.md)
- [Designe flersprogede rapporter](er-design-multilingual-reports.md)
- [API til ER-struktur](er-apis-app73.md)
- [Funktionen CASE](er-functions-logical-case.md)
- [Funktionen CONCATENATE](er-functions-text-concatenate.md)
- [Funktionen DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [Funktionen FILTER](er-functions-list-filter.md)
- [Funktionen FIRSTORNULL](er-functions-list-firstornull.md)
- [Funktionen FORMAT](er-functions-text-format.md)
- [Funktionen IF](er-functions-logical-if.md)
- [Funktionen ORDERBY](er-functions-list-orderby.md)
- [Funktionen SESSIONNOW](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
