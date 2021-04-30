---
title: Microsoft Office-brugergrænsefladestil for nyt dokument i styring af forretningsdokumenter
description: Dette emne indeholder oplysninger om, hvordan du kan bruge den nye brugergrænseflade til dokumenter i funktionen Styring af forretningsdokumenter i den elektroniske rapportering (ER).
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881030"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="b1c28-103">Microsoft Office-brugergrænsefladestil for nyt dokument i styring af forretningsdokumenter</span><span class="sxs-lookup"><span data-stu-id="b1c28-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1c28-104">Styring af forretningsdokumenter gør det muligt for erhvervsbrugere at redigere forretningsdokumentskabeloner ved at bruge en Microsoft 365-tjeneste eller det relevante Microsoft Office-skrivebordsprogram.</span><span class="sxs-lookup"><span data-stu-id="b1c28-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="b1c28-105">Redigeringer kan omfatte designændringer eller nye installationer, eller brugerne kan tilføje pladsholdere for at medtage yderligere data uden at skulle ændre kildekoden.</span><span class="sxs-lookup"><span data-stu-id="b1c28-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="b1c28-106">Du kan finde flere oplysninger om, hvordan du arbejder med Styring af forretningsdokumenter, i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="b1c28-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="b1c28-107">Den nye brugergrænseflade er klarere og mere praktisk at bruge.</span><span class="sxs-lookup"><span data-stu-id="b1c28-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="b1c28-108">Området **Forretningsdokument** viser kun de skabeloner, der er tilgængelige for den aktuelle udbyder.</span><span class="sxs-lookup"><span data-stu-id="b1c28-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="b1c28-109">På den tidligere brugergrænseflade har fanen **Skabelon** vist alle de skabeloner, der var tilgængelige for alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="b1c28-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="b1c28-110">Den viste også alle de skabeloner, der blev oprettet og redigeret af enhver bruger, der havde samme rolle.</span><span class="sxs-lookup"><span data-stu-id="b1c28-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="b1c28-111">Knappen **Nyt dokument** giver dig mulighed for at oprette og redigere en skabelon i en formatkonfiguration for elektronisk rapportering (ER), der er leveret af en anden udbyder.</span><span class="sxs-lookup"><span data-stu-id="b1c28-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="b1c28-112">I eksemplet i dette emne er udbyderen Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b1c28-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="b1c28-113">Du kan også oprette en skabelon ved at overføre din egen skabelon i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="b1c28-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="b1c28-114">Videoen [Oprette et nyt forretningsdokument ved hjælp af Styring af forretningsdokumenter](https://youtu.be/gAIYl-mM_pw) (vist ovenfor) er medtaget i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="b1c28-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="b1c28-115">Gøre den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="b1c28-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="b1c28-116">Hvis du vil begynde at bruge den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter, skal du aktivere funktionen **Office-lignende brugergrænsefladeoplevelse for Styring af forretningsdokumenter** i arbejdsområdet **Administration af funktioner**.</span><span class="sxs-lookup"><span data-stu-id="b1c28-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="b1c28-117">Udfør følgende trin for at aktivere denne funktion for alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="b1c28-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="b1c28-118">I arbejdsområdet **Funktionsstyring** under fanen **Alle** skal du vælge funktionen **Office-lignende brugergrænsefladeoplevelse for Styring af forretningsdokumenter** på listen.</span><span class="sxs-lookup"><span data-stu-id="b1c28-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="b1c28-119">Vælg **Aktivér nu** for at aktivere den valgte funktion.</span><span class="sxs-lookup"><span data-stu-id="b1c28-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="b1c28-120">Opdater siden for at få adgang til den nye funktion.</span><span class="sxs-lookup"><span data-stu-id="b1c28-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="b1c28-121">Redigere skabeloner, der ejes af andre udbydere</span><span class="sxs-lookup"><span data-stu-id="b1c28-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="b1c28-122">I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.</span><span class="sxs-lookup"><span data-stu-id="b1c28-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Arbejdsområdet til Styring af forretningsdokumenter](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="b1c28-124">Vælg det dokument, der skal bruges som skabelon, under fanen **Vælg**, og vælg derefter **Opret dokument**.</span><span class="sxs-lookup"><span data-stu-id="b1c28-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Dialogboksen Forretningsdokumenter](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="b1c28-126">I den nye dialogboks skal du i feltet **Titel** ændre titlen efter behov.</span><span class="sxs-lookup"><span data-stu-id="b1c28-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="b1c28-127">Titelteksten bruges til at navngive den nye ER-formatkonfiguration, der oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="b1c28-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="b1c28-128">Kladdeversionen af denne konfiguration (**FTI-debitorrapport (GER) Kopi**) vil indeholde den redigerede skabelon og vil blive brugt til at køre dette ER-format for den aktuelle bruger.</span><span class="sxs-lookup"><span data-stu-id="b1c28-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="b1c28-129">Den oprindelige skabelon fra ER-basisformatkonfigurationen vil blive brugt til at køre dette ER-format for enhver anden bruger.</span><span class="sxs-lookup"><span data-stu-id="b1c28-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="b1c28-130">I feltet **Navn** skal du ændre navnet på den første revision af den redigerbare skabelon, der oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="b1c28-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="b1c28-131">I feltet **Kommentar** skal du opdatere bemærkningerne til revisionen af den redigerbare skabelon, der oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="b1c28-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="b1c28-132">Vælg **OK** for at bekræfte starten af redigeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="b1c28-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dialogboksen Dokumentoprettelse](./media/BDM_overview_new_template3.png)

<span data-ttu-id="b1c28-134">Knappen **Nyt dokument** bruges til at oprette og redigere en skabelon i en ER-formatkonfiguration, der er leveret af en anden udbyder.</span><span class="sxs-lookup"><span data-stu-id="b1c28-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="b1c28-135">I dette eksempel er udbyderen Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b1c28-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="b1c28-136">Når du vælger **Nyt dokument**, kan du se alle de skabeloner, der ejes af den aktuelle udbyder og andre udbydere.</span><span class="sxs-lookup"><span data-stu-id="b1c28-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="b1c28-137">Når du har valgt skabelonen, vil den blive åbnet til redigering.</span><span class="sxs-lookup"><span data-stu-id="b1c28-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="b1c28-138">Den redigerede skabelon gemmes derefter i en ny ER-formatkonfiguration, der genereres automatisk.</span><span class="sxs-lookup"><span data-stu-id="b1c28-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="b1c28-139">Uploade en skabelon, der bruger et eksisterende Excel-format</span><span class="sxs-lookup"><span data-stu-id="b1c28-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="b1c28-140">Følg disse trin for at angive påkrævede oplysninger, før du uploader en skabelon.</span><span class="sxs-lookup"><span data-stu-id="b1c28-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="b1c28-141">I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.</span><span class="sxs-lookup"><span data-stu-id="b1c28-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Arbejdsområdet til Styring af forretningsdokumenter](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="b1c28-143">På siden **Opret en ny skabelon** under fanen **Upload** under fanen **Skabelon** skal du vælge **Gennemse** for at finde og vælge den Excel-fil, du vil bruge som skabelon.</span><span class="sxs-lookup"><span data-stu-id="b1c28-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="b1c28-144">I afsnittet **Skabelon** udfyldes felterne **Titel** og **Beskrivelse** automatisk.</span><span class="sxs-lookup"><span data-stu-id="b1c28-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="b1c28-145">De angiver navnet på og beskrivelsen af den nye ER-formatkonfiguration, der oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="b1c28-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="b1c28-146">Hvis det er nødvendigt, kan du redigere felterne.</span><span class="sxs-lookup"><span data-stu-id="b1c28-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="b1c28-147">Angiv typen af forretningsdokument i feltet **Navn** i sektionen **Dokumenttype**.</span><span class="sxs-lookup"><span data-stu-id="b1c28-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="b1c28-148">Denne værdi bruges til at søge i den korrekte datakilde (det vil sige konfigurationen af ER-modellen).</span><span class="sxs-lookup"><span data-stu-id="b1c28-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Fanen Skabelon](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="b1c28-150">Vælg **Anvend filter** i oversigtspanelet **Filter** under fanen **Datakilde**.</span><span class="sxs-lookup"><span data-stu-id="b1c28-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="b1c28-151">I sektionen **Datakilde** udfyldes feltet **Navn** automatisk, eller du kan vælge en værdi manuelt.</span><span class="sxs-lookup"><span data-stu-id="b1c28-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="b1c28-152">Du kan bruge filteret til at søge efter det relevante datakildenavn ved hjælp af navn, beskrivelse, lande-/områdekode og forretningsdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="b1c28-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Fanen Datakilde](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="b1c28-154">Oversigtspanelet **Filter** bruges til at søge i den korrekte datakilde (det vil sige konfigurationen af ER-modellen).</span><span class="sxs-lookup"><span data-stu-id="b1c28-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="b1c28-155">Du kan redigere alle filterfelter for at finde den datakilde, der passer bedst til det dokument, du uploader.</span><span class="sxs-lookup"><span data-stu-id="b1c28-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="b1c28-156">Betingelserne i oversigtspanelet **Filter** bruges som **ELLER**-betingelser.</span><span class="sxs-lookup"><span data-stu-id="b1c28-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="b1c28-157">Vælg **Registrer automatisk** under fanen **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="b1c28-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="b1c28-158">Feltet **Roddefinition** udfyldes automatisk, eller du kan vælge en værdi manuelt.</span><span class="sxs-lookup"><span data-stu-id="b1c28-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="b1c28-159">Denne fane viser sluttilknytningen for elementerne fra skabelonen og modellen.</span><span class="sxs-lookup"><span data-stu-id="b1c28-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Fanen Tilknytning](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="b1c28-161">Tilknytningen i sektionen **Skabelonstruktur** bruger det fulde match af navne eller beskrivelser i datakilden på brugerens sprog og i cellenavnet i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="b1c28-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="b1c28-162">Vælg **Opret dokument** for at bekræfte, at du vil oprette en skabelon og starte redigeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="b1c28-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="b1c28-163">Yderligere oplysninger finder du i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="b1c28-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="b1c28-164">Hvis der ikke er en udbyder i Elektronisk rapportering, kan du oprette en.</span><span class="sxs-lookup"><span data-stu-id="b1c28-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="b1c28-165">Hvis der ikke findes en aktiv udbyder, kan du vælge at aktivere en.</span><span class="sxs-lookup"><span data-stu-id="b1c28-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="b1c28-166">Hvis du vil oprette en udbyder, skal du ændre navnet på udbyderen i feltet **Navn**, opdatere den nye udbyders internetadresse i feltet **Internetadresse** og vælge **OK** for at bekræfte.</span><span class="sxs-lookup"><span data-stu-id="b1c28-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![Oprette en ny udbyder i BDM](./media/bdm_create_provider.png)
    
- <span data-ttu-id="b1c28-168">Hvis du vil aktivere en eksisterende udbyder, skal du vælge navnet på udbyderen i feltet **Konfigurationsudbyder** og vælge **OK** for at indstille udbyderen til aktiv.</span><span class="sxs-lookup"><span data-stu-id="b1c28-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![Aktivere udbyder i BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="b1c28-170">Hver BDM-skabelon refererer til udbyderen som konfigurations forfatter.</span><span class="sxs-lookup"><span data-stu-id="b1c28-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="b1c28-171">Derfor kræves der en aktiv udbyder for skabelonen.</span><span class="sxs-lookup"><span data-stu-id="b1c28-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
