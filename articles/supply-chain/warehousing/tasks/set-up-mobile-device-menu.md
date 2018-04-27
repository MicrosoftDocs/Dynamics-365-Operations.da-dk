--- 
title: "Konfigurere et menupunkt for mobilenheden til fuldførelse af arbejde på en indkøbsordre"
description: "Denne fremgangsmåde viser, hvordan du konfigurerer et menupunkt for en mobilenhed."
author: BibiSp
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b80c258d6a779a8fc5bb6c846abd3af7e69d5e06
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a>Konfigurere et menupunkt for mobilenheden til fuldførelse af arbejde på en indkøbsordre

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du konfigurerer et menupunkt for en mobilenhed. I dette eksempel bruges menupunktet til at udføre arbejde af typen Indkøbsordre. Det arbejde, der er gyldigt, bestemmes af den arbejdsklasse, der er knyttet til menupunktet. Du kan bruge denne guide i USMF-demodatafirmaet. Denne procedure udføres typisk af en lagerstedschef.


## <a name="create-a-mobile-device-menu-item"></a>Oprette et menupunkt på en mobilenhed
1. Gå til menupunkter i mobilenhed.
2. Klik på Ny.
3. Skriv en værdi i feltet Menupunktnavn.
    * Angiv en entydig værdi. Du kan for eksempel skrive POMove. Husk værdien, du skal bruge den senere.  
4. Skriv en værdi i feltet Titel.
    * Dette er den titel, der vises på mobilenheden. Du kan for eksempel skrive PO Move.  
5. Vælg "Arbejde" i feltet Tilstand.
6. Vælg Ja i feltet Brug eksisterende arbejde.
    * Dette menupunkt på mobilenheden bruges til at udføre eksisterende arbejde. Derfor skal du indstille værdien til Ja.  
    * Feltet Vis lagerstatus bestemmer, om lagerstatus for den disponible lagerbeholdning vises for lagermedarbejderen på mobilenheden.  
7. Vælg "Systemgruppering" i feltet Ledet af.
    * Når du markerer noget i feltet Ledet af, vises der flere felter i sektionen Generelt på denne side. De felter, der vises, afhænger af, hvad du har valgt. Når du vælger Systemgruppering, tilføjes der to nye felter. De beskrives nedenfor.  
8. Vælg 'WorkPoolId' i feltet Systemgrupperingsfelt.
    * Når lagermedarbejderne åbner dette menupunkt, bliver de bedt om at scanne et arbejdspulje-id. Alle arbejdsordrer med dette arbejdspulje-id og åbne arbejdsordrelinjer med en af arbejdsklasserne føjet til dette menupunkt bliver overført til brugeren.  
9. Skriv en værdi i feltet Systemgrupperingslabel.
    * Dette er den tekst, der vises for brugeren på mobilenheden. Du kan for eksempel skrive Arbejdspulje.  
10. Vælg Ja i feltet Tilsidesæt nummerplade under læg på lager.
    * Denne indstilling gør det muligt for lagermedarbejderne at tilsidesætte målnummerplade, når varer anbringes på en nummerpladestyret lokalitet.  
11. Vælg Ja i feltet Gruppér vareplacering.
    * Hvis alle læg på lager-linjerne i arbejdsordren deler den samme lokalitet, modtager brugeren en kombineret læg på lager-instruktion for alle linjer.  
    * Id for arbejdsrevisionsskabelon: En arbejdsskabelon gør det muligt at angive, at arbejdsprocessen for et menupunkt skal afbrydes, så en anden handling kan udføres. Hvis dette menupunkt f.eks. er for indgående arbejde, kan revisionsskabelonen kræve, at arbejderen kontrollerer temperaturen. Det tidspunkt, hvor processen afbrydes, er angivet på revisionsskabelonen og kan f.eks. være, når arbejdet startes eller afsluttes, eller når status ændres.  
12. Udvid sektionen Arbejdsklasser.
13. Klik på Ny.
14. Skriv "Køb" i feltet Arbejdsklasse-id.
    * Arbejdspuljen begrænser det arbejde, som menupunktet kan bruges til. I dette tilfælde bruges den til åbne arbejdsordrelinjer, der har købets arbejdsklasse-id.  
15. Klik på Gem.

## <a name="set-up-work-confirmation"></a>Konfigurer arbejdsbekræftelse
1. Klik på Konfiguration af arbejdsbekræftelse.
2. Vælg "Pluk" i feltet Arbejdstype.
3. Marker afkrydsningsfeltet Bekræft automatisk.
    * Arbejdsinstruktionen med arbejdstypen Pluk bliver bekræftet automatisk. Denne instruktion vises ikke for brugeren.  
4. Klik på Ny.
5. Vælg 'Læg på lager' i feltet Arbejdstype.
6. Marker afkrydsningsfeltet Bekræftelse af lokation.
    * Lagermedarbejderen bliver bedt om at udføre en bekræftelsesscanning af lokaliteten, når varen anbringes.  
7. Klik på Gem.
8. Luk siden.
9. Luk siden.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Føje menupunktet til en mobilenhedsmenu
1. Gå til menuen Mobilenhed.
2. Klik på Rediger.
3. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på feltet Navn med værdien 'indgående'.
    * Du vil finde den menu, du bruger til indgående menupunkter. I USMF kaldes dette felt Indgående.  
4. Vælg 'en værdi' i træet.
5. Klik på den pil, der peger mod højre.
6. Klik på Gem.
7. Luk siden.


