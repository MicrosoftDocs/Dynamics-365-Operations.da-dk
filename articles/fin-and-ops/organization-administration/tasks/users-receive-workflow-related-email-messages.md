---
title: Aktivér brugerne til at modtage e-mails, der er relateret til arbejdsgangen
description: Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6800d02878123388611d35760123d0215e9d539f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "344587"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="807c6-103">Aktivér brugerne til at modtage e-mails, der er relateret til arbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="807c6-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="807c6-104">Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="807c6-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="807c6-105">For eksempel kan e-mails sendes til brugerne, når dokumenter tildeles til dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="807c6-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="807c6-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="807c6-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="807c6-107">Gå til Systemadministration > Brugere > Brugere.</span><span class="sxs-lookup"><span data-stu-id="807c6-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="807c6-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="807c6-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="807c6-109">Klik på Brugerindstillinger.</span><span class="sxs-lookup"><span data-stu-id="807c6-109">Click User options.</span></span>
4. <span data-ttu-id="807c6-110">Klik på fanen Arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="807c6-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="807c6-111">Sørg for, at sektionen Beskeder er udvidet.</span><span class="sxs-lookup"><span data-stu-id="807c6-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="807c6-112">I sektionen Beskeder kan du angive, hvordan du ønsker, brugeren skal have besked om hændelser, der er relateret til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="807c6-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="807c6-113">Vælg en indstilling i feltet Beskedtype for arbejdsgang for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="807c6-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="807c6-114">Grupperet – beskeder om linjeelementer grupperes i en enkelt e-mail.</span><span class="sxs-lookup"><span data-stu-id="807c6-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="807c6-115">Individuelt – der sendes en e-mail for hvert linjeelement.</span><span class="sxs-lookup"><span data-stu-id="807c6-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="807c6-116">Hvis du ønsker, at brugeren skal modtage beskeder i klienten, skal du markere afkrydsningsfeltet Send beskeder i e-mail.</span><span class="sxs-lookup"><span data-stu-id="807c6-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="807c6-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="807c6-117">Click Save.</span></span>
7. <span data-ttu-id="807c6-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="807c6-118">Close the page.</span></span>

