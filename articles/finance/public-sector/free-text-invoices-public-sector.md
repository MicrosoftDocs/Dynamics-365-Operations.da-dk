---
title: Fritekstfakturaer i den offentlige sektor
description: I dette emne beskrives funktionen til fritekstfakturaer, som er tilgængelig for den offentlige sektor, samt besvares almindelige spørgsmål om brugen af faktureringsklassifikationer og faktureringskoder til fritekstfakturaer.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillingClassification, CustBillingCode, CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 25821
ms.assetid: 483e2726-ec48-4d1f-82f5-bffddea301ce
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f458e52ac77496682018e496dcedce358549ad3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407651"
---
# <a name="free-text-invoices-in-the-public-sector"></a>Fritekstfakturaer i den offentlige sektor

[!include [banner](../includes/banner.md)]

I dette emne beskrives funktionen til fritekstfakturaer, som er tilgængelig for den offentlige sektor, samt besvares almindelige spørgsmål om brugen af faktureringsklassifikationer og faktureringskoder til fritekstfakturaer.

<a name="do-i-have-to-select-a-billing-classification-for-every-free-text-invoice"></a>Skal jeg vælge en faktureringsklassifikation for hver fritekstfaktura?
-------------------------------------------------------------------------

Ja, når faktureringsklassifikationer er aktiveret, er det nødvendigt at angive en faktureringsklassifikation for hver fritekstfaktura. Faktureringsklassifikationen styrer, hvilke faktureringskoder der kan angives på fakturaen. Den styrer også betalingsvilkår og -betingelser, nummerserier og behandlingen af fakturaen. Du kan få flere oplysninger om faktureringsklassifikationer i [Faktureringsklassifikationer og faktureringskoder i den offentlige sektor](billing-classifications-billing-codes-public-sector.md).

## <a name="what-happens-if-ive-already-created-free-text-invoices-when-i-enable-billing-classifications"></a>Hvad sker der, hvis jeg allerede har oprettet fritekstfakturaer, når jeg aktiverer faktureringsklassifikationer?
Hvis en faktura ikke er bogført endnu, når du har aktiveret faktureringsklassifikationer, skal du tildele en faktureringsklassifikation til fakturaen, før du kan bogføre den. Når du åbner siden for at få vist fakturaen, får du en meddelelse om, at faktureringsklassifikationen er påkrævet.

## <a name="why-should-i-use-billing-codes-when-i-create-free-text-invoices"></a>Hvorfor skal jeg bruge faktureringskoder, når jeg opretter fritekstfakturaer?
Når du vælger en faktureringskode, angives der automatisk standardværdier på mange felter på fakturalinjen. Dette gør dataindtastningen hurtigere og mere nøjagtig. Faktureringskoder bruges også med bogføringsdefinitioner til at styre, hvordan debitorposteringer bogføres i Finans.

## <a name="im-creating-a-free-text-invoice-and-the-billing-code-that-i-want-to-use-isnt-available-what-should-i-do"></a>Jeg opretter en fritekstfaktura, og den faktureringskode, der skal bruges, er ikke tilgængelig. Hvad skal jeg gøre?
Kontrollér først, at fakturaen bruger den rigtige faktureringsklassifikation. Kun visse faktureringskoder kan bruges sammen med hver faktureringsklassifikation. Hvis faktureringsklassifikationen er korrekt, skal du derefter vælge en af de faktureringskoder, der er tilgængelige for den fritekstfaktura, du opretter.

## <a name="i-can-change-some-of-the-fields-on-my-free-text-invoices-all-of-the-time-and-i-can-change-all-of-the-fields-some-of-the-time-but-some-of-the-fields-i-can-only-change-some-of-the-time-whats-up-with-that"></a>Jeg kan ændre nogle af felterne på mine fritekstfakturaer hele tiden, og jeg kan ændre alle felterne nogle gange. Men nogle af felterne kan jeg kun ændre nogle gange. Hvorfor det?
Indstillinger på faktureringskoden styrer, om du kan ændre bestemte felter.

-   Hvis faktureringskoden på en fritekstfakturalinje ikke tillader ændringer på fakturaen, kan du ikke ændre beløbet, prisen eller beløbets detaljer på linjen. 

> [!TIP] 
> Hvis feltet **Faktureringskode** afgør er angivet til salgspris, kan du ikke ændre prisen, men du kan ændre beløbet indirekte ved at ændre antallet.

-   Hvis faktureringskoden på en fritekstfakturalinje ikke tillader ændringer til finanskonti, kan du ikke ændre regnskabsfordelinger på linjen. Du kan ændre den hovedkonto, der vises på fritekstfakturalinjen, men denne ændring påvirker kun, hvad der vises. Ændring af hovedkontoen påvirker ikke fordelingerne.
-   Når der er et projekt, der er tilknyttet fakturalinjen, styrer faktureringskoden, om du kan ændre projekt-id, kategori og finanskonto. 

> [!TIP] 
> Hvis du vil ændre finanskontoen for fakturalinjer, der er relateret til projekter, skal ændringerne tillades, både på selve faktureringskoden og afsnittet Projekter på siden Debitorparametre.

Du kan få flere oplysninger om faktureringskoder i [Faktureringsklassifikationer og faktureringskoder i den offentlige sektor](billing-classifications-billing-codes-public-sector.md).

## <a name="where-does-the-interest-code-on-a-free-text-invoice-come-from"></a>Hvor kommer rentekoden på en fritekstfaktura fra?
Rentekoden kan indstilles på faktureringskoden, faktureringsklassifikationen eller posteringsprofilen.





