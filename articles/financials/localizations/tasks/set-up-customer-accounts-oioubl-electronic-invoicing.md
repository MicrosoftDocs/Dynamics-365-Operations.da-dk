---
title: Konfigurere debitorkonti til elektronisk OIOUBL-fakturering
description: Denne opgave gennemgår, hvordan du konfigurerer en debitorkonto for elektronisk OIOUBL fakturering.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, RegNumTaxIdLookup, smmContactPerson, DirPartyLookup, ContactPersonLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 188a25210fcbb62b71d69c40cd49b8262128a1c5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "370288"
---
# <a name="set-up-customer-accounts-for-oioubl-electronic-invoicing"></a><span data-ttu-id="d2527-103">Konfigurere debitorkonti til elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="d2527-103">Set up customer accounts for OIOUBL electronic invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2527-104">Denne opgave gennemgår, hvordan du konfigurerer en debitorkonto for elektronisk OIOUBL fakturering.</span><span class="sxs-lookup"><span data-stu-id="d2527-104">This task walks you through how to set up a customer account for OIOUBL electronic invoicing.</span></span> 



<span data-ttu-id="d2527-105">Denne opgave blev oprettet ved hjælp af demodatafirmaet USMF med landet/området i den juridiske enheds primære adresse opdateret til Danmark.</span><span class="sxs-lookup"><span data-stu-id="d2527-105">This task was created using the demo data company USMF with the country/region of legal entity primary address updated to be Denmark.</span></span>



<span data-ttu-id="d2527-106">Det er den tredje af seks procedurer, der viser processen til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="d2527-106">This is the third procedure, out of six, that demonstrates the process of generating e-invoices using electronic reporting configurations.</span></span> <span data-ttu-id="d2527-107">Denne opgave bruger eksemplet med OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge.</span><span class="sxs-lookup"><span data-stu-id="d2527-107">This task uses the OIOUBL e-invoice example which is common for Denmark, Austria, and Norway.</span></span>

1. <span data-ttu-id="d2527-108">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="d2527-108">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="d2527-109">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="d2527-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d2527-110">Filtrer f.eks. efter feltet Konto med værdien "US-023".</span><span class="sxs-lookup"><span data-stu-id="d2527-110">For example, filter on the Account field with a value of 'US-023'.</span></span>
3. <span data-ttu-id="d2527-111">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d2527-111">Click Edit.</span></span>
4. <span data-ttu-id="d2527-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d2527-112">In the list, click the link in the selected row.</span></span>

## <a name="enable-a-customer-account-for-oioubl-electronic-invoicing"></a><span data-ttu-id="d2527-113">Aktivere en debitorkonto til elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="d2527-113">Enable a customer account for OIOUBL electronic invoicing</span></span>
1. <span data-ttu-id="d2527-114">Udvid sektionen Faktura og levering.</span><span class="sxs-lookup"><span data-stu-id="d2527-114">Expand the Invoice and delivery section.</span></span>
2. <span data-ttu-id="d2527-115">Indtast eller vælg en værdi i feltet SE-nummer.</span><span class="sxs-lookup"><span data-stu-id="d2527-115">In the Tax exempt number field, enter or select a value.</span></span>
3. <span data-ttu-id="d2527-116">Vælg Ja i feltet eFaktura.</span><span class="sxs-lookup"><span data-stu-id="d2527-116">Select Yes in the eInvoice field.</span></span>
4. <span data-ttu-id="d2527-117">Skriv en værdi i feltet EAN.</span><span class="sxs-lookup"><span data-stu-id="d2527-117">In the EAN field, type a value.</span></span> <span data-ttu-id="d2527-118">For eksempel "5798000362147".</span><span class="sxs-lookup"><span data-stu-id="d2527-118">For example '5798000362147'..</span></span>

## <a name="set-up-contact-information-for-a-customer"></a><span data-ttu-id="d2527-119">Konfigurer kontaktoplysninger for en kunde</span><span class="sxs-lookup"><span data-stu-id="d2527-119">Set up contact information for a customer</span></span>

