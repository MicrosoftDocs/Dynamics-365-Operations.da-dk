---
title: Åbne økonomikladdeskabeloner i Office
description: I dette emne beskrives de problemer, der kan opstå, når du opretter brugerdefinerede økonomikladder ved hjælp af en Microsoft Excel-skabelon.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089451"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="915dd-103">Åbne økonomikladdeskabeloner i Office</span><span class="sxs-lookup"><span data-stu-id="915dd-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="915dd-104">I dette emne beskrives de problemer, der kan opstå, når du opretter brugerdefinerede økonomikladder ved hjælp af en Microsoft Excel-skabelon.</span><span class="sxs-lookup"><span data-stu-id="915dd-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="915dd-105">Symptom</span><span class="sxs-lookup"><span data-stu-id="915dd-105">Symptom</span></span>

<span data-ttu-id="915dd-106">Du har oprettet en brugerdefineret Excel-skabelon til økonomikladder, men den vises ikke i menuen **Åbn linjer i Excel**.</span><span class="sxs-lookup"><span data-stu-id="915dd-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="915dd-107">Den kan vises i menuen, men der åbnes en anden skabelon, når du vælger den.</span><span class="sxs-lookup"><span data-stu-id="915dd-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="915dd-108">Løsning</span><span class="sxs-lookup"><span data-stu-id="915dd-108">Resolution</span></span>

<span data-ttu-id="915dd-109">Standardfunktionen Åbn i Excel bruger roddatakilden (tabellen) på den aktuelle side til at bestemme, hvilke Office-skabeloner eller dataenheder der vises som indstillinger i menuen **Åbn i Excel**.</span><span class="sxs-lookup"><span data-stu-id="915dd-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="915dd-110">Denne funktionsmåde er ikke en ideel oplevelse for økonomikladder, fordi økonomikladder bruger de samme tabeller (LedgerJournalTable og LedgerJournalTrans) som roddatakilde for mange andre typer kladder.</span><span class="sxs-lookup"><span data-stu-id="915dd-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="915dd-111">I forbindelse med økonomikladder er funktionen Åbn linjer i Excel beregnet til at vise skabeloner, der er udviklet til den kladde, du aktuelt arbejder i forbindelse med, f.eks. økonomikladden eller en betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="915dd-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="915dd-112">En skabelon, der er beregnet til at blive brugt sammen med en kreditorbetalingskladde, vil f.eks. være designet til at gennemtvinge din primære konto som en kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="915dd-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="915dd-113">Hvis du vil hæve en skabelon, så den er tilgængelig på menuerne **Åbn linjer i Excel** og **Åbn i Excel**, er en nem udvikleroplevelse at implementere **LedgerIJournalExcelTemplate**-grænsefladen og udvide **DocuTemplateRegistrationBase**-klassen.</span><span class="sxs-lookup"><span data-stu-id="915dd-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="915dd-114">Mange eksempler på denne fremgangsmåde er implementeret i systemet.</span><span class="sxs-lookup"><span data-stu-id="915dd-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="915dd-115">Et eksempel, der kan bruges til reference, er **LedgerDailyJournalExcelTemplate**-grænsefladen, der blev oprettet til økonomikladden (eller kassekladden).</span><span class="sxs-lookup"><span data-stu-id="915dd-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="915dd-116">Når **LedgerIJournalExcelTemplate**-grænsefladen er implementeret for skabelonen, filtrerer menuen **Åbn linjer i Excel** kladder efter kladdetypen og viser kun de skabeloner, der er tilgængelige for den pågældende kladde.</span><span class="sxs-lookup"><span data-stu-id="915dd-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="915dd-117">Grænsefladen indeholder også en valideringsmetode, der sikrer, at en skabelon ikke kan åbnes for en kladde, hvis den ikke opfylder kravene til kontotypen.</span><span class="sxs-lookup"><span data-stu-id="915dd-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="915dd-118">Du kan f.eks. angive, at kontotypen skal være af typen **Kreditor** eller **Finans**.</span><span class="sxs-lookup"><span data-stu-id="915dd-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="915dd-119">Du kan finde flere oplysninger om denne funktion i [Føje skabeloner til menuen Åbn i Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="915dd-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
