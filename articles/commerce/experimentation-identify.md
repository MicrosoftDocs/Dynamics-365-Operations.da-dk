---
title: Identificere en hypotese og fastslå målepunkter for et eksperiment
description: Dette emne indeholder en beskrivelse af, hvordan du kan identificere hypoteser og succesmålepunkter for et eksperiment, du kører på et e-handelswebsted i Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930162"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="7ee52-103">Identificere en hypotese og fastslå succesmålepunkter for et eksperiment</span><span class="sxs-lookup"><span data-stu-id="7ee52-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="7ee52-104">Den første fase i eksperiments livscyklus omfatter identifikation af hypotesen til eksperimentet og bestemmelse af, hvilke målepunkter du vil spore for at evaluere succesen.</span><span class="sxs-lookup"><span data-stu-id="7ee52-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="7ee52-105">I følgende diagram vises alle de trin, der er nødvendige for at [konfigurere og køre et eksperiment](experimentation-overview.md) på et e-handelswebsted i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7ee52-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="7ee52-106">Yderligere trin behandles i separate emner.</span><span class="sxs-lookup"><span data-stu-id="7ee52-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="7ee52-107">[ ![Eksperimenteringens brugerrejse - identifikation](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="7ee52-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="7ee52-108">En hypotese er et udsagn, hvor du forudsiger resultatet af eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="7ee52-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="7ee52-109">Mange faktorer går ud på at definere en hypotese, f.eks. research om brugeradfærd og webstedsdata, du har indsamlet.</span><span class="sxs-lookup"><span data-stu-id="7ee52-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="7ee52-110">Med hypotesen kan du definere den antagelse eller teori, du vil validere med dit eksperiment.</span><span class="sxs-lookup"><span data-stu-id="7ee52-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="7ee52-111">Et eksempel på en hypotese til dit eksperiment kan være "*et billede af en hvid t-shirt på min startside vil skabe mere trafik end en sweater i sommermånederne, da folk vil være let påklædt i lyse farver om sommeren*".</span><span class="sxs-lookup"><span data-stu-id="7ee52-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="7ee52-112">I dette tilfælde skal du oprette variationer, der omfatter en hvid t-shirt og en sweater, og publicere begge dele på samme tid.</span><span class="sxs-lookup"><span data-stu-id="7ee52-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="7ee52-113">Hvis du vil validere en hypotese, skal det vellykkede eller mislykkede eksperiment være direkte knyttet til brugerhandlinger. Hvis webstedets bruger f.eks. klikker på et link eller en knap.</span><span class="sxs-lookup"><span data-stu-id="7ee52-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks a link or button.</span></span> <span data-ttu-id="7ee52-114">Disse handlinger skal svare til hændelser, der rapporteres til en tredjepartstjenestes sporing af eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="7ee52-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="7ee52-115">Over tid vil den procentdel af brugerne, der udfører handlingen, blive talt som en metrikværdi, som du kan bruge til at generere rapporter og foretage analyser.</span><span class="sxs-lookup"><span data-stu-id="7ee52-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="7ee52-116">Du kan se alle tilgængelige hændelser og attributter i emnet [Commerce-komponenthændelser for diagnosticering og fejlfinding](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="7ee52-116">Refer to the [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) topic to review all of the available events and attributes.</span></span>

## <a name="previous-step"></a><span data-ttu-id="7ee52-117">Forrige trin</span><span class="sxs-lookup"><span data-stu-id="7ee52-117">Previous step</span></span>
[<span data-ttu-id="7ee52-118">Eksperimenteren i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7ee52-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="7ee52-119">Næste trin</span><span class="sxs-lookup"><span data-stu-id="7ee52-119">Next step</span></span>
[<span data-ttu-id="7ee52-120">Konfigurere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="7ee52-120">Set up an experiment</span></span>](experimentation-setup.md)
