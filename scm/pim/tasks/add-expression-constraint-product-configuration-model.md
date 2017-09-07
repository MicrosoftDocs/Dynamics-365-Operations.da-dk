--- 
title: "Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel"
description: "Denne procedure viser, hvordan du kan føje et nyt begrænsningsudtryk til en produktkonfigurationsmodel."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b8286eba5c799789ebba9a501a5a0b06ccdaabb1
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan føje et nyt begrænsningsudtryk til en produktkonfigurationsmodel. Den viser, hvordan du kan bemyndige, at der skal anvendes hjørnebeskyttelse på en højttaler, hvis brugeren har valgt et frontgitter i metal. Proceduren bruger komponenten Højttaler af topkvalitet i demofirmaet USMF.


## <a name="create-an-expression-constraint"></a>Oprette en udtryksbegrænsning
1. Klik på Definition af produktvariantmodel.
2. Klik på Produktkonfigurationsmodeller.
3. Find og vælg den ønskede post på listen.
    * I dette eksempel bruges højttalermodellen af topkvalitet.  
4. Klik op linket i den valgte række på listen.
5. Udvid afsnittet Begrænsninger.
6. Klik på Tilføj.
7. Klik på Opret.
8. Skriv en værdi i feltet Navn.

## <a name="enter-expression"></a>Indtast udtryk
1. Klik på udtrykket Rediger.
    * Hvis du låser op brugergrænsefladen i opgaveregistrering på dette tidspunkt, kan du bruge IntelliSense og listen over symboler til at opbygge begrænsningsudtrykket.  
2. I feltet ConstraintBody skal du angive 'Implies[FrontGrill=="Metal", CornerProtection]'.
    * Logikken for dette udtryk siger: Hvis kølergitteret er af metal, skal hjørnebeskyttelsesindstillingen være markeret.  
3. Klik på Valider.
    * Valideringsfunktionen kører gennem begrænsningsudtrykket og kontrollerer for syntaksfejl.  
4. Klik på Luk.
5. Klik på OK.

