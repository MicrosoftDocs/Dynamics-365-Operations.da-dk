--- 
title: "Konfigurere en arbejdsskabelon for indkøbsordrer"
description: "Denne procedure fokuserer på konfiguration af en simpel arbejdsskabelon, der skal bruges, når varer, du har modtaget, lægges på lager."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: aa561d558827e78529ef797b6df6dd3c1dcce34d
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Konfigurere en arbejdsskabelon for indkøbsordrer

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure fokuserer på konfiguration af en simpel arbejdsskabelon, der skal bruges, når varer, du har modtaget, lægges på lager. Arbejdsskabeloner bestemmer det sæt instruktioner, der vises for lagermedarbejderen på en mobilenhed, når varer flyttes fra modtagelsesområdet. Du kan bruge denne procedure med de nævnte data i demodatafirmaet USMF. Før du starter denne vejledning, skal du oprette et arbejdspulje-id. I dette eksempel bruges arbejdspulje-id'et Indgående. Denne procedure er beregnet til lagerchefen.

1. Gå til Lagerstedsstyring > Opsætning > Arbejde > Arbejdsskabeloner.
2. I feltet Arbejdsordretype skal du vælge "Indkøbsordrer".

## <a name="create-a-work-template-header"></a>Oprette et arbejdsskabelonhoved
1. Klik på Ny.
2. Indtast et tal i feltet Sekvensnummer.
    * Dette er den rækkefølge, som arbejdsskabelonerne skal evalueres i. Du kan om nødvendigt ændre rækkefølgen.  
3. Indtast en værdi i feltet Arbejdsskabelon.
    * Dette er det entydige id for denne skabelon.  
4. Skriv en værdi i feltet Beskrivelse af arbejdsskabelon.
    * Indstillingen Gyldig markeres ikke, før du har fuldført alle de oplysninger, der er nødvendige for skabelonen, og derefter har klikket på Gem.  
    * En arbejdsordre af typen Indkøbsordre kan ikke behandles automatisk, så lad indstillingen Udfør automatisk behandling være indstillet til Nej.  
5. Indtast en værdi i feltet Arbejdspulje-id.
    * Med arbejdspulje-id'er kan du organisere arbejde i grupper. Den værdi, du angiver her, bliver standardværdien for arbejde, der oprettes ved hjælp af denne skabelon.  
6. Skriv 1 i feltet Arbejdsprioritet.
    * Dette angiver vigtigheden af arbejdet, og den værdi, du angiver her, bliver brugt som standard for alt arbejde, der oprettes ved hjælp af denne skabelon.  
7. Klik på Gem.
    * Du skal gemme arbejdsskabelonhovedet, før knappen Rediger forespørgsel bliver tilgængelig.  

## <a name="set-up-the-query-for-the-work-template"></a>Konfigurer forespørgslen til arbejdsskabelonen
1. Klik på Rediger forespørgsel.
    * Vi skal angive en begrænsning, så skabelonen kun kan bruges på et bestemt lagersted.  
2. Klik på Tilføj.
3. Markér den valgte række på listen.
4. I feltet Felt skal du skrive "lagersted".
5. Skriv en værdi i feltet Kriterier.
6. Klik på OK.
7. Klik på Ja.

## <a name="set-work-template-details"></a>Angiv arbejdsskabelondetaljer
1. Klik på Ny.
2. Vælg "Pluk" i feltet Arbejdstype.
3. Skriv "køb" i feltet Arbejdsklasse-id.
    * Den arbejdsklassen, som du angiver her, bliver standard på alle arbejdslinjer af typen Pluk, som oprettes ved hjælp af denne skabelon. Arbejdsklassen kan ikke tilsidesættes i arbejdsordrelinjerne. Arbejdsklasser bruges til at dirigere og/eller begrænse typen af arbejdsordrelinjer, som en lagermedarbejder kan behandle på en mobilenhed.  
4. Klik på Ny.
5. Vælg 'Læg på lager' i feltet Arbejdstype.
6. Skriv en værdi i feltet Arbejdsklasse-id.
    * Pluk og læg-instruktionerne er et sæt. Hvert pluk/lægsæt skal have samme arbejdsklasse. Brug samme arbejdsklasse, som du angav for plukinstruktionen.  
7. Klik på Gem.
    * Bemærk, at afkrydsningsfeltet Gyldig nu er markeret.  


