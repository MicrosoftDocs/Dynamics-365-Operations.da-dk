---
title: Konfigurere bedragerimeddelelser
description: "Dette emne forklarer, hvordan du opretter regler for at advare kundeservicemedarbejdere om potentielt falske oplysninger ved behandling af ordrer. Du kan definere bestemte koder, der skal bruges for automatisk eller manuelt at sætte mistænkelige ordrer på hold."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="a728a-104">Konfigurere bedragerimeddelelser</span><span class="sxs-lookup"><span data-stu-id="a728a-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a728a-105">Dette emne forklarer, hvordan du opretter regler for at advare kundeservicemedarbejdere om potentielt falske oplysninger ved behandling af ordrer.</span><span class="sxs-lookup"><span data-stu-id="a728a-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="a728a-106">Du kan definere bestemte koder, der skal bruges for automatisk eller manuelt at sætte mistænkelige ordrer på hold.</span><span class="sxs-lookup"><span data-stu-id="a728a-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="a728a-107">Før du konfigurerer og bruger regler til kontrol af bedrageri, skal du aktivere kontrol af bedrageri og definere de grundlæggende værdier for kontrol af bedrageri i parametrene for callcentret.</span><span class="sxs-lookup"><span data-stu-id="a728a-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="a728a-108">Der findes to typer bedrageriregler:</span><span class="sxs-lookup"><span data-stu-id="a728a-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="a728a-109">**Statiske regler** bruger en bestemt værdi, f.eks. et telefonnummer, der er blevet blacklistet.</span><span class="sxs-lookup"><span data-stu-id="a728a-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="a728a-110">**Dynamisk regler** kan oprettes ud fra variabler og betingelser.</span><span class="sxs-lookup"><span data-stu-id="a728a-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="a728a-111">Før du kan oprette en dynamisk regel, skal du oprette de variabler og betingelser, der definerer, hvem reglen gælder for, og hvor reglen skal anvendes.</span><span class="sxs-lookup"><span data-stu-id="a728a-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="a728a-112">Det kan f.eks. være, at du vil oprette en regel, der kræver, at en salgsordre, som debitor 1202 afgiver, og som har en værdi på 1.000,0 eller mere, skal sættes på hold, indtil debitorbetalingen kan kontrolleres.</span><span class="sxs-lookup"><span data-stu-id="a728a-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="a728a-113">I dette tilfælde er variablerne debitor 1202 og en ordretotal på 1.000,00.</span><span class="sxs-lookup"><span data-stu-id="a728a-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="a728a-114">Betingelsen angiver, at hvis debitor 1202 afgiver en ordre, og det samlede beløb på ordren er lig med eller mere end 1.000,00, skal salgsordren sættes på hold, indtil debitorbetalingen kan kontrolleres.</span><span class="sxs-lookup"><span data-stu-id="a728a-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




