---
title: Bogføringskonti for anskaffelse af anlægsaktiver
description: I denne artikel beskrives det, hvordan du konfigurerer finansbogføringskonti til anskaffelse af anlægsaktiver.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8fea6b1cd79b5536341a7cb50e5592ea38a7392d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441496"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="ce54c-103">Bogføringskonti for anskaffelse af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="ce54c-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce54c-104">I denne artikel beskrives det, hvordan du konfigurerer finansbogføringskonti til anskaffelse af anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="ce54c-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="ce54c-105">Konti, der bruges til at bogføre anskaffelser af anlægsaktiver kan variere afhængigt af den metode, der bruges til at anskaffe aktivet.</span><span class="sxs-lookup"><span data-stu-id="ce54c-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="ce54c-106">På siden Posteringsprofiler for anlægsaktiver under fanen Finans skal du vælge Anskaffelse og Anskaffelsesregulering for at konfigurere konti til anlægsaktiver, der skal bogføres i Finans.</span><span class="sxs-lookup"><span data-stu-id="ce54c-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="ce54c-107">I kladder og på indkøbsordrer er finanskontoen normalt den statuskonto, hvor det nye anlægsaktivs anskaffelsesværdi debiteres.</span><span class="sxs-lookup"><span data-stu-id="ce54c-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="ce54c-108">Denne konto kan ikke ses i kladden og kan ikke erstattes under posteringer.</span><span class="sxs-lookup"><span data-stu-id="ce54c-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="ce54c-109">Modkonto er ligeledes en statuskonto.</span><span class="sxs-lookup"><span data-stu-id="ce54c-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="ce54c-110">I finanskladden og anlægsaktivkladden er denne konto ofte den bankkonto, der bruges til at betale for anskaffelsen af anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="ce54c-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="ce54c-111">Modkontoen er en standardkonto, der foreslås automatisk i kladderne.</span><span class="sxs-lookup"><span data-stu-id="ce54c-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="ce54c-112">Den kan ændres i kladden til en hvilken som helst anden konto fra kontoplanen eller til en kreditorkonto, hvis anlægsaktivet er købt hos en leverandør.</span><span class="sxs-lookup"><span data-stu-id="ce54c-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="ce54c-113">Når Fakturajournal eller Indkøbsordrer i Kreditor bruges til anskaffelse af anlægsaktiver, erstattes modkontoen for anlægsaktivposteringen med den kreditorkonto, der er valgt til posteringen.</span><span class="sxs-lookup"><span data-stu-id="ce54c-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="ce54c-114">For anskaffelser, der bogføres vha. kladden Lager til anlægsaktiver i Finans, købes anlægsaktivet ikke fra eksterne kilder, men overføres fra firmaets eget lager.</span><span class="sxs-lookup"><span data-stu-id="ce54c-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="ce54c-115">Derfor er modkontoen en lagerafgangskonto for lagervaren i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="ce54c-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="ce54c-116">Du kan finde flere oplysninger under [Anskaffelse af aktiver via indkøb](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="ce54c-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>



