---
title: Modul for indtjekning ved afhentning
description: Dette emne omhandler modulet for indtjekning ved afhentning og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e7bae4ae7c2f3367132b03accb31c01c5f3b673e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937571"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="71509-103">Modul for indtjekning ved afhentning</span><span class="sxs-lookup"><span data-stu-id="71509-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="71509-104">Dette emne omhandler modulet for indtjekning ved afhentning og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="71509-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="71509-105">Modulet for indtjekning ved afhentning indeholder en bekræftelsesside til kunder, der bruger Dynamics 365 Commerce-funktionerne til kunders indtjekning for at underrette en butik om deres ankomst.</span><span class="sxs-lookup"><span data-stu-id="71509-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="71509-106">Med modulet for indtjekning ved afhentning kan du også konfigurere en formular, der indsamler yderligere oplysninger fra kunder for at lette ordreleveringen.</span><span class="sxs-lookup"><span data-stu-id="71509-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="71509-107">Disse oplysninger omfatter en kundes parkeringspladssnummer samt mærke og model for kundens køretøj.</span><span class="sxs-lookup"><span data-stu-id="71509-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="71509-108">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="71509-108">Module properties</span></span>

| <span data-ttu-id="71509-109">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="71509-109">Property name</span></span> | <span data-ttu-id="71509-110">Værdier</span><span class="sxs-lookup"><span data-stu-id="71509-110">Values</span></span> | <span data-ttu-id="71509-111">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="71509-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="71509-112">Bekræftelsestekst</span><span class="sxs-lookup"><span data-stu-id="71509-112">Confirmation text</span></span> | <span data-ttu-id="71509-113">Tekststreng</span><span class="sxs-lookup"><span data-stu-id="71509-113">Text string</span></span> | <span data-ttu-id="71509-114">Indhold til den overskrift, som vises på siden for bekræftelse af indtjekning.</span><span class="sxs-lookup"><span data-stu-id="71509-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="71509-115">Vis QR-kode</span><span class="sxs-lookup"><span data-stu-id="71509-115">Show QR code</span></span> | <span data-ttu-id="71509-116">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="71509-116">**True** or **False**</span></span> | <span data-ttu-id="71509-117">Når denne egenskab er angivet til **Sand**, viser siden til bekræftelse af indtjekning en QR-kode, der repræsenterer ordrebekræftelsens id.</span><span class="sxs-lookup"><span data-stu-id="71509-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="71509-118">Overskrift for yderligere oplysninger</span><span class="sxs-lookup"><span data-stu-id="71509-118">Additional information heading</span></span> | <span data-ttu-id="71509-119">Tekststreng</span><span class="sxs-lookup"><span data-stu-id="71509-119">Text string</span></span> | <span data-ttu-id="71509-120">Indhold til den overskrift, der vises, når der er konfigureret felter til yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="71509-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="71509-121">Nøgler for yderligere oplysninger</span><span class="sxs-lookup"><span data-stu-id="71509-121">Additional information keys</span></span> | <span data-ttu-id="71509-122">Par af ressource-id/ressourceværdi</span><span class="sxs-lookup"><span data-stu-id="71509-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="71509-123">Hver nøgle opretter et formularfelt og en tilknyttet etiket, der bruges til at indsamle yderligere oplysninger fra kunder.</span><span class="sxs-lookup"><span data-stu-id="71509-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="71509-124">Nøgler for yderligere oplysninger \> Ressource-id</span><span class="sxs-lookup"><span data-stu-id="71509-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="71509-125">Tekststreng</span><span class="sxs-lookup"><span data-stu-id="71509-125">Text string</span></span> | <span data-ttu-id="71509-126">Hver oplysningsnøgle opretter et formularfelt og en tilknyttet etiket, der bruges til at indsamle yderligere oplysninger fra kunder.</span><span class="sxs-lookup"><span data-stu-id="71509-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="71509-127">Denne egenskab identificerer nøglen for yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="71509-127">This property identifies the additional information key.</span></span> <span data-ttu-id="71509-128">I den opgave, der er oprettet i POS, vises værdien for denne egenskab som etiketten i instruktionsfeltet.</span><span class="sxs-lookup"><span data-stu-id="71509-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="71509-129">Nøgler for yderligere oplysninger \> Ressourceværdi</span><span class="sxs-lookup"><span data-stu-id="71509-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="71509-130">Tekststreng</span><span class="sxs-lookup"><span data-stu-id="71509-130">Text string</span></span> | <span data-ttu-id="71509-131">Etiketten for tekstfeltet i opgaven i POS.</span><span class="sxs-lookup"><span data-stu-id="71509-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="71509-132">Nøgler for yderligere oplysninger \> Påkrævet</span><span class="sxs-lookup"><span data-stu-id="71509-132">Additional information keys \> Required</span></span> | <span data-ttu-id="71509-133">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="71509-133">**True** or **False**</span></span> | <span data-ttu-id="71509-134">Denne egenskab angiver, om debitorerne skal udfylde formularfeltet, før de kan fortsætte.</span><span class="sxs-lookup"><span data-stu-id="71509-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="71509-135">Når denne egenskab er angivet til **Sand**, vises en stjerne ved siden af formularetiketten, og der udføres en null-kontrol for at forhindre debitorer i at fortsætte, hvis der ikke er angivet en værdi.</span><span class="sxs-lookup"><span data-stu-id="71509-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="71509-136">Føje modulet for indtjekning ved afhentning til en side</span><span class="sxs-lookup"><span data-stu-id="71509-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="71509-137">Modulet for indtjekning ved afhentning skal føjes til den nye side, som du opretter til bekræftelse af indtjekning.</span><span class="sxs-lookup"><span data-stu-id="71509-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="71509-138">Denne side fungerer som bekræftelse af indtjekning for kunder, der vælger linket **Jeg er her** eller knappen i deres mail.</span><span class="sxs-lookup"><span data-stu-id="71509-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="71509-139">Konfigurere formularen til yderligere oplysninger</span><span class="sxs-lookup"><span data-stu-id="71509-139">Configure the additional information form</span></span>

<span data-ttu-id="71509-140">Hvis der ikke er konfigureret nøgler for yderligere oplysninger, får kunderne som standard vist modulet for bekræftelse af indtjekning.</span><span class="sxs-lookup"><span data-stu-id="71509-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="71509-141">Når bekræftelsen af indtjekning vises, oprettes der en opgave i POS for den butik, hvor ordren afhentes.</span><span class="sxs-lookup"><span data-stu-id="71509-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="71509-142">Når der er konfigureret en eller flere nøgler for yderligere oplysninger, bliver kunderne først bedt om at angive oplysninger.</span><span class="sxs-lookup"><span data-stu-id="71509-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="71509-143">Når de vælger **Send**, vises bekræftelsen af indtjekning, og der oprettes en opgave i POS.</span><span class="sxs-lookup"><span data-stu-id="71509-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="71509-144">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="71509-144">Additional resources</span></span>

[<span data-ttu-id="71509-145">Aktivere beskeder om kunders indtjekning i POS</span><span class="sxs-lookup"><span data-stu-id="71509-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
