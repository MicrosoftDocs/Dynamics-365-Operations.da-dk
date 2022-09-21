---
title: Konfigurere en alternativ dataflow for anbefalinger
description: Denne artikel beskriver, hvordan du konfigurerer et miljø ved at bruge en alternativ dataflow til at levere data til anbefalingstjenesten.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460158"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Konfigurere en alternativ dataflow for anbefalinger

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer et miljø ved at bruge en alternativ dataflow til at levere data til anbefalingstjenesten.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Sammenligning af standard-dataflow med alternativ dataflow

I følgende illustration vises dataflowet uden for feltet i et miljø.

![Standard-dataflow i et miljø](media/reco-out-of-the-box-dataflow-2.png)

I følgende illustration vises et alternativt dataflow, hvor synkroniseringsbatchjobbet for enhedslageret erstattes med alternative dataflowtrin.

![Alternativ dataflow i et miljø](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Forudsætninger

- I denne artikel antages det, at du allerede har aktiveret tjenesten med anbefalinger for miljøet. Du kan finde flere oplysninger under [Aktivere produktanbefalinger](enable-product-recommendations.md).
- Når du arbejder med filer og mapper i Microsoft Azure Data Lake Storage-konto:

    - Du kan enten bruge Azure-webportalgrænsefladen eller programmet Azure Storage Explorer.
    - Startpunkterne for arbejdet med filer og mapper er i containeren **dynamics365-financeandoperations**, der er placeret under den mappe, der er navngivet, så de svarer til din URL-adresse til miljøet.
    - Hvis navnet på dit sandkassemiljø er **MyUAT**, vil URL-adressen for miljøet være `myuat.sandbox.operations.dynamics.com`.
    - Hvis der er oprettet forbindelse til mere end ét miljø til samme lagerkonto, har hvert miljø sin egen rodmappe.

## <a name="prerequisites"></a>Forudsætninger

Før du kan fuldføre trinnene i denne artikel, skal du kontrollere, at følgende forudsætninger er opfyldt:

### <a name="set-up-microsoft-power-platform"></a>Opret Microsoft Power Platform

Følg instruktionerne i [Aktivere Microsoft Power Platform-integration](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md) for at konfigurere Microsoft Power Platform.

### <a name="install-the-export-to-data-lake-add-in"></a>Installere tilføjelsesprogrammet Eksport til Azure Data Lake

Hvis du vil installere tilføjelsesprogrammet Eksporter til Data Installer, skal du følge instruktionerne i [Installere tilføjelsesprogrammet Eksport til Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> Noter konfigurationsværdierne, da du skal bruge dem til nogle af de trin, der følger.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Konfigurere tabeller, der skal eksporteres, i Dynamics 365

Tabelsynkronisering fra Dynamics 365 til Azure Data Lake Storage administreres på side n **Eksporter til Data Lake**. Da den side ikke har et menupunkt i øjeblikket, er det kun brugere i sikkerhedsrollen **Systemadministrator**, der kan åbne det.

Hvis du vil konfigurere tabeller, der skal eksporteres i Dynamics 365, skal du følge disse trin.

1. Hvis du vil åbne siden **Eksporter til Data Lake**, skal du føje strengen `?mi=DataFeedsDefinitionWorkspace` til miljøets grundlæggende URL-adresse som vist i følgende eksempel:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. På siden **Eksporter til Data Lake** og kopier de tabeller, der er vist i afsnittet [Liste over RetailSales-kubetabeller](#list-of-retailsales-cube-tables) i denne artikel.
1. Udvid listen over filterindstillinger i kolonnen **Systemnavn**.
1. For filtertypen er vælg **en af**. Sæt derefter markøren i tekstboksen, og indsæt listen over de tabeller, du har kopieret fra **Eksport til Data Lake**.
1. Vælg **Anvend** nederst på listen med filterindstillinger.
1. Markér alle rækker i gitteret, og vælg derefter **Aktivér**.

> [!NOTE]
> Før du går videre til næste trin, skal alle rækker opdateres til statussen **I gang**. Fejlfinde og løs eventuelle fejl efter behov.

### <a name="create-a-synapse-workspace"></a>Opret et Synapse-arbejdsområde

Hvis du vil oprette et synapse-arbejdsområde, hvis du ikke allerede har ét, skal du følge instruktionerne i [Quickstart: Oprette et arbejdsområde til Synapse](/azure/synapse-analytics/quickstart-create-workspace).

Hvis du vil holde styr på dine Azure-ressourcer, anbefales det, at du holder styr på Data Azure-lagringskontoen og arbejdsområdet i Synapse i en ressourcegruppe i Azure. Du kan genbruge den lagerkonto, du oprettede, da du installerede Eksport til Data Lake-tilføjelsesprogrammet.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Oprette en database i Synapse til anbefaling af databehandling

Du kan bruge programmet Common Data Model Utility konsol (CDMUtil_ConsoleApp) til at oprette en database i arbejdsområdet i Synapse og udfylde den fra tabellerne i Common Data Model i Data Lake Storage. Vi anbefaler, at du bruger værktøjet Common Data Model sammen med databasen i et udviklingsmiljø, hvis der er nogen udvidelser.

> [!NOTE]
> Det antages i følgende fremgangsmåde, at der ikke føjes udvidelsesdata til RetailSales-kuben.

Opret en database i Synapse ved at udføre følgende trin.

1. Gå til [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app), og følg trinnene til hentning af **CDMUtilConsoleApp.zip**-filen.
1. Udtrække postfilen til en lokal mappe.
1. Åbn **CDMUtil_ConsoleApp.dll.config** i en teksteditor, og opdater følgende værdier:

    1. Indstil **Lejer-id**-værdi (Azure-lejer-id).
    1. Angiv værdien for **Adgangsnøglen** (adgangsnøglen til kontoen Data Lake-lagringskonto).

        1. Opret en Lagerkonto i Azure-portalen.
        1. Vælg **Adgangsnøgler** i menuen til venstre på siden.
        1. Vælg **Vis nøgler** øverst på siden.
        1. Vælg kopieringsknappen til et af de to nøglefelter, og indsæt derefter værdien mellem de dobbelte anførselstegn i konfigurationsfilen.

    1. Angiv værdien **ManifestURL** for URL-adressen for **Tables.manifest.cdm.json**-filen i Azure Data Lake Storage. Find URL-adressen ved at gå til filen på Azure-portalen, vælge ellipsen (**...**) i højre side af visningen og derefter vælge **Egenskaber**. URL-adressen er den første egenskab, der vises under fanen **Oversigt**.
    1. Angiv værdien **TargetDbConnectionString** til forbindelsesstrengen til den indbyggede SQL-pulje til serverløse i arbejdsområdet i Synapse.

        1. Vælg fanen **Administrer** i arbejdsområdet i Synapse.
        1. Vælg **SQL-puljer** på undermenuen.
        1. Vælg navnet **Indbygget** for at få vist egenskaberne for puljen.
        1. Vælg den type forbindelse, ADO.NET vil bruge, i egenskabsdialogboksen. Kopiér derefter værdien for forbindelsesstrengen, og indsæt den mellem de dobbelte anførselstegn i konfigurationsfilen.

        > [!NOTE]
        > Du skal have rettighed til at oprette databaser. For at gøre det nemmere at bruge den indbyggede **sqladminuser**-administratorkonto.

    1. Opstil noden **ProcessEntities** og angiv værdien til **Sand** (f.eks. `<add key="ProcessEntities" value ="true"/>`).

1. Gem og luk **CDMUtil_ConsoleApp.dll.config**-filen.
1. Kopier filen **EntityList.json** til mappen **/Manifest**.
1. Kør **cdmutil_consoleapp.exe** i et kommandopromptvindue.

> [!NOTE]
> Når du gennemser outputtet, skal der være 35 enheder/visninger, mindst 75 tabeller og ingen fejl.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Forberede mappen Data Arbejde med RetailSales-aggregeringsmålinger

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Sikkerhedskopiere dine aktuelle RetailSales-kubedata fra Data Lake Storage

Det er lettest at sikkerhedskopiere dine aktuelle RetailSales-kubedata ved at omdøbe mappen **RetailSales** i Data Lake-lagring **RetailSales-sikkerhedskopi** eller noget lignende. Med denne metode bevares de eksisterende data, hvis der senere skal foretages fejlfinding.

Mappen **/RetailSales-kuben** kan findes på følgende placering:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Oprette en ny RetailSales-mappe og overføre modelfilen

Benyt følgende fremgangsmåde for at oprette en ny **RetailSales-mappe** og overføre **model.json-filen** til Data Lake-lagring.

1. Opret en ny tom mappe på samme niveau som det forrige bibliotek, og navngive den **RetailSales**.
1. Overfør **model.json-filen** til det nye bibliotek.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Oprette en pipeline til kopiering af RetailSales-kubedataene

Pipelinen læser RetailSales-kubevisninger og eksporterer dataene til .csv-filer i Data Lake-lagring.

Oprette en pipeline til kopiering af RetailSales-kubedataene ved at gøre følgende.

1. Vælg fanen **Integrer** i arbejdsområdet i Synapse.
1. Vælg plustegnet (**+**), og vælg derefter **Import fra pipeline-skabelon**.
1. Hent og vælg derefter filen [ExportRetailSalesCubeViews.zip](https://aka.ms/reco-alternate-dataflow-files).
1. Vælg den tilknyttede SQL-databasetjeneste.
1. Vælg den tilknyttede lagringskontotjeneste.
1. Åbn værktøjet **Kopier data**, og rediger **mappesti**-egenskaben til **\<environment_name\>/...**.

### <a name="test-execution-of-the-pipeline"></a>Test udførelse af pipeline

Det anbefales, at du tester pipelinen ved kun at bruge én visning. Visningen **RetailSales_RetailMediaTemplateView** virker godt, da den normalt indeholder mindre end 10 rækker.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>Planlægge, at pipelinen skal køre på en gentagelsesplan

Hver gang pipelinen køres, finder Azure-forbruget sted. Det anbefales, at du planlægger udførelser med intervaller på 48 timer eller mere. Du kan altid køre pipelinen manuelt, hvis du skal synkronisere data med det samme. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Tabeloversigt til synkronisering fra Dynamics 365 til Data Lake Storage

Følgende liste over tabeller er et undersæt af alle de tabeller, der er påkrævet for hele RetailSales-kuben. Kun 15 af visningerne i RetailSales-kuben bruges af anbefalingstjenesten, og listen over påkrævede tabeller er filtreret tilsvarende.

### <a name="list-of-retailsales-cube-tables"></a>Liste over RetailSales-kubetabeller

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Catalog
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- Salestable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Få vist listen for den parameter, der skal gå til Synapse-pipelinen

Følgende kommaseparerede liste indeholder de RetailSales-kubevisninger, som pipelinen vil udføre en "vælg"-handling på. Derefter kopieres resultaterne til Data Lake Storage.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> Pipeline-parameteren skal være en liste over visningsnavne, der er adskilt af enkelte kommaer. Der må ikke være mellemrum eller linjetegn.

## <a name="environment-specific-fixes"></a>Miljøspecifik rettelse

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW-rettelse

Visningen **RETAILCHANNELVIEW** indeholder et hard-coded heltal, der repræsenterer en organisation af typen "detailkanal". Den faktiske værdi af typen kan ændres fra miljø til miljø eller fra lejer til lejer.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Følg disse trin for at opdatere de hard-coded heltal.

1. I Dynamics 365 kan du slå **ChannelID-værdien** for din onlinekanal op.
1. Kør følgende forespørgsel på en forekomst af SQL Server Management Studio (SSMS), der er tilknyttet Synapse-databasen.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Kopiér værdien fra første kolonne (**INSTANCERELATIONTYPE**), og indsæt den i visningsdefinitionen.

## <a name="troubleshooting"></a>Fejlfinding

### <a name="pipeline-task-fails"></a>Pipeline-opgaven mislykkes

Der bør være 15 udførelser af pipeline-opgaver til opgaven **CopyData**. Hvis en kørsel mislykkes, skal du validere, at alle afhængige SQL-objekter findes, og at forespørgslerne køres. Det er lettest at komme til alle afhængighederne ved at bruge SSMS til at oprette forbindelse til databasen. Du kan derefter vælge og holde (eller højreklikke) en visning og vælge **Generer OPRET som i et nyt vindue**.

Du kan modtage følgende fejlmeddelelse:

- Fejl: Fejl opstod på siden 'Kilde'
- Ekstern fil til håndtering af fejl: 'Maks. antal fejl'.
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Eksempelscenario

I dette eksempel mislykkes **RetailSales_RetailProductCategory**, og du modtager fejlen "Maks. antal fejl".

Du kan løse denne fejl ved at udføre disse trin:

1. Åbn filen **EntityList.json** i en teksteditor (f.eks. Visual Studio Code).
1. Find visningsdefinitionen for **RetailSales_RetailProductCategory**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Denne visning afhænger kun af én anden visning: **RetailProductCategoryView** _. Find visningsdefinitionen for _*RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Visningen afhænger af tre andre visninger: **RETAILPRODUCTCATEGORY**, **ECORESPRODUCTTRANSLATIONS** og **RETAILCATEGORYEXPANDED**. Find definitionen for hver af disse visninger, og få vist dens afhængigheder. Fortsæt, indtil du finder alle de afhængige visninger.

    Her er hele listen i trærækkefølgen for afhængigheder. Tretten visninger skal valideres.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. I Excel skal du oprette følgende 13 **select count(\*) fra \<view_name\>** opgørelser. Kør disse opgørelser i SSMS, og send resultaterne til tekst. Rul derefter gennem resultaterne for at se, om nogen af visningerne er mislykket. Den første fejl foreslår, at mindst én af visningerne mislykkes.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Du kan kontrollere, hvad du er i gang med at se på ved at oprette en rodafhængig visning, så du kan generere visningsdefinitionen i SSMS. Kontroller derefter, at der er en kolonne i Azure Data Lake-filen, der hedder **r.filepath**. Tilstedeværelse af denne kolonne angiver, at den visning, du undersøger, er læsning af data fra Data Lake Storage.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
