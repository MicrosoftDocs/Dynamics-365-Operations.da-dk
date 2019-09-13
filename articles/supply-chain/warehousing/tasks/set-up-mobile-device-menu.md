---
title: Konfigurere et menupunkt på en mobilenhed til at udføre arbejde af typen indkøbsordre
description: I dette emne vises, hvordan du konfigurerer et menupunkt for en mobilenhed.
author: ShylaThompson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1c922d16b46e26031e5f80886e4e4e8f08bcdaf
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916852"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Konfigurere et menupunkt på en mobilenhed til at udføre arbejde af typen indkøbsordre

[!include [task guide banner](../../includes/task-guide-banner.md)]

I dette emne vises, hvordan du konfigurerer et menupunkt for en mobilenhed. I dette eksempel bruges menupunktet til at udføre arbejde af typen Indkøbsordre. Det arbejde, der er gyldigt, bestemmes af den arbejdsklasse, der er knyttet til menupunktet. Du kan bruge denne guide i USMF-demodatafirmaet. Denne procedure udføres typisk af en lagerstedschef.


## <a name="create-a-mobile-device-menu-item"></a>Oprette et menupunkt på en mobilenhed
1. Gå til **Menupunkter i mobilenhed** ved at angive dem i søgepanelet.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Menupunktnavn**. Angiv en entydig værdi. Du kan for eksempel skrive `POMove`. Husk værdien, du skal bruge den senere.  
4. Skriv en værdi i feltet **Titel**. Dette er den titel, der vises på mobilenheden. Du kan for eksempel skrive `PO Move`.  
5. Vælg **Arbejde** i feltet **Tilstand**.
6. Vælg **Ja** i feltet **Brug eksisterende arbejde**.
    - Dette menupunkt på mobilenheden bruges til at udføre eksisterende arbejde. Derfor skal du indstille værdien til **Ja**.  
    - Feltet **Vis lagerstatus** bestemmer, om lagerstatus for den disponible lagerbeholdning vises for lagermedarbejderen på mobilenheden.  
7. Vælg **Systemgruppering** i feltet **Ledet af**. Når du markerer noget i feltet **Ledet af**, vises der flere felter i sektionen **Generelt** på denne side. De felter, der vises, afhænger af, hvad du har valgt. Når du vælger **Systemgruppering**, tilføjes der to nye felter. De beskrives nedenfor.  
8. Vælg **WorkPoolId** i feltet **Systemgruppering**. Når lagermedarbejderne åbner dette menupunkt, bliver de bedt om at scanne et arbejdspulje-id. Alle arbejdsordrer med dette arbejdspulje-id og åbne arbejdsordrelinjer med en af arbejdsklasserne føjet til dette menupunkt bliver overført til brugeren.  
9. Skriv en værdi i feltet **Systemgrupperingslabel**. Dette er den tekst, der vises for brugeren på mobilenheden. Du kan for eksempel skrive **Arbejdspulje**.  
10. Vælg **Ja** i feltet **Tilsidesæt nummerplade under læg på lager**. Denne indstilling gør det muligt for lagermedarbejderne at tilsidesætte målnummerplade, når varer anbringes på en nummerpladestyret lokalitet.  
11. Vælg **Ja** i feltet **Gruppér vareplacering**.
    - Hvis alle læg på lager-linjerne i arbejdsordren deler den samme lokalitet, modtager brugeren en kombineret læg på lager-instruktion for alle linjer. 
    - Id for arbejdsrevisionsskabelon: En arbejdsskabelon gør det muligt at angive, at arbejdsprocessen for et menupunkt skal afbrydes, så en anden handling kan udføres. Hvis dette menupunkt f.eks. er for indgående arbejde, kan revisionsskabelonen kræve, at arbejderen kontrollerer temperaturen. Det tidspunkt, hvor processen afbrydes, er angivet på revisionsskabelonen og kan f.eks. være, når arbejdet startes eller afsluttes, eller når status ændres.  
12. Udvid sektionen **Arbejdsklasser**.
13. Vælg **Ny**.
14. Skriv `Purchase` i feltet **Arbejdsklasse-id**. Arbejdspuljen begrænser det arbejde, som menupunktet kan bruges til. I dette tilfælde bruges den til åbne arbejdsordrelinjer, der har købets arbejdsklasse-id.  
15. Vælg **Gem**.

## <a name="set-up-work-confirmation"></a>Konfigurer arbejdsbekræftelse
1. Vælg **Konfiguration af arbejdsbekræftelse**.
2. Vælg **Pluk** i feltet **Arbejdstype**.
3. Marker afkrydsningsfeltet **Bekræft automatisk**. Arbejdsinstruktionen med arbejdstypen Pluk bliver bekræftet automatisk. Denne instruktion vises ikke for brugeren.  
4. Vælg **Ny**.
5. Vælg "Læg på lager" i feltet **Arbejdstype**.
6. Marker afkrydsningsfeltet **Bekræftelse af lokation**. Lagermedarbejderen bliver bedt om at udføre en bekræftelsesscanning af lokaliteten, når varen anbringes.  
7. Vælg **Gem**.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Føje menupunktet til en mobilenhedsmenu
1. Gå til menuen **Mobilenhed** ved at angive den i søgepanelet.
2. Vælg **Rediger**.
3. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på feltet **Navn** med værdien **indgående**. Du vil finde den menu, du bruger til indgående menupunkter. I USMF kaldes dette felt **Indgående**.  
4. Vælg **en værdi** i træet.
5. Vælg den pil, der peger mod højre.
6. Vælg **Gem**.
7. Luk siden.
