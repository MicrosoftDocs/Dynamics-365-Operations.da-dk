---
title: "Opsætning af elektronisk indberetning til at levere strøm BI med data fra Dynamics 365 til operationer"
description: "Dette emne forklarer, hvordan du kan bruge din konfiguration af elektronisk rapportering(ER) til at arrangere overførslen af data fra din forekomst af Dynamics 365 for Operations til Power BI-tjenester. I dette emne bruges som eksempel Intrastat-posteringer som virksomhedens data, der skal overføres. Power BI-kortvisualiseringen bruger disse Intrastat-posteringsdata til at præsentere en visning til analyse af virksomhedens import-/eksportaktiviteter i Power BI-rapporten."
author: kfend
manager: AnnBe
ms.date: 2016-10-31 13 - 22 - 29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ed0192c44b6d7e88120c64e539ebb0ac3b379831
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-electronic-reporting-to-provide-power-bi-with-data-from-dynamics-365-for-operations"></a>Opsætning af elektronisk indberetning til at levere strøm BI med data fra Dynamics 365 til operationer

Dette emne forklarer, hvordan du kan bruge din konfiguration af elektronisk rapportering(ER) til at arrangere overførslen af data fra din forekomst af Dynamics 365 for Operations til Power BI-tjenester. I dette emne bruges som eksempel Intrastat-posteringer som virksomhedens data, der skal overføres. Power BI-kortvisualiseringen bruger disse Intrastat-posteringsdata til at præsentere en visning til analyse af virksomhedens import-/eksportaktiviteter i Power BI-rapporten.

<a name="overview"></a>Overblik
--------

Microsoft Power BI er en samling af softwaretjenester, apps og connectorer, der arbejder sammen for at gøre eksterne datakilder til sammenhængende, visuelt fængslende og interaktiv indsigt. Elektronisk rapportering (ER) gør det muligt for brugere af Microsoft Dynamics 365 for Operations nemt at konfigurere datakilder og arrangere dataoverførsel fra Dynamics 365 for Operations til Power BI. Data overføres som filer i formatet OpenXML-regneark (Microsoft Excel-projektmappefil). De overførte filer gemmes på en Microsoft SharePoint Server, der er konfigureret til dette formål. De gemte filer bruges i Power BI til at oprette rapporter, der omfatter visuelle effekter (tabeller, diagrammer, kort osv.). Power BI-rapporter deles med Power BI-brugere, og der er adgang til dem i Power BI-dashboards og på Dynamics 365 for Operations-sider. I dette emne forklares følgende opgaver:

-   Konfigurere Dynamics 365 for Operations.
-   Forberede konfigurationen af ER-format til at hente data fra Dynamics 365 for Operations.
-   Konfigurere ER-miljøet for at overføre data til Power BI.
-   Bruge overførte data til at oprette en Power BI-rapport.
-   Gøre Power BI-rapporten tilgængelig i Dynamics 365 for Operations.

## <a name="prerequisites"></a>Forudsætninger
Før du kan følge eksemplet i dette emne, skal du have følgende adgang:

-   Adgang til Dynamics 365 for Operations for en af følgende roller:
    -   Udvikler til elektronisk rapportering
    -   Funktionel konsulent i elektronisk rapportering
    -   Systemadministrator
-   Adgang til den SharePoint-server, der er konfigureret til brug sammen med Dynamics 365 for Operations
-   Adgang til strøm Power BI-strukturen

## <a name="configure-document-management-parameters"></a>Konfigurere parametre til dokumentstyring
1.  På siden **Dokumentstyringsparametre** skal du konfigurere adgang til den SharePoint-server, der skal bruges i den virksomhed, som du er logget på (DEMF firmaet i dette eksempel).
2.  Test forbindelsen til SharePoint-serveren for at sikre, at du har fået tildelt adgang. [![Styring af parametre dokumentside](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Åbn det konfigurerede SharePoint-websted. Opret en ny mappe, hvor ER skal gemme Excel-filer, der har de forretningsdata, som Power BI-rapporter kræver som kilde til Power BI-datasæt.
4.  I Dynamics 365 for Operations skal du på siden **Dokumenttyper** oprette en ny dokumenttype, der skal bruges til at få adgang til SharePoint-mappen, du netop har oprettet. Angiv **Fil** i feltet **Gruppe** og **SharePoint** i feltet **Placering**, og angiv derefter adressen på SharePoint-mappen. [![Typer af dokumentside](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Konfigurere ER-parametre
1.  I arbejdsområdet **Elektronisk rapportering** skal du klikke på linket **Parametre til elektronisk rapportering**.
2.  Under fanen **Vedhæftede filer** skal du vælge **Fil** som dokumenttype for alle felter.
3.  I arbejdsområdet **Elektronisk rapportering** skal du aktivere den provider, der kræves, ved at klikke på **Angiv som aktiv**. Yderligere oplysninger finder du ved at afspille opgaveguiden **Vælg ER-serviceudbyder**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Bruge en ER-datamodel som datakilde
Du skal have en ER-datamodel som kilde til forretningsdata, der bruges i Power BI-rapporter. Denne datamodel overføres fra ER konfigurationslageret. Yderligere oplysninger finder du under [Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services](download-electronic-reporting-configuration-lcs.md) eller ved at afspille opgaveguiden **Importere ER-konfiguration fra Lifecycle Services**. Vælg **Intrastat **som den datamodel, der vil blive overført fra det valgte ER-konfigurationslager. (I dette eksempel skal version 1 af modellen bruges.) Du kan derefter få adgang til den **Intrastat** ER model-konfigurationen på den **konfigurationer** side. [![Konfigurationer side](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Designe en ER-formatkonfiguration
Du skal oprette en ny ER-formatkonfiguration, der bruger **Intrastat**-datamodellen som kilde til forretningsdata. Denne formatkonfiguration skal generere outputresultater som elektroniske dokumenter i OpenXML-format (Excel-fil). Yderligere oplysninger finder du ved at afspille opgaveguiden **Oprette en ER-konfiguration til rapporter i OPENXML-format**. Navngiv den nye konfiguration af **import-/eksportaktiviteter** som vist i følgende illustration. Brug Excel-filen med [ER-data - import- og eksportoplysninger](https://go.microsoft.com/fwlink/?linkid=845208) som en skabelon, når du designer ER-formatet. (Afspil for at få oplysninger om, hvordan du importerer en skabelon format guiden opgave.) [![Import / export aktiviteter konfiguration](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) til at ændre den **Import / export aktiviteter** formatere konfiguration, skal du følge disse trin.

1.  Klik på **Designer**.
2.  Under fanen **Format** skal du navngive filelementet for dette format **Excel-outputfil**. [![Excel output-fil-element](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  Under fanen **Overførsel** skal du angive navnet på den Excel-fil, der skal oprettes, når dette format køres. Konfigurer det relaterede udtryk for at returnere værdien **Import- og eksportoplysninger** (filtypenavnet .xlsx tilføjes automatisk). [![Format designer](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Tilføj et nyt element for datakilde til dette format. (Denne fasttekst er påkrævet for yderligere databinding).
    1.  Navngive datakilden **retning\_enum**.
    2.  Vælg **Fasttekst til datamodel** som datakildetype.
    3.  Henvis til fastteksten **Retning** for datamodel.

    [![retning\_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  Fuldfør bindingen af elementer i **Intrastat**-datamodellen og elementer i designformatet som vist i følgende illustration. [![Fuldfører bindingen](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Når den er kørt, genererer ER-formatet outputresultatet i Excel-format. Den sender oplysninger om Intrastat-transaktionerne til outputresultatet og adskiller dem som transaktioner, der beskriver enten importaktiviteter eller eksportaktiviteter. Klik på **køre** til at teste det nye format ER en liste over Intrastat-posteringer på den **Intrastat** side (**skat**&gt;**erklæringer**&gt;**Udenrigshandel**&gt;**Intrastat**). [![Intrastat-side](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) der oprettes følgende output resultat. Filen hedder **Import- og eksportoplysninger.xlsx**, som du har angivet i formateringsindstillingerne. [![Import og eksport af details.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Konfigurere ER-destinationen
Du skal konfigurere ER-strukturen til at sende outputresultatet af den nye ER-formatkonfiguration på en særlig måde.

-   Outputresultatet skal sendes til mappen på den valgte SharePoint-Server.
-   Hver afvikling af formatkonfigurationen skal oprette en ny version af samme Excel-fil.

På den **elektronisk indberetning** side (**virksomhedsadministration**&gt;**elektronisk indberetning**), skal du klikke på den **elektronisk rapportering destination** vare, og Tilføj en ny destination. I feltet **Reference** skal du vælge **Import-/eksportaktiviteter**-formatkonfigurationen, du oprettede tidligere. Følg disse trin for at tilføje en ny post for fildestination til referencen.

1.  Brug feltet **Navn** til at angive titlen på fildestinationen.
2.  I feltet **Filnavn** skal du vælge navnet **Excel-outputfil** for komponenten Excel-filformat.

Klik på knappen **Indstillinger** til den nye destinationspost. I **Indstillinger for destination**-dialogboksen skal du følge disse trin.

1.  Under fanen **Power BI** skal du angive indstillingen **Aktiveret** til **Ja**.
2.  I feltet **SharePoint** skal du vælge den **Delt**-dokumenttype, du oprettede tidligere.

## <a name="schedule-execution-of-the-configured-er-format"></a>Planlægge kørsel af konfigureret ER-format
På den **konfigurationer** side (**virksomhedsadministration**&gt;**elektronisk indberetning**&gt;**konfigurationer**), i træet konfigurationer, skal du vælge den **Import / export aktiviteter** konfiguration, du oprettede tidligere. Skift status for version 1.1 fra **Udkast** til **Komplet** for at gøre dette format tilgængeligt til brug. [![Konfigurationer side](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) Vælg den færdige version af den **Import / export aktiviteter** konfiguration og derefter klikke på **køre**. Bemærk, at der anvendes den destination, der er konfigureret til outputresultatet, som genereres i Excel-format. Angiv indstillingen **Batchbehandling** til **Ja** for at køre denne rapport i fuldautomatisk tilstand. Klik på **Gentages** for at planlægge den krævede gentagelse af denne batchkørsel. Gentagelsen definerer, hvor ofte de opdaterede data overføres fra Dynamics 365 for Operations til Power BI. [![Dialogboksen parametre for elektronisk rapport](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) når den er konfigureret, kan du finde ER kørsel af rapporten på den **kørsler** side (**systemadministration &gt;forespørgsler &gt;kørsler**). [![Batch job siden](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) når dette job køres for første gang, destinationen, der opretter en ny Excel-fil med det navn, der er konfigureret i det valgte SharePoint-mappe. Hver gang jobbet køres, opretter destinationen en ny version af denne Excel-fil. [![Ny version af Excel-fil](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Oprette et Power BI-datasæt ved hjælp af outputresultatet i ER-formatet
Log på Power BI, og åbn en eksisterende Power BI-gruppe (arbejdsområde), eller opret en ny gruppe. Enten klikke på **Tilføj** under **filer** i den **Import- eller Opret forbindelse til Data** afsnit, eller klik på plus-tegnet (**+**) ud for **datasæt** i venstre rude. [![Oprettelse af et dataset](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) Vælg den **SharePoint-gruppewebsteder** indstilling, og angiv derefter stien til SharePoint Server, du vil bruge (**https://ax7partner.spoppe.com** i vores eksempel). Gå derefter til mappen **/Delte dokumenter/GER data/PowerBI**, og vælg den Excel-fil, du har oprettet som kilde for data til det nye Power BI-datasæt. [![At vælge Excel-fil](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) skal du klikke på **Connect**, og klik derefter på **Import**. Der oprettes et nyt datasæt, der er baseret på den valgte Excel-fil. Datasættet kan også føjes automatisk til det nyoprettede dashboard. [![DataSet på dashboardet](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) konfigurere tidsplanen for dette dataset for at tvinge en periodisk opdatering opdatering. Periodiske opdateringer gør det muligt at bruge nye forretningsdata, der kommer fra Dynamics 365 for Operations, via periodisk kørsel af ER-rapporten gennem nye versioner af den Excel-fil, der oprettes på SharePoint-serveren.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Oprette en Power BI-rapport ved hjælp af det nye datasæt
Hvis du vil oprette en ny Power BI-rapport, skal du klikke på det **Import- og eksportoplysninger** Power BI-datasæt, du har oprettet. Konfigurer derefter den visuelle effekt. Du kan for eksempel vælge **Kartogram** som visualisering og konfigurere den som følger:

-   Tildel **CountryOrigin**-feltet i datasættet til feltet **Placering** i kortvisualiseringen.
-   Tildel **Mængde**-feltet i datasættet til feltet **Farvemætning** i kortvisualiseringen.
-   Tilføj **Aktivitet**- og **År**-datasætfelterne til felterne **Filtre** i kortvisualiseringen.

Gem Power BI-rapporten som **Import- og eksportoplysningsrapport**. [![Importere og eksportere oplysninger rapport](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Bemærk, at kortet viser de lande/regioner, der er nævnt i Excel-filen (Østrig og Schweiz i dette eksempel). Disse lande/områder er farvet for at vise den procentvise andel af de fakturerede beløb for hver. Opdater listen over Intrastat-transaktioner. Der tilføjes en eksporttransaktion, der kommer fra Italien. [![Liste over Intrastat-transaktioner,](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) vente på næste planlagte kørsel af rapporten ER og den næste planlagte opdatering af strøm BI dataset. Gennemgå derefter Power BI-rapporten (vælg kun at få vist importtransaktioner). Det opdaterede kort viser nu Italien. [![Opdaterede kort](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>Få adgang til Power BI-rapport i Dynamics 365 for Operations
Konfigurer integrationen mellem Dynamics 365 for Operations og Power BI. Yderligere oplysninger finder du under [Konfiguration af Power BI til arbejdsområder](configure-power-bi-integration.md). På den **elektronisk indberetning** side af arbejdsområdet, der understøtter Power BI integration (**virksomhedsadministration**&gt;**arbejdsområder**&gt;**elektronisk rapportering arbejdsområde**), skal du klikke på **indstillinger**&gt;**åbne rapporten katalog**. Vælg den **Import- og eksportoplysninger** Power BI-rapport, du har oprettet, for at få vist rapporten som et handlingselement på den valgte side. Klik på handlingselement for at åbne den Dynamics 365 for Operations-side, der viser den rapport, du har designet i Power BI. [![Importere og eksportere oplysninger om rapport](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Se også
--------

[Destinationer for elektronisk rapportering](electronic-reporting-destinations.md)

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)


