---
title: Kontrollere, at dobbeltskrivning er konfigureret i Finance and Operations-apps og Common Data Service
description: I dette emne forklares det, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i Finance and Operations-apps og i Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172639"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="f5534-103">Kontrollere, at dobbeltskrivning er konfigureret i Finance and Operations-apps og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f5534-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f5534-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f5534-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="f5534-105">Der redegøres specifikt for, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i Finance and Operations-apps og i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f5534-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="f5534-106">Kontrollere, at dobbeltskrivning er konfigureret i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="f5534-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="f5534-107">Hvis du vil finde ud af, om de fejl, du ser, når du forsøger at gemme poster til opdatering, kommer fra dobbeltskrivning, skal du først kontrollere, at dobbeltskrivning er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="f5534-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="f5534-108">Hvis du har administratorrettigheder i Finance and Operations-appen, skal du gå til **Arbejdsområder \> Datastyring** og vælge feltet **Dobbeltskrivning**.</span><span class="sxs-lookup"><span data-stu-id="f5534-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="f5534-109">Hvis detaljerne for de sammenkædede miljøer og listen over enhedstilknytninger, der kører, vises, er dobbeltskrivning konfigureret.</span><span class="sxs-lookup"><span data-stu-id="f5534-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![Kontrollere Finance and Operations-appforbindelsen, når du har administratorrettigheder](media/verify_fin_ops_1.png)

+ <span data-ttu-id="f5534-111">Hvis du ikke har administratorrettigheder, modtager du fejlmeddelelsen *Der kan ikke skrives data til enheden \<enhedsnavn\>*.</span><span class="sxs-lookup"><span data-stu-id="f5534-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="f5534-112">I eksemplet i følgende illustration kan du ikke oprette en kundepost i Finance and Operations-appen, fordi dobbeltskrivning er konfigureret, men referencedataene for debitorgruppen og betalingsbetingelser findes ikke i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f5534-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![Kontrollere Finance and Operations-appforbindelsen, når du ikke har administratorrettigheder](media/verify_fin_ops_2.png)

<span data-ttu-id="f5534-114">Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Finance and Operations-apps, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="f5534-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="f5534-115">Kontrollere, at dobbeltskrivning er konfigureret i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f5534-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="f5534-116">Når du opretter data, og du ser feltet **Firma** på siderne i Common Data Service, er dobbeltskrivning konfigureret.</span><span class="sxs-lookup"><span data-stu-id="f5534-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![Kontrollere Common Data Service-forbindelsen](media/verify_cds.png)

<span data-ttu-id="f5534-118">Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Common Data Service, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="f5534-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="f5534-119">Du kan finde oplysninger om, hvordan du kan få vist detaljer om fejl, hvis der opstår fejl, mens du opretter data i Common Data Service, under [Aktivere og få vist sporingsloggen for plug-ins i Common Data Service for at få vist detaljer om fejl](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="f5534-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>
