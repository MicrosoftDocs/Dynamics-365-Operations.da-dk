---
title: Gøre afgrænsningstegn for kontoplaner entydigt
description: I dette emne forklares det, hvordan du ikke kan have samme afgrænsningstegn til kontoplanen og dimensionsværdier. Du skal ændre afgrænsningstegnets værdier efter opgraderingen.
author: panolte
ms.date: 03/30/2018
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
ms.openlocfilehash: f4f89772dedb5433c3da3f0f7bf02106641f59a8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748101"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gøre afgrænsningstegn for kontoplaner entydigt

[!include [banner](../includes/banner.md)]

Du kan bruge samme afgrænsningstegn til kontoplanen og dimensionsværdierne i Microsoft Dynamics AX 2012. I aktuelle versioner af Finance and Operations kan ikke du anvende det samme afgrænsningstegn til kontoplanen og dimensionsværdierne. Hvis der er anvendes samme afgrænsningstegn, kan du ændre det efter opgraderingen. 

Denne funktion er tilgængelig i følgende versioner:
- Finance and Operations-version 8.0
- Finance and Operations version 7.1, KB 4094701 kan ikke få adgang til de økonomiske dimensioner, når dimensionsværdierne indeholder afgrænsningstegnet for kontoplan
- Finance and Operations version 7.2, KB 4092967 kan ikke vælge underprojekt som en dimension, når formatet for underprojekt indeholder afgrænsningstegnet for dimensioner

## <a name="update-delimiter"></a>Opdatere afgrænsningstegn
Hvis der er en konflikt med kontoplanen, kan afgrænsningstegnet for kontoplanen og formatet for projekt/underprojekt-id ændres. Ingen andre afgrænsningstegn kan ændres. 
- Du kan ændre afgrænsningstegnet for kontoplanen efter opgradering i **Finansparametre** > **Kontoplaner og dimensioner** > **Skift afgrænsningstegn**. 
- Hvis der er kun konflikten med formatet for projekt/underprojekt-id, kan du ændre værdien i **Parametre for projektstyring og regnskab** > **Generelt** > **Rediger underprojektformat**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Sådan afgør du, om dit miljø kræver opdaterede afgrænsningstegn 
Hvis afgrænsningstegnene i det opgraderede miljø er i konflikt, kan systemet blive ustabilt ved indtastning af værdier ved segmenteret postkontrol eller dimensionspostkontrol. Det betyder, at du skal altid bruge opslag eller en pop op-menu ved indtastning af kombinationer af konti og dimensioner.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]