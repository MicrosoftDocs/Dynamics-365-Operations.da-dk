---
title: Konfigurere TDS-registreringsnumre for juridiske enheder
description: Dette emne beskriver, hvordan du kan konfigurere registreringsnumre for kildeskat (TDS – Tax Deducted at Source) for juridiske enheder.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 3550b2b7b305702ffc337ba0a9bb79f60a9de120
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023115"
---
# <a name="set-up-tds-registration-numbers-for-legal-entities"></a><span data-ttu-id="8df1b-103">Konfigurere TDS-registreringsnumre for juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="8df1b-103">Set up TDS registration numbers for legal entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8df1b-104">Dette emne beskriver, hvordan du kan konfigurere registreringsnumre for kildeskat (TDS – Tax Deducted at Source) for juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="8df1b-104">This topic explains how to set up Tax Deducted at Source (TDS) registration numbers for legal entities.</span></span>

1. <span data-ttu-id="8df1b-105">Gå til **Organisationsadministration \> Organisationer \> Juridiske enheder**.</span><span class="sxs-lookup"><span data-stu-id="8df1b-105">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>

    <span data-ttu-id="8df1b-106">[![Siden Juridiske enheder](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span><span class="sxs-lookup"><span data-stu-id="8df1b-106">[![Legal entities page](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span></span>

2. <span data-ttu-id="8df1b-107">I feltet **Permanent kontonummer** i oversigtspanelet **Skatteoplysninger** skal du angive det permanente kontonummer (PAN – Permanent Account Number) for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="8df1b-107">On the **Tax information** FastTab, in the **Permanent account number** field, enter the permanent account number (PAN) of the legal entity.</span></span>
3. <span data-ttu-id="8df1b-108">I feltet **Kredsnummer** skal du angive kredsnummeret for skattemyndigheden.</span><span class="sxs-lookup"><span data-stu-id="8df1b-108">In the **Circle number** field, enter the circle number of the TDS authority.</span></span>
4. <span data-ttu-id="8df1b-109">I feltet **Myndighedsnummer** skal du angive myndighedsnummeret for skattemyndigheden.</span><span class="sxs-lookup"><span data-stu-id="8df1b-109">In the **Ward number** field, enter the ward number of the TDS authority.</span></span>
5. <span data-ttu-id="8df1b-110">Angiv oplysningerne om den skattemedarbejder, der er ansat hos skattemyndigheden, i feltet **Skattemedarbejder**.</span><span class="sxs-lookup"><span data-stu-id="8df1b-110">In the **Assessing officer** field, enter the details of the assessing officer for the TDS authority.</span></span>
6. <span data-ttu-id="8df1b-111">Vælg kategorien for fradragstypen for den juridiske enhed i feltet **Fradragstype**.</span><span class="sxs-lookup"><span data-stu-id="8df1b-111">In the **Type of deductor** field, select the deductor type category for the legal entity.</span></span>
7. <span data-ttu-id="8df1b-112">Vælg **Registrerings-id'er** i handlingsruden for at åbne siden **Adminstrer adresser**.</span><span class="sxs-lookup"><span data-stu-id="8df1b-112">On the Action Pane, select **Registration IDs** to open the **Manage addresses** page.</span></span>
8. <span data-ttu-id="8df1b-113">Vælg **Tilføj** eller **Rediger** i oversigtspanelet **Skatteoplysninger** for at åbne siden **Administrer skatteoplysninger**, hvor du kan opbevare skatteregistreringen.</span><span class="sxs-lookup"><span data-stu-id="8df1b-113">On the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>

    <span data-ttu-id="8df1b-114">[![Siden Administrer adresser](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span><span class="sxs-lookup"><span data-stu-id="8df1b-114">[![Manage addresses page](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span></span>

9. <span data-ttu-id="8df1b-115">Angiv registreringsnummeret i feltet **Skattekontonummer (TAN)** i oversigtspanelet **A-skat**.</span><span class="sxs-lookup"><span data-stu-id="8df1b-115">On the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the registration number.</span></span> <span data-ttu-id="8df1b-116">Dette tal skal indeholde fire alfabetiske tegn, derefter fem numeriske tegn og derefter ét alfabetisk tegn.</span><span class="sxs-lookup"><span data-stu-id="8df1b-116">This number must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="8df1b-117">Her er et eksempel: **AXDF87645F**.</span><span class="sxs-lookup"><span data-stu-id="8df1b-117">Here is an example: **AXDF87645F**.</span></span>
10. <span data-ttu-id="8df1b-118">Indtast en beskrivelse af registreringsnummeret for A-skat i feltet **Navn eller beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="8df1b-118">In the **Name or description** field, enter a description of the withholding tax registration number.</span></span>

    <span data-ttu-id="8df1b-119">[![Siden Administrer skatteoplysninger](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span><span class="sxs-lookup"><span data-stu-id="8df1b-119">[![Manage tax information page](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span></span>

11. <span data-ttu-id="8df1b-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8df1b-120">Close the page.</span></span>
