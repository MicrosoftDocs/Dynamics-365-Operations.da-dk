---
title: Importere ER-konfiguration fra Lifecycle Services
description: Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan importere en ny version af en elektronisk rapporteringskonfiguration (ER) til Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 036d7e7e3f79e0945d6fef866a30edd41e688c07
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "337250"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a>Importere ER-konfiguration fra Lifecycle Services

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

