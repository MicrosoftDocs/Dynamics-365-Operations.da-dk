--- 
title: "Ændre og køre format for at bruge dokumentstyringsfiler i formatoutput"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.openlocfilehash: b38f69fc169367aa56468b2c8f06b65fd1291c79
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs"></a>Ændre og køre format for at bruge dokumentstyringsfiler i formatoutput

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER. Disse trin kan udføres i DEMF-virksomheden.

For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 4: Kør model)".

Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Rediger formatet til udfyldning af vedhæftede filer til generering af meddelelser i binært format
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Udvid 'Debitorfakturamodel' i træet.
3. Udvid 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.
4. Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)\Eksempelmeddelelse i elektronisk faktura' i træet.
5. Klik på Designer.
    * Du udfylder fakturameddelelsen i det oprettede output som en XML-fil ved hjælp af Unicode-kodning.  
6. Klik på Tilføj rod for at åbne dialogboksen.
7. Vælg "Common\File" i træet.
8. Skriv "Xml-meddelelse" i feltet Navn.
    * Xml-meddelelse  
9. Skriv "UTF-8" i feltet Kodning.
    * UTF-8  
10. Klik på OK.
    * Konfigurer generering af output som en zip-fil.  
11. Klik på Tilføj rod for at åbne dialogboksen.
12. Vælg "Common\Folder" i træet.
13. Skriv "Output i zip-format" i feltet Navn.
    * Output i zip-format  
14. Klik på OK.
15. Vælg 'Output i zip-format' i træet.
    * Føj vedhæftede filer til den genererende zip-fil som filer med de oprindelige navne og filtyper.  
16. Klik på Tilføj for at åbne dialogboksen.
17. Vælg "Common\File" i træet.
18. Skriv 'Vedhæftet fil' i feltet Navn.
    * Vedhæftet fil  
19. Klik på OK.
20. Vælg 'Output i zip-format\Vedhæftet fil' i træet.
21. Klik på Tilføj for at åbne dialogboksen.
22. Vælg 'Text\Base64' i træet.
23. Klik på OK.

## <a name="map-new-format-elements-to-data-model"></a>Tilknyt nye formateringselementer til datamodellen
1. Klik på fanen Tilknytning.
2. Udvid 'model' i træet.
3. Udvid 'model\Vedhæftede filer i fakturaer' i træet.
4. Vælg 'Output i zip-format\Vedhæftet fil\Base64' i træet.
5. Vælg 'model\Vedhæftede filer i fakturaer\Filindhold' i træet.
6. Klik på Bind.
7. Vælg 'Output i zip-format\Vedhæftet fil' i træet.
8. Klik på Rediger filnavn.
9. Udvid 'model' i træet.
10. Udvid 'model\Vedhæftede filer i fakturaer' i træet.
11. Vælg 'model\Vedhæftede filer i fakturaer\Filnavn' i træet.
12. Klik på Tilføj datakilde.
13. Klik på Gem.
14. Luk siden.
15. Vælg 'model\Vedhæftede filer i fakturaer' i træet.
16. Klik på Bind.
17. Klik på Gem.
18. Luk siden.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Kør rapporten, der er designet til den valgte faktura
1. Klik på Kør.
2. Udvid posterne for at inkludere sektion ().
3. Klik på Filtrér.
4. Markér rækken Debitorfakturajournal og feltet Salgsordre.
5. Skriv ordrenummer 000148 i kriteriefeltet "Salgsordre".
    * 000148  
6. Klik på OK.
7. Klik på OK.
    * Gennemse det genererede output. Bemærk, at ud over fakturameddelelsen i XML-format er der oprettet en enkelt fil for hver vedhæftet fil. De vedhæftede filer er udfyldt med zip-outputtet i binært format.  


