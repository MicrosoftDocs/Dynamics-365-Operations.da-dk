---
title: ER-destinationstype for printer
description: Dette emne forklarer, hvordan du kan konfigurere en printerdestination for hver komponent af typen MAPPE eller FIL i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter i enten PDF eller Microsoft Office-formater (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
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
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019687"
---
# <a name="PrinterDestinationType"></a><span data-ttu-id="b6fe9-103">Printerdestination</span><span class="sxs-lookup"><span data-stu-id="b6fe9-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6fe9-104">Du kan sende et genereret dokument direkte til en netværksprinter til direkte udskrivning.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b6fe9-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="b6fe9-105">Prerequisites</span></span>

<span data-ttu-id="b6fe9-106">Før du går i gang, skal du installere og konfigurere Dokumentets ruteplanlægningsagent og derefter registrere netværksprinterne.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="b6fe9-107">Du kan finde flere oplysninger i [Installere dokumentets ruteplanlægningsagent for at aktivere netværksudskrivning](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="b6fe9-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="b6fe9-108">Gør printerdestinationen tilgængelig</span><span class="sxs-lookup"><span data-stu-id="b6fe9-108">Make the Printer destination available</span></span>

<span data-ttu-id="b6fe9-109">Hvis du vil gøre **Printer**-destinationen tilgængelig i den aktuelle forekomst af Microsoft Dynamics 365 Finance, skal du gå til arbejdsområdet **Funktionsstyring** og aktivere følgende funktioner i denne rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="b6fe9-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="b6fe9-110">Konverter udgående dokumenter for elektronisk rapportering fra Microsoft Office-formater til PDF</span><span class="sxs-lookup"><span data-stu-id="b6fe9-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="b6fe9-111">Dokumentets ruteplanlægningsagent som elektronisk rapporteringsdestination for udgående dokumenter</span><span class="sxs-lookup"><span data-stu-id="b6fe9-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="b6fe9-112">[![Aktivere funktionen til ER-printerdestination i Funktionsstyring](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="b6fe9-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="b6fe9-113">Anvendelighed</span><span class="sxs-lookup"><span data-stu-id="b6fe9-113">Applicability</span></span>

<span data-ttu-id="b6fe9-114">**Printer**-destinationen kan kun konfigureres for filkomponenter, der bruges til at generere output enten i PDF-format, der kan udskrives (PDF-fletning eller PDF-filformatelementer) eller Microsoft Office Excel/Word-format (Excel-fil).</span><span class="sxs-lookup"><span data-stu-id="b6fe9-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="b6fe9-115">Når der genereres output i PDF-format, sendes det til en printer.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="b6fe9-116">Når der genereres output i Microsoft Office-format, konverteres det automatisk til PDF-format og sendes derefter til en printer.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="b6fe9-117">Begrænsninger</span><span class="sxs-lookup"><span data-stu-id="b6fe9-117">Limitations</span></span>

<span data-ttu-id="b6fe9-118">Denne funktion er en prøveversionsfunktion og er underlagt de vilkår for anvendelse, der er beskrevet i [Supplerende vilkår for anvendelse for Microsoft Dynamics 365-prøveversioner](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="b6fe9-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="b6fe9-119">**Printer**-destinationen implementeres kun i forbindelse med installationer i skyen.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="b6fe9-120">Brug printerdestinationen</span><span class="sxs-lookup"><span data-stu-id="b6fe9-120">Use the Printer destination</span></span>

1. <span data-ttu-id="b6fe9-121">Angiv indstillingen **Aktiveret** til **Ja** for at sende et genereret dokument til en printer.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="b6fe9-122">I feltet **Printernavn** skal du vælge den ønskede netværksprinter.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="b6fe9-123">Angiv indstillingen **Gem i udskriftsarkiv?** til **Ja** for at gemme det genererede output i udskriftsarkivet, så det er tilgængeligt til yderligere udskrivning.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="b6fe9-124">Hvis du senere vil have adgang til arkiveret, skal du gå til **Organisationsadministration** \> **Forespørgsler og rapporter** \> **Rapportarkiv**.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="b6fe9-125">[![Brug af printerdestinationen](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="b6fe9-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b6fe9-126">Indstillingen **Konverter til PDF** behøver ikke at blive aktiveret, når du konfigurer destinationen **Printer**.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="b6fe9-127">PDF-konvertering til udskrivningsformål sker, også selvom indstillingen er slået fra.</span><span class="sxs-lookup"><span data-stu-id="b6fe9-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6fe9-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b6fe9-128">Additional resources</span></span>

- [<span data-ttu-id="b6fe9-129">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="b6fe9-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="b6fe9-130">Destinationer for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="b6fe9-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
