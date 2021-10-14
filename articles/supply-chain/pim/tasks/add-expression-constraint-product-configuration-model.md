---
title: Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel
description: Denne procedure viser, hvordan du kan føje et nyt begrænsningsudtryk til en produktkonfigurationsmodel.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77e8b991a2615a8f5d238acc4655f231edb6ca98
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569643"
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