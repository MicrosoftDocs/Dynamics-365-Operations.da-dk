--- 
title: Designe konfigurationer for at generere dokumenter med programdata
description: "For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Generere dokumenter med opdatering til programdata (Del 1 - Importere konfigurationer)."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ad5508ea5807f505b29f2e60a1459c9c22552694
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="design-configurations-to-generate-documents-with-application-data"></a>Designe konfigurationer for at generere dokumenter med programdata

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Generere dokumenter med opdatering til programdata (Del 1: Importere konfigurationer).



I denne procedure forklares det, hvordan du designer elektroniske rapportering (ER) konfigurationer for at generere et elektronisk dokument. I denne procedure skal du køre den ER-importerede formatkonfiguration, der er oprettet for eksempelfirmaet, Litware Inc., for at generere elektroniske dokumenter.



Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Disse trin kan udføres ved hjælp af DEMF-datasættet. 



Før du begynder, skal du ændre landekonteksten for DEMF firmaet fra DEU (Tyskland) til BEL (Belgien). Klik på Virksomhedsadministration > Organisationer > Juridiske enheder for at opdatere landekoden i den primære adresse for den juridiske enhed DEMF. Genstart programmet.


## <a name="run-imported-er-format"></a>Kør det importerede ER format
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Udvid 'Intrastat (model)' i træet.
3. Vælg 'Intrastat (model)\Intrastat (format)' i træet.
4. Klik på Kør.
    * Kør kladdeversionen af ER-formatkonfigurationen for at generere Intrastat-rapporten.  
5. Skriv 'intrastat.xml' i feltet Angiv filnavn.
    * Angiv navnet på filen.  
6. Klik på OK.
    * Gennemse den genererede XML-fil.  
7. Luk siden.
8. Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.
    * Åbn denne formular for at få vist Intrastat-posteringer, der er medtaget i det genererede elektroniske dokument.  
9. Klik på Intrastat-arkiv.
    * Da det udførte ER-format ikke indeholder nogen indstillinger for opdatering af programdata, er detaljerne for den fuldførte Intrastat-rapport ikke blevet arkiveret.  
10. Luk siden.
11. Luk siden.


