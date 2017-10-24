---
title: Styring og oprettelse af produktkategori
description: "Dette emne beskriver de forbedringer, der er foretaget af styringsoplevelsen for produktkategorier i Retail. Disse forbedringer giver markedsføringschefer mulighed for at have en korrelation mellem produkthierarki i Retail og oplysninger om frigivne produkter."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 6b9afb40b68b672514c083d99efbc9bd098dd561
ms.openlocfilehash: b158ff5b277c125e0aa158c071007ed8a0f25482
ms.contentlocale: da-dk
ms.lasthandoff: 10/03/2017

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="2dc23-104">Styring og oprettelse af produktkategori</span><span class="sxs-lookup"><span data-stu-id="2dc23-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="2dc23-105">Forbedringer, der er foretaget af styringsoplevelsen for produktkategorier i Retail, giver markedsføringschefer mulighed for at have en korrelation mellem produkthierarki i Retail og oplysninger om frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="2dc23-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="2dc23-106">For at få vist disse forbedringer i arbejdsområdet **Kategori og produktstyring**, skal du vælge **Produkthierarki i Retail** for at åbne siden **Ny struktur i produktkategori i Retail**.</span><span class="sxs-lookup"><span data-stu-id="2dc23-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="2dc23-107">I tidligere versioner var produktegenskaberne inddelt i grundlæggende produktegenskaber og produktegenskaber i Retail, baseret på området for deres anvendelse.</span><span class="sxs-lookup"><span data-stu-id="2dc23-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="2dc23-108">Produktegenskaber i Retail var *globale*.</span><span class="sxs-lookup"><span data-stu-id="2dc23-108">Retail product properties were *global*.</span></span> <span data-ttu-id="2dc23-109">For en bestemt produktegenskab deles den samme værdi med andre ord på tværs af alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="2dc23-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="2dc23-110">Grundlæggende produktegenskaber var *specifikke for juridisk enhed*.</span><span class="sxs-lookup"><span data-stu-id="2dc23-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="2dc23-111">En given produktegenskab kan med andre ord variere på tværs af juridiske enheder baseret på de enkelte forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="2dc23-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="2dc23-112">Med disse forbedringer for produktegenskaber i produktkategorien i Retail vil vi fortsætte med at adskille felterne, baseret på deres anvendelse i en gruppe, for at afspejle detaljeformstrukturen i frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="2dc23-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="2dc23-113">Du kan skifte mellem at administrere specifikke egenskaber for juridisk enhed på tværs af alle juridiske enheder og styre dem for en bestemt juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="2dc23-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="2dc23-114">Du skal blot vælge **Vis/Rediger for alle juridiske enheder** eller **Vis/Rediger for en bestemt juridisk enhed** efter dit behov.</span><span class="sxs-lookup"><span data-stu-id="2dc23-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="2dc23-115">Markedsføringschefer kan også definere standardværdier for et ekstra sæt produktegenskaber på niveauet for en individuel kategori.</span><span class="sxs-lookup"><span data-stu-id="2dc23-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="2dc23-116">Disse egenskabsværdier nedarves af et produkt baseret på deres tilknytning til en kategori på tidspunktet for oprettelse af produktet.</span><span class="sxs-lookup"><span data-stu-id="2dc23-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="2dc23-117">Vælg egenskaber til opdatering af produkter fra kategoriformularen i Retail</span><span class="sxs-lookup"><span data-stu-id="2dc23-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="2dc23-118">Du kan bruge en logisk gruppering af egenskaber til at vælge, hvilke opdaterede produktegenskaber, der skal overføres til tilknyttede produkter.</span><span class="sxs-lookup"><span data-stu-id="2dc23-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="2dc23-119">Markedsføringschefer kan ændre disse nedarvede egenskaber for hvert produkt, for at imødekomme individuelle virksomhedsbehov.</span><span class="sxs-lookup"><span data-stu-id="2dc23-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

