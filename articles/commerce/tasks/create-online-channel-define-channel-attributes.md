---
title: Opret onlinekanal og definer kanalattributter
description: Denne procedure gennemgår oprettelse af en ny onlinekanal og tilføjelse af den til organisationshierarkiet.
author: jashanno
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e28e717dcf594c5079b4b6987331115356b6bdbc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798507"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Opret onlinekanal og definer kanalattributter

[!include [banner](../includes/banner.md)]

Denne procedure gennemgår oprettelse af en ny onlinekanal og tilføjelse af den til organisationshierarkiet. Du skal oprette organisationshierarkiet, før du kan oprette en ny onlinekanal. Proceduren bruger USRT-demodatafirmaet.


## <a name="create-a-new-online-channel"></a>Opret en ny onlinekanal
1. Gå til Retail og Commerce > Kanaler > Onlinebutikker.
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
7. Klik på Commerce-kanal.
8. Klik på OK.
9. Klik på Publicer for at åbne dialogboksen Fjern.
10. Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.
11. Klik på Publicer.

## <a name="configure-orders-for-near-real-time-notification"></a>Konfigurere ordrer for næsten i realtids-påmindelse
1. Gå til Retail og Commerce > Konfiguration af hovedkontor > Parametre > Commerce-parametre.
2. Vælg "Ja" i Brug realtidstjeneste til oprettelse af eCommerce-ordre.
3. Kør distributionsplanen 1070 for at synkronisere ændringerne til kanaldatabasen. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]