---
title: Underleverandørarbejde
description: Med dette emne kan du opbygge en gennemgang af underleverandørarbejde i produktion i Dynamics 365 Supply Chain Management.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: f771c15d98abe3689054d43cc8b33632121522a3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255535"
---
# <a name="subcontracting"></a><span data-ttu-id="53f93-103">Underleverandørarbejde</span><span class="sxs-lookup"><span data-stu-id="53f93-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53f93-104">Med dette emne kan du opbygge en gennemgang af underleverandørarbejde i produktion i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="53f93-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="53f93-105">Den første del af dette emne beskriver opsætningen af dataene.</span><span class="sxs-lookup"><span data-stu-id="53f93-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="53f93-106">Den anden del fører dig gennem trinnene i gennemgangen.</span><span class="sxs-lookup"><span data-stu-id="53f93-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="53f93-107">Målgruppe</span><span class="sxs-lookup"><span data-stu-id="53f93-107">Target audience</span></span>

<span data-ttu-id="53f93-108">I dette emne lærer du, hvordan du konfigurerer underleverandørarbejde i produktion.</span><span class="sxs-lookup"><span data-stu-id="53f93-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="53f93-109">Du skal bruge eksisterende data i den juridiske enhed HQUS til at foretage grundlæggende opsætning af et aktivitetsflow for underleverandørarbejde.</span><span class="sxs-lookup"><span data-stu-id="53f93-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="53f93-110">Demodataene i den juridiske enhed HQUS omfatter opsætningsparametre, der er forudindstillet til at understøtte trinnene i gennemgangen.</span><span class="sxs-lookup"><span data-stu-id="53f93-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="53f93-111">Selvom gennemgangen omhandler vigtige smertepunkter og udfordringer for forskellige roller, kan den fuldføres af systemadministratoren.</span><span class="sxs-lookup"><span data-stu-id="53f93-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="53f93-112">Demoscenarie</span><span class="sxs-lookup"><span data-stu-id="53f93-112">Demo scenario</span></span>

<span data-ttu-id="53f93-113">Højttalere af høj kvalitet produceres i den juridiske enhed HQUS.</span><span class="sxs-lookup"><span data-stu-id="53f93-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="53f93-114">Under fremstillingsprocessen gennemgår højttalerne følgende tre operationer.</span><span class="sxs-lookup"><span data-stu-id="53f93-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="53f93-115">**Formontering** – Højttalerens kabinet samles.</span><span class="sxs-lookup"><span data-stu-id="53f93-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="53f93-116">Materialet til kabinettet plukkes på materialelagerstedet, før operationen startes.</span><span class="sxs-lookup"><span data-stu-id="53f93-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="53f93-117">**Belægning** – Når højttalerkabinettet er samlet, skal det belægges.</span><span class="sxs-lookup"><span data-stu-id="53f93-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="53f93-118">Denne handling udføres af en leverandør (underleverandør).</span><span class="sxs-lookup"><span data-stu-id="53f93-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="53f93-119">Det formonterede højttalerkabinet leveres til underleverandøren af belægning sammen med to materialer.</span><span class="sxs-lookup"><span data-stu-id="53f93-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="53f93-120">**Finish** – Efter det formonterede højttalerkabinet er blevet belagt af underleverandøren, returneres det til den juridiske enhed HQUS, så den endelige montage af højttaleren kan fuldføres.</span><span class="sxs-lookup"><span data-stu-id="53f93-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="53f93-121">I følgende illustration vises de tre operationer og de materialer, de forbruger.</span><span class="sxs-lookup"><span data-stu-id="53f93-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Operationerne Formontering, Belægning og Finish og de materialer, de forbruger](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="53f93-123">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="53f93-123">Setup</span></span>

<span data-ttu-id="53f93-124">Før du begynder denne gennemgang, skal du konfigurere dataene.</span><span class="sxs-lookup"><span data-stu-id="53f93-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="53f93-125">Konfigurer det færdige produkt</span><span class="sxs-lookup"><span data-stu-id="53f93-125">Set up the finished product</span></span>

<span data-ttu-id="53f93-126">Denne procedure der fører dig gennem opsætningen af det frigivne produkt D8100, "Belagt kabinet".</span><span class="sxs-lookup"><span data-stu-id="53f93-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="53f93-127">Vælg **Administration af produktoplysninger \> Produkter \> Frigivne produkter** for at åbne siden **Frigivne produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="53f93-128">Angiv **D8100** i Quick filter-feltet for at finde det eksisterende frigivne produkt.</span><span class="sxs-lookup"><span data-stu-id="53f93-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Filtrering for frigivet produkt D8100 på siden Frigivne produktdetaljer](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="53f93-130">I handlingsruden skal du under fanen **Opret** vælge **Rute** for at åbne siden **Rute**.</span><span class="sxs-lookup"><span data-stu-id="53f93-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="53f93-131">På siden **Rute** vises de otte ruteversioner for det frigivne produkt D8100.</span><span class="sxs-lookup"><span data-stu-id="53f93-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="53f93-132">De otte ruteversioner er opdelt i fire ruter på sted 1 og sted 5.</span><span class="sxs-lookup"><span data-stu-id="53f93-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="53f93-133">Rute 000400 anvendes til efterkalkulation, rute 00041 bruges, når operationen Belægning er en intern handling, og rute 00042 bruges, når operationen Belægning er en ekstern operation.</span><span class="sxs-lookup"><span data-stu-id="53f93-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Otte ruteversioner på siden Rute](./media/subcontract03_route-page.png)

4. <span data-ttu-id="53f93-135">I den øverste rude i **Versioner**-gitteret skal du vælge ruteversion **00042** for sted **5**.</span><span class="sxs-lookup"><span data-stu-id="53f93-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="53f93-136">I den nederste rude under fanen **Oversigt** skal du vælge operationen **20** (**Cbnt CtSc**) i gitteret.</span><span class="sxs-lookup"><span data-stu-id="53f93-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Operation 20 for ruteversion 00042 for sted 5 er valgt](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="53f93-138">Vælg fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="53f93-138">Select the **General** tab.</span></span>

    <span data-ttu-id="53f93-139">Bemærk, at feltet **Rutetype** er angivet til **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="53f93-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="53f93-140">Denne værdi angiver, at operation 20 (Cbnt CtSc) er en operation, der er udført af underleverandør.</span><span class="sxs-lookup"><span data-stu-id="53f93-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Feltet Rutetype angivet til Leverandør under fanen Generelt](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="53f93-142">Vælg fanen **Ressourcebehov**.</span><span class="sxs-lookup"><span data-stu-id="53f93-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="53f93-143">Egenskaber skal bruges til at finde en passende ressource i produktionsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="53f93-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="53f93-144">For operation 20 (Cbnt CtSc) skal du bemærke, at en ressource, der har to egenskaber, **Belægning** og **Belagte kabinetter**, er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="53f93-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Belægning og Belagte kabinetter som egenskaber under fanen Ressourcebehov](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="53f93-146">Vælg **Disponible ressourcer** for at åbne **Disponible ressourcer**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="53f93-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="53f93-147">Der findes tre ressourcer, der opfylder ressourcebehovet til operationen.</span><span class="sxs-lookup"><span data-stu-id="53f93-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="53f93-148">Bemærk, at ressourcerne 8851 og 8852 er af typen **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="53f93-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Tre disponible ressourcer i dialogboksen Disponible ressourcer](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="53f93-150">Vælg **OK** at lukke **Disponible ressourcer**-dialogboksen, og vend tilbage til siden **Rute**.</span><span class="sxs-lookup"><span data-stu-id="53f93-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="53f93-151">Luk siden **Rute** for at vende tilbage til siden **Frigivne produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Siden Frigivne produktdetaljer](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="53f93-153">I handlingsruden skal du under fanen **Opret** vælge **Styklisteversioner** for at åbne siden **Styklisteversioner**.</span><span class="sxs-lookup"><span data-stu-id="53f93-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="53f93-154">Siden **Styklisteversioner** viser de fire styklisteversioner for det frigivne produkt D8100.</span><span class="sxs-lookup"><span data-stu-id="53f93-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="53f93-155">Styklisten 000040 anvendes til efterkalkulation og planlægning, styklisten 000041 bruges, hvis handlingen Belægning udføres internt, og styklisterne 000042 og 000043 bruges, hvis handlingen Belægning udføres af underleverandør.</span><span class="sxs-lookup"><span data-stu-id="53f93-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="53f93-156">Bemærk, at vare S8050 er et produkt af **Service**-varetypen.</span><span class="sxs-lookup"><span data-stu-id="53f93-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="53f93-157">Varen repræsenterer det arbejde, der udføres af underleverandør.</span><span class="sxs-lookup"><span data-stu-id="53f93-157">This item represents the subcontracted work.</span></span>

    ![Fire styklisteversioner på siden Styklisteversioner](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="53f93-159">Brug oversigtspanelet **Styklistelinjer** til at vælge **Rediger** for at åbne **Rediger styklistelinje**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="53f93-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="53f93-160">Når en produktionsordre er oprettet og forkalkuleret for det frigivne produkt D8100, genereres en indkøbsordre automatisk for vare S8050.</span><span class="sxs-lookup"><span data-stu-id="53f93-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="53f93-161">Denne indkøbsordre bliver knyttet til produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="53f93-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="53f93-162">For indkøbsordrer, der skal genereres automatisk, skal feltet **Linjetype** være angivet til **Leverandør**, og kreditorkontoen for underleverandøren skal være valgt.</span><span class="sxs-lookup"><span data-stu-id="53f93-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="53f93-163">I dette tilfælde er kreditorkontoen US-801.</span><span class="sxs-lookup"><span data-stu-id="53f93-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="53f93-164">Bemærk, at styklistelinjen er tilknyttet operationen Belægning via operationsnummeret (i dette tilfælde 20).</span><span class="sxs-lookup"><span data-stu-id="53f93-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Dialogboksen Rediger styklistelinje](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="53f93-166">Opret en adgangskode til lagermedarbejdere</span><span class="sxs-lookup"><span data-stu-id="53f93-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="53f93-167">Du skal definere en adgangskode for de lagermedarbejdere, der bruger en håndholdt enhed.</span><span class="sxs-lookup"><span data-stu-id="53f93-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="53f93-168">Vælg **Lagerstedsstyring \> Konfiguration \> Arbejder** for at åbne siden **Arbejdsbrugere**.</span><span class="sxs-lookup"><span data-stu-id="53f93-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="53f93-169">I oversigtspanelet **Brugere** skal du vælge rækken for bruger **51**.</span><span class="sxs-lookup"><span data-stu-id="53f93-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Siden Arbejdsbrugere](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="53f93-171">Vælg **Nulstil adgangskode**.</span><span class="sxs-lookup"><span data-stu-id="53f93-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="53f93-172">I felterne **Adgangskode** og **Bekræft adgangskode** skal du angive **1**.</span><span class="sxs-lookup"><span data-stu-id="53f93-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="53f93-173">Vælg **Angiv adgangskode**.</span><span class="sxs-lookup"><span data-stu-id="53f93-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="53f93-174">Trinvis gennemgang</span><span class="sxs-lookup"><span data-stu-id="53f93-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="53f93-175">**Scenario og baggrund**</span><span class="sxs-lookup"><span data-stu-id="53f93-175">**Scenario and background**</span></span>

<span data-ttu-id="53f93-176">Der oprettes en produktionsordre på 10 styk for produkt D8100, "Belagt kabinet".</span><span class="sxs-lookup"><span data-stu-id="53f93-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="53f93-177">Belægningen af kabinetterne er en underleverandøroperation, der udføres hos leverandør US-801, Perfect Coating Solutions.</span><span class="sxs-lookup"><span data-stu-id="53f93-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="53f93-178">Produktionsordren består af tre operationer.</span><span class="sxs-lookup"><span data-stu-id="53f93-178">The production order consists of three operations.</span></span> <span data-ttu-id="53f93-179">I den første operation er kabinettet formonteret som en intern operation.</span><span class="sxs-lookup"><span data-stu-id="53f93-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="53f93-180">Materialet til formonteringen frigives til pluk på råvarelageret.</span><span class="sxs-lookup"><span data-stu-id="53f93-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="53f93-181">Når formonteringen er fuldført, sendes det formonterede kabinet til Perfect Coating Solutions sammen med to materialer, der kræves til operationen Belægning.</span><span class="sxs-lookup"><span data-stu-id="53f93-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="53f93-182">Når det belagte kabinet modtages fra leverandøren, gennemgår det en endelig montage, før det færdigmeldes.</span><span class="sxs-lookup"><span data-stu-id="53f93-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="53f93-183">Vælg **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer** for at åbne siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="53f93-184">I handlingsruden skal du vælge **Ny produktionsordre** for at åbne dialogboksen **Oprettelse af produktionsordre**.</span><span class="sxs-lookup"><span data-stu-id="53f93-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Dialogboksen Oprettelse af produktionsordre](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="53f93-186">Vælg **D8100** i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="53f93-187">Når du har valgt varenummeret, vises felter for lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="53f93-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="53f93-188">Vælg **Krom** i feltet **Farve**.</span><span class="sxs-lookup"><span data-stu-id="53f93-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="53f93-189">Der vises en meddelelse, hvor du bliver spurgt, om de aktive versioner for styklisten og ruten skal indsættes.</span><span class="sxs-lookup"><span data-stu-id="53f93-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Meddelelsesboks](./media/subcontract13_message-box.png)

5. <span data-ttu-id="53f93-191">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="53f93-191">Select **Yes**.</span></span> 

    <span data-ttu-id="53f93-192">I **Opret produktionsordre**-dialogboksen er de aktive versioner af styklisten og ruten for produkt D8100 automatisk valgt i felterne **Styklistenummer** og **Rutenummer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="53f93-193">I dette tilfælde er stykliste **000040** og rute **000040** valgt.</span><span class="sxs-lookup"><span data-stu-id="53f93-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="53f93-194">Version 000040 bruges til efterkalkulation og planlægning for både styklisten og ruten.</span><span class="sxs-lookup"><span data-stu-id="53f93-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="53f93-195">Vælg **5** i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="53f93-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="53f93-196">Vælg **51** i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="53f93-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="53f93-197">I felterne **Styklistenummer** og **Rutenummer** skal du ændre den værdi, der automatisk er valgt, til **000042**.</span><span class="sxs-lookup"><span data-stu-id="53f93-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="53f93-198">Version 000042 bruges til at give i underentreprise belægningen af kabinettet til leverandør US-801 for både styklisten og ruten.</span><span class="sxs-lookup"><span data-stu-id="53f93-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Værdier i dialogboksen Opret produktionsordre](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="53f93-200">Vælg **Opret** for at oprette produktionsordren og vende tilbage til siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Ny produktionsordre på siden Alle produktionsordrer](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="53f93-202">I handlingsruden skal du under fanen **Produktionsordre** vælge **Estimat** for at åbne **Estimat**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="53f93-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Dialogboksen Estimat](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="53f93-204">Vælg **OK** for at bekræfte estimatet og vende tilbage til siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="53f93-205">Når produktionsordren er estimeret, genereres indkøbsordren for servicevare S8050 for leverandør US-801.</span><span class="sxs-lookup"><span data-stu-id="53f93-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="53f93-206">I handlingsruden skal du under fanen **Produktionsordre** vælge **Stykliste** for at åbne siden **Stykliste**, hvor du kan få vist styklistelinjer for produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="53f93-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="53f93-207">For servicevare S8050 skal du bemærke, at der er en reference til den indkøbsordre, der blev genereret, da produktionsordren blev estimeret.</span><span class="sxs-lookup"><span data-stu-id="53f93-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Produktionsordrens styklistelinjer på siden Stykliste](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="53f93-209">Luk siden **Stykliste** for at vende tilbage til siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="53f93-210">I handlingsruden skal du under fanen **Tidsplan** vælge **Finplanlægge** for at åbne **Finplanlægning**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="53f93-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="53f93-211">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="53f93-211">Specify the following values:</span></span>

    - <span data-ttu-id="53f93-212">Vælg **Fremad fra i morgen** i feltet **Planlægningsvej**.</span><span class="sxs-lookup"><span data-stu-id="53f93-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="53f93-213">Angiv **Kapacitetsbegrænsning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="53f93-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Dialogboksen Finplanlægning](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="53f93-215">Vælg **OK** for at lukke **Finplanlægning**-dialogboksen og vende tilbage til siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="53f93-216">I handlingsruden skal du under fanen **Tidsplan** vælge **Gantt** for at åbne siden **Gantt-diagram - ressourcevisning**.</span><span class="sxs-lookup"><span data-stu-id="53f93-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="53f93-217">Gantt-diagrammet indeholder en visuel oversigt over, hvordan produktionsjob planlægges på ressourcer.</span><span class="sxs-lookup"><span data-stu-id="53f93-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="53f93-218">Bemærk, at den eksterne belægningsoperation består af tre job: et procesjob, et transportjob og et køtidsjob.</span><span class="sxs-lookup"><span data-stu-id="53f93-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Gantt-diagram på Gantt-diagram - siden Ressourcevisning](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="53f93-220">Luk siden **Gantt-diagram - ressourcevisning** for at vende tilbage til siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="53f93-221">I handlingsruden skal du under fanen **Produktionsordre** vælge **Frigivelse** for at åbne **Frigivelse**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="53f93-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Dialogboksen Frigivelse](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="53f93-223">Vælg **OK** for at lukke dialogboksen **Frigivelse**.</span><span class="sxs-lookup"><span data-stu-id="53f93-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="53f93-224">Vælg **Produktionsstyring \> Periodiske opgaver \> Frigiv til lagersted \> Automatisk frigivelse af stykliste- og formellinjer** for at åbne dialogboksen **Automatisk frigivelse af stykliste- og formellinjer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Dialogboksen Automatisk frigivelse af stykliste- og formellinjer](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="53f93-226">Vælg **OK** for at køre automatisk frigivelse af stykliste- og formellinjejob.</span><span class="sxs-lookup"><span data-stu-id="53f93-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="53f93-227">Dette job frigiver plukarbejde for råmaterialer til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="53f93-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="53f93-228">Vælg **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer** for at åbne siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="53f93-229">Du kan bruge feltet Quick filter til at vælge den produktionsordre, du har arbejdet på.</span><span class="sxs-lookup"><span data-stu-id="53f93-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="53f93-230">I handlingsruden skal du under fanen **Lagersted** vælge **Arbejdsdetaljer** for at åbne siden **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="53f93-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="53f93-231">Bemærk, at siden viser to sæt af arbejde til pluk af råmateriale.</span><span class="sxs-lookup"><span data-stu-id="53f93-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="53f93-232">Det første arbejde er for materialerne M8100 og M8101.</span><span class="sxs-lookup"><span data-stu-id="53f93-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="53f93-233">Disse materialer forbruges af operation 10.</span><span class="sxs-lookup"><span data-stu-id="53f93-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="53f93-234">Det andet arbejde er for materialerne M8202 og M8250.</span><span class="sxs-lookup"><span data-stu-id="53f93-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="53f93-235">Materialerne forbruges af operation 20, som er operationen hos underleverandøren.</span><span class="sxs-lookup"><span data-stu-id="53f93-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![To sæt af arbejde til pluk af råmateriale på siden Arbejde](./media/subcontract22_work-page.png)

26. <span data-ttu-id="53f93-237">Start lagerstedsappen for at behandle lagerstedets arbejde for operation 10.</span><span class="sxs-lookup"><span data-stu-id="53f93-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="53f93-238">Vælg **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer** for at åbne siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="53f93-239">Du kan bruge feltet Quick filter til at vælge den produktionsordre, du har arbejdet på.</span><span class="sxs-lookup"><span data-stu-id="53f93-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="53f93-240">I handlingsruden skal du under fanen **Produktionsordre** vælge **Start** for at åbne **Start**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="53f93-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="53f93-241">Angiv følgende værdier under fanen **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="53f93-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="53f93-242">I feltet **Fra opr.nr.**</span><span class="sxs-lookup"><span data-stu-id="53f93-242">In the **From Oper. No.**</span></span> <span data-ttu-id="53f93-243">skal du vælge **10**.</span><span class="sxs-lookup"><span data-stu-id="53f93-243">field, select **10**.</span></span>
    - <span data-ttu-id="53f93-244">I feltet **Til opr.nr.**</span><span class="sxs-lookup"><span data-stu-id="53f93-244">In the **To Oper. No.**</span></span> <span data-ttu-id="53f93-245">skal du vælge **10**.</span><span class="sxs-lookup"><span data-stu-id="53f93-245">field, select **10**.</span></span>

    ![Værdier, der er angivet under fanen Generelt](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="53f93-247">Vælg **OK** for at lukke **Start**-dialogboksen og vende tilbage til siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="53f93-248">Bemærk, at status for produktionsordren nu er **Startet**.</span><span class="sxs-lookup"><span data-stu-id="53f93-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="53f93-249">Materialerne til operation 10 forbruges af en automatisk bogføring af pluklistekladden.</span><span class="sxs-lookup"><span data-stu-id="53f93-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="53f93-250">Tidsforbruget for operation 10 er medtaget i en automatisk bogføring af en rutekortskladde.</span><span class="sxs-lookup"><span data-stu-id="53f93-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="53f93-251">Start lagerstedsappen for at behandle lagerstedets arbejde for operation 20.</span><span class="sxs-lookup"><span data-stu-id="53f93-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="53f93-252">I handlingsruden skal du under fanen **Produktionsordre** vælge **Start** for at åbne **Start**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="53f93-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="53f93-253">Angiv følgende værdier under fanen **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="53f93-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="53f93-254">I feltet **Fra opr.nr.**</span><span class="sxs-lookup"><span data-stu-id="53f93-254">In the **From Oper. No.**</span></span> <span data-ttu-id="53f93-255">skal du vælge **20**.</span><span class="sxs-lookup"><span data-stu-id="53f93-255">field, select **20**.</span></span>
    - <span data-ttu-id="53f93-256">I feltet **Til opr.nr.**</span><span class="sxs-lookup"><span data-stu-id="53f93-256">In the **To Oper. No.**</span></span> <span data-ttu-id="53f93-257">skal du vælge **20**.</span><span class="sxs-lookup"><span data-stu-id="53f93-257">field, select **20**.</span></span>
    - <span data-ttu-id="53f93-258">Angiv **10** i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="53f93-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="53f93-259">Vælg **Nej** i feltet **Bogfør plukliste nu**.</span><span class="sxs-lookup"><span data-stu-id="53f93-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Værdier, der er angivet under fanen Generelt](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="53f93-261">Vælg **OK** for at lukke **Start**-dialogboksen og vende tilbage til siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="53f93-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="53f93-262">Der oprettes en plukliste for de materialer, der bruges til operationen Belægning og til servicevaren.</span><span class="sxs-lookup"><span data-stu-id="53f93-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="53f93-263">Servicevaren repræsenterer omkostningerne for operationen hos underleverandøren.</span><span class="sxs-lookup"><span data-stu-id="53f93-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="53f93-264">I handlingsruden skal du under fanen **Vis** vælge **Plukliste** for at åbne siden **Plukliste**.</span><span class="sxs-lookup"><span data-stu-id="53f93-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="53f93-265">Vælg pluklisten, der ikke er bogført, og vælg derefter kladdenummeret for at få vist kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="53f93-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Kladdelinjer på siden Plukliste](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="53f93-267">I handlingsruden skal du vælge **Udskriv** \> **Plukliste (rapport)** for at åbne dialogboksen **Plukliste (rapport)**.</span><span class="sxs-lookup"><span data-stu-id="53f93-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="53f93-268">Angiv indstillingen **Brug følgeseddellayout** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="53f93-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Dialogboksen Plukliste (rapport)](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="53f93-270">Vælg **OK** for at generere en **Plukliste**-rapport.</span><span class="sxs-lookup"><span data-stu-id="53f93-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="53f93-271">I dette tilfælde udskrives en leverandørfølgeseddel fra pluklistekladden for produktionen.</span><span class="sxs-lookup"><span data-stu-id="53f93-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="53f93-272">Følgeseddelen angiver de materialer, der leveres til den leverandør, der udfører belægningsoperationen.</span><span class="sxs-lookup"><span data-stu-id="53f93-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Plukliste (rapport)](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="53f93-274">Luk **Plukliste**-rapporten for at vende tilbage til siden **Plukliste**.</span><span class="sxs-lookup"><span data-stu-id="53f93-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="53f93-275">I handlingsruden skal du vælge **Bogfør** for at åbne **Bogfør kladde**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="53f93-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Dialogboksen Bogfør kladde](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="53f93-277">Vælg **OK** for at lukke dialogboksen **Bogfør kladde**.</span><span class="sxs-lookup"><span data-stu-id="53f93-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="53f93-278">Åbn indkøbsordren</span><span class="sxs-lookup"><span data-stu-id="53f93-278">Open the purchase order.</span></span>

    ![Siden Indkøbsordre](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="53f93-280">I handlingsruden under fanen **Indkøb** skal du vælge **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="53f93-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="53f93-281">Vælg **Bogfør** for at åbne dialogboksen **Bogfør kladde**.</span><span class="sxs-lookup"><span data-stu-id="53f93-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="53f93-282">Vælg **OK** for at lukke **Bogfør kladde**-dialogboksen og vende tilbage til siden **Indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="53f93-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="53f93-283">Skift enhedspris fra **33** til **40**.</span><span class="sxs-lookup"><span data-stu-id="53f93-283">Change the unit price from **33** to **40**.</span></span>

    ![Enhedspris, der er ændret på siden Indkøbsordre](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="53f93-285">Bekræft indkøbsordren igen.</span><span class="sxs-lookup"><span data-stu-id="53f93-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="53f93-286">Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="53f93-286">Product receipt.</span></span>

    ![Dialogboksen Konterer produktkvittering](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="53f93-288">Indkøbsfaktura.</span><span class="sxs-lookup"><span data-stu-id="53f93-288">Purchase invoice.</span></span>
52. <span data-ttu-id="53f93-289">Opdater status for sammenholdelse.</span><span class="sxs-lookup"><span data-stu-id="53f93-289">Update the match status.</span></span>

    ![Siden Kreditorfaktura](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="53f93-291">Færdigmelding.</span><span class="sxs-lookup"><span data-stu-id="53f93-291">Report as finished.</span></span>

    ![Dialogboksen Færdigmelding](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="53f93-293">Slut.</span><span class="sxs-lookup"><span data-stu-id="53f93-293">End.</span></span>

    ![Dialogboksen Slut](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="53f93-295">Omkostningssammenligning.</span><span class="sxs-lookup"><span data-stu-id="53f93-295">Cost comparison.</span></span>

    ![Sammenligningsdiagrammer for omkostning](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="53f93-297">Manglende opsætning i data.</span><span class="sxs-lookup"><span data-stu-id="53f93-297">Missing setup in data.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]