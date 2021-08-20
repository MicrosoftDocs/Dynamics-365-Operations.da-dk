---
title: Lokalisere fejl i priser, rabatter og aftaler
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med priser, rabatter og aftaler.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 237ec60823eb5fded09c32d6a51b1eb504456a1dc666d7d6f2e6678382433de9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762836"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Lokalisere fejl i priser, rabatter og aftaler

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med priser, rabatter og aftaler.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>Jeg kan ikke knytte en købsaftale til en indkøbsordrelinje, når indkøbsordren er oprettet.

En købsaftale skal knyttes til en indkøbsordre, når indkøbsordren oprettes. Ellers kan indkøbsordrelinjer ikke knyttes til købsaftalelinjer.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Hvilken kontrol aktiverer meddelelsen "Opdater priser og rabatter, der er angivet manuelt eller med et eksternt dokument"?

Når du ændrer afsendelsesdatoen, kan du få vist en meddelelse, der angiver "Opdater priser og rabatter, der er angivet manuelt eller med et eksternt dokument". Du modtager denne meddelelse, for hvis afsendelsesdatoen ændres, kan en anden samhandels- eller salgsaftale udløses og forårsage en prisændring. En ændring af afsendelsesdatoen kan også påvirke lagertidsplaner og andre relaterede oplysninger.

Meddelelsen udløses, hver gang en af datoerne eller andre parametre ændres. Formålet med meddelelsen er at sikre, at du er opmærksom på prisændringer, der kan forekomme på grund af disse ændringer.

Meddelelsen er anmodningen om evaluering af samhandelsaftalen. En fuldstændig beskrivelse finder du i [Politikker til evaluering af samhandelsaftale](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>En købsordrekvittering omfatter ikke alle gebyrer.

### <a name="reproduce-the-issue"></a>Genskabe problemet

Følgende procedurer viser en måde at genskabe problemet på.

1. På siden **Indkøbs- og forsyningsparametre** skal du under fanen **Levering** kontrollere, at indstillingen **Generér gebyrer på produktkvittering** er angivet til *Ja*.
1. Opret en indkøbsordre, der inkluderer gebyrer.
1. Bekræft indkøbsordren.
1. Modtag indkøbsordren.
1. Kig på den kvitteringstotalen, og sammenlign den med den forventede total.
1. Bemærk, at ikke alle gebyrer er medtaget i købsordrekvitteringen.

### <a name="issue-resolution"></a>Problemløsning

Løsningen afhænger af den måde, som de forskellige gebyrer er konfigureret på. Du kan finde oplysninger om, hvordan du konfigurerer gebyrer, så de opfylder dine behov, i følgende blogindlæg: [Bogføre diverse gebyrer på tidspunktet for produktmodtagelse](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Priser og rabatter i samhandelsaftaler anvendes ikke på salgs- eller indkøbsordrelinjer, der er importeret via Dataadministration.

### <a name="issue-description"></a>Problembeskrivelse

Samhandelsaftaler, der anvendes på salgs- eller indkøbsordrelinjer, gælder ikke på linjer, der er importeret via Dataadministration. De samme samhandelsaftaler anvendes dog på salgs- eller indkøbsordrelinjer, der er oprettet manuelt.

### <a name="reason-for-the-issue"></a>Årsag til problemet

Hvis indkøbsordrelinjer, der importeres via Dataadministration, allerede indeholder prisoplysninger, evalueres samhandelsaftalen ikke igen for disse linjer. Hvis f.eks. **Linjerabatprocent** eller nogen af pris- og rabatværdierne er angivet for en linje, vil samhandelsaftaler ikke blive slået op for denne linje.

### <a name="issue-workaround"></a>Problemløsning

Denne funktionsmåde forventes og er ens for både salgsordrer og indkøbsordrer.

Du kan løse problemet ved at importere indkøbsordrelinjerne uden at angive prisoplysninger. Samhandelsaftalerne vil derefter blive anvendt, og indkøbsordrelinjerne opdateres på baggrund af de definerede samhandelsaftaler.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>En leverandørrabat bliver ikke akkumuleret på basis af fakturaer.

### <a name="issue-description"></a>Problembeskrivelse

Hvis fakturaer, der er bogført, har forskellige forfaldsdatoer, afspejles disse fakturaer ikke i de leverandørrabatter, der genereres af dem.

### <a name="issue-resolution"></a>Problemløsning

Forfaldsdatoen tages som standard ikke i betragtning, når leverandørrabatten beregnes. Overvej at tilpasse systemet, så forfaldsdatoen og relationen til fakturaen er mere synlig i forhold til den faktiske leverandørrabat.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Enhedspriser på indkøbsordrer beregnes ikke ud fra enhedsomregningen.

### <a name="issue-description"></a>Problembeskrivelse

Når en enhed ændres i en indkøbsordre, genberegnes priserne for samhandelsaftaler ikke ifølge definitionerne for enhedsomregning.

### <a name="issue-resolution"></a>Problemløsning

Priser hentes altid fra samhandelsaftaler (eller andre prisindstillinger i systemet, f.eks. salgsaftaler eller varepriser), og de angives for en enhed.

Hvis enheden ændres på en ordrelinje, søger systemet efter en pris for den nye enhed og anvender denne pris. Hvis der ikke findes en pris for enheden, vil systemet ikke anvende en pris. Enhedsomregningen kan ikke bruges til at genberegne prisen til en anden enhed. Teoretisk er prisen for en kasse på ti måske ikke lig med ti gange prisen på en enkelt kasse.

### <a name="issue-workaround"></a>Problemløsning

En måde at løse dette problem på er at sikre, at der bruges samhandelsaftaler for de enheder, du forventer skal bruges på ordrelinjerne for varen.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>Valutaomregningsproblemer opstår med samhandelsaftaler.

Priserne i samhandelsaftaler genberegnes ikke i henhold til valutaen, når valutaen afviger på en indkøbsordre.

Med funktionen *Generisk valuta* kan du kun definere priser og rabatter i én valuta. Du kan derefter omregne til andre valutaer efter behov. Når omregningen er udført, kan funktionen desuden automatisk anvende intelligent afrunding.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Når jeg åbner siden Købsaftale i en linjevisningstilstand, kan jeg ikke tilpasse siden ved at føje feltet Prisenhed til oversigten på linjen.

Visse delte felter i aftalestrukturen kan ikke medtages i personlige indstillinger. Denne begrænsning forekommer på grund af den implementerede datamodel. Du kan derfor ikke tilpasse feltet **Prisenhed**.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>Den maksimale grænse for en købsaftale er ikke gældende på en indkøbsrekvisition.

### <a name="issue-description"></a>Problembeskrivelse

Når en indkøbsrekvisition er knyttet til en købsaftale, er maksimumgrænsen fra købsaftalen ikke gældende i indkøbsrekvisitionen. Standardprisoplysningerne angives korrekt, men mere end maksimumgrænsen fra købsaftalen kan bestilles i indkøbsrekvisitionen.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde forventes. Da rekvisitioner ikke altid er godkendt, bør et antal eller beløb ikke reserveres på købsaftalen. Derfor når du ikke maksimumgrænsen fra købsaftalen.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Der kan oprettes samhandelsaftaler ud fra afviste tilbudsanmodninger. Systemet forhindrer derfor ikke, at samhandelskladderne oprettes, hvis linjen i tilbudsanmodningen ikke er blevet accepteret.

Du kan oprette samhandelsaftaler som svar på en tilbudsanmodning, uanset om den er blevet accepteret eller afvist. Du kan finde flere oplysninger under [Oversigt over tilbudsanmodninger](request-quotations.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]