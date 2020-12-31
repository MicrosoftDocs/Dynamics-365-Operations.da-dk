---
title: Ny brugergrænseflade i dokumenter i styring af forretningsdokumenter
description: Dette emne indeholder oplysninger om, hvordan du kan bruge den nye brugergrænseflade i dokumenter i funktionen Styring af forretningsdokumenter i den elektroniske rapporteringsstruktur (ER).
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681346"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="f4429-103">Ny brugergrænseflade i dokumenter i styring af forretningsdokumenter</span><span class="sxs-lookup"><span data-stu-id="f4429-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4429-104">Styring af forretningsdokumenter gør det muligt for erhvervsbrugere at redigere forretningsdokumentskabeloner ved at bruge en Microsoft 365-tjeneste eller det relevante Microsoft Office-skrivebordsprogram.</span><span class="sxs-lookup"><span data-stu-id="f4429-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="f4429-105">Redigeringer kan omfatte designændringer eller nye installationer, eller brugerne kan tilføje pladsholdere for at medtage yderligere data uden at skulle ændre kildekoden.</span><span class="sxs-lookup"><span data-stu-id="f4429-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="f4429-106">Du kan finde flere oplysninger om, hvordan du arbejder med Styring af forretningsdokumenter, i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="f4429-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="f4429-107">Den nye brugergrænseflade i dokumentet er klarere og mere praktisk at bruge.</span><span class="sxs-lookup"><span data-stu-id="f4429-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="f4429-108">Området **Forretningsdokument** viser kun de skabeloner, der er tilgængelige for den aktuelle udbyder.</span><span class="sxs-lookup"><span data-stu-id="f4429-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="f4429-109">Knappen **Nyt dokument** giver brugerne mulighed for at oprette og redigere en skabelon i en formatkonfiguration for elektronisk rapportering (ER), der er leveret af en anden udbyder.</span><span class="sxs-lookup"><span data-stu-id="f4429-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="f4429-110">I eksemplet i dette emne er udbyderen Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f4429-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="f4429-111">Gøre den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter tilgængeligt</span><span class="sxs-lookup"><span data-stu-id="f4429-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="f4429-112">Hvis du vil begynde at bruge den nye brugergrænseflade i dokumenter i Styring af forretningsdokumenter, skal du aktivere funktionen **Office-lignende brugergrænsefladeoplevelse for Styring af forretningsdokumenter** i arbejdsområdet **Administration af funktioner**.</span><span class="sxs-lookup"><span data-stu-id="f4429-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="f4429-113">Udfør følgende trin for at aktivere denne funktion for alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="f4429-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="f4429-114">I arbejdsområdet **Funktionsstyring** under fanen **Ny** skal du vælge funktionen **Office-lignende brugergrænsefladeoplevelse for Styring af forretningsdokumenter** på listen.</span><span class="sxs-lookup"><span data-stu-id="f4429-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="f4429-115">Vælg **Aktivér nu** for at aktivere den valgte funktion.</span><span class="sxs-lookup"><span data-stu-id="f4429-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="f4429-116">Opdater siden for at få adgang til den nye funktion.</span><span class="sxs-lookup"><span data-stu-id="f4429-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="f4429-117">Rediger skabeloner, der ejes af andre udbydere</span><span class="sxs-lookup"><span data-stu-id="f4429-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="f4429-118">I arbejdsområdet **Styring af forretningsdokumenter** skal du vælge **Nyt dokument**.</span><span class="sxs-lookup"><span data-stu-id="f4429-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Arbejdsområdet til Styring af forretningsdokumenter](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="f4429-120">Vælg i dialogboksen det dokument, der skal bruges som skabelon, og vælg derefter **Opret dokument**.</span><span class="sxs-lookup"><span data-stu-id="f4429-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Dialogboksen Forretningsdokumenter](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="f4429-122">I den nye dialogboks skal du i feltet **Titel** ændre titlen efter behov.</span><span class="sxs-lookup"><span data-stu-id="f4429-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="f4429-123">Titelteksten bruges til at navngive den nye ER-formatkonfiguration, der oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="f4429-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="f4429-124">Kladdeversionen af denne konfiguration (**FTI-debitorrapport (GER) Kopi**) vil indeholde den redigerede skabelon og vil blive brugt til at køre dette ER-format for den aktuelle bruger.</span><span class="sxs-lookup"><span data-stu-id="f4429-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="f4429-125">Den oprindelige skabelon fra ER-basisformatkonfigurationen vil blive brugt til at køre dette ER-format for enhver anden bruger.</span><span class="sxs-lookup"><span data-stu-id="f4429-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="f4429-126">I feltet **Navn** skal du ændre navnet på den første revision af den redigerbare skabelon, der oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="f4429-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="f4429-127">I feltet **Kommentar** skal du opdatere bemærkningerne til revisionen af den redigerbare skabelon, der oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="f4429-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="f4429-128">Vælg **OK** for at bekræfte starten af redigeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f4429-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dialogboksen Dokumentoprettelse](./media/BDM_overview_new_template3.png)

<span data-ttu-id="f4429-130">Knappen **Nyt dokument** bruges til at oprette og redigere en skabelon i en ER-formatkonfiguration, der er leveret af en anden udbyder.</span><span class="sxs-lookup"><span data-stu-id="f4429-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="f4429-131">I dette eksempel er udbyderen Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f4429-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="f4429-132">Når du vælger **Nyt dokument**, kan du se alle de skabeloner, der ejes af den aktuelle udbyder og andre udbydere.</span><span class="sxs-lookup"><span data-stu-id="f4429-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="f4429-133">Når du har valgt skabelonen, vil den blive åbnet til redigering.</span><span class="sxs-lookup"><span data-stu-id="f4429-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="f4429-134">Den redigerede skabelon gemmes derefter i en ny ER-formatkonfiguration, der genereres automatisk.</span><span class="sxs-lookup"><span data-stu-id="f4429-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="f4429-135">Yderligere oplysninger finder du i [Oversigt over styring af forretningsdokumenter](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="f4429-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>
