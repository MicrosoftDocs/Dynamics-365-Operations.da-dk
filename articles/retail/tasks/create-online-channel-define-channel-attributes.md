---
title: Opret onlinekanal og definer kanalattributter
description: Denne procedure gennemgår oprettelse af en ny onlinekanal og tilføjelse af den til organisationshierarkiet.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569515"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Opret onlinekanal og definer kanalattributter

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure gennemgår oprettelse af en ny onlinekanal og tilføjelse af den til organisationshierarkiet. Du skal oprette organisationshierarkiet, før du kan oprette en ny onlinekanal. Proceduren bruger USRT-demodatafirmaet.


## <a name="create-a-new-online-channel"></a>Opret en ny onlinekanal
1. Gå til Detail og handel > Kanaler > Onlinebutikker.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Indtast eller vælg en værdi i feltet Lagersted.
5. Vælg en indstilling i feltet Lagertidszone.
6. Indtast eller vælg en værdi i feltet Standardkunde.
7. Indtast eller vælg en værdi i feltet Kundeadressekartotek.
8. Indtast eller vælg en værdi i feltet Betalingsbetingelse.
9. Indtast eller vælg en værdi i feltet Betalingsmåde.
10. Indtast eller vælg en værdi i feltet Profil til e-mailbesked.
11. Udvid sektionen Økonomiske dimensioner.
12. Indtast eller vælg en værdi i feltet BusinessUnit.
    * På samme måde kan du angive værdien for alle andre standarddimensioner.  
13. Klik på Gem.

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Føj onlinekanalen til organisationshierarkiet
1. Luk siden.
2. Gå til Virksomhedsadministration > Organisationer > Organisationshierarkier.
3. Find og vælg den ønskede post på listen.
4. Klik på Vis.
5. Klik på Rediger.
    * Du kan vælge en hvilket som helst hierarkinode, hvor du vil indsætte den nye kanal.  
6. Klik på Indsæt.
7. Klik på Detailkanal.
8. Klik på OK.
9. Klik på Publicer for at åbne dialogboksen Fjern.
10. Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.
11. Klik på Publicer.

