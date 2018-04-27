--- 
title: "Finde forældede produktvarianter"
description: "Denne procedure viser, hvordan du finder forældede frigivne produkter eller produktvarianter, og hvordan du knytter en status for produktlivscyklus til de forældede produkter."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 3a59f988de5290d1d69d013b762f87d0cce10e39
ms.contentlocale: da-dk
ms.lasthandoff: 02/08/2018

---
# <a name="find-obsolete-product-variants"></a>Finde forældede produktvarianter 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du finder forældede frigivne produkter eller produktvarianter, og hvordan du knytter en status for produktlivscyklus til de forældede produkter. Forudsætning: Du skal definere mindst én status for produktlivscyklus, der er inaktiv for planlægning, før du kan afspille denne opgaveguide.


## <a name="run-a-simulation"></a>Køre en simulering
1. Gå til Administration af produktoplysninger > Periodiske opgaver > Skift livscyklusstatus for forældede produkter.
2. Indtast eller vælg en værdi i feltet Ny status for produktlivscyklus.
3. Vælg Ja i feltet Kør en simulering uden at opdatere produktdata.
4. Indtast et tal i feltet Udelad produkter, der er oprettet inden for det angivne antal dage.
5. Indtast et tal i feltet Udelad produkter, der er brugt i transaktioner (i antal dage).
6. Udvid posterne for at inkludere sektion.
7. Klik på Filtrér.
8. Markér den valgte række på listen.
9. Skriv en værdi i feltet Kriterier.
10. Klik på OK.
11. Klik på OK.

> [!NOTE]
> Det anbefales at køre en simulering i batch, hvis du forventer at søge i et stort antal produkter. Du skal også kontrollere, at simuleringen ikke køres under den mest aktive arbejdstid for firmaet.  

## <a name="review-the-simulation-results"></a>Gennemse simuleringsresultaterne.
1. Gå til Administration af produktoplysninger > Forespørgsler og rapporter > Vedligeholdelsesoversigt over status for produktlivscyklus.
   
> [!NOTE]
> På denne side kan du få vist resultaterne af simuleringen og vurdere, hvor mange produkter og produktvarianter der skal knyttes til en ny status for produktlivscyklus, når du kører opdateringen uden simulering.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>Kør opdateringen af livscyklusstatus for forældede produkter
1. Luk siden.
2. Gå til Administration af produktoplysninger > Periodiske opgaver > Skift livscyklusstatus for forældede produkter.
3. Udvid posterne for at inkludere sektion.

> [!NOTE]
> Bemærk, at dit seneste valg er blevet gemt.  

4. Vælg Nej i feltet Kør en simulering uden at opdatere produktdata.
5. Udvid sektionen Kør i baggrunden.

> [!NOTE]
> Afhængigt af hvor mange produkter og produktvarianter, der er berørt, kan du overveje at køre dette job i batch. Kontroller, at du ikke kører et stort opdateringsjobbet under den mest aktive arbejdstid i firmaet.  

6. Klik på OK.
7. Gå til Administration af produktoplysninger > Forespørgsler og rapporter > Vedligeholdelsesoversigt over status for produktlivscyklus.

> [!NOTE]
> Gennemse de ændrede udgivne produkter og produktvarianter.  

8. Find og vælg den ønskede post på listen.


