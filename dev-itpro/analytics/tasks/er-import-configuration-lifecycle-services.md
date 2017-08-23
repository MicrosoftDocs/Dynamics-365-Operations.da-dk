--- 
title: Importere en konfiguration fra Lifecycle Services til elektronisk rapportering (ER)
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan importere en ny version af en elektronisk rapporteringskonfiguration (ER) til Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ab453d3ee44e206aea148de8dc3b428dc5056576
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a>Importere en konfiguration fra Lifecycle Services til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan importere en ny version af en elektronisk rapporteringskonfiguration (ER) til Microsoft Lifecycle Services (LCS).

I dette eksempel skal du vælge den ønskede version af ER-konfigurationen og importere den til eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, fordi ER-konfigurationer deles af firmaer. For at fuldføre disse trin, skal du først fuldføre trinnene i proceduren "Overføre en ER-konfiguration til Lifecycle Services". Adgang til LCS er også nødvendig for at udføre disse trin.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Konfigurationer.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Slette en delt version af datamodelkonfiguration
1. Vælg 'Eksempelmodelkonfiguration' i træet.
    * Den første version af en eksempeldatamodelkonfiguration, der er oprettet og udgivet til LCS under proceduren "Overføre en ER-konfiguration til Lifecycle Services". I denne procedure vil du slette denne version af ER-konfigurationen. Denne version af en eksempeldatamodelkonfiguration importeres senere fra LCS.  
2. Find og vælg den ønskede post på listen.
    * Vælg den konfigurationsversion, der har statussen 'Delt'. Denne status angiver, at konfigurationen er blevet publiceret til LCS.  
3. Klik på Skift status.
4. Klik på Annuller.
    * Skift status for den valgte version fra 'Delt' til 'Annulleret' for at gøre den tilgængelig for sletning.  
5. Klik på OK.
6. Find og vælg den ønskede post på listen.
    * Vælg den konfigurationsversion, der har statussen 'Annulleret'.  
7. Klik på Slet.
8. Klik på Ja.
    * Bemærk, at kun kladdeversion 2 af den valgte datamodelkonfiguration er tilgængelig.  
9. Luk siden.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Importere en delt version af datamodelkonfiguration fra LCS
1. Markér den valgte række på listen.
    * Åbn listen over lagre for konfigurationsudbyderen Litware, Inc.  
2. Klik på Lagre.
3. Klik på Åbn.
    * Vælg LCS-lageret, og åbn det.  
4. Markér den valgte række på listen.
    * Vælg den første version af 'Eksempelmodelkonfiguration' på versionslisten.  
5. Klik på Importer.
6. Klik på Ja.
    * Bekræft importen af den valgte version fra LCS.  
    * Bemærk, at meddelelsen (over formen) bekræfter fuldførelsen af importen af den valgte version.  
7. Luk siden.
8. Luk siden.
9. Klik på Konfigurationer.
10. Vælg 'Eksempelmodelkonfiguration' i træet.
11. Find og vælg den ønskede post på listen.
    * Vælg den konfigurationsversion, der har statussen 'Delt'.  
    * Bemærk, at den delte version 1 af den valgte datamodelkonfiguration nu også er tilgængelig.  


