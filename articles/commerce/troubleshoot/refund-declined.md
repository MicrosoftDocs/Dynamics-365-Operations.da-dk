---
title: Refusion af en returordre afvises
description: Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når en refusion på en returordre afvises, fordi det kreditkort, der bruges til fakturering, ikke er det samme som det kort, der blev brugt under den oprindelige betalingsgodkendelse.
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
ms.openlocfilehash: 99fd4b816b1a3a1fe3c2d1579be45b43fdc3d385
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020750"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="cc363-103">Refusion af en returordre afvises</span><span class="sxs-lookup"><span data-stu-id="cc363-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc363-104">Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når en refusion på en returordre afvises, fordi det kreditkort, der bruges til fakturering, ikke er det samme som det kort, der blev brugt under den oprindelige betalingsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="cc363-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="cc363-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="cc363-105">Description</span></span>

<span data-ttu-id="cc363-106">En refusion afvises, når det kreditkort, der bruges til at fakturere en returordre, afviger fra det kort, der blev brugt under den oprindelige betalingsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="cc363-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="cc363-107">Du får vist følgende fejlmeddelelse: "Nogle betalinger har ikke den korrekte status til bogføring.</span><span class="sxs-lookup"><span data-stu-id="cc363-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="cc363-108">Valider status for alle betalinger inden faktureringen igen."</span><span class="sxs-lookup"><span data-stu-id="cc363-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="cc363-109">Oplysningerne om betalingstilladelsen indeholder følgende fejlmeddelelse: "Adyen-gateway SendRequest() mislykkedes med status 'InternalServerError'.22144; Tomt svar, der returneres fra Adyen.(22001);"</span><span class="sxs-lookup"><span data-stu-id="cc363-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Afviste refusion af en returordre](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="cc363-111">Løsning</span><span class="sxs-lookup"><span data-stu-id="cc363-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="cc363-112">Aktiver skjulte returneringer i Adyen</span><span class="sxs-lookup"><span data-stu-id="cc363-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="cc363-113">Hvis du vil aktivere skjulte returneringer, skal du udføre trinnene i [Fejlfinding af Dynamics 365 Payment Connector for Adyen-problemer](adyen-support.md), så du kan kontakte Adyen-supportteamet og anmode om, at skjulte returneringer aktiveres på din Adyen-forhandlerkonto.</span><span class="sxs-lookup"><span data-stu-id="cc363-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc363-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cc363-114">Additional resources</span></span>

[<span data-ttu-id="cc363-115">Dynamics 365-betalingsconnector til Adyen</span><span class="sxs-lookup"><span data-stu-id="cc363-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="cc363-116">Konfigurer Adyen-betalingsconnector til Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cc363-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
