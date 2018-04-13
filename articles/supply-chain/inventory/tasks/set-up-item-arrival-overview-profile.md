---
title: Konfigurere en oversigtsprofil for varemodtagelse
description: "Denne opgave fokuserer på oprettelse af en profil for modtagelsesoversigt."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 5ddc491d73bbb6ac02e37a9c9b9d93545f6f9556
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a>Konfigurere en oversigtsprofil for varemodtagelse

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne opgave fokuserer på oprettelse af en profil for modtagelsesoversigt. Profilen for modtagelsesoversigt er en samling af regler, der anvendes, når siden Modtagelsesoversigt åbnes af en bruger. Du kan bruge denne procedure i USMF-demodatafirmaet. Denne procedure vil typisk blive udført af en modtagende medarbejder.





1. Gå til Lagerstyring > Opsætning > Distribution > Profiler for oversigt over modtagelse.
2. Klik på Ny.
    * Da du næsten altid vil arbejde på samme lagersted og aflaste fulde lastbillæs, bør du oprette en profil for modtagelsesoversigt for at forenkle processen med at registrere modtagne varer.  
3. Indtast en værdi i feltet Navn for profil for oversigt over modtagelse.
4. Vælg en indstilling i feltet Vis linjer.
    * Vælg, hvilke linjer der skal vises for tilgangene: Alle – Vis alle linjer, uanset status.   I gang – Vis linjer for tilgange, hvor statussen er Afsluttet eller Delvist. Dette betyder, at enten det fulde antal eller et delvist antal er registreret for hver linje i en modtagelseskladde.   Ikke færdig – Vis linjer for tilgange, hvor statussen er Ingen eller Delvist. Dette betyder, at enten intet eller kun et delvist antal er registreret for hver linje i en modtagelseskladde.  
5. Udvid eller skjul sektionen Modtagelsesindstillinger.
6. Indtast en værdi i feltet Dage frem.
    * Dette angiver et filter for at vise de kvitteringslinjer, der forventes at blive modtaget inden for de næste par dage (afhængigt af det nummer, du angiver).  
7. Indtast en værdi i feltet Dage tilbage.
    * Dette angiver et filter for at vise de kvitteringslinjer, der forventes at blive modtaget et antal dage før dags dato.  
8. Indtast en værdi i feltet Lagersteder.
    * Filter på et eller flere lagersteder.  
9. Vælg en værdi i feltet Leveringsmåde.
    * Dette angiver et filter til kun at vise modtagelseslinjerne med denne leveringsmåde.  
10. Vælg WHS i feltet Navn.
11. I feltet Lagersted skal du vælge et lagersted 24.
    * Dette er det standardlagersted, der skal bruges til registrerede modtagelseslinjer, der bruger denne profil.  
12. Vælg Baydoor i feltet Lokation.
    * Dette er den standardlokalitet, der skal bruges til registrerede modtagelseslinjer, som bruger denne profil.  
13. Vis eller skjul sektionen Oplysninger om modtagelsesforespørgsel.
14. Vælg lokation 2 i feltet Begræns til sted.
    * Dette angiver et filter til kun at vise modtagelseslinjerne med dette sted.  
15. Angiv indstillingen Indkøbsordrer til Ja.
    * Vælg kvitteringslinjer fra åbne indkøbsordrer.  
16. Angiv indstillingen Flytteordrer til Ja.
    * Vælg kvitteringslinjer fra flytteordrer.  
17. Klik på Gem.
18. Luk siden.

