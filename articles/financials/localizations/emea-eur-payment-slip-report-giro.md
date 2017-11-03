---
title: Indbetalingskortrapport for Europa
description: Dette emne indeholder oplysninger om indbetalingskortrapporter for Europa.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264604
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a64a2ae8c84802a06e4f0f54a99bed3966c337f4
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="payment-slip-report-for-europe"></a><span data-ttu-id="8cf87-103">Indbetalingskortrapport for Europa</span><span class="sxs-lookup"><span data-stu-id="8cf87-103">Payment slip report for Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8cf87-104">Dette emne indeholder oplysninger om indbetalingskortrapporter for Europa.</span><span class="sxs-lookup"><span data-stu-id="8cf87-104">This topic provides information about payment slip reports for Europe.</span></span>

<span data-ttu-id="8cf87-105">Funktionerne for indbetalingskortrapporter er tilgængelige for juridiske enheder, der har deres primære adresse i Danmark, Belgien, Norge, Schweiz eller Finland.</span><span class="sxs-lookup"><span data-stu-id="8cf87-105">The functionality for payment slip reports is available for legal entities that have their primary address in Denmark, Belgium, Norway, Switzerland, or Finland.</span></span> <span data-ttu-id="8cf87-106">Virksomheder vedhæfter ofte udskrevne indbetalingskort til fakturaer for at angive en betalingsreference til brug ved bogføring og betaling.</span><span class="sxs-lookup"><span data-stu-id="8cf87-106">Businesses often attach printed payment slips to invoices to provide a payment reference for posting and settlement.</span></span> <span data-ttu-id="8cf87-107">Indbetalingskortet kan bruges til projekt- eller servicefakturaer, rykkere, rentenotaer og kontoopgørelser samt til salgsfakturaer og fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="8cf87-107">The payment slip can be used for project or service invoices, collection letters, interest notes, and account statements, in addition to sales invoices and free text invoices.</span></span>

## <a name="set-up-a-creditor-id-number-denmark-only"></a><span data-ttu-id="8cf87-108">Oprette et kreditor-id-nummer (kun Danmark)</span><span class="sxs-lookup"><span data-stu-id="8cf87-108">Set up a creditor ID number (Denmark only)</span></span>
<span data-ttu-id="8cf87-109">Følg disse trin for at angive din virksomheds kreditoridentifikationsnummer (ID).</span><span class="sxs-lookup"><span data-stu-id="8cf87-109">Follow these steps to enter your company's creditor identification (ID) number.</span></span> <span data-ttu-id="8cf87-110">Dit pengeinstitut leverer dette nummer.</span><span class="sxs-lookup"><span data-stu-id="8cf87-110">Your financial institution provides this number.</span></span> <span data-ttu-id="8cf87-111">Nummeret bruges som reference, når der modtages debitorbetalinger gennem pengeinstitutter.</span><span class="sxs-lookup"><span data-stu-id="8cf87-111">It's used as a reference when customer payments are received through financial institutions.</span></span>

1.  <span data-ttu-id="8cf87-112">Klik på **Virksomhedsadministration** &gt; **Organisationer** &gt; **Organisation** &gt; **Juridiske enheder**.</span><span class="sxs-lookup"><span data-stu-id="8cf87-112">Click **Organization administration** &gt; **Setup** &gt; **Organization** &gt; **Legal entities**.</span></span>
2.  <span data-ttu-id="8cf87-113">På oversigtspanelet **Bankkontooplysninger** i feltet **FI-kreditor-ID** skal du angive dit entydige otte-cifrede kreditor-id.</span><span class="sxs-lookup"><span data-stu-id="8cf87-113">On the **Bank account information** FastTab, in the **FI-Creditor ID** field, enter your unique eight-digit creditor ID number.</span></span>
3.  <span data-ttu-id="8cf87-114">Luk formen for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="8cf87-114">Close the form to save your changes.</span></span>

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a><span data-ttu-id="8cf87-115">Oprette et formater for vedhæftning af indbetalingskort for fakturaer, rentenotaer, rykkere og kontoudtog</span><span class="sxs-lookup"><span data-stu-id="8cf87-115">Set up a payment slip attachment format for invoices, interest notes, collection letters, and account statements</span></span>
<span data-ttu-id="8cf87-116">Følg disse trin for at oprette et format for indbetalingskort til vedhæftning til salgsfakturaer, fritekstfakturaer, rentenotaer, rykkere og kontoopgørelser.</span><span class="sxs-lookup"><span data-stu-id="8cf87-116">Follow these steps to set up a format for payment slip attachments that accompany sales invoices, free text invoices, interest notes, collection letters, and account statements.</span></span>

1.  <span data-ttu-id="8cf87-117">Klik på **Debitor** &gt; **Opsætning** &gt; **Formularer** &gt; **Formularopsætning**.</span><span class="sxs-lookup"><span data-stu-id="8cf87-117">Click **Accounts receivable** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2.  <span data-ttu-id="8cf87-118">Under fanen **Faktura** i feltet **Tilknyttet betalingsbilag på debitorfaktura** skal du vælge formatet for vedhæftning af indbetalingskortet.</span><span class="sxs-lookup"><span data-stu-id="8cf87-118">On the **Invoice** tab, in the **Associated payment attachment on customer invoice** field, select the payment slip attachment format.</span></span>
3.  <span data-ttu-id="8cf87-119">Under fanerne **Fritekstfaktura**, **Rentenota**, **Rykker** og **Kontoudtog** skal du vælge et format for vedhæftning af indbetalingskort for hver dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="8cf87-119">On the **Free text invoice**, **Interest note**, **Collection letter**, and **Account statement** tabs, select a payment slip attachment format for each document type.</span></span>
4.  <span data-ttu-id="8cf87-120">Luk formen for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="8cf87-120">Close the form to save your changes.</span></span>

<span data-ttu-id="8cf87-121">Følg disse trin for at oprette et format for vedhæftning af indbetalingskort til projektfakturaer.</span><span class="sxs-lookup"><span data-stu-id="8cf87-121">Follow these steps to set up a format for payment slip attachments that accompany project invoices.</span></span>

1.  <span data-ttu-id="8cf87-122">Klik på **Projektstyring og regnskab** &gt; **Konfiguration** &gt; **Formularer** &gt; **Formularopsætning**.</span><span class="sxs-lookup"><span data-stu-id="8cf87-122">Click **Project management and accounting** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2.  <span data-ttu-id="8cf87-123">I feltet **Tilknyttet betalingsbilag** skal du vælge formatet for vedhæftningen af indbetalingskortet.</span><span class="sxs-lookup"><span data-stu-id="8cf87-123">In the **Associated payment attachment** field, select the payment slip attachment format.</span></span>

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a><span data-ttu-id="8cf87-124">Tildele et format for vedhæftning af indbetalingskort til en debitorkonto</span><span class="sxs-lookup"><span data-stu-id="8cf87-124">Assign a payment slip attachment format to a customer account</span></span>
<span data-ttu-id="8cf87-125">Når du har oprettet formatet for et indbetalingskort til vedhæftning til salgsfakturaer, fritekstfakturaer, rentenotaer, rykkere, kontoopgørelser og projektfakturaer, kan du tildele specifikke formater til en udvalgt debitor.</span><span class="sxs-lookup"><span data-stu-id="8cf87-125">After you set up the payment slip attachment format for sales invoices, free text invoices, interest notes, collection letters, account statements, and project invoices, you can assign specific formats for a selected customer.</span></span>

1.  <span data-ttu-id="8cf87-126">Klik på **Debitor** &gt; **Generelt** &gt; **Kunder** &gt; **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="8cf87-126">Click **Accounts receivable** &gt; **Common** &gt; **Customers** &gt; **All customers**.</span></span>
2.  <span data-ttu-id="8cf87-127">Opret en ny debitor, eller vælg en eksisterende debitor.</span><span class="sxs-lookup"><span data-stu-id="8cf87-127">Create a new customer, or select an existing customer.</span></span>
3.  <span data-ttu-id="8cf87-128">I oversigtspanelet **Faktura og levering** i felterne **På en debitorfaktura**, **På en fritekstfaktura**, **På en rentenota**, **På en rykker**, **På en projektfaktura** og **På en kontoopgørelse** skal du vælge formatet for vedhæftning af indbetalingskort, der skal ledsage hver type dokument, der sendes til den valgte debitor.</span><span class="sxs-lookup"><span data-stu-id="8cf87-128">On the **Invoice and delivery** FastTab, in the **On a customer invoice**, **On a free text invoice**, **On an interest note**, **On a collection letter**, **On a project invoice**, and **On an account statement** fields, select the format for payment slip attachments that will accompany documents of each type that are sent to the selected customer.</span></span>
4.  <span data-ttu-id="8cf87-129">Luk formen for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="8cf87-129">Close the form to save your changes.</span></span>





