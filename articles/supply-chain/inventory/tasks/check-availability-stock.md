--- 
title: "Kontrollere tilgængelighed af lagerbeholdning"
description: "Denne fremgangsmåde viser, hvordan du kontrollerer disponible og fysisk disponibel lagerbeholdning for et bestemt varenummer."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: 
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62338fe11c30781f264e626fad835a2ba9dca837
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="check-the-availability-of-stock"></a>Kontrollere tilgængelighed af lagerbeholdning

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du kontrollerer disponible og fysisk disponibel lagerbeholdning for et bestemt varenummer. Den viser også, hvordan du får leveringsoplysninger relateret til en vare. Fysisk disponibel lagerbeholdning er den disponible lagerbeholdning, der er tilgængelig – den er købt, modtaget og registreret. Den disponible lagerbeholdning indeholder den tilgængelige disponible lagerbeholdning, men også det lager, der er bestilt og forventes, men endnu ikke modtaget eller registreret. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data. Hvis du bruger USMF, kan du bruge eksempelværdier, der vises. Disse opgaver udføres normalt af en lagerarbejder.


## <a name="check-on-hand-inventory-for-an-item"></a>Kontrollér disponibel lagerbeholdning for en vare
1. Gå til Lagerstyring > Forespørgsler og rapporter > Disponibel lagerbeholdning.
2. Vælg varenummerrækken.
    * Hvis du vil forespørge om den disponible lagerbeholdning efter varenummer, skal du markere den række, hvor tabellen er angivet til den disponible lagerbeholdning og felt er angivet til varenummer.  
3. Vælg den vare, du vil forespørge på, i feltet Kriterier.
    * Hvis du bruger demodatafirmaet USMF, kan du vælge 'M9201'.  
4. Klik på OK.
5. Klik på Dimensioner.
    * Med fanen Dimensioner kan du vælge, hvor mange oplysninger du vil se om den disponible lagerbeholdning. Hvis du har brug for data vedrørende reservation, skal du få vist alle lagerdimensioner for de varer, der bruger avancerede lagerstedsprocesser (WHS).  
6. Klik på OK.
7. Klik på Relaterede oplysninger i handlingsruden.
    * Hvis du ikke kan se dette, skal du muligvis klikke på ellipseknappen (...) for at få vist yderligere indstillinger i handlingsruden.  
8. Klik på Leveringsoversigt.
    * Fanen Leveringsoversigt indeholder leveringsoplysninger for en bestemt vare, som disponibelt antal, leveringstid og kreditoroplysninger.  
9. Udvid sektionen Tilgængelige.
10. Vis sektionen Kreditorer.
11. Luk siden.
12. Luk siden.

## <a name="check-physical-on-hand-inventory"></a>Kontrollér fysisk disponibel lagerbeholdning
1. Gå til Lagerstedsstyring > Forespørgsler og rapporter > Fysisk disponibel lagerbeholdning.
2. Indtast en værdi i feltet Varenummer.
    * Du kan bruge felterne Sted og Lagersted til at filtrere listen over varer.  
3. Opdater siden.
4. Klik på Visningsdimensioner.
    * Med fanen Dimensionsvisning kan du vælge, hvor mange oplysninger du vil se om den disponible lagerbeholdning.  
5. Klik på OK.
6. Luk siden.

## <a name="check-on-hand-inventory-by-location"></a>Kontrollér disponibel lagerbeholdning efter lokation.
1. Gå til Lagerstedsstyring > Forespørgsler og rapporter > Disponibel efter lokation.
2. Skriv en værdi i feltet Lagersted.
    * Hvis du bruger demodatafirmaet USMF, kan du bruge "51".  
3. Opdater siden.
4. Klik på Visningsdimensioner.
5. Klik på OK.
6. Luk siden.


