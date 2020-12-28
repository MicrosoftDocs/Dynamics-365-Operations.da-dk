---
title: Skjule leveringsmåder uden fragtmand i forsendelsesindstillingerne i POS
description: Dette emne beskriver en konfigurationsindstilling, der kan forhindre leveringsmåder uden fragtmand i at blive vist som valgmulighed, når der oprettes forsendelsesordrer i POS.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 38d57ed5f8d2b8725cd11156f0135988bb76e047
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411167"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="bcade-103">Skjule leveringsmåder uden fragtmand i forsendelsesindstillingerne i POS</span><span class="sxs-lookup"><span data-stu-id="bcade-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bcade-104">Dette emne beskriver en konfigurationsindstilling, der er tilgængelig for POS-programmet.</span><span class="sxs-lookup"><span data-stu-id="bcade-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="bcade-105">Denne konfigurationsindstilling ændrer funktionaliteten af den valgte leveringsmåde, når der oprettes forsendelsesordrer i POS.</span><span class="sxs-lookup"><span data-stu-id="bcade-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="bcade-106">Når brugere opretter kundeforsendelsesordrer i POS, kan de vælge en leveringsmåde for forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="bcade-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="bcade-107">Denne funktionalitet er tilgængelig, uanset om hele ordren leveres eller kun udvalgte linjer.</span><span class="sxs-lookup"><span data-stu-id="bcade-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="bcade-108">Som standard viser dialogboksen, hvor der vælges leveringsmåde, alle de gyldige leveringsmåder for kombinationen af en kanal, en vare og en leveringsadresse.</span><span class="sxs-lookup"><span data-stu-id="bcade-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="bcade-109">Disse leveringsmåder defineres på siden **Leveringsmåder** i Headquarters (**Salg og marketing \> Opsætning \> Fordeling \> Leveringsmåder**).</span><span class="sxs-lookup"><span data-stu-id="bcade-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="bcade-110">Leveringsmåder uden fragtmand som f.eks. **Udfør** eller **Afhentning** kan også vises som valg i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bcade-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="bcade-111">Der er dog tilføjet en funktion, som giver dig mulighed for at skjule leveringsmåder uden fragtmand i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bcade-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="bcade-112">Hvis du vil aktivere denne funktion, skal du på siden **Commerce-parametre** under fanen **Kundeordrer** angive indstillingen **Vis kun fragtmandstilstande for indstillingen forsendelsesordrer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bcade-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="bcade-113">Når du har aktiveret denne funktion og kører de relevante distributionsjob for at synkronisere oplysningerne til kanaldatabasen, vises leveringsmåder uden fragtmand ikke som muligt valg under processen til oprettelse af forsendelsesordrer i POS.</span><span class="sxs-lookup"><span data-stu-id="bcade-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>
