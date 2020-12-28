---
title: Konfigurere parametre for administration af frynsegoder pr. firma
description: Konfigurere parametre for administration af frynsegoder pr. firma i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692739"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="f0dcb-103">Konfigurere parametre for administration af frynsegoder pr. firma</span><span class="sxs-lookup"><span data-stu-id="f0dcb-103">Configure Benefits management parameters per company</span></span>

<span data-ttu-id="f0dcb-104">For hver organisation, der tilbyder frynsegoder, skal du konfigurere indstillinger for e-mails med bekræftelse af frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="f0dcb-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="f0dcb-105">Konfigurere indstillinger for e-mails om frynsegoder</span><span class="sxs-lookup"><span data-stu-id="f0dcb-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="f0dcb-106">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for personale** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f0dcb-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="f0dcb-107">Angiv værdier for følgende felter under fanen **Frynsegodeadministration**:</span><span class="sxs-lookup"><span data-stu-id="f0dcb-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="f0dcb-108">Felt</span><span class="sxs-lookup"><span data-stu-id="f0dcb-108">Field</span></span> | <span data-ttu-id="f0dcb-109">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="f0dcb-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f0dcb-110">**Send bekræftelsesmail**</span><span class="sxs-lookup"><span data-stu-id="f0dcb-110">**Send confirmation email**</span></span> | <span data-ttu-id="f0dcb-111">Når denne funktion er slået til, sendes der en bekræftelses-e-mail til medarbejdere, når de tjekker ud fra frynsegodetilmeldingsoplevelsen i Employee Self-Service.</span><span class="sxs-lookup"><span data-stu-id="f0dcb-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="f0dcb-112">**Skabelon for bekræftelsesmail**</span><span class="sxs-lookup"><span data-stu-id="f0dcb-112">**Confirmation email template**</span></span> | <span data-ttu-id="f0dcb-113">Vælg den skabelon til organisationsmail, der skal bruges, når tilmeldingsbekræftelsen sendes.</span><span class="sxs-lookup"><span data-stu-id="f0dcb-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="f0dcb-114">Hvis du ikke vælger en skabelon, sendes der følgende generiske e-mail:</span><span class="sxs-lookup"><span data-stu-id="f0dcb-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="f0dcb-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="f0dcb-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="f0dcb-116">Tillykke!</span><span class="sxs-lookup"><span data-stu-id="f0dcb-116">Congratulations!</span></span> <span data-ttu-id="f0dcb-117">Du har fuldført tilmeldingen til frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="f0dcb-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="f0dcb-118">Tak</span><span class="sxs-lookup"><span data-stu-id="f0dcb-118">Thank you,</span></span><br><span data-ttu-id="f0dcb-119"><Firma/Organisationsnavn> Frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="f0dcb-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="f0dcb-120">**Afsenderadresse for standardmail**</span><span class="sxs-lookup"><span data-stu-id="f0dcb-120">**Default email sender address**</span></span> | <span data-ttu-id="f0dcb-121">Den e-mailadresse, der skal bruges ved afsendelse af bekræftelsesmailen.</span><span class="sxs-lookup"><span data-stu-id="f0dcb-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="f0dcb-122">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f0dcb-122">Select **Save**.</span></span>