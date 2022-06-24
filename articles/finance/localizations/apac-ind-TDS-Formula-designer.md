---
title: Formeldesigner til skatteberegninger
description: Denne artikel viser et eksempel på, hvordan kildeskat (TDS – Tax Deducted at Source) beregnes på basis af den formel, der er defineret for hver kildeskattekode i kildeskattegruppen, der er tilknyttet transaktionen.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1196f7258c898a55f3f29ddce7457e6f527185d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889855"
---
# <a name="formula-designer-for-tds-calculations"></a>Formeldesigner til skatteberegninger

[!include [banner](../includes/banner.md)]

Denne artikel viser et eksempel på, hvordan kildeskat (TDS – Tax Deducted at Source) beregnes på basis af den formel, der er defineret for hver kildeskattekode. Kildeskattekoder defineres i den kildeskattegruppe, der er tilknyttet transaktionen. Før du designer skatteformler, skal du fuldføre den grundlæggende opsætning, der kræves for kildeskat, som angivet i følgende fremgangsmåde. 

- Konfigurer grupper af skattekomponenter ved hjælp af siden **Komponentgrupper for A-skat**. 
- Konfigurer skattekomponenter, og knyt skattekomponentgruppen til skattekomponenterne ved hjælp af siden **Komponenter for A-skat**. 
- Konfigurer skattekoder, og knyt skattekomponenter til skattekoderne ved hjælp af siden **Koder for A-skat**. 
- Konfigurer kildeskattegrupper ved hjælp af siden **Grupper for A-skat**. Knyt derefter kildeskattekoderne til kildeskattegruppen, og definer formlen ved hjælp af siden **Formeldesigner**. 

**Elsempelformel**

I dette eksempel er kildeskattegruppen Leje knyttet til en indkøbsfaktura, der er oprettet for kreditor A. Fakturabeløbet er $100.000. I følgende tabel kan du se skatteberegningen for fakturaen.

| Skattegruppe                                                   | Kildeskattekoder, der er tilknyttet kildeskattegruppen | Værdi              | Skattegrundlag (Formeldesigner) | Beregningsudtryk (Formeldesigner) | Grundbeløb | Beregnet skattebeløb |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Leje                                                         | Kildeskat (kildeskattekomponent-kildeskat)                | 10 %                | Bruttobeløb                      |                                            | 100,000      | 10,000                 |
| Tillægsafgift (skattekomponent-tillægsafgift)                         | 10 %                                     | Uden bruttobeløb | +Kildeskat                              |                   10000                    | 1.000        |                       |
| PE-Cess (kildeskattekomponent-PE-Cess)                            | 2 %                                      | Uden bruttobeløb | +Kildeskat+Tillægsafgift                    |                   11000                    | 220         |                       |
| SHE Cess (skattekomponent-SHE Cess)                          | 1 %                                      | Uden bruttobeløb | +Kildeskat+Tillægsafgift                    |                   11000                    | 110         |                       |
| **Kildeskat** **i** **alt** **beregnet** **for** **fakturaen** | **11,330**                               |                    |                                   |                                            |             |                       |

Bilagsposterne oprettes på følgende måde.

| Konto           | Debet  | Kredit |
| ----------------- | ------ | ------ |
| Leje              | 100,000 |        |
| Kreditor A          |        | 100,000 |
| Kreditor A          | 11,330  |        |
| Skyldig kildeskat       |        | 10,000  |
| Skyldig tllægsafgift |        | 1.000   |
| Skyldig PE-Cess   |        | 220    |
| Skyldig SHE-Cess  |        | 110    |
