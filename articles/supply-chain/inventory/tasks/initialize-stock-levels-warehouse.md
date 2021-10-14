---
title: Initialisere lagerbeholdninger på lagerstedet
description: Denne procedure viser, hvordan du får den disponible lagerbeholdning opdateret manuelt ved hjælp af en lagerbevægelseskladden.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 264dabf9c1c10c3d2cee3e0c942abbfa249f21f5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565873"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Initialisere lagerbeholdninger på lagerstedet

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du får den disponible lagerbeholdning opdateret manuelt ved hjælp af en lagerbevægelseskladden. (Det er også muligt at opdatere den disponible lagerbeholdning ved at importere posteringer i dataenheder). Du kan køre denne guide i demodatafirmaet USMF, hvor alle de nødvendige komponenter som kladdenavn, vareopsætning, posteringsprofiler og konti er tilgængelige. Guiden foreslår specifikke værdier for varen og dimensionerne, der bruges. Hvis du vælger et andet element, skal du indtaste værdier for forskellige dimensioner.

1. Gå til Lagerstyring > Kladdeposteringer > Elementer > Bevægelser.
2. Klik på Ny.
3. Klik på rullelisten i feltet Navn for at åbne opslaget.
4. Vælg IMov.
    * Det er en god ide at bruge forskellige journalnavnskabeloner for de forskellige forretningsmæssige formål.  
5. Klik op linket i den valgte række på listen.
6. I feltet Modkonto skal du angive værdien "140200".
    * Dette er den modkonto, der skal være standardkontoen på kladdelinjerne. Det er muligt at tilsidesætte standardindstillingerne for at tildele forskellige modkonti pr. linje.  
7. Klik på OK.
8. Klik på Ny.
9. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
10. Vælg vare A0001.
11. Klik op linket i den valgte række på listen.
12. Klik på fanen Lagerdimensioner.
13. Klik på rullelisten i feltet Sted for at åbne opslaget.
14. Vælg sted 1.
15. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
16. Vælg lagersted 13.
17. Klik op linket i den valgte række på listen.
18. Klik på rullelisten i feltet Lokation for at åbne opslaget.
19. Vælg lokalitet 13.
20. Angiv et tal i feltet Antal.
21. Klik på Gem.
22. Klik på Bogfør.
23. Markér eller fjern markeringen af afkrydsningsfeltet Overfør alle posteringsfejl til en ny kladde.
    * Hvis du aktiverer denne indstilling, kopieres alle linjer, der ikke kan bogføres, til en ny journal. Du kan bruge oplysningerne i logfilen til at løse problemerne og derefter bogføre linjerne igen.  
24. Klik på OK.
25. Luk siden.
26. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]