---
title: Opdatere strukturen for en forretningsdokumentskabelon
description: Dette emne forklarer, hvordan du opdaterer strukturen i en skabelon til et forretningsdokument ved hjælp af funktionen til administration af forretningsdokumenter.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: cb0188e372b5f6275472cf040d10bb796eed1858
ms.sourcegitcommit: 95d2fc0fa7d17d3a96f7969f12c985b018b4ff94
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/12/2020
ms.locfileid: "4728083"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="e8389-103">Opdatere strukturen for en forretningsdokumentskabelon</span><span class="sxs-lookup"><span data-stu-id="e8389-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e8389-104">I ruden **Skabelonstruktur** i editoren for skabeloner til [administration af forretningsdokumenter](er-business-document-management.md) kan du redigere en skabelon til forretningsdokumenter ved at [føje nye felter](er-bdm-add-field-to-excel-template.md) til skabelonen i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e8389-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="e8389-105">Skabelonens struktur opdateres derefter automatisk i Dynamics 365 Finance, så den afspejler de ændringer, du har foretaget i ruden **Skabelonstruktur**.</span><span class="sxs-lookup"><span data-stu-id="e8389-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="e8389-106">Du kan også redigere en skabelon ved hjælp af Office 365-onlinefunktioner.</span><span class="sxs-lookup"><span data-stu-id="e8389-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="e8389-107">Du kan f.eks. føje et nyt navngivet element, f.eks. et billede eller en figur, til det redigerbare regneark.</span><span class="sxs-lookup"><span data-stu-id="e8389-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="e8389-108">I dette tilfælde opdateres skabelonens struktur ikke automatisk i Finans, og det element, du har tilføjet, vises ikke i ruden **Skabelonstruktur**.</span><span class="sxs-lookup"><span data-stu-id="e8389-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="e8389-109">Opdater skabelonstrukturen manuelt i Finans ved at vælge **Opdater struktur** på editorsiden for skabelonen.</span><span class="sxs-lookup"><span data-stu-id="e8389-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="e8389-110">Du kan få flere oplysninger om denne funktion ved at udføre følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="e8389-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="e8389-111">Eksempel: Opdatere strukturen for en forretningsdokumentskabelon</span><span class="sxs-lookup"><span data-stu-id="e8389-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="e8389-112">Dette eksempel viser, hvordan en systemadministrator kan opdatere strukturen i en skabelon til et forretningsdokument i Finans, når skabelonen er ændret i Office Online.</span><span class="sxs-lookup"><span data-stu-id="e8389-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="e8389-113">I følgende afsnit beskrives de trin, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="e8389-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="e8389-114">Forberede en skabelon til forretningsdokumenter til redigering</span><span class="sxs-lookup"><span data-stu-id="e8389-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="e8389-115">Gennemfør følgende procedurer i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="e8389-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="e8389-116">Konfigurere ER-parametre</span><span class="sxs-lookup"><span data-stu-id="e8389-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="e8389-117">Importere ER-løsninger</span><span class="sxs-lookup"><span data-stu-id="e8389-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="e8389-118">Aktivere styring af forretningsdokumenter</span><span class="sxs-lookup"><span data-stu-id="e8389-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="e8389-119">Konfigurere parametre</span><span class="sxs-lookup"><span data-stu-id="e8389-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="e8389-120">Redigere en forretningsdokumentskabelon</span><span class="sxs-lookup"><span data-stu-id="e8389-120">Edit a business document template</span></span>

1. <span data-ttu-id="e8389-121">I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.</span><span class="sxs-lookup"><span data-stu-id="e8389-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="e8389-122">Vælg skabelonen **Fritekstfaktura (ER-eksempel) (Excel)** på siden **Opret en ny skabelon**.</span><span class="sxs-lookup"><span data-stu-id="e8389-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="e8389-123">Vælg **Opret dokument**.</span><span class="sxs-lookup"><span data-stu-id="e8389-123">Select **Create document**.</span></span>
4. <span data-ttu-id="e8389-124">I feltet **Titel** skal du angive **FTI-eksempel Litware**.</span><span class="sxs-lookup"><span data-stu-id="e8389-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="e8389-125">Vælg **OK** for at oprette den nye skabelon.</span><span class="sxs-lookup"><span data-stu-id="e8389-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8389-126">Hvis du endnu ikke er logget på Office Online, bliver du [omdirigeret til Office 365-logonsiden](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="e8389-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="e8389-127">Hvis du vil vende tilbage til Finans-miljøet, skal du vælge knappen **Tilbage** i browseren.</span><span class="sxs-lookup"><span data-stu-id="e8389-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="e8389-128">Den nye skabelon åbnes til redigering i det integrerede Excel Online-kontrolelement på editorsiden for skabelonen.</span><span class="sxs-lookup"><span data-stu-id="e8389-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="e8389-129">[![Bruge arbejdsområdet Styring af forretningsdokumenter til at starte redigering af en skabelon til forretningsdokumenter](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="e8389-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="e8389-130">Gennemse den aktuelle struktur i den redigerbare skabelon</span><span class="sxs-lookup"><span data-stu-id="e8389-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="e8389-131">I Excel Online skal du gå til båndet, vælge fanen **Vis** og vælge **Gitterlinjer** i gruppen **Vis**.</span><span class="sxs-lookup"><span data-stu-id="e8389-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="e8389-132">Vælg rektanglet oven over skabelonens titel i den redigerbare skabelon.</span><span class="sxs-lookup"><span data-stu-id="e8389-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="e8389-133">Dette rektangel er et billede med navnet **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="e8389-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="e8389-134">Hvis ruden **Skabelonstruktur** er skjult, skal du vælge **Vis struktur**.</span><span class="sxs-lookup"><span data-stu-id="e8389-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="e8389-135">I ruden **Skabelonstruktur** skal du udvide **Rapport \> Faktura \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="e8389-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="e8389-136">Bemærk, at elementet **rptHeaderCompLogo** i skabelonstrukturen i Finans vises som underordnet element til **Rapport \> Faktura \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="e8389-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="e8389-137">[![Bruge arbejdsområdet Styring af forretningsdokumenter til at gennemse den aktuelle struktur i en redigerbar skabelon](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="e8389-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="e8389-138">Opdatere strukturen for en forretningsdokumentskabelon ved at slette et billede</span><span class="sxs-lookup"><span data-stu-id="e8389-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="e8389-139">Vælg billedet **rptHeaderCompLogo** i den redigerbare skabelon i Excel Online.</span><span class="sxs-lookup"><span data-stu-id="e8389-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="e8389-140">Benyt en af følgende fremgangsmåder for at slette det valgte billede fra den redigerbare skabelon:</span><span class="sxs-lookup"><span data-stu-id="e8389-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="e8389-141">Vælg **Slet**-tasten på tastaturet.</span><span class="sxs-lookup"><span data-stu-id="e8389-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="e8389-142">Vælg og hold nede på (eller højreklik på) billedet, og vælg derefter **Klip**.</span><span class="sxs-lookup"><span data-stu-id="e8389-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8389-143">Elementet **RptHeaderCompLogo** findes i øjeblikket stadig i skabelonstrukturen i Finans, selvom billedet ikke længere er medtaget i Excel-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="e8389-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="e8389-144">Vælg **Opdater struktur** for at synkronisere den redigerbare skabelons struktur i Excel og Finans.</span><span class="sxs-lookup"><span data-stu-id="e8389-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="e8389-145">I ruden **Skabelonstruktur** skal du udvide **Rapport \> Faktura \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="e8389-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="e8389-146">Bemærk, at elementet **rptHeaderCompLogo** ikke længere er medtaget i skabelonstrukturen i Finans.</span><span class="sxs-lookup"><span data-stu-id="e8389-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="e8389-147">[![Bruge arbejdsområdet Styring af forretningsdokumenter til at slette et billede fra en skabelon til forretningsdokumenter](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="e8389-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="e8389-148">Opdatere strukturen for en forretningsdokumentskabelon ved at tilføje et billede</span><span class="sxs-lookup"><span data-stu-id="e8389-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="e8389-149">I Excel Online skal du gå til båndet, vælge fanen **Indsæt** og vælge **Billede** i gruppen **Illustrationer**.</span><span class="sxs-lookup"><span data-stu-id="e8389-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="e8389-150">Vælg **Vælg fil**, gå til det billede, du vil tilføje, markér det, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8389-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="e8389-151">Vælg **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="e8389-151">Select **Insert**.</span></span>
4. <span data-ttu-id="e8389-152">Flyt det nye billede, indtil det er på det rigtige sted.</span><span class="sxs-lookup"><span data-stu-id="e8389-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="e8389-153">Som standard navngiver Excel billedet.</span><span class="sxs-lookup"><span data-stu-id="e8389-153">By default, Excel names the picture.</span></span> <span data-ttu-id="e8389-154">Det kan f.eks. give billedet navnet **Billede 2**.</span><span class="sxs-lookup"><span data-stu-id="e8389-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="e8389-155">Vælg **Opdater struktur** for at synkronisere den redigerbare skabelons struktur i Excel og Finans.</span><span class="sxs-lookup"><span data-stu-id="e8389-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="e8389-156">I ruden **Skabelonstruktur** skal du udvide **Rapport \> Faktura \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="e8389-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="e8389-157">Bemærk, at det nye billede nu er medtaget som et element i skabelonstrukturen i Finans.</span><span class="sxs-lookup"><span data-stu-id="e8389-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="e8389-158">[![Bruge arbejdsområdet Styring af forretningsdokumenter til at føje et billede til en skabelon til forretningsdokumenter](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="e8389-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="e8389-159">Relaterede links</span><span class="sxs-lookup"><span data-stu-id="e8389-159">Related links</span></span>

[<span data-ttu-id="e8389-160">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="e8389-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="e8389-161">Oversigt over styring af forretningsdokumenter</span><span class="sxs-lookup"><span data-stu-id="e8389-161">Business document management overview</span></span>](er-business-document-management.md)
