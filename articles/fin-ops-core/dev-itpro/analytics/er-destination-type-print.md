---
title: ER-destinationstype for printer
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer en printerdestination for de enkelte MAPPE- eller FIL-komponenter i et ER-format (elektronisk rapportering).
author: NickSelin
manager: AnnBe
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 19613d9dfba21d591d96a2df45bedb80c043b3a7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561944"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="f0458-103">Printerdestination</span><span class="sxs-lookup"><span data-stu-id="f0458-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0458-104">Du kan sende et genereret dokument direkte til en netværksprinter til direkte udskrivning.</span><span class="sxs-lookup"><span data-stu-id="f0458-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f0458-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="f0458-105">Prerequisites</span></span>

<span data-ttu-id="f0458-106">Før du går i gang, skal du installere og konfigurere Dokumentets ruteplanlægningsagent og derefter registrere netværksprinterne.</span><span class="sxs-lookup"><span data-stu-id="f0458-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="f0458-107">Du kan finde flere oplysninger i [Installere dokumentets ruteplanlægningsagent for at aktivere netværksudskrivning](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="f0458-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="f0458-108">Gør printerdestinationen tilgængelig</span><span class="sxs-lookup"><span data-stu-id="f0458-108">Make the Printer destination available</span></span>

<span data-ttu-id="f0458-109">Hvis du vil gøre **Printer**-destinationen tilgængelig i den aktuelle forekomst af Microsoft Dynamics 365 Finance, skal du gå til arbejdsområdet **Funktionsstyring** og aktivere følgende funktioner i denne rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="f0458-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="f0458-110">Konverter udgående dokumenter for elektronisk rapportering fra Microsoft Office-formater til PDF</span><span class="sxs-lookup"><span data-stu-id="f0458-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="f0458-111">Dokumentets ruteplanlægningsagent som elektronisk rapporteringsdestination for udgående dokumenter</span><span class="sxs-lookup"><span data-stu-id="f0458-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="f0458-112">[![Aktivere funktionen til ER-printerdestination i Funktionsstyring](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="f0458-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="f0458-113">Anvendelighed</span><span class="sxs-lookup"><span data-stu-id="f0458-113">Applicability</span></span>

<span data-ttu-id="f0458-114">**Printer**-destinationen kan kun konfigureres for filkomponenter, der bruges til at generere output enten i PDF-format, der kan udskrives (PDF-fletning eller PDF-filformatelementer) eller Microsoft Office Excel/Word-format (Excel-fil).</span><span class="sxs-lookup"><span data-stu-id="f0458-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="f0458-115">Når der genereres output i PDF-format, sendes det til en printer.</span><span class="sxs-lookup"><span data-stu-id="f0458-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="f0458-116">Når der genereres output i Microsoft Office-format, konverteres det automatisk til PDF-format og sendes derefter til en printer.</span><span class="sxs-lookup"><span data-stu-id="f0458-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="f0458-117">Begrænsninger</span><span class="sxs-lookup"><span data-stu-id="f0458-117">Limitations</span></span>

<span data-ttu-id="f0458-118">**Printer**-destinationen implementeres kun i forbindelse med installationer i skyen.</span><span class="sxs-lookup"><span data-stu-id="f0458-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="f0458-119">Brug printerdestinationen</span><span class="sxs-lookup"><span data-stu-id="f0458-119">Use the Printer destination</span></span>

1. <span data-ttu-id="f0458-120">Angiv indstillingen **Aktiveret** til **Ja** for at sende et genereret dokument til en printer.</span><span class="sxs-lookup"><span data-stu-id="f0458-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="f0458-121">I feltet **Printernavn** skal du vælge den ønskede netværksprinter.</span><span class="sxs-lookup"><span data-stu-id="f0458-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="f0458-122">Angiv indstillingen **Gem i udskriftsarkiv?** til **Ja** for at gemme det genererede output i udskriftsarkivet, så det er tilgængeligt til yderligere udskrivning.</span><span class="sxs-lookup"><span data-stu-id="f0458-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="f0458-123">Hvis du senere vil have adgang til arkiveret, skal du gå til **Organisationsadministration** \> **Forespørgsler og rapporter** \> **Rapportarkiv**.</span><span class="sxs-lookup"><span data-stu-id="f0458-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="f0458-124">[![Brug af printerdestinationen](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="f0458-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="f0458-125">Indstillingen **Konverter til PDF** behøver ikke at blive aktiveret, når du konfigurer destinationen **Printer**.</span><span class="sxs-lookup"><span data-stu-id="f0458-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="f0458-126">PDF-konvertering til udskrivningsformål sker, også selvom indstillingen er slået fra.</span><span class="sxs-lookup"><span data-stu-id="f0458-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="f0458-127">Hvis du vil bruge en bestemt [sideretning](electronic-reporting-destinations.md#SelectPdfPageOrientation), når du udskriver et udgående dokument i Excel-format, skal du aktivere indstillingen **Konverter til PDF**.</span><span class="sxs-lookup"><span data-stu-id="f0458-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="f0458-128">Når du sætter indstillingen **Konverter til PDF** til **Ja**, bliver feltet **Sideretning** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="f0458-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="f0458-129">Du kan vælge en sideretning i feltet **Sideretning**.</span><span class="sxs-lookup"><span data-stu-id="f0458-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0458-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f0458-130">Additional resources</span></span>

- [<span data-ttu-id="f0458-131">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="f0458-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f0458-132">Destinationer for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="f0458-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
