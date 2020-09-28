---
title: ER-destinationstype for e-mail
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere en maildestination for hver komponent af typen MAPPE eller FIL i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745555"
---
# <a name="email-destination"></a><span data-ttu-id="e8edf-103">Maildestination</span><span class="sxs-lookup"><span data-stu-id="e8edf-103">Email destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8edf-104">Du kan konfigurere en e-maildestination for hver komponent af typen MAPPE eller FIL i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="e8edf-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="e8edf-105">På baggrund af destinationsindstillingen leveres et genereret dokument som en vedhæftet fil til en e-mail.</span><span class="sxs-lookup"><span data-stu-id="e8edf-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="e8edf-106">Indstil **Aktiveret** til **Ja** for at sende en outputfil via mail.</span><span class="sxs-lookup"><span data-stu-id="e8edf-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="e8edf-107">Når denne indstilling er aktiveret, kan du angive e-mailmodtagere og redigere e-mailens emne og brødtekst.</span><span class="sxs-lookup"><span data-stu-id="e8edf-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="e8edf-108">Du kan konfigurere konstanttekster til e-mailens emne og brødtekst, eller du kan bruge ER [formler](er-formula-language.md) til dynamisk at oprette e-mailtekster.</span><span class="sxs-lookup"><span data-stu-id="e8edf-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="e8edf-109">Du kan konfigurere e-mailadresser for ER på to måder.</span><span class="sxs-lookup"><span data-stu-id="e8edf-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="e8edf-110">Konfigurationen kan fuldføres på samme måde, som funktionen Udskriftsstyring fuldfører den, eller du kan løse en e-mailadresse ved at bruge en direkte reference til ER-konfigurationen via en formel.</span><span class="sxs-lookup"><span data-stu-id="e8edf-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="e8edf-111">[![Aktivere e-maildestination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="e8edf-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="e8edf-112">E-mailadressetyper</span><span class="sxs-lookup"><span data-stu-id="e8edf-112">Email address types</span></span>

<span data-ttu-id="e8edf-113">Når du vælger **Rediger** i felterne **Til** eller **Cc**, åbnes dialogboksen **Mail til**.</span><span class="sxs-lookup"><span data-stu-id="e8edf-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="e8edf-114">Du kan derefter vælge type e-mailadresse, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="e8edf-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="e8edf-115">I øjeblikket understøttes e-mailtyperne **Konfigurationsmail** og **Udskriftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="e8edf-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="e8edf-116">[![Vælge e-mailtype](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="e8edf-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="e8edf-117">Udskriftsstyring</span><span class="sxs-lookup"><span data-stu-id="e8edf-117">Print management</span></span>

<span data-ttu-id="e8edf-118">Hvis du vælger e-mailtypen **Udskriftsstyring**, kan du angive fast e-mailadresser i feltet **Til**.</span><span class="sxs-lookup"><span data-stu-id="e8edf-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="e8edf-119">[![Konfigurere faste e-mailadresser](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="e8edf-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="e8edf-120">Hvis du vil bruge mailadresser, der ikke er faste, skal du vælge mailkildetypen for en fildestination.</span><span class="sxs-lookup"><span data-stu-id="e8edf-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="e8edf-121">Følgende værdier understøttes: **Kunde**, **Leverandør**, **Kundeemne**, **Kontakt**, **Konkurrent**, **Arbejder**, **Ansøger**, **Mulig kreditor** og **Ikke-godkendt kreditor**.</span><span class="sxs-lookup"><span data-stu-id="e8edf-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="e8edf-122">Når du har valgt en kildetype for mail, skal du bruge knappen ved feltet **Kildekonto for mail** til at åbne formularen **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="e8edf-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="e8edf-123">Du kan bruge denne formular til at tilknytte en formel, der på kørselstidspunktet returnerer **partskontoen** for den valgte kildetype fra det behandlede dokument til e-maildestinationen.</span><span class="sxs-lookup"><span data-stu-id="e8edf-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="e8edf-124">[![Konfigurere e-mailens kildekonto](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="e8edf-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="e8edf-125">Formler er specifikke for ER-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e8edf-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="e8edf-126">Angiv en dokumentspecifik reference til en debitor- eller kreditorparttype i feltet **Formel**.</span><span class="sxs-lookup"><span data-stu-id="e8edf-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="e8edf-127">I stedet for at skrive kan du finde datakildenoden, der repræsenterer debitor- eller kreditorkontoen, og derefter vælge **Tilføj datakilde** for at opdatere formlen.</span><span class="sxs-lookup"><span data-stu-id="e8edf-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="e8edf-128">Hvis du f.eks. bruger konfigurationen **ISO 20022-kreditoverførsel**, er den node, der repræsenterer en kreditorkonto, `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="e8edf-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="e8edf-129">Hvis du angiver en strengværdi som f.eks. `"DE-001"` og gemmer en formel, sendes der en e-mail til kontaktpersonen for leverandøren, **DE-001**.</span><span class="sxs-lookup"><span data-stu-id="e8edf-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="e8edf-130">[![Siden ER-formeldesigner](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="e8edf-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="e8edf-131">[![Konfigurere kildeattributter for mailkonto](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="e8edf-131">[![Configure email source attributes account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="e8edf-132">Konfigurationsmail</span><span class="sxs-lookup"><span data-stu-id="e8edf-132">Configuration email</span></span>

<span data-ttu-id="e8edf-133">Brug denne e-mailtype, hvis den konfiguration, du bruger, har en node i datakilderne, der returnerer en **e-mailadresse**.</span><span class="sxs-lookup"><span data-stu-id="e8edf-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="e8edf-134">Du kan bruge datakilder og funktioner i formeldesigneren til at få en korrekt formateret e-mailadresse.</span><span class="sxs-lookup"><span data-stu-id="e8edf-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="e8edf-135">Hvis du f.eks. bruger konfigurationen **ISO 20022-kreditoverførsel**, er den node, der repræsenterer en e-mailadresse for en kreditors kontaktperson, `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="e8edf-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="e8edf-136">[![Konfigurere kilden til e-mailadressen](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="e8edf-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8edf-137">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e8edf-137">Additional resources</span></span>

- [<span data-ttu-id="e8edf-138">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="e8edf-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e8edf-139">Destinationer for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="e8edf-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="e8edf-140">Formeldesigner i elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="e8edf-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
