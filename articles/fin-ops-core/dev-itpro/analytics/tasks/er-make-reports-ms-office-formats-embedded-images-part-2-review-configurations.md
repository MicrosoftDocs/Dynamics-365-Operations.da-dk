---
title: Gennemgå konfigurationer til at generere rapporter i Office-format, der har integrerede billeder
description: I dette emne forklares det, hvordan du designer konfigurationer af rapportering for at generere elektroniske dokumenter med integrerede billeder. (Del 1 – Konfigurere parametre).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: 3eee6300350dd96c34f2eab44704d1895e6171ff
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093639"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Gennemgå konfigurationer til at generere rapporter i Office-format, der har integrerede billeder

[!include [banner](../../includes/banner.md)]

For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden "ER Oprette rapporter i Microsoft Office-formater med integrerede billeder (Del 1: Konfigurere parametre)".

Denne procedure viser, hvordan du designer elektroniske rapporteringskonfigurationer (ER) for at generere elektroniske dokumenter, der indeholder integrerede billeder i Microsoft Excel og Microsoft Word. I dette eksempel skal du gennemse ER-konfigurationer for eksempelfirmaet Litware Inc. 

Denne procedure er beregnet til brugere, der har fået tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Trinnene kan udføres ved hjælp af USMF datasættet.


## <a name="review-the-imported-data-model"></a>Gennemse den importerede datamodel
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Vælg 'Model for checks' i træet.
3. Klik på Designer.
    * Denne model er udviklet til at repræsentere betalingschecks fra en forretningsmæssig betragtning og tilknytningen af denne model til programmets datakilder. Gennemse denne model ved hjælp af ER Operations-designeren. Bemærk, at attributterne for de modelelementer, der præsenteres: struktur, navn, beskrivelse, datatype og så videre.   
4. Udvid 'root' i træet.
5. Vælg 'rod\checks' i træet.
6. Udvid 'rod\checks' i træet.
7. Udvid 'rod\checks\attributter' i træet.
8. Udvid 'rod\indbetaler' i træet.
9. Vælg 'rod\istestrun' i træet.
10. Vælg 'rod\layout' i træet.
    * Layoutelementet for denne model repræsenterer detaljerede oplysninger om udskrivning af checkformularlayoutet for den valgte bankkonto. Den indeholder også to noder af datatypen Container til lagring af billeder.   
11. Udvid 'rod\layout' i træet.
12. Vælg 'rod\layout\firmalogo' i træet.
13. Vælg 'rod\layout\firmalogo' i træet.
14. Vælg 'rod\layout\firmalogo\billede' i træet.
15. Vælg 'rod\layout\firmalogo\isprinted' i træet.
16. Vælg 'rod\layout\signatur' i træet.
17. Udvid 'rod\layout\signatur' i træet.
18. Vælg 'rod\layout\signatur\billede' i træet.
19. Vælg 'rod\layout\signatur\isprinted' i træet.
    * Bemærk, at de to billeddatamodelelementer er bundet til felterne i de tabeller, der indeholder billeder af firmaets logo og den autoriserede persons signatur i binært format.  
20. Udvid 'rod\layout\vandmærke' i træet.
21. Klik på Tilknyt model til datakilde.
22. Klik på Designer.
23. Udvid 'chequesselected' i træet.
24. Udvid 'layout' i træet.
25. Vælg 'layout\firmalogo' i træet.
26. Udvid 'layout\signatur' i træet.
27. Udvid 'layout\vandmærke' i træet.
28. Slå "Vis detaljer" til.
    * Bemærk, at checkdatamodelelementet er bundet til tabellen TmpChequePrintout, der på kørselstidspunktet indeholder poster for checks, som brugeren har valgt til udskrivning.   
29. Luk siden.
30. Luk siden.
31. Luk siden.

## <a name="review-the-imported-format"></a>Gennemse det importerede format
1. Udvid 'Model for checks' i træet.
2. Vælg 'Model for checks\Checkudskrivningsformat' i træet.
3. Klik på Designer.
4. Klik på Vedhæftede filer.
5. Klik på Åbn.
    * Åbn den vedhæftede rapports skabelon i Excel.  
    * Gennemse den vedhæftede rapports Excel-skabelon, der skal bruges til at udskrive checks. Skabelonen indeholder to checks pr. side og er designet til at udskrive checks til den fortrykte formular. Bemærk, at to tomme billeder er integreret. Disse tomme billeder er beregnet til firmalogoet og signaturen fra den person, der godkender en betaling. Kontroller, at billederne hedder henholdsvis CompLogo og SignatureImage i Excel.   
6. Luk siden.
7. Udvid 'Rapport' i træet.
8. Udvid 'Rapport\ChequeLines' i træet.
9. Vælg 'Rapport\ChequeLines\CompLogo' i træet.
10. Slå "Vis detaljer" til.
    * Bemærk, at celleelementet for formatet 'CompLogo' repræsenterer det Excel-element, der bruges til at udfylde feltet med firmalogobilledet i rapporten. Dette formatelement er bundet til det billeddatamodelelement, der på kørselstidspunktet indeholder et billede af firmalogoet i binært format.   
11. Klik på fanen Tilknytning.
12. Klik på Rediger aktiveret.
    * Bemærk, at du kan ændre celleelementet for formatet 'CompLogo', så det ikke længere er aktiveret. I så fald skjuler det tilknyttede Excel-billedelement et firmalogo i den genererede rapport. Hvis det aktiverede udtryk returnerer TRUE, og den definerede binding ikke viser et billede, viser det tilknyttede Excel-billedelement et billede, der er gemt i Excel-skabelonen.   
13. Luk siden.
14. Udvid 'labels: Container' i træet.
    * Nogle etiketter, der vises i den fortrykte checkformular, medtages i rapporten, når den oprettes til testformål. Disse etiketter udskrives dog ikke under den egentlige udskrivning, fordi den fortrykte formular allerede indeholder dem.  
15. Luk siden.

