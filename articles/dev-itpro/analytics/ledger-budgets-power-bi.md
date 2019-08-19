---
title: Power BI-indhold til Faktisk vs. budget
description: I dette emne beskrives Power BI-indhold til Faktisk vs. budget. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdet.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a577ab24aaf86c1f7a22953e03f397a2e8213c78
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849423"
---
# <a name="actual-vs-budget-power-bi-content"></a>Power BI-indhold til Faktisk vs. budget

[!include [banner](../includes/banner.md)]

I dette emne beskrives Power BI-indhold til **Faktisk vs. budget**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indholdet til **Faktisk vs. budget** er beregnet til personer, der er ansvarlige for at overvåge performance for faktisk vs. budget i deres organisation. Power BI-indholdet til **Faktisk vs. budget** skaber synlighed i dine budgetafvigelser. Du kan analysere budgettet for det indeværende år efter kontokategori, budgetkode, hovedkonto, beskrivelser af hovedkonto eller regnskabsperiode for at få en bedre forståelse af årsagen til eventuelle afvigelser.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet
Rapporter fra Power BI-indholdet **Faktisk vs. budget** vises i arbejdsområderne **Finansbudgetter og budgetter** og **Regnskabsdirektør**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet
Følgende tabel indeholder oplysninger om de nøgletal, der findes på de enkelte rapportsider i Power BI-indholdet til **Faktisk vs. budget**.

| Rapport                      | Metrik                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Udgifter - Faktisk vs. budget | <ul><li>Samlede udgifter i år</li><li>Budgetterede samlede udgifter i år</li></ul>  |
| Indtægt - Faktisk vs. budget  | <ul><li>Samlet omsætning i år</li><li>Samlet budgetteret omsætning i år</li><ul>     |
| Udgift                     | <ul><li>Samlede udgifter i år</li><li>Mål for udgifter baseret på budget</li><ul> |
| Indtægter                     | <ul><li>Samlet omsætning i år</li><li>Mål for indtægter baseret på budget</li><ul>   |
| Nettoresultat                  | <ul><li>Nettoresultat i år</li><li>Mål for nettoindkomst baseret på budget</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder

| Enhed                    | Indhold                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Finansaktiviteter | Transaktionsbeløb for Finans                                       |
| Budgetaktiviteter         | Transaktionsbeløb for budgetregisteret                                      |
| Hovedkonti             | Hovedkonti til at filtrere rapporter efter                                               |
| Regnskabskalendere          | Regnskabskalendere til at filtrere rapporter efter                                            |
| Finans                   | Finanskonti, der kan bruges til at filtrere rapporten til det aktuelle finansmodul              |
| Budgetkoder              | Budgetkoder, som rapporter kan filtreres efter                                                |
| Juridiske enheder            | Juridiske enheder, der kan bruges til at filtrere rapporten til den aktuelle juridisk enhed |
