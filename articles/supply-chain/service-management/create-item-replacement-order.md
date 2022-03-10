---
title: Oprette en genanskaffelsesordre for en vare
description: Der oprettes normalt en genanskaffelsesordre for en vare, når et produkt er returneret og kontrolleret.
author: josaw1
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57bbb8eb638b990914dc00f9700ff0c1925c48852862b02e09f3f26415d3e347
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745496"
---
# <a name="create-an-item-replacement-order"></a>Oprette en genanskaffelsesordre for en vare 

[!include [banner](../includes/banner.md)]


Der oprettes normalt en genanskaffelsesordre for en vare, når et produkt er returneret og kontrolleret. Når en vare skal erstattes, inden den er returneret, eller når den oprindelige vare ikke vil blive returneret, kan du oprette en genanskaffelsesordre for en vare, straks du opretter en returordre.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Oprette en erstatningsordre, når du modtaget en returneret vare

1.  Klik på **Salg og marketing** \> **Generelt** \> **Returordrer** \> **Alle returordrer**.

2.  Opret en ny returordre, eller vælg en returordre fra listen for at åbne formularen **Returordre - RMA-nummer: %1, %2**.

3.  Klik på **Returlinje**, og vælg derefter **Erstatningsvare**.

4.  Vælg den vare, der skal erstatte den returnerede vare. Angiv varespecifikationer, og klik derefter på **Anvend**.

5.  Klik på **Følgeseddel** for at generere en følgeseddel til returordren. Der oprettes en salgsordre for den valgte erstatningsvare.
    
    Når salgsordren er oprettet for erstatningsvaren, søges der automatisk i salgsaftaler, og hvis der findes en relevant salgsaftale, anvendes den på salgsordren.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Oprette en erstatningsordre, før du modtager en vare, der returneres

1.  Klik på **Salg og marketing** \> **Generelt** \> **Returordrer** \> **Alle returordrer**.

2.  Opret en ny returordre, eller vælg en returordre fra listen for at åbne formularen **Returordre - RMA-nummer: %1, %2**.

3.  Klik på **Find salgsordre**, hvis du vil identificere salgsordren for den returnerede vare. Udfyld formularen **Find salgsordre**, og klik derefter på **OK** for at lukke formularen og vende tilbage til formularen **Returordre - RMA-nummer: %1, %2**. Salgsordrelinjen for den returnerede vare kopieres til returordren.

4.  Klik på **Erstatningsordre** for at åbne formularen **Opret salgsordre**.

5.  Marker afkrydsningsfeltet **Kopier returordrelinjer** for at overføre detaljer fra den returordre, du markerede i formularen **Returordre - RMA-nummer: %1, %2**, til denne salgsordre.

6.  Angiv eller tilpas detaljerne efter behov.
    
    Hvis du identificerede salgsordren i trin 3 i , og hvis salgsordrelinjen for den returnerede vare er knyttet til en salgsaftale, vises id'et for den relevante salgsaftale for vareerstatningsordren automatisk i feltet **Salgsaftale-id**.

7.  Klik på **OK** for at lukke formularen **Opret salgsordre** og åbne formularen **Salgsordre**, hvor du kan fortsætte med at angive oplysninger for den nye salgsordre. Alle gældende returordrelinjer kopieres til den nye salgsordre. 
    
    Hvis id'et for salgsaftalen vises automatisk i feltet **Salgsaftale-id**, er salgsaftalen blevet knyttet til salgsordrehovedet for vareerstatningsordren. Hvis der er en gældende forpligtelse i salgsaftalen, som endnu ikke er opfyldt, og salgsordren er oprettet, før salgsaftalen udløber, oprettes der et link mellem salgsaftalelinjen og salgsordrelinjen. Derfor kopieres oplysninger fra salgsaftalen som f.eks. varepris, til den nye salgsordrelinje. 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]