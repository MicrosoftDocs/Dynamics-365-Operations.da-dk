---
title: Oversigt over avanceret bankafstemning
description: I denne artikel beskrives forløbet for den avancerede bankafstemningsproces. Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c76b38e957c1c76a80c76782f45405573b7f191
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842601"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="99817-104">Oversigt over avanceret bankafstemning</span><span class="sxs-lookup"><span data-stu-id="99817-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99817-105">I denne artikel beskrives forløbet for den avancerede bankafstemningsproces.</span><span class="sxs-lookup"><span data-stu-id="99817-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="99817-106">Med funktionen Avanceret bankafstemning kan du importere bankkontoudtog, der kan afstemmes automatisk fra bankposteringerne.</span><span class="sxs-lookup"><span data-stu-id="99817-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="99817-107">Med funktionen til avanceret afstemning kan du importere bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="99817-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="99817-108">De importerede bankkontoudtog kan derefter afstemmes automatisk fra inden for bankposteringer.</span><span class="sxs-lookup"><span data-stu-id="99817-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="99817-109">Her er trinene i arbejdsgangen til avanceret bankafstemning.</span><span class="sxs-lookup"><span data-stu-id="99817-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="99817-110">Konfigurer import af et kontoudtog.</span><span class="sxs-lookup"><span data-stu-id="99817-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="99817-111">Importer bankkontoudtog gennem dataenhedsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="99817-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="99817-112">Tre typiske bankkontoudtogsformater er indbygget: ISO20022, BAI2 og MT940.</span><span class="sxs-lookup"><span data-stu-id="99817-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="99817-113">Funktionaliteten kan udvides til et vilkårligt format.</span><span class="sxs-lookup"><span data-stu-id="99817-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="99817-114">Opret en nummerserie, der skal bruges til avanceret bankafstemning, og definer sammenholdningsregler for bankafstemning.</span><span class="sxs-lookup"><span data-stu-id="99817-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="99817-115">En sammenholdningsregel for afstemning er et sæt af kriterier, der anvendes til at filtrere kontoudtogslinjer og Microsoft Dynamics 365 for Finance and Operations-banktransaktionslinjer under afstemningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="99817-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="99817-116">Du kan oprette mere end én sammenholdningsregel for at automatisere og optimere dine afstemningsprocesser, afhængigt af din forretningspraksis.</span><span class="sxs-lookup"><span data-stu-id="99817-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="99817-117">Afstem bankkontoudtog med bankposteringer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="99817-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="99817-118">Udfør automatisk sammenholdning og oprettelse af kladder til afstemning.</span><span class="sxs-lookup"><span data-stu-id="99817-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="99817-119">Få vist bankkontoudtog og bankposteringer i Finance and Operations side om side.</span><span class="sxs-lookup"><span data-stu-id="99817-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="99817-120">Bogføre automatisk Finance and Operations-banktransaktioner, hvis de vises på bankens kontoudtog, men ikke i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="99817-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="99817-121">Generere en afstemningsopgørelse.</span><span class="sxs-lookup"><span data-stu-id="99817-121">Generate a reconciliation statement.</span></span>





