---
title: Arkivér udskrevne debitorfakturaer med hash-numre
description: Dette emne forklarer, hvordan du aktiverer arkivering for at gemme udskrevne kundefakturaer med hash-numre.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018972"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="3c97f-103">Arkivér udskrevne debitorfakturaer med hash-numre</span><span class="sxs-lookup"><span data-stu-id="3c97f-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="3c97f-104">I nogle lande er der et juridisk krav om at gemme beregnede hash-numre i systemet sammen med udskrifter af visse dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3c97f-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="3c97f-105">Hash-numre kan bruges til rapportering til myndigheder og under revisioner.</span><span class="sxs-lookup"><span data-stu-id="3c97f-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="3c97f-106">Dette emne forklarer, hvordan du konfigurere arkivering for at gemme udskrevne kundefakturaer med hash-numre.</span><span class="sxs-lookup"><span data-stu-id="3c97f-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3c97f-107">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="3c97f-107">Prerequisites</span></span>

- <span data-ttu-id="3c97f-108">I arbejdsområdet **Funktionsstyring** aktiveres funktionen **Arkivér udskrevne kundefakturaer med hash-numre**.</span><span class="sxs-lookup"><span data-stu-id="3c97f-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="3c97f-109">Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3c97f-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="3c97f-110">Konfigurer de formater, de kan udskrives af de ønskede dokumenter i **Udskriftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="3c97f-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="3c97f-111">Denne funktionalitet kan anvendes på følgende dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3c97f-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="3c97f-112">**Debitor**</span><span class="sxs-lookup"><span data-stu-id="3c97f-112">**Accounts receivable**</span></span>
- <span data-ttu-id="3c97f-113">Debitorfaktura</span><span class="sxs-lookup"><span data-stu-id="3c97f-113">Customer invoice</span></span>
- <span data-ttu-id="3c97f-114">Kreditnota til kunden</span><span class="sxs-lookup"><span data-stu-id="3c97f-114">Customer credit note</span></span>
- <span data-ttu-id="3c97f-115">Fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="3c97f-115">Free text invoice</span></span>
- <span data-ttu-id="3c97f-116">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="3c97f-116">Free text credit note</span></span>

<span data-ttu-id="3c97f-117">**Projektstyring og regnskab**</span><span class="sxs-lookup"><span data-stu-id="3c97f-117">**Project management and accounting**</span></span>
- <span data-ttu-id="3c97f-118">Projektfaktura</span><span class="sxs-lookup"><span data-stu-id="3c97f-118">Project invoice</span></span>
- <span data-ttu-id="3c97f-119">Projektkreditnota</span><span class="sxs-lookup"><span data-stu-id="3c97f-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="3c97f-120">Konfigurer kundemasterdata</span><span class="sxs-lookup"><span data-stu-id="3c97f-120">Configure customer master data</span></span>
<span data-ttu-id="3c97f-121">Gennemfør følgende trin for at konfigurere kundedata, og aktivfør muligheden for automatisk at gemme udskrevne fakturaer som vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="3c97f-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="3c97f-122">Gå til **Debitor** > **Alle debitorer**.</span><span class="sxs-lookup"><span data-stu-id="3c97f-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="3c97f-123">Vælg en debitor, og i oversigtsfeltet **Faktura og levering** i sektionen **E-FAKTURA** i feltet **Vedhæftet til e-faktura** vælges **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3c97f-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="3c97f-124">Udskriv fakturaer</span><span class="sxs-lookup"><span data-stu-id="3c97f-124">Print invoices</span></span>
<span data-ttu-id="3c97f-125">Du kan bogføre og udskrive en hvilken som helst fritekst-, debitor- og projektfaktura eller -kreditnota for kunden, som er konfigureret i den forrige procedure.</span><span class="sxs-lookup"><span data-stu-id="3c97f-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="3c97f-126">Åbn siden **Vedhæftede filer** for den udskrevne faktura.</span><span class="sxs-lookup"><span data-stu-id="3c97f-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="3c97f-127">I oversigtsfeltet **Vedhæftede filer** i feltgruppen **Yderligere detaljer** i feltet **Hash-nummer til dokument** skal du finde det gemte hash-nummer, der er beregnet til den udskrevne faktura.</span><span class="sxs-lookup"><span data-stu-id="3c97f-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Hash-nummer på vedhæftet fil](media/attach-hash-num.jpg)

