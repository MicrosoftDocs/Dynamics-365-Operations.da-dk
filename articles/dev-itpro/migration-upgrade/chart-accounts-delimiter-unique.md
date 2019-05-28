---
title: Gøre afgrænsningstegn for kontoplaner entydigt
description: I Dynamics 365 for Finance and Operations kan du ikke have samme afgrænsningstegn til kontoplanen og dimensionsværdier. Du skal ændre afgrænsningstegnets værdier efter opgraderingen.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559522"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gøre afgrænsningstegn for kontoplaner entydigt

[!include [banner](../includes/banner.md)]

Du kan bruge samme afgrænsningstegn til kontoplanen og dimensionsværdierne i Microsoft Dynamics AX 2012. I Dynamics 365 for Finance and Operations kan du ikke have samme afgrænsningstegn til kontoplanen og dimensionsværdier. Hvis der er anvendes samme afgrænsningstegn, kan du ændre det efter opgraderingen. 

Denne funktion er tilgængelig i:
- Dynamics 365 for Finance and Operations-version 8.0
- Dynamics 365 for Finance and Operations version 7.1, KB 4094701 kan ikke få adgang til de økonomiske dimensioner, når dimensionsværdierne indeholder afgrænsningstegnet for kontoplan
- Dynamics 365 for Finance and Operations version 7.2, KB 4092967 kan ikke vælge underprojekt som en dimension, når formatet for underprojekt indeholder afgrænsningstegnet for dimensioner

## <a name="update-delimiter"></a>Opdatere afgrænsningstegn
Hvis der er en konflikt med kontoplanen, kan afgrænsningstegnet for kontoplanen og formatet for projekt/underprojekt-id ændres. Ingen andre afgrænsningstegn kan ændres. 
- Du kan ændre afgrænsningstegnet for kontoplanen efter opgradering til Finance and Operations i **Finansparametre** > **Kontoplaner og dimensioner** > **Skift afgrænsningstegn**. 
- Hvis der er kun konflikten med formatet for projekt/underprojekt-id, kan du ændre værdien i **Parametre for projektstyring og regnskab** > **Generelt** > **Rediger underprojektformat**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Sådan afgør du, om dit miljø kræver opdaterede afgrænsningstegn 
Hvis afgrænsningstegnene i det opgraderede miljø er i konflikt, kan systemet blive ustabilt ved indtastning af værdier ved segmenteret postkontrol eller dimensionspostkontrol. Det betyder, at du skal altid bruge opslag eller en pop op-menu ved indtastning af kombinationer af konti og dimensioner.
