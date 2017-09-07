--- 
title: "Køre format til at bruge dokumentstyringsfiler i formatoutput til elektronisk rapportering (ER)"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6e1d7a54055829a1e9215a44f8eba346291f6717
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Køre format til at bruge dokumentstyringsfiler i formatoutput til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER. Disse trin kan udføres i DEMF-virksomheden.

For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 3: Opret model)".

Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Tilføj de nødvendige vedhæftede filer for en salgsordre til en enkelt faktura
1. Gå til Debitor > Fakturaer > Åbne debitorfakturaer.
2. Brug Quick Filter til at finde poster. Du kan for eksempel filtrere på feltet Faktura med værdien 'CIV-000148'.
    * CIV-000148  
3. Klik for at følge linket til den valgte faktura.
    * CIV-000148  
4. Klik for at følge linket i feltet Salgsordre.
    * 000148  
5. Vælg indstillingen Hoved i feltet Linjer eller hoved.
    * Marker Hoved for at angive, at dette vil være mål for tilføjelse af vedhæftede filer.  
6. Klik på Vedhæft.
    * Tilføj et par filer som vedhæftede filer til denne salgsordre. Brug filerne af de dokumenttyper, som understøttes i Dokumentstyring (med filtypenavne DOCX, DPF, XML, JPG osv.). Gennemse og vælg filer, der skal vedhæftes og behandles yderligere med den relaterede faktura i den elektroniske ER-meddelelse.  
7. Klik på Ny.
8. Klik på Filer.
9. Klik på Ny.
10. Klik på Filer.
11. Luk siden.
12. Luk siden.
13. Luk siden.
14. Luk siden.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Kør rapporten, der er designet til den valgte faktura
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Udvid 'Debitorfakturamodel' i træet.
3. Udvid 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.
4. Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)\Eksempelmeddelelse i elektronisk faktura' i træet.
5. Klik på Kør.
6. Udvid posterne for at inkludere sektion ().
7. Klik på Filtrér.
8. Markér rækken Debitorfakturajournal og feltet Salgsordre.
9. Skriv "000148" i feltet Kriterier.
    * Skriv ordrenummer 000148 i kriteriefeltet "Salgsordre".  
10. Klik på OK.
11. Klik på OK.
    * Gennemse det genererede output. Bemærk, at der er oprettet en enkelt XML-node for hver vedhæftet fil. Indholdet i den vedhæftede fil udfyldes til XML-outputtet i MIME-tekstformat (base64).  

