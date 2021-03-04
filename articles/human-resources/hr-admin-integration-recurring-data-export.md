---
title: Opret en app til tilbagevendende dataeksport
description: Denne artikel viser, hvordan du opretter en Microsoft Azure-logikapp, der eksporterer data fra Microsoft Dynamics 365 Human Resources i en tilbagevendende tidsplan.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: edd4b999624a845fc145ed9ff348ae9cba782719
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417846"
---
# <a name="create-a-recurring-data-export-app"></a>Opret en app til tilbagevendende dataeksport

Denne artikel viser, hvordan du opretter en Microsoft Azure-logikapp, der eksporterer data fra Microsoft Dynamics 365 Human Resources i en tilbagevendende tidsplan. Selvstudiet benytter REST API for DMF-pakke (programmeringsgrænseflade til program) i Personale til at eksportere dataene. Når dataene er eksporteret, gemmer logikappen den eksporterede datapakke i en Microsoft OneDrive for Business-mappe.

## <a name="business-scenario"></a>Forretningsscenarie

I et typisk forretningsscenarie til Microsoft Dynamics 365-integration skal data eksporteres til et downstream-system i en tilbagevendende tidsplan. Dette selvstudium viser, hvordan du kan eksportere alle poster for arbejdere fra Microsoft Dynamics 365 Human Resources og gemme listen over arbejdere i en OneDrive for Business-mappe.

> [!TIP]
> De specifikke data, der eksporteres i dette selvstudium, og destinationen for de eksporterede data, er kun eksempler. Du kan nemt ændre dem, så de opfylder dine forretningsbehov.

## <a name="technologies-used"></a>Anvendte teknologier

I dette selvstudium bruges følgende teknologier:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – Masterdatakilden for arbejdere, der skal eksporteres.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – Den teknologi, der omfatter organisering og planlægning af den tilbagevendende eksport.

    - **[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – Den teknologi, der bruges til at forbinde logikappen med de nødvendige slutpunkter.

        - [HTTP med Azure AD](https://docs.microsoft.com/connectors/webcontents/)-connector
        - [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)-connector

- **[REST API for DMF-pakke](../dev-itpro/data-entities/data-management-api.md)** – den teknologi, der bruges til at udløse eksporten og overvåge, hvordan den skrider frem.
- **[OneDrive for Business](https://onedrive.live.com/about/business/)** – Destinationen for de eksporterede arbejdere.

## <a name="prerequisites"></a>Forudsætninger

Før du starter øvelsen i dette selvstudium, skal du have følgende elementer:

- Et Personale-miljø med administratorrettigheder i miljøet
- Et [Azure-abonnement](https://azure.microsoft.com/free/) som vært for logikappen

## <a name="the-exercise"></a>Øvelsen

I slutningen af denne øvelse har du en logikapp, der har forbindelse til dit Personale-miljø og din OneDrive for Business-konto. Logikappen eksporterer en datapakke fra Personale; vent til eksporten er fuldført, hent den eksporterede datapakke, og gem datapakken i den OneDrive for Business-mappe, du har angivet.

Den fuldførte logikapp ligner den i følgende illustration.

![Oversigt over logikapp](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>Trin 1: Opret et dataeksportprojekt i Personale

Opret i Personale et dataeksportprojekt, der eksporterer arbejdere. Navngiv projektet **Eksport af medarbejdere**, og sørg for, at indstillingen **Generér datapakke** er angivet til **Ja**. Føj en enkelt enhed (**Arbejder**) til projektet, og vælg det format, der skal eksporteres i. (Microsoft Excel-formatet bruges i dette selvstudium).

![Dataprojektet Eksport af medarbejdere](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Husk navnet på dataeksportprojektet. Du skal bruge det, når du opretter logikappen i næste trin.

### <a name="step-2-create-the-logic-app"></a>Trin 2: Opret logikappen

Hovedparten af opgaven omfatter oprettelse af logikappen.

1. Opret en logikapp i Azure-portalen.

    ![Side til oprettelse af logikapp](media/integration-logic-app-creation-1.png)

2. Start med en tom logikapp i Logic Apps Designer.
3. Tilføj en [udløser for gentagelsesplan](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) for at køre logikappen hver 24. time (eller i henhold til en tidsplan efter eget valg).

    ![Dialogboksen Gentagelse](media/integration-logic-app-recurrence-step.png)

4. Kald [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST-API for at planlægge eksport af din datapakke.

    1. Brug handlingen **Kald en HTTP-anmodning** fra HTTP med Azure AD-connector.

        - **URL-adresse til grundlæggende ressourcer:** URL-adressen til dit Personale-miljø (medtag ikke oplysninger om sti/navneområde).
        - **Azure AD-ressource URI-adresse:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > Personale-tjenesten har endnu ikke en connector, der viser alle de API'er, der udgør REST API for DMF-pakken, f.eks. **ExportToPackage**. Du skal i stedet kalde API'erne ved at bruge rå HTTPS-anmodninger via HTTP med Azure AD-connector. Denne connector bruger Azure Active Directory (Azure AD) til godkendelse og autorisation til Personale.

        ![HTTP med Azure AD-connector](media/integration-logic-app-http-aad-connector-step.png)

    2. Log på Personale-miljøet via HTTP med Azure AD-connector.
    3. Konfigurer en HTTP **POST**-anmodning for at kalde **ExportToPackage** DMF REST-API'en.

        - **Metode:** POST
        - **URL-adresse for anmodning:** https://\<hostname\>/navneområder/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **Indhold i anmodningen:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Aktivere en HTTP-anmodningshandling](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > Det kan være en god ide at omdøbe hvert trin, så det er mere sigende end standardnavnet **Kald en HTTP-anmodning**. Du kan f.eks. omdøbe dette trin **ExportToPackage**.

5. [Initialiser en variabel](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) for at gemme udførelsesstatus for anmodningen **ExportToPackage**.

    ![Handlingen Initialiser variabel](media/integration-logic-app-initialize-variable-step.png)

6. Vent, indtil udførelsesstatus for dataeksport er **Fuldført**.

    1. Tilføj en [Indtil loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop), der gentages, indtil værdien af variablen **ExecutionStatus** er **Fuldført**.
    2. Tilføj en **Forsinkelse**-handling, der venter fem sekunder, før der sendes en forespørgsel om den aktuelle udførelsesstatus for eksporten.

        ![Indtil løkke-container](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Angiv grænseantallet til **15** for at vente maksimalt 75 sekunder (15 gentagelser × 5 sekunder), til eksporten er fuldført. Hvis eksporten tager længere tid, skal du justere grænsen for antal efter behov.        

    3. Tilføj en **Kald en HTTP-anmodning**-handling for at kalde [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST-API, og angiv variablen **ExecutionStatus** til resultatet af **GetExecutionSummaryStatus**-svaret.

        > I dette eksempel udføres der ikke fejlkontrol. **GetExecutionSummaryStatus**-API'en kan returnere ikke-gennemførte terminaltilstande (dvs. tilstande, der ikke er angivet til **Fuldført**). Yderligere oplysninger finder du i [API-dokumentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).

        - **Metode:** POST
        - **URL-adresse for anmodning:** https://\<hostname\>/navneområder/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **Indhold i anmodningen:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > Du skal muligvis angive værdien for **Indhold i anmodningen** i kodevisning eller i funktionseditoren i designeren.

        ![Handlingen Aktiver en HTTP-anmodning 2](media/integration-logic-app-get-execution-status-step.png)

        ![Handlingen Angiv variabel](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > Værdien for handlingen **Angiv variabel** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) adskiller sig fra værdien for **Aktiver en HTTP-anmodning 2**-indholdsværdi, også selv om designeren viser værdierne på samme måde.

7. Hent URL-adressen til hentning for den eksporterede pakke.

    - Tilføj en **Kald en HTTP-anmodning**-handling for at kalde [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST-API'en.

        - **Metode:** POST
        - **URL-adresse for anmodning:** https://\<hostname\>/navneområder/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **Indhold i anmodningen:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![GetExportedPackageURL-handling](media/integration-logic-app-get-exported-package-step.png)

8. Hent den eksporterede pakke.

    - Tilføj en HTTP **GET**-anmodning (en indbygget [HTTP-connectorhandling](https://docs.microsoft.com/azure/connectors/connectors-native-http)) for at hente pakken fra den URL-adresse, der blev returneret i forrige trin.

        - **Metode:** GET
        - **URI-adresse:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > Du skal muligvis angive værdien for **URI-adresse** i kodevisning eller i funktionseditoren i designeren.

        ![HTTP GET-handling](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > Denne anmodning kræver ingen yderligere godkendelse, fordi den URL-adresse, som **GetExportedPackageUrl**-API'en returnerer, inkluderer et token for signaturer til delt adgang, der giver adgang til at hente filen.

9. Gem den hentede pakke ved hjælp af [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)-connector.

    - Tilføj en OneDrive for Business [Opret fil](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file)-handling.
    - Opret forbindelse til OneDrive for Business-kontoen efter behov.

        - **Mappesti:** En mappe efter eget valg
        - **Filnavn:** worker\_package.zip
        - **Filindhold:** Indholdet fra det forrige trin (dynamisk indhold)

        ![Oprette filhandling](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>Trin 3: Test logikappen

Hvis du vil teste logikappen, skal du vælge knappen **Kør** i designeren. Du kan se, at trinnene i logikappen begynder at blive afviklet. Efter 30 til 40 sekunder bør logikappen være færdig med at køre, og din OneDrive for Business-mappe bør indeholde en ny pakkefil, der indeholder de eksporterede arbejdere.

Hvis der rapporteres om en fejl for et af trinnene, skal du vælge det trin, der er fejl ved, i designerne og undersøge felterne **Input** og **Output** for det. Foretag fejlfinding, og juster trinnet som nødvendigt for at rette fejlene.

I følgende illustration vises det, hvordan Logic Apps Designer ser ud, når alle trin i logikappen kører korrekt.

![Gennemført kørsel af logikapp](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Resume

I dette selvstudium lærte du, hvordan du kan bruge en logikapp til at eksportere data fra Personale og gemme de eksporterede i en OneDrive for Business-mappe. Du kan ændre trinene i dette selvstudium efter behov, så det passer til dine forretningsbehov.




[!INCLUDE[footer-include](../includes/footer-banner.md)]