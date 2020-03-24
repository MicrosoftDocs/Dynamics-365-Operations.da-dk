---
title: Periodiske opgaver for kreditstyring
description: I dette emne beskrives de periodiske opgaver, der er en del af processen til administration af kreditmaksimum for kunder.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ca9bb7f77283ec30d4648d6763f4156494050ac
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124156"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="2040b-103">Periodiske kreditsstyringsopgaver</span><span class="sxs-lookup"><span data-stu-id="2040b-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2040b-104">I dette emne beskrives de periodiske opgaver, der er en del af processen til administration af kreditmaksimum for kunder.</span><span class="sxs-lookup"><span data-stu-id="2040b-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="2040b-105">Opdater risikoscorer</span><span class="sxs-lookup"><span data-stu-id="2040b-105">Update risk scores</span></span>

<span data-ttu-id="2040b-106">Efterhånden som virksomheder udvikler sig og deres omstændigheder ændres, kan det også betyde, at kunders kreditrisici ændres.</span><span class="sxs-lookup"><span data-stu-id="2040b-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="2040b-107">For at sikre opretholdelse af relevante kreditlofter for kunderne skal du regelmæssigt gennemgå kriterierne for hver risikovurdering og opdatere vurderingerne for hver kunde.</span><span class="sxs-lookup"><span data-stu-id="2040b-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="2040b-108">Du kan opdatere følgende vurderinger på siden **Opdater risikovurderinger** (**Kredit \> Periodiske opgaver \> Kreditstyring \> Opdater risikovurderinger**).</span><span class="sxs-lookup"><span data-stu-id="2040b-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="2040b-109">Alle brugerdefinerede beregninger behandles også.</span><span class="sxs-lookup"><span data-stu-id="2040b-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="2040b-110">**Betalingsdage i gennemsnit**– Denne vurdering er det gennemsnitlige antal dage, inden en kunde betaler fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2040b-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="2040b-111">**Kunde siden** – Denne vurdering er det antal år, som en kunde har været kunde i din organisation.</span><span class="sxs-lookup"><span data-stu-id="2040b-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="2040b-112">**Har drevet forretning siden** – Denne vurdering er det antal år, som en kunde har drevet forretning på området.</span><span class="sxs-lookup"><span data-stu-id="2040b-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="2040b-113">Værdien i feltet **Virksomhedsstart** på siden **Kunder** bruges.</span><span class="sxs-lookup"><span data-stu-id="2040b-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="2040b-114">**Udestående dages salg** – Denne vurdering er baseret på debitorsaldoen, salgsindtægterne og antallet af dage for den foregående 12-måneders periode.</span><span class="sxs-lookup"><span data-stu-id="2040b-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="2040b-115">**Gennemsnitlig saldo** – Denne vurdering er baseret på debitorsaldoen for den forrige 12-måneders periode.</span><span class="sxs-lookup"><span data-stu-id="2040b-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="2040b-116">**Kreditstyringsgruppe**, **Kontostatus** og **Land** – Disse vurderinger bruger oplysninger fra kunden.</span><span class="sxs-lookup"><span data-stu-id="2040b-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="2040b-117">Opdatere statistik for debitorsaldo</span><span class="sxs-lookup"><span data-stu-id="2040b-117">Update customer balance statistics</span></span>

<span data-ttu-id="2040b-118">Du kan køre processen **Opdatere statistik for debitorsaldo** for at opdatere beregningen af saldostatistik, der vises på siden med **Forespørgsler om saldostatistik**.</span><span class="sxs-lookup"><span data-stu-id="2040b-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="2040b-119">Disse oplysninger bruges til at beregne risikovurderinger og de værdier, der vises i faktaboksene med kreditstatistik på siden **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="2040b-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="2040b-120">Når du kører processen, opdateres debitorsaldostatistik for en enkelt debitor.</span><span class="sxs-lookup"><span data-stu-id="2040b-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="2040b-121">Hvis du vil definere et batchjob, der skal køre processen for flere debitorer, kan du bruge siden **Beregn saldostatistik** (**Kreditstyring \> Periodiske opgaver \> Beregn saldostatistik**).</span><span class="sxs-lookup"><span data-stu-id="2040b-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>
