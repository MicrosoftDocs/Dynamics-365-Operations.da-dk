---
title: Du kan ikke anvende en skabelon på et frigivet produkt
description: Du kan ikke anvende en skabelon på et frigivet produkt.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026364"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="97cb0-103">Du kan ikke anvende en skabelon til at oprette et frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="97cb0-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="97cb0-104">KB-nummer: 4612097</span><span class="sxs-lookup"><span data-stu-id="97cb0-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="97cb0-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="97cb0-105">Symptoms</span></span>

<span data-ttu-id="97cb0-106">Når du opretter et nyt frigivet produkt ved hjælp af dialogboksen **Nyt frigivet produkt**, kan du vælge en skabelon.</span><span class="sxs-lookup"><span data-stu-id="97cb0-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="97cb0-107">Skabelonen skal indeholde standardindstillinger for mange felter i det nye frigivne produkt.</span><span class="sxs-lookup"><span data-stu-id="97cb0-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="97cb0-108">Nogle eller alle felter er dog ikke indstillet, når du har valgt skabelonen.</span><span class="sxs-lookup"><span data-stu-id="97cb0-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="97cb0-109">Årsag</span><span class="sxs-lookup"><span data-stu-id="97cb0-109">Cause</span></span>

<span data-ttu-id="97cb0-110">På mange sider i Microsoft Dynamics 365 Supply Chain Management kan du oprette en skabelon, der fastlægger de første indstillinger for de poster, der vises på disse sider.</span><span class="sxs-lookup"><span data-stu-id="97cb0-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="97cb0-111">Du kan oprette en af disse skabeloner ved at vælge **Postoplysninger** under fanen **Indstillinger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="97cb0-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="97cb0-112">Frigivne produkter er dog meget mere komplekse end de fleste andre typer poster.</span><span class="sxs-lookup"><span data-stu-id="97cb0-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="97cb0-113">Du kan vælge **Postoplysninger** på siden **Frigivne produkter** for at oprette en skabelon, og selvom du kan vælge denne skabelon, når du opretter et frigivet produkt, indeholder skabelonen ikke de forventede feltværdier for det nye frigivne produkt.</span><span class="sxs-lookup"><span data-stu-id="97cb0-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="97cb0-114">Derfor kan du ikke bruge skabeloner med "postoplysninger" til frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="97cb0-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="97cb0-115">Du skal i stedet oprette dedikerede produktskabeloner.</span><span class="sxs-lookup"><span data-stu-id="97cb0-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="97cb0-116">Løsning</span><span class="sxs-lookup"><span data-stu-id="97cb0-116">Resolution</span></span>

<span data-ttu-id="97cb0-117">Når du vil oprette en produktskabelon, skal du bruge menuen **Skabelon** under fanen **Produkt** i handlingsruden og ikke knappen **Postoplysninger** under fanen **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="97cb0-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="97cb0-118">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="97cb0-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="97cb0-119">Vælg **Skabelon** under fanen **Produkt** i gruppen **Ny** i handlingsruden, og vælg derefter enten **Opret personlig skabelon** eller **Opret delt skabelon** efter behov.</span><span class="sxs-lookup"><span data-stu-id="97cb0-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
