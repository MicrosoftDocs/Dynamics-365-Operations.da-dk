---
title: Konfigurere parametre for administration af frynsegoder pr. firma
description: Konfigurere parametre for administration af frynsegoder pr. firma i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 87d4f1e7580b333fd17d3b779aafa47c5baed424
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805652"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="a8a75-103">Konfigurere parametre for administration af frynsegoder pr. firma</span><span class="sxs-lookup"><span data-stu-id="a8a75-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a8a75-104">For hver organisation, der tilbyder frynsegoder, skal du konfigurere indstillinger for e-mails med bekræftelse af frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="a8a75-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="a8a75-105">Konfigurere indstillinger for e-mails om frynsegoder</span><span class="sxs-lookup"><span data-stu-id="a8a75-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="a8a75-106">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for personale** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="a8a75-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="a8a75-107">Angiv værdier for følgende felter under fanen **Frynsegodeadministration**:</span><span class="sxs-lookup"><span data-stu-id="a8a75-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="a8a75-108">Felt</span><span class="sxs-lookup"><span data-stu-id="a8a75-108">Field</span></span> | <span data-ttu-id="a8a75-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a8a75-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a8a75-110">**Send bekræftelsesmail**</span><span class="sxs-lookup"><span data-stu-id="a8a75-110">**Send confirmation email**</span></span> | <span data-ttu-id="a8a75-111">Når denne funktion er slået til, sendes der en bekræftelses-e-mail til medarbejdere, når de tjekker ud fra frynsegodetilmeldingsoplevelsen i Employee Self-Service.</span><span class="sxs-lookup"><span data-stu-id="a8a75-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="a8a75-112">**Skabelon for bekræftelsesmail**</span><span class="sxs-lookup"><span data-stu-id="a8a75-112">**Confirmation email template**</span></span> | <span data-ttu-id="a8a75-113">Vælg den skabelon til organisationsmail, der skal bruges, når tilmeldingsbekræftelsen sendes.</span><span class="sxs-lookup"><span data-stu-id="a8a75-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="a8a75-114">Hvis du ikke vælger en skabelon, sendes der følgende generiske e-mail:</span><span class="sxs-lookup"><span data-stu-id="a8a75-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="a8a75-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="a8a75-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="a8a75-116">Tillykke!</span><span class="sxs-lookup"><span data-stu-id="a8a75-116">Congratulations!</span></span> <span data-ttu-id="a8a75-117">Du har fuldført tilmeldingen til frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="a8a75-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="a8a75-118">Tak</span><span class="sxs-lookup"><span data-stu-id="a8a75-118">Thank you,</span></span><br><span data-ttu-id="a8a75-119"><Firma/Organisationsnavn> Frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="a8a75-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="a8a75-120">**Afsenderadresse for standardmail**</span><span class="sxs-lookup"><span data-stu-id="a8a75-120">**Default email sender address**</span></span> | <span data-ttu-id="a8a75-121">Den e-mailadresse, der skal bruges ved afsendelse af bekræftelsesmailen.</span><span class="sxs-lookup"><span data-stu-id="a8a75-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="a8a75-122">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a8a75-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]