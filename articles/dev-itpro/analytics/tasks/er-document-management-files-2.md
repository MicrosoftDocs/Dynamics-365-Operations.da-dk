--- 
title: Udvide datamodel for at bruge dokumentstyringsfiler i formatoutput
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.openlocfilehash: bde8c612af22ba6bf4561732399fcf2cb1b5c9b3
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs"></a>Udvide datamodel for at bruge dokumentstyringsfiler i formatoutput

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER. Disse trin kan udføres i en hvilken som helst virksomhed.

For at fuldføre disse trin skal du først udføre trinnene i opgaveguiden "ER Brug filer fra Dokumentstyring i formatoutput (del 1: Forbered datamodel)".

Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


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

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a>Knytte nye datamodelelementer til Dynamics 365 for Finance and Operations-datakilder
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


