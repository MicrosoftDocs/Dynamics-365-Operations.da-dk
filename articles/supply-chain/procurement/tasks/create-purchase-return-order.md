---
title: Oprette en købsreturordre
description: Denne fremgangsmåde viser, hvordan du kan oprette en indkøbsreturordre ved hjælp af handlingen Kreditnota for at kopiere linjer fra et kreditorfakturadokument til en ny indkøbsordre.
author: GalynaFedorova
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying, InventMarking, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 841229434fc278224f85d8d6782f80a31f4e23a9
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678709"
---
# <a name="create-a-purchase-return-order"></a>Oprette en købsreturordre

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du kan oprette en indkøbsreturordre ved hjælp af handlingen Kreditnota for at kopiere linjer fra et kreditorfakturadokument til en ny indkøbsordre. Det viser også, hvordan du kan bekræfte ordren og behandle forsendelsen af varerne tilbage til leverandøren. Eksemplet i denne procedure kan bruges i demodatafirmaet USMF. Denne opgave foretages typisk af en indkøber.

## <a name="create-a-new-purchase-return-order"></a>Opret en ny indkøbsreturordre
1. Gå til **Navigationsruden > Moduler > Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer**. Det første trin er at oprette en ny indkøbsordre, der skal bruges som indkøbsreturordre.  
2. Klik på **Ny**.
3. Skriv "US-102" i feltet **Kreditorkonto**.
4. Klik på **OK**.
5. Klik på **Køb** i **Handlingsrude**.
6. Klik på **Kreditnota**. Det er den side, hvorfra du kan kopiere fra en eksisterende kreditorfaktura til din returordre. Dette er den samme side, der bruges til andre kopieringshandlinger. Men da vi har åbnet den fra handlingen Kreditnota, er siden konfigureret til at understøtte oprettelsen af en returordre, der modregner kreditorfakturaer.  
7. Udvid sektionen **Parametre**.
    - Indstillingen **Vend fortegn** vælges automatisk og kan ikke ændres. Derved sikres, at tegnet ændres for mængderne, og at de ordrelinjer, der er tilføjet, modregnes kreditorfakturaen.  
    - Indstillingen **Kopiér gebyrer** vælges automatisk og kan ikke ændres. Det betyder, at gebyrer fra kreditorfakturaen føjes til købsreturvareordren for at modregne det oprindelige gebyr. Det er muligt at redigere ændringerne i ordrehovedet og på linjerne senere.  
    - Indstillingen **Kopier præcis** vælges automatisk og kan ikke ændres. Dette sikrer, at der oprettes en nøjagtig kopi af værdierne i alle felter på kreditorfakturaoverskriften og på linjerne. Det betyder, at der oprettes en indkøbsreturordre med værdier, der stemmer overens med alle vilkår, der bruges sammen med kreditorfakturadokumentet. 
    - Indstillingen **Slet købslinjer** sletter alle indkøbsordrelinjer, der allerede findes på indkøbsordren, før der tilføjes nye linjer. I dette eksempel har vi endnu ikke tilføjet nogen linjer til indkøbsreturordren, så det ville ikke have nogen effekt. Brug denne indstilling med omhu, da det sletter alle eksisterende linjer uden yderligere varsel.  
    * Indstillingen **Kopier ordrehoved** vælges automatisk og kan ikke ændres. Dette sikrer, at oplysninger kopieres fra kreditorfakturaen og anvendes på indkøbsreturordrehovedet. Dette er nyttigt, fordi det bidrager til at sikre, at indkøbsreturordren udligner fakturaen ved hjælp af lignende vilkår.  
8. Skjul sektionen **Parametre**.
9. Udvid afsnittet **Fakturaer**. Siden er blevet åbnet via handlingen Kreditnota, så den eneste mulighed er at kopiere oplysninger fra kreditorfakturaer. Denne fane viser alle tilgængelige fakturaer for den kreditorkonto, der er angivet på den indkøbsreturordre, du oprettede tidligere.   Fakturaerne identificeres ved fakturabilag eller indkøbsordre-id.
10. Find den kreditorfaktura, der er identificeret ved fakturanummer AP-0006, og fremhæv linjen ved at klikke på et felt på den pågældende linje.
11. Vælg linjen ved at markere afkrydsningsfeltet for linjen. Bemærk, at de linjer, der er tilgængelige på kreditorfakturaen, automatisk vælges sammen med ordren. Denne særlige kreditorfaktura har 2 ordrelinjer. I dette eksempel vil vi returnere en del af mængden fra den anden linje.
12. Fremhæv den anden linje (den med vare M0006) ved at klikke på et felt på den pågældende linje.
13. I feltet **Antal** skal du ændre antallet til 10. Det er det antal, der skal returneres til leverandøren. 
14. Fremhæv den første linje (den med vare M0005) ved at klikke på et felt på den pågældende linje.
15. Fjern markeringen i afkrydsningsfeltet for linjen. Kun de linjer, du har valgt, kopieres til din ordre.
16. Skjul afsnittet **Fakturaer**.
17. Udvid sektionen **Valgte linjer eller hoved, der skal kopieres**. Denne visning indeholder en oversigt over alle dokumenter og linjer, du har valgt til at blive kopieret til din ordre.  
18. Skjul sektionen **Valgte linjer eller overskrifter, der skal kopieres**.
19. Klik på **OK**. Den linje, du har valgt, er nu kopieret til din indkøbsreturordre. Feltet **Antal** viser -10.   
20. Klik på **Lager** i sektionen **Indkøbsordrelinje**.
21. Klik på **Markering**. Den ordrelinje, der er oprettet, er markeret mod lagertransaktion fra kreditorfakturaen. Dette sikrer, at det lager, der er returneret til leverandøren, er det samme som det lager, der blev modtaget fra dem tidligere. Der er situationer, hvor mærkningen ikke opstår, for eksempel hvis lageret allerede er markeret som forbrugt, eller hvis produktet er et, der ikke bruger mærkning.  

22. Klik på **OK**.

## <a name="confirm-and-record-the-shipment-of-goods"></a>Bekræft og registrer forsendelsen af varer
1. Klik på **Handlinger > Bekræft**.
2. Klik på **Modtag** i **handlingsruden**.
3. Klik på **Produktkvittering**.
    - Denne side bruges til at registrere produktkvitteringer for indkøbsordrer og til at behandle returneringen af varer tilbage til leverandøren. Ordrelinjer med et negativt antal betyder, at varer skal returneres til leverandøren, og det dokument, der kan oprettes fra denne side, kan bruges som følgeseddel i den forbindelse.   
    - Vælg Bestilt antal i feltet **Antal** i dette eksempel. Dette sikrer, at forsendelsen behandles for hele det bestilte antal, som ordrelinjerne blev oprettet med.   
4. Skriv en værdi i feltet **Produktkvittering**. Dette felt bruges til at angive en reference, der skal bruges som bilag for produktkvitteringskladden.  
5. Klik på **OK**. Varerne er nu registreret som leveret på indkøbsreturordren, og der er oprettet en produktkvitteringskladde. Du kan bruge handlingen Produktkvittering til at gennemse de kladder, der er oprettet med indkøbsordren, og til at se, hvad der er modtaget eller returneret, og hvornår.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]