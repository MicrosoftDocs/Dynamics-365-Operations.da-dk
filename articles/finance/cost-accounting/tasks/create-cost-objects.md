---
title: Oprette omkostningsobjekter
description: Denne fremgangsmåde viser, hvordan du opretter omkostningsobjekter ved at importere den økonomiske dimension af typen Bærer til omkostningsregnskabet via en dataconnector.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734124"
---
# <a name="create-cost-objects"></a>Oprette omkostningsobjekter 

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du opretter omkostningsobjekter ved at importere den økonomiske dimension af typen Bærer til omkostningsregnskabet via en dataconnector. Demofirmaet USMF bruges til at oprette denne procedure. 


## <a name="create-new-cost-objects"></a>Opret nye omkostningsobjekter
1. Gå til **Omkostningsregnskab > Dimensioner > Dimensioner for omkostningsobjekt**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Navn**.
4. Indtast eller vælg en værdi i feltet **Dataconnector for dimensionsmedlemmer**.
5. Indtast en værdi i feltet **Beskrivelse**.
6. Klik på **Gem**.

## <a name="configure-the-data-connector"></a>Konfigurer dataconnectoren
1. Klik på **Konfigurer leverandør af dimensionsmedlem**.
    * Vælg CostCenter for at importere CostCenter-dimensionen til omkostningsregnskabet.  
2. Vælg Bærer i feltet **Dimensionens navn**.
3. Klik på **OK**.

## <a name="import-cost-centers"></a>Importér bærere
1. Klik på **Importér dimensionsmedlemmer**.
2. Klik på **OK**.

## <a name="view-the-imported-cost-centers"></a>Få vist de importerede bærere
1. Klik på **Vis dimensionsmedlemmer**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
