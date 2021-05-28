---
title: Indstillinger for Varetrækprincip på styklistelinjer overholdes ikke
description: Indstillinger for Varetrækprincip på styklistelinjer overholdes ikke.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026373"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="233ad-103">Indstillinger for Varetrækprincip på styklistelinjer overholdes ikke</span><span class="sxs-lookup"><span data-stu-id="233ad-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="233ad-104">KB-nummer: 4612725</span><span class="sxs-lookup"><span data-stu-id="233ad-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="233ad-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="233ad-105">Symptoms</span></span>

<span data-ttu-id="233ad-106">Dette problem opstår, når feltet **Automatisk styklisteforbrug** under fanen **Automatisk opdatering** på siden **Produktionsstyringsparametre** er indstillet til *Varetrækprincip*.</span><span class="sxs-lookup"><span data-stu-id="233ad-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="233ad-107">Denne indstilling angiver, at alle styklistelinjer automatisk skal forbruges, når der modtages en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="233ad-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="233ad-108">Hvis feltet **Varetrækprincip** på styklistelinjer udtrykkeligt er indstillet til *Manuel*, kan du forvente, at styklistelinjerne ikke forbruges automatisk.</span><span class="sxs-lookup"><span data-stu-id="233ad-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="233ad-109">Når dette problem opstår, forbruges styklistelinjer, hvor feltet **Varetrækprincip** er indstillet til *Manuel*, dog automatisk.</span><span class="sxs-lookup"><span data-stu-id="233ad-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="233ad-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="233ad-110">Resolution</span></span>

<span data-ttu-id="233ad-111">Hvis du ønsker at løse dette problem, kan produktionsstyringsparametrene konfigureres til at overstyre indstillingen af **Varetrækprincip** på styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="233ad-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="233ad-112">Kontroller værdien i feltet **Automatisk styklisteforbrug** under fanen **Automatisk opdatering** på siden **Produktionsstyringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="233ad-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="233ad-113">Hvis indstillingen er *Altid*, ignorerer systemet indstillingen **Varetrækprincip** på alle styklistelinjer og rydder altid linjerne.</span><span class="sxs-lookup"><span data-stu-id="233ad-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="233ad-114">Hvis systemet skal overholde indstillingen i **Varetrækprincip** på styklistelinjer, skal du ændre værdien i feltet **Automatisk styklisteforbrug** til *Varetrækprincip*.</span><span class="sxs-lookup"><span data-stu-id="233ad-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
