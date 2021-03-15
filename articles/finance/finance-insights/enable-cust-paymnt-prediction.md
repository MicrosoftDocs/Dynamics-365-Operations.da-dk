---
title: Aktivere forudsigelser om debitorbetalinger (prøveversion)
description: Dette emne forklarer, hvordan du aktiverer og konfigurere funktionen Forudsigelser om debitorbetalinger i Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 584c1af5f9252a4b8c88a8866a64184bd0595b2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009412"
---
# <a name="enable-customer-payment-predictions-preview"></a>Aktivere forudsigelser om debitorbetalinger (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne forklarer, hvordan du aktiverer og konfigurere funktionen Forudsigelser om debitorbetalinger i Finance Insights. Du kan aktivere funktionen i arbejdsområdet **Administration af funktioner** og angive konfigurationsindstillingerne på siden **Finance Insights-parametre**. Dette emne indeholder også oplysninger, der kan hjælpe dig med at bruge funktionen effektivt.

> [!NOTE]
> Før du fuldfører følgende trin, skal du sørge for at fuldføre de nødvendige trin i emnet [Konfigurere til Finance Insights](configure-for-fin-insites.md).

1. Brug oplysninger fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til at oprette forbindelse til den primære forekomst af Azure SQL for det pågældende miljø. Kør følgende Transact-SQL (T-SQL)-kommando for at aktivere funktioner til sandkassemiljøet. (Du skal muligvis aktivere adgang til din IP-adresse i LCS, før du kan oprette fjernforbindelse til applikationsobjektserveren \[AOS\] .)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > Hvis din installation af Microsoft Dynamics 365 Finance er en Service Fabric-installation, kan du springe dette trin over. Finance Insights-team burde allerede have aktiveret funktionen til dig. Hvis du ikke kan se funktionen i arbejdsområdet **Funktionsstyring**, eller hvis der opstår problemer, når du forsøger at aktivere den, skal du kontakte <fiap@microsoft.com>.

2. Slå funktionen til Indsigt i debitorbetalinger til:

    1. Gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.
    2. Find den funktion, der kaldes **Indsigt i debitorbetaling (prøveversoin)**.
    3. Vælg **Aktiver nu**.

    Funktionen Indsigter i debitorbetaling er nu aktiveret og klar til at blive konfigureret.

3. Konfigurer funktionen til Indsigt i debitorbetalinger:

    1. Gå til **Kredit og rykkere \> Opsætning \> Finance Insights \> Finance Insights-parametre**.

        Siden [![Finance Insigths-parametre, før funktionen er konfigureret](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. På siden **Financial insights-parametre** på fanen **Indsigt i debitorbetalinger** skal du vælge **Vis de datafelter, der bruges i forudsigelsesmodellen**-linket for at åbne siden **Datafelterne til forudsigelsesmodel**. Der kan du få vist standardlisten over felter, der bruges til at oprette en prognosemodel for kunstig intelligens (AI) for debitorbetalingsforudsigelser.

        Hvis du vil bruge standardlisten over felter til at oprette forudsigelsesmodellen, skal du lukke siden **Datafelter til forudsigelsesmodel** og derefter på siden **Financial Insights-parametre** angive indstlilingen **Aktiver funktion** til **Ja**.

    3. Angiv transaktionsperioden til "meget sent" for at definere, hvad forudsigelsen **Meget sent** betyder for virksomheden.

        For hver åben faktura vil systemet estimere betalingssandsynligheden i tre filsæt: **Til tiden**, **Sent** og **Meget sent**.

        - **Til tiden** – Dette filsæt omfatter betalinger, der er angivet til betaling på eller før transaktionens forfaldsdato.
        - **Sent** – Dette filsæt omfatter betalinger, der er angivet til betaling efter forfaldsdatoen for transaktionen, men før starten af transaktionsperioden "Meget sent".
        - **Meget sent** – Dette filsæt omfatter betalinger, der er angivet til betaling efter forfaldsdatoen for transaktionen "Meget sent".

        > [!NOTE]
        > Hvis du ændrer transaktions perioden "meget sent" og vælger **Skift sent-tærskel**, efter at der er oprettet en model til AI-forudsigelse for debitorbetalinger, slettes den eksisterende forudsigelsesmodel, og der oprettes en ny model. Den nye prognosemodel flytter posteringerne til den "meget forsinkede" periode på baggrund af de indstillinger, der blev angivet for at definere den.

    4. Når du er færdig med at definere transaktionsperioden "meget sent", skal du vælge **Opret forudsigelsesmodel** for at oprette forudsigelsesmodellen. Afsnittet **Forudsigelsesmodel** på siden **Financial Insights-parametre** viser status for forudsigelsesmodellen.

        > [!NOTE]
        > Når forudsigelsesmodellen oprettes, kan du når som helst vælge **Nulstil modeloprettelse** for at genstarte processen.

    Funktionen er nu konfigureret og klar til brug.

Når funktionen er slået til og konfigureret, og forudsigelsesmodellen er oprettet og fungerer, viser afsnittet **Forudsigelsesmodel** på siden **Financial Insights-parametre**, at modellen er nøjagtig, som vist i følgende illustration.

[![Nøjagtigheden af forudsigelsesmodellen på siden Financial Insights-parametre](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Frigiv detaljer

Financial Insights, offentlig prøveversion er tilgængelig for prøveimplementeringer i USA, Europa og Storbritannien. Microsoft tilføjer trinvist understøttelse af flere regioner.

De offentlige prøveversionsfunktioner kan og bør kun aktiveres i sandkasse miljøer i niveau 2. Opsætnings- og AI-modeller, der er oprettet i et sandkassemiljø, kan ikke overføres til et produktionsmiljø. Yderligere oplysninger finder du under [Supplerende vilkår for anvendelse af Microsoft Dynamics 365 Prøveversioner](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]