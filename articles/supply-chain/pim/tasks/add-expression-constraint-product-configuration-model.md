---
title: Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel
description: Denne procedure viser, hvordan du kan føje et nyt begrænsningsudtryk til en produktkonfigurationsmodel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920875"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du kan føje et nyt begrænsningsudtryk til en produktkonfigurationsmodel. Den viser, hvordan du kan bemyndige, at der skal anvendes hjørnebeskyttelse på en højttaler, hvis brugeren har valgt et frontgitter i metal. Proceduren bruger komponenten Højttaler af topkvalitet i demofirmaet USMF.

## <a name="create-an-expression-constraint"></a>Oprette en udtryksbegrænsning

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.
3. Find og vælg den ønskede post på listen.
    * I dette eksempel bruges højttalermodellen af topkvalitet.  
4. Vælg linket i den valgte række på listen.
5. Udvid sektionen **Begrænsninger**.
6. Vælg **Tilføj**.
7. Vælg **Opret**.
8. Skriv en værdi i feltet **Navn**.

## <a name="enter-expression"></a>Indtast udtryk

1. Vælg **Rediger udtryk**.
    * Hvis du låser op brugergrænsefladen i opgaveregistrering på dette tidspunkt, kan du bruge IntelliSense og listen over symboler til at opbygge begrænsningsudtrykket.  
2. I feltet **ConstraintBody** skal du indtaste 'Implies[FrontGrill=="Metal", CornerProtection]'.
    * Logikken for dette udtryk siger: Hvis kølergitteret er af metal, skal hjørnebeskyttelsesindstillingen være markeret.  
3. Vælg **Valider**.
    * Valideringsfunktionen kører gennem begrænsningsudtrykket og kontrollerer for syntaksfejl.  
4. Vælg **Luk**.
5. Vælg **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]