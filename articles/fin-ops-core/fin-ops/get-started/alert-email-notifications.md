---
title: Klientpåmindelsesbeskeder via e-mail
description: Dette emne indeholder oplysninger om, hvordan du opretter regler, der sender e-mailbeskeder om foruddefinerede hændelser, der indtræffer.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a0cf8037ba151bb4e68da1cf4609fb2e4806303a
ms.sourcegitcommit: b952b9f9066a5317259b8344db4c5d99eab4bf3c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/25/2020
ms.locfileid: "3165769"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="1cf79-103">Klientpåmindelsesbeskeder via mail</span><span class="sxs-lookup"><span data-stu-id="1cf79-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cf79-104">Du kan definere brugerdefinerede regler for påmindelser, som overvåger filtrerede visninger af data og automatisk sender e-mailbeskeder, når foruddefinerede hændelser indtræffer.</span><span class="sxs-lookup"><span data-stu-id="1cf79-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="1cf79-105">Muligheden for at sende e-mailbeskeder er tilgængelig for alle understøttede typer af påmindelser og kan også aktiveres for eksisterende påmindelsesregler.</span><span class="sxs-lookup"><span data-stu-id="1cf79-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="1cf79-106">Du kan bruge indbyggede kontrolelementer til at oprette påmindelsesregler, der overvåger de filtrerede visninger af batchjob i systemet.</span><span class="sxs-lookup"><span data-stu-id="1cf79-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="1cf79-107">Ved at overvåge værdien af feltet **Status** kan du også konfigurere regler for påmindelser, der sender e-mail, når der opstår fejl i et batchjob.</span><span class="sxs-lookup"><span data-stu-id="1cf79-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="1cf79-108">Når disse påmindelsesregler oprettes, behøver du ikke længere at kontrollere, om der er ændringer af forretningsdata i rapporter.</span><span class="sxs-lookup"><span data-stu-id="1cf79-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="1cf79-109">Du kan i stedet lade den intelligente ændringsregistreringstjeneste foretage overvågning for dig.</span><span class="sxs-lookup"><span data-stu-id="1cf79-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="1cf79-110">Klientpåmindelser afhænger af det e-mailundersystem, der leveres via integration med Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="1cf79-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="1cf79-111">Det anbefales, at du bruger SMTP-udbyderen (Simple Mail Transfer Protocol), så e-maildistribution ikke behøver at kræve en lokal mailklient.</span><span class="sxs-lookup"><span data-stu-id="1cf79-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="1cf79-112">Hvis du vil sende beskeder via e-mail, skal kunder konfigurere integrerede e-mailtjenester.</span><span class="sxs-lookup"><span data-stu-id="1cf79-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="1cf79-113">E-mailbeskederne sendes til modtagerne på vegne af påmindelsesejere.</span><span class="sxs-lookup"><span data-stu-id="1cf79-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="1cf79-114">Yderligere oplysninger om, hvordan du kan konfigurere e-mail, finder du i [Konfigurere og sende e-mail](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="1cf79-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="1cf79-115">Følgende billede viser **Opret påmindelsesregel** dialogboksen, som nu indeholder en **Send e-mail** indstilling.</span><span class="sxs-lookup"><span data-stu-id="1cf79-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="1cf79-116">[![Dialogboksen Opret påmindelsesregel, hvor indstillingen Send e-mail er sat til Ja](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="1cf79-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="1cf79-117">Når **Send e-mail** er indstillet til **Ja**, bliver påmindelsesbeskeder fortsat leveret via Handlingscenter.</span><span class="sxs-lookup"><span data-stu-id="1cf79-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="1cf79-118">E-mailskabeloner til påmindelsesbeskeder</span><span class="sxs-lookup"><span data-stu-id="1cf79-118">Alert notification email templates</span></span>

<span data-ttu-id="1cf79-119">Tjenesten sender e-mailbeskeder ved hjælp af foruddefinerede e-mailskabeloner, der leverer de grundlæggende oplysninger om påmindelsesbeskeden.</span><span class="sxs-lookup"><span data-stu-id="1cf79-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="1cf79-120">Følgende billede viser strukturen af påmindelsesbeskederne, når de modtages via e-mail.</span><span class="sxs-lookup"><span data-stu-id="1cf79-120">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="1cf79-121">[![Skabelonbaserede påmindelsesbeskeder til oprettelse af poster, ændringer af felter og sletning af skabelon](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="1cf79-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
