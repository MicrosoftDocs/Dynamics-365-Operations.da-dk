---
title: Konfigurere en betalingsmetode for ISO20022-kreditoverførsler
description: Denne procedure viser, hvordan du kan konfigurere kreditorbetalingsmåden for ISO20022-kreditoverførsel eller en anden betalingstype ved hjælp af elektronisk rapportering for at generere en fil.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ae91ce361ab3e4e799ec82ca9e05c9e11d81ed1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256564"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="643c6-103">Konfigurere en betalingsmetode for ISO20022-kreditoverførsler</span><span class="sxs-lookup"><span data-stu-id="643c6-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="643c6-104">Denne procedure viser, hvordan du kan konfigurere kreditorbetalingsmåden for ISO20022-kreditoverførsel eller en anden betalingstype ved hjælp af elektronisk rapportering for at generere en fil.</span><span class="sxs-lookup"><span data-stu-id="643c6-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="643c6-105">Før du udfører denne opgave, skal du konfigurere eksportformatkonfigurationer og betalingskonti.</span><span class="sxs-lookup"><span data-stu-id="643c6-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="643c6-106">Denne opgave blev oprettet ved hjælp af DEMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="643c6-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="643c6-107">Det er den tredje procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="643c6-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="643c6-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="643c6-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="643c6-109">Gå til Kreditor > Opsætning af betaling > Betalingsmåder.</span><span class="sxs-lookup"><span data-stu-id="643c6-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="643c6-110">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="643c6-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="643c6-111">Filtrer f.eks. efter feltet Betalingsmåde med værdien "SEPA CT".</span><span class="sxs-lookup"><span data-stu-id="643c6-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="643c6-112">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="643c6-112">Click Edit.</span></span>
4. <span data-ttu-id="643c6-113">Vælg "Total" i feltet Periode.</span><span class="sxs-lookup"><span data-stu-id="643c6-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="643c6-114">Vælg Elektronisk betaling i feltet Betalingstype.</span><span class="sxs-lookup"><span data-stu-id="643c6-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="643c6-115">Udvid sektionen Filformater.</span><span class="sxs-lookup"><span data-stu-id="643c6-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="643c6-116">Vælg Ja i feltet Generisk elektronisk indberetning.</span><span class="sxs-lookup"><span data-stu-id="643c6-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="643c6-117">Skriv eller vælg en værdi i feltet Eksportér formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="643c6-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="643c6-118">Vælg værdien ISO20022-overførsel (DE) på listen.</span><span class="sxs-lookup"><span data-stu-id="643c6-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="643c6-119">Hvis listen er tom, betyder det, at der ikke er nogen importeret og aktiv eksportformatkonfiguration for kreditorbetaling.</span><span class="sxs-lookup"><span data-stu-id="643c6-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="643c6-120">Vælg "Bank" i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="643c6-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="643c6-121">I feltet Betalingskonto skal du specificere værdierne "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="643c6-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="643c6-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="643c6-122">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]