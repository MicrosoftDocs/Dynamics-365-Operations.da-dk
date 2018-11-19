---
title: Konfigurere tilbudsstyring
description: I dette emne beskrives, hvordan du kan konfigurere tilbud i Talent.
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: fa2f2f9f67562524961352a87a7db49992776e46
ms.contentlocale: da-dk
ms.lasthandoff: 10/22/2018

---
# <a name="set-up-offer-management"></a><span data-ttu-id="90dba-103">Konfigurere tilbudsstyring</span><span class="sxs-lookup"><span data-stu-id="90dba-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="90dba-104">Når en kandidat overgår til tilbudsstadiet i Dynamics 365 for Talent: Attract, skal du sikre dig, at der hurtigt kan oprettes tilbud til kandidaten, at de kan godkendes efter behov og sendes til kandidaten.</span><span class="sxs-lookup"><span data-stu-id="90dba-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="90dba-105">Da de fleste tilbud er standard, kan de oprettes fra genanvendelige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="90dba-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="90dba-106">I Attract er alle tilbud samlet i en tilbudspakke, der er en samling af et eller flere tilbudsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="90dba-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="90dba-107">I dette emne beskrives de trin, som Attract-administratorer skal følge for at konfigurere forskellige tilbudspakkeskabeloner som en del af tilbudsstyringsfunktionerne i Attract.</span><span class="sxs-lookup"><span data-stu-id="90dba-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="90dba-108">Brugere med ikke-administrator roller har ikke adgang til disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="90dba-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="90dba-109">Tilbudsstyringsfunktioner er tilgængelige som en del af tilføjelsesprogrammet til omfattende ansættelser.</span><span class="sxs-lookup"><span data-stu-id="90dba-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="90dba-110">Tilbudsdata</span><span class="sxs-lookup"><span data-stu-id="90dba-110">Offer data</span></span> 

<span data-ttu-id="90dba-111">Tilbudsdata er den mindste enhed i tilbudspakkeskabelonen.</span><span class="sxs-lookup"><span data-stu-id="90dba-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="90dba-112">Et typisk tilbud består af standardtekst og et sæt værdier.</span><span class="sxs-lookup"><span data-stu-id="90dba-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="90dba-113">Værdisættene er de eneste enheder, der kan skifte fra tilbud til tilbud.</span><span class="sxs-lookup"><span data-stu-id="90dba-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="90dba-114">Under oprettelsen af tilbuddet er det vigtigste aspekt, som den, der har oprettet tilbuddet, kan fokusere på, listen over pladsholderefor tilbudsdata, som findes i en tilbudspakkeskabelon.</span><span class="sxs-lookup"><span data-stu-id="90dba-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="90dba-115">Du kan angive tilbudsdata ved at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="90dba-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="90dba-116">Gå til **Tilbudsstyring**.</span><span class="sxs-lookup"><span data-stu-id="90dba-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="90dba-117">Udvid sektionen **Bibliotek** i den venstre navigationsrude, og gå derefter til **Tilbudsdata**.</span><span class="sxs-lookup"><span data-stu-id="90dba-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="90dba-118">På siden **Tilbudsdata** finder du sektionerne **Detaljer om kandidat** og **Jobdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="90dba-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="90dba-119">Attract indeholder som standard nogle tilbudsdatapladsholdere.</span><span class="sxs-lookup"><span data-stu-id="90dba-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="90dba-120">Der er sektioner på siden, hvor du kan organisere forskellige tilbudsdatapladsholdere i logiske grupper.</span><span class="sxs-lookup"><span data-stu-id="90dba-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="90dba-121">Disse sektioner kan hjælpe med vedligeholdelse af tilbudsdata og udfyldning af data under oprettelsen af tilbuddet.</span><span class="sxs-lookup"><span data-stu-id="90dba-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="90dba-122">Hvis du vil oprette en ny sektion med tilbudsdata, skal du klikke på **Tilføj en sektion** og angive et entydigt navn til sektionen.</span><span class="sxs-lookup"><span data-stu-id="90dba-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="90dba-123">Hvis du vil tilføje tilbudsdatapladsholdere i en bestemt sektion, skal du klikke på **Tilføj tilbudsdata** og angive et entydigt navn til pladsholderen.</span><span class="sxs-lookup"><span data-stu-id="90dba-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="90dba-124">Hvis du vil redigere navnet på en sektion, skal du pege på navnet på sektionen og opdatere navnet.</span><span class="sxs-lookup"><span data-stu-id="90dba-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="90dba-125">Hvis du vil redigere navnet på en eksisterende tilbudsdatapladsholder, skal du først sikre dig, at pladsholderen ikke allerede er en del af en skabelon.</span><span class="sxs-lookup"><span data-stu-id="90dba-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="90dba-126">Derefter skal du pege på navnet på tilbudsdatapladsholderen og opdatere navnet efter behov.</span><span class="sxs-lookup"><span data-stu-id="90dba-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="90dba-127">Hvis du vil slette en eksisterende tilbudsdatapladsholder, skal du først sikre dig, at pladsholderen ikke er en del af en anden skabelon.</span><span class="sxs-lookup"><span data-stu-id="90dba-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="90dba-128">Derefter skal du pege på pladsholderen, og når ikonet Papirkurv vises, skal du klikke på papirkurven for at slette tilbudsdatapladsholderen.</span><span class="sxs-lookup"><span data-stu-id="90dba-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="90dba-129">Du kan se, hvor mange skabeloner en tilbudsdatapladsholder er en del af ved hjælp af antalsindikatoren ud for de enkelte tilbudsdata.</span><span class="sxs-lookup"><span data-stu-id="90dba-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="90dba-130">Hvis du vil slette en sektion, skal du pege på navnet.</span><span class="sxs-lookup"><span data-stu-id="90dba-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="90dba-131">Hvis ingen af tilbudsdatapladsholderne i sektionen vises i en skabelon, kan du klikke på ikonet for papirkurven for at slette den.</span><span class="sxs-lookup"><span data-stu-id="90dba-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="90dba-132">Når du sletter sektionen, slettes også alle tilbudsdatapladsholdere i sektionen.</span><span class="sxs-lookup"><span data-stu-id="90dba-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="90dba-133">Når tilbudsdatapladsholderne er konfigureret, kan du bruge dem på tværs af alle dokumentskabeloner.</span><span class="sxs-lookup"><span data-stu-id="90dba-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="90dba-134">Tilbudsdatapladsholdere er ikke begrænset til en bestemt skabelon – det samme sæt kan bruges på tværs af alle skabeloner.</span><span class="sxs-lookup"><span data-stu-id="90dba-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="90dba-135">Regler for tilbudsdata</span><span class="sxs-lookup"><span data-stu-id="90dba-135">Offer data rules</span></span>

<span data-ttu-id="90dba-136">De fleste organisationer har regler for, hvordan tilbud skal oprettes.</span><span class="sxs-lookup"><span data-stu-id="90dba-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="90dba-137">En organisation kan f.eks. kræve, at den maksimale årsløn for en bestemt kombination af sted og anciennitetsniveau skal ligge inden for et bestemt interval, eller at der kun kan anvendes nogle få bestemte værdier for tilbudsniveauet i den nye stilling.</span><span class="sxs-lookup"><span data-stu-id="90dba-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="90dba-138">Attract understøtter aktuelt alle sådanne dataregler ved hjælp af en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="90dba-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="90dba-139">Når du vil forberede CSV-filen med datareglerne, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="90dba-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="90dba-140">Bestem tilbudsdatapladsholderen for regelsættet.</span><span class="sxs-lookup"><span data-stu-id="90dba-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="90dba-141">F.eks. **Årsløn**.</span><span class="sxs-lookup"><span data-stu-id="90dba-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="90dba-142">Identificer de afhængige værdier for tilbudspladsholderdata.</span><span class="sxs-lookup"><span data-stu-id="90dba-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="90dba-143">F.eks. **Placering af stilling** og **Niveau**.</span><span class="sxs-lookup"><span data-stu-id="90dba-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="90dba-144">Angiv kolonne 1 og 2 som **Placering af stilling** og **Niveau**.</span><span class="sxs-lookup"><span data-stu-id="90dba-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="90dba-145">Du kan overføre en værdi i intervallet ved at vælge **Årsløn** i kolonne 3 og 4.</span><span class="sxs-lookup"><span data-stu-id="90dba-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="90dba-146">Du kan overføre en bestemt værdi i stedet for et interval ved kun at vælge **Årsløn** i kolonne 3.</span><span class="sxs-lookup"><span data-stu-id="90dba-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="90dba-147">Angiv værdier i Microsoft Excel-filen ud fra de roller, du anvender.</span><span class="sxs-lookup"><span data-stu-id="90dba-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="90dba-148">Sørg for, at hver række er en entydig kombination af alle de værdier, der er sat sammen.</span><span class="sxs-lookup"><span data-stu-id="90dba-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="90dba-149">Gem filen i CSV-format.</span><span class="sxs-lookup"><span data-stu-id="90dba-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="90dba-150">Når du vil overføre filen med tilbudsdatareglerne, skal du gøre følgende.</span><span class="sxs-lookup"><span data-stu-id="90dba-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="90dba-151">Gå til **Tilbudsstyring**.</span><span class="sxs-lookup"><span data-stu-id="90dba-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="90dba-152">Udvid sektionen **Bibliotek** i det venstre navigationspanel, og gå derefter til **Regler for tilbudsdata**.</span><span class="sxs-lookup"><span data-stu-id="90dba-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="90dba-153">Klik på **Nyt datasæt** for at åbne dialogboksen **Overfør**.</span><span class="sxs-lookup"><span data-stu-id="90dba-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="90dba-154">Angiv et entydigt navn til regelsættet, og overfør derefter den gemte CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="90dba-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="90dba-155">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="90dba-155">Click **Add**.</span></span>
    <span data-ttu-id="90dba-156">Regelsættet behandles i baggrunden, og du får besked i app og via e-mail, når behandlingen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="90dba-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="90dba-157">Du får besked, hvis der opstår fejl under behandlingen af overførslen.</span><span class="sxs-lookup"><span data-stu-id="90dba-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="90dba-158">Du kan derefter hente fejlloggen, rette filen og overføre den igen.</span><span class="sxs-lookup"><span data-stu-id="90dba-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="90dba-159">Du kan bruge knappen (**...**), hvis du vil hente regelsættet og opdatere værdisættet.</span><span class="sxs-lookup"><span data-stu-id="90dba-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="90dba-160">Når du har opdateret, kan du overføre filen igen.</span><span class="sxs-lookup"><span data-stu-id="90dba-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="90dba-161">Du kan slette et eksisterende overført regelsæt, hvis den pladsholder, der defineres, ikke bruges i en anden dokumentskabelon.</span><span class="sxs-lookup"><span data-stu-id="90dba-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTER]
> - <span data-ttu-id="90dba-163">Hver enkelt pladsholder kan kun have ét entydigt sæt kolonner, som den er afhængig af.</span><span class="sxs-lookup"><span data-stu-id="90dba-163">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="90dba-164">F.eks. hvis **Årsløn** er afhængig af **Placering af stilling** og **Niveau**, du kan ikke overføre et andet regelsæt, hvor **Årsløn** er afhængig af et andet sæt af kolonner.</span><span class="sxs-lookup"><span data-stu-id="90dba-164">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="90dba-165">Du kan hente eksempelregelsæt med tilbudsdata under fanen **Eksempler** på siden **Regler for tilbudsdata**.</span><span class="sxs-lookup"><span data-stu-id="90dba-165">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="90dba-166">Når den, der har oprettet et tilbud, tilsidesætter de værdier, der anbefales i tilbudsdatareglerne, markeres tilbuddet som ikke-standard, og arbejdsgangen for tilbudsgodkendelse gøres obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="90dba-166">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="90dba-167">Dokumentskabeloner</span><span class="sxs-lookup"><span data-stu-id="90dba-167">Document templates</span></span>

<span data-ttu-id="90dba-168">En tilbudsdokumentskabelon kan hjælpe administratorer oprette tilbudsbreve.</span><span class="sxs-lookup"><span data-stu-id="90dba-168">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="90dba-169">Tilbudsdokumentskabelonen er en kombination af den tekst, der skal være en del af tilbuddet, samt de definerede tilbudsdatapladsholdere.</span><span class="sxs-lookup"><span data-stu-id="90dba-169">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="90dba-170">Gør følgende for at oprette en tilbudsdokumentskabelon.</span><span class="sxs-lookup"><span data-stu-id="90dba-170">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="90dba-171">Gå til **Tilbudsstyring**.</span><span class="sxs-lookup"><span data-stu-id="90dba-171">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="90dba-172">Udvid sektionen **Bibliotek** i den venstre navigationsrude, og gå til **Skabeloner**.</span><span class="sxs-lookup"><span data-stu-id="90dba-172">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="90dba-173">Siden **Skabeloner** indeholder en liste over de dokumentskabeloner, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="90dba-173">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="90dba-174">Klik på **Ny skabelon** for at oprette en ny dokumentskabelon.</span><span class="sxs-lookup"><span data-stu-id="90dba-174">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="90dba-175">Angiv et entydigt navn til skabelonen, og klik på **Opret**.</span><span class="sxs-lookup"><span data-stu-id="90dba-175">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="90dba-176">Du kan bruge RTF-editoren til at indsætte eller redigere tilbudsdokumentets indhold.</span><span class="sxs-lookup"><span data-stu-id="90dba-176">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="90dba-177">Du kan indsætte tabeller, billeder og hyperlinks ved hjælp af de tilgængelige indstillinger øverst i teksteditoren.</span><span class="sxs-lookup"><span data-stu-id="90dba-177">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="90dba-178">Du kan indsætte tilbudsdatapladsholdere i tilbudsskabelondokumentet ved at:</span><span class="sxs-lookup"><span data-stu-id="90dba-178">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="90dba-179">Trække og slippe fra højre rude.</span><span class="sxs-lookup"><span data-stu-id="90dba-179">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="90dba-180">Indsætte hashtag for tilbudsdatapladsholderen direkte på den ønskede placering.</span><span class="sxs-lookup"><span data-stu-id="90dba-180">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="90dba-181">Skriv **\#**, og begynd at skrive navnet på tilbudsdatapladsholderen.</span><span class="sxs-lookup"><span data-stu-id="90dba-181">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="90dba-182">Der vises indstillinger på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="90dba-182">Options will appear in the drop-down list.</span></span> <span data-ttu-id="90dba-183">Klik eller tryk på **Enter** for at indsætte tilbudsdatapladsholderen.</span><span class="sxs-lookup"><span data-stu-id="90dba-183">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTER]
    > - <span data-ttu-id="90dba-185">Hvis du vil knytte en pladsholder til tilbudsdokumentskabelonen, uden at kandidaten kan se pladsholderværdien, skal du pege på tilbudsdatapladsholderen og klikke på ikonet **Fastgør**.</span><span class="sxs-lookup"><span data-stu-id="90dba-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="90dba-186">Dette overfører pladsholderen til sektionen **Fastgjorte tilbudsdata** i tilbudsdokumentskabelonen.</span><span class="sxs-lookup"><span data-stu-id="90dba-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="90dba-187">Du kan fjerne fastgørelsen ved at følge samme fremgangsmåde, men klikke på **Frigør** på listen over tilbudsdatapladsholdere.</span><span class="sxs-lookup"><span data-stu-id="90dba-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="90dba-188">For at få vist listen over aktive tilbudsdatapladsholdere skal du skifte til fanen **Aktiv** i den højre rude.</span><span class="sxs-lookup"><span data-stu-id="90dba-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="90dba-189">Hvis du indsætter en pladsholder, der styres af et regelsæt for tilbudsdata, kan du se tilbudsdatapladsholderens afhængighed af andre værdier.</span><span class="sxs-lookup"><span data-stu-id="90dba-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="90dba-190">Alternativt kan vælge **Importér** for at importere indholdet fra en .docx-fil på din lokale computer og redigere den efter behov.</span><span class="sxs-lookup"><span data-stu-id="90dba-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="90dba-191">På denne måde behøver du ikke at skrive i alt indhold i editoren.</span><span class="sxs-lookup"><span data-stu-id="90dba-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="90dba-192">Hvis du vil se tilbudsdokumentet formateret, kan du bruge indstillingen **Eksempel** øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="90dba-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="90dba-193">Hvis du vil styre, om den, der opretter et tilbud, skal kunne redigere tilbudsdokumentets indhold, skal du bruge indstillingen **Administrer rettighed** øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="90dba-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="90dba-194">Hvis den, der har oprettet tilbuddet, kun skal kunne indsætte pladsholderværdier og ikke redigere tekst, skal du indstille rettighedsværdien til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="90dba-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="90dba-195">Klik på **Gem** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="90dba-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="90dba-196">Skabelonen gemmes i kladdetilstand.</span><span class="sxs-lookup"><span data-stu-id="90dba-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="90dba-197">Hvis du vil afslutte og markere dokumentet som publiceret, skal du klikke på **Afslut**.</span><span class="sxs-lookup"><span data-stu-id="90dba-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="90dba-198">Du kan se, hvilke dokumentskabeloner der er aktive, i kladdetilstand og er arkiveret og ikke længere i brug på dokumentskabelonbibliotekets landingsside.</span><span class="sxs-lookup"><span data-stu-id="90dba-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="90dba-199">Du kan slette alle tilbudsdokumentskabeloner, der ikke er en del af en eksisterende tilbudspakkeskabelon.</span><span class="sxs-lookup"><span data-stu-id="90dba-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="90dba-200">Skabeloner til tilbudspakker</span><span class="sxs-lookup"><span data-stu-id="90dba-200">Offer package templates</span></span>

<span data-ttu-id="90dba-201">Tilbudspakker er de tilbudselementer, der deles med kandidaten. De består af en kombination af en eller flere tilbudsdokumentskabeloner.</span><span class="sxs-lookup"><span data-stu-id="90dba-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="90dba-202">Gør følgende for at oprette en tilbudspakke.</span><span class="sxs-lookup"><span data-stu-id="90dba-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="90dba-203">Gå til **Tilbudsstyring**.</span><span class="sxs-lookup"><span data-stu-id="90dba-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="90dba-204">Gå til **Pakker** fra den venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="90dba-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="90dba-205">Der vises en liste over aktive pakkeskabeloner, der er tilgængelige for personer, der vil oprette tilbud.</span><span class="sxs-lookup"><span data-stu-id="90dba-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="90dba-206">Hvis du vil oprette en ny tilbudspakke, skal du klikke på **Ny pakke**.</span><span class="sxs-lookup"><span data-stu-id="90dba-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="90dba-207">Angiv et entydigt navn, og klik på **Opret**.</span><span class="sxs-lookup"><span data-stu-id="90dba-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="90dba-208">Klik på **Tilføj skabelon**.</span><span class="sxs-lookup"><span data-stu-id="90dba-208">Click **Add template**.</span></span>

    >[!NOTER]
    > - <span data-ttu-id="90dba-210">Du kan vælge at oprette en ny skabelon eller vælge fra en eksisterende.</span><span class="sxs-lookup"><span data-stu-id="90dba-210">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="90dba-211">Hvis du vil tilføje en eksisterende skabelon, skal du kontrollere, at tilbudsdokumentskabelonen er gemt, færdiggjort og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="90dba-211">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="90dba-212">Du kan vælge lige så mange dokumentskabeloner, som du vil.</span><span class="sxs-lookup"><span data-stu-id="90dba-212">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="90dba-213">Klik på **Udført** for at vende tilbage til **Pakkestyring**.</span><span class="sxs-lookup"><span data-stu-id="90dba-213">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="90dba-214">Du kan konfigurere rækkefølgen af dokumenterne, og du kan også angive, om der kræves bestemte tilbudsdokumenter under oprettelsen af tilbuddet.</span><span class="sxs-lookup"><span data-stu-id="90dba-214">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="90dba-215">Den, der opretter tilbuddet, får mulighed for at slette de dokumenter, der er markeret som **Kræves ikke**.</span><span class="sxs-lookup"><span data-stu-id="90dba-215">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="90dba-216">Hvis du vil gemme tilbudspakkeskabelonen, så den kan bruges af alle, der opretter tilbud, skal du klikke på **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="90dba-216">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="90dba-217">Du kan se udkast til tilbudspakkeskabeloner ved at gå til fanen **Kladder**. Hvis der foretages en ændring af tilbudspakkeskabelonen, skal den gemmes og udgives igen.</span><span class="sxs-lookup"><span data-stu-id="90dba-217">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="90dba-218">Konfigurere en tilbudsproces</span><span class="sxs-lookup"><span data-stu-id="90dba-218">Configure an offer process</span></span>

<span data-ttu-id="90dba-219">Der er flere dele af tilbudsoprettelsesprocessen, som kan konfigureres af en Attract-administrator.</span><span class="sxs-lookup"><span data-stu-id="90dba-219">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="90dba-220">**Godkendelser af tilbud** - Vælg, om der skal kræves godkendelser af et tilbud, før det kan sendes til kandidaten.</span><span class="sxs-lookup"><span data-stu-id="90dba-220">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="90dba-221">Som administrator kan du også bestemme, om alle tilbudsgodkendelser skal ske fortløbende eller i en parallel godkendelsesproces.</span><span class="sxs-lookup"><span data-stu-id="90dba-221">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="90dba-222">Du kan også bestemme, om godkendere af tilbuddet skal tilføje en kommentar sammen med deres tilbudsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="90dba-222">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="90dba-223">Tilbudsgodkendelser er obligatoriske for alle ikke-standard tilbud.</span><span class="sxs-lookup"><span data-stu-id="90dba-223">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="90dba-224">**Kandidatens tilbudsoplevelse** - Som administrator kan du vælge at angive, om alle tilbud skal have en udløbsdato, og i så fald hvad udløbsdatoens forskydning skal være som standard.</span><span class="sxs-lookup"><span data-stu-id="90dba-224">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="90dba-225">Du kan også konfigurere, om kandidater kan vælge at afvise et tilbud.</span><span class="sxs-lookup"><span data-stu-id="90dba-225">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="90dba-226">**e-signaturer** - Den eneste indstilling med elektronisk signatur, der er tilgængelig for kandidater i øjeblikket, er at skrive deres navn i tilbudspakken, når de accepter tilbuddet.</span><span class="sxs-lookup"><span data-stu-id="90dba-226">**e-Signatures** - Currently, the only electronic signature option available is for candidates to type their name in the offer package while accepting the offer.</span></span> <span data-ttu-id="90dba-227">Vi introducerer partnerintegration med andre udbydere af elektroniske signaturer i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="90dba-227">We will introduce partner integrations with other electronic signature providers in the future.</span></span>


<span data-ttu-id="90dba-228">Hvis du vil vide mere om oprettelsen af tilbuddet, kan du se under [Oprettelse, godkendelse og signering af tilbud](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="90dba-228">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>

