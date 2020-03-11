---
title: Implementere brugerdefinerede felter for Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android
description: Dette emne indeholder almindelige mønstre til brug af udvidelser i forbindelse med implementering af brugerdefinerede felter.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 48854c15e429d51dcf30ea804eb636dee7965443
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080766"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="00f8a-103">Implementere brugerdefinerede felter for Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android</span><span class="sxs-lookup"><span data-stu-id="00f8a-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00f8a-104">Dette emne indeholder almindelige mønstre til brug af udvidelser i forbindelse med implementering af brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="00f8a-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="00f8a-105">Følgende emner behandles:</span><span class="sxs-lookup"><span data-stu-id="00f8a-105">The following topics are covered:</span></span>

- <span data-ttu-id="00f8a-106">De forskellige datatyper, som den brugerdefinerede feltstruktur understøtter</span><span class="sxs-lookup"><span data-stu-id="00f8a-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="00f8a-107">Sådan får du vist skrivebeskyttede eller redigerbare felter på timeseddelposter og gemmer brugerleverede værdier i databasen igen</span><span class="sxs-lookup"><span data-stu-id="00f8a-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="00f8a-108">Sådan får du vist skrivebeskyttede felter i timeseddelhovedet</span><span class="sxs-lookup"><span data-stu-id="00f8a-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="00f8a-109">Sådan integrerer du anden brugerdefineret forretningslogik for at angive standardværdier i felter og foretage yderligere validering</span><span class="sxs-lookup"><span data-stu-id="00f8a-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="00f8a-110">Målgruppe</span><span class="sxs-lookup"><span data-stu-id="00f8a-110">Audience</span></span>

<span data-ttu-id="00f8a-111">Dette emne er henvendt til udviklere, der integrerer deres brugerdefinerede felter i det Microsoft Dynamics 365 Project Timesheet-mobilprogram, der er tilgængeligt for Apple IOS Android og Google.</span><span class="sxs-lookup"><span data-stu-id="00f8a-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="00f8a-112">Forudsætningen er, at læserne kender til X++-udviklings- og projekttimeseddelfunktionerne.</span><span class="sxs-lookup"><span data-stu-id="00f8a-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="00f8a-113">Datakontrakt – TSTimesheetCustomField X++-klasse</span><span class="sxs-lookup"><span data-stu-id="00f8a-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="00f8a-114">**TSTimesheetCustomField**-klassen er den X++-datakontraktklasse, der repræsenterer oplysninger om et brugerdefineret felt til timeseddelfunktionaliteten.</span><span class="sxs-lookup"><span data-stu-id="00f8a-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="00f8a-115">Lister over brugerdefinerede feltobjekter overføres både til TSTimesheetDetails-datakontrakten og TSTimesheetEntry-datakontrakten, så der kan vises brugerdefinerede felter i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="00f8a-116">**TSTimesheetDetails** - Timeseddel-hovedkontrakten.</span><span class="sxs-lookup"><span data-stu-id="00f8a-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="00f8a-117">**TSTimesheetEntry** - Timeseddel-transaktionskontrakten.</span><span class="sxs-lookup"><span data-stu-id="00f8a-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="00f8a-118">Grupper af disse objekter, der har samme projektoplysninger og **timesheetLineRecId**-værdi, udgør en linje.</span><span class="sxs-lookup"><span data-stu-id="00f8a-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="00f8a-119">fieldBaseType (typer)</span><span class="sxs-lookup"><span data-stu-id="00f8a-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="00f8a-120">Egenskaben **FieldBaseType** i objektet **TsTimesheetCustom** bestemmer, hvilken type felt der vises i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="00f8a-121">Følgende værdier for **Typer** understøttes.</span><span class="sxs-lookup"><span data-stu-id="00f8a-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="00f8a-122">Typeværdi</span><span class="sxs-lookup"><span data-stu-id="00f8a-122">Types value</span></span> | <span data-ttu-id="00f8a-123">Type</span><span class="sxs-lookup"><span data-stu-id="00f8a-123">Type</span></span>              | <span data-ttu-id="00f8a-124">Kommentarer</span><span class="sxs-lookup"><span data-stu-id="00f8a-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="00f8a-125">0</span><span class="sxs-lookup"><span data-stu-id="00f8a-125">0</span></span>           | <span data-ttu-id="00f8a-126">Streng (og fasttekst)</span><span class="sxs-lookup"><span data-stu-id="00f8a-126">String (and Enum)</span></span> | <span data-ttu-id="00f8a-127">Feltet vises som et tekstfelt.</span><span class="sxs-lookup"><span data-stu-id="00f8a-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="00f8a-128">1</span><span class="sxs-lookup"><span data-stu-id="00f8a-128">1</span></span>           | <span data-ttu-id="00f8a-129">Heltal</span><span class="sxs-lookup"><span data-stu-id="00f8a-129">Integer</span></span>           | <span data-ttu-id="00f8a-130">Værdien vises som et tal uden decimalpladser.</span><span class="sxs-lookup"><span data-stu-id="00f8a-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="00f8a-131">2</span><span class="sxs-lookup"><span data-stu-id="00f8a-131">2</span></span>           | <span data-ttu-id="00f8a-132">Kommatal</span><span class="sxs-lookup"><span data-stu-id="00f8a-132">Real</span></span>              | <span data-ttu-id="00f8a-133">Værdien vises som et tal, der har decimalpladser.</span><span class="sxs-lookup"><span data-stu-id="00f8a-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="00f8a-134">Hvis du vil vise kommatalsværdien som en valuta i appen, skal du bruge egenskaben **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="00f8a-135">Du kan bruge egenskaben **numberOfDecimals** til at angive antallet af decimaler, der skal vises.</span><span class="sxs-lookup"><span data-stu-id="00f8a-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="00f8a-136">3</span><span class="sxs-lookup"><span data-stu-id="00f8a-136">3</span></span>           | <span data-ttu-id="00f8a-137">Dato</span><span class="sxs-lookup"><span data-stu-id="00f8a-137">Date</span></span>              | <span data-ttu-id="00f8a-138">Datoformater bestemmes af brugerens indstilling for **Format for dato, klokkeslæt og tal**, der er angivet under **Præferencer af sprog og land/område** i **Brugerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="00f8a-139">4</span><span class="sxs-lookup"><span data-stu-id="00f8a-139">4</span></span>           | <span data-ttu-id="00f8a-140">Boolesk</span><span class="sxs-lookup"><span data-stu-id="00f8a-140">Boolean</span></span>           | |
| <span data-ttu-id="00f8a-141">15</span><span class="sxs-lookup"><span data-stu-id="00f8a-141">15</span></span>          | <span data-ttu-id="00f8a-142">GUID</span><span class="sxs-lookup"><span data-stu-id="00f8a-142">GUID</span></span>              | |
| <span data-ttu-id="00f8a-143">16</span><span class="sxs-lookup"><span data-stu-id="00f8a-143">16</span></span>          | <span data-ttu-id="00f8a-144">Int64</span><span class="sxs-lookup"><span data-stu-id="00f8a-144">Int64</span></span>             | |

- <span data-ttu-id="00f8a-145">Hvis egenskaben **stringOptions** ikke findes i objektet **TSTimesheetCustomField**, vises der et fritekstfelt for brugeren.</span><span class="sxs-lookup"><span data-stu-id="00f8a-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="00f8a-146">Egenskaben **stringLength** kan bruges til at angive den maksimale strenglængde, som brugerne kan angive.</span><span class="sxs-lookup"><span data-stu-id="00f8a-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="00f8a-147">Hvis egenskaben **stringOptions** findes i objektet **TSTimesheetCustomField**, er listeelementerne de eneste værdier, som brugerne kan vælge ved hjælp af alternativknapper.</span><span class="sxs-lookup"><span data-stu-id="00f8a-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="00f8a-148">I dette tilfælde kan strengfeltet fungere som en fasttekstværdi med henblik på brugerindtastning.</span><span class="sxs-lookup"><span data-stu-id="00f8a-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="00f8a-149">Hvis du vil gemme værdien i databasen som en fasttekst, skal du manuelt knytte strengværdien til fasttekstværdien igen, før du gemmer den i databasen, ved hjælp af kommandokæden (se eksemplet i afsnittet "Bruge kommandokæde på klassen TSTimesheetEntryService for at gemme en timeseddelpost fra appen i databasen igen" senere i dette emne).</span><span class="sxs-lookup"><span data-stu-id="00f8a-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="00f8a-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="00f8a-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="00f8a-151">Du kan bruge denne egenskab til at formatere kommatalsværdier som valuta.</span><span class="sxs-lookup"><span data-stu-id="00f8a-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="00f8a-152">Denne fremgangsmåde kan kun anvendes, hvis **fieldBaseType**-værdien er **Kommatal**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="00f8a-153">**TSCustomFieldExtendedType:None** – Der anvendes ingen formatering.</span><span class="sxs-lookup"><span data-stu-id="00f8a-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="00f8a-154">**TSCustomFieldExtendedType::Currency** – Formatér værdien som valuta.</span><span class="sxs-lookup"><span data-stu-id="00f8a-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="00f8a-155">Når valutaformatering er aktiv, kan feltet **stringValue** bruges til at overføre den valutakode, der skal vises i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="00f8a-156">Værdien er en skrivebeskyttet værdi.</span><span class="sxs-lookup"><span data-stu-id="00f8a-156">The value is a read-only value.</span></span>

    <span data-ttu-id="00f8a-157">Feltet **realValue** indeholder det pengebeløb, der skal gemmes i databasen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="00f8a-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="00f8a-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="00f8a-159">Du kan bruge denne egenskab til at angive, hvor det brugerdefinerede felt skal vises i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="00f8a-160">**TSCustomFieldSection::Header** – Feltet vises i sektionen **Vis flere oplysninger** i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="00f8a-161">Disse felter er altid skrivebeskyttede.</span><span class="sxs-lookup"><span data-stu-id="00f8a-161">These fields are always read-only.</span></span>
- <span data-ttu-id="00f8a-162">**TSCustomFieldSection::Line** – Feltet vises efter alle felter med out-of-box-linjer på timeseddelposter.</span><span class="sxs-lookup"><span data-stu-id="00f8a-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="00f8a-163">Disse felter kan enten redigeres eller skrivebeskyttes.</span><span class="sxs-lookup"><span data-stu-id="00f8a-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="00f8a-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="00f8a-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="00f8a-165">Denne egenskab identificerer feltet, når de værdier, som appen angiver, gemmes i databasen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="00f8a-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="00f8a-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="00f8a-167">Denne egenskab identificerer feltet, når de værdier, som appen angiver, gemmes i databasen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="00f8a-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="00f8a-168">isEditable (NoYes)</span></span>

<span data-ttu-id="00f8a-169">Indstil denne egenskab til **Ja** for at angive, at feltet i sektionen til timeseddelindtastningen skal kunne redigeres af brugerne.</span><span class="sxs-lookup"><span data-stu-id="00f8a-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="00f8a-170">Indstil egenskaben til **Nej** for at gøre feltet skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="00f8a-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="00f8a-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="00f8a-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="00f8a-172">Indstil denne egenskab til **Ja** for at angive, at feltet i sektionen til timeseddelindtastningen skal være obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="00f8a-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="00f8a-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="00f8a-173">label (str)</span></span>

<span data-ttu-id="00f8a-174">Denne egenskab specificerer den etiket, der vises ud for feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="00f8a-175">stringOptions (liste over strenge)</span><span class="sxs-lookup"><span data-stu-id="00f8a-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="00f8a-176">Denne egenskab kan kun anvendes, når **fieldBaseType** er indstillet til **Streng**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="00f8a-177">Hvis **stringOptions** er valgt, er de strengværdier, der kan vælges via alternativknapper, angivet af strengene på listen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="00f8a-178">Hvis der ikke er angivet nogen strenge, er fritekstindtastning i strengfeltet tilladt (se eksemplet i afsnittet "Bruge kommandokæden på klassen TSTimesheetEntryService for at gemme en timeseddelpost fra appen i databasen igen" senere i dette emne).</span><span class="sxs-lookup"><span data-stu-id="00f8a-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="00f8a-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="00f8a-179">stringLength (int)</span></span>

<span data-ttu-id="00f8a-180">Denne egenskab specificerer den maksimale længde for et strengfelt.</span><span class="sxs-lookup"><span data-stu-id="00f8a-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="00f8a-181">Den kan kun anvendes, når **fieldBaseType** er indstillet til **Streng**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="00f8a-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="00f8a-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="00f8a-183">Denne egenskab specificerer det antal decimalpladser, der vises for et kommatalsfelt.</span><span class="sxs-lookup"><span data-stu-id="00f8a-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="00f8a-184">Den kan kun anvendes, når **fieldBaseType** er indstillet til **Kommatal**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="00f8a-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="00f8a-185">orderSequence (int)</span></span>

<span data-ttu-id="00f8a-186">Denne egenskab styrer den rækkefølge, som de brugerdefinerede felter i appen vises i, når der er angivet mere end ét brugerdefineret felt.</span><span class="sxs-lookup"><span data-stu-id="00f8a-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="00f8a-187">Felterne med de laveste numre vises først.</span><span class="sxs-lookup"><span data-stu-id="00f8a-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="00f8a-188">booleanValue (boolesk)</span><span class="sxs-lookup"><span data-stu-id="00f8a-188">booleanValue (boolean)</span></span>

<span data-ttu-id="00f8a-189">For felter af typen **Boolesk** overfører denne egenskab den booleske værdi for feltet mellem serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="00f8a-190">guidValue (GUID)</span><span class="sxs-lookup"><span data-stu-id="00f8a-190">guidValue (guid)</span></span>

<span data-ttu-id="00f8a-191">For felter af typen **GUID** overfører denne egenskab GUID-værdien (globally unique identifier) for feltet mellem serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="00f8a-192">int64Value (Int64)</span><span class="sxs-lookup"><span data-stu-id="00f8a-192">int64Value (int64)</span></span>

<span data-ttu-id="00f8a-193">For felter af typen **Int64** overfører denne egenskab int64-værdien for feltet mellem serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="00f8a-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="00f8a-194">intValue (int)</span></span>

<span data-ttu-id="00f8a-195">For felter af typen **Int** overfører denne egenskab int-værdien for feltet mellem serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="00f8a-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="00f8a-196">realValue (real)</span></span>

<span data-ttu-id="00f8a-197">For felter af typen **Kommatal** overfører denne egenskab kommatalsværdien for feltet mellem serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="00f8a-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="00f8a-198">stringValue (str)</span></span>

<span data-ttu-id="00f8a-199">For felter af typen **Streng** overfører denne egenskab strengværdien for feltet mellem serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="00f8a-200">Den bruges også til felter af typen **Kommatal**, der er formateret som valuta.</span><span class="sxs-lookup"><span data-stu-id="00f8a-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="00f8a-201">For disse felter bruges egenskaben til at overføre valutakoden til appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="00f8a-202">dateValue (dato)</span><span class="sxs-lookup"><span data-stu-id="00f8a-202">dateValue (date)</span></span>

<span data-ttu-id="00f8a-203">For felter af typen **Date** overfører denne egenskab datoværdien for feltet mellem serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="00f8a-204">Vise og gemme et brugerdefineret felt i sektionen til timeseddelindtastning</span><span class="sxs-lookup"><span data-stu-id="00f8a-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="00f8a-205">Nedenfor vises et skærmbillede fra mobilappen af oprettelse af en timeseddelpost.</span><span class="sxs-lookup"><span data-stu-id="00f8a-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="00f8a-206">Den viser de indbyggede felter og et brugerdefineret felt i afsnittet "Tidsregistrering", der kaldes "Teststreng" med fasttekstværdien "Anden indstilling".</span><span class="sxs-lookup"><span data-stu-id="00f8a-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Brugerdefineret felt til teststreng i appen](media/timesheet-entry.jpg)



<span data-ttu-id="00f8a-208">Nedenfor vises et skærmbillede fra mobilappen af brugeren, der vælger en af de fasttekstindstillinger, der er tilgængelige for det brugerdefinerede felt "Teststreng".</span><span class="sxs-lookup"><span data-stu-id="00f8a-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="00f8a-209">De to indstillinger er "Første indstilling" og "Anden indstilling" vist som alternativknapper.</span><span class="sxs-lookup"><span data-stu-id="00f8a-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="00f8a-210">Den anden indstilling er aktuelt markeret.</span><span class="sxs-lookup"><span data-stu-id="00f8a-210">The second option is currently selected.</span></span>

![Alternativknapper til det brugerdefinerede felt Teststreng](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="00f8a-212">Udvide tabellen TSTimesheetLine, så den har et brugerdefineret felt</span><span class="sxs-lookup"><span data-stu-id="00f8a-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="00f8a-213">I typiske scenarier er det sandsynligt, at dataene til et brugerdefineret felt i sektionen til timeseddelindtastning gemmes i tabellen TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="00f8a-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="00f8a-214">Der kan dog bruges andre tabeller, hvis dataene kan hentes på basis af en TSTimesheetTrans-post, der er angivet, eller hvis der ikke er angivet en bestemt postkontekst (hvis feltet f.eks. er skrivebeskyttet i projektparametrene).</span><span class="sxs-lookup"><span data-stu-id="00f8a-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="00f8a-215">Bemærk, at brugerdefinerede felter ikke behøver at have nogen understøttende databaseposter.</span><span class="sxs-lookup"><span data-stu-id="00f8a-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="00f8a-216">De kan genereres dynamisk på basis af X++-logik.</span><span class="sxs-lookup"><span data-stu-id="00f8a-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="00f8a-217">Denne fremgangsmåde kan være nyttig i skrivebeskyttede scenarier (se afsnittet "Bruge kommandokæde på klassen TSTimesheetDetails, buildCustomFieldListForHeader-metoden til at angive timeseddeloplysninger" for at få et eksempel på dynamisk genererede brugerdefinerede feltværdier).</span><span class="sxs-lookup"><span data-stu-id="00f8a-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="00f8a-218">Nedenfor vises et skærmbillede fra Visual Studio af applikationsobjekttræet.</span><span class="sxs-lookup"><span data-stu-id="00f8a-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="00f8a-219">Billedet viser en udvidelse af tabellen TSTimesheetLine, hvor TestLineString-feltet er tilføjet som et brugerdefineret felt.</span><span class="sxs-lookup"><span data-stu-id="00f8a-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Linjestreng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="00f8a-221">Bruge kommandokæde på metoden buildCustomFieldList i klassen TSTimesheetSettings til at få vist et felt i sektionen timeseddelpost</span><span class="sxs-lookup"><span data-stu-id="00f8a-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="00f8a-222">Denne kode bestemmer visningsindstillingerne for feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="00f8a-223">Den styrer f.eks. feltets type, etiketten, om feltet er obligatorisk, og hvilken sektion feltet vises i.</span><span class="sxs-lookup"><span data-stu-id="00f8a-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="00f8a-224">I følgende eksempel vises et strengfelt til tidsposter.</span><span class="sxs-lookup"><span data-stu-id="00f8a-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="00f8a-225">Dette felt indeholder to indstillinger, **Første indstilling** og **Anden indstilling**, der er tilgængelige via alternativknapper.</span><span class="sxs-lookup"><span data-stu-id="00f8a-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="00f8a-226">Feltet i appen er knyttet til feltet **TestLineString**, som føjes til tabellen TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="00f8a-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="00f8a-227">Bemærk brugen af metoden **TSTimesheetCustomField::newFromMetatdata ()**, der kan forenkle initialiseringen af egenskaberne for det brugerdefinerede felt: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** og **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="00f8a-228">Du kan også angive disse parametre manuelt, som du foretrækker.</span><span class="sxs-lookup"><span data-stu-id="00f8a-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="00f8a-229">Bruge kommandokæde på metoden buildCustomFieldListForEntry i klassen TSTimesheetEntry til at angive værdier i en timeseddelpost</span><span class="sxs-lookup"><span data-stu-id="00f8a-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="00f8a-230">Metoden **buildCustomFieldListForEntry** bruges til at angive værdier på de gemte timeseddellinjer i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="00f8a-231">Det kræver en TSTimesheetTrans-post som parameter.</span><span class="sxs-lookup"><span data-stu-id="00f8a-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="00f8a-232">Felter fra den pågældende post kan bruges til at udfylde den brugerdefinerede feltværdi i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="00f8a-233">Bruge kommandokæde på klassen TSTimesheetEntryService for at gemme en timeseddelpost fra appen i databasen igen</span><span class="sxs-lookup"><span data-stu-id="00f8a-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="00f8a-234">Hvis du vil gemme et brugerdefineret felt i databasen igen ved normal brug, skal du udvide flere metoder:</span><span class="sxs-lookup"><span data-stu-id="00f8a-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="00f8a-235">Metoden **timesheetLineNeedsUpdating** bruges til at bestemme, om linjeposten er ændret af brugeren i appen, og om den skal gemmes i databasen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="00f8a-236">Hvis ydeevnen ikke er noget problem, kan denne metode forenkles, så den altid returnerer **sand**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="00f8a-237">Metoderne **populateTimesheetLineFromEntryDuringCreate** og **populateTimesheetLineFromEntryDuringUpdate** kan udvides, så de angiver værdier i TSTimesheetLine-databaseposten fra den leverede TSTimesheetEntry-datakontraktpost.</span><span class="sxs-lookup"><span data-stu-id="00f8a-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="00f8a-238">I eksemplet nedenfor skal du lægge mærke til, hvordan tilknytningen mellem databasefeltet og indtastningsfeltet udføres manuelt via X++-kode.</span><span class="sxs-lookup"><span data-stu-id="00f8a-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="00f8a-239">Metoden **populateTimesheetWeekFromEntry** kan også udvides, hvis det brugerdefinerede felt, der er knyttet til **TSTimesheetEntry**-objektet, skal skrive tilbage til TSTimesheetLineweek-databasetabellen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="00f8a-240">I følgende eksempel gemmes den **firstOption**- eller **secondOption**-værdi, som brugeren vælger til databasen, som en rå strengværdi.</span><span class="sxs-lookup"><span data-stu-id="00f8a-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="00f8a-241">Hvis databasefeltet er et felt af typen **Fasttekst**, kan disse værdier knyttes manuelt til en fasttekstværdi og derefter gemmes i et fasttekstfelt i databasetabellen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="00f8a-242">Vise et brugerdefineret felt i hovedsektionen på timeseddel</span><span class="sxs-lookup"><span data-stu-id="00f8a-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="00f8a-243">Nedenfor vises et skærmbillede fra mobilappen af en bruger, der ser på en timeseddel.</span><span class="sxs-lookup"><span data-stu-id="00f8a-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="00f8a-244">Knappen "Flere oplysninger" er valgt i øverste højre hjørne for at vise indstillingen "Vis flere oplysninger".</span><span class="sxs-lookup"><span data-stu-id="00f8a-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Kommandoen Vis flere oplysninger](media/show-more.png)

<span data-ttu-id="00f8a-246">Nedenfor vises et skærmbillede fra mobilappen, der viser sektionen "Flere" på en timeseddel.</span><span class="sxs-lookup"><span data-stu-id="00f8a-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="00f8a-247">Der er føjet et brugerdefineret felt med navnet "Udnyttelsesgraden for denne timeseddel (beregnet brugerdefineret felt)" til timesedlens hovedsektion.</span><span class="sxs-lookup"><span data-stu-id="00f8a-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="00f8a-248">Der er angivet en skrivebeskyttet værdi, "0.667", i det brugerdefinerede felt.</span><span class="sxs-lookup"><span data-stu-id="00f8a-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Sektionen Flere](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="00f8a-250">Udvide tabellen TSTimesheetTable, så den har et brugerdefineret felt</span><span class="sxs-lookup"><span data-stu-id="00f8a-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="00f8a-251">I typiske scenarier er det sandsynligt, at dataene til et brugerdefineret felt i hovedsektionen hentes fra tabellen TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="00f8a-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="00f8a-252">Der kan dog bruges andre tabeller, hvis dataene kan hentes på basis af en TSTimesheetTable-post, der er angivet, eller hvis der ikke er angivet en bestemt postkontekst (hvis feltet f.eks. er skrivebeskyttet i projektparametrene).</span><span class="sxs-lookup"><span data-stu-id="00f8a-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="00f8a-253">Bemærk, at brugerdefinerede felter ikke behøver at have nogen understøttende databaseposter.</span><span class="sxs-lookup"><span data-stu-id="00f8a-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="00f8a-254">De kan genereres dynamisk på basis af X++-logik.</span><span class="sxs-lookup"><span data-stu-id="00f8a-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="00f8a-255">I eksemplet nedenfor vises denne fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="00f8a-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="00f8a-256">Felter i hovedsektionen er altid skrivebeskyttede i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="00f8a-257">Bruge kommandokæde på metoden buildCustomFieldList i klassen TSTimesheetSettings til at få vist et felt i hovedsektionen</span><span class="sxs-lookup"><span data-stu-id="00f8a-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="00f8a-258">Denne kode bestemmer visningsindstillingerne for feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="00f8a-259">Den styrer f.eks. feltets type, etiketten, om feltet er obligatorisk, og hvilken sektion feltet vises i.</span><span class="sxs-lookup"><span data-stu-id="00f8a-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="00f8a-260">Følgende eksempel viser en beregnet værdi i hovedsektionen i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="00f8a-261">Bruge kommandokæde på metoden buildCustomFieldListForHeader i klassen TSTimesheetDetails til at angive oplysninger i en timeseddel</span><span class="sxs-lookup"><span data-stu-id="00f8a-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="00f8a-262">Metoden **buildCustomFieldListForHeader** bruges til at angive hovedoplysninger i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="00f8a-263">Det kræver en TSTimesheetTable-post som parameter.</span><span class="sxs-lookup"><span data-stu-id="00f8a-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="00f8a-264">Felter fra den pågældende post kan bruges til at udfylde den brugerdefinerede feltværdi i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="00f8a-265">I følgende eksempel læses der ikke værdier fra databasen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="00f8a-266">I stedet bruges X++-logik til at generere en beregnet værdi, der derefter vises i appen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="00f8a-267">Andre muligheder for konfigurerbarhed/udvidelsesmuligheder</span><span class="sxs-lookup"><span data-stu-id="00f8a-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="00f8a-268">Tilføje yderligere validering for appen</span><span class="sxs-lookup"><span data-stu-id="00f8a-268">Adding additional validation for the app</span></span>

<span data-ttu-id="00f8a-269">Eksisterende logik for timeseddelfunktionalitet på databaseniveau fungerer stadig som forventet.</span><span class="sxs-lookup"><span data-stu-id="00f8a-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="00f8a-270">Hvis du vil afbryde udførelsen af gemme- eller sendehandlinger og vise en bestemt fejlmeddelelse, kan du føje **udløs fejl("meddelelse til bruger")** til koden via en kommandokædeudvidelse.</span><span class="sxs-lookup"><span data-stu-id="00f8a-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="00f8a-271">Her er tre eksempler på nyttige udvidelsesmetoder:</span><span class="sxs-lookup"><span data-stu-id="00f8a-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="00f8a-272">Hvis **validateWrite** i tabellen TSTimesheetLine returnerer **falsk** under en lagringshandling for en timeseddellinje, vises der en fejlmeddelelse i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="00f8a-273">Hvis **validateSubmit** i tabellen TSTimesheetTable returnerer **falsk** under afsendelse af en timeseddel i appen, vises der en fejlmeddelelse for brugeren.</span><span class="sxs-lookup"><span data-stu-id="00f8a-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="00f8a-274">Logik, der udfylder felter (f.eks. **Linjeegenskab**) under **indsæt**-metoden i TSTimesheetLine-tabellen, kører stadig.</span><span class="sxs-lookup"><span data-stu-id="00f8a-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="00f8a-275">Skjule og markere out of box-felter som skrivebeskyttede via konfiguration</span><span class="sxs-lookup"><span data-stu-id="00f8a-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="00f8a-276">Fra projektparametrene kan du gøre out of box-felter skrivebeskyttede eller skjulte i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="00f8a-277">Angiv indstillingerne i sektionen **Mobile timesedler** under fanen **Timeseddel** på siden **Parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projektparametre](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="00f8a-279">Ændre de aktiviteter, der er tilgængelige for valg via udvidelser</span><span class="sxs-lookup"><span data-stu-id="00f8a-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="00f8a-280">De aktiviteter, der er tilgængelige for valg til et projekt, udfyldes via metoderne **getActivitiesForProject()** og **getActivityQuery()** i klassen **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="00f8a-281">Du kan bruge kommandokæden til at ændre denne funktionalitet, så den svarer til firmascenariet for de aktiviteter, der er tilgængelige for valg til et bestemt projekt.</span><span class="sxs-lookup"><span data-stu-id="00f8a-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="00f8a-282">Angive en standardprojektkategori på timeseddelposter</span><span class="sxs-lookup"><span data-stu-id="00f8a-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="00f8a-283">Indtastning af en standardprojektkategori på timeseddelposter sker på tre niveauer.</span><span class="sxs-lookup"><span data-stu-id="00f8a-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="00f8a-284">Du kan bruge kommandokæden til at udvide funktionaliteten på et eller flere af disse niveauer for at opnå den ønskede funktionsmåde.</span><span class="sxs-lookup"><span data-stu-id="00f8a-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="00f8a-285">Følgende hierarki bruges:</span><span class="sxs-lookup"><span data-stu-id="00f8a-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="00f8a-286">Appen forsøger at placere standardkategorien fra projektressourcen.</span><span class="sxs-lookup"><span data-stu-id="00f8a-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="00f8a-287">Denne standardkategori er angivet i metoderne **getCurrentUserResource** og **getDelegatedResourcesForCurrentUser** i klassen **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="00f8a-288">Hvis standardkategorien ikke findes på projektressourceniveau, forsøger appen at trække den fra projektaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="00f8a-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="00f8a-289">Denne standardkategori indstilles i metoden **getActivitiesForProject** i klassen **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="00f8a-290">Hvis standardkategorien ikke findes på projektaktivitetsniveau, tages standardkategorien fra projektparametrene.</span><span class="sxs-lookup"><span data-stu-id="00f8a-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="00f8a-291">Denne standardkategori indstilles i metoden **getProjectDetailsbyRule** i klassen **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="00f8a-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
