---
title: Opsætning af elektroniske signaturer
description: Brug denne procedure til at konfigurere elektroniske signaturer.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be8d2c95b95be621c81d41fd98e5857caa8bbbcb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981764"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="24d31-103">Opsætning af elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="24d31-103">Set up electronic signatures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24d31-104">Brug denne procedure til at konfigurere elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="24d31-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="24d31-105">En elektronisk signatur bekræfter identiteten på en person, som skal starte eller godkende en computerproces.</span><span class="sxs-lookup"><span data-stu-id="24d31-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="24d31-106">Det demodatafirma, der bruges til at oprette denne procedure, er DAT.</span><span class="sxs-lookup"><span data-stu-id="24d31-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="24d31-107">Aktiver konfigurationsnøglen for elektronisk signatur</span><span class="sxs-lookup"><span data-stu-id="24d31-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="24d31-108">Gå til Systemadministration > Opsætning > Licenskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="24d31-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="24d31-109">Udvid "Administration" i træet.</span><span class="sxs-lookup"><span data-stu-id="24d31-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="24d31-110">Kontroller, at afkrydsningsfeltet Elektronisk signatur markeret.</span><span class="sxs-lookup"><span data-stu-id="24d31-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="24d31-111">Hvis afkrydsningsfeltet Elektronisk signatur ikke er markeret, skal du aktivere vedligeholdelsestilstand.</span><span class="sxs-lookup"><span data-stu-id="24d31-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="24d31-112">Vedligeholdelsestilstand kan aktiveres i dette miljø ved at køre et vedligeholdelsesjob fra Lifecycle Services eller lokalt ved hjælp af værktøjet Deployment.Setup.</span><span class="sxs-lookup"><span data-stu-id="24d31-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="24d31-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="24d31-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="24d31-114">Konfigurere parametre for elektronisk signatur</span><span class="sxs-lookup"><span data-stu-id="24d31-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="24d31-115">Gå til Virksomhedsadministration > Opsætning > Elektronisk signatur > Parametre for elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="24d31-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="24d31-116">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="24d31-116">Click Edit.</span></span>
3. <span data-ttu-id="24d31-117">Skriv en værdi i feltet Meddelelse.</span><span class="sxs-lookup"><span data-stu-id="24d31-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="24d31-118">Indtast den besked, som underskrivere vil få, når der kræves en signatur.</span><span class="sxs-lookup"><span data-stu-id="24d31-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="24d31-119">Du kan indtaste en hvilken som helst tekst.</span><span class="sxs-lookup"><span data-stu-id="24d31-119">You can enter any text.</span></span> <span data-ttu-id="24d31-120">Typisk fortæller denne tekst brugeren, hvad det at signere et dokument elektronisk betyder.</span><span class="sxs-lookup"><span data-stu-id="24d31-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="24d31-121">Hvis du vil indtaste beskedteksten på flere sprog, skal du klikke på knappen Oversættelser.</span><span class="sxs-lookup"><span data-stu-id="24d31-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="24d31-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="24d31-122">Click Save.</span></span>
5. <span data-ttu-id="24d31-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="24d31-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="24d31-124">Konfigurere årsagskoder for elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="24d31-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="24d31-125">Gå til Virksomhedsadministration > Opsætning > Elektronisk signatur > Årsagskoder for elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="24d31-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="24d31-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="24d31-126">Click New.</span></span>
    * <span data-ttu-id="24d31-127">Du skal angive årsagskoder, før du bruger elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="24d31-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="24d31-128">Der kræves en gyldig årsagskode, når du signerer et dokument.</span><span class="sxs-lookup"><span data-stu-id="24d31-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="24d31-129">En underskriver vælger en årsagskode, som angiver formålet med en elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="24d31-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="24d31-130">En årsagskode kan f.eks. bruges til at angive juridisk godkendelse.</span><span class="sxs-lookup"><span data-stu-id="24d31-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="24d31-131">Skriv en værdi i feltet Årsagskode.</span><span class="sxs-lookup"><span data-stu-id="24d31-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="24d31-132">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="24d31-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="24d31-133">Angiv flere årsagskoder, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="24d31-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="24d31-134">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="24d31-134">Click Save.</span></span>
6. <span data-ttu-id="24d31-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="24d31-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="24d31-136">Krav om elektroniske signaturer for eksisterende processer</span><span class="sxs-lookup"><span data-stu-id="24d31-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="24d31-137">Gå til Virksomhedsadministration > Opsætning > Elektronisk signatur > Elektronisk signatur-krav.</span><span class="sxs-lookup"><span data-stu-id="24d31-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="24d31-138">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="24d31-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="24d31-139">Vælg en proces, der kræver elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="24d31-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="24d31-140">Marker eller fjern markeringen i afkrydsningsfeltet Signatur er påkrævet efter behov.</span><span class="sxs-lookup"><span data-stu-id="24d31-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="24d31-141">Gentag disse trin for hver proces, der kræver elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="24d31-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="24d31-142">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="24d31-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="24d31-143">Opret et brugerdefineret krav om elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="24d31-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="24d31-144">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="24d31-144">Click New.</span></span>
2. <span data-ttu-id="24d31-145">Marker eller fjern markeringen i afkrydsningsfeltet Signatur er påkrævet efter behov.</span><span class="sxs-lookup"><span data-stu-id="24d31-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="24d31-146">I feltet Navn skal du angive et navn til den proces, der kræver elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="24d31-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="24d31-147">Klik på rullelisten i feltet Tabelnavn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="24d31-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="24d31-148">På listen skal du finde og vælge den tabel, hvor de data, der skal signeres, er gemt.</span><span class="sxs-lookup"><span data-stu-id="24d31-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="24d31-149">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="24d31-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="24d31-150">Klik på rullelisten i feltet Feltnavn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="24d31-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="24d31-151">På listen skal du finde og vælge det felt i tabellen, som du vil overvåge.</span><span class="sxs-lookup"><span data-stu-id="24d31-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="24d31-152">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="24d31-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="24d31-153">Angiv, hvornår der kræves en signatur.</span><span class="sxs-lookup"><span data-stu-id="24d31-153">Specify when a signature is required.</span></span>     <span data-ttu-id="24d31-154">Vælg Altid, hvis en signature kræves, når dataene i feltet ændres.</span><span class="sxs-lookup"><span data-stu-id="24d31-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="24d31-155">Vælg Kun, hvis der kun kræves en signatur under visse omstændigheder.</span><span class="sxs-lookup"><span data-stu-id="24d31-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="24d31-156">Hvis du vælger Kun, skal du også vælge en af følgende indstillinger: Når der indsættes en post, Når en post opdateres eller Når en post slettes.</span><span class="sxs-lookup"><span data-stu-id="24d31-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="24d31-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="24d31-157">Click Save.</span></span>
11. <span data-ttu-id="24d31-158">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="24d31-158">Close the page.</span></span>

