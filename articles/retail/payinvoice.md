---
title: Konfigurer betalingsfakturascenarier
description: "I dette emne beskrives, hvordan du kan konfigurere Dynamics 365 for Retail til at understøtte forskellige scenarier relateret til fakturabetalinger."
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.contentlocale: da-dk
ms.lasthandoff: 01/04/2019

---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="b1cf9-103">Konfigurer betalingsfakturascenarier</span><span class="sxs-lookup"><span data-stu-id="b1cf9-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b1cf9-104">Funktionen Betale en faktura i Dynamics 365 for Retail er blevet udvidet for at understøtte:</span><span class="sxs-lookup"><span data-stu-id="b1cf9-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>

- <span data-ttu-id="b1cf9-105">Udbetaling af flere salgsordrefakturaer i en enkelt POS-transaktion.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="b1cf9-106">Betaling af forskellige debitorfakturatyper, herunder fritekstfakturaer, projektbaserede fakturaer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="b1cf9-107">Hvis du vil aktivere disse scenarier, skal funktionalitetsprofilen for butikker være konfigureret som beskrevet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="b1cf9-108">Gå til **Detail \> Konfiguration af kanal \> POS setup \> POS-profiler \> Funktionalitetsprofiler**, og vælg en profil, der er knyttet til de butikker, som du vil foretage ændringerne for.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-108">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="b1cf9-109">På fanen **Funktioner** kan du konfigurere følgende parametre efter behov.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="b1cf9-110">**Salgsordrefaktura** – Vælg **Ja** for at give brugere mulighed for at betale en eller flere salgsordrebaserede fakturaer i en enkelt POS-transaktion.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="b1cf9-111">**Fritekstfaktura** – Vælg **Ja** for at give brugere mulighed for at betale en eller flere fritekstbaserede fakturaer i en enkelt POS-transaktion.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="b1cf9-112">**Projektfaktura** – Vælg **Ja** for at give brugerne mulighed for at betale en eller flere projektbaserede fakturaer i en enkelt POS-transaktion.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="b1cf9-113">**Salgsordre kreditnota** – Vælg **Ja** for at tillade brugere at udligne flere salgsordrebaserede kreditnotaer i forhold til åbne fakturaer eller behandle en refusion til kunden for en åben kreditnota.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="b1cf9-114">Betaling eller udligning af delbeløb understøttes ikke endnu.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-114">Payment or settlement of partial amounts is not yet supported.</span></span>

