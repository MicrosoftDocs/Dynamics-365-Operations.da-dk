---
title: Inddrivelse af moms i Udgiftsstyring
description: "Dette emne forklarer, hvordan du kan få refunderet beløb fra berettigede momstransaktioner."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: da-dk
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a><span data-ttu-id="af81d-103">Inddrivelse af moms i Udgiftsstyring</span><span class="sxs-lookup"><span data-stu-id="af81d-103">VAT recovery in Expense management</span></span>

<span data-ttu-id="af81d-104">For at få beløb refunderet fra berettigede momstransaktioner skal en virksomhed eller organisation identificere, indsamle, kontrollere og indsende nøjagtige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="af81d-104">To receive refunds on eligible value-added tax (VAT) transactions, a company or organization must identify, collect, verify, and submit accurate information.</span></span> <span data-ttu-id="af81d-105">Denne proces omfatter flere forskellige opgaver, og afhængigt af virksomhedens størrelse, kan den omfatte flere medarbejdere eller roller.</span><span class="sxs-lookup"><span data-stu-id="af81d-105">This process includes multiple tasks and, depending on the size of your company, can include several employees or roles.</span></span>

<span data-ttu-id="af81d-106">For at få moms retur vha. Udgiftsstyring skal følgende opgaver fuldføres:</span><span class="sxs-lookup"><span data-stu-id="af81d-106">To recover VAT by using Expense management, the following prerequisites must be completed:</span></span>

- <span data-ttu-id="af81d-107">Der skal oprettes momsgrupper for lande/områder fordelt på udgiftsarter.</span><span class="sxs-lookup"><span data-stu-id="af81d-107">Tax codes must be created for countries/regions that are allocated to expense categories.</span></span>
- <span data-ttu-id="af81d-108">Der skal oprettes en momsgruppe for hver momskode.</span><span class="sxs-lookup"><span data-stu-id="af81d-108">A sales tax group must be created for each tax code.</span></span>
- <span data-ttu-id="af81d-109">Der skal oprettes en varemomskode for hver momsgruppe.</span><span class="sxs-lookup"><span data-stu-id="af81d-109">An item sales tax code must be created for each sales tax group.</span></span>

<span data-ttu-id="af81d-110">Når dette er fuldført, kan medarbejdere udføre disse trin for at anmode om momsrefusioner.</span><span class="sxs-lookup"><span data-stu-id="af81d-110">After the prerequisites are completed, employees follow these steps to request refunds for VAT transactions.</span></span>

1. <span data-ttu-id="af81d-111">I en udgiftsrapport skal der angives momsoplysninger om kreditkorttransaktioner for at identificere berettiget inddrivelse af moms.</span><span class="sxs-lookup"><span data-stu-id="af81d-111">On an expense report, enter tax information about credit card transactions to identify eligible VAT refunds.</span></span>
2. <span data-ttu-id="af81d-112">Kontroller, at alle momsoplysninger er fuldstændige, og bogfør derefter udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="af81d-112">Make sure that all tax information is complete, and then post the expense report.</span></span>
3. <span data-ttu-id="af81d-113">Behandl udgifter, der er berettigede til international momsopkrævning.</span><span class="sxs-lookup"><span data-stu-id="af81d-113">Process expenses that are eligible for international VAT recovery.</span></span>
4. <span data-ttu-id="af81d-114">Sende momsinddrivelsesdata til en tredjepartsleverandør for registrering af international inddrivelse af moms.</span><span class="sxs-lookup"><span data-stu-id="af81d-114">Send VAT recovery data to the third-party vendor to file international recovery returns.</span></span>
5. <span data-ttu-id="af81d-115">Behandle udgifter for indenlandsk inddrivelse af moms.</span><span class="sxs-lookup"><span data-stu-id="af81d-115">Process expenses for domestic VAT recovery.</span></span>

<span data-ttu-id="af81d-116">De følgende afsnit indeholder eksempler på, hvordan Contoso-medarbejdere udfører de enkelte trin.</span><span class="sxs-lookup"><span data-stu-id="af81d-116">The following sections provide examples that show how Contoso employees complete each step.</span></span>

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a><span data-ttu-id="af81d-117">I en udgiftsrapport skal du angive momsoplysninger om kreditkorttransaktioner for at identificere berettigede momsrefusioner</span><span class="sxs-lookup"><span data-stu-id="af81d-117">On an expense report, enter tax information about credit card transactions to identify eligible VAT refunds</span></span>

<span data-ttu-id="af81d-118">Nancy, som er sælger hos Contoso i USA, er for nylig kommet hjem fra en forretningsrejse til Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="af81d-118">Nancy, a Contoso sales representative who is based in the US, recently returned from a sales trip to the United Kingdom.</span></span> <span data-ttu-id="af81d-119">I løbet af rejsen har hun brugt sit private kreditkort til at betale for måltider.</span><span class="sxs-lookup"><span data-stu-id="af81d-119">During her trip, she incurred some personal credit card expenses for meals.</span></span> <span data-ttu-id="af81d-120">Nancy skal nu oprette en udgiftsrapport for at få dækket sine udgifter.</span><span class="sxs-lookup"><span data-stu-id="af81d-120">Nancy must now create an expense report to reconcile her expenses.</span></span>

<span data-ttu-id="af81d-121">Når Nancy indtaster oplysninger i sin udgiftsrapport, vælger hun **Storbritannien** i feltet **Land/område** på siden **Rediger udgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="af81d-121">When Nancy enters information on her expense report, she selects **United Kingdom** in the **Country/region** field on the **Edit expense report** page.</span></span> <span data-ttu-id="af81d-122">Listen over momsgrupper filtreres derefter, så den kun viser de grupper, der gælder for Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="af81d-122">The list of sales tax groups is then filtered so that it shows only the groups that apply to the United Kingdom.</span></span> <span data-ttu-id="af81d-123">Nancy vælger momsgruppen **Storbritannien 001**, og derefter vælger hun varemomsgruppen **Måltider**.</span><span class="sxs-lookup"><span data-stu-id="af81d-123">Nancy selects the **United Kingdom 001** sales tax group and then selects the **Meals** item sales tax group.</span></span> <span data-ttu-id="af81d-124">Derefter tilføjer hun en ny postering for overnatning.</span><span class="sxs-lookup"><span data-stu-id="af81d-124">She then adds a new transaction for her lodging.</span></span> <span data-ttu-id="af81d-125">Da der kun er én momsgruppe og varemomsgruppe for overnatning i Storbritannien, udfyldes disse oplysninger automatisk i Nancys udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="af81d-125">Because there is only one sales tax group and item sales tax group for lodging in the United Kingdom, this information is automatically filled in on Nancy's expense report.</span></span>

<span data-ttu-id="af81d-126">I henhold til Contosos politik skal alle udgifter have en sammenholdelseskvittering.</span><span class="sxs-lookup"><span data-stu-id="af81d-126">Per Contoso policy, all expenses must have a matching receipt.</span></span> <span data-ttu-id="af81d-127">Når Nancy gemmer sin udgiftsrapport, modtager hun derfor en meddelelse om, at hun skal vedhæfte en kvittering for hver transaktion, hun har angivet på udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="af81d-127">Therefore, when Nancy saves her expense report, she receives a message that states that she must attach a receipt for each transaction that she listed on her expense report.</span></span> <span data-ttu-id="af81d-128">Nancy kontrollerer, at hun har vedhæftet et digitalt billede af alle kvitteringer til udgiftsrapporten, og derefter sender hun rapporten til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="af81d-128">Nancy verifies that she has attached a digital image of each transaction receipt to her expense report and then submits her report for approval.</span></span> <span data-ttu-id="af81d-129">Derefter sender hun papirkvitteringerne til back-office-teamet.</span><span class="sxs-lookup"><span data-stu-id="af81d-129">She then sends the paper receipts to the back-office processing team.</span></span> <span data-ttu-id="af81d-130">Dette team sender de relevante momsdata til tredjepartsleverandøren, der administrerer international momsinddrivelse for Contoso.</span><span class="sxs-lookup"><span data-stu-id="af81d-130">This team will send the VAT recovery data to the third-party vendor that files international VAT recovery returns for Contoso.</span></span>

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a><span data-ttu-id="af81d-131">Kontroller, at alle momsoplysninger er fuldstændige, og bogfør derefter udgiftsrapporten</span><span class="sxs-lookup"><span data-stu-id="af81d-131">Make sure that all tax information is complete, and then post the expense report</span></span>

<span data-ttu-id="af81d-132">April, som er kreditorkoordinator hos Contoso, skal angive alle momsoplysninger, der mangler i en udgiftsrapport, før rapporten kan blive bogført.</span><span class="sxs-lookup"><span data-stu-id="af81d-132">April, the Accounts payable coordinator for Contoso, must enter any tax information that is missing from an expense report before the report can be posted.</span></span> <span data-ttu-id="af81d-133">Hun åbner siden **Detaljer om udgiftsrapporter** og ser Nancys godkendte udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="af81d-133">She opens the **Expense report details** page and sees Nancy's approved expense report.</span></span> <span data-ttu-id="af81d-134">April åbner derefter udgiftsrapporten for at få vist posteringsdetaljerne.</span><span class="sxs-lookup"><span data-stu-id="af81d-134">April then opens the expense report to view the details of the transactions.</span></span> <span data-ttu-id="af81d-135">Hun kan se, at Nancy ikke har angivet en varemomsgruppe for en af posteringerne.</span><span class="sxs-lookup"><span data-stu-id="af81d-135">She sees that Nancy didn't enter an item sales tax group for one of the transactions.</span></span> <span data-ttu-id="af81d-136">Da disse oplysninger ikke er angivet, kan April ikke bogføre udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="af81d-136">Because this information isn't provided, April can't post the expense report.</span></span> <span data-ttu-id="af81d-137">April ser derfor på siden **Momskonfigurationer** i Udgiftsstyring og finder den relevante varemomsgruppe for landet/området samt posteringstypen.</span><span class="sxs-lookup"><span data-stu-id="af81d-137">Therefore, April looks on the **Tax configurations** page in Expense management, and finds the appropriate item sales tax group for the country/region and the transaction type.</span></span> <span data-ttu-id="af81d-138">Nu kan April bogføre udgiftsrapporten i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="af81d-138">April can now post the expense report to the general ledger.</span></span>

<span data-ttu-id="af81d-139">Når April bogfører udgiftsrapporten, opretter der et arbejdselement for momsinddrivelse.</span><span class="sxs-lookup"><span data-stu-id="af81d-139">When April posts the expense report, a VAT recoverable work item is created.</span></span> <span data-ttu-id="af81d-140">Dette arbejdselement tildeles et medlem af back-office-teamet.</span><span class="sxs-lookup"><span data-stu-id="af81d-140">This work item is assigned to a member of the back-office processing team.</span></span> <span data-ttu-id="af81d-141">April får en meddelelse, der bekræfter, at bogføringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="af81d-141">April receives a message that confirms that posting was successful.</span></span> <span data-ttu-id="af81d-142">Denne meddelelse viser også antallet af fundne momstransaktioner, der kan refunderes.</span><span class="sxs-lookup"><span data-stu-id="af81d-142">This message also lists the number of VAT transactions that were identified for recovery.</span></span>

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a><span data-ttu-id="af81d-143">Behandl udgifter, der er berettigede til international momsopkrævning</span><span class="sxs-lookup"><span data-stu-id="af81d-143">Process expenses that are eligible for international VAT recovery</span></span>

<span data-ttu-id="af81d-144">Arnie, som er medlem af Contosos back-office-team, er ansvarlig for at bekræfte, at alle de påkrævede oplysninger i forbindelse med momsinddrivelse er inkluderet i udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="af81d-144">Arnie, a member of Contoso's back-office processing team, is responsible for confirming that all the required information for VAT recovery is included on expense reports.</span></span> <span data-ttu-id="af81d-145">Han åbner siden **Udgift med momsopkrævning** og vælger den udgiftsrapport, som Nancy har sendt.</span><span class="sxs-lookup"><span data-stu-id="af81d-145">He opens the **Expense tax recovery** page and selects the expense report that Nancy submitted.</span></span> <span data-ttu-id="af81d-146">Arnie kontrollerer, at alle de nødvendige kvitteringer er vedhæftet, og at den korrekte momsgruppe og varemomsgruppe er angivet.</span><span class="sxs-lookup"><span data-stu-id="af81d-146">Arnie verifies that all the required receipts are attached, and that the correct sales tax group and item sales tax codes were entered.</span></span>

<span data-ttu-id="af81d-147">Da Arnie modtager papirkvitteringerne fra Nancy, kontrollerer han dem mod de digitale kvitteringer og ændrer derefter status for udgiftsrapporten til **Klar til opkrævning**.</span><span class="sxs-lookup"><span data-stu-id="af81d-147">When Arnie receives the paper receipts from Nancy, he verifies the paper receipts against the digital receipts and then changes the status of the expense report to **Ready for recovery**.</span></span>

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a><span data-ttu-id="af81d-148">Sende momsinddrivelsesdata til en tredjepartsleverandør for registrering af international inddrivelse af moms</span><span class="sxs-lookup"><span data-stu-id="af81d-148">Send VAT recovery data to the third-party vendor to file international recovery returns</span></span>

<span data-ttu-id="af81d-149">Da Arnie er klar til at sende udgiftsrapportdataene til den tredjepartsleverandør, der registrerer momsinddrivelsen, åbner han siden **Udgift med momsopkrævning**.</span><span class="sxs-lookup"><span data-stu-id="af81d-149">When Arnie is ready to send the expense report data to the third-party vendor that will file the VAT recovery returns, he opens the **Expense tax recovery** page.</span></span> <span data-ttu-id="af81d-150">Han filtrerer siden, så den kun viser de udgiftsrapporter, der er markeret som **Klar til opkrævning**.</span><span class="sxs-lookup"><span data-stu-id="af81d-150">He filters the page so that it shows only the expense reports that are marked as **Ready for recovery**.</span></span> <span data-ttu-id="af81d-151">Derefter vælger han **Filer** &gt; **Eksportér til Excel**.</span><span class="sxs-lookup"><span data-stu-id="af81d-151">Arnie then selects **File** &gt; **Export to Excel**.</span></span> <span data-ttu-id="af81d-152">Momsoplysningerne fra udgiftsrapporten eksporteres til et Microsoft Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="af81d-152">The VAT information from the expense reports is exported to a Microsoft Excel worksheet.</span></span> <span data-ttu-id="af81d-153">Arnie sender regnearket til tredjepartsleverandøren og medsender en besked om, at papirkvitteringerne er blevet sendt med kurer.</span><span class="sxs-lookup"><span data-stu-id="af81d-153">Arnie submits this worksheet to the third-party vendor and includes a message that states that the paper receipts have been sent by courier.</span></span>

## <a name="process-expenses-for-domestic-vat-recovery"></a><span data-ttu-id="af81d-154">Behandle udgifter for indenlandsk inddrivelse af moms</span><span class="sxs-lookup"><span data-stu-id="af81d-154">Process expenses for domestic VAT recovery</span></span>

<span data-ttu-id="af81d-155">Arnie skal kontrollere, at udgiftsrapportposteringerne er berettigede for inddrivelse af moms, og at de digitale kvitteringer er vedhæftet rapporterne.</span><span class="sxs-lookup"><span data-stu-id="af81d-155">Arnie must verify that the expense report transactions are eligible for VAT recovery, and that the digital receipts are attached to the reports.</span></span> <span data-ttu-id="af81d-156">For at starte behandlingen af berettigede udgifter til indenlandsk inddrivelse åbner Arnie siden **Udgift med momsopkrævning** og vælger den udgiftsrapport, der kræver godkendelse.</span><span class="sxs-lookup"><span data-stu-id="af81d-156">To start to process eligible expenses for domestic recovery, Arnie opens the **Expense tax recovery** page and selects the expense report that requires verification.</span></span> <span data-ttu-id="af81d-157">Han bekræfter, at kvitteringerne lyder på virksomhedens navn frem for medarbejderens.</span><span class="sxs-lookup"><span data-stu-id="af81d-157">He verifies that receipts are in the name of the company instead of the employee.</span></span> <span data-ttu-id="af81d-158">Ved momsopkrævning skal kvitteringer være udstedt i virksomhedens navn.</span><span class="sxs-lookup"><span data-stu-id="af81d-158">For VAT recovery, receipts must be in the name of the company.</span></span> <span data-ttu-id="af81d-159">Arnie kontrollerer derefter, at den korrekte momsgruppe og varemomsgruppe er angivet.</span><span class="sxs-lookup"><span data-stu-id="af81d-159">Arnie then confirms that the correct sales tax group and item sales tax codes were applied.</span></span>

<span data-ttu-id="af81d-160">Da Arnie modtager papirkvitteringerne, ændrer han status for udgiftsrapporten til **Klar til opkrævning**.</span><span class="sxs-lookup"><span data-stu-id="af81d-160">When Arnie receives the paper receipts, he changes the status of the expense report to **Ready for recovery**.</span></span> <span data-ttu-id="af81d-161">Han kan derefter indsende anmodningen om refusion til den relevante skattemyndighed.</span><span class="sxs-lookup"><span data-stu-id="af81d-161">He can then file the return with the appropriate tax authority.</span></span> <span data-ttu-id="af81d-162">I dette tilfælde er skattemyndighederne det amerikanske skattevæsen (IRS - Internal Revenue Service).</span><span class="sxs-lookup"><span data-stu-id="af81d-162">In this case, the appropriate tax authority in the US is the Internal Revenue Service (IRS).</span></span>
