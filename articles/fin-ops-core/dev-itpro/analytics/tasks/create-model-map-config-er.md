---
title: Oprette modeltilknytningskonfigurationer til elektronisk rapportering
description: Du kan bruge denne procedure til at designe en ny modeltilknytningskonfiguration til elektronisk rapportering og bruge indbyggede ER-funktioner til effektive samlede beregninger.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6ba23af5f7eb517cc58994e54e918b2a305da17
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142150"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>Oprette modeltilknytningskonfigurationer til elektronisk rapportering

[!include [banner](../../includes/banner.md)]

Du kan bruge denne procedure til at designe en ny modeltilknytningskonfiguration til elektronisk rapportering og bruge indbyggede ER-funktioner til effektive samlede beregninger. I denne procedure skal du oprette en konfiguration til eksempelfirmaet Litware, Inc. 

Denne procedure er til brugere, der er tildelt rollen som Systemadministrator eller Elektronisk rapporteringsudvikler.

Disse trin kan udføres ved hjælp af ethvert datasæt. Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".  
2. Klik på Rapporteringskonfigurationer.
3. Klik på Vis filtre.
4. Angiv filterværdien "Intrastat" i feltet "Navn", og brug filteroperatoren "begynder med".
    * Anvend dette filter til at finde 'Intrastat'-datamodelkonfigurationen. Denne model findes muligvis allerede i konfigurationstræet. Hvis det er tilfældet, kan du springe over næste underordnede opgave.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Hent den Intrastat-modelkonfiguration, der leveres af Microsoft
1. Luk siden.
2. Luk siden.
3. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
4. Find og vælg den ønskede post på listen.
    * Vælg feltet Microsoft-udbyder.  
5. Klik på Lagre.
    * Klik på Lagre i feltet Microsoft-udbyder.  
6. Klik på Vis filtre.
7. Angiv filterværdien "ressourcer" i feltet "Typenavn", og brug filteroperatoren "indeholder". 
8. Klik på Åbn.
9. Vælg 'Intrastat model' i træet.
10. Klik på Importer.
11. Klik på Ja.
    * Du har importeret den ER-modelkonfiguration, der indeholder den datamodel, du vil bruge til at undersøge, hvordan du kan bruge den nye ER-funktionalitet.  
12. Luk siden.
13. Luk siden.
14. Klik på Rapporteringskonfigurationer.

## <a name="add-a-new-model-mapping-configuration"></a>Tilføj en ny modeltilknytningskonfiguration
1. Vælg 'Intrastat model' i træet.
2. Klik på Opret konfiguration for at åbne dialogboksen.
3. Skriv "Modeltilknytning baseret på datamodellen Intrastat" i feltet Ny.
4. Skriv 'Tilknytning af Intrastat-eksempel' i feltet Navn.
    * Tilknytning af Intrastat-eksempel  
5. Klik på Opret konfiguration.

