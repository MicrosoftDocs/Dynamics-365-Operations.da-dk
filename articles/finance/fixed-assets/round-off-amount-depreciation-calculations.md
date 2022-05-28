---
title: Afrunde beløb til afskrivningsberegninger
description: I dette emne beskrives det Afrund afskrivning-felt, der findes på sider med opsætning af en bog.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: kfend
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98d6a21bea4688d6f258a98eab174485ceee2cfc
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726719"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Afrunde beløb til afskrivningsberegninger

[!include [banner](../includes/banner.md)]

I dette emne beskrives det **Afrund afskrivning**-felt, der findes på sider med **opsætning af en bog**.

Afrunding af afskrivningsbeløb angives for hver bog. Afrunding af afskrivningsbeløb bruges i anlægsaktivets afskrivningsprofil, der viser den fremtidige afskrivning og værdi af anlægsaktivet samt i afskrivningsforslagene. Angiv laveste afskrivningsbeløb, der er tilladt i denne bog. 

Afskrivningsbeløbet i den sidste afskrivningsperiode afrundes ikke, uanset den afrunding der er konfigureret. I slutningen af den sidste afskrivningsperiode skal værdien af anlægsaktivet være 0 (nul) eller scrapværdien, hvis der anvendes scrapværdi.

### <a name="example"></a>Eksempel

Afskrivning uden afrunding er beregnet til 2.444,44. Som følgende tabel viser afhænger det foreslåede beløb af, hvordan afrundingen konfigureres.

| Afrundingsmetode | Afskrivningsbeløb |
|-----------------|---------------------|
| Afrunding 0,1    | 2.444,40            |
| Afrunding 1,00   | 2.444,00            |
| Afrunding 10,00  | 2.440,00            |
| Afrunding 100,00 | 2.400,00            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
