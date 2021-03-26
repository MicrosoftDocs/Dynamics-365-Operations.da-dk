---
title: Deaktivere regler i konsistenskontrol af detailtransaktioner
description: Dette emne beskriver funktionen til deaktivering af regler i konsistenskontrol af transaktion i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: abd97819d44963d22269efc9536f746c3c0b3812
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230584"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="21a1c-103">Deaktivere regler i konsistenskontrol af detailtransaktioner</span><span class="sxs-lookup"><span data-stu-id="21a1c-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21a1c-104">Detailhandlere kan have forretningsscenarier og -processer, der er specifikke for dem.</span><span class="sxs-lookup"><span data-stu-id="21a1c-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="21a1c-105">Derfor gælder alle de regler, der som standard er inkluderet i konsistenskontrollen af handelstransaktioner, ikke for alle detailforretninger.</span><span class="sxs-lookup"><span data-stu-id="21a1c-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="21a1c-106">For at sørge for tilpasning til forskellige situationer, indeholder Microsoft Dynamics 365 Commerce funktionalitet, der kan bruges til at deaktivere de regler, der ikke er relevante.</span><span class="sxs-lookup"><span data-stu-id="21a1c-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="21a1c-107">Hvis du vil have vist en liste over de regler, der er tilgængelige i konsistenskontrollen af transaktioner i dit miljø, og have vist status for hver regel, skal du gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre** og vælge fanen **Transaktionsvalidering**.</span><span class="sxs-lookup"><span data-stu-id="21a1c-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="21a1c-108">Status for alle regler angives som standard til **Aktiveret**.</span><span class="sxs-lookup"><span data-stu-id="21a1c-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="21a1c-109">Derfor bruges alle reglerne til at validere transaktioner, før de trækkes ind i handelsopgørelserne.</span><span class="sxs-lookup"><span data-stu-id="21a1c-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="21a1c-110">Hvis du vil deaktivere en regel, skal du ændre dens status til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="21a1c-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="21a1c-111">Deaktiverede regler tages ikke i betragtning, når transaktioner valideres under beregningsprocessen for opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="21a1c-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="21a1c-112">Hvis du vil springe hele valideringsprocessen over, uanset hvilke regler der er aktiveret, skal du gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre** og derefter under fanen **Transaktionsvalidering** angive indstillingen **Deaktiver konsistenskontrol for Commerce-transaktioner** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="21a1c-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="21a1c-113">Når denne indstilling er angivet til **Nej**, kan den ikke indstilles tilbage til **Ja** fra brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="21a1c-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]