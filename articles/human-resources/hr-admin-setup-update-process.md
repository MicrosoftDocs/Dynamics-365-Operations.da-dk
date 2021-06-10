---
title: Opdater proces
description: Microsoft Dynamics 365 Human Resources er en ægte Software som en service (SaaS), der tilbyder kontinuerlige serviceopdateringer til program- og platformændringer.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2466c53885340991aeeb0a07af83517473b332b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053629"
---
# <a name="update-process"></a><span data-ttu-id="f695c-103">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="f695c-103">Update process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f695c-104">Microsoft Dynamics 365 Human Resources er en ægte Software som en service (SaaS), der tilbyder kontinuerlige serviceopdateringer uden manuel indgriben.</span><span class="sxs-lookup"><span data-stu-id="f695c-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="f695c-105">Disse opdateringer indeholder både program- og platformsændringer, der ofte giver vigtige forbedringer af tjenesten, herunder lovpligtige opdateringer.</span><span class="sxs-lookup"><span data-stu-id="f695c-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="f695c-106">Opdateringspolitik</span><span class="sxs-lookup"><span data-stu-id="f695c-106">Update policy</span></span>

<span data-ttu-id="f695c-107">Opdateringer udgives regelmæssigt til alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="f695c-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="f695c-108">Human Resources understøttes i overensstemmelse med [Livscykluspolitik for Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), der giver leverer klare retningslinjer for tilgængeligheden af support.</span><span class="sxs-lookup"><span data-stu-id="f695c-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="f695c-109">Opdateringstakt af versioner</span><span class="sxs-lookup"><span data-stu-id="f695c-109">Release cadence</span></span> 

<span data-ttu-id="f695c-110">Human Resources-opdateringer anvendes automatisk til alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="f695c-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="f695c-111">Der frigives to typer versioner af Human Resources:</span><span class="sxs-lookup"><span data-stu-id="f695c-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="f695c-112">**Serviceopdateringer**: Opdateringer foretages hver anden uge og omfatter fejlrettelser og nye funktioner.</span><span class="sxs-lookup"><span data-stu-id="f695c-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="f695c-113">Serviceopdateringer omfatter også relevante platformsopdateringer, når de frigives.</span><span class="sxs-lookup"><span data-stu-id="f695c-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="f695c-114">Du kan få en ide om, hvornår der udgives opdateringer af platformen i [Tabel 3: Platformsversioner](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="f695c-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span></span> <span data-ttu-id="f695c-115">Opdateringer hver anden uge sker i en midlertidigt global udrulning på tværs af områder.</span><span class="sxs-lookup"><span data-stu-id="f695c-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="f695c-116">Du kan finde flere oplysninger om opdateringer hver anden uge i [Nyheder eller ændringer i Dynamics 365 Human Resources](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="f695c-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="f695c-117">Alle understøttede datacentre opdateres hver anden uge, medmindre andet er angivet.</span><span class="sxs-lookup"><span data-stu-id="f695c-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="f695c-118">Områderne USA, Australien, Europa, Storbritannien, Asien og Canada medtages i opdateringer hver anden uge.</span><span class="sxs-lookup"><span data-stu-id="f695c-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="f695c-119">**Dataverse-løsningsopdateringer**: Disse opdateringer forekommer ca. hver 6. uge efter behov.</span><span class="sxs-lookup"><span data-stu-id="f695c-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="f695c-120">De omfatter nye enheder og ændringer af eksisterende objekter i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f695c-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="f695c-121">Disse opdateringer frigives til samme regioner som de opdateringer hver anden uge, og de tager ca. seks uger at replikere gennem alle datacentre.</span><span class="sxs-lookup"><span data-stu-id="f695c-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="f695c-122">Løsningsopdateringer kan muligvis blive justeret efter serviceopdateringer hver anden uge.</span><span class="sxs-lookup"><span data-stu-id="f695c-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="f695c-123">Løsningsopdateringer er tilgængelige i alle datacentre, når de er frigivet.</span><span class="sxs-lookup"><span data-stu-id="f695c-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="f695c-124">Hvis du ikke vil vente på, at opdateringerne replikeres automatisk, kan du anvende disse opdateringer manuelt i alle miljøer i alle datacentre.</span><span class="sxs-lookup"><span data-stu-id="f695c-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="f695c-125">Når det er nødvendigt, leverer Human Resources også følgende typer rettelser:</span><span class="sxs-lookup"><span data-stu-id="f695c-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="f695c-126">**Revision (hotfix)**: Fejlrettelser, der kan forekomme sammen med eller separat i forhold til en serviceopdateringsversion hver anden uge</span><span class="sxs-lookup"><span data-stu-id="f695c-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="f695c-127">**Fejlrettelse i nødstilfælde**: Proaktive og reaktive hotfixes, der er uafhængige af hinanden, kan indeholde ændringer, der kun vedrører konfiguration eller kode til at løse problemer med aktive websteder og kan forekomme uafhængigt af en serviceopdateringsversion hver anden uge</span><span class="sxs-lookup"><span data-stu-id="f695c-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="f695c-128">Versioner gennemses, testes og valideres i et internt miljø.</span><span class="sxs-lookup"><span data-stu-id="f695c-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="f695c-129">Når builds er godkendt, kan de installeres.</span><span class="sxs-lookup"><span data-stu-id="f695c-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2021"></a><span data-ttu-id="f695c-130">Undtagelser til udgivelsestakten i 2021</span><span class="sxs-lookup"><span data-stu-id="f695c-130">Release cadence exceptions in 2021</span></span>

<span data-ttu-id="f695c-131">For at kunne tage højde for feriedage er frigivelsesplanen for november og december 2021 følgende.</span><span class="sxs-lookup"><span data-stu-id="f695c-131">To account for holidays, the release schedule for November and December 2021 is as follows:</span></span>

- <span data-ttu-id="f695c-132">Frigivelse i november: 1. november - 14. november</span><span class="sxs-lookup"><span data-stu-id="f695c-132">November release: November 1 - November 14</span></span>
- <span data-ttu-id="f695c-133">Frigivelse i december: 29. november - 12. december</span><span class="sxs-lookup"><span data-stu-id="f695c-133">December release: November 29 - December 12</span></span>
 
<span data-ttu-id="f695c-134">Den to-ugers frigivelsestakt vil fortsætte som sædvanligt den 10. januar 2022.</span><span class="sxs-lookup"><span data-stu-id="f695c-134">The two-week release cadence will resume as usual on January 10, 2022.</span></span>

## <a name="communications"></a><span data-ttu-id="f695c-135">Kommunikation</span><span class="sxs-lookup"><span data-stu-id="f695c-135">Communications</span></span>

<span data-ttu-id="f695c-136">Du kan finde ud af, hvad der planlægges for Human Resources, og hvad vi har udgivet på følgende placeringer:</span><span class="sxs-lookup"><span data-stu-id="f695c-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="f695c-137">Dynamics 365 Human Resources-oversigt</span><span class="sxs-lookup"><span data-stu-id="f695c-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="f695c-138">Dynamics 365-frigivelsesplaner</span><span class="sxs-lookup"><span data-stu-id="f695c-138">Dynamics 365 Release Plans</span></span>](/dynamics365/release-plans/)

- [<span data-ttu-id="f695c-139">Nyheder eller ændringer i Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f695c-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="f695c-140">[Problemsøgning i Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (kun for platformsrelaterede fejl)</span><span class="sxs-lookup"><span data-stu-id="f695c-140">[Issue search in Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="f695c-141">Human Resources-blog</span><span class="sxs-lookup"><span data-stu-id="f695c-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="f695c-142">Human Resources Yammer-fællesskab</span><span class="sxs-lookup"><span data-stu-id="f695c-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="f695c-143">Prøveversionsfunktioner i et sandkassemiljø</span><span class="sxs-lookup"><span data-stu-id="f695c-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="f695c-144">Du kan validere funktioner i prøveversioner i et sandkassemiljø, før du aktiverer dem i produktionsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="f695c-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="f695c-145">Du kan finde flere oplysninger om aktivering af nye funktioner under [Oversigt over funktionsstyring](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f695c-145">For more information about enabling features, see [Feature management overview](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="f695c-146">Alle nye funktioner vises i forhåndsvisning i mindst 30 dage og typisk 30-60 dage.</span><span class="sxs-lookup"><span data-stu-id="f695c-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="f695c-147">De vigtigste funktioner er normalt tilgængelige i oktober og april hvert år efter forhåndsvisningsperioden.</span><span class="sxs-lookup"><span data-stu-id="f695c-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="f695c-148">Så snart du ser nye egenskaber i arbejdsområdet Administration af funktioner, kan du slå dem til.</span><span class="sxs-lookup"><span data-stu-id="f695c-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="f695c-149">Nogle funktioner er muligvis som slået til som standard.</span><span class="sxs-lookup"><span data-stu-id="f695c-149">Some features may be on by default.</span></span>

<span data-ttu-id="f695c-150">På visse tidspunkter er en integreret funktion som standard slået til og kan ikke slås fra (f.eks. arbejdsområdet Administration af funktioner).</span><span class="sxs-lookup"><span data-stu-id="f695c-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="f695c-151">Når en funktion er generelt tilgængelig, kan den slås til eller fra i produktionsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="f695c-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="f695c-152">Arbejdsområdet Administration af funktioner angiver, hvornår en visningsfunktion skal være obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f695c-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="f695c-153">Denne dato er som regel den 1. oktober eller 1. april for at tilpasse det med de halvårlige frigivelsesplaner.</span><span class="sxs-lookup"><span data-stu-id="f695c-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="f695c-154">Du kan ikke slå de obligatoriske funktioner fra.</span><span class="sxs-lookup"><span data-stu-id="f695c-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="f695c-155">Indtil den bliver obligatorisk, kan du slå en funktion til og fra i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="f695c-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="f695c-156">Vi anbefaler, at du får vist funktioner i prøveversioner i et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="f695c-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="f695c-157">Det er bedst at oprette en kopi af dit aktuelle produktionsmiljø eller database i et sandkassemiljø, så du kan få den fulde erfaring med de nye funktioner sammen med dine data.</span><span class="sxs-lookup"><span data-stu-id="f695c-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="f695c-158">Yderligere oplysninger om klargøring af et sandkassemiljø finder du [Klargøre et Human Resources-projekt](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="f695c-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="f695c-159">Hvis du skal fjerne et testmiljø, kan du se [Fjerne en forekomst](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="f695c-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="f695c-160">Rapportere fejl</span><span class="sxs-lookup"><span data-stu-id="f695c-160">Report bugs</span></span>

<span data-ttu-id="f695c-161">Under test af funktioner i prøveversion eller afprøvning af nye funktioner, kan du finde elementer, der ikke fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="f695c-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="f695c-162">Rapporter eventuelle fejl via [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="f695c-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="f695c-163">Se også</span><span class="sxs-lookup"><span data-stu-id="f695c-163">See also</span></span>

[<span data-ttu-id="f695c-164">Dynamics 365 og Power Platform frigivelsesplaner</span><span class="sxs-lookup"><span data-stu-id="f695c-164">Dynamics 365 and Power Platform Release Plans</span></span>](/dynamics365/release-plans)</br>
[<span data-ttu-id="f695c-165">Nyheder eller ændringer i Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f695c-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="f695c-166">Livscykluspolitik for software</span><span class="sxs-lookup"><span data-stu-id="f695c-166">Software lifecycle policy</span></span>](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]