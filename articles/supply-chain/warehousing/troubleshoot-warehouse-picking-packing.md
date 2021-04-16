---
title: Foretage fejlfinding af pluk og pakning
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du plukker og pakker i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1a54fa9dc21fb1691d74905a1215f4dfea31f136
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828124"
---
# <a name="troubleshoot-picking-and-packing"></a>Foretage fejlfinding af pluk og pakning

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du plukker og pakker i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Jeg får vist følgende fejlmeddelelse: "Dimensionslokation kan ikke være tom, hvis der er angivet dimensionsserienummer".

### <a name="issue-description"></a>Problembeskrivelse

Du får vist denne fejlmeddelelse, hvis du opretter en flytteordre for en serievare ved hjælp af et lagersted, der er aktiveret til avanceret lokationsstyring (WMS), og du derefter forsøger at bekræfte forsendelsen, efter at arbejdet er fuldført.

### <a name="issue-resolution"></a>Problemløsning

Feltet **Standardtilgangslokation** er tomt for et transitlagersted i "fra"-lagerstedet. Du kan løse dette problem ved at angive en standardtilgangslokation på transitlagerstedet. Kontrollér, at denne lokation er id-styret.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Jeg får vist følgende fejlmeddelelse: "Ugyldigt id".

### <a name="issue-description"></a>Problembeskrivelse

Du får vist denne fejlmeddelelse i mobilappen Lokationsstyring, når du scanner et nummerplade-id.

### <a name="issue-resolution"></a>Problemløsning

Kontrollér, at nummerpladens id findes i id-tabellen, og at varerne og antallet på id'et er tilgængelige (med andre ord blokeres de ikke).

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Jeg får vist følgende fejlmeddelelse: "Feltets lastvægt (=-%1) kan kun indeholde positive tal. Opdateringen er annulleret".

### <a name="issue-description"></a>Problembeskrivelse

Du får vist denne fejlmeddelelse, hvis der er åbent arbejde, når du behandler arbejde fra pakkelokationer til midlertidige lokationer, eller fra midlertidige lokationer til dock-lokationer.

### <a name="issue-resolution"></a>Problemløsning

Du kan løse dette problem ved at gå til **Systemadministration \> Periodiske opgaver \> Database \> Konsistenskontrol** og køre processen til **Konsistenskontrol af lagersteds lastvægt**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Jeg får vist følgende fejlmeddelelse: "Antallet er ikke gyldigt for enheden %1".

### <a name="issue-description"></a>Problembeskrivelse

Du får vist denne fejlmeddelelse, når du forsøger at udføre et *opdelt pluk* på tværs af flere batches.

### <a name="issue-resolution"></a>Problemløsning

Lagermedarbejderen skal bruge *Kort pluk* som proces i mobilappen Lokationsstyring. Hvis du forsøger at plukke flere batcher fra samme lokation, kan du også bruge indstillingen **Fuld** i appen.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Jeg kan ikke flytte lager til en lokation, der er id-kontrolleret.

### <a name="issue-description"></a>Problembeskrivelse

Du kan ikke reducere plukantal på en last.

### <a name="issue-resolution"></a>Problemløsning

I tidligere versioner kan du ikke reducere plukantal på en last. Du kan dog nu vælge at flytte et pluk til en id-kontrolleret lokation. Du skal angive både en **Lokation**-værdi og en **ID**-værdi for lastlinjen på siden **Reducer plukket antal**.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Kan jeg udskrive en følgeseddel eller pakkeindhold efter lagersted?

### <a name="issue-description"></a>Problembeskrivelse

Du vil udskrive en følgeseddel eller pakkeindhold efter lagersted eller sted på siden **Opdater skabelonlinje for arbejdsrevision**.

### <a name="issue-resolution"></a>Problemløsning

Når du udskriver et dokument ved hjælp af indstillinger for udskriftsstyring, skal du begrænse omfanget (lokation/lagersted) via udskriftsstyring i stedet for at vælge **Rediger udskriftsindstillinger** på siden **Opdater skabelonlinje for arbejdsrevision**.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Jeg kan ikke annullere en følgeseddel, når den er bogført fra en salgsordre.

### <a name="issue-description"></a>Problembeskrivelse

Når pluk- og forsendelsesprocesser er aktiveret for WMS, kan du ikke annullere en følgeseddel, når den er bogført fra en salgsordre.

### <a name="issue-resolution"></a>Problemløsning

Hvis du vil rette bogførte følgesedler for varer, der er aktiveret for WMS, skal bogføringen ske fra lasten, ikke fra ordren. Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning. Generelt kan en salgsordre, der er plukket og afsendt via lokationsstyringsprocesser, få opdateret følgeseddel fra lasen eller forsendelsen og selve salgsordredokumentet. Men hvis du opdaterer følgeseddel på salgsordren fra salgsordredokumentet, kan tilbageførslen af følgesedlen stadig ikke udføres fra last- eller salgsordren. Det anbefales derfor, at du bruger bogføring af følgesedlen fra lasten. I dette tilfælde vil tilbageførsel, der foretages fra lasten, blive aktiveret.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Jeg får følgende fejlmeddelelse: "Der kan ikke findes nok arbejde for klyngen".

### <a name="issue-description"></a>Problembeskrivelse

Når du bruger *Systemstyret klyngepluk* som proces, hvis du konfigurerer en klyngeprofil, hvor der f.eks. kan plukkes 10 placeringer, fungerer processen som planlagt, når der er nok arbejde til at plukke til 10 placeringer. Men hvis der kun er otte placeringer, der kan plukkes, får du vist denne fejlmeddelelse, fordi der ikke er nok arbejde til én klynge.

### <a name="issue-resolution"></a>Problemløsning

Du kan løse dette problem ved at redigere klyngeprofilen og angive indstillingen **Aktivér placeringer** til *Nej*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]