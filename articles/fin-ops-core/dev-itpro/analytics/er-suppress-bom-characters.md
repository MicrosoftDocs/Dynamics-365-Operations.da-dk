---
title: Designe ER-konfigurationer til at udelade tegn for byterækkefølgemærke i genererede filer
description: I dette emne forklares det, hvordan du kan konfigurere et ER-format (elektronisk rapportering), så der genereres rapporter, hvor tegn for byterækkefølgemærke udelades.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ada93c0192aadac70c38c8c8c4f3af86ff6fc3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893270"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="15387-103">Designe ER-konfigurationer til at udelade tegn for byterækkefølgemærke i genererede filer</span><span class="sxs-lookup"><span data-stu-id="15387-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15387-104">Du kan designe [elektronisk rapportering (ER)](general-electronic-reporting.md) som [løsning](er-quick-start1-new-solution.md) for at oprette udgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="15387-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="15387-105">Hvis du vil generere dokumenterne som tekst- eller XML-filer, skal løsningen indeholde en ER-[konfiguration](general-electronic-reporting.md#Configuration), der indeholder en ER-[formatkomponent](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="15387-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="15387-106">Hvis du vil angive den [tegnkodning](/windows/win32/intl/character-sets), der repræsenterer sættet af tegn i genererede filer, skal ER-formatet indeholde formatelementet **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="15387-106">To specify the [character encoding](/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="15387-107">Hvis du vil konfigurere ER-formatkomponenten, skal du åbne [kladde](general-electronic-reporting.md#component-versioning)-versionen af ER-konfigurationen i ER-formatdesigneren og tilføje elementet **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="15387-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="15387-108">I feltet **Kodning** skal du angive kodningen af udgående filer, der genereres under kørsel ved hjælp af denne komponent.</span><span class="sxs-lookup"><span data-stu-id="15387-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="15387-109">Hvis formatet indeholder et forkert kodningsnavn, vises der en fejl, når du gemmer ændringerne i indstillingerne af formatet.</span><span class="sxs-lookup"><span data-stu-id="15387-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Tilføje et rodelement på siden Formatdesigner](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="15387-111">Hvis du angiver **UTF-8**, **UTF-16** eller **UTF-32** som kodning, bliver indstillingen **Undertryk BOM-tegn** tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="15387-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="15387-112">Angiv denne indstilling til **Ja** for at udelade [byterækkefølgemærketegn (BOM)](/globalization/encoding/byte-order-mark) i udgående filer, der genereres under kørslen, når det redigerbare ER-format køres.</span><span class="sxs-lookup"><span data-stu-id="15387-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="15387-113">Hvis du ikke udfylder feltet **Kodning**, bruges standardkodningen **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="15387-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Angive indstillingen Undertryk BOM-tegn på siden Formatdesigner](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="15387-115">Hvis du vil gennemse funktionaliteten under kørslen, skal du gennemføre den relevante procedure.</span><span class="sxs-lookup"><span data-stu-id="15387-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="15387-116">Udfør f.eks. trinnene i emnet [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md).</span><span class="sxs-lookup"><span data-stu-id="15387-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="15387-117">Når du har fuldført trinnene i sektionen [Rediger formatet, så beregningen er baseret på genereret output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) i dette emne, skal du følge disse ekstra trin.</span><span class="sxs-lookup"><span data-stu-id="15387-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="15387-118">Angiv UTF-kodningen:</span><span class="sxs-lookup"><span data-stu-id="15387-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="15387-119">Vælg **Rapport**-elementet af typen **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="15387-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="15387-120">Angiv **UTF-8**-kodningen i **Kodning**-feltet.</span><span class="sxs-lookup"><span data-stu-id="15387-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="15387-121">Opret en XML-fil, der indeholder et BOM-tegn:</span><span class="sxs-lookup"><span data-stu-id="15387-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="15387-122">Angiv indstillingen **Undertryk BOM-tegn** til **Nej** for at medtage BOM-tegn i genererede XML-filer.</span><span class="sxs-lookup"><span data-stu-id="15387-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="15387-123">Udfør trinnene i sektionen [Udskyde udførelsen af oversigts-XML-elementet, så den beregnede total bruges](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) af emnet [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md), og gem den genererede fil som **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="15387-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="15387-124">Opret en XML-fil, der ikke indeholder et BOM-tegn:</span><span class="sxs-lookup"><span data-stu-id="15387-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="15387-125">Angiv indstillingen **Undertryk BOM-tegn** til **Ja** for at udelade BOM-tegn i genererede XML-filer.</span><span class="sxs-lookup"><span data-stu-id="15387-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="15387-126">Udfør trinnene i sektionen [Udskyde udførelsen af oversigts-XML-elementet, så den beregnede total bruges](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) af emnet [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md), og gem den genererede fil som **SampleXmlReport (1).xml**.</span><span class="sxs-lookup"><span data-stu-id="15387-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="15387-127">Sammenlign de genererede filer i et filsammenligningsværktøj.</span><span class="sxs-lookup"><span data-stu-id="15387-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="15387-128">Den første forskel, du bemærker, er i filhovedet.</span><span class="sxs-lookup"><span data-stu-id="15387-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="15387-129">Filen SampleXmlReport.xml indeholder et BOM-tegn, mens filen SampleXmlReport (1).xml ikke gør.</span><span class="sxs-lookup"><span data-stu-id="15387-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Sammenligning af genererede filer med et filsammenligningsværktøj](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="15387-131">Se også</span><span class="sxs-lookup"><span data-stu-id="15387-131">See also</span></span>

- [<span data-ttu-id="15387-132">Udskyde udførelse af XML-elementer i ER-formater</span><span class="sxs-lookup"><span data-stu-id="15387-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]