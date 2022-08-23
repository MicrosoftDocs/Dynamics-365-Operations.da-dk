---
title: Gøre afgrænsningstegn for kontoplaner entydigt
description: Denne artikel forklarer, hvordan du ikke kan have samme afgrænsningstegn til kontoplanen og dimensionsværdier. Du skal ændre afgrænsningstegnets værdier efter opgraderingen.
author: RyanCCarlson2
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: RCarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.openlocfilehash: 2184d26e104f803ae1bf59155cf18f560652f318
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292490"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gøre afgrænsningstegn for kontoplaner entydigt

[!include [banner](../includes/banner.md)]

Du kan bruge samme afgrænsningstegn til kontoplanen og dimensionsværdierne i Microsoft Dynamics AX 2012. I aktuelle versioner af programmer til finans og drift kan ikke du anvende det samme afgrænsningstegn til kontoplanen og dimensionsnavne- eller værdier. Hvis der er anvendes samme afgrænsningstegn, kan du ændre det efter opgraderingen. 

## <a name="update-delimiter"></a>Opdatere afgrænsningstegn
Hvis der er en konflikt med kontoplanen, kan afgrænsningstegnet for kontoplanen og formatet for projekt/underprojekt-id ændres. Ingen andre afgrænsningstegn kan ændres. 
- Du kan ændre afgrænsningstegnet for kontoplanen efter opgradering i **Finansparametre** > **Kontoplaner og dimensioner** > **Skift afgrænsningstegn**. 
- Hvis der er kun konflikten med formatet for projekt/underprojekt-id, kan du ændre værdien i **Parametre for projektstyring og regnskab** > **Generelt** > **Rediger underprojektformat**. 

### <a name="other-considerations"></a>Andre overvejelser
På samme måde som med projekt-/underprojekt-id bør andre masterdataposter, der bruges som økonomiske dimensioner, f.eks. leverandører eller kunder, ikke have værdier for konto-id'er, der bruger samme tegn som afgrænsningstegnet til kontoplanen. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Sådan afgør du, om dit miljø kræver opdaterede afgrænsningstegn 
Hvis afgrænsningstegnene i det opgraderede miljø er i konflikt, kan systemet blive ustabilt ved indtastning af værdier ved segmenteret postkontrol eller dimensionspostkontrol. Det betyder, at du skal altid bruge opslag eller en pop op-menu ved indtastning af kombinationer af konti og dimensioner.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

