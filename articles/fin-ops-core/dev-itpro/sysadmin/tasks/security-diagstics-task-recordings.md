---
title: Sikkerhedsdiagnosticering for opgaveregistreringer
description: Dette emne giver oplysninger om, hvordan du kan analysere og administrere krav til sikkerhedstilladelser på basis af en opgaveregistrering.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: fada3abb9362426c7c9ec33f5d25552edf3ef630
ms.sourcegitcommit: 71fec2553158c332ce4d4bfcedc2c1ab58c1a1a5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2020
ms.locfileid: "3340669"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="b632e-103">Sikkerhedsdiagnosticering for opgaveregistreringer</span><span class="sxs-lookup"><span data-stu-id="b632e-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="b632e-104">Før du begynder</span><span class="sxs-lookup"><span data-stu-id="b632e-104">Before you begin</span></span>

<span data-ttu-id="b632e-105">Dette emne giver oplysninger om, hvordan du kan analysere og administrere krav til sikkerhedstilladelser på basis af en opgaveregistrering.</span><span class="sxs-lookup"><span data-stu-id="b632e-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="b632e-106">Før du fuldfører trinnene i dette emne, skal du have en opgaveregistrering for den forretningsproces, der skal analyseres.</span><span class="sxs-lookup"><span data-stu-id="b632e-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="b632e-107">Du kan registrere en forretningsproces ved at se [Ressourcer for Arbejdsrutineoptager](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="b632e-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="b632e-108">Administrere sikkerhed for en opgaveregistrering</span><span class="sxs-lookup"><span data-stu-id="b632e-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="b632e-109">Gå til **Systemadministration** > **Sikkerhed** > **Sikkerhedsdiagnosticering for opgaveregistrering**.</span><span class="sxs-lookup"><span data-stu-id="b632e-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="b632e-110">Åbn opgaveregistreringen fra dens placering.</span><span class="sxs-lookup"><span data-stu-id="b632e-110">Open the task recording from its location.</span></span> <span data-ttu-id="b632e-111">Vælg **Åbn fra denne pc** eller **Åbn fra Lifecycle Services**, og vælg derefter **Luk**.</span><span class="sxs-lookup"><span data-stu-id="b632e-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="b632e-112">Derved åbnes siden **Detaljer om sikkerhedsmenupunkter**, der viser de sikkerhedsobjekter, der kræves til processen.</span><span class="sxs-lookup"><span data-stu-id="b632e-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="b632e-113">Menupunkterne **Handling** og **Output** er ikke medtaget på listen.</span><span class="sxs-lookup"><span data-stu-id="b632e-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="b632e-114">Vælg en bruger i feltet **Bruger-id**.</span><span class="sxs-lookup"><span data-stu-id="b632e-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="b632e-115">Hvis brugeren ikke har rettigheder til visse menupunkter, opdateres feltet **Manglende tilladelser** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b632e-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Siden Detaljer om sikkerhedsmenupunkter](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="b632e-117">Vælg **Tilføj reference** for at få vist en liste over sikkerhedsobjekterne, herunder roller, pligter og rettigheder, der giver den manglende tilladelse.</span><span class="sxs-lookup"><span data-stu-id="b632e-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="b632e-118">Vælg et sikkerhedsobjekt på listen:</span><span class="sxs-lookup"><span data-stu-id="b632e-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="b632e-119">Hvis **Rolle** er valgt, skal du vælge **Føj rolle til bruger**.</span><span class="sxs-lookup"><span data-stu-id="b632e-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="b632e-120">Derved åbnes siden **Tildel brugere roller**.</span><span class="sxs-lookup"><span data-stu-id="b632e-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="b632e-121">Du kan finde flere oplysninger på siden [Tildele brugere til sikkerhedsroller](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b632e-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="b632e-122">Hvis **Pligt** er valgt, skal du vælge **Føj pligt til rolle**, vælge de roller, som pligten skal føjes til, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="b632e-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="b632e-123">Hvis **Rettighed** er valgt, skal du vælge **Føj rettighed til pligter**, vælge de roller, som pligten skal føjes til, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="b632e-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>