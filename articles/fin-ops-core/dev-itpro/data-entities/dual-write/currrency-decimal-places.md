---
title: Migrering af valutadatatype til dobbeltskrivning
description: Dette emne indeholder en beskrivelse af, hvordan du kan ændre det antal decimaler, som dobbeltskrivning understøtter for valuta.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 889337560f073708fb16b2dc173f9872593dd570
ms.sourcegitcommit: be4fcf8f19c55e852a729b215a16e24e971ff5b7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456808"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="4c050-103">Migrering af valutadatatype til dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="4c050-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c050-104">Du kan øge antallet af decimaler, der understøttes for valutaværdier, til højst 10.</span><span class="sxs-lookup"><span data-stu-id="4c050-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="4c050-105">Standardgrænsen er fire decimaler.</span><span class="sxs-lookup"><span data-stu-id="4c050-105">The default limit is four decimal places.</span></span> <span data-ttu-id="4c050-106">Ved at øge antallet af decimaler undgår du datatab, når du bruger dobbeltskrivning til synkronisering af data.</span><span class="sxs-lookup"><span data-stu-id="4c050-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="4c050-107">Stigningen i antallet af decimaler er et tilvalg.</span><span class="sxs-lookup"><span data-stu-id="4c050-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="4c050-108">Hvis du vil implementere den, skal du bede Microsoft om hjælp.</span><span class="sxs-lookup"><span data-stu-id="4c050-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="4c050-109">Ændring af antallet af decimaler har to trin:</span><span class="sxs-lookup"><span data-stu-id="4c050-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="4c050-110">Anmod om migrering fra Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c050-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="4c050-111">Ret antallet af decimaler i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4c050-111">Change the number of decimal places in Common Data Service.</span></span>

<span data-ttu-id="4c050-112">Finance and Operations-appen og Common Data Service skal understøtte det samme antal decimaler i valutaværdier.</span><span class="sxs-lookup"><span data-stu-id="4c050-112">The Finance and Operations app and Common Data Service must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="4c050-113">Ellers kan der opstå datatab, når disse oplysninger synkroniseres mellem apps.</span><span class="sxs-lookup"><span data-stu-id="4c050-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="4c050-114">Migreringsprocessen konfigurerer den måde, værdierne for valuta og valutakurs gemmes på, men den ændrer ikke nogen data.</span><span class="sxs-lookup"><span data-stu-id="4c050-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="4c050-115">Når migreringen er fuldført, kan antallet af decimaler for valutakoder og prisfastsættelse øges, og de data, som brugerne indtaster og ser, kan have større decimalpræcision.</span><span class="sxs-lookup"><span data-stu-id="4c050-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="4c050-116">Migrering er valgfri.</span><span class="sxs-lookup"><span data-stu-id="4c050-116">Migration is optional.</span></span> <span data-ttu-id="4c050-117">Hvis du kan få fordel ved understøttelse af flere decimaler, anbefales du at overveje migrering.</span><span class="sxs-lookup"><span data-stu-id="4c050-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="4c050-118">Organisationer, der ikke har brug for værdier med mere end fire decimaler, behøver ikke at overføre data.</span><span class="sxs-lookup"><span data-stu-id="4c050-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="4c050-119">Anmodning om migrering fra Microsoft</span><span class="sxs-lookup"><span data-stu-id="4c050-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="4c050-120">Lager til eksisterende valutafelter i Common Data Service understøtter ikke mere end fire decimalpladser.</span><span class="sxs-lookup"><span data-stu-id="4c050-120">Storage for existing currency fields in Common Data Service can't support more than four decimal places.</span></span> <span data-ttu-id="4c050-121">Under migreringsprocessen kopieres valutaværdier derfor til nye interne felter i databasen.</span><span class="sxs-lookup"><span data-stu-id="4c050-121">Therefore, during the migration process, currency values are copied to new internal fields in the database.</span></span> <span data-ttu-id="4c050-122">Denne proces foregår løbende, indtil alle data er overført.</span><span class="sxs-lookup"><span data-stu-id="4c050-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="4c050-123">Internt i slutningen af migreringen erstatter de nye lagertyper de gamle lagertyper, men dataværdierne er uændrede.</span><span class="sxs-lookup"><span data-stu-id="4c050-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="4c050-124">Valutafelterne kan derefter understøtte op til ti decimaler.</span><span class="sxs-lookup"><span data-stu-id="4c050-124">The currency fields can then support up to 10 decimal places.</span></span> <span data-ttu-id="4c050-125">Under migreringsprocessen kan Common Data Service fortsat blive brugt uden afbrydelser.</span><span class="sxs-lookup"><span data-stu-id="4c050-125">During the migration process, Common Data Service can continue to be used without interruption.</span></span>

<span data-ttu-id="4c050-126">På samme tid ændres valutakurserne, så de understøtter op til 12 decimaler i stedet for den aktuelle grænse på 10.</span><span class="sxs-lookup"><span data-stu-id="4c050-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="4c050-127">Denne ændring er påkrævet, så antallet af decimaler er det samme i både Finance and Operations-appen og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4c050-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Common Data Service.</span></span>

<span data-ttu-id="4c050-128">Migrering ændrer ikke nogen data.</span><span class="sxs-lookup"><span data-stu-id="4c050-128">Migration doesn't change any data.</span></span> <span data-ttu-id="4c050-129">Når felterne for valuta og valutakurs konverteres, kan administratorer konfigurere systemet til at bruge op til ti decimaler for valutafelter ved at angive antallet af decimaler for hver transaktionsvaluta og for prisfastsættelse.</span><span class="sxs-lookup"><span data-stu-id="4c050-129">After the currency and exchange rate fields are converted, admins can configure the system to use up to 10 decimal places for currency fields by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="4c050-130">Anmode om en migrering</span><span class="sxs-lookup"><span data-stu-id="4c050-130">Request a migration</span></span>

<span data-ttu-id="4c050-131">Hvis du vil gøre denne funktion tilgængelig, skal du sende en mail til **CDSExpandDecimal@microsoft.com** og medtage følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="4c050-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="4c050-132">**Emne:** Anmodning om at aktivere udvidet decimalunderstøttelse for \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="4c050-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="4c050-133">**Brødtekst:** Jeg vil gerne aktivere udvidet decimalunderstøttelse for min organisation \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="4c050-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="4c050-134">En Microsoft-repræsentant vil kontakte dig inden for to til tre arbejdsdage angående de næste trin.</span><span class="sxs-lookup"><span data-stu-id="4c050-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="4c050-135">Når du anmoder om en migrering, skal du være opmærksom på følgende oplysninger og planlægge i overensstemmelse hermed:</span><span class="sxs-lookup"><span data-stu-id="4c050-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="4c050-136">Den tid, der kræves til at overføre dataene, afhænger af mængden af data i systemet.</span><span class="sxs-lookup"><span data-stu-id="4c050-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="4c050-137">Det kan tage flere dage at overføre store databaser.</span><span class="sxs-lookup"><span data-stu-id="4c050-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="4c050-138">Størrelsen på databasen øges midlertidigt, mens migreringen kører, fordi der skal bruges yderligere plads til indeks.</span><span class="sxs-lookup"><span data-stu-id="4c050-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="4c050-139">Det meste af den ekstra plads frigøres, når migreringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="4c050-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="4c050-140">Hvis der opstår fejl under migreringsprocessen, og det forhindrer, at migreringen fuldføres, udløser systemet beskeder til Microsoft Support, så supportpersonalet kan gribe ind.</span><span class="sxs-lookup"><span data-stu-id="4c050-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="4c050-141">Men selvom der opstår fejl under migreringen, forbliver Common Data Service fuldt tilgængeligt for almindelig brug.</span><span class="sxs-lookup"><span data-stu-id="4c050-141">However, even if errors occur during the migration, Common Data Service remains fully available for regular use.</span></span>
+ <span data-ttu-id="4c050-142">Migreringsprocessen kan ikke fortrydes.</span><span class="sxs-lookup"><span data-stu-id="4c050-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="4c050-143">Ændring af antal decimaler</span><span class="sxs-lookup"><span data-stu-id="4c050-143">Changing the number of decimal places</span></span>

<span data-ttu-id="4c050-144">Når migreringen er fuldført, kan Common Data Service gemme tal, der har flere decimaler.</span><span class="sxs-lookup"><span data-stu-id="4c050-144">After the migration is completed, Common Data Service can store numbers that have more decimal places.</span></span> <span data-ttu-id="4c050-145">Administratorer kan vælge, hvor mange decimaler der skal bruges til bestemte valutakoder og til prisfastsættelse.</span><span class="sxs-lookup"><span data-stu-id="4c050-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="4c050-146">Brugere af Microsoft Power Apps, Power BI og Power Automate kan derefter se og bruge tal, der har flere decimaler.</span><span class="sxs-lookup"><span data-stu-id="4c050-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="4c050-147">Hvis du vil foretage denne ændring, skal du opdatere følgende indstillinger i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="4c050-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="4c050-148">**Systemindstillinger: valutapræcision for prisfastsættelse** – Feltet **Vælg den valutapræcision, der bruges til prissætning i hele systemet** definerer, hvordan valutaen fungerer for organisationen, når **Prissætningsnøjagtighed** er valgt.</span><span class="sxs-lookup"><span data-stu-id="4c050-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** field defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="4c050-149">**Forretningsstyring: valutaer** – I feltet **Valutapræcision** kan du angive et brugerdefineret antal decimaler for en bestemt valuta.</span><span class="sxs-lookup"><span data-stu-id="4c050-149">**Business Management: Currencies** – The **Currency Precision** field lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="4c050-150">Der er reserve i indstillingen for hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="4c050-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="4c050-151">Der er nogle begrænsninger:</span><span class="sxs-lookup"><span data-stu-id="4c050-151">There are some limitations:</span></span>

+ <span data-ttu-id="4c050-152">Du kan ikke konfigurere valutafeltet for et objekt.</span><span class="sxs-lookup"><span data-stu-id="4c050-152">You can't configure the currency field on an entity.</span></span>
+ <span data-ttu-id="4c050-153">Du kan kun angive fire decimaler på niveauerne **Prisfastsættelse** og **Transaktionsvaluta**.</span><span class="sxs-lookup"><span data-stu-id="4c050-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="4c050-154">Systemindstillinger: valutapræcision for prisfastsættelse</span><span class="sxs-lookup"><span data-stu-id="4c050-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="4c050-155">Når migreringen er fuldført, kan administratorer angive valutapræcisionen.</span><span class="sxs-lookup"><span data-stu-id="4c050-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="4c050-156">Gå til **Indstillinger \> Administration**, og vælg **Systemindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="4c050-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="4c050-157">Under fanen **Generelt** skal du ændre værdien af feltet **Vælg den valutapræcision, der bruges til prissætning i hele systemet**, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="4c050-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** field, as shown in the following illustration.</span></span>

![Systemindstillinger for valuta](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="4c050-159">Forretningsstyring: valutaer</span><span class="sxs-lookup"><span data-stu-id="4c050-159">Business Management: Currencies</span></span>

<span data-ttu-id="4c050-160">Hvis du kræver, at valutapræcisionen for en bestemt valuta er forskellig fra den valutapræcision, der bruges til prisfastsættelsen, kan du ændre den.</span><span class="sxs-lookup"><span data-stu-id="4c050-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="4c050-161">Gå til **Indstillinger \> Forretningsstyring**, vælg **Valutaer**, og vælg den valuta, der skal ændres.</span><span class="sxs-lookup"><span data-stu-id="4c050-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="4c050-162">Angiv derefter feltet **Valutapræcision** til det antal decimaler, du ønsker, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="4c050-162">Then set the **Currency Precision** field to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Valutaindstillinger for en bestemt landestandard](media/specific-currency.png)

### <a name="entities-currency-field"></a><span data-ttu-id="4c050-164">Objekter: valutafelt</span><span class="sxs-lookup"><span data-stu-id="4c050-164">Entities: Currency field</span></span>

<span data-ttu-id="4c050-165">Det antal decimaler, der kan konfigureres for bestemte valutafelter, er begrænset til fire.</span><span class="sxs-lookup"><span data-stu-id="4c050-165">The number of decimal places that can be configured for specific currency fields is limited to four.</span></span>