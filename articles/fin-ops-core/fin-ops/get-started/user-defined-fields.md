---
title: Oprette og arbejde med brugerdefinerede felter
description: I dette emne vises, hvordan du kan oprette brugerdefinerede felter gennem brugergrænsefladen for at skræddersy programmet, så det passer til din virksomhed.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 5f74397bcdd59a1fe24f5b6046081cbd2bed461b
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693539"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="6a6d2-103">Oprette og arbejde med brugerdefinerede felter</span><span class="sxs-lookup"><span data-stu-id="6a6d2-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a6d2-104">Selvom der findes et omfattende sæt af felter klar til brug til administration af en lang række forretningsprocesser, er der nogle gange et behov for, at et firma kan spore flere oplysninger i systemet.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="6a6d2-105">Mens programmører kan bruges til at tilføje disse felter som filtypenavne i udviklingsværktøjerne, kan felter tilføjes direkte fra brugergrænsefladen i funktionen til brugerdefinerede felter, hvilket giver dig mulighed for at skræddersy programmet, så det passer til din virksomhed ved hjælp af din webbrowser.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="6a6d2-106">Muligheden for at tilføje brugerdefinerede felter findes i platformsopdatering 13 og nyere.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-106">The ability to add custom fields is available in platform update 13 and later.</span></span> <span data-ttu-id="6a6d2-107">Kun brugere med specielle tilladelser har adgang til denne funktion.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-107">Only users with special permissions have access to this feature.</span></span>

<span data-ttu-id="6a6d2-108">Denne video viser, hvor let det er at føje et brugerdefineret felt til en side: [Tilføje brugerdefinerede felter](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="6a6d2-108">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="6a6d2-109">Oprettelse af brugerdefinerede felter</span><span class="sxs-lookup"><span data-stu-id="6a6d2-109">Creating custom fields</span></span>

<span data-ttu-id="6a6d2-110">Når du har identificeret yderligere oplysninger, du vil spore i programmet, kan du oprette det brugerdefinerede felt i den relevante tabel og vise det nye felt på en side.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-110">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="6a6d2-111">Følgende trin beskriver processen til oprettelse af et brugerdefineret felt og placeringen af det på en formular.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-111">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="6a6d2-112">Gå til formularen, hvor der er behov for det nye felt.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-112">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="6a6d2-113">Da slutmålet er at vise det brugerdefinerede felt i en formular, befinder startpunktet for oprettelse af brugerdefinerede felter i sig i området til brugertilpasning.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-113">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="6a6d2-114">Åbn værktøjslinjen til brugertilpasning ved at vælge **Indstillinger** og derefter **Tilpas denne formular**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-114">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="6a6d2-115">Klik på **Indsæt** og derefter på **Felt**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-115">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="6a6d2-116">Vælg området af formularen, hvor du vil vise det nye felt.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-116">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="6a6d2-117">Efter markeringen viser dialogboksen **Indsæt felter** en liste over eksisterende felter, der kan indsættes i det valgte område i formularen.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-117">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="6a6d2-118">Kontrollér, at feltet, du er interesseret i, ikke allerede findes på listen.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-118">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="6a6d2-119">Hvis det er tilfældet, kan du blot markere feltet på listen og klikke på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-119">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="6a6d2-120">Klik på den **Opret nyt felt** oven over listen for at starte processen med at oprette et brugerdefineret felt.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-120">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="6a6d2-121">Derved åbnes dialogboksen **Opret nyt felt**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-121">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="6a6d2-122">Hvis du ikke kan se knappen **Opret nyt felt**, har du ikke de nødvendige tilladelser til at bruge denne funktion.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-122">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="6a6d2-123">I dialogboksen **Opret nyt felt** skal du angive følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-123">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="6a6d2-124">Vælg den databasetabel, hvor feltet skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-124">Select the database table where this field should be added.</span></span> <span data-ttu-id="6a6d2-125">Bemærk, at kun de tabeller, der understøtter brugerdefinerede felter, vises på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-125">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="6a6d2-126">Se afsnittet nedenfor, for at få tekniske oplysninger om understøttede tabeller.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-126">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="6a6d2-127">Vælg datatypen for det nye felt.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-127">Select the data type for the new field.</span></span> <span data-ttu-id="6a6d2-128">De tilgængelige datatyper er afkrydsningsfelt, dato, dato/klokkeslæt, decimal, tal, valgliste og tekst.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-128">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="6a6d2-129">Hvis du vælger datatypen tekst, kan du også angive den maksimale længde for den tekst, der kan angives i dette felt.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-129">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="6a6d2-130">Hvis du vælger datatypen valglisten, kan du også vælge sættet af gyldige værdier for feltet.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-130">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="6a6d2-131">Angiv et navn, en etiket og en hjælpetekst for feltet.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-131">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="6a6d2-132">Navnet svarer til det fysiske feltnavn i databasen, mens etiket og hjælpeteksten er den tekst, der bruges til at repræsentere feltet i brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-132">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="6a6d2-133">Hvis dette er det eneste felt, du skal oprette til denne formular, skal du klikke på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-133">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="6a6d2-134">Hvis du vil oprette flere felter, skal du klikke på **Gem og ny**, og gå tilbage til trin 7.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-134">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="6a6d2-135">Bemærk, at der i øjeblikket er en grænse på **20 brugerdefinerede felter pr. tabel**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-135">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="6a6d2-136">Når du forlader dialogboksen **Opret nyt felt**, kommer du tilbage til dialogboksen **Indsæt felter**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-136">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="6a6d2-137">Alle brugerdefinerede felter, der lige er tilføjet, bliver automatisk markeret på listen til at blive indsat i formularen.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-137">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="6a6d2-138">Klik på **Indsæt** for at indsætte de markerede felter i det valgte område i formularen.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-138">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="6a6d2-139">**Valgfrit:** Aktivér tilstanden **Flyt** fra værktøjslinjen til personlige indstillinger for at flytte de nye felter til den ønskede placering i det valgte område.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-139">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="6a6d2-140">Se [Tilpasse brugeroplevelsen](personalize-user-experience.md) for at få yderligere oplysninger om, hvordan du bruger de forskellige funktioner for tilpasning til at optimere en formular til din personlige brug.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-140">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="6a6d2-141">Dele brugerdefinerede felter med andre brugere</span><span class="sxs-lookup"><span data-stu-id="6a6d2-141">Sharing custom fields with other users</span></span>

<span data-ttu-id="6a6d2-142">Når du har oprettet et brugerdefineret felt og vist det i en formular, ønsker du muligvis at give denne opdaterede sidevisning, der indeholder det nye felt, til andre brugere i systemet.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-142">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="6a6d2-143">Dette kan gøres på to forskellige måder ved hjælp af funktionerne til brugertilpasning af produktet:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-143">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="6a6d2-144">Den anbefalede rute er via systemadministratoren, der kan overføre en tilpasning til alle brugere eller en undergruppe af brugere.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-144">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="6a6d2-145">Du kan finde flere oplysninger i [Tilpasse brugeroplevelsen](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="6a6d2-145">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="6a6d2-146">Du kan også eksportere dine ændringer (kaldet *tilpasninger*), og du sende dem til en eller flere brugere og få hver af disse brugere til at importere dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-146">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="6a6d2-147">Indstillingen **Administrer** på værktøjslinjen for personlige indstillinger giver dig mulighed for at eksportere og importere tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-147">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="6a6d2-148">Administration af brugerdefinerede felter</span><span class="sxs-lookup"><span data-stu-id="6a6d2-148">Managing custom fields</span></span>

<span data-ttu-id="6a6d2-149">Styring af de brugerdefinerede felter i systemet kan udføres ved hjælp af siden **Brugerdefinerede felter** i moudlet til systemadministration.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-149">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="6a6d2-150">Denne side giver brugere adgang til mange egenskaber, herunder:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-150">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="6a6d2-151">Få vist en liste over alle de brugerdefinerede felter i systemet.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-151">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="6a6d2-152">Begrænset redigering af eksisterende brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-152">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="6a6d2-153">Sletning af brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-153">Deleting custom fields.</span></span>
- <span data-ttu-id="6a6d2-154">Visning af brugerdefinerede felter på dataenheder.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-154">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="6a6d2-155">Angivelse af oversættelser af etiketter til brugerdefineret felt og hjælpetekst.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-155">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="6a6d2-156">Visning af alle brugerdefinerede felter</span><span class="sxs-lookup"><span data-stu-id="6a6d2-156">Viewing all custom fields</span></span>

<span data-ttu-id="6a6d2-157">Siden **Brugerdefinerede felter** giver oversigt over alle de brugerdefinerede felter, der er defineret i systemet.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-157">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="6a6d2-158">Du skal blot markere den tabel, du er interesseret i, og siden opdateres for at vise en liste over de brugerdefinerede felter, der er knyttet til den pågældende tabel.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-158">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="6a6d2-159">Når du vælger et brugerdefineret felt på listen, kan du få vist alle detaljer om feltet.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-159">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="6a6d2-160">Redigering af brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-160">Editing custom fields</span></span>

<span data-ttu-id="6a6d2-161">Når der er oprettet et brugerdefineret felt, er det kun visse dele af oplysningerne om det brugerdefinerede felt, der kan ændres på siden **Brugerdefinerede felter**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-161">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="6a6d2-162">Du *kan* ændre disse attributter:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-162">You *can* modify these attributes:</span></span>

- <span data-ttu-id="6a6d2-163">Label</span><span class="sxs-lookup"><span data-stu-id="6a6d2-163">Label</span></span>
- <span data-ttu-id="6a6d2-164">Hjælpetekst</span><span class="sxs-lookup"><span data-stu-id="6a6d2-164">Help text</span></span>
- <span data-ttu-id="6a6d2-165">Længde, for tekstfelter</span><span class="sxs-lookup"><span data-stu-id="6a6d2-165">Length, for Text fields</span></span>

<span data-ttu-id="6a6d2-166">Du *kan ikke* redigere følgende attributter:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-166">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="6a6d2-167">Feltnavn</span><span class="sxs-lookup"><span data-stu-id="6a6d2-167">Field name</span></span>
- <span data-ttu-id="6a6d2-168">Datatype</span><span class="sxs-lookup"><span data-stu-id="6a6d2-168">Data type</span></span>

<span data-ttu-id="6a6d2-169">For felter på valglister kan sættet af gyldige værdier for det brugerdefinerede felt derudover omarrangeres, og der kan tilføjes nye værdier, men eksisterende værdier for feltet på valglisten kan ikke fjernes.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-169">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="6a6d2-170">Husk at klikke på **Anvend ændringer**, når du er færdig med at redigere felter for en bestemt tabel, så ændringerne gemmes.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-170">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="6a6d2-171">Visning af brugerdefinerede felter på dataenheder</span><span class="sxs-lookup"><span data-stu-id="6a6d2-171">Exposing custom fields on data entities</span></span>

<span data-ttu-id="6a6d2-172">Det kan også være vigtigt at tillade brugerdefinerede felter at være synlige på dataenheder.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-172">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="6a6d2-173">Dataenheder bruges i funktionen [Oversigt over integration af Office](../../dev-itpro/office-integration/office-integration.md), samt hvad angår scenarier til import og eksport af data.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-173">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="6a6d2-174">Følg disse trin for at få vist et brugerdefineret felt i en dataenhed:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-174">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="6a6d2-175">Vælg det brugerdefinerede felt på formularen **Brugerdefinerede felter**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-175">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="6a6d2-176">Udvid afsnittet **Enheder** afsnit for at få vist sættet af relevante enheder.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-176">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="6a6d2-177">Klik på knappen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-177">Click the **Edit** button.</span></span>
4. <span data-ttu-id="6a6d2-178">Rediger feltet **Aktiveret** til at være markeret for hver enhed, der skal vise dette felt.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-178">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="6a6d2-179">Klik på **Anvend ændringer** for at gemme dine valg.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-179">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="6a6d2-180">Tillad, at brugerdefinerede felter vises på andre sprog</span><span class="sxs-lookup"><span data-stu-id="6a6d2-180">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="6a6d2-181">Det der kan være behov for adgang til brugerdefinerede felter på forskellige sprog, indeholder siden **Brugerdefinerede felter** en mekanisme, så etiketten og hjælpeteksten til et brugerdefineret felt kan oversættes til andre sprog.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-181">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="6a6d2-182">De følgende trin beskriver processen til oversættelse af brugerdefinerede felter til andre sprog:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-182">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="6a6d2-183">Vælg det brugerdefinerede felt på siden **Brugerdefinerede felter**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-183">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="6a6d2-184">Vælg knappen **Oversættelser** i bunden af handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-184">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="6a6d2-185">Der åbnes en rullemenu med eksisterende oversættelser til dette felt.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-185">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="6a6d2-186">Rullemenuen **Sprog** viser det sæt af sprog, hvor der allerede er angivet oversættelser.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-186">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="6a6d2-187">Hvis du vil redigere en eksisterende oversættelse, skal du vælge det ønskede sprog i menuen og ændre værdierne for etiketten og hjælpeteksten.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-187">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="6a6d2-188">Ellers skal du klikke på knappen **Tilføj sprog**, vælge det ønskede sprog i menuen og derefter angive oversatte værdier for etiketten og hjælpeteksten.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-188">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="6a6d2-189">Klik på **OK**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-189">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="6a6d2-190">Sletning af brugerdefinerede felter</span><span class="sxs-lookup"><span data-stu-id="6a6d2-190">Deleting custom fields</span></span>

<span data-ttu-id="6a6d2-191">I sjældne tilfælde kan du beslutte, at et brugerdefineret felt ikke længere er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-191">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="6a6d2-192">Når dette sker kan en systemadministrator vælge at slette feltet fra siden **Brugerdefinerede felter**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-192">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="6a6d2-193">Det gør du ved at sikre, at det rette felt er markeret, klikke på **Slet**, klikke på **Ja** for at bekræfte sletningen og derefter klikke på **Anvend ændringer**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-193">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="6a6d2-194">Denne handling kan ikke fortrydes, og det vil resultere i, at de data, der er knyttet til feltet, slettes permanent fra databasen.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-194">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="6a6d2-195">Appendiks</span><span class="sxs-lookup"><span data-stu-id="6a6d2-195">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="6a6d2-196">Hvem kan oprette brugerdefinerede felter?</span><span class="sxs-lookup"><span data-stu-id="6a6d2-196">Who can create custom fields?</span></span>

<span data-ttu-id="6a6d2-197">Som en sikring af systemet er det kun systemadministratorer, der som standard kan oprette brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-197">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="6a6d2-198">Men de superbrugere, som organisationen finder det nødvendigt, kan gives rettigheder af en systemadministrator til at oprette brugerdefinerede felter ved hjælp af sikkerhedsrollen **Superbruger for tilpasning på kørselstidpunkt**.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-198">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="6a6d2-199">Brugere uden denne sikkerhedsrolle vil ikke kunne oprette brugerdefinerede felter, men de vil stadig kunne se og anvende brugerdefinerede felter, der er tilføjet af andre brugere i systemet.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-199">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="6a6d2-200">Hvilke tabeller understøtte brugerdefinerede felter?</span><span class="sxs-lookup"><span data-stu-id="6a6d2-200">What tables support custom fields?</span></span>

<span data-ttu-id="6a6d2-201">Af ydelsesmæssige og tekniske årsager tillader kun tabeller, der opfylder følgende betingelser, i øjeblikket, at brugerdefinerede felter tilføjes.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-201">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="6a6d2-202">Tabellen skal mærkes som en af disse grupper:</span><span class="sxs-lookup"><span data-stu-id="6a6d2-202">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="6a6d2-203">Multi</span><span class="sxs-lookup"><span data-stu-id="6a6d2-203">Group</span></span>
    - <span data-ttu-id="6a6d2-204">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="6a6d2-204">WorksheetHeader</span></span>
    - <span data-ttu-id="6a6d2-205">Hoved</span><span class="sxs-lookup"><span data-stu-id="6a6d2-205">Main</span></span>
    - <span data-ttu-id="6a6d2-206">Diverse</span><span class="sxs-lookup"><span data-stu-id="6a6d2-206">Miscellaneous</span></span>
    - <span data-ttu-id="6a6d2-207">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a6d2-207">Parameter</span></span>
    - <span data-ttu-id="6a6d2-208">Reference</span><span class="sxs-lookup"><span data-stu-id="6a6d2-208">Reference</span></span>
    - <span data-ttu-id="6a6d2-209">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="6a6d2-209">TransactionHeader</span></span>

- <span data-ttu-id="6a6d2-210">Tabellen kan ikke udvide en anden tabel.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-210">The table cannot extend another table.</span></span>
- <span data-ttu-id="6a6d2-211">Tabellen kan ikke markeres som en systemtabel.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-211">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="6a6d2-212">Tabellen må ikke være en midlertidig tabel.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-212">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="6a6d2-213">Kan jeg henvise til brugerdefinerede felter fra udviklingsværktøjerne?</span><span class="sxs-lookup"><span data-stu-id="6a6d2-213">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="6a6d2-214">Brugerdefinerede felter kan kun administreres via brugergrænsefladen, og der kan ikke henvises til dem ved hjælp af en kode.</span><span class="sxs-lookup"><span data-stu-id="6a6d2-214">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 
