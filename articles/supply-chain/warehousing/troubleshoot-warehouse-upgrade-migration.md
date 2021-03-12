---
title: Foretage fejlfinding af opgradering og migrering til avanceret lokationsstyring
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du opgraderer og overfører til avanceret lokationsstyring.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993862"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="5fee5-103">Foretage fejlfinding af opgradering og migrering til avanceret lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="5fee5-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fee5-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du opgraderer og overfører til avanceret lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="5fee5-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="5fee5-105">Jeg får vist følgende fejlmeddelelse: "java.security.cert.certPathValidatorException: Tillidsanker for certificeringsstien blev ikke fundet".</span><span class="sxs-lookup"><span data-stu-id="5fee5-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5fee5-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="5fee5-106">Issue description</span></span>

<span data-ttu-id="5fee5-107">Du modtager denne fejlmeddelelse i lagerstedsappen, fordi der ikke er tillid til selvsignerede certifikater på Android 8 + i lokale miljøer.</span><span class="sxs-lookup"><span data-stu-id="5fee5-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5fee5-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="5fee5-108">Issue resolution</span></span>

<span data-ttu-id="5fee5-109">Brug et eksternt (offentligt) nøglecenter.</span><span class="sxs-lookup"><span data-stu-id="5fee5-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="5fee5-110">Der findes en rettelse til dette problem i version 1.9.0.0 af lagerstedsappen.</span><span class="sxs-lookup"><span data-stu-id="5fee5-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="5fee5-111">Du kan finde flere oplysninger om dette problem, og hvordan det løses, under [Foretage fejlfinding af problemer med forbindelsen til lagerstedsappen](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5fee5-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="5fee5-112">Hvad er den godkendte proces for flytning fra grundlæggende lagerstyring til avanceret lagerstyring?</span><span class="sxs-lookup"><span data-stu-id="5fee5-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="5fee5-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="5fee5-113">Issue description</span></span>

<span data-ttu-id="5fee5-114">Du kører i øjeblikket under lagerbeholdning/lagerstyring og bruger grundlæggende lagerbeholdningsfunktioner, og du vil flytte til avanceret lagerstyring for at udnytte mobilenheder, -bølger og -arbejde.</span><span class="sxs-lookup"><span data-stu-id="5fee5-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="5fee5-115">Der opstår dog problemer, når du forsøger at flytte.</span><span class="sxs-lookup"><span data-stu-id="5fee5-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="5fee5-116">Du kan f.eks. ikke ændre dine produkter, så de bruger lagringsdimensioner (sted, lagersted og lokation), da produkterne har transaktioner for dem.</span><span class="sxs-lookup"><span data-stu-id="5fee5-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="5fee5-117">Derfor skal du kende den godkendte proces for flytning fra grundlæggende lagerstyring til avanceret lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="5fee5-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5fee5-118">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="5fee5-118">Issue resolution</span></span>

<span data-ttu-id="5fee5-119">Du kan finde flere oplysninger om processen for flytning fra grundlæggende lagerstyring til avanceret lagerstyring i følgende blogindlæg og dokumentation:</span><span class="sxs-lookup"><span data-stu-id="5fee5-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="5fee5-120">Aktivere lokationsstyringsproces for eksisterende varer og lagersteder</span><span class="sxs-lookup"><span data-stu-id="5fee5-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="5fee5-121">Migrering af Microsoft Dynamics AX WMS til nye R3-lagersteds- og transportfunktioner</span><span class="sxs-lookup"><span data-stu-id="5fee5-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="5fee5-122">WMSI/WMS2-varemigrering</span><span class="sxs-lookup"><span data-stu-id="5fee5-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="5fee5-123">Opgradere lokationsstyring fra Microsoft Dynamics AX 2012 til Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5fee5-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
