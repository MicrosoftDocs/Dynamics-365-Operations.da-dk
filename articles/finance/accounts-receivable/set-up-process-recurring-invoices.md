---
title: Oprette og behandle tilbagevendende fakturaer
description: I denne artikel beskrives det, hvordan du opretter og behandler tilbagevendende fakturaer. Du kan bruge tilbagevendende fakturaer, hvis du skal fakturere kunder for samme beløb med jævne mellemrum.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b443630d1612b5095fefa74b5ed6d057be534b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441458"
---
# <a name="set-up-and-process-recurring-invoices"></a>Oprette og behandle tilbagevendende fakturaer

[!include [banner](../includes/banner.md)]

I denne artikel beskrives det, hvordan du opretter og behandler tilbagevendende fakturaer. Du kan bruge tilbagevendende fakturaer, hvis du skal fakturere kunder for samme beløb med jævne mellemrum.

<a name="create-a-recurring-free-text-invoice-template"></a>Oprette en skabelon til en tilbagevendende fritekstfaktura
---------------------------------------------

Hvis du regelmæssigt skal fakturere kunder for de samme tjenester, kan du definere en skabelon til fritekstfakturaer, som kan genbruges til oprettelse af fakturaerne. Denne skabelon indeholder følgende oplysninger:

-   Hovedoplysninger, som momsgrupper, betalingsbetingelser og betalingsmåde
-   Linjeoplysninger som beskrivelse af tjenesten, indtægtskonti, enhedspris og fakturabeløb
-   Gebyrer for forsendelse eller håndtering
-   Regnskabsfordelinger samt økonomiske dimensionsoplysninger som bærere og virksomhedsenheder

Du opretter reelt en hel faktura og gemme den som en skabelon. Du kan konfigurere skabeloner ved hjælp af siden **Tilbagevendende fakturaer**.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Tildele en fritekstfakturaskabelon til en debitor, og angiv oplysninger om gentagelse
Når skabelonen er oprettet, skal du tildele skabelonen til de kunder, som du vil fakturere. Derudover skal du angive, hvornår og hvor ofte fakturaen skal bruges. Du kan tildele skabelonerne under fanen **Faktura** på siden **Kunder**. Føj skabelonen til listen, og opdater følgende oplysninger:

-   Startdatoen og eventuelt slutdatoen for den tilbagevendende fakturering.
-   Hyppigheden af den tilbagevendende fakturering (f.eks. hver dag eller en gang om måneden)
-   Det maksimale faktureringsbeløb (hvis disse oplysninger er påkrævet)

En kunde kan have flere skabeloner, der har forskellige frekvenser.

## <a name="generate-the-recurring-invoices"></a>Oprette de tilbagevendende fakturaer
På siden **Tilbagevendende fakturaer** er der en opgave, der behandler skabeloner til tilbagevendende fakturaer. Du angiver fakturadatoen og skabelonen, som fakturaerne skal oprettes ud fra. Fakturaer oprettes og tildeles et enkelt gentagelses-id for hver gruppe fakturaer, der er behandlet.

<a name="post-recurring-free-text-invoices"></a>Bogføre tilbagevendende fritekstfakturaer
---------------------------------

Når der er oprettet tilbagevendende fakturaer, vises fakturaens gentagelses-id'er i en bogføringsopgave på siden **Tilbagevendende fakturaer**. Du kan få vist alle fakturaer for et gentagelses-id ved at klikke på linket. Under din gennemgang af fakturaer for gentagelses-id'et kan du slette enkelte fakturaer. Kundens indstillinger for gentagelse nulstilles for den pågældende skabelon, så den kan gendannes senere. Du kan bogføre en, mange eller alle fakturaer for et gentagelses-id. Hvis arbejdsgange er aktiveret, skal du klikke på **Send**, før du kan bogføre fakturaerne.

<a name="print-recurring-free-text-invoices"></a>Udskriv tilbagevendende fritekstfakturaer
----------------------------------

Når tilbagevendende fakturaer bogføres, kan du udskrive fakturaer fra listesiden med fritekstfakturaer. Du kan udskrive de fakturaer, der er valgt, eller du kan vælge et interval af fakturaer, der skal udskrives.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]