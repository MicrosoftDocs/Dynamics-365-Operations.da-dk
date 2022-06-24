---
title: Konfigurere en arbejdsskabelon for indkøbsordrer
description: Denne artikel beskriver, hvordan du konfigurerer en simpel arbejdsskabelon, der skal bruges, når varer, du har modtaget, lægges på lager.
author: Mirzaab
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee6bc896a979c326001e1596e4a463753005fabf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877357"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Konfigurere en arbejdsskabelon for indkøbsordrer

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer en simpel arbejdsskabelon, der skal bruges, når varer, du har modtaget, lægges på lager. Arbejdsskabeloner bestemmer det sæt instruktioner, der vises for lagermedarbejderen på en mobilenhed, når varer flyttes fra modtagelsesområdet. Du kan bruge denne procedure med de nævnte data i demodatafirmaet USMF. Før du starter denne vejledning, skal du oprette et arbejdspulje-id. I dette eksempel bruges arbejdspulje-id'et Indgående. Denne procedure er beregnet til lagerchefen.

1. I navigationsruden skal du gå til **Moduler > Lokationsstyring > Opsætning > Arbejde > Arbejdsskabeloner**.
2. I feltet **Arbejdsordretype** skal du vælge **Indkøbsordrer**.

## <a name="create-a-work-template-header"></a>Oprette et arbejdsskabelonhoved
1. Vælg **Ny**.
2. Indtast et tal i feltet **Serienummer**. Dette er den rækkefølge, som arbejdsskabelonerne skal evalueres i. Du kan om nødvendigt ændre rækkefølgen.  
3. Indtast en værdi i feltet **Arbejdsskabelon**. Dette er det entydige id for denne skabelon.  
4. Skriv en værdi i feltet **Beskrivelse af arbejdsskabelon**.
    - Indstillingen **Gyldig** markeres ikke, før du har fuldført alle de oplysninger, der er nødvendige for skabelonen, og derefter har valgt **Gem**.  
    - En arbejdsordre af typen **Indkøbsordre** kan ikke behandles automatisk, så lad indstillingen **Udfør automatisk behandling** være indstillet til **Nej**.  
5. Indtast en værdi i feltet **Arbejdspulje-id**. Med arbejdspulje-id'er kan du organisere arbejde i grupper. Den værdi, du angiver her, bliver standardværdien for arbejde, der oprettes ved hjælp af denne skabelon.  
6. Skriv `1` i feltet **Arbejdsprioritet**. Dette angiver vigtigheden af arbejdet, og den værdi, du angiver her, bliver brugt som standard for alt arbejde, der oprettes ved hjælp af denne skabelon.  
7. Vælg **Gem**. Du skal gemme arbejdsskabelonhovedet, før knappen **Rediger forespørgsel** bliver tilgængelig.  

## <a name="set-up-the-query-for-the-work-template"></a>Konfigurer forespørgslen til arbejdsskabelonen
1. Vælg **Rediger forespørgsel**. Vi skal angive en begrænsning, så skabelonen kun kan bruges på et bestemt lagersted.  
2. Vælg **Tilføj**.
3. I feltet **Felt** for den nye række skal du skrive `warehouse`.
4. Skriv en værdi i feltet **Kriterier**.
5. Vælg **OK**.
6. Vælg **Ja**.

## <a name="set-work-template-details"></a>Angiv arbejdsskabelondetaljer
1. Vælg **Ny**.
2. Vælg **Pluk** i feltet **Arbejdstype**.
3. Skriv `purchase` i feltet **Arbejdsklasse-id**. Den arbejdsklassen, som du angiver her, bliver standard på alle arbejdslinjer af typen Pluk, som oprettes ved hjælp af denne skabelon. Arbejdsklassen kan ikke tilsidesættes i arbejdsordrelinjerne. Arbejdsklasser bruges til at dirigere og/eller begrænse typen af arbejdsordrelinjer, som en lagermedarbejder kan behandle på en mobilenhed.  
4. Vælg **Ny**.
5. Vælg **Læg på lager** i feltet **Arbejdstype**.
6. Skriv en værdi i feltet **Arbejdsklasse-id**. Pluk og læg-instruktionerne er et sæt. Hvert pluk/lægsæt skal have samme arbejdsklasse. Brug samme arbejdsklasse, som du angav for plukinstruktionen.  
7. Vælg **Gem**. Bemærk, at afkrydsningsfeltet **Gyldig** nu er markeret.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]