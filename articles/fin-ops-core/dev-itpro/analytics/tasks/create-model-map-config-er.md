---
title: Oprette modeltilknytningskonfigurationer til elektronisk rapportering
description: Du kan bruge denne procedure til at designe en ny modeltilknytningskonfiguration til elektronisk rapportering og bruge indbyggede ER-funktioner til effektive samlede beregninger.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c52f5d23f6c1cdad346a8a5e94535a4cba19057
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562874"
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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]