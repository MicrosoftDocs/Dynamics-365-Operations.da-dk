---
title: Importere konfigurationer til at generere dokumenter, der har programdata
description: For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Oprette en konfigurationsudbyder og markere den som aktiv".
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f919d953c3aa0c8d16366167a12e52d35f32cdf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684613"
---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>Importere konfigurationer til at generere dokumenter, der har programdata

[!include [banner](../../includes/banner.md)]

For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Oprette en konfigurationsudbyder og markere den som aktiv".

I denne procedure forklares det, hvordan du designer elektroniske rapportering (ER) konfigurationer for at generere et elektronisk dokument. I denne procedure skal du importere de nødvendige ER-konfigurationer, der er oprettet til eksempelfirmaet Litware, Inc., og bruge dem til at generere elektroniske dokumenter. Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Disse trin kan udføres ved hjælp af DEMF-datasættet. Før du går i gang, skal du hente og gemme filerne i Hjælp-emnet "Generere elektroniske dokumenter og opdatere programdata ved hjælp af værktøjet Elektronisk rapportering" (generate-electronic-documents-update-application-data/). Filerne er Intrastat (model).xml, Intrastat (tilknytning).xml og Intrastat (format).xml.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren Opret en konfigurationsudbyder, og markér den som aktiv.  
    * Denne procedure viser, hvordan du bruger ER-funktioner til at fuldføre en opdatering af programdata, og hvordan du kan generere en Intrastat-rapport. Oplysningerne om rapporteringsprocessen arkiveres i tabellerne i programmet. I øjeblikket, når Intrastat-rapporteringsprocessen aktiveres fra Intrastat-formularen, foretages arkiveringen ud fra den logik, der er programmeret i den eksisterende kildekode. I denne procedure skal du konfigurere en lignende, men forenklet logik for programdata udelukkende ved hjælp af ER-strukturen. Der foretages ingen ændringer af kildekoden.   

## <a name="import-er-configurations"></a>Importér ER-konfigurationer
1. Klik på Rapporteringskonfigurationer.
2. Klik på Udveksling.
3. Klik på Indlæs fra XML-fil.
    * Importer den ER-modelkonfiguration, der indeholder den datamodel, der skal bruges som datakilde ved oprettelse af Intrastat-rapporten. Senere skal du udvide denne datamodeldefinition for at bruge den til en opdatering af programdata for at arkivere oplysninger fra Intrastat-rapporteringsprocessen.   
    * Klik på Gennemse, og vælg Intrastat (model) .XML-filen.  
4. Klik på OK.
5. Vælg 'Intrastat (model)' i træet.
6. Klik på Designer.
7. Udvid 'For udgående dokument' i træet.
8. Udvid 'For udgående dokument\Transaktioner' i træet.
    * Gennemse strukturen af den importerede datamodel. Bemærk, at rodelementet 'For udgående dokument' er defineret til at angive dataflowet til hentning af data fra programmet og bruge det som datakilde ved generering af Intrastat-rapporten. 'Transaktioner (liste over poster)' bruges til at repræsentere listen over Intrastat-transaktioner, der skal rapporteres. Da du skal arkivere rapporterede varekoder, bruges det entydige id for en enkelt varekode 'Varepost-id (Int64)' i dette dataflow.   
9. Luk siden.
10. Klik på Udveksling.
11. Klik på Indlæs fra XML-fil.
    * Importer den ER-tilknytningskonfiguration, der angiver dataflowet ved hentning af data fra programmet og derefter bruge dem til at generere Intrastat-rapporten. Senere skal du udvide denne modeltilknytningsdefinition for at hente data fra Intrastat-rapporten og bruge dem til en opdatering af programdataene for at arkivere oplysninger fra Intrastat-rapporteringsprocessen.   
    * Klik på Gennemse, og vælg Intrastat (tilknytning) .XML-filen.  
12. Klik på OK.
13. Udvid 'Intrastat (model)' i træet.
14. Vælg 'Intrastat (model)\Intrastat (tilknytning)' i træet.
15. Klik på Designer.
    * Bemærk, at den aktuelle modeltilknytning indeholder værdien 'Til model' i feltet Retning. Det betyder, at denne modeltilknytning er udviklet til at hente data fra programmet og gemme dem i datamodellen.  
16. Klik på Designer.
17. Udvid 'Liste' i træet.
18. Udvid "Transaktioner= Liste" i træet.
    * Gennemse strukturen af den model-tilknytning, der bruger den datamodel, der filtreres baseret på rodelementet 'For udgående dokument'. Bemærk, at den tilføjede datakilde 'Liste' giver adgang til de nødvendige programdata, som er listen over poster fra Intrastat-tabellen.  
19. Luk siden.
20. Luk siden.
21. Klik på Udveksling.
22. Klik på Indlæs fra XML-fil.
    * Importer den ER formatkonfiguration, der angiver layoutet for Intrastat-rapporten og processen med at angive data i rapporten. Senere skal du udvide denne formatdefinition for at angive data fra Intrastat-rapporten i datamodellen og derefter bruge dem til at opdatere programdataene for at arkivere oplysningerne fra Intrastat-rapporteringsprocessen.   
    * Klik på Gennemse, og vælg Intrastat (format) .XML-filen.  
23. Klik på OK.
24. Vælg 'Intrastat (model)\Intrastat (format)' i træet.
25. Klik på Designer.
26. Klik på Udvid/skjul.
27. Vælg 'Fil\Rapport' i træet.
28. Klik på fanen Tilknytning.
29. Vælg 'Fil' i træet.
    * Gennemse strukturen af det format, der bruges til at generere Intrastat-rapporten. Bemærk, at det er udviklet til at oprette en XML-fil ved at udfylde data fra den datamodel, der er baseret på rodelementet 'For udgående dokument'. Kontroller, at navnet på den genererede fil er defineret i brugerdialogboksformularen ('fn'-datakilden bruges til det).   
30. Luk siden.

