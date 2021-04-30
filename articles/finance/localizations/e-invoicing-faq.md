---
title: Ofte stillede spørgsmål om elektronisk fakturering
description: Dette emne indeholder oplysninger om ofte stillede spørgsmål om elektronisk fakturering.
author: gionoder
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1ba1a6c5542c10306d4b7494d33e7ff04504fa95
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893772"
---
# <a name="electronic-invoicing-faq"></a>Ofte stillede spørgsmål om elektronisk fakturering

[!include [banner](../includes/banner.md)]

Dette emne besvarer ofte stillede spørgsmål om elektronisk fakturering. Elektronisk fakturering udvider de funktioner for elektronisk fakturering, der findes i Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Project Operations. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Hvad er vigtigt ved elektronisk fakturering, og hvorfor skal det være en opgave for min organisation?

Driftsmæssig kompleksitet og risiko fortsætter med at stige globalt, mens organisationer vokser globalt og udvider deres fodaftryk på tværs af geografiske områder. Vedligeholdelse af overholdelse af angivne standarder og tilpasning til regler, der ofte ændres, er et stadigt stigende problem, og det er af særlig vigtighed, når der faktureres. Fakturering har traditionelt været dyrt og udsat for fejl, da firmaer er afhængige af papirdokumenter og manuelt intensive processer.  

Organisationer er begyndt at gå væk fra papirfakturaer for at reducere omkostningerne og gøre processen hurtigere. Offentlige myndigheder bruger i stigende grad elektronisk fakturering som en væsentlig del af skattedigitaliseringen. Ved at kræve, at organisationer sender skatteoplysninger digitalt til skattemyndighederne, kan myndighederne minimere skatteunddragelse og -manipulering og reducere snyd. 

Verden skifter til papirløs dokumentbehandling, og uden implementering af elektronisk fakturering kan kunder risikere at få problemer med overholdelse af angivne standarder, unødvendige omkostninger og komme bagud i forhold til konkurrenter. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Omfatter Finance, Supply Chain Management og Project Operations ikke allerede elektronisk fakturering? Hvilken værdi har dette for mig som kunde? 

Elektronisk fakturering udvider funktionerne til elektronisk fakturering, der findes i Finance, Supply Chain Management og Project Operations. Funktionaliteten forenkler også overholdelse af de nyeste standarder for elektronisk fakturering og giver en sammenhængende oplevelse i forskellige geografiske områder inden for elektronisk fakturabehandling og -udveksling. Funktionerne til elektronisk fakturering låser op for en vifte af fordele, herunder: 

   - Hurtigere og nemmere tilpasning til lande-/områdespecifikke krav.
   - Standardiserede implementeringer af en løsning til elektronisk fakturering. 
   - Forbedret sporing af e-fakturaer.  
   - Nemmere vedligeholdelse for at overholde ændringer i de lovgivningsmæssige krav og den lokale forretningspraksis. 
   - Forenklet pakkeløsning.
   - Skaleringsegenskaber for en stor mængde sendte dokumenter, der medfører hurtigere omsætning.
   - Mulighed for at dele dine løsninger med andre virksomheder.

## <a name="does-electronic-invoicing-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Understøtter elektronisk fakturering de lokale installationer af Finance, Supply Chain Management og Project Operations? 

Den aktuelle platform tillader ikke brugen af versionen i det lokale miljø, og der er ingen planer om at understøtte den i fremtiden.

## <a name="does-electronic-invoicing-interface-with-the-vendor-import-automation-feature"></a>Har elektronisk fakturering grænseflade med funktionen til automatisk kreditorimport?

Nej. Der er planer for denne grænseflade, men der er ingen planlagt tidslinje. Når det er planlagt, oplyses datoerne på forhånd i [Frigivelsesplaner](/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Hvordan håndterer elektronisk fakturering vedhæftede filer i den elektroniske faktura? Er der brug for en SharePoint-server, når der integreres PDF-filer i XML-filen?

De filer, der er tilknyttet den elektroniske faktura, håndteres som integrerede binære data i et XML-element. Der er ikke brug for en SharePoint-server for at integrere PDF-filer, men den vedhæftede fil skal gemmes i dokumentstyringssystemet i Finance, Supply Chain Management og Project Operations.

## <a name="is-electronic-invoicing-available-according-to-the-regulations-of-my-countryregion"></a>Er elektronisk fakturering tilgængelig i henhold til lovgivningen i mit land/område?

Elektronisk fakturering er en mikroserviceplatform, der vil være globalt tilgængelig.

Microsoft planlægger at publicere de elektroniske fakturaformater og integrationer for de lande og områder, der er funktionelt lokaliseret af Microsoft. Du kan finde flere oplysninger i [Tilgængelighed af funktioner til elektronisk fakturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Hvis det elektroniske faktureringsformat for dit land/område ikke er angivet, understøtter platformen dette scenario i fremtiden. Du kan stadig udnytte konfigurationsfunktionerne i elektronisk fakturering og selv konfigurere det elektroniske faktureringsformat, eller du kan samarbejde ammen med en partner/ISV om at konfigurere dem for din organisation.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Er Dynamics 365 til Regulatory Services et nyt modul som Human Resources eller Project Operations, der er knyttet til Finance eller Supply Chain Management? Er der ekstraomkostninger for det?

Dynamics 365 til Regulatory Services (RCS) er en cloudtjeneste til konfiguration af ressourcer til globalisering. RCS kan frit benyttes af alle licensindehavere til Finance, Supply Chain Management og Project Operations.

I forbindelse med tilmelding til RCS skal du gå til <https://marketing.configure.global.dynamics.com/>.

Du kan finde flere oplysninger i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing--or-just-turn-it-on-in-feature-management"></a>Skal jeg tilmelde mig for at få elektronisk fakturering eller blot aktivere den i Funktionsstyring?

Hvis du har en licens til Finance, Supply Chain Management og Project Operations, kan du se [Introduktion til tilføjelsesprogrammet til serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md) for at tilmelde dig elektronisk fakturering.

## <a name="does-electronic-invoicing-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Fungerer elektronisk fakturering med virtuelle maskiner på niveau 1? Hvad er det minimale påkrævede miljø?

Integration med elektronisk fakturering kræver mindst en virtuel maskine på niveau 2 som vært for Finance eller Supply Chain Management. Du kan finde flere oplysninger om miljøplanlægning under [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-have-a-test-mode-for-testing-invoice-submission"></a>Er der en testtilstand for elektronisk fakturering til test af fakturaafsendelse?

Dette kan opnås ved hjælp af konfigurationen. Hvis du vil teste afsendelsen af fakturaer, kan du oprette forbindelse til Finance eller Supply Chain Management fra et UAT-miljø (test af brugeraccept) og sende testfakturaerne. Elektronisk fakturering understøtter konfiguration af test til digitale certifikater, og hvis der er e-fakturaer, der kræver digital godkendelse, understøttes opsætningen af en URL-adresse fra testwebtjenester, der er udgivet af skattemyndighederne.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Findes der dokumentation for landespecifikke standardfunktioner til elektronisk fakturering?

Ja. Du kan finde oplysninger om tilgængeligheden af funktioner til elektronisk fakturering og de formater, de understøtter, under [Tilgængelighed af funktioner for elektronisk fakturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Hvis du ikke fandt det svar, du leder efter, kan du sende dit spørgsmål via mail til Product Development Team på <D365EInvoicePreview@microsoft.com>. Vi vil enten kontakte dig eller forbedre dækningen af denne side med Ofte stillede spørgsmål.