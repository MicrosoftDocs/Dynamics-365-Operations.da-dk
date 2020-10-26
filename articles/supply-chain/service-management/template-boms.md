---
title: Styklisteskabeloner
description: En styklisteskabelon indeholder en standardiseret liste over komponenter for serviceobjekter, der serviceres regelmæssigt.
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e732f64b389acafee23427594225dfacda71cc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985762"
---
# <a name="template-boms"></a><span data-ttu-id="014b2-103">Styklisteskabeloner</span><span class="sxs-lookup"><span data-stu-id="014b2-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="014b2-104">En styklisteskabelon giver dig en standardiseret liste over komponenter for serviceobjekter, der serviceres regelmæssigt.</span><span class="sxs-lookup"><span data-stu-id="014b2-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="014b2-105">Komponenterne i styklisteskabelonen repræsenterer de enkelte underkomponenter i serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="014b2-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="014b2-106">Ved at anvende en styklisteskabelon på et serviceobjekt kan du registrere de underkomponenter, der er erstattet på serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="014b2-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="014b2-107">Hvis du vil anvende en styklisteskabelon på en serviceaftale eller en serviceordre, skal du knytte den til en serviceobjektrelation.</span><span class="sxs-lookup"><span data-stu-id="014b2-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="014b2-108">Du kan kun anvende én styklisteskabelon på et serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="014b2-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="014b2-109">Oprette en styklisteskabelon</span><span class="sxs-lookup"><span data-stu-id="014b2-109">Create a template BOM</span></span>

<span data-ttu-id="014b2-110">Følgende tabel indeholder oplysninger om de forskellige metoder, du kan bruge til at oprette en styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="014b2-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="014b2-111">Metode</span><span class="sxs-lookup"><span data-stu-id="014b2-111">Method</span></span></p></th>
<th><p><span data-ttu-id="014b2-112">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="014b2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="014b2-113">Produktion</span><span class="sxs-lookup"><span data-stu-id="014b2-113">Production</span></span></p></td>
<td><p><span data-ttu-id="014b2-114">Styklisteskabelonen er baseret på en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="014b2-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="014b2-115">Denne indstilling kan kun anvendes, hvis du arbejder i et produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="014b2-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="014b2-116">Fordelen er, at du har en aktuel og detaljeret liste over de komponenter, der udgør en vare.</span><span class="sxs-lookup"><span data-stu-id="014b2-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="014b2-117">Vare BOM</span><span class="sxs-lookup"><span data-stu-id="014b2-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="014b2-118">Styklisteskabelonen er baseret på en varestykliste.</span><span class="sxs-lookup"><span data-stu-id="014b2-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="014b2-119">I modsætning til produktionsstyklisten er varestyklisten en statisk liste over de komponenter, en vare består af.</span><span class="sxs-lookup"><span data-stu-id="014b2-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="014b2-120">Eksisterende skabelon</span><span class="sxs-lookup"><span data-stu-id="014b2-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="014b2-121">Skabelonen er baseret på en eksisterende styklisteskabelon.</span><span class="sxs-lookup"><span data-stu-id="014b2-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="014b2-122">Manuel</span><span class="sxs-lookup"><span data-stu-id="014b2-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="014b2-123">Hvis du ved, hvilke reservedele der typisk udskiftes i et serviceobjekt, kan du oprette din styklisteskabelon manuelt.</span><span class="sxs-lookup"><span data-stu-id="014b2-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="014b2-124">Med denne metode kan du sikre, at komponenterne i skabelonen afspejler de faktiske krav på arbejdspladsen.</span><span class="sxs-lookup"><span data-stu-id="014b2-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="014b2-125">Anvende en styklisteskabelon på en serviceaftale eller en serviceordre</span><span class="sxs-lookup"><span data-stu-id="014b2-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="014b2-126">Du kan anvende en styklisteskabelon på en serviceaftale, en serviceordre eller begge.</span><span class="sxs-lookup"><span data-stu-id="014b2-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="014b2-127">Serviceaftalen omfatter normalt det langvarige forhold til en kunde.</span><span class="sxs-lookup"><span data-stu-id="014b2-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="014b2-128">Historikken over udskiftninger, der registreres i servicestyklisten, kan med fordel registreres i serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="014b2-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="014b2-129">Du kan også anvende en styklisteskabelon på en serviceordre for at registrere historikken for den service, der er udført på et serviceobjekt.</span><span class="sxs-lookup"><span data-stu-id="014b2-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="014b2-130">Kopiere historikken i en servicestykliste</span><span class="sxs-lookup"><span data-stu-id="014b2-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="014b2-131">Du kan kopiere historikken for en servicestykliste fra én serviceaftale til en anden.</span><span class="sxs-lookup"><span data-stu-id="014b2-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="014b2-132">Ved at kopiere servicehistorikken mellem serviceaftaler kan du registrere udskiftninger for en vare.</span><span class="sxs-lookup"><span data-stu-id="014b2-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="014b2-133">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="014b2-133">**Example**</span></span>

<span data-ttu-id="014b2-134">Du har oprettet en treårig serviceaftale for en kundes bil.</span><span class="sxs-lookup"><span data-stu-id="014b2-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="014b2-135">I denne periode bliver kunden vant til den gode service, som virksomheden yder.</span><span class="sxs-lookup"><span data-stu-id="014b2-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="014b2-136">Så når aftalen udløber, ønsker kunden at indgå en ny.</span><span class="sxs-lookup"><span data-stu-id="014b2-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="014b2-137">Du kan nu forhandle en mere fordelagtig aftale for firmaet.</span><span class="sxs-lookup"><span data-stu-id="014b2-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="014b2-138">Da du kan få brug for registreringen af udskiftede komponenter i fremtiden, kopierer du historikken for servicestyklisten til den nye aftale.</span><span class="sxs-lookup"><span data-stu-id="014b2-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="014b2-139">Redigere styklisteskabelonen</span><span class="sxs-lookup"><span data-stu-id="014b2-139">Modify the template BOM</span></span>

<span data-ttu-id="014b2-140">Hvis der ikke er knyttet en styklisteskabelon til et serviceobjekt, kan du redigere eller slette linjerne i den.</span><span class="sxs-lookup"><span data-stu-id="014b2-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="014b2-141">Når styklisteskabelonen er knyttet til et serviceobjekt, kan du kun redigere den lokale version af styklisten.</span><span class="sxs-lookup"><span data-stu-id="014b2-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="014b2-142">Hvis du vil kopiere opsætningen af en lokal version af styklisteskabelonen, kan du oprette en ny styklisteskabelon baseret på den lokale version.</span><span class="sxs-lookup"><span data-stu-id="014b2-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="014b2-143">Du kan finde flere oplysninger under [Redigere en servicestykliste](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="014b2-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="014b2-144">Hvis du erstatter en vare på styklisten, kan du registrere erstatningen på styklistelinjen i styklistedesigneren.</span><span class="sxs-lookup"><span data-stu-id="014b2-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="014b2-145">Du kan eventuelt oprette en serviceordrelinje for erstatningsobjektet.</span><span class="sxs-lookup"><span data-stu-id="014b2-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="014b2-146">Hvis du opretter en serviceordrelinje, kan du fakturere erstatningsvaren.</span><span class="sxs-lookup"><span data-stu-id="014b2-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="014b2-147">Hvis du ikke opretter en serviceordrelinje for en erstatning, bevares registreringen af erstatningen, så du kan spore serviceobjektets historik.</span><span class="sxs-lookup"><span data-stu-id="014b2-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="014b2-148">Ændre visningen af oplysninger på styklistelinjen</span><span class="sxs-lookup"><span data-stu-id="014b2-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="014b2-149">Du kan ændre visningen af oplysninger for en styklistelinje for alle styklisteskabeloner og servicestyklister.</span><span class="sxs-lookup"><span data-stu-id="014b2-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="014b2-150">Ændringerne anvendes på alle styklisteskabeloner og servicestyklister.</span><span class="sxs-lookup"><span data-stu-id="014b2-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="014b2-151">Dette omfatter de styklister, der er knyttet til serviceobjekter.</span><span class="sxs-lookup"><span data-stu-id="014b2-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="014b2-152">Oprette nummerserier for styklisteskabelonerne</span><span class="sxs-lookup"><span data-stu-id="014b2-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="014b2-153">Hvis du vil bruge styklisteskabeloner, skal du oprette to nummerserier.</span><span class="sxs-lookup"><span data-stu-id="014b2-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="014b2-154">Opret én nummerserie for styklisteskabelonen og én for linjenummeret for styklistehistorikken.</span><span class="sxs-lookup"><span data-stu-id="014b2-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="014b2-155">Nummerserier bruges til at tildele identifikatorer til poster, der kræver dem.</span><span class="sxs-lookup"><span data-stu-id="014b2-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="014b2-156">Før du kan tildele en nummerserie til en styklisteskabelon eller et linjenummer for styklistehistorikken, skal du angive nummerseriekoderne.</span><span class="sxs-lookup"><span data-stu-id="014b2-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="014b2-157">Oprette nummerserier</span><span class="sxs-lookup"><span data-stu-id="014b2-157">Set up number sequences</span></span>

1.  <span data-ttu-id="014b2-158">Opret nummerserier for styklisteskabeloner og linjenummeret for styklistehistorikken på listesiden **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="014b2-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="014b2-159">Klik på **Servicestyring** \> **Opsætning** \> **Parametre for servicestyring**.</span><span class="sxs-lookup"><span data-stu-id="014b2-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="014b2-160">Klik på **Nummerserier**, og vælg derefter en nummerseriekode for de nummerseriereferencer, du oprettede i formularen **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="014b2-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="014b2-161">Luk formen for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="014b2-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="014b2-162">Linjenummeret for styklistehistorikken bruges til at knytte posteringer i styklisteoversigten til en serviceaftale eller serviceordre.</span><span class="sxs-lookup"><span data-stu-id="014b2-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="014b2-163">Nummeret vises ikke i brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="014b2-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="014b2-164">Se også</span><span class="sxs-lookup"><span data-stu-id="014b2-164">See also</span></span>

[<span data-ttu-id="014b2-165">Oprette en styklisteskabelon</span><span class="sxs-lookup"><span data-stu-id="014b2-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="014b2-166">Administrere styklisteskabeloner på objektrelationer</span><span class="sxs-lookup"><span data-stu-id="014b2-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="014b2-167">Redigere en servicestykliste</span><span class="sxs-lookup"><span data-stu-id="014b2-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 


