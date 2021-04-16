---
title: ER Brug dokumentstyringsfiler i formatoutput (del 3 - Opret format)
description: Dette emne beskriver, hvordan du konfigurerer et format for elektronisk rapportering til at bruge dokumentstyringsfiler i ER-output. (Del 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99a286b4e40ddeb7f4ff37c1ece3c678b26c838b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755004"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a>ER Brug dokumentstyringsfiler i formatoutput (del 3 - Opret format)

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER. Disse trin kan udføres i en hvilken som helst virksomhed.

For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 2: Udvid datamodel)".

Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="create-a-format-to-process-invoices"></a>Opret et format til behandling af fakturaer
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Rapporteringskonfigurationer.
3. Udvid 'Debitorfakturamodel' i træet.
4. Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.
    * Du skal oprette et format for at generere elektroniske meddelelser med oplysninger om de filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.  
5. Klik på Opret konfiguration for at åbne dialogboksen.
6. Skriv "Format baseret på datamodel\Debitorfakturamodel (brugerdefineret)" i feltet Ny.
7. Skriv 'Eksempelmeddelelse i elektronisk faktura' i feltet navn.
    * Eksempelmeddelelse i elektronisk faktura  
8. Indtast eller vælg en værdi i feltet Definition af datamodel.
    * InvoiceCustomer  
9. Klik på Opret konfiguration.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Design et format til udfyldning af vedhæftede filer til generering af en meddelelse i MIME-format
1. Klik på Designer.
2. Klik på Tilføj rod for at åbne dialogboksen.
3. Vælg "XML\Element'' i træet.
4. Skriv 'Faktura' i feltet Navn.
    * Fakturaer  
5. Klik på OK.
6. Klik på Tilføj for at åbne dialogboksen.
7. Vælg "XML\Attribut" i træet.
8. Skriv 'SalesOrder' i feltet Navn.
    * SalesOrder  
9. Klik på OK.
10. Klik på Tilføj attribut.
11. Skriv "InvoiceNumber" i feltet Navn.
    * InvoiceNumber  
12. Klik på OK.
13. Klik på Tilføj attribut.
14. Skriv 'InvoiceAmount' i feltet Navn.
    * InvoiceAmount  
15. Klik på OK.
16. Klik på Tilføj for at åbne dialogboksen.
17. Vælg "XML\Element'' i træet.
18. Skriv "EnclosedDocs" i feltet Navn.
    * EnclosedDocs  
19. Klik på OK.
20. Vælg 'Faktura\EnclosedDocs' i træet.
21. Klik på Tilføj element.
22. Skriv 'Dokument' i feltet Navn.
    * Dokument  
23. Klik på OK.
24. Vælg 'Faktura\EnclosedDocs\Dokument' i træet.
25. Klik på Tilføj for at åbne dialogboksen.
26. Vælg "XML\Attribut" i træet.
27. Skriv "FileName" i feltet Navn.
    * FileName  
28. Klik på OK.
29. Klik på Tilføj for at åbne dialogboksen.
30. Vælg "XML\Element'' i træet.
31. Skriv 'FileContent' i feltet Navn.
    * FileContent  
32. Klik på OK.
33. Vælg 'Invoice\EnclosedDocs\Document\FileContent' i træet.
34. Klik på Tilføj for at åbne dialogboksen.
35. Vælg 'Text\Base64' i træet.
36. Klik på OK.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Knyt formateringselementer til datamodellen som en datakilde
1. Vælg 'Faktura\SalesOrder' i træet.
2. Klik på fanen Tilknytning.
3. Udvid 'model' i træet.
4. Vælg 'model\Salgsordrenummer(SalesId)' i træet.
5. Klik på Bind.
6. Vælg 'Faktura\InvoiceNumber' i træet.
7. Udvid 'model\Basisfaktura(InvoiceBase)' i træet.
8. Vælg 'model\Basisfaktura(InvoiceBase)\Fakturanummer(Id)' i træet.
9. Klik på Bind.
10. Vælg 'Faktura\InvoiceAmount' i træet.
11. Vælg 'model\Basisfaktura(InvoiceBase)\Fakturabeløb(Amount)' i træet.
12. Klik på Bind.
13. Udvid 'model\Vedhæftede filer i fakturaer' i træet.
14. Vælg 'model\Vedhæftede filer i fakturaer\Filindhold' i træet.
15. Vælg 'Invoice\EnclosedDocs\Document\FileContent\Base64' i træet.
16. Klik på Bind.
17. Vælg 'model\Vedhæftede filer i fakturaer\Filnavn' i træet.
18. Vælg 'Invoice\EnclosedDocs\Document\FileName' i træet.
19. Klik på Bind.
20. Vælg 'model\Vedhæftede filer i fakturaer' i træet.
21. Vælg 'Faktura\EnclosedDocs\Dokument' i træet.
22. Klik på Bind.
23. Klik på Gem.
24. Luk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]