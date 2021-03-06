---
title: Generere dokumenter, der har programdata
description: For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Generere dokumenter med opdatering til programdata (Del 4 - Redigere format)".
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2591f5b32417dd7517f76fc237d2337af64b3f61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745029"
---
# <a name="generate-documents-that-have-application-data"></a>Generere dokumenter, der har programdata

[!include [banner](../../includes/banner.md)]

For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Generere dokumenter med opdatering til programdata (Del 4: Redigere format)".



I denne procedure forklares det, hvordan du designer elektroniske rapportering (ER) konfigurationer for at generere et elektronisk dokument og opdatere programdata. Du kan udføre ER-formatkonfigurationen for at generere Intrastat-rapporten og opdatere programdata for at arkivere oplysninger om rapporteringsprocessen i denne procedure.



Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Disse trin kan udføres ved hjælp af DEMF-datasættet. Før du begynder, skal du sørge for, at landekonteksten for DEMF-firmaet er BEL (Belgien).


## <a name="set-up-foreign-trade-parameters"></a>Konfigurer udenrigshandelsparametre
1. Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre.
2. Klik på fanen Nummerserier.

    For at arkivere oplysninger om Intrastat-rapporteringsproces skal vi kunne identificere poster for hvert arkiv, vi har oprettet. I den forbindelse skal der konfigureres en særlig nummerserie.  

3. Vælg referencen, der er 'Id for Intrastat-arkiv'.
4. Skriv en værdi i feltet Nummerseriekode.

    Skriv eller vælg værdien 'Fore_2' i feltet 'Nummerseriekode'.  

5. Nummerseriekoden ResolveChanges.
6. Klik på Gem.
7. Luk siden.

## <a name="run-modified-er-format"></a>Kør ændret ER format
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Udvid 'Intrastat (model)' i træet.
3. Vælg 'Intrastat (model)\Intrastat (format)' i træet.
4. Klik på Kør.
5. Skriv 'intrastat2.xml' i feltet Angiv filnavn.
6. Klik på OK.

## <a name="review-er-format-executions-results"></a>Gennemse resultaterne af udførelse af ER-format
Gennemse den genererede XML-fil.  
1. Luk siden.
2. Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.

    Åbn denne formular, der indeholder Intrastat-posteringer, der er medtaget i det genererede elektroniske dokument.  

3. Klik på Intrastat-arkiv.

    Da det udførte ER-format nu indeholder indstillinger for opdatering af programdata, er detaljerne for den fuldførte Intrastat-rapportering blevet arkiveret. I denne formular kan du se overskriftsposten for det oprettede arkiv.  

4. Klik på Detaljer.

    I denne formular kan du se oplysninger om det oprettede arkiv.  

5. Luk siden.
6. Luk siden.
7. Luk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]