--- 
title: "Undersøge eller løse undtagelser"
description: "Du kan køre kreditorfakturapolitikker, når du bogfører en kreditorfaktura ved hjælp af siden Kreditorfaktura, og når du åbner siden Overtrædelser af politik til kreditorfaktura."
author: abruer
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 6c191d0d5ad5c05ce3a9280bcca7c6916f0d963b
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="research-or-resolve-exceptions"></a>Undersøge eller løse undtagelser

[!include[task guide banner](../../includes/task-guide-banner.md)]

Du kan køre kreditorfakturapolitikker, når du bogfører en kreditorfaktura ved hjælp af siden Kreditorfaktura, og når du åbner siden Overtrædelser af politik til kreditorfaktura. Du kan også konfigurere arbejdsgangen for kreditorfakturaer til at køre politikker for kreditorfakturaer, hver gang du sender en faktura videre i arbejdsgangen. 

Kreditorfakturapolitikker gælder ikke for fakturaer, der er oprettet i indgangsbogen eller i fakturajournalen. 

Kreditorfakturapolitikker benyttes ikke til validering af fakturasammenholdelse, men er i stedet konfigureret på siden Kreditorparametre.

Denne registrering anvender demofirmaet USMF. Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin. Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Forberede oprettelse af politikker for kreditorfakturaer
1. Gå til Kreditor > Opsætning > Kreditorparametre.
2. Klik på fanen Fakturavalidering.
3. Markér eller fjern markeringen af afkrydsningsfeltet Opdater status for fakturahoved automatisk.
4. Klik på OK.
5. Vælg en indstilling i feltet Bogfør faktura med uoverensstemmelser.
6. Luk siden.
7. Gå til Kreditor > Konfiguration af politik > Politikker for kreditorfakturaer.
8. Klik på Parametre.
9. Klik på btnAdd.
10. Luk siden.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Oprette politikregeltyper for kreditorfakturaer
1. Gå til Kreditor > Konfiguration af politik > Regeltyper til politik for kreditorfakturaer.
2. Klik på Ny.
3. Skriv en værdi i feltet Regelnavn.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på rullelisten i feltet Forespørgselsnavn for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på Gem.
9. Luk siden.

## <a name="define-a-vendor-invoice-policy"></a>Definere en politik for kreditorfaktura
1. Gå til Kreditor > Konfiguration af politik > Politikker for kreditorfakturaer.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Skriv en værdi i feltet Beskrivelse.
5. Udvid eller skjul sektionen Politikorganisationer.
6. Vælg "Contoso Entertainment System USA" i træet.
7. Klik på Tilføj.
8. Udvid eller skjul sektionen Politikregler.
9. Klik på Opret politikregel.
10. Skriv en værdi i feltet Beskrivelse af politikregel.
11. Klik på Filtrér.
12. Klik på Tilføj.
13. Markér den valgte række på listen.
14. Klik på rullelisten i feltet Tabel for at åbne opslaget.
15. Klik op linket i den valgte række på listen.
16. Klik på rullelisten i feltet Afledt tabel for at åbne opslaget.
17. Klik op linket i den valgte række på listen.
18. Klik på rullelisten i feltet Felt for at åbne opslaget.
19. Skriv en værdi i feltet Felt.
20. Luk siden.
21. Skriv en værdi i feltet Kriterier.
22. Klik på OK.
23. Klik på OK.
24. Luk siden.
25. Luk siden.


