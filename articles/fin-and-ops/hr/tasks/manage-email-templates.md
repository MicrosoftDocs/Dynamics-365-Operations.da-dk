---
title: Administrere mailskabeloner
description: Du kan overføre oplysninger fra din organisations database til bogmærkerne i et nyt dokument og bruge dem i skabeloner, der kan hjælper dig med at kommunikere effektivt med ansøgere og kandidater.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4667d0506c5ae6bea87b982c7feebab8963797a6
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "859154"
---
# <a name="manage-email-templates"></a><span data-ttu-id="cb3c1-103">Administrere mailskabeloner</span><span class="sxs-lookup"><span data-stu-id="cb3c1-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb3c1-104">Du kan overføre oplysninger fra din organisations database til bogmærkerne i et nyt dokument og bruge dem i skabeloner, der kan hjælper dig med at kommunikere effektivt med ansøgere og kandidater.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="cb3c1-105">Det kan du gøre ved at oprette en skabelon, der indeholder standardtekst og nogle bogmærker, hvor systemdataene skal indsættes.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="cb3c1-106">Du kan f.eks. indsætte adresse og kontaktoplysninger for ansøgeren i et Microsoft Word-dokument, som du kan bruge ved kommunikation med ansøgeren.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="cb3c1-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="cb3c1-108">Vælg de bogmærker, der skal bruges i dine e-mailskabeloner</span><span class="sxs-lookup"><span data-stu-id="cb3c1-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="cb3c1-109">Gå til Ansøgningsbogmærker.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-109">Go to Application bookmarks.</span></span>
2. <span data-ttu-id="cb3c1-110">Find og vælg den ønskede korrespondancehandling på listen.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="cb3c1-111">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-111">Click Edit.</span></span>
4. <span data-ttu-id="cb3c1-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cb3c1-113">Vælg de felter, du gerne vil bruge i en e-mailskabelon for den valgte korrespondancehandling, og flyt dem til Bogmærkefelter.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-113">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="cb3c1-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-114">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="cb3c1-115">Oprette en e-mail-skabelon</span><span class="sxs-lookup"><span data-stu-id="cb3c1-115">Create an email template</span></span>
1. <span data-ttu-id="cb3c1-116">Gå til Personale > Rekruttering > Kommunikation > Skabeloner til ansøgnings-e-mail.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-116">Go to Human resources > Recruitment > Communication > Application e-mail templates.</span></span>
2. <span data-ttu-id="cb3c1-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-117">Click New.</span></span>
3. <span data-ttu-id="cb3c1-118">Vælg "Samtale" i feltet Korrespondancehandling.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-118">In the Correspondence action field, select 'Interview'.</span></span>
    * <span data-ttu-id="cb3c1-119">Vælg den korrespondancehandling, der indeholder bogmærkerne, der skal bruges til denne type e-mailkommunikation.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-119">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="cb3c1-120">Indtast en værdi i feltet E-mail-skabelon.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-120">In the E-mail template field, type a value.</span></span>
5. <span data-ttu-id="cb3c1-121">Skriv en værdi i feltet Emne.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-121">In the Subject field, type a value.</span></span>
6. <span data-ttu-id="cb3c1-122">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-122">In the Text field, type a value.</span></span>
7. <span data-ttu-id="cb3c1-123">Find og vælg det ønskede bogmærkefelt på listen.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-123">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="cb3c1-124">Fortsæt med at skrive din e-mailmeddelelse, og indsæt bogmærkefelter, hvor du skal bruge dem.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-124">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
    * <span data-ttu-id="cb3c1-125">Fortsæt med at skrive din e-mailmeddelelse, og indsæt bogmærkefelter, hvis du vil.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-125">Continue typing your email message inserting the bookmark fields where desired.</span></span>  
9. <span data-ttu-id="cb3c1-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cb3c1-126">Click Save.</span></span>

