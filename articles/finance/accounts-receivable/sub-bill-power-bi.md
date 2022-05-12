---
title: Abonnementsfakturering Power BI-indhold
description: Dette emne beskriver, hvad der er omfattet af abonnementsfakturering i Microsoft Power BI-indholdet.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: fad96bdaf60e7772e9ea1ff937435b0274303505
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645395"
---
# <a name="subscription-billing-power-bi-content"></a>Abonnementsfakturering Power BI-indhold

[!include[banner](../includes/banner.md)]

Dette emne beskriver, hvad der er omfattet af abonnementsfakturering i Microsoft Power BI-indholdet. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken. 

## <a name="overview"></a>Overblik

Faktureringsindhold til Power BI-abonnement er oprettet for abonnementsfaktureringsassistenter og ledere. Den indeholder nøgleværdier for abonnementsfakturering, f.eks. MRR (månedligt tilbagevendende omsætning) til faktureringsplaner, og oplysninger om vandfald om udsættelser. Dataene bruges fra faktureringsplanerne og udskudte planer til at give et overblik over tilbagevendende indtægter og indtægter.

Indholdet Power BI har følgende tre faner, der giver i alt fire analyserapporter: 

- **Analyser – MRR** – Denne fane indeholder rapporten **Månedlig tilbagevendende fakturering** og rapporten **Faktureringsplandetaljer**.
- **Analyser – Waterfall** – Denne fane viser rapporten **Indtægtskilde**.
- **Analyser – Afskrivningssaldo** – Denne fane indeholder rapporten **Afskrivningssaldo**.

## <a name="view-data-on-the-analytical-reports"></a>Få vist data på analyserapporter

Før du kan få vist data på analyserapporterne, skal du køre en periodisk proces, der genererer rapporteringsdataene for hver enkelt rapport. Disse data, som rapporterne kræver, skal genereres, da de ikke gemmes direkte i databasen. 

1. Gå til **Abonnementsfakturering \> Tilbagevendende kontraktfakturering \> \> Batchbehandling af MRR-analyserapport**, og benyt følgende fremgangsmåde:

    1. Angiv et datointerval på højst tre år.
    2. Valgfrit: Konfigurer et batchprocesjob, der gentages, så dataene jævnligt opdateres.
    3. Vælg **OK**.

2. Når batchjobbet er kørt færdigt, skal du gå til **Systemadministration \> Opsætning \> Enhedsbutik**, og opdater den aggregerede måling i **MRR-rapporten**. 
3. Gå til **Abonnementsfakturering \> Udskydelser af omsætning og udgifter \> Periodiske opgaver \> Batchbehandling af vandfaldsanalyserapport**, og benyt følgende fremgangsmåde:

    1. Angiv en startdato og en slutdato, der højst dækker 26 perioder. 
    2. Hvis du vil have vist det budgetterede beløb for tidligere perioder i den aktuelle periode, skal du angive indstillingen **Budgetterede tidligere beløb i den aktuelle periode** til **Ja**.
    3. Valgfrit: Konfigurer et batchprocesjob, der gentages, så dataene jævnligt opdateres.
    4. Vælg **OK**. 

4. Når batchjobbet er kørt færdigt, skal du gå til **Systemadministration \> Opsætning \> Enhedsbutik**, og opdater **Vandfaldsrapport**-samlede måling.
5. Gå til **Abonnementsfakturering \> Udskydelser af omsætning og udgifter \> Periodiske opgaver \> Batchbehandling af analyserapport over saldoafskrivning**, og benyt følgende fremgangsmåde:

    1. Angiv en startdato og en slutdato, der højst dækker 26 perioder. 
    2. Hvis du vil have vist det budgetterede beløb for tidligere perioder i den aktuelle periode, skal du angive indstillingen **Budgetterede tidligere beløb i den aktuelle periode** til **Ja**.
    3. Valgfrit: Konfigurer et batchprocesjob, der gentages, så dataene jævnligt opdateres.
    4. Vælg **OK**.

6. Når batchjobbet er kørt færdigt, skal du gå til **Systemadministration \> Opsætning \> Enhedsbutik**, og opdater **Rapport om afskrivningssaldo**-samlede måling.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet

Faktureringsindholdet af Power BI-abonnement vises i arbejdsområdet til **abonnementsfakturering**.
