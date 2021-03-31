---
title: 'Konfigurere afskrivningsmodeller '
description: Denne procedure gennemgår processen med at oprette en ny afskrivningsmodel og knytte den til en anlægsaktivgruppe.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd65cb77872b3e2f74402cf8c92c8b8989cea6ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224687"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="aebcd-103">Konfigurere afskrivningsmodeller </span><span class="sxs-lookup"><span data-stu-id="aebcd-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aebcd-104">Denne procedure gennemgår processen med at oprette en ny afskrivningsmodel og knytte den til en anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="aebcd-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="aebcd-105">Opret en afskrivningsmodel</span><span class="sxs-lookup"><span data-stu-id="aebcd-105">Create a depreciation book</span></span>
1. <span data-ttu-id="aebcd-106">Gå til Anlægsaktiver > Opsætning > Afskrivningsmodeller.</span><span class="sxs-lookup"><span data-stu-id="aebcd-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="aebcd-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="aebcd-107">Click New.</span></span>
3. <span data-ttu-id="aebcd-108">Skriv en værdi i feltet Afskrivningsmodel.</span><span class="sxs-lookup"><span data-stu-id="aebcd-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="aebcd-109">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="aebcd-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="aebcd-110">Markér eller fjern markeringen af afkrydsningsfeltet Beregn afskrivning.</span><span class="sxs-lookup"><span data-stu-id="aebcd-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="aebcd-111">Klik på rullelisten i feltet Afskrivningsprofil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="aebcd-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="aebcd-112">Find og vælg den ønskede afskrivningsprofil på listen.</span><span class="sxs-lookup"><span data-stu-id="aebcd-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="aebcd-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="aebcd-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="aebcd-114">Klik på rullelisten i feltet Alternativ afskrivningsprofil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="aebcd-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="aebcd-115">Vælg den ønskede afskrivningsprofil på listen.</span><span class="sxs-lookup"><span data-stu-id="aebcd-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="aebcd-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="aebcd-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aebcd-117">Afskrivningsprofilen Ekstraordinær bruges som yderligere afskrivningsmetode for et aktiv under usædvanlige omstændigheder.</span><span class="sxs-lookup"><span data-stu-id="aebcd-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="aebcd-118">Du kan f.eks. bruge dette til at registrere afskrivning, der sker som følge af en naturkatastrofe.</span><span class="sxs-lookup"><span data-stu-id="aebcd-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="aebcd-119">Markér eller fjern markeringen af afkrydsningsfeltet Opret reguleringer af afskrivning med basisreguleringer.</span><span class="sxs-lookup"><span data-stu-id="aebcd-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="aebcd-120">Klik på rullelisten i feltet Kalender for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="aebcd-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="aebcd-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="aebcd-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="aebcd-122">Knyt afskrivningsmodellen til en anlægsaktivgruppe</span><span class="sxs-lookup"><span data-stu-id="aebcd-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="aebcd-123">Klik på Anlægsaktivgrupper.</span><span class="sxs-lookup"><span data-stu-id="aebcd-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="aebcd-124">Klik på rullelisten i feltet Anlægsaktivgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="aebcd-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="aebcd-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="aebcd-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="aebcd-126">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="aebcd-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="aebcd-127">Vælg en indstilling i feltet Afskrivningsprincip.</span><span class="sxs-lookup"><span data-stu-id="aebcd-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="aebcd-128">Angiv et tal i feltet Levetid.</span><span class="sxs-lookup"><span data-stu-id="aebcd-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="aebcd-129">Bemærk, at værdien i Afskrivningsperioder beregnes efter angivelse af levetid.</span><span class="sxs-lookup"><span data-stu-id="aebcd-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]