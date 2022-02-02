---
title: Fejlfinde problemer med opsætningen af Finance Insights
description: Dette emne indeholder en oversigt over problemer, der kan opstå, når du bruger funktionerne i Finance Insights. Den forklarer også, hvordan disse problemer kan afhjælpes.
author: panolte
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: c1bbdbec2bc0273a73ffc13a4cce024543af5a13
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968830"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Fejlfinde problemer med opsætningen af Finance Insights

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over problemer, der kan opstå, når du bruger funktionerne i Finance Insights. Den forklarer også, hvordan disse problemer kan afhjælpes.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Symptom: Hvorfor kan jeg ikke tilknytte destinationskolonnen Customer Payment Insights Data Integration-skabelon til destination?

### <a name="resolution"></a>Løsning

Du bruger måske en skabelon til en tidligere version. Inden version 10.0.17 kunne forhåndsversionskunder konfigurere **Resultater af indsigt i kundebetaling (CDS til Fin og Ops)** Dataintegration (DI)-skabelonen ved hjælp af **forudsigelsesmodel for debitorbetalinger (forhåndsversion)**-enheden. Efter en opgradering til 10.0.17 og senere skal du bruge **Resultater af indsigt i kundebetaling (CDS til Fin og Ops 10.0.17 og senere)** DI-skabelonen til at fuldføre tilknytningen. Du kan muligvis ikke tilknytte destinationskolonnen i DI-skabelonen, før listen over datastyringsenheden er opdateret, og enheden for **betalingsudførelsesresultatet** vises i den. Hvis du vil opdatere enhedslisten og få vist resultatet af forudsigelsen af betalingen, skal du udføre trin både i Microsoft Dynamics 365 Finance og Dataverse (tidligere kendt som Common Data Service \[CDS\]-administratorportalen).

### <a name="in-finance"></a>I Finans

Følg disse trin i Finans efter opgraderingen.

1. Gå til **Systemadministration \> Arbejdsområder \> Datastyring**.
2. I arbejdsområdet **Datastyring** skal du markere feltet **Rammeparametre**.
3. Vælg **Enhedsindstillinger** på siden Parametre for **dataimport/eksportstruktur**, og vælg derefter **Listen Opdater enhed**.
4. Luk siden **Parametre for dataimport/eksportstruktur**.
5. I arbejdsområdet **Datastyring** skal du markere feltet **Dataenheder**.
6. Søg efter resultatet af "Forudsigelse af betaling". Kontroller, at enheden for **betalingsudførelsesresultatet** ikke er forhåndsversionsversionen. Navnet på eksempelversionen afsluttes i "(forhåndsversion)." Hvis du kun får vist forhåndsversionen af enheden, kan du kontakte Microsoft Support.

### <a name="in-dataverse"></a>I Dataverse

Følg disse trin i [Power Platform Administration](https://admin.powerplatform.microsoft.com/environments) for at opdatere dine dataintegrationsprojekter.

1. Hvis du bruger en eksempelversion af Finance Insights, skal du fjerne det DI-projekt, der er knyttet til **Resultater af indsigt i kundebetaling (CDS til Fin and Ops)**-skabelonen.
2. Følg trinnene i [Oprette et dataintegratorprojekt](create-data-integrate-project.md). Du kan bruge skabelonen **Resultater af indsigt i kundebetaling (CDS til Fin og Ops 10.0.17 og senere)**.

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Symptom: Når jeg forsøger at åbne AI Builder ved at bruge linkene på opsætningssiden Forudsigelser om debitorbetalinger, hvorfor får jeg vist følgende fejlmeddelelse: "Beklager, der har været en afbrydelse"?

### <a name="resolution"></a>Løsning

Dynamics 365 Finance-brugere skal have en Microsoft Power Apps-brugerkonto til miljøet, og den pågældende brugerkonto skal have rollen Systemtilpasser. Systemadministratoren for Microsoft Power Apps kan oprette brugerkontoen og tildele rollen. Du kan derefter gå til <https://make.preview.powerapps.com/>, logge på med denne brugerkonto og prøve linkene igen.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Symptom: Hvorfor vises der ingen data under fanen Likviditetsbudget i arbejdsområdet til likviditetsbudget?

### <a name="resolution"></a>Løsning

Funktionen til likviditetsbudgettering i Likviditets- og bankstyring og funktionen Likviditetsbudgetter i Finance Insights skal være konfigureret og aktiveret, så der vises data i arbejdsområdet til **likviditetsbudgetter** korrekt.

Opret og aktivér først likviditetsbudget- og likviditetskonti. Du kan finde flere oplysninger under [Likviditetsbudget](../cash-bank-management/cash-flow-forecasting.md). Hvis denne opsætning er fuldført, men du ikke kan se de forventede resultater, kan du finde flere oplysninger i [Fejlfinding af opsætning af likviditetsbudgettering](../cash-bank-management/cash-flow-forecasting-tsg.md).

Bekræft derefter, at funktionen Likviditetsbudgetter i Finance Insights (**Likviditets- og bankstyringsopsætningen \> Konfiguration \> Finance Insights \> likviditetsbudgetter**) er aktiveret, og at uddannelse af AI-modellen er gennemført. Hvis kurset ikke er fuldført, skal du vælge **Budget nu** for at starte modelkurserne.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Symptom: Hvorfor er installationen af en ny tilføjelse knap ikke synlig i Microsoft Dynamics Lifecycle Services?

### <a name="resolution"></a>Løsning

Først skal du kontrollere, at rollen **Miljøbestyrer** eller **Projektejer** er tildelt brugeren i feltet **Projektsikkerhedsrolle** i Microsoft Dynamics Lifecycle Services (LCS). Installation af nye tilføjelsesprogrammet kræver en af disse projektsikkerhedsroller.

Hvis den korrekte projektsikkerhedsrolle er tildelt til dig, skal du måske opdatere browservinduet for at se knappen **Installer et nyt tilføjelsesprogram**.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Symptom: Tilføjelsesprogrammet Finance Insights forekommer ikke at være installation. Hvorfor?

### <a name="resolution"></a>Løsning

Følgende trin bør være udført.

- Kontroller, at du har adgang til **Systemadministrator** og **Systemtilpasser** i Power Portal Administration.
- Kontroller, at der anvendes en Dynamics 365 Finance eller lignende licens til den bruger, der installerer tilføjelsesprogrammet.
- Kontroller, at følgende Azure AD-app er registreret i Azure AD: 

  | Applikation                  | App-id           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
