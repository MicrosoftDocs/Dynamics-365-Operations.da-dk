---
title: Designe konfigurationer til at generere dokumenter, der har programdata
description: Denne artikel forklarer, hvordan du designer konfigurationer af elektronisk rapportering (ER) for at generere et elektronisk dokument. (Del 1 – Importere konfigurationer).
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8494f54c6f84e63e75469aa9d80d090c050b0f7f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290538"
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
