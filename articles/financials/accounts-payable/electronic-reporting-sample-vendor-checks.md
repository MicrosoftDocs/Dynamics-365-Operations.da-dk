---
title: Kreditoreksempelchecks til elektronisk rapportering
description: Dette emne indeholder generelle oplysninger om brug af eksempelcheckformater i elektronisk rapportering.
author: ShylaThompson
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6cae0ce1ec88f0500f8d281d314d59dc7001a384
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

[!include [banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a><span data-ttu-id="7bc6a-103">Eksempelcheckformater til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="7bc6a-103">Electronic reporting sample check formats</span></span>

<span data-ttu-id="7bc6a-104">Du kan bruge elektronisk rapportering (ER) til at formatere kreditorchecks.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="7bc6a-105">Der findes mange checkformater, som er specifikke for bank- og checkudbyderen, på markedet.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="7bc6a-106">Der er medtaget eksempelcheckformater i betalingscheckmodellen i værktøjslageret i elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="7bc6a-107">Disse eksempelchecks kaldes **Check i midten (USA)** og **Check på øverste talon nedenfor (USA)**.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="7bc6a-108">Hvilke checkformater understøttes i øjeblikket?</span><span class="sxs-lookup"><span data-stu-id="7bc6a-108">What check formats are currently supported?</span></span>

<span data-ttu-id="7bc6a-109">Du bør altid gå til biblioteket med delte aktiver i Microsoft Dynamics Lifecycle Services (LCS) og få vist den aktuelle liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="7bc6a-110">Næste afsnit, "Hvad skal jeg bruge for at komme i gang?", indeholder et link til et emne, der forklarer, hvordan du opretter et LCS-lager, så du kan se tilgængelige konfigurationer og importere valgte konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="7bc6a-111">Microsoft Dynamics 365 for Finance and Operations edition omfatter et eksempelformat, hvor checken er øverst efterfulgt af to sektioner til remittering.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-111">Microsoft Dynamics 365 for Finance and Operations, includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="7bc6a-112">Det omfatter også et eksempelformat, hvor checken er i midten mellem to remitteringsafsnit.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="7bc6a-113">Disse eksempelformater svarer til Deluxe-forretningscheckformater.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="7bc6a-114">Hvad skal jeg bruge for at komme i gang?</span><span class="sxs-lookup"><span data-stu-id="7bc6a-114">What do I have to set up?</span></span>

- <span data-ttu-id="7bc6a-115">Før du kan udskrive checks ved hjælp af ER, skal mindst én aktiv checkkonfiguration importeres til dine ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="7bc6a-116">Du kan finde vejledning i [Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="7bc6a-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
- <span data-ttu-id="7bc6a-117">Når du konfigurerer check i Kontant- og bankstyring for bankkontoen, skal du markere afkrydsningsfeltet **Generisk elektronisk eksportformat** og derefter vælge det relevante checkformat som en eksportformatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="7bc6a-118">Du skal også angive antallet af bilagslinjer, der skal udskrives på remitteringen.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="7bc6a-119">Husk at medtage overskriftsrækker, når du beregner dette tal.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="7bc6a-120">For de to eksempelformater er det anbefalede antal følgeseddellinjer 17.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="7bc6a-121">Men dette nummer varierer afhængigt af din checkbeholdning og printerdriverne.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="7bc6a-122">Det anbefales at udskrive en prøvecheck for at validere checklayoutet.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="7bc6a-123">For at udskrive en prøvecheck skal du vælge indstillingen **Udskriv prøve**.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="7bc6a-124">Eksempelcheckformaterne fungerer bedst, når **Margener** er indstillet til **Ingen** i de avancerede printeregenskaber for Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="7bc6a-125">Når prøvechecken er oprettet, skal du aktivere redigering af Excel-outputtet og konfigurere sidelayoutet, så alle margener er indstillet til **0** (nul).</span><span class="sxs-lookup"><span data-stu-id="7bc6a-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="7bc6a-126">Sammenlign testkopien af checkene med din checkbeholdning, og juster indstillingerne, indtil du er tilfreds med justeringen.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="7bc6a-127">Når du genererer betalinger for den konfigurerede bankkonto i betalingskladden, udskrives checks ved hjælp af det angivne format.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="7bc6a-128">Du kan finde flere oplysninger under [Redigere et elektronisk rapporteringsformat](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="7bc6a-128">For more information, see [Modify an Electronic reporting format](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

