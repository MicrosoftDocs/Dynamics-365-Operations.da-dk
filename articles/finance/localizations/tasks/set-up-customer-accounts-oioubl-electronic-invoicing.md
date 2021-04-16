---
title: Konfigurere debitorkonti til elektronisk OIOUBL-fakturering
description: Denne opgave gennemgår, hvordan du konfigurerer en debitorkonto for elektronisk OIOUBL fakturering.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, RegNumTaxIdLookup, smmContactPerson, DirPartyLookup, ContactPersonLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31e588d97b299f674a33193fe9e25b5b731536ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819442"
---
# <a name="set-up-customer-accounts-for-oioubl-electronic-invoicing"></a><span data-ttu-id="2a98f-103">Konfigurere debitorkonti til elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="2a98f-103">Set up customer accounts for OIOUBL electronic invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a98f-104">Denne opgave gennemgår, hvordan du konfigurerer en debitorkonto for elektronisk OIOUBL fakturering.</span><span class="sxs-lookup"><span data-stu-id="2a98f-104">This task walks you through how to set up a customer account for OIOUBL electronic invoicing.</span></span> 



<span data-ttu-id="2a98f-105">Denne opgave blev oprettet ved hjælp af demodatafirmaet USMF med landet/området i den juridiske enheds primære adresse opdateret til Danmark.</span><span class="sxs-lookup"><span data-stu-id="2a98f-105">This task was created using the demo data company USMF with the country/region of legal entity primary address updated to be Denmark.</span></span>



<span data-ttu-id="2a98f-106">Det er den tredje af seks procedurer, der viser processen til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="2a98f-106">This is the third procedure, out of six, that demonstrates the process of generating e-invoices using electronic reporting configurations.</span></span> <span data-ttu-id="2a98f-107">Denne opgave bruger eksemplet med OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge.</span><span class="sxs-lookup"><span data-stu-id="2a98f-107">This task uses the OIOUBL e-invoice example which is common for Denmark, Austria, and Norway.</span></span>

1. <span data-ttu-id="2a98f-108">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="2a98f-108">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="2a98f-109">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="2a98f-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2a98f-110">Filtrer f.eks. efter feltet Konto med værdien "US-023".</span><span class="sxs-lookup"><span data-stu-id="2a98f-110">For example, filter on the Account field with a value of 'US-023'.</span></span>
3. <span data-ttu-id="2a98f-111">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="2a98f-111">Click Edit.</span></span>
4. <span data-ttu-id="2a98f-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2a98f-112">In the list, click the link in the selected row.</span></span>

## <a name="enable-a-customer-account-for-oioubl-electronic-invoicing"></a><span data-ttu-id="2a98f-113">Aktivere en debitorkonto til elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="2a98f-113">Enable a customer account for OIOUBL electronic invoicing</span></span>
1. <span data-ttu-id="2a98f-114">Udvid sektionen Faktura og levering.</span><span class="sxs-lookup"><span data-stu-id="2a98f-114">Expand the Invoice and delivery section.</span></span>
2. <span data-ttu-id="2a98f-115">Indtast eller vælg en værdi i feltet SE-nummer.</span><span class="sxs-lookup"><span data-stu-id="2a98f-115">In the Tax exempt number field, enter or select a value.</span></span>
3. <span data-ttu-id="2a98f-116">Vælg Ja i feltet eFaktura.</span><span class="sxs-lookup"><span data-stu-id="2a98f-116">Select Yes in the eInvoice field.</span></span>
4. <span data-ttu-id="2a98f-117">Skriv en værdi i feltet EAN.</span><span class="sxs-lookup"><span data-stu-id="2a98f-117">In the EAN field, type a value.</span></span> <span data-ttu-id="2a98f-118">For eksempel "5798000362147".</span><span class="sxs-lookup"><span data-stu-id="2a98f-118">For example '5798000362147'..</span></span>

## <a name="set-up-contact-information-for-a-customer"></a><span data-ttu-id="2a98f-119">Konfigurer kontaktoplysninger for en kunde</span><span class="sxs-lookup"><span data-stu-id="2a98f-119">Set up contact information for a customer</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]