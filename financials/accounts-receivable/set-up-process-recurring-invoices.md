---
title: Oprette og behandle tilbagevendende fakturaer
description: "I denne artikel beskrives det, hvordan du opretter og behandler tilbagevendende fakturaer. Du kan bruge tilbagevendende fakturaer, hvis du skal fakturere kunder for samme beløb med jævne mellemrum."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f14e9227ef56f428d18999aa7b52254580cdfa4
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-and-process-recurring-invoices"></a>Oprette og behandle tilbagevendende fakturaer

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
På siden **Tilbagevendende fakturaer **er der en opgave, der behandler skabeloner til tilbagevendende fakturaer. Du angiver fakturadatoen og skabelonen, som fakturaerne skal oprettes ud fra. Fakturaer oprettes og tildeles et enkelt gentagelses-id for hver gruppe fakturaer, der er behandlet.
Bogføre tilbagevendende fritekstfakturaer
---------------------------------

Når der er oprettet tilbagevendende fakturaer, vises fakturaens gentagelses-id'er i en bogføringsopgave på siden **Tilbagevendende fakturaer**. Du kan få vist alle fakturaer for et gentagelses-id ved at klikke på linket. Under din gennemgang af fakturaer for gentagelses-id'et kan du slette enkelte fakturaer. Kundens indstillinger for gentagelse nulstilles for den pågældende skabelon, så den kan gendannes senere. Du kan bogføre en, mange eller alle fakturaer for et gentagelses-id. Hvis arbejdsgange er aktiveret, skal du klikke på **Send**, før du kan bogføre fakturaerne.
Udskriv tilbagevendende fritekstfakturaer
----------------------------------

Når tilbagevendende fakturaer bogføres, kan du udskrive fakturaer fra listesiden med fritekstfakturaer. Du kan udskrive de fakturaer, der er valgt, eller du kan vælge et interval af fakturaer, der skal udskrives.

