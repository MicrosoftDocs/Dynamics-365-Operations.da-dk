---
title: Power BI-indhold til Faktisk vs. budget
description: Denne artikel beskriver Power BI-indhold til Faktisk vs. budget. Det forklarer, hvordan du får adgang til rapporterne, og giver oplysninger om datamodellen.
author: panolte
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ff57d052b66103ad716ad8d55afb4fcb095d2c02
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847276"
---
# <a name="actual-vs-budget-power-bi-content"></a>Power BI-indhold til Faktisk vs. budget

[!include [banner](../includes/banner.md)]

Denne artikel beskriver Microsoft Power BI-indhold til **Faktisk vs. budget**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]