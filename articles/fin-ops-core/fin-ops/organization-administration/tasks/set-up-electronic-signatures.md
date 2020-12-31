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
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 088fe3c42b00a6a495aeee19a4e3640054a8aa2a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694759"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="d98c1-103">Opsætning af elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="d98c1-103">Set up electronic signatures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d98c1-104">Brug denne procedure til at konfigurere elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="d98c1-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="d98c1-105">En elektronisk signatur bekræfter identiteten på en person, som skal starte eller godkende en computerproces.</span><span class="sxs-lookup"><span data-stu-id="d98c1-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="d98c1-106">Det demodatafirma, der bruges til at oprette denne procedure, er DAT.</span><span class="sxs-lookup"><span data-stu-id="d98c1-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="d98c1-107">Aktiver konfigurationsnøglen for elektronisk signatur</span><span class="sxs-lookup"><span data-stu-id="d98c1-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="d98c1-108">Gå til Systemadministration > Opsætning > Licenskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d98c1-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="d98c1-109">Udvid "Administration" i træet.</span><span class="sxs-lookup"><span data-stu-id="d98c1-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="d98c1-110">Kontroller, at afkrydsningsfeltet Elektronisk signatur markeret.</span><span class="sxs-lookup"><span data-stu-id="d98c1-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="d98c1-111">Hvis afkrydsningsfeltet Elektronisk signatur ikke er markeret, skal du aktivere vedligeholdelsestilstand.</span><span class="sxs-lookup"><span data-stu-id="d98c1-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="d98c1-112">Vedligeholdelsestilstand kan aktiveres i dette miljø ved at køre et vedligeholdelsesjob fra Lifecycle Services eller lokalt ved hjælp af værktøjet Deployment.Setup.</span><span class="sxs-lookup"><span data-stu-id="d98c1-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="d98c1-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d98c1-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="d98c1-114">Konfigurere parametre for elektronisk signatur</span><span class="sxs-lookup"><span data-stu-id="d98c1-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="d98c1-115">Gå til Virksomhedsadministration > Opsætning > Elektronisk signatur > Parametre for elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="d98c1-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="d98c1-116">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d98c1-116">Click Edit.</span></span>
3. <span data-ttu-id="d98c1-117">Skriv en værdi i feltet Meddelelse.</span><span class="sxs-lookup"><span data-stu-id="d98c1-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="d98c1-118">Indtast den besked, som underskrivere vil få, når der kræves en signatur.</span><span class="sxs-lookup"><span data-stu-id="d98c1-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="d98c1-119">Du kan indtaste en hvilken som helst tekst.</span><span class="sxs-lookup"><span data-stu-id="d98c1-119">You can enter any text.</span></span> <span data-ttu-id="d98c1-120">Typisk fortæller denne tekst brugeren, hvad det at signere et dokument elektronisk betyder.</span><span class="sxs-lookup"><span data-stu-id="d98c1-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="d98c1-121">Hvis du vil indtaste beskedteksten på flere sprog, skal du klikke på knappen Oversættelser.</span><span class="sxs-lookup"><span data-stu-id="d98c1-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="d98c1-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d98c1-122">Click Save.</span></span>
5. <span data-ttu-id="d98c1-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d98c1-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="d98c1-124">Konfigurere årsagskoder for elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="d98c1-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="d98c1-125">Gå til Virksomhedsadministration > Opsætning > Elektronisk signatur > Årsagskoder for elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="d98c1-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="d98c1-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d98c1-126">Click New.</span></span>
    * <span data-ttu-id="d98c1-127">Du skal angive årsagskoder, før du bruger elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="d98c1-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="d98c1-128">Der kræves en gyldig årsagskode, når du signerer et dokument.</span><span class="sxs-lookup"><span data-stu-id="d98c1-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="d98c1-129">En underskriver vælger en årsagskode, som angiver formålet med en elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="d98c1-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="d98c1-130">En årsagskode kan f.eks. bruges til at angive juridisk godkendelse.</span><span class="sxs-lookup"><span data-stu-id="d98c1-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="d98c1-131">Skriv en værdi i feltet Årsagskode.</span><span class="sxs-lookup"><span data-stu-id="d98c1-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="d98c1-132">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d98c1-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d98c1-133">Angiv flere årsagskoder, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="d98c1-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="d98c1-134">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d98c1-134">Click Save.</span></span>
6. <span data-ttu-id="d98c1-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d98c1-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="d98c1-136">Krav om elektroniske signaturer for eksisterende processer</span><span class="sxs-lookup"><span data-stu-id="d98c1-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="d98c1-137">Gå til Virksomhedsadministration > Opsætning > Elektronisk signatur > Elektronisk signatur-krav.</span><span class="sxs-lookup"><span data-stu-id="d98c1-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="d98c1-138">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d98c1-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d98c1-139">Vælg en proces, der kræver elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="d98c1-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="d98c1-140">Marker eller fjern markeringen i afkrydsningsfeltet Signatur er påkrævet efter behov.</span><span class="sxs-lookup"><span data-stu-id="d98c1-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="d98c1-141">Gentag disse trin for hver proces, der kræver elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="d98c1-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="d98c1-142">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d98c1-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="d98c1-143">Opret et brugerdefineret krav om elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="d98c1-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="d98c1-144">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d98c1-144">Click New.</span></span>
2. <span data-ttu-id="d98c1-145">Marker eller fjern markeringen i afkrydsningsfeltet Signatur er påkrævet efter behov.</span><span class="sxs-lookup"><span data-stu-id="d98c1-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="d98c1-146">I feltet Navn skal du angive et navn til den proces, der kræver elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="d98c1-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="d98c1-147">Klik på rullelisten i feltet Tabelnavn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d98c1-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d98c1-148">På listen skal du finde og vælge den tabel, hvor de data, der skal signeres, er gemt.</span><span class="sxs-lookup"><span data-stu-id="d98c1-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="d98c1-149">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d98c1-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d98c1-150">Klik på rullelisten i feltet Feltnavn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d98c1-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d98c1-151">På listen skal du finde og vælge det felt i tabellen, som du vil overvåge.</span><span class="sxs-lookup"><span data-stu-id="d98c1-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="d98c1-152">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d98c1-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d98c1-153">Angiv, hvornår der kræves en signatur.</span><span class="sxs-lookup"><span data-stu-id="d98c1-153">Specify when a signature is required.</span></span>     <span data-ttu-id="d98c1-154">Vælg Altid, hvis en signature kræves, når dataene i feltet ændres.</span><span class="sxs-lookup"><span data-stu-id="d98c1-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="d98c1-155">Vælg Kun, hvis der kun kræves en signatur under visse omstændigheder.</span><span class="sxs-lookup"><span data-stu-id="d98c1-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="d98c1-156">Hvis du vælger Kun, skal du også vælge en af følgende indstillinger: Når der indsættes en post, Når en post opdateres eller Når en post slettes.</span><span class="sxs-lookup"><span data-stu-id="d98c1-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="d98c1-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d98c1-157">Click Save.</span></span>
11. <span data-ttu-id="d98c1-158">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d98c1-158">Close the page.</span></span>

