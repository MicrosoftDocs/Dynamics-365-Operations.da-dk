---
title: "Føje analyser til arbejdsområder ved hjælp af Power BI Embedded"
description: "Dette emne viser, hvordan du kan integrere en Power BI-rapport under fanen Analyser i et arbejdsområde."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 9ee81bbdd22fed4ef6ea97080fe1f6b3d82bcaf5
ms.openlocfilehash: ee95c3d79f7f401c767b9bc8415b21369c14478b
ms.contentlocale: da-dk
ms.lasthandoff: 11/06/2017

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Føje analyser til arbejdsområder ved hjælp af Power BI Embedded

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Denne funktion understøttes i Dynamics 365 for Finance and Operations (version 7.2 og nyere).

## <a name="introduction"></a>Introduktion
Dette emne viser, hvordan du kan integrere en Microsoft Power BI-rapport under fanen **Analyser** i et arbejdsområde. I det eksempel, der er angivet her, skal vi udvide arbejdsområdet **Reservationsstyring** i Flådeadministration-programmet for at integrere et analysearbejdsområde under fanen **Analyser**.

## <a name="prerequisites"></a>Forudsætninger
+ Adgang til et udviklermiljø, der kører platformsopdatering 8 eller nyere.
+ En analyserapport (.pbix-fil), der er oprettet ved hjælp af Microsoft Power BI Desktop, og som har en datamodel, der leveres fra databasen Enhedslager.

## <a name="overview"></a>Overblik
Uanset om du udvider et eksisterende arbejdsområde i et program eller indfører et nyt arbejdsområde, du selv har oprettet, kan du bruge integrerede analysevisninger til at levere nyttig indsigt og interaktive visninger af dine forretningsdata. Tilføjelse af en fane til analyse i et arbejdsområdet består af fire trin.

1. Tilføj en .pbix-fil som en Dynamics 365-ressource.
2. Definer en analysefane i et arbejdsområde.
3. Integrer .pbix-ressourcen under fanen i arbejdsområdet.
4. Valgfrit: Tilføj udvidelser for at tilpasse visningen.

> [!NOTE]
> Du kan finde flere oplysninger om oprettelse af analyserapporter i [Introduktion til Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/). Denne side er en fremragende kilde til indsigt, der kan hjælpe dig med at oprette effektive analyserapporteringsløsninger.

## <a name="add-a-pbix-file-as-a-resource"></a>Tilføje en .pbix-fil som en ressource
Før du begynder, skal du oprette eller anskaffe den Power BI-rapport, du vil integrere i arbejdsområdet. Du kan finde flere oplysninger om oprettelse af analyserapporter i [Introduktion til Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).
 
Følg disse trin for at tilføje en .pbix-fil som en Visual Studio-projektgenstand.

1. Opret et nyt projekt i den relevante model.
2. Vælg projektet i Solution Explorer, højreklik og vælg derefter **Tilføj** > **Nyt element**.
3. I dialogboksen **Tilføj nyt element** under **Operationsgenstande** skal du vælge skabelonen **Ressource**.
4. Angiv et navn, der skal bruges til at referere til rapporten i X ++-metadata, og klik derefter på **Tilføj**.

    ![Dialogboksen Tilføj nyt element](media/analytical-workspace-add.png)

5. Find .pbix filen med definitionen af analyserapporten, og klik derefter på **Åbn**.

    ![Dialogboksen Vælg en ressourcefil](media/analytical-workspace-select-resource.png)
  
Nu, hvor du har tilføjet .pbix filen som en ressource i Dynamics 365, kan du integrere rapporterne i arbejdsområder og tilføje direkte hyperlinks ved hjælp af menupunkter.

## <a name="add-a-tab-control-to-an-application-workspace"></a>Føje et fanekontrolelement til et arbejdsområde i et program
I dette eksempel skal vi udvide arbejdsområdet **Reservationsstyring** i Flådeadministration-modellen ved at tilføje fanen **Analyser** til definitionen af formularen **FMClerkWorkspace**.
 
Følgende illustration viser, hvordan formularen **FMClerkWorkspace** ser ud i designeren i Microsoft Visual Studio.

![FMClerkWorkspace-formular før ændringer](media/analytical-workspace-definition-before.png)

Følg disse trin for at udvide formulardefinitionen for arbejdsområdet **Reservationsstyring**.

1. Åbn formulardesigneren for at udvide designdefinitionen.
2. Vælg det øverste element **Design | Pattern: Workspace Operational** i designdefinitionen.
3. Højreklik, og vælg derefter **New** > **Tab** for at tilføje et nyt kontrolelement med navnet **FormTabControl1**.
4. Vælg **FormTabControl1** i formulardesigneren.
5. Højreklik, og vælg derefter **New Tab Page** for at tilføje en ny fane.
6. Giv fanesiden et nyt, sigende navn, f.eks. **Arbejdsområde**.
7. Vælg **FormTabControl1** i formulardesigneren.
8. Højreklik, og vælg derefter **New Tab Page**.
9. Giv fanesiden til et nyt, sigende navn, f.eks. **Analyse**.
10. Vælg **Analytics (Tab Page)** i formulardesigneren.
11. Indstil egenskaben **Caption** til **Analytics**.
12. Højreklik på kontrolelementet, og vælg derefter **New** > **Group** for at tilføje et nyt formulargruppekontrolelement.
13. Giv formulargruppen et nyt, sigende navn, f.eks. **powerBIRapportGruppe**.
14. I formulardesigneren skal du vælge **PanoramaBody (Tab)** og derefter trække kontrolelementet til fanen **Workspace**.
15. Vælg det øverste element **Design | Pattern: Workspace Operational** i designdefinitionen.
16. Højreklik, og vælg derefter **Remove pattern**.
17. Højreklik igen, og vælg derefter **Add pattern** > **Workspace Tabbed**.
18. Opret et build for at bekræfte ændringerne.
 
I følgende illustration vises designet, når disse ændringer er anvendt.

![FMClerkWorkspace efter ændringer](media/analytical-workspace-definition-after.png)

Nu, hvor du har tilføjet de kontrolelementer til formularen, der skal bruges til at integrere arbejdsområderapporten, skal du definere størrelsen på det overordnede kontrolelement, så det kan rumme layoutet. Som standard er både siden **Filterrude** og siden **Fane** synlige i rapporten. Du kan dog ændre synligheden af disse kontrolelementer alt efter rapportens målforbruger.
 
> [!NOTE]
> Til integrerede arbejdsområder anbefaler vi, at du bruger udvidelser for at skjule både siden **Filterrude** og siden **Fane** med henblik på konsistens.
 
Du har nu fuldført udvidelsen af programformulardefinitionen. Du kan finde flere oplysninger om, hvordan du bruger udvidelser til at foretage tilpasninger, i [Tilpasning: Overlejring og udvidelser](../extensibility/customization-overlayering-extensions.md).

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a>Tilføje X ++-forretningslogik for at integrere et fremviserkontrolelement
Følg disse trin for at tilføje forretningslogik, der initialiserer det kontrolelement til rapportfremvisningen, der er integreret i arbejdsområdet **Reservationsstyring**.

1. Åbn formulardesigneren **FMClerkWorkspace** for at udvide designdefinitionen.
2. Tryk på F7 for at få adgang til koden bag ved kodedefinitionen.
3. Tilføj følgende X++-kode.

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. Opret et build for at bekræfte ændringerne.

Du har nu fuldført tilføjelsen af forretningslogik for at initialisere det integrerede rapportfremviserkontrolelement. I følgende illustration vises arbejdsområdet, når disse ændringer er anvendt.

![Rapport, der er integreret i arbejdsområdet](media/analytical-workspace-final.png)

> [!NOTE]
> Du kan åbne den eksisterende operationsvisning ved hjælp af fanerne i arbejdsområde under sidetitlen.

## <a name="reference"></a>Reference

### <a name="pbireporthelperinitializereportcontrol-method"></a>PBIReportHelper.initializeReportControl-metode
Dette afsnit indeholder oplysninger om den hjælpeklasse, der bruges til at integrere en Power BI-rapport (.pbix-ressource) i et kontrolelement i formulargruppen.

#### <a name="syntax"></a>Syntaks
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a>Parametre

| Navn | Betegnelse |
|---|---|
| resourceName | Navnet på .pbix ressourcen. |
| formGroupControl | Kontrolelementet til formulargruppen, som Power BI-rapportkontrolelementet skal anvendes på. |
| defaultPageName | Standardsidenavnet. |
| showFilterPane | En boolesk værdi, der angiver, om filterruden skal vises (**true**) eller skjules (**false**). |
| showNavPane | En boolesk værdi, der angiver, om navigationsruden skal vises (**true**) eller skjules (**false**). |
| defaultFilters | Standardfiltrene for Power BI-rapporten. |

