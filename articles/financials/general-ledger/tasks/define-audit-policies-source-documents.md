--- 
title: Definere revisionspolitikker for kildedokumenter
description: "Denne procedure viser, hvordan du kan konfigurere og køre regler for overvågningspolitik."
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b05f744120e940bfea3e92b8aac3e41fc8151d9
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="define-audit-policies-for-source-documents"></a>Definere revisionspolitikker for kildedokumenter

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan konfigurere og køre regler for overvågningspolitik. I eksemplet bruges udgiftsrapporter med udgiftstypen hotel. Denne procedure bruger demofirmaet USMF. Rollen revisor indeholder de korrekte tilladelser til at kunne udføre disse opgaver.

1. Gå til Revisionspanel > Opsætning > Politikregeltype.
2. Klik på Ny.
3. Skriv en værdi i feltet Regelnavn.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg Udgiftsrapportlinje i feltet Forespørgselsnavn.
6. Vælg Aggregér i forespørgselstypefeltet
7. Vælg Juridisk enhed i feltet Juridisk enhed.
8. Vælg Dato og klokkeslæt for ændring i feltet Dokumentdatohenvisning
9. Klik på Gem.
10. Gå til Revisionspanel > Opsætning > Overvågningspolitikker.
11. Klik på Ny.
12. Skriv en værdi i feltet Navn.
13. Udvid sektionen Politikorganisationer.
14. Vælg "Contoso Entertainment System USA" i træet.
15. Klik på Tilføj.
16. Vælg "Contoso Consulting USA" i træet'.
17. Klik på Tilføj.
18. Vælg "Contoso Retail USA" i træet'.
19. Klik på Tilføj.
20. Skjul sektionen Politikorganisationer.
21. Udvid sektionen Politikregler.
22. Find og vælg den Politikregel, som blev oprettet tidligere, på listen.
23. Klik på Opret politikregel.
24. Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.
25. Klik på Filtrér.
26. Vælg rækken for Udgiftsart på listen, og angiv detaljerne til Hotel
27. Indtast eller vælg en værdi i feltet Kriterier.
28. Klik på fanen Aggregér.
29. Klik på Tilføj.
30. Vælg feltværdien Transaktionsbeløb på listen
31. Indtast eller vælg en værdi i feltet Felt.
32. Vælg "Sum"i feltet Aggregeringsfunktion.
33. Klik på fanen Gruppér efter.
34. Klik på Tilføj.
35. Vælg værdien Medarbejder på listen  
36. Klik på Tilføj.
37. Vælg værdien Udgiftsart på listen
38. Indtast eller vælg en værdi i feltet Felt.
39. Klik på fanen Har.
40. Klik på Tilføj.
41. Vælg Transaktionsbeløb
42. Indtast eller vælg en værdi i feltet Felt.
43. Vælg "Sum"i feltet Aggregeringsfunktion.
44. Skriv ">2000" i feltet Kriterier.
45. Klik på OK.
46. Klik på Test.
47. Angiv en dato og klokkeslæt i feltet Startdato for dokumentudvælgelse.
48. Angiv en dato og klokkeslæt i feltet Slutdato for dokumentudvælgelse.
49. Klik på Kør test.
50. Klik på Overvågningspolitik i handlingsruden.
51. Klik på Flere indstillinger.
52. Angiv en dato og et klokkeslæt i feltet Startdato.
53. Angiv en dato og et klokkeslæt i feltet Slutdato.
54. Klik på Batch.
55. Udvid sektionen Kør i baggrunden.
56. Vælg Ja i feltet Batchbehandling.
57. Klik på OK.
58. Gå til Revisionspanel > Overvåg sager.
59. Find og vælg den ønskede post på listen.
60. Klik op linket i den valgte række på listen.
61. Udvid sektionen Tilknytninger.
62. Find og vælg den ønskede post på listen.
63. Klik op linket i den valgte række på listen.


