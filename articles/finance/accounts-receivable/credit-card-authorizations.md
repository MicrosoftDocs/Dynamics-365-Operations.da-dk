---
title: Opsætning, godkendelse og opsamling af kreditkort
description: Denne artikel indeholder en oversigt over kreditkortgodkendelse i Microsoft Dynamics 365 Finance. Den indeholder oplysninger om, hvordan du kan konfigurere en betalingstjeneste, føje et kreditkort til en salgsordre og erklære en tilladelse ugyldig.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b59d54df9427961e2c4fb6f1387646d6fe8dfc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837123"
---
# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="804bf-104">Opsætning, godkendelse og opsamling af kreditkort</span><span class="sxs-lookup"><span data-stu-id="804bf-104">Credit card setup, authorization, and capture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="804bf-105">Denne artikel indeholder en oversigt over kreditkortgodkendelse i Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="804bf-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="804bf-106">Den indeholder oplysninger om, hvordan du kan konfigurere en betalingstjeneste, føje et kreditkort til en salgsordre og erklære en tilladelse ugyldig.</span><span class="sxs-lookup"><span data-stu-id="804bf-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="804bf-107">Opsætning af kreditkortbetalingstjeneste</span><span class="sxs-lookup"><span data-stu-id="804bf-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="804bf-108">Hvis du vil bruge kreditkort, skal du konfigurere og aktivere en betalingstjeneste på siden Betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="804bf-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="804bf-109">En betalingstjeneste fungerer som en bro mellem din juridiske enhed og den bank, der behandler en debitors kreditkort.</span><span class="sxs-lookup"><span data-stu-id="804bf-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="804bf-110">Du skal arbejde med en udbyder af kreditkort, der er angivet i feltet Betalingsconnector, og konfigurere en konto hos denne udbyder.</span><span class="sxs-lookup"><span data-stu-id="804bf-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="804bf-111">Du skal derefter konfigurere andre indstillinger på siden Betalingstjenester, konfigurere kreditkorttyper for American Express, Discover og MasterCard på siden Kreditkorttyper og aktivere udbyderen som standardudbyder.</span><span class="sxs-lookup"><span data-stu-id="804bf-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="804bf-112">Du skal også følge disse trin for at fuldføre konfigurationen:</span><span class="sxs-lookup"><span data-stu-id="804bf-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="804bf-113">På siden Debitorparametre skal du angive parametre for brug af kreditkortgodkendelser.</span><span class="sxs-lookup"><span data-stu-id="804bf-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="804bf-114">På siden Betalingsbetingelser skal du konfigurere betalingsbetingelser for kreditkort.</span><span class="sxs-lookup"><span data-stu-id="804bf-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="804bf-115">Vælg Kreditkort i feltet Betalingstype.</span><span class="sxs-lookup"><span data-stu-id="804bf-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="804bf-116">Angiv kreditkortoplysninger for debitorer på siden Debitorkreditkort.</span><span class="sxs-lookup"><span data-stu-id="804bf-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="804bf-117">Tilføje et nyt kreditkort</span><span class="sxs-lookup"><span data-stu-id="804bf-117">Adding a new credit card</span></span>
<span data-ttu-id="804bf-118">Du kan oprette nye kreditkortposter på siden Debitorer ved hjælp af Debitor, Opsætning, Kreditkort.</span><span class="sxs-lookup"><span data-stu-id="804bf-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="804bf-119">Du kan også oprette kreditkortposter, når du angiver salgsordrer på siden Salgsordre ved hjælp af Administrer, Debitor, Kreditkort, Registrer.</span><span class="sxs-lookup"><span data-stu-id="804bf-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>

<a name="adding-a-credit-card-to-a-sales-order"></a><span data-ttu-id="804bf-120">Føje et kreditkort til en salgsordre</span><span class="sxs-lookup"><span data-stu-id="804bf-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="804bf-121">Du kan føje et kreditkort til en salgsordre ved at vælge et kreditkort i kreditkortopslaget på oversigtspanelet Prisen og rabatter på siden Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="804bf-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="804bf-122">Start godkendelsesprocessen ved at vælge Kreditkort og Godkend i handlingsruden på fanen Administrer.</span><span class="sxs-lookup"><span data-stu-id="804bf-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>

<a name="authorizing-a-credit-card"></a><span data-ttu-id="804bf-123">Godkende et kreditkort</span><span class="sxs-lookup"><span data-stu-id="804bf-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="804bf-124">Når et kreditkort godkendes, kontrolleres kortnummeret og kortholders navn, og den disponible saldo bekræftes.</span><span class="sxs-lookup"><span data-stu-id="804bf-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="804bf-125">Kreditkortets kontrolnummer og kortindehaverens adresse kan eventuelt verificeres.</span><span class="sxs-lookup"><span data-stu-id="804bf-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="804bf-126">Debitors disponible kreditsaldo reduceres derefter med fakturabeløbet.</span><span class="sxs-lookup"><span data-stu-id="804bf-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="804bf-127">Betalingstjenesten sender oplysninger om, hvorvidt kreditkortet er godkendt eller afvist.</span><span class="sxs-lookup"><span data-stu-id="804bf-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="804bf-128">Når salgsordren faktureres, trækkes (opsamles) fakturabeløbet på kreditkortet.</span><span class="sxs-lookup"><span data-stu-id="804bf-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="804bf-129">Værdi for kontrolnummer på kreditkort</span><span class="sxs-lookup"><span data-stu-id="804bf-129">Card verification value</span></span>

<span data-ttu-id="804bf-130">Du kan kræve at få oplyst kortets verifikationsværdi, der også kaldes kortets sikkerhedskode.</span><span class="sxs-lookup"><span data-stu-id="804bf-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="804bf-131">I forbindelse med American Express er det en firecifret værdi.</span><span class="sxs-lookup"><span data-stu-id="804bf-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="804bf-132">I forbindelse med Discover, MasterCard og Visa er det en trecifret værdi.</span><span class="sxs-lookup"><span data-stu-id="804bf-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="804bf-133">Bekræftelse af adresse</span><span class="sxs-lookup"><span data-stu-id="804bf-133">Address verification</span></span>

<span data-ttu-id="804bf-134">Kontrol af adresseoplysninger sendes altid til betalingsudbyderen.</span><span class="sxs-lookup"><span data-stu-id="804bf-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="804bf-135">Du kan vælge, hvor mange oplysninger der er nødvendige for, at en postering kan accepteres.</span><span class="sxs-lookup"><span data-stu-id="804bf-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="804bf-136">Sørg for at tjekke med din udbyder for at finde ud af, om de kan acceptere disse oplysninger.</span><span class="sxs-lookup"><span data-stu-id="804bf-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="804bf-137">Her er indstillingerne for bekræftelse af adresse:</span><span class="sxs-lookup"><span data-stu-id="804bf-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="804bf-138">**Acceptér altid postering** – Accepterer posteringen, uanset resultaterne af adressekontrollen.</span><span class="sxs-lookup"><span data-stu-id="804bf-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="804bf-139">**Kontoindehaver** – Sammenlign kortholderens navn på posteringen med oplysningerne fra kreditkortudstederen.</span><span class="sxs-lookup"><span data-stu-id="804bf-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="804bf-140">**Faktureringsadresse** – Sammenlign kortindehaverens navn og faktureringsadressen for posteringen med kreditkortudstederens oplysninger.</span><span class="sxs-lookup"><span data-stu-id="804bf-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="804bf-141">**Postnummer i faktureringsadresse** – Sammenlign kortindehaverens navn, faktureringsadresse og postnummer for posteringen med kreditkortudstederens oplysninger.</span><span class="sxs-lookup"><span data-stu-id="804bf-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="804bf-142">Dataunderstøttelse</span><span class="sxs-lookup"><span data-stu-id="804bf-142">Data support</span></span>
<span data-ttu-id="804bf-143">For hver kreditkorttype, der understøttes, kan du angive niveauet af dataunderstøttelse.</span><span class="sxs-lookup"><span data-stu-id="804bf-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="804bf-144">Niveauet styrer, hvor mange oplysninger om en transaktion der overføres til betalingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="804bf-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="804bf-145">Sørg for at tjekke med din udbyder for at finde ud af, om de kan stille sådanne oplysninger til rådighed.</span><span class="sxs-lookup"><span data-stu-id="804bf-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="804bf-146">Her er indstillingerne for understøttelsen af data:</span><span class="sxs-lookup"><span data-stu-id="804bf-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="804bf-147">**Niveau 1** – Overfører posteringsdato, posteringsbeløb og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="804bf-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="804bf-148">**Niveau 2** – Overfører oplysninger fra niveau 1 samt afsendelses- og forhandleradresser og momsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="804bf-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="804bf-149">**Niveau 3** – Overfører alle oplysninger fra niveau 2 samt ordrelinjeoplysninger.</span><span class="sxs-lookup"><span data-stu-id="804bf-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="804bf-150">Delvise betalinger</span><span class="sxs-lookup"><span data-stu-id="804bf-150">Partial payments</span></span>
<span data-ttu-id="804bf-151">Hvis du leverer en del af en ordre, registreres beløbet til den delvise ordre, og tilladelsen, som gælder beløbet for hele ordren, lukkes.</span><span class="sxs-lookup"><span data-stu-id="804bf-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="804bf-152">En ny godkendelse overføres derefter til det resterende beløb for den del af ordren, der ikke er leveret.</span><span class="sxs-lookup"><span data-stu-id="804bf-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="804bf-153">Annullere en godkendelse</span><span class="sxs-lookup"><span data-stu-id="804bf-153">Voiding an authorization</span></span>
<span data-ttu-id="804bf-154">Du kan ændre betalingsmåden for at annullere en kreditkortgodkendelse, til en anden metode, der ikke har en type af kreditkort.</span><span class="sxs-lookup"><span data-stu-id="804bf-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]