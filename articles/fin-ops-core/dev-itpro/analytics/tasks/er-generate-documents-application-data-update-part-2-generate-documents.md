---
title: Designe konfigurationer til at generere dokumenter, der har programdata
description: I dette emne forklares det, hvordan du designer konfigurationer af elektronisk rapportering (ER) for at generere et elektronisk dokument. (Del 1 – Importere konfigurationer).
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: 217eca9bd1502d4327857720fb2d32a3ec3508ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563168"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Designe konfigurationer til at generere dokumenter, der har programdata

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]