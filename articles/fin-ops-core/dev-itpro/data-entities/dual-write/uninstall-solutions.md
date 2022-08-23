---
title: Fjerne orkestreringsløsninger til dobbeltskrivningsapplikation
description: Denne artikel indeholder en beskrivelse af, hvordan du kan afinstallere løsninger til orkestrering af dobbeltskrivningsprogrammer.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: fd9dc98ec1323a2ef262a330a400a6bd3833e554
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288724"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Fjerne orkestreringsløsninger til dobbeltskrivningsapplikation

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en beskrivelse af, hvordan du kan afinstallere løsninger til orkestrering af dobbeltskrivningsprogrammer.

Nogle kunder installerer ved en fejl den orkestreringspakke for dobbeltskrivningsprogram, der installerer flere løsninger i deres Microsoft Dataverse-miljø. Installationen af de ekstraordinære løsninger i pakken kan forårsage uventede og uønskede problemer.

Hvis du vil løse problemer, der er relateret til installationen af orkestreringspakken til dobbeltskrivningsprogram, skal du afinstallere de uønskede dobbeltskrivningsløsninger i følgende rækkefølge:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (hvis den findes)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (hvis du vil afinstallere denne løsning, skal du åbne en supportanmodning hos Microsoft).
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Hvis løsningerne til part- og globalt adressekartotek er installeret, skal du afinstallere løsningerne i følgende rækkefølge:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. Part
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
