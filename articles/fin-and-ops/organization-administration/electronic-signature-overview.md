---
title: Elektroniske signaturer
description: Denne artikel giver et overblik over elektroniske signaturer og beskriver, hvordan de kan bruges i Microsoft Dynamics 365 for Finance and Operations.
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 676510ef503d51d914ba762e7ac15e2c4811c6ba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553218"
---
# <a name="electronic-signatures"></a><span data-ttu-id="dc76e-103">Elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="dc76e-103">Electronic signatures</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc76e-104">Denne artikel giver et overblik over elektroniske signaturer og beskriver, hvordan de kan bruges i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dc76e-104">This article provides an overview of electronic signatures and describes how they can be used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="dc76e-105">Hvad er en elektronisk signatur?</span><span class="sxs-lookup"><span data-stu-id="dc76e-105">What is an electronic signature?</span></span>

<span data-ttu-id="dc76e-106">En elektronisk signatur bekræfter identiteten på en person, som skal starte eller godkende en computerproces.</span><span class="sxs-lookup"><span data-stu-id="dc76e-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="dc76e-107">I nogle brancher er en elektronisk signatur lige så juridisk bindende som en håndskrevet signatur.</span><span class="sxs-lookup"><span data-stu-id="dc76e-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="dc76e-108">Elektroniske signaturer er et lovmæssigt krav i adskillige regulerede brancher som f.eks. lægemiddelsektoren, fødevareindustrien samt luftfart og forsvar.</span><span class="sxs-lookup"><span data-stu-id="dc76e-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="dc76e-109">De er også nødvendigt for at overholde forskrifterne i 21 CFR afsnit 11, der er udstedt af det amerikanske fødevareministerium FDA (Food and Drug Administration) i USA.</span><span class="sxs-lookup"><span data-stu-id="dc76e-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="dc76e-110">En elektronisk signatur er i sig selv ikke det samme som en digital signatur.</span><span class="sxs-lookup"><span data-stu-id="dc76e-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="dc76e-111">En elektronisk signatur er blot en erstatning for en håndskrevet signatur, mens en digital signatur omfatter yderligere sikkerhedsmæssige foranstaltninger.</span><span class="sxs-lookup"><span data-stu-id="dc76e-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="dc76e-112">En digital signatur kan bidrage til at identificere, om en anden bruger eller proces har forfalsket dataene.</span><span class="sxs-lookup"><span data-stu-id="dc76e-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="dc76e-113">En digital signatur kan også bekræftes, og denne bekræftelse kan ikke gendrives af ejeren af det certifikat, som blev brugt til at signere dataene.</span><span class="sxs-lookup"><span data-stu-id="dc76e-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="dc76e-114">Som beskrevet nedenfor har elektroniske signaturer i Microsoft Dynamics 365 for Finance and Operations en indbygget funktion til digital signatur.</span><span class="sxs-lookup"><span data-stu-id="dc76e-114">As described below, electronic signatures in Microsoft Dynamics 365 for Finance and Operations have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="dc76e-115">Elektroniske signaturer i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dc76e-115">Electronic signatures in Dynamics 365 for Finance and Operations</span></span>

<span data-ttu-id="dc76e-116">I Finance and Operations kan du bruge elektroniske signaturer til kritiske forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="dc76e-116">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="dc76e-117">Nogle processer har indbyggede funktioner til elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="dc76e-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="dc76e-118">Du kan også oprette tilpassede signaturkrav for enhver databasetabel og ethvert felt.</span><span class="sxs-lookup"><span data-stu-id="dc76e-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="dc76e-119">Elektroniske signaturer har en indbygget funktion til digitale signaturer.</span><span class="sxs-lookup"><span data-stu-id="dc76e-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="dc76e-120">Alle brugere, som signerer dokumenter, skal have tildelt et gyldigt kryptografisk certifikat.</span><span class="sxs-lookup"><span data-stu-id="dc76e-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="dc76e-121">Når et dokument signeres, godkendes den private nøgle, som er tilknyttet det pågældende certifikat.</span><span class="sxs-lookup"><span data-stu-id="dc76e-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="dc76e-122">Finance and Operations registrerer oplysninger om elektroniske signaturer i en log for at angive et revisionsspor.</span><span class="sxs-lookup"><span data-stu-id="dc76e-122">Finance and Operations records electronic signature information in a log to provide an audit trail.</span></span> <span data-ttu-id="dc76e-123">Hvis du vil oprette elektroniske signaturer, skal du se under [Opsætning af elektroniske signaturer (Opgaveguide)](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="dc76e-123">To set up electronic signatures, see [Set up electronic signatures (Task guide)](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="dc76e-124">Brugere, der kræver adgang til elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="dc76e-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="dc76e-125">Tre slags brugere kræver normalt sikkerhedsadgang til elektroniske signaturer: administratorer af elektroniske signaturer, underskrivere og revisorer af elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="dc76e-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="dc76e-126">Administratorer af elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="dc76e-126">Electronic signature administrator</span></span>

<span data-ttu-id="dc76e-127">Administratorer af elektroniske signaturer konfigurerer krav til signaturer, generelle parametre og godkendere, og de modtager besked, når signaturer ikke kan bekræftes.</span><span class="sxs-lookup"><span data-stu-id="dc76e-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="dc76e-128">En bruger, der er tildelt sikkerhedsrollen **It-chef**, har som standard tilladelse til at administrere elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="dc76e-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="dc76e-129">Underskriver</span><span class="sxs-lookup"><span data-stu-id="dc76e-129">Signer</span></span>

<span data-ttu-id="dc76e-130">En underskriver angiver elektroniske signaturer på dokumenter og til processer, der kræver signaturer.</span><span class="sxs-lookup"><span data-stu-id="dc76e-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="dc76e-131">En bruger, der er tildelt sikkerhedsrollen **Systembruger**, har som standard tilladelse til at signere dokumenter elektronisk.</span><span class="sxs-lookup"><span data-stu-id="dc76e-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="dc76e-132">Underskriveren kan kræve yderligere tilladelser, før der gives adgang til data, der er relateret til det dokument eller den proces, der signeres.</span><span class="sxs-lookup"><span data-stu-id="dc76e-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="dc76e-133">En bruger, der ændrer data, og derefter skal signere for disse ændringer, skal have tilladelse til at ændre dataene.</span><span class="sxs-lookup"><span data-stu-id="dc76e-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="dc76e-134">En bruger, der signerer på vegne af en anden bruger, kan ikke kræve adgang til dataene.</span><span class="sxs-lookup"><span data-stu-id="dc76e-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="dc76e-135">Et eksempel på denne type bruger er en tilsynsførende, der signerer for en medarbejders ændringer.</span><span class="sxs-lookup"><span data-stu-id="dc76e-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="dc76e-136">Revisorer af elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="dc76e-136">Electronic signature auditor</span></span>

<span data-ttu-id="dc76e-137">Revisorer af elektroniske signaturer gennemgår databaseloggen og signaturgennemsynsloggen, der er tilgængelig fra databaseloggen.</span><span class="sxs-lookup"><span data-stu-id="dc76e-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="dc76e-138">En bruger, der er tildelt sikkerhedsrollen **It-chef**, har som standard tilladelse til at overvåge elektroniske signaturer.</span><span class="sxs-lookup"><span data-stu-id="dc76e-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="dc76e-139">Hvis du bruger en anden rolle end **It-chef**, skal du sikre dig, at rollen er tildelt følgende rettigheder:</span><span class="sxs-lookup"><span data-stu-id="dc76e-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="dc76e-140">Vis fejl i elektroniske signaturer</span><span class="sxs-lookup"><span data-stu-id="dc76e-140">View electronic signature failures</span></span>
- <span data-ttu-id="dc76e-141">Vis databaselog</span><span class="sxs-lookup"><span data-stu-id="dc76e-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="dc76e-142">Elektronisk signering af dokumenter</span><span class="sxs-lookup"><span data-stu-id="dc76e-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="dc76e-143">Sådan hentes et certifikat</span><span class="sxs-lookup"><span data-stu-id="dc76e-143">Get a certificate</span></span>

<span data-ttu-id="dc76e-144">Før du signerer dokumenter digitalt i Finance and Operations, skal du anmode om et certifikat.</span><span class="sxs-lookup"><span data-stu-id="dc76e-144">Before you sign documents electronically in Finance and Operations, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="dc76e-145">Finance and Operations bruger Microsoft SQL Server-funktioner til at oprette certifikater og aktivere elektronisk signering.</span><span class="sxs-lookup"><span data-stu-id="dc76e-145">Finance and Operations uses Microsoft SQL Server features to create certificates and enable electronic signing.</span></span> <span data-ttu-id="dc76e-146">Der kræves ikke yderligere certifikater eller offentlige nøgleinfrastrukturer (PKI).</span><span class="sxs-lookup"><span data-stu-id="dc76e-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="dc76e-147">Når du anmoder om et certifikat, oprettes der en offentlig nøgle og en privat nøgle til dig i Finance and Operations-databasen.</span><span class="sxs-lookup"><span data-stu-id="dc76e-147">When you request a certificate, a public key and a private key are created for you in the Finance and Operations database.</span></span> <span data-ttu-id="dc76e-148">Den private nøgle er krypteret ved hjælp af en adgangskode, som kun du kender.</span><span class="sxs-lookup"><span data-stu-id="dc76e-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="dc76e-149">Når du signerer et dokument digitalt, bekræftes din identitet, når du indtaster adgangskoden.</span><span class="sxs-lookup"><span data-stu-id="dc76e-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="dc76e-150">Når du vil anmode om et certifikat, skal du på siden **Indstillinger** under fanen **Konti** klikke på **Hent certifikat**.</span><span class="sxs-lookup"><span data-stu-id="dc76e-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="dc76e-151">Du skal indtaste og bekræfte den adgangskode, du vil bruge til signering.</span><span class="sxs-lookup"><span data-stu-id="dc76e-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="dc76e-152">Adgangskoden bruges for at beskytte din private nøgle og godkende brugen af dit certifikat.</span><span class="sxs-lookup"><span data-stu-id="dc76e-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="dc76e-153">Denne adgangskode gemmes ikke i databasen, og den er ikke tilgængelig for nogen anden, end ikke Finance and Operations-administratoren.</span><span class="sxs-lookup"><span data-stu-id="dc76e-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the Finance and Operations administrator.</span></span>

<span data-ttu-id="dc76e-154">Hvis du glemmer den adgangskode, der er tilknyttet dit certifikat, skal du nulstille det pågældende certifikat.</span><span class="sxs-lookup"><span data-stu-id="dc76e-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="dc76e-155">Hvis du nulstiller certifikatet, påvirker det ikke dokumenter, du har signeret ved hjælp af det tidligere certifikat.</span><span class="sxs-lookup"><span data-stu-id="dc76e-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="dc76e-156">Du kan nulstille certifikatet ved på siden **Indstillinger** at klikke på **Nulstil certifikat**.</span><span class="sxs-lookup"><span data-stu-id="dc76e-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="dc76e-157">Signere et dokument elektronisk</span><span class="sxs-lookup"><span data-stu-id="dc76e-157">Sign a document electronically</span></span>

<span data-ttu-id="dc76e-158">Siden **Dokumentsignering** vises, når du foretager en ændring, der kræver en elektronisk signatur.</span><span class="sxs-lookup"><span data-stu-id="dc76e-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="dc76e-159">Klik på fanen **Dokument** på siden **Underskriv dokument** for at gennemse ændringerne i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="dc76e-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="dc76e-160">Vælg en årsagskode på fanen **Signatur**.</span><span class="sxs-lookup"><span data-stu-id="dc76e-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="dc76e-161">Angiv en kommentar, hvis der kræves en kommentar.</span><span class="sxs-lookup"><span data-stu-id="dc76e-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="dc76e-162">Hvis dit bruger-id ikke vises i feltet **Underskriver**, skal du vælge det på listen.</span><span class="sxs-lookup"><span data-stu-id="dc76e-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="dc76e-163">Angiv din lokalitet, hvis disse oplysninger er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="dc76e-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="dc76e-164">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc76e-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="dc76e-165">Signere en anden brugers ændringer</span><span class="sxs-lookup"><span data-stu-id="dc76e-165">Sign for another user's changes</span></span>

<span data-ttu-id="dc76e-166">Af og til vil du måske gerne have, at en bruger signerer for en anden brugers ændringer.</span><span class="sxs-lookup"><span data-stu-id="dc76e-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="dc76e-167">Det kan f.eks. være nødvendigt, at en tilsynsførende signerer for ændringer, som en medarbejder foretager på styklister.</span><span class="sxs-lookup"><span data-stu-id="dc76e-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="dc76e-168">Brug denne procedure til at angive en Finance and Operations-bruger som underskriver for en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="dc76e-168">Use this procedure to designate a Finance and Operations user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="dc76e-169">Når én bruger underskriver for en anden brugers ændringer, skal signaturen angives på den arbejdsstation, hvor den bruger, der udførte ændringen, arbejder.</span><span class="sxs-lookup"><span data-stu-id="dc76e-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="dc76e-170">Brugeren kan ikke gemme ændringen, før signaturen er blevet angivet.</span><span class="sxs-lookup"><span data-stu-id="dc76e-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="dc76e-171">Udfør disse trin for at angive godkendere.</span><span class="sxs-lookup"><span data-stu-id="dc76e-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="dc76e-172">På siden **Indstillinger** under fanen **Konti** skal du klikke på **Angiv godkender**.</span><span class="sxs-lookup"><span data-stu-id="dc76e-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="dc76e-173">Vælg id'et for den bruger, som skal signere for en anden brugers ændringer, i feltet **Bruger-id for godkender**.</span><span class="sxs-lookup"><span data-stu-id="dc76e-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="dc76e-174">Vælg id'et for den bruger, hvis ændringer der skal signeres for, i feltet **Signer for bruger-id**.</span><span class="sxs-lookup"><span data-stu-id="dc76e-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>
