---
title: Oprette og fakturere en intern indkøbsordre til intern brug
description: Denne artikel beskriver oprettelse og fakturering af en intern indkøbsordre til intern brug
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 2260128c276ab7b712f7c97945b188ea42099fb4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877531"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Oprette og fakturere en intern indkøbsordre til intern brug

[!include [banner](../../includes/banner.md)]

Du kan oprette en intern indkøbsordre for en intern kreditor. Herved oprettes der automatisk en intern salgsordre til den interne kreditor.

![Intern købsproces](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Oprette en intern indkøbsordre og en tilsvarende intern salgsordre

Udfør disse trin i den juridiske enhed AAA, som vist i illustrationen.

1. Vælg **Kreditor** \> **Indkøbsordrer** \> **Alle indkøbsordrer**.
1. Opret en indkøbsordre til en intern kreditor på listesiden **Alle indkøbsordrer**. Feltværdier kopieres fra kreditorkontoen til indkøbsordren.

    Da du arbejder med en intern kreditor, oprettes der en intern salgsordre i den juridiske enhed, der svarer til kreditoren. Nummeret på den interne salgsordre kan være det samme som nummeret på den interne indkøbsordre, og den kan indeholde id'et på den juridiske enhed. Den nummerstruktur, der bruges, afhænger af valget i feltet **Salgsordrenummerering** på siden **Intern**. Hvis du eksempelvis opretter indkøbsordren 00029\_064 i den juridiske enhed AAA, er salgsordrenummeret i den juridiske enhed BBB AAA00029\_64.

    Der vises en meddelelse med oplysninger om, at der er oprettet en intern indkøbsordre og en intern salgsordre. Meddelelsen omfatter den interne salgsordrenummer til referencebrug.

1. Føj linjeelementer til indkøbsordren. De tilsvarende linjeelementer føjes automatisk til den interne salgsordre. Hvis et element ikke findes i den anden juridiske enhed, vises en meddelelse, og du kan ikke føje elementet til indkøbsordren. Du kan løse problemet ved at skifte til den anden juridiske enhed og frigive produktet til den pågældende juridiske enhed. Elementet bliver tilgængeligt og kan føjes til salgsordrer i den pågældende juridiske enhed. Skift derefter tilbage til den juridiske enhed for indkøbsordren, og fortsæt med at tilføje linjeelementer.
1. Når du er færdig med at skrive oplysninger til indkøbsordren, skal du bekræfte den.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>Behandl den interne følgeseddel og debitorfaktura

Udfør disse trin i den juridiske enhed BBB, som vist i illustrationen.

1. Gå til **Debitor \> Salgsordrer \> Alle salgsordrer**.
1. Vælg en intern salgsordre i listen på listesiden **Alle salgsordrer**.
1. Vælg fanen **Pluk og pak** i handlingsruden, og vælg derefter **følgesedlen**.
1. Marker afkrydsningsfeltet **Postering**.
1. Vælg **OK**. Følgesedlen er bogført i den juridiske enhed BBB.
1. Vælg en intern salgsordre i listen på listesiden **Alle salgsordrer**.
1. I handlingsruden skal du vælge fanen **Faktura** og derefter vælge **Faktura**.
1. Marker afkrydsningsfeltet **Postering**.
1. Vælg **OK**.

    Debitorfakturaen for den interne salgsordre bogføres i den juridiske enhed BBB.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>Behandl den interne produktkvittering og kreditorfaktura

Udfør disse trin i den juridiske enhed AAA, som vist i illustrationen.

1. Gå til **Kreditor \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Vælg en intern indkøbsordre i listen på listesiden **Alle indkøbsordrer**.
1. Vælg **Modtag**, og vælg derefter **Produktkvittering** i handlingsruden. Produktkvitteringen oprettes. Produktkvitteringsnummeret er den samme som det interne følgeseddelnummer.
1. Marker afkrydsningsfeltet **Postering**.
1. Vælg **OK**.
1. Vælg en intern indkøbsordre i listen på listesiden **Alle indkøbsordrer**.
1. I handlingsruden skal du vælge **Faktura** og derefter vælge **Faktura**. Kreditorfakturaen oprettes. Kreditorfakturanummeret er det samme som det interne kreditorfakturanummer.
1. Fuldfør angivelsen af kreditorfakturaen, og bogfør den.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
