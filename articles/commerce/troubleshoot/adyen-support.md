---
title: Fejlfinding i Dynamics 365 Payment Connector for Adyen-problemer
description: Dette emne indeholder fejlfindingsvejledning, der kan hjælpe dig med at få support, når du har problemer med Microsoft Dynamics 365 Payment Connector for Adyen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 707efeba9553b996e4e33a4754e42a9d22643e33
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019583"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="2826e-103">Fejlfinding i Dynamics 365 Payment Connector for Adyen-problemer</span><span class="sxs-lookup"><span data-stu-id="2826e-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2826e-104">Dette emne indeholder fejlfindingsvejledning, der kan hjælpe dig med at få support, når du har problemer med Microsoft Dynamics 365 Payment Connector for Adyen.</span><span class="sxs-lookup"><span data-stu-id="2826e-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="2826e-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2826e-105">Description</span></span>

<span data-ttu-id="2826e-106">Du har problemer med Dynamics 365 Payment Connector for Adyen i følgende områder, og du har brug for support fra Adyen-teamet:</span><span class="sxs-lookup"><span data-stu-id="2826e-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="2826e-107">POS (Configuration of Point of sale), MPOS (Modern Point of sale), call center eller Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2826e-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="2826e-108">Adyens betalingsserviceudbyders (PSP) referencenummer (f.eks. hvis du har spørgsmål om afvisning, herunder manuel indtastning af \[MKE\]-afvisning)</span><span class="sxs-lookup"><span data-stu-id="2826e-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="2826e-109">Alt, hvad der ikke fungerer i testmiljøer eller live forhandlermiljøer</span><span class="sxs-lookup"><span data-stu-id="2826e-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="2826e-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="2826e-110">Resolution</span></span>

<span data-ttu-id="2826e-111">Du kan bruge følgende mailskabelon til at starte supportprocessen med Adyen-teamet.</span><span class="sxs-lookup"><span data-stu-id="2826e-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="2826e-112">Hvis du vil foretage fejlfinding, skal du sørge for, at mailen indeholder alle de nødvendige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2826e-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="2826e-113">Felt</span><span class="sxs-lookup"><span data-stu-id="2826e-113">Field</span></span>        | <span data-ttu-id="2826e-114">Værdi</span><span class="sxs-lookup"><span data-stu-id="2826e-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="2826e-115">Til</span><span class="sxs-lookup"><span data-stu-id="2826e-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="2826e-116">Cc</span><span class="sxs-lookup"><span data-stu-id="2826e-116">Cc</span></span>           | |
| <span data-ttu-id="2826e-117">Emnelinje</span><span class="sxs-lookup"><span data-stu-id="2826e-117">Subject line</span></span> | <span data-ttu-id="2826e-118">Microsoft Dynamics Supportanmodning</span><span class="sxs-lookup"><span data-stu-id="2826e-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="2826e-119">Tekst</span><span class="sxs-lookup"><span data-stu-id="2826e-119">Body</span></span>         | <p><span data-ttu-id="2826e-120">Hej Support</span><span class="sxs-lookup"><span data-stu-id="2826e-120">Hi Support,</span></span></p><p><span data-ttu-id="2826e-121">Giv support til følgende problem:</span><span class="sxs-lookup"><span data-stu-id="2826e-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="2826e-122">Handlendes konto</span><span class="sxs-lookup"><span data-stu-id="2826e-122">Merchant account</span></span></li><li><span data-ttu-id="2826e-123">Miljø (Test/Prod)</span><span class="sxs-lookup"><span data-stu-id="2826e-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="2826e-124">Kanal (POS/callcenter/Handel e-handel)</span><span class="sxs-lookup"><span data-stu-id="2826e-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="2826e-125">PSP-referencenummer, hvis der indgår en bestemt transaktion i problemet (du kan finde PSP-referencenummeret på kvitteringen i kundeområdet Adyen eller i transaktionsmenuen på POS-terminalen.)</span><span class="sxs-lookup"><span data-stu-id="2826e-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="2826e-126">Skærmbillede eller billede af fejlmeddelelsen, hvis det er relevant</span><span class="sxs-lookup"><span data-stu-id="2826e-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="2826e-127">Logfiler til hændelsesvisning (i .txt-format)</span><span class="sxs-lookup"><span data-stu-id="2826e-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="2826e-128">Beskrivelse af de trin til problem- og fejlfinding, som du har forsøgt</span><span class="sxs-lookup"><span data-stu-id="2826e-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="2826e-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2826e-129">Additional resources</span></span>

[<span data-ttu-id="2826e-130">Accepter betalinger med Adyen-connector til Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2826e-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="2826e-131">Dynamics 365-betalingsconnector til Adyen</span><span class="sxs-lookup"><span data-stu-id="2826e-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="2826e-132">Konfigurer Adyen-betalingsconnector til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2826e-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
