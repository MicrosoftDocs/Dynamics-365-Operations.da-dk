---
title: Oversigt over avanceret bankafstemning
description: I denne artikel beskrives forløbet for den avancerede bankafstemningsproces. Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f85ece0b25237c194777b41566860c49d4b9d39
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258202"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="6236c-104">Oversigt over avanceret bankafstemning</span><span class="sxs-lookup"><span data-stu-id="6236c-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6236c-105">I denne artikel beskrives forløbet for den avancerede bankafstemningsproces.</span><span class="sxs-lookup"><span data-stu-id="6236c-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="6236c-106">Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne.</span><span class="sxs-lookup"><span data-stu-id="6236c-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="6236c-107">Med funktionen til avanceret afstemning kan du importere bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="6236c-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="6236c-108">De importerede bankkontoudtog kan derefter afstemmes automatisk fra inden for bankposteringer.</span><span class="sxs-lookup"><span data-stu-id="6236c-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="6236c-109">Her er trinene i arbejdsgangen til avanceret bankafstemning.</span><span class="sxs-lookup"><span data-stu-id="6236c-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="6236c-110">Konfigurer import af et kontoudtog.</span><span class="sxs-lookup"><span data-stu-id="6236c-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="6236c-111">Importer bankkontoudtog gennem dataenhedsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="6236c-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="6236c-112">Tre typiske bankkontoudtogsformater er indbygget: ISO20022, BAI2 og MT940.</span><span class="sxs-lookup"><span data-stu-id="6236c-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="6236c-113">Funktionaliteten kan udvides til et vilkårligt format.</span><span class="sxs-lookup"><span data-stu-id="6236c-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="6236c-114">Opret en nummerserie, der skal bruges til avanceret bankafstemning, og definer sammenholdningsregler for bankafstemning.</span><span class="sxs-lookup"><span data-stu-id="6236c-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="6236c-115">En sammenholdningsregel for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og Microsoft Dynamics 365 Finance-banktransaktionslinjer under afstemningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="6236c-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="6236c-116">Du kan oprette mere end én sammenholdningsregel for at automatisere og optimere dine afstemningsprocesser, afhængigt af din forretningspraksis.</span><span class="sxs-lookup"><span data-stu-id="6236c-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="6236c-117">Afstem bankkontoudtog med Finance-banktransaktioner.</span><span class="sxs-lookup"><span data-stu-id="6236c-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="6236c-118">Udfør automatisk sammenholdning og oprettelse af kladder til afstemning.</span><span class="sxs-lookup"><span data-stu-id="6236c-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="6236c-119">Få vist bankkontoudtog og Finance-banktransaktioner side om side.</span><span class="sxs-lookup"><span data-stu-id="6236c-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="6236c-120">Bogføre automatisk Finance-banktransaktioner, hvis de vises på bankkontoudtog, men ikke i Finance-appen.</span><span class="sxs-lookup"><span data-stu-id="6236c-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="6236c-121">Generere en afstemningsopgørelse.</span><span class="sxs-lookup"><span data-stu-id="6236c-121">Generate a reconciliation statement.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]