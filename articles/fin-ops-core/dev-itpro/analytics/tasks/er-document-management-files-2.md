---
title: 'ER Brug dokumentstyringsfiler i formatoutput (del 2: Udvidet datamodel)'
description: Dette emne beskriver, hvordan du konfigurerer et ER-format (elektronisk rapportering) til at bruge dokumentstyringsfiler (vedhæftede filer) i ER-output. (Del 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b47c35790ce04a494b6c58f6e04fa9b829d2ab93
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559767"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>ER Brug dokumentstyringsfiler i formatoutput (del 2: Udvidet datamodel)

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER. Disse trin kan udføres i en hvilken som helst virksomhed.

For at fuldføre disse trin skal du først udføre trinnene i opgaveguiden "ER Brug filer fra Dokumentstyring i formatoutput (del 1: Forbered datamodel)".

Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Udvid datamodellen for at vise filerne fra Dokumentstyring i den
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Rapporteringskonfigurationer.
3. Udvid 'Debitorfakturamodel' i træet.
4. Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.
5. Klik på Designer.
6. Vælg 'Debitorfakturamodel(InvoiceCustomer)' i træet.
    * Vi vil udvide denne datamodel for at se eventuelle filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.  
7. Klik på Ny for at åbne dialogboksen Fjern.
8. Skriv 'Vedhæftede filer i fakturaer' i feltet Navn.
    * Vedhæftede filer i fakturaer  
9. Vælg "Liste over poster" i feltet Varetype.
10. Klik på Tilføj.
11. Klik på Ny for at åbne dialogboksen Fjern.
12. Skriv 'Filindhold' i feltet Navn.
    * Filindhold  
13. Vælg "Container" i feltet Varetype.
14. Klik på Tilføj.
15. Klik på Ny for at åbne dialogboksen Fjern.
16. Skriv "Filnavn" i feltet Navn.
    * Filnavn  
17. Vælg "Streng" i feltet Varetype.
18. Klik på Tilføj.

## <a name="map-new-data-model-elements-to-data-sources"></a>Tilknyt nye datamodelelementer til datakilder
1. Klik på Tilknyt model til datakilde.
2. Brug Quick Filter til at filtrere på feltet Definition med værdien 'InvoiceCustomer'.
    * InvoiceCustomer  
    * Vi knytter nye modelelementer til relevante datakilder.  
3. Klik på Designer.
4. Vælg 'Vedhæftede filer i fakturaer' i træet.
5. Udvid 'Vedhæftede filer i fakturaer' i træet.
6. Vælg 'Vedhæftede filer i fakturaer\Filnavn' i træet.
7. Klik på Rediger.
8. Angiv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i feltet Formel.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Klik på Gem.
10. Luk siden.
11. Vælg 'Vedhæftede filer i fakturaer\Filindhold' i træet.
12. Klik på Rediger.
13. Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i feltet Formel.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.<'Documents'.'getFileContentAsContainer()'  
14. Klik på Gem.
15. Luk siden.
16. Vælg 'Vedhæftede filer i fakturaer' i træet.
17. Klik på Rediger.
18. Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i feltet Formel.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Klik på Gem.
20. Luk siden.
21. Klik på Gem.
22. Luk siden.
23. Luk siden.
24. Luk siden.
25. Klik på Skift status.
26. Klik på Fuldført.
27. Klik på OK.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]