---
title: Systemadministratorer kan ikke fjerne ordrehold, fordi de ikke er godkendt
description: Systemadministratorer kan ikke fjerne ordrehold, fordi de ikke er godkendt.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026388"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="43bd4-103">Systemadministratorer kan ikke fjerne ordrehold, fordi de ikke er godkendt</span><span class="sxs-lookup"><span data-stu-id="43bd4-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="43bd4-104">KB-nummer: 4614642</span><span class="sxs-lookup"><span data-stu-id="43bd4-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="43bd4-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="43bd4-105">Symptoms</span></span>

<span data-ttu-id="43bd4-106">Systemadministratorer kan ikke fjerne salgsordrehold, medmindre de har den specifikke rolle, der er tildelt i koden for ordreholdet.</span><span class="sxs-lookup"><span data-stu-id="43bd4-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="43bd4-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="43bd4-107">Resolution</span></span>

<span data-ttu-id="43bd4-108">Adgangen til visse handlinger, f.eks. fjernelse af salgsordrehold, er baseret på konfigurationen af en forretningspolitik.</span><span class="sxs-lookup"><span data-stu-id="43bd4-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="43bd4-109">Systemadministratorer har typisk ikke tilladelse til at udføre handlinger af denne type.</span><span class="sxs-lookup"><span data-stu-id="43bd4-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="43bd4-110">Adgangen til at udføre en bestemt opgave styres oftere af forretningspolitikker, og kun bestemte personer i en organisation er godkendt til at udføre den pågældende opgave.</span><span class="sxs-lookup"><span data-stu-id="43bd4-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="43bd4-111">Eksempler omfatter godkendelser, der er resultatet af godkendelser af arbejdsgange, og specifikke opgaver, der er resultatet af en arbejdsgangskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="43bd4-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="43bd4-112">Selvom der ikke er knyttet nogen arbejdsgang til ordrehold, er princippet det samme.</span><span class="sxs-lookup"><span data-stu-id="43bd4-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="43bd4-113">En relevant rolle tildeler den specifikke gruppe personer i en organisation, som har ret til at fjerne ordrehold.</span><span class="sxs-lookup"><span data-stu-id="43bd4-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="43bd4-114">Denne rettighed skal ikke nødvendigvis tildeles til alle administratorer, da denne fremgangsmåde overtræder den definerede forretningspolitik.</span><span class="sxs-lookup"><span data-stu-id="43bd4-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
