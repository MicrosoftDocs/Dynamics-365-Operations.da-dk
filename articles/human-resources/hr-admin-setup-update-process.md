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
# <a name="update-process"></a>Opdater proces

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources er en ægte Software som en service (SaaS), der tilbyder kontinuerlige serviceopdateringer uden manuel indgriben. Disse opdateringer indeholder både program- og platformsændringer, der ofte giver vigtige forbedringer af tjenesten, herunder lovpligtige opdateringer.

## <a name="update-policy"></a>Opdateringspolitik

Opdateringer udgives regelmæssigt til alle miljøer. Human Resources understøttes i overensstemmelse med [Livscykluspolitik for Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), der giver leverer klare retningslinjer for tilgængeligheden af support.

## <a name="release-cadence"></a>Opdateringstakt af versioner 

Human Resources-opdateringer anvendes automatisk til alle miljøer. Der frigives to typer versioner af Human Resources:

- **Serviceopdateringer**: Opdateringer foretages hver anden uge og omfatter fejlrettelser og nye funktioner. Serviceopdateringer omfatter også relevante platformsopdateringer, når de frigives. Du kan få en ide om, hvornår der udgives opdateringer af platformen i [Tabel 3: Platformsversioner](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases). Opdateringer hver anden uge sker i en midlertidigt global udrulning på tværs af områder. Du kan finde flere oplysninger om opdateringer hver anden uge i [Nyheder eller ændringer i Dynamics 365 Human Resources](hr-admin-whats-new.md).

    Alle understøttede datacentre opdateres hver anden uge, medmindre andet er angivet. Områderne USA, Australien, Europa, Storbritannien, Asien og Canada medtages i opdateringer hver anden uge. 

- **Dataverse-løsningsopdateringer**: Disse opdateringer forekommer ca. hver 6. uge efter behov. De omfatter nye enheder og ændringer af eksisterende objekter i Dataverse. Disse opdateringer frigives til samme regioner som de opdateringer hver anden uge, og de tager ca. seks uger at replikere gennem alle datacentre. Løsningsopdateringer kan muligvis blive justeret efter serviceopdateringer hver anden uge.

> [!NOTE]
> Løsningsopdateringer er tilgængelige i alle datacentre, når de er frigivet. Hvis du ikke vil vente på, at opdateringerne replikeres automatisk, kan du anvende disse opdateringer manuelt i alle miljøer i alle datacentre.

Når det er nødvendigt, leverer Human Resources også følgende typer rettelser:

- **Revision (hotfix)**: Fejlrettelser, der kan forekomme sammen med eller separat i forhold til en serviceopdateringsversion hver anden uge

- **Fejlrettelse i nødstilfælde**: Proaktive og reaktive hotfixes, der er uafhængige af hinanden, kan indeholde ændringer, der kun vedrører konfiguration eller kode til at løse problemer med aktive websteder og kan forekomme uafhængigt af en serviceopdateringsversion hver anden uge

Versioner gennemses, testes og valideres i et internt miljø. Når builds er godkendt, kan de installeres.

## <a name="release-cadence-exceptions-in-2021"></a>Undtagelser til udgivelsestakten i 2021

For at kunne tage højde for feriedage er frigivelsesplanen for november og december 2021 følgende.

- Frigivelse i november: 1. november - 14. november
- Frigivelse i december: 29. november - 12. december
 
Den to-ugers frigivelsestakt vil fortsætte som sædvanligt den 10. januar 2022.

## <a name="communications"></a>Kommunikation

Du kan finde ud af, hvad der planlægges for Human Resources, og hvad vi har udgivet på følgende placeringer:

- [Dynamics 365 Human Resources-oversigt](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365-frigivelsesplaner](/dynamics365/release-plans/)

- [Nyheder eller ændringer i Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Problemsøgning i Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (kun for platformsrelaterede fejl)

- [Human Resources-blog](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer-fællesskab](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Prøveversionsfunktioner i et sandkassemiljø

Du kan validere funktioner i prøveversioner i et sandkassemiljø, før du aktiverer dem i produktionsmiljøet. Du kan finde flere oplysninger om aktivering af nye funktioner under [Oversigt over funktionsstyring](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Alle nye funktioner vises i forhåndsvisning i mindst 30 dage og typisk 30-60 dage. De vigtigste funktioner er normalt tilgængelige i oktober og april hvert år efter forhåndsvisningsperioden. Så snart du ser nye egenskaber i arbejdsområdet Administration af funktioner, kan du slå dem til. Nogle funktioner er muligvis som slået til som standard.

På visse tidspunkter er en integreret funktion som standard slået til og kan ikke slås fra (f.eks. arbejdsområdet Administration af funktioner).

Når en funktion er generelt tilgængelig, kan den slås til eller fra i produktionsmiljøer. Arbejdsområdet Administration af funktioner angiver, hvornår en visningsfunktion skal være obligatorisk. Denne dato er som regel den 1. oktober eller 1. april for at tilpasse det med de halvårlige frigivelsesplaner. Du kan ikke slå de obligatoriske funktioner fra. Indtil den bliver obligatorisk, kan du slå en funktion til og fra i alle miljøer.

Vi anbefaler, at du får vist funktioner i prøveversioner i et sandkassemiljø. Det er bedst at oprette en kopi af dit aktuelle produktionsmiljø eller database i et sandkassemiljø, så du kan få den fulde erfaring med de nye funktioner sammen med dine data.

Yderligere oplysninger om klargøring af et sandkassemiljø finder du [Klargøre et Human Resources-projekt](hr-admin-setup-provision.md). Hvis du skal fjerne et testmiljø, kan du se [Fjerne en forekomst](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Rapportere fejl

Under test af funktioner i prøveversion eller afprøvning af nye funktioner, kan du finde elementer, der ikke fungerer som forventet. Rapporter eventuelle fejl via [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Se også

[Dynamics 365 og Power Platform frigivelsesplaner](/dynamics365/release-plans)</br>
[Nyheder eller ændringer i Dynamics 365 Human Resources](hr-admin-whats-new.md)</br>
[Livscykluspolitik for software](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]