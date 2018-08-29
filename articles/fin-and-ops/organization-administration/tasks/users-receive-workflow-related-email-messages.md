--- 
title: Konfigurere systemet til at sende arbejdsgangsrelateret mail til brugere
description: "Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a><span data-ttu-id="3a51a-103">Konfigurere systemet til at sende arbejdsgangsrelateret mail til brugere</span><span class="sxs-lookup"><span data-stu-id="3a51a-103">Configure the system to send workflow-related email to users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a51a-104">Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="3a51a-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="3a51a-105">For eksempel kan e-mails sendes til brugerne, når dokumenter tildeles til dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="3a51a-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="3a51a-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="3a51a-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3a51a-107">Gå til Systemadministration > Brugere > Brugere.</span><span class="sxs-lookup"><span data-stu-id="3a51a-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="3a51a-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3a51a-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3a51a-109">Klik på Brugerindstillinger.</span><span class="sxs-lookup"><span data-stu-id="3a51a-109">Click User options.</span></span>
4. <span data-ttu-id="3a51a-110">Klik på fanen Arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="3a51a-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="3a51a-111">Sørg for, at sektionen Beskeder er udvidet.</span><span class="sxs-lookup"><span data-stu-id="3a51a-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="3a51a-112">I sektionen Beskeder kan du angive, hvordan du ønsker, brugeren skal have besked om hændelser, der er relateret til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="3a51a-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="3a51a-113">Vælg en indstilling i feltet Beskedtype for arbejdsgang for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="3a51a-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="3a51a-114">Grupperet – beskeder om linjeelementer grupperes i en enkelt e-mail.</span><span class="sxs-lookup"><span data-stu-id="3a51a-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="3a51a-115">Individuelt – der sendes en e-mail for hvert linjeelement.</span><span class="sxs-lookup"><span data-stu-id="3a51a-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="3a51a-116">Hvis du ønsker, at brugeren skal modtage beskeder i klienten, skal du markere afkrydsningsfeltet Send beskeder i e-mail.</span><span class="sxs-lookup"><span data-stu-id="3a51a-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="3a51a-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3a51a-117">Click Save.</span></span>
7. <span data-ttu-id="3a51a-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3a51a-118">Close the page.</span></span>


