---
title: Konfigurere en oversigtsprofil for varemodtagelse
description: Denne artikel fokuserer på oprettelse af en modtagelsesoversigtsprofil.
author: yufeihuang
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8517710f5d0be1859f86449152712d950281769a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872001"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Konfigurere en oversigtsprofil for varemodtagelse

[!include [banner](../../includes/banner.md)]

Denne artikel fokuserer på oprettelse af en modtagelsesoversigtsprofil. Profilen for modtagelsesoversigt er en samling af regler, der anvendes, når siden Modtagelsesoversigt åbnes af en bruger. Du kan bruge denne procedure i USMF-demodatafirmaet. Denne procedure vil typisk blive udført af en modtagende medarbejder.

1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Distribution > Profiler for oversigt over modtagelse**.
2. Vælg **Ny**. Da du næsten altid vil arbejde på samme lagersted og aflaste fulde lastbillæs, bør du oprette en profil for modtagelsesoversigt for at forenkle processen med at registrere modtagne varer.  
3. Indtast en værdi i feltet **Navn for profil for oversigt over modtagelse**.
4. Vælg en indstilling i feltet **Vis linjer**. Vælg, hvilke linjer der skal vises for tilgangene:  

    - **Alle** – Vis alle linjer uanset status.   
    - **I gang** – Vis linjer for tilgange, hvor statussen er Afsluttet eller Delvist. Dette betyder, at enten det fulde antal eller et delvist antal er registreret for hver linje i en modtagelseskladde.   
    - **Ikke færdig** – Vis linjer for tilgange, hvor statussen er Ingen eller Delvist. Dette betyder, at enten intet eller kun et delvist antal er registreret for hver linje i en modtagelseskladde.  

5. Udvid eller skjul sektionen **Modtagelsesindstillinger**.
6. Indtast en værdi i feltet **Dage frem**. Dette angiver et filter for at vise de kvitteringslinjer, der forventes at blive modtaget inden for de næste par dage (afhængigt af det nummer, du angiver).  
7. Indtast en værdi i feltet **Dage tilbage**. Dette angiver et filter for at vise de kvitteringslinjer, der forventes at blive modtaget et antal dage før dags dato.  
8. Indtast en værdi i feltet **Lagersteder**. Filter på et eller flere lagersteder.  
9. Vælg en værdi i feltet **Leveringsmåde**. Dette angiver et filter til kun at vise modtagelseslinjerne med denne leveringsmåde.  
10. Vælg WHS i feltet **Navn**.
11. I feltet **Lagersted** skal du vælge et lagersted 24. Dette er det standardlagersted, der skal bruges til registrerede modtagelseslinjer, der bruger denne profil.  
12. Vælg **Baydoor** i feltet **Lokation**. Dette er den standardlokalitet, der skal bruges til registrerede modtagelseslinjer, som bruger denne profil.  
13. Vis eller skjul sektionen **Oplysninger om modtagelsesforespørgsel**.
14. Vælg lokation 2 i feltet **Begræns til sted**. Dette angiver et filter til kun at vise modtagelseslinjerne med dette sted.  
15. Vælg **Ja** i indstillingen **Indkøbsordrer**. Vælg kvitteringslinjer fra åbne indkøbsordrer.  
16. Vælg **Ja** i indstillingen **Flytteordrer**. Vælg kvitteringslinjer fra flytteordrer.  
17. Vælg **Gem**.
18. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
