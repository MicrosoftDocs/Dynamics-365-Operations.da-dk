---
title: Indstillinger for POS-program og brugersprog
description: "Dette emne beskriver, hvordan du ændrer indstillinger for sprog i Retail Modern POS (MPOS) og Cloud POS."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: a9b2d8dec04ed3653b2ebcfbd2492fc40d96b77b
ms.contentlocale: da-dk
ms.lasthandoff: 06/29/2017



---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="dfae4-103">Indstillinger for POS-program og brugersprog</span><span class="sxs-lookup"><span data-stu-id="dfae4-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="dfae4-104">Dette emne beskriver, hvordan du ændrer indstillinger for sprog i Retail Modern POS (MPOS) og Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="dfae4-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="dfae4-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="dfae4-105">Overview</span></span>
========

<span data-ttu-id="dfae4-106">Retail Modern POS (MPOS) og Cloud POS understøtter miljøer, hvor indstillinger for sprog og oversættelser kan variere mellem butikken og brugerindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="dfae4-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="dfae4-107">Butikken kunne for eksempel være placeret i et område, hvor engelsk er mest almindelige for deres kunder, men nogle arbejdere foretrækker at bruge programmet med franske oversættelser.</span><span class="sxs-lookup"><span data-stu-id="dfae4-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="dfae4-108">Datasprog</span><span class="sxs-lookup"><span data-stu-id="dfae4-108">Data language</span></span>
<span data-ttu-id="dfae4-109">Uanset brugerens indstillinger bruger MPOS og sky POS altid butikkens sprogindstillinger til at bestemme de oversættelser, der bruges til data.</span><span class="sxs-lookup"><span data-stu-id="dfae4-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="dfae4-110">Dette sikrer, at alle brugere og kunder får en ensartet oplevelse.</span><span class="sxs-lookup"><span data-stu-id="dfae4-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="dfae4-111">Eksempler på data omfatter:</span><span class="sxs-lookup"><span data-stu-id="dfae4-111">Examples of data include:</span></span>

-   <span data-ttu-id="dfae4-112">Produkter</span><span class="sxs-lookup"><span data-stu-id="dfae4-112">Products</span></span>
-   <span data-ttu-id="dfae4-113">Attributter og værdier</span><span class="sxs-lookup"><span data-stu-id="dfae4-113">Attributes and values</span></span>
-   <span data-ttu-id="dfae4-114">Kategorinavne</span><span class="sxs-lookup"><span data-stu-id="dfae4-114">Category names</span></span>
-   <span data-ttu-id="dfae4-115">Transaktionskvitteringer, der er udskrevet eller sendt på mail</span><span class="sxs-lookup"><span data-stu-id="dfae4-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="dfae4-116">Navne på betalingsmetoder</span><span class="sxs-lookup"><span data-stu-id="dfae4-116">Payment method names</span></span>
-   <span data-ttu-id="dfae4-117">Linjevisningsmeddelelser</span><span class="sxs-lookup"><span data-stu-id="dfae4-117">Line display messages</span></span>

<span data-ttu-id="dfae4-118">Butikkens sprog bruges også til de hoved POS-logonskærmen, da brugeren ikke er kendt, inden du logger på.</span><span class="sxs-lookup"><span data-stu-id="dfae4-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="dfae4-119">Hvis en oversættelse ikke er tilgængelig for butikkens sprog, gendannes POS til virksomhedens sprog.</span><span class="sxs-lookup"><span data-stu-id="dfae4-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="dfae4-120">Konfigurere butikkens sprogindstilling</span><span class="sxs-lookup"><span data-stu-id="dfae4-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="dfae4-121">Butikkens sprogindstilling er angivet fra **Alle detailbutikker** på siden **Detailbutik** under **Generelt &gt; Internationale indstillinger &gt; Sprog.</span><span class="sxs-lookup"><span data-stu-id="dfae4-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="dfae4-122">**Brug rullelisten til at vælge sproget for hver butik.</span><span class="sxs-lookup"><span data-stu-id="dfae4-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="dfae4-123">Sprog i brugergrænseflade</span><span class="sxs-lookup"><span data-stu-id="dfae4-123">User interface language</span></span>
<span data-ttu-id="dfae4-124">POS-brugerens sprogindstilling bestemmer de oversættelser, der bruges i programmets brugergrænseflade.</span><span class="sxs-lookup"><span data-stu-id="dfae4-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="dfae4-125">Dette omfatter alle etiketter, menuer og lister, der ikke betragtes som data.</span><span class="sxs-lookup"><span data-stu-id="dfae4-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="dfae4-126">Eneste undtagelse er den tekst, der vises på POS-knapmatricer.</span><span class="sxs-lookup"><span data-stu-id="dfae4-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="dfae4-127">Knapmatricer understøtter ikke oversættelser, så de viser altid teksten, der er defineret på knappen.</span><span class="sxs-lookup"><span data-stu-id="dfae4-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="dfae4-128">For at understøtte oversatte knapper skal du kopiere og vedligeholde særskilte knapmatricer og tildele dem til brugerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="dfae4-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="dfae4-129">Konfigurere brugerens sprogindstilling</span><span class="sxs-lookup"><span data-stu-id="dfae4-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="dfae4-130">POS-brugerens sprogindstilling er angivet under **Alle arbejdere** på siden **Arbejder** under **Detail &gt; Sprog**.</span><span class="sxs-lookup"><span data-stu-id="dfae4-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="dfae4-131">Det er ikke angivet under hovedfanen Profil.</span><span class="sxs-lookup"><span data-stu-id="dfae4-131">It is not set on the main Profile tab.</span></span>  <span data-ttu-id="dfae4-132">Denne indstilling bruges ikke af POS.</span><span class="sxs-lookup"><span data-stu-id="dfae4-132">This setting is not used by POS.</span></span> <span data-ttu-id="dfae4-133">Hvis brugerens sprog ikke er angivet, eller det er indstillet til et sprog, hvor oversættelser er ikke tilgængelige, vender POS tilbage til butikkens sprog.</span><span class="sxs-lookup"><span data-stu-id="dfae4-133">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="dfae4-134">** **</span><span class="sxs-lookup"><span data-stu-id="dfae4-134">** **</span></span>       | <span data-ttu-id="dfae4-135">**Sprog i brugergrænseflade** ** **</span><span class="sxs-lookup"><span data-stu-id="dfae4-135">**UI language** ** **</span></span>      | <span data-ttu-id="dfae4-136">**Datasprog (produkter, kvitteringsformater, linjevisning osv.)**</span><span class="sxs-lookup"><span data-stu-id="dfae4-136">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="dfae4-137">**Regnskab**</span><span class="sxs-lookup"><span data-stu-id="dfae4-137">**Company**</span></span> | <span data-ttu-id="dfae4-138">Standard</span><span class="sxs-lookup"><span data-stu-id="dfae4-138">Default</span></span>                    | <span data-ttu-id="dfae4-139">Standard</span><span class="sxs-lookup"><span data-stu-id="dfae4-139">Default</span></span>                                                           |
| <span data-ttu-id="dfae4-140">**Butik**</span><span class="sxs-lookup"><span data-stu-id="dfae4-140">**Store**</span></span>   | <span data-ttu-id="dfae4-141">Tilsidesætter firma</span><span class="sxs-lookup"><span data-stu-id="dfae4-141">Overrides company</span></span>          | <span data-ttu-id="dfae4-142">Tilsidesætter firma</span><span class="sxs-lookup"><span data-stu-id="dfae4-142">Overrides company</span></span>                                                 |
| <span data-ttu-id="dfae4-143">**Bruger**</span><span class="sxs-lookup"><span data-stu-id="dfae4-143">**User**</span></span>    | <span data-ttu-id="dfae4-144">Tilsidesætter butik eller firma</span><span class="sxs-lookup"><span data-stu-id="dfae4-144">Overrides store or company</span></span> | <span data-ttu-id="dfae4-145">Aldrig</span><span class="sxs-lookup"><span data-stu-id="dfae4-145">Never</span></span>                                                             |






