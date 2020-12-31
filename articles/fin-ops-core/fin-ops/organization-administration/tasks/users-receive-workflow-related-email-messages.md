---
title: Aktivér brugerne til at modtage e-mails, der er relateret til arbejdsgangen
description: Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b7a953ea54286a7e48b392728d2cc9bb2902072
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692812"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="a0a38-103">Aktivér brugerne til at modtage e-mails, der er relateret til arbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="a0a38-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0a38-104">Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="a0a38-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="a0a38-105">For eksempel kan e-mails sendes til brugerne, når dokumenter tildeles til dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="a0a38-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="a0a38-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="a0a38-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a0a38-107">Gå til **Navigationsrude > Moduler > Systemadministration > Brugere > Brugere**.</span><span class="sxs-lookup"><span data-stu-id="a0a38-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="a0a38-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a0a38-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a0a38-109">Klik på **Brugerindstillinger** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="a0a38-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="a0a38-110">Klik på fanen **Arbejdsgang**. Kontrollér, at sektionen **Beskeder** er udvidet.</span><span class="sxs-lookup"><span data-stu-id="a0a38-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="a0a38-111">I sektionen **Beskeder** kan du angive, hvordan du ønsker, brugeren skal have besked om hændelser, der er relateret til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="a0a38-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="a0a38-112">Vælg en indstilling i feltet **Beskedtype for arbejdsgang for linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="a0a38-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="a0a38-113">Grupperet – beskeder om linjeelementer grupperes i en enkelt e-mail.</span><span class="sxs-lookup"><span data-stu-id="a0a38-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="a0a38-114">Individuelt – der sendes en e-mail for hvert linjeelement.</span><span class="sxs-lookup"><span data-stu-id="a0a38-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="a0a38-115">Hvis du ønsker, at brugeren skal modtage beskeder i klienten, skal du markere afkrydsningsfeltet **Send beskeder i e-mail**.</span><span class="sxs-lookup"><span data-stu-id="a0a38-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="a0a38-116">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a0a38-116">Click **Save**.</span></span>
7. <span data-ttu-id="a0a38-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a38-117">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="a0a38-118">E-mailskabelonerne til arbejdsgangen leveres fra enten systemmailskabeloner eller virksomhedsmailskabeloner, afhængigt af om arbejdsgangen er på systemniveau (ikke firmaspecifik) eller på virksomhedsniveau (firmaspecifik).</span><span class="sxs-lookup"><span data-stu-id="a0a38-118">The workflow email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>
