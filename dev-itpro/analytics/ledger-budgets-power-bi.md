---
title: Power BI-indhold til Faktisk vs. budget
description: "I dette emne beskrives Power BI-indhold til Faktisk vs. budget. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdet."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5d52cce3cccb16f0645d9de1832ebeffbfaf3a09
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Power BI-indhold til Faktisk vs. budget

[!include[banner](../includes/banner.md)]


I dette emne beskrives Microsoft Power BI-indhold til **Faktisk vs. budget**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken. 

# <a name="overview"></a>Overblik

Power BI-indholdet til **Faktisk vs. budget** er beregnet til personer, der er ansvarlige for at overvåge performance for faktisk vs. budget i deres organisation. Power BI-indholdet til **Faktisk vs. budget** skaber synlighed i dine budgetafvigelser. Du kan analysere budgettet for det indeværende år efter kontokategori, budgetkode, hovedkonto, beskrivelser af hovedkonto eller regnskabsperiode for at få en bedre forståelse af årsagen til eventuelle afvigelser. 

# <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold
Hvis du bruger opdateringen til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition fra juli 2017, vises rapporter fra Power BI-indholdet til **Faktisk vs. budget** i arbejdsområderne **Finansbudgetter og budgetter** og **Regnskabsdirektør**.

# <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet
Følgende tabel indeholder oplysninger om de nøgletal, der findes på de enkelte rapportsider i Power BI-indholdet til **Faktisk vs. budget**.

| Rapport                      | Metrik |
|-----------------------------|---------|
| Udgifter - Faktisk vs. budget | <ul><li>Samlede udgifter i år</li><li>Budgetterede samlede udgifter i år</li></ul> |
| Indtægt - Faktisk vs. budget  | <ul><li>Samlet omsætning i år</li><li>Samlet budgetteret omsætning i år</li><ul> |
| Udgift                     | <ul><li>Samlede udgifter i år</li><li>Mål for udgifter baseret på budget </li><ul> |
| Indtægter                     | <ul><li>Samlet omsætning i år</li><li>Mål for indtægter baseret på budget </li><ul> |
| Nettoresultat                  | <ul><li>Nettoresultat i år</li><li>Mål for nettoindkomst baseret på budget </li><ul> |

## <a name="extending-the-power-bi-content"></a>Udvidelse af Power BI-indhold
Når du bruger de indholdspakker, der er tilgængelige i Microsoft Dynamics Lifecycle Services (LCS), kan du levere fremragende analyser til personer, der ikke logger på Microsoft Dynamics 365. Du kan redigere disse indholdspakker, så de omfatter andre rapporter eller grafik, og derefter udgive indholdspakkerne på din Power BI.com-lejer med henblik på analyse. 

Du kan finde Power BI-indholdet til **Faktisk vs. budget** i biblioteket med delte aktiver i LCS. Du kan finde flere oplysninger om, hvordan du downloader indhold og implementerer det i din organisation, under [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md). Hvis du vil se en demo, der viser, hvordan du implementerer Power BI-indholdet, kan du se dette Office Mix [Power BI-indhold fra Microsoft og dine partnere i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

# <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder

| Enhed                    | Indhold |
|---------------------------|----------|
| Finansaktiviteter | Transaktionsbeløb for Finans |
| Budgetaktiviteter         | Transaktionsbeløb for budgetregisteret |
| Hovedkonti             | Hovedkonti til at filtrere rapporter efter |
| Regnskabskalendere          | Regnskabskalendere til at filtrere rapporter efter |
| Finans                   | Finanskonti, der kan bruges til at filtrere rapporten til det aktuelle finansmodul |
| Budgetkoder              | Budgetkoder, som rapporter kan filtreres efter |
| Juridiske enheder            | Juridiske enheder, der kan bruges til at filtrere rapporten til den aktuelle juridisk enhed |

