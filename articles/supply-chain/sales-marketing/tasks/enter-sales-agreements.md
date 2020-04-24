---
title: Indgå salgsaftaler
description: Dette emne viser, hvordan du opretter en salgsaftale, der forpligter en af dine kunder til at købe et produkt for et aftalt beløb over en tidsperiode mod at få særlige rabatter.
author: omulvad
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 723621f61a237d4b390271e65bce204c44ee4fc2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204326"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="d9e09-103">Indgå salgsaftaler</span><span class="sxs-lookup"><span data-stu-id="d9e09-103">Enter sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9e09-104">Dette emne viser, hvordan du opretter en salgsaftale, der forpligter en af dine kunder til at købe et produkt for et aftalt beløb over en tidsperiode mod at få særlige rabatter.</span><span class="sxs-lookup"><span data-stu-id="d9e09-104">This topic explains how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="d9e09-105">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="d9e09-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="d9e09-106">Konfigurere salgsaftaleoverskrift</span><span class="sxs-lookup"><span data-stu-id="d9e09-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="d9e09-107">Gå i navigationsruden til **Moduler > Salg og marketing > Salgsaftaler > Salgsaftaler**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-107">In the navigation pane, go to **Modules > Sales and marketing > Sales agreements > Sales agreements**.</span></span>
2. <span data-ttu-id="d9e09-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-108">Select **New**.</span></span>
3. <span data-ttu-id="d9e09-109">Vælg den ønskede post på rullemenuen i feltet **Debitorkonto**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-109">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="d9e09-110">Vælg den ønskede post på rullemenuen i feltet **Salgsaftaleklassifikation**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-110">In the **Sales agreement classification** field, select the desired record from the drop-down menu.</span></span>
5. <span data-ttu-id="d9e09-111">Udvid sektionen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-111">Expand the **General** section.</span></span>
6. <span data-ttu-id="d9e09-112">Vælg **Bundet produktværdi** i feltet **Standardtilsagn**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-112">In the **Default commitment** field, select **Product value commitment**.</span></span> <span data-ttu-id="d9e09-113">En tilsagnstype er et obligatorisk kriterium, som du skal tildele til aftalen for at definere, hvordan aftalekontrakten skal opfyldes.</span><span class="sxs-lookup"><span data-stu-id="d9e09-113">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="d9e09-114">Med de fire foruddefinerede typer kan du angive kundens tilsagnsmål udtrykt som en mængde eller værdi.</span><span class="sxs-lookup"><span data-stu-id="d9e09-114">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="d9e09-115">Mængdetilsagnstypen kan kun anvendes på et bestemt produkt, men de værdibaserede typerne gælder for salget af specifikke og ikke-specifikke produkter.</span><span class="sxs-lookup"><span data-stu-id="d9e09-115">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
7. <span data-ttu-id="d9e09-116">Indstil datoen i feltet **Udløbsdato** til en fremtidig dato, hvor du vil have, at aftalen udløber.</span><span class="sxs-lookup"><span data-stu-id="d9e09-116">In the **Expiration date** field, set the date to a future date when you want the agreement to expire.</span></span>
8. <span data-ttu-id="d9e09-117">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-117">Select **OK**.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="d9e09-118">Konfigurere bundede produktværdilinjer</span><span class="sxs-lookup"><span data-stu-id="d9e09-118">Set up product value commitment lines</span></span>
1. <span data-ttu-id="d9e09-119">Vælg **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-119">Select **Add line**.</span></span>
2. <span data-ttu-id="d9e09-120">Vælg den ønskede post på rullemenuen i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-120">In the **Item number** field, select the desired record from the drop-down menu.</span></span> <span data-ttu-id="d9e09-121">Tilsagnstypen, som du har valgt til denne aftale, påvirker, hvilken type oplysninger du kan angive for aftalelinjerne.</span><span class="sxs-lookup"><span data-stu-id="d9e09-121">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="d9e09-122">For en værdibaseret aftale skal du for eksempel angive det samlede nettobeløb (i den aftalte valuta), som kunden giver tilsagn om at købe varer fra dig for.</span><span class="sxs-lookup"><span data-stu-id="d9e09-122">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="d9e09-123">I dette eksempel er felterne **Antal** og **Enhed** på linjen ikke tilgængelige, fordi du opretter en aftale for kunden om at købe en bestemt værdi af et produkt.</span><span class="sxs-lookup"><span data-stu-id="d9e09-123">In this example the **Quantity** and **Unit** fields on the line are unavailable because you're creating an agreement for the customer to buy a specific value of a product.</span></span>   
3. <span data-ttu-id="d9e09-124">Angiv det pengebeløb, som kunden har forpligtet sig til at købe for, i feltet **Nettobeløb**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-124">In the **Net amount** field, enter the monetary amount that the customer has committed to buying.</span></span>
4. <span data-ttu-id="d9e09-125">Angiv en værdi i procent, som skal gælde for kundens salgsordrelinjer, der er knyttet til denne aftale, i feltet **Rabatprocent**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-125">In the **Discount percent** field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
5. <span data-ttu-id="d9e09-126">Vis eller skjul sektionen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-126">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="d9e09-127">Vælg **Ja** i feltet **Maks. gennemtvinges**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-127">Select **Yes** in the **Max is enforced** field.</span></span>
    - <span data-ttu-id="d9e09-128">Hvis du vælger **Maks. gennemtvinges** betyder det, at det samlede beløb for alle de salgsordrelinjer, der bruger tilsagnets specielle priser, rabatter og/eller betalingsbetingelser, ikke må overstige det beløb, der er angivet i tilsagnet.</span><span class="sxs-lookup"><span data-stu-id="d9e09-128">Selecting **Max is enforced** means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    - <span data-ttu-id="d9e09-129">Minimum- og maksimumfrigivelsesbeløbet angiver et interval af værdier, der skal sælges på hver salgsordre, der bruger den valgte aftale.</span><span class="sxs-lookup"><span data-stu-id="d9e09-129">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
7. <span data-ttu-id="d9e09-130">Udvid sektionen **Salgsaftaleoverskrift**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-130">Expand the **Sales agreement header** section.</span></span> <span data-ttu-id="d9e09-131">Medmindre aftalens status er indstillet til **Gældende**, kan salgsordrer ikke knyttes til aftalen og kan derfor ikke bidrage til opfyldelsen af denne aftale.</span><span class="sxs-lookup"><span data-stu-id="d9e09-131">Unless the status of the agreement is set to **Effective**, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="d9e09-132">Du kan ændre statussen manuelt på dette trin.</span><span class="sxs-lookup"><span data-stu-id="d9e09-132">You can change the status manually at this stage.</span></span> <span data-ttu-id="d9e09-133">Status vil dog normalt ændres, når du bekræfter aftalen for kunden.</span><span class="sxs-lookup"><span data-stu-id="d9e09-133">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
8. <span data-ttu-id="d9e09-134">Klik på **Salgsaftale** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d9e09-134">On the Action Pane, select **Sales agreement**.</span></span>
9. <span data-ttu-id="d9e09-135">Vælg **Bekræftelse**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-135">Select **Confirmation**.</span></span> <span data-ttu-id="d9e09-136">Kontrollér, at indstillingen **Markér aftale som gældende** er sat til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-136">Make sure that the **Mark agreement as effective** option is set to **Yes**.</span></span>  
10. <span data-ttu-id="d9e09-137">Vælg **Ja** i feltet **Udskriv rapport**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-137">Select **Yes** in the **Print report** field.</span></span>
11. <span data-ttu-id="d9e09-138">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9e09-138">Select **OK**.</span></span>
12. <span data-ttu-id="d9e09-139">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9e09-139">Close the page.</span></span> <span data-ttu-id="d9e09-140">Aftalen er nu gældende.</span><span class="sxs-lookup"><span data-stu-id="d9e09-140">The agreement is now effective.</span></span> <span data-ttu-id="d9e09-141">Du kan begynde at knytte kundens ordrer til aftalen for at modpostere mod tilsagnsmålet.</span><span class="sxs-lookup"><span data-stu-id="d9e09-141">You can start linking the customer's orders to the agreement to offset against the committed target.</span></span>  

