---
title: Ofte stillede spørgsmål om elektronisk fakturering
description: Denne artikel indeholder oplysninger om ofte stillede spørgsmål om elektronisk fakturering.
author: gionoder
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: fbb43438a9da567460eb744afb64dae5274f04a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904348"
---
# <a name="electronic-invoicing-faq"></a>Ofte stillede spørgsmål om elektronisk fakturering

[!include [banner](../includes/banner.md)]

Denne artikel besvarer ofte stillede spørgsmål om tjenesten Elektronisk fakturering. Elektronisk fakturering udvider de funktioner for elektronisk fakturering, der findes i Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Project Operations. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Hvad er vigtigt ved elektronisk fakturering, og hvorfor skal det være en opgave for min organisation?

Driftsmæssig kompleksitet og risiko fortsætter med at stige globalt, mens organisationer vokser globalt og udvider deres fodaftryk på tværs af geografiske områder. Vedligeholdelse af overholdelse af angivne standarder og tilpasning til regler, der ofte ændres, er et stadigt stigende problem, og det er af særlig vigtighed, når der faktureres. Fakturering har traditionelt været dyrt og udsat for fejl, da firmaer er afhængige af papirdokumenter og manuelt intensive processer.  

Organisationer er begyndt at gå væk fra papirfakturaer for at reducere omkostningerne og gøre processen hurtigere. Offentlige myndigheder bruger i stigende grad elektronisk fakturering som en væsentlig del af skattedigitaliseringen. Ved at kræve, at organisationer sender skatteoplysninger digitalt til skattemyndighederne, kan myndighederne minimere skatteunddragelse og -manipulering og reducere snyd. 

Verden skifter til papirløs dokumentbehandling, og uden implementering af elektronisk fakturering kan kunder risikere at få problemer med overholdelse af angivne standarder, unødvendige omkostninger og komme bagud i forhold til konkurrenter. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Omfatter Finance, Supply Chain Management og Project Operations ikke allerede elektronisk fakturering? Hvilken værdi har dette for mig som kunde? 

Elektronisk fakturering udvider de funktioner til elektronisk fakturering, der findes i Finance, Supply Chain Management og Project Operations. Funktionaliteten forenkler også overholdelse af de nyeste standarder for elektronisk fakturering og giver en sammenhængende oplevelse i forskellige geografiske områder inden for elektronisk fakturabehandling og -udveksling. Funktionerne til elektronisk fakturering låser op for en vifte af fordele, herunder: 

   - Hurtigere og nemmere tilpasning til lande-/områdespecifikke krav.
   - Standardiserede implementeringer af en løsning til elektronisk fakturering. 
   - Forbedret sporing af e-fakturaer.  
   - Nemmere vedligeholdelse for at overholde ændringer i de lovgivningsmæssige krav og den lokale forretningspraksis. 
   - Forenklet pakkeløsning.
   - Skaleringsegenskaber for en stor mængde sendte dokumenter, der medfører hurtigere omsætning.
   - Mulighed for at dele dine løsninger med andre virksomheder.

## <a name="does-electronic-invoicing-service-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Understøtter Elektronisk fakturering de lokale installationer af Finance, Supply Chain Management og Project Operations? 

Den aktuelle platform tillader ikke brugen af versionen i det lokale miljø, og der er ingen planer om at understøtte den i fremtiden.

## <a name="does-electronic-invoicing-service-interface-with-the-vendor-import-automation-feature"></a>Rummer grænsefladen for tjenesten Elektronisk fakturering funktionen til automatisk kreditorimport?

Nej Der er planer for denne grænseflade, men der er ingen planlagt tidslinje. Når det er planlagt, oplyses datoerne på forhånd i [Frigivelsesplaner](/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-service-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Hvordan håndterer tjenesten Elektronisk fakturering vedhæftede filer i den elektroniske faktura? Er der brug for en SharePoint-server, når der integreres PDF-filer i XML-filen?

De filer, der er tilknyttet den elektroniske faktura, håndteres som integrerede binære data i et XML-element. Der er ikke brug for en SharePoint-server for at integrere PDF-filer, men den vedhæftede fil skal gemmes i dokumentstyringssystemet i Finance, Supply Chain Management og Project Operations.

## <a name="is-electronic-invoicing-service-available-according-to-the-regulations-of-my-countryregion"></a>Er tjenesten Elektronisk fakturering tilgængelig i henhold til lovgivningen i mit land/område?

Tjenesten Elektronisk fakturering er en mikroserviceplatform, der vil være globalt tilgængelig.

Microsoft planlægger at publicere de elektroniske fakturaformater og integrationer for de lande og områder, der er funktionelt lokaliseret af Microsoft. Du kan finde flere oplysninger i [Tilgængelighed af funktioner til elektronisk fakturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Hvis det elektroniske faktureringsformat for dit land/område ikke er angivet, understøtter platformen dette scenario i fremtiden. Du kan stadig udnytte konfigurationsfunktionerne i elektronisk fakturering og selv konfigurere det elektroniske faktureringsformat, eller du kan samarbejde ammen med en partner/ISV om at konfigurere dem for din organisation.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Er Dynamics 365 til Regulatory Services et nyt modul som Human Resources eller Project Operations, der er knyttet til Finance eller Supply Chain Management? Er der ekstraomkostninger for det?

Dynamics 365 til Regulatory Services (RCS) er en cloudtjeneste til konfiguration af ressourcer til globalisering. RCS kan frit benyttes af alle licensindehavere til Finance, Supply Chain Management og Project Operations.

I forbindelse med tilmelding til RCS skal du gå til <https://marketing.configure.global.dynamics.com/>.

Du kan finde flere oplysninger i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing-service-or-just-turn-it-on-in-feature-management"></a>Skal jeg tilmelde mig for at få tjenesten Elektronisk fakturering, eller skal jeg blot aktivere den i Funktionsstyring?

Hvis du har en licens til Finance, Supply Chain Management og Project Operations, kan du se [Introduktion til tilføjelsesprogrammet til serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md) for at tilmelde dig elektronisk fakturering.

## <a name="does-electronic-invoicing-service-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Fungerer tjenesten Elektronisk fakturering sammen med virtuelle maskiner på niveau 1? Hvad er det minimale påkrævede miljø?

Integration med tjenesten Elektronisk fakturering kræver mindst en virtuel maskine på niveau 2 som vært for Finance eller Supply Chain Management. Du kan finde flere oplysninger om miljøplanlægning under [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-service-have-a-test-mode-for-testing-invoice-submission"></a>Er der en testtilstand for tjenesten Elektronisk fakturering til test af fakturaafsendelse?

Dette kan opnås ved hjælp af konfigurationen. Hvis du vil teste afsendelsen af fakturaer, kan du oprette forbindelse til Finance eller Supply Chain Management fra et UAT-miljø (test af brugeraccept) og sende testfakturaerne. Elektronisk fakturering understøtter konfiguration af test til digitale certifikater, og hvis der er e-fakturaer, der kræver digital godkendelse, understøttes opsætningen af en URL-adresse fra testwebtjenester, der er udgivet af skattemyndighederne.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Findes der dokumentation om de landespecifikke standardfunktioner til Elektronisk fakturering?

Ja. Du kan finde oplysninger om tilgængeligheden af funktioner til Elektronisk fakturering og de formater, de understøtter, i [Tilgængelighed af funktioner til elektronisk fakturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

## <a name="does-the-electronic-invoicing-service-allow-a-legal-entity-in-finance-or-supply-chain-management-that-is-configured-for-a-specific-country-to-consume-electronic-invoicing-features-from-different-countryregions"></a>Giver tjenesten Elektronisk fakturering mulighed for, at en juridisk enhed i Finance eller Supply Chain Management, der er konfigureret for et bestemt land/område, kan bruge funktioner til elektronisk fakturering fra forskellige lande/områder?

Ja. Funktionerne til elektronisk fakturering kan bruges til at behandle afsendelse af virksomhedsdokumenter uafhængigt af landet/området for den juridiske enhed, hvis følgende gælder:

   - Det virksomhedsdokument, der genereres, bruger den relevante dokumentmodeltilknytning.
   - Der er en match mellem virksomhedsdokumentet og anvendelighedsregler, der er konfigureret i funktionen til elektronisk fakturering.

## <a name="does-the-electronic-invoicing-service-use-the-same-configuration-and-design-experience-provided-by-the-electronic-reporting-module-in-finance-and-supply-chain-management"></a>Bruger tjenesten Elektronisk fakturering samme konfigurations- og designfunktioner fra modulet Elektronisk rapportering i Finance og Supply Chain Management? 

Ja. Samme designerværktøjer, der bruges i modulet Elektronisk rapportering (ER) i Finance og Supply Chain Management, bruges til at oprette og konfigurere tilknytning af datamodeller og filformatkonfigurationer. Disse designerværktøjer bruges også i Regulatory Configuration Services (RCS) til at oprette og konfigurere tilknytning af datamodeller og filformatkonfigurationer, der bruges i konfigurationen af e-faktureringsfunktionerne.

## <a name="can-the-applicability-rules-be-extended-and-configured-so-that-they-arent-tied-to-any-specific-parameter-such-as-a-legal-entity"></a>Kan anvendelsesreglerne udvides og konfigureres, så de ikke er knyttet til en bestemt parameter, f.eks. en juridisk enhed?

Ja. Anvendelsesreglerne kan konfigureres fuldt ud. Du kan tilføje eller fjerne sætninger, bygge logikhandlinger og gruppere og fjerne gruppering af sætninger. Du kan finde flere oplysninger i [Anvendelighedsregler](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#applicability-rules).

## <a name="does-the-electronic-invoicing-service-support-adding-other-er-format-configurations-to-generate-other-types-of-documents-does-it-support-sending-the-documents-electronically-to-customers-such-as-a-delivery-note"></a>Understøtter tjenesten Elektronisk fakturering tilføjelse af andre ER-formatkonfigurationer, så der kan genereres andre dokumenttyper? Understøtter den afsendelse af elektroniske dokumenter til kunder, f.eks. en leveringsnota?

Du kan bruge andre ER-formatkonfigurationer til at producere de ønskede outputfiler. Konfigurationen af ER-format skal dog afledes af samme ER-fakturamodeltilknytning, som er konfigureret i Finance eller Supply Chain Management for at generere virksomhedsdokumenter. Afsendelse af outputfilen direkte til kunden som en EDI-transaktion understøttes ikke som standard af Elektronisk fakturering.

## <a name="does-the-electronic-invoicing-service-support-exchanging-electronic-invoices-with-customers-does-it-support-configuring-different-invoice-formats-for-the-same-invoice"></a>Understøtter tjenesten Elektronisk fakturering udveksling af elektroniske fakturaer med kunder? Understøtter det konfiguration af forskellige fakturaformater for samme faktura?

Muligheden for at modtage og importere elektroniske kreditorfakturaer er på vej, men automatisk afsendelse af de elektroniske fakturaer til kunder understøttes ikke i øjeblikket.

## <a name="does-the-electronic-invoicing-service-extend-to-support-exchanging-edi-messages-with-other-companies"></a>Udvides tjenesten Elektronisk fakturering til at understøtte udveksling af EDI-meddelelser med andre firmaer?

Tjenesten Elektronisk fakturering har fokus på at udveksle elektroniske fakturameddelelsestyper baseret på lovkrav om overholdelse af angivne standarder. Modtagelse og import af elektroniske kreditorfakturaer er på vej, men afsendelse af elektroniske fakturafiler til kunden understøttes ikke i øjeblikket som standard, undtagen i scenarier, hvor afsendelse af elektronisk faktura til kunden er omfattet af et lovkrav.

## <a name="does-the-electronic-invoicing-service-support-importing-or-merging-customizations-made-in-the-er-format-configurations-from-the-legacy-electronic-invoicing-feature"></a>Understøtter tjenesten Elektronisk fakturering import eller fletning af tilpasninger, der er foretaget i ER-formatkonfigurationer fra den tidligere funktion for Elektronisk fakturering?

Du kan genbruge ER-formatkonfigurationer i tjenesten Elektronisk fakturering. Konfigurationen af ER-format skal dog afledes af samme ER-fakturamodeltilknytning, som den elektroniske fakturafunktion anvender, og som er konfigureret i Finance eller Supply Chain Management for at generere virksomhedsdokumenterne.

## <a name="does-the-electronic-invoicing-service-support-issuing-electronic-invoices-from-custom-made-tables-if-so-how-do-you-create-the-er-data-model-configurations-for-these-new-tables-and-entities"></a>Understøtter tjenesten Elektronisk fakturering udstedelse af elektroniske fakturaer fra brugerdefinerede tabeller? Hvordan kan du i så fald oprette ER-datamodelkonfigurationerne for disse nye tabeller og enheder?

Ja. Det kræver dog, at du tilpasser fakturamodeltilknytningen og tilføjer de nødvendige referencer til de brugerdefinerede tabeller, eller at du opretter en ny tilknytning af en fakturamodel, afhængigt af kompleksiteten.

## <a name="does-the-electronic-invoicing-service-support-different-web-service-endpoints"></a>Understøtter tjenesten Elektronisk fakturering forskellige webtjenesters slutpunkter?

Elektronisk fakturering understøtter forskellige webtjenesters slutpunkter. Du kan bruge konfigurerbar integration med REST-webtjenester eller en række landespecifikke parametre for webtjenesteintegrationer. Der kan konfigureres forskellige slutpunkter for samme webtjenester og API'er ved hjælp af forskellige versioner af konfigurationer. Du kan finde flere oplysninger i [Liste over parametre efter handling](e-invoicing-setup.md#list-of-parameters-by-action).

## <a name="is-electronic-invoicing-integrated-with-the-various-invoice-operators-apis-from-the-nordic-countries-or-should-that-be-handled-on-a-case-by-case-basis"></a>Er Elektronisk fakturering integreret med de forskellige fakturaoperatørers API'er fra de nordiske lande/områder, eller skal de håndteres fra sag til sag?

Microsoft udvider løbende funktionel dækning for at tilbyde standardintegrationer ved hjælp af funktionerne til elektronisk fakturering. Du kan finde flere oplysninger om de formater og integrationer, der understøttes, i [Tilgængelighed af funktioner for elektronisk fakturering](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Hvis du ikke fandt det svar, du leder efter, kan du sende dit spørgsmål via mail til Product Development Team på <D365EInvoicePreview@microsoft.com>. Vi vil enten kontakte dig eller forbedre dækningen af denne side med Ofte stillede spørgsmål.
