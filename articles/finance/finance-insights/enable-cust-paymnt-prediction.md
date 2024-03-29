---
title: Aktivere forudsigelser om debitorbetalinger
description: Denne artikel forklarer, hvordan du aktiverer og konfigurere funktionen Forudsigelser om debitorbetalinger i Finance Insights.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f04ee9db5efe3595dea30d641c5097d6b90c0d77
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898201"
---
# <a name="enable-customer-payment-predictions"></a>Aktivere forudsigelser om debitorbetalinger

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du aktiverer og konfigurere funktionen Forudsigelser om debitorbetalinger i Finance Insights. Du kan aktivere funktionen i arbejdsområdet **Administration af funktioner** og angive konfigurationsindstillingerne på siden **Konfiguration af Finance Insights**. Denne artikel indeholder også oplysninger, der kan hjælpe dig med at bruge funktionen effektivt.

> [!NOTE]
> Før du fuldfører følgende trin, skal du sørge for at fuldføre de nødvendige trin i artiklen [Konfigurere til Finance Insights](configure-for-fin-insites.md).

1. Slå funktionen til Forudsigelser om debitorbetalinger til:

    1. Åbn arbejdsområdet **Administration af funktioner**.
    2. Vælg **Søg efter opdateringer**.
    3. Søg efter **Forudsigelser om debitorbetalinger** under fanen **Alle**. Hvis du ikke kan finde denne funktion, skal du søge efter **(Forhåndsversion) Forudsigelser om debitorbetalinger**. 
    4. Slå funktionen til.

    Funktionen Forudsigelser om debitorbetalinger er nu aktiveret og klar til at blive konfigureret.

2. Konfigurer funktionen til Indsigt i debitorbetalinger:

    1. Gå til **Kredit og rykkere \> Opsætning \> Finance Insights \> Forudsigelser om debitorbetalinger**.
    2. På siden **Konfiguration af Finance Insights** på fanen **Forudsigelser om debitorbetalinger** skal du vælge **Vis de datafelter, der bruges i forudsigelsesmodellen** for at åbne siden **Datafelter til forudsigelsesmodel**. Der kan du få vist standardlisten over felter, der bruges til at oprette en prognosemodel for kunstig intelligens (AI) for debitorbetalingsforudsigelser.

        Hvis du vil bruge standardlisten over felter til at oprette forudsigelsesmodellen, skal du lukke siden **Datafelter til forudsigelsesmodel** og derefter på siden **Konfiguration af Finance Insights** angive indstillingen **Aktivér funktion** til **Ja**.
        
   > [!NOTE]
   > Funktionen **Forudsigelser om debitorbetalinger** kræver mere end 100 transaktioner i de foregående seks til ni måneder. Transaktionerne kan omfatte fritekstfakturaer, salgsordrer og debitorbetalinger. Disse data skal fordeles på tværs af indstillingerne **Til tiden**, **For sent** og **Meget sent**.    
     

    3. Angiv transaktionsperioden til "meget sent" for at definere, hvad forudsigelsen **Meget sent** betyder for virksomheden.

        For hver åben faktura vil systemet estimere betalingssandsynligheden i tre filsæt: **Til tiden**, **Sent** og **Meget sent**.

        - **Til tiden** – Dette filsæt omfatter betalinger, der er angivet til betaling på eller før transaktionens forfaldsdato.
        - **Sent** – Dette filsæt omfatter betalinger, der er angivet til betaling efter forfaldsdatoen for transaktionen, men før starten af transaktionsperioden "Meget sent".
        - **Meget sent** – Dette filsæt omfatter betalinger, der er angivet til betaling efter forfaldsdatoen for transaktionen "Meget sent".

        > [!NOTE]
        > Hvis du ændrer transaktions perioden "meget sent" og vælger **Skift sent-tærskel**, efter at der er oprettet en model til AI-forudsigelse for debitorbetalinger, slettes den eksisterende forudsigelsesmodel, og der oprettes en ny model. Den nye prognosemodel flytter posteringerne til den "meget forsinkede" periode på baggrund af de indstillinger, der blev angivet for at definere den.

    4. Når du er færdig med at definere transaktionsperioden "meget sent", skal du vælge **Opret forudsigelsesmodel** for at oprette forudsigelsesmodellen. Afsnittet **Forudsigelsesmodel** på siden **Konfiguration af Finance Insights** viser status for forudsigelsesmodellen.

        > [!NOTE]
        > Når forudsigelsesmodellen oprettes, kan du når som helst vælge **Nulstil modeloprettelse** for at genstarte processen.

    Funktionen er nu konfigureret og klar til brug.

Når funktionen er slået til og konfigureret, og forudsigelsesmodellen er oprettet og fungerer, viser afsnittet **Forudsigelsesmodel** på siden **Finance Insights-parametre** modellens nøjagtighed.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
