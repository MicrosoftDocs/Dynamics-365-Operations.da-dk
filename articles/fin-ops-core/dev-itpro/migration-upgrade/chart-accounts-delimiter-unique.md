---
title: Gøre afgrænsningstegn for kontoplaner entydigt
description: I dette emne forklares det, hvordan du ikke kan have samme afgrænsningstegn til kontoplanen og dimensionsværdier. Du skal ændre afgrænsningstegnets værdier efter opgraderingen.
author: panolte
ms.date: 03/23/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 433e9f8a7b0a9f476c74096a4bd7fef03c87dee1
ms.sourcegitcommit: 0d5ee97670bdeb1986aaea880f32962b5e374751
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468042"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gøre afgrænsningstegn for kontoplaner entydigt

[!include [banner](../includes/banner.md)]

Du kan bruge samme afgrænsningstegn til kontoplanen og dimensionsværdierne i Microsoft Dynamics AX 2012. I aktuelle versioner af Finance and Operations kan ikke du anvende det samme afgrænsningstegn til kontoplanen og dimensionsværdierne. Hvis der er anvendes samme afgrænsningstegn, kan du ændre det efter opgraderingen. 

## <a name="update-delimiter"></a>Opdatere afgrænsningstegn
Hvis der er en konflikt med kontoplanen, kan afgrænsningstegnet for kontoplanen og formatet for projekt/underprojekt-id ændres. Ingen andre afgrænsningstegn kan ændres. 
- Du kan ændre afgrænsningstegnet for kontoplanen efter opgradering i **Finansparametre** > **Kontoplaner og dimensioner** > **Skift afgrænsningstegn**. 
- Hvis der er kun konflikten med formatet for projekt/underprojekt-id, kan du ændre værdien i **Parametre for projektstyring og regnskab** > **Generelt** > **Rediger underprojektformat**. 

### <a name="other-considerations"></a>Andre overvejelser
På samme måde som med projekt-/underprojekt-id bør andre masterdataposter, der bruges som økonomiske dimensioner, f.eks. leverandører eller kunder, ikke have værdier for konto-id'er, der bruger samme tegn som afgrænsningstegnet til kontoplanen. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Sådan afgør du, om dit miljø kræver opdaterede afgrænsningstegn 
Hvis afgrænsningstegnene i det opgraderede miljø er i konflikt, kan systemet blive ustabilt ved indtastning af værdier ved segmenteret postkontrol eller dimensionspostkontrol. Det betyder, at du skal altid bruge opslag eller en pop op-menu ved indtastning af kombinationer af konti og dimensioner.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
