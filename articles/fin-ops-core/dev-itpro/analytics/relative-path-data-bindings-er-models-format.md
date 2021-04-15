---
title: Brug en relativ sti i databindinger for ER-modeller og -formater
description: ER-værktøjet (Electronic Reporting) giver dig mulighed for at definere elektroniske formatstrukturer og derefter beskrive, hvordan disse strukturer skal udfyldes.
author: NickSelin
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 141d58c2183c386584b0b974f4997e7a81ef3109
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749980"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="9722f-103">Brug en relativ sti i databindinger for ER-modeller og -formater</span><span class="sxs-lookup"><span data-stu-id="9722f-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9722f-104">ER-værktøjet (Electronic Reporting) giver brugerne mulighed for at definere elektroniske formatstrukturer og derefter beskrive, hvordan disse strukturer skal udfyldes ved hjælp af de data og algoritmer, der findes i programmet.</span><span class="sxs-lookup"><span data-stu-id="9722f-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in the application.</span></span> <span data-ttu-id="9722f-105">Du kan finde flere oplysninger under [Oprette ER-konfigurationer (Electronic reporting)](electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="9722f-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="9722f-106">Hvis du vil angive dataflowet til hentning af Finance and Operations-data og bruge dem til at generere et elektronisk dokument, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="9722f-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="9722f-107">Bind konfigurerede datakilder til elementer i den domænespecifikke datamodel, der er designet [datamodel](general-electronic-reporting.md#data-model-and-model-mapping-components).</span><span class="sxs-lookup"><span data-stu-id="9722f-107">Bind configured data sources to elements of the designed domain-specific [data model](general-electronic-reporting.md#data-model-and-model-mapping-components).</span></span> <span data-ttu-id="9722f-108">Modelstrukturen og de valgte datakilder kan være en del af en kompleks hierarkisk struktur.</span><span class="sxs-lookup"><span data-stu-id="9722f-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="9722f-109">Derfor kan endelige bindinger være temmelig store og indeholde mange elementer af forskellige typer (f.eks. relationer, tabeller og metoder).</span><span class="sxs-lookup"><span data-stu-id="9722f-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="9722f-110">Bindingerne kan blive mindre læselige og ret komplekse at gennemgå og forstå, især for ikke-ejere.</span><span class="sxs-lookup"><span data-stu-id="9722f-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="9722f-111">Bind datamodelelementer med [formateringskomponenter](general-electronic-reporting.md#FormatComponentOutbound) for at definere, hvilke data der udfyldes fra datamodellen til det genererede output.</span><span class="sxs-lookup"><span data-stu-id="9722f-111">Bind data model elements with [format](general-electronic-reporting.md#FormatComponentOutbound) components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="9722f-112">Hvis du vil forbedre anvendeligheden af ER-tilknytningsdesignere, er funktionen [relativ sti](er-formula-language.md#relative-path) blevet udgivet.</span><span class="sxs-lookup"><span data-stu-id="9722f-112">To improve usability of ER mapping designers, the [relative path](er-formula-language.md#relative-path) feature has been released.</span></span> <span data-ttu-id="9722f-113">Indstillingen for gengivelsen af den relative sti er som standard slået til for alle nye forekomster af programmet, hvor ER-designoplevelsen er aktiveret (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="9722f-113">By default, the relative path representation option is turned on for any new instance of the application where ER design experience is enabled (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="9722f-114">Vi har implementeret den relative sti, så brugerne kan fortsætte med at bruge den fulde sti, når arbejdet med denne præsentation med ER-bindinger.</span><span class="sxs-lookup"><span data-stu-id="9722f-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="9722f-115">[![Brugerparametre](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="9722f-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="9722f-116">Når parameteren for brug af den relative sti er slået til, erstatter et enkelt @-tegn stien til det overordnede element i bindingen for det aktuelle modelelement.</span><span class="sxs-lookup"><span data-stu-id="9722f-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="9722f-117">Hele bindingsstien bliver kortere, hvilket gør hele tilknytningen mere tydelig og nemmere at forstå.</span><span class="sxs-lookup"><span data-stu-id="9722f-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="9722f-118">I de fleste tilfælde er det ikke nødvendigt at rulle yderligere i ER-designeren for at få vist alle bindingerne i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="9722f-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="9722f-119">[![Modeltilknytningsdesigner](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="9722f-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="9722f-120">Når du går i gang med at designe et nyt ER-udtryk, skal du kun angive ét tegn for at definere en binding til et felt af i overordnede element.</span><span class="sxs-lookup"><span data-stu-id="9722f-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="9722f-121">[![Formeldesigner](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="9722f-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="9722f-122">Når du vælger at ændre datakilden for det overordnede modelelement med den absolutte sti, skal du manuelt binde dette modelelement samt alle indlejrede elementer til en ny datakilde.</span><span class="sxs-lookup"><span data-stu-id="9722f-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="9722f-123">Når en relativ sti er aktiveret, og du vælger en ny datakilde, der skal bindes til et overordnet element, får du mulighed for automatisk at binde alle indlejrede elementer i dette overordnede element sammen med et enkelt klik.</span><span class="sxs-lookup"><span data-stu-id="9722f-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="9722f-124">[![Erstat eksisterende stimeddelelse](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="9722f-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="9722f-125">Hvis du bekræfter genbinding af af indlejrede elementer, placeres det nye overordnede element på stien for alle de indlejrede elementer, der indeholder det eksisterende overordnede element.</span><span class="sxs-lookup"><span data-stu-id="9722f-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="9722f-126">Denne funktion bryder ikke bagud-kompatibiliteten for ER-strukturen.</span><span class="sxs-lookup"><span data-stu-id="9722f-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="9722f-127">Alle tidligere designede ER-konfigurationer vil fungere med denne nye funktion, og der kræves ingen opgraderinger eller konverteringer.</span><span class="sxs-lookup"><span data-stu-id="9722f-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="9722f-128">Alle de ændringer, der introduceres ved masseændring af bindinger af indlejrede elementer i modeltilknytninger, gemmes korrekt i et konfigurationsdelta (sporing af ændringer).</span><span class="sxs-lookup"><span data-stu-id="9722f-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="9722f-129">Det giver kunderne mulighed for at basere den afledte version af modeltilknytninger på en hvilken som helst ny basisversion af den, der er ændret, ved hjælp af denne nye funktion.</span><span class="sxs-lookup"><span data-stu-id="9722f-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9722f-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9722f-130">Additional resources</span></span>

[<span data-ttu-id="9722f-131">ER-formelsprog</span><span class="sxs-lookup"><span data-stu-id="9722f-131">ER formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]