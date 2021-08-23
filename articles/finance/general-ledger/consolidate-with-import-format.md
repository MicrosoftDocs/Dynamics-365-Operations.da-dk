---
title: Import af format til konsolidering
description: Dette emne indeholder detaljerede oplysninger om det importformat, der bruges til konsolidering af økonomiske data fra flere juridiske enheder.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6d25ebfedfe748dfa262c1d4b0671539e6150a0f9f05dfca42e87f23486fbb19
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746410"
---
# <a name="import-format-for-consolidation"></a>Import af format til konsolidering

[!include [banner](../includes/banner.md)]

Dette emne indeholder detaljerede oplysninger om det importformat, der bruges til konsolidering af økonomiske data fra flere juridiske enheder. Importformatet skal gemmes som en tekstfil (.txt).

## <a name="import-format"></a>Importformat

Følgende tabel indeholder det importformat, du skal bruge, når du laver en konsolidering under en import.

| Posttabel | Formater | Notater |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>Posttabellen</li><li>Kildens hovedkonto-id</li><li>Hovedkontolinjen</li><li>Hovedkontotypen</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Hovedkonto-id</li><li>Transaktionsdatoen</li><li>Regnskabsperiodetypen (**0** = Start, **1** = Drift og **2** = Ultimo)</li><li>Posteringsvaluta</li><li>Debet eller kredit (**0** = Debet og **1** = Kredit)</li><li>Posteringslag</li><li>Transaktionsbeløb</li><li>Kvantitet</li><li>Den lokale RecID (entydig værdi for int64 for posteringen)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Postnummeret (posteringsnummer i budgethoved)</li><li>Standarddatoen i budgetregisteret</li><li>Budgetmodel-id'et</li><li>Budgettype (**1** - Oprindeligt budget, **2** - Overførsel, **3** - Revision, **4** - Behæftelse, **5** - Forudgående behæftelse, **6** - Overført budget, **7** - Projekt, **8** - Anlægsaktiver, **9** - Efterspørgselsprognose, **10** - Forsyningsprognose, **11** - Fordelinger, **12** - Foreløbigt budget).</li><li>Dato for linjen</li><li>Hovedkonto-id for linjen</li><li>Valutakoden for linjen</li><li>Beløbet på linjen i transaktionsvalutaen</li><li>Værdien for heltal for budgettypen for linjen (udgift eller omsætning)</li></ul> |
| 4            | DEMF | RecordCompany er den juridiske kildeenhed. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Hovedkonto-id</li><li>Transaktionsdato</li><li>Regnskabsperiodetype (0 Start, 1 Drift og 2 Ultimo)</li><li>Transaktionsvaluta</li><li>Debet eller kredit (0 for Debet og 1 for Kredit)</li><li>Posteringslag</li><li>Transaktionsbeløb</li><li>Mængde</li><li>Lokalt RecID (entydig værdi for int64 for posteringen)</li></ul>  |
| 6            | BusinessUnit, 1 Afdeling, 2 | De økonomiske dimensionsattributter, der er defineret i segmentrækkefølgen.<p>Du kan bruge siden **Eksport** til at kontrollere, hvordan attributterne er defineret.</p> |
| 7            | 002,1,658 | <ul><li>Økonomisk dimensionsværdi</li><li>Den økonomiske dimension som det indeks, der er angivet i RecordDimensions</li><li>Et entydigt post-id, der er entydigt og tilknyttet det entydige post-id fra RecordTrans eller RecordTrans2</li></ul> |
| 8            | 002,1,1 | <ul><li>Dimensionsværdier, der er knyttet til posteringen fra RecordBudget</li><li>Den økonomiske dimension som det indeks, der er angivet i RecordDimensions</li><li>Et entydigt linjepost-id, der justeres efter rækkefølgen af posteringslinjerne i filen</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
