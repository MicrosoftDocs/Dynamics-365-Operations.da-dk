---
title: Kontrollere konfiguration af dobbeltskrivning i Finance and Operations-apps og Dataverse
description: I dette emne forklares det, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i Finance and Operations-apps og i Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: af746d1d20ddd1552bce797288c6d62d69d7bd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748843"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="3cec6-103">Kontrollere konfiguration af dobbeltskrivning i Finance and Operations-apps og Dataverse</span><span class="sxs-lookup"><span data-stu-id="3cec6-103">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="3cec6-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3cec6-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="3cec6-105">Der redegøres specifikt for, hvordan du kan bestemme, om dobbeltskrivning er konfigureret i Finance and Operations-apps og i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3cec6-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="3cec6-106">Kontrollere, at dobbeltskrivning er konfigureret i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="3cec6-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="3cec6-107">Hvis du vil finde ud af, om de fejl, du ser, når du forsøger at gemme rækker til opdatering, kommer fra dobbeltskrivning, skal du først kontrollere, at dobbeltskrivning er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="3cec6-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="3cec6-108">Hvis du har administratorrettigheder i Finance and Operations-appen, skal du gå til **Arbejdsområder \> Datastyring** og vælge feltet **Dobbeltskrivning**.</span><span class="sxs-lookup"><span data-stu-id="3cec6-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="3cec6-109">Hvis detaljerne for de sammenkædede miljøer og listen over tabeltilknytninger, der kører, vises, er dobbeltskrivning konfigureret.</span><span class="sxs-lookup"><span data-stu-id="3cec6-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Kontrollere Finance and Operations-appforbindelsen, når du har administratorrettigheder](media/verify_fin_ops_1.png)

+ <span data-ttu-id="3cec6-111">Hvis du ikke har administratorrettigheder, modtager du fejlmeddelelsen *Der kan ikke skrives data til enheden \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="3cec6-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="3cec6-112">I eksemplet i følgende illustration kan du ikke oprette en kunderække i Finance and Operations-appen, fordi dobbeltskrivning er konfigureret, men referencedataene for debitorgruppen og betalingsbetingelser findes ikke i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3cec6-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Kontrollere Finance and Operations-appforbindelsen, når du ikke har administratorrettigheder](media/verify_fin_ops_2.png)

<span data-ttu-id="3cec6-114">Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Finance and Operations-apps, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="3cec6-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="3cec6-115">Kontrollere, at dobbeltskrivning er konfigureret i Dataverse</span><span class="sxs-lookup"><span data-stu-id="3cec6-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="3cec6-116">Når du opretter data, og du ser kolonnen **Firma** på siderne i Dataverse, er dobbeltskrivning konfigureret.</span><span class="sxs-lookup"><span data-stu-id="3cec6-116">When you create data, if you see the **Company** column on pages in Dataverse, dual-write is configured.</span></span>

![Kontrollere Dataverse-forbindelsen](media/verify_cds.png)

<span data-ttu-id="3cec6-118">Du kan finde flere oplysninger om, hvordan du løser problemer, når du opretter data i Dataverse, under [Fejlfinding i forbindelse med problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="3cec6-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="3cec6-119">Du kan finde oplysninger om, hvordan du kan få vist detaljer om fejl, hvis der opstår fejl, mens du opretter data i Dataverse, under [Aktivere og få vist sporingsloggen for plug-ins i Dataverse for at få vist detaljer om fejl](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="3cec6-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]