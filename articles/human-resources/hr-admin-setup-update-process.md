---
title: Opdater proces
description: Microsoft Dynamics 365 Human Resources er en ægte Software som en service (SaaS), der tilbyder kontinuerlige serviceopdateringer til program- og platformændringer.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 267682f4497bacf70f93840a948d0e525dfa4aa1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092195"
---
# <a name="update-process"></a>Opdater proces

Microsoft Dynamics 365 Human Resources er en ægte Software som en service (SaaS), der tilbyder kontinuerlige serviceopdateringer uden manuel indgriben. Disse opdateringer indeholder både program- og platformsændringer, der ofte giver vigtige forbedringer af tjenesten, herunder lovpligtige opdateringer.

## <a name="update-policy"></a>Opdateringspolitik

Opdateringer udgives regelmæssigt til alle miljøer. Personale understøttes i overensstemmelse med [Livscykluspolitik for Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), der giver leverer klare retningslinjer for tilgængeligheden af support.

## <a name="release-cadence"></a>Opdateringstakt af versioner

Personale-opdateringer anvendes automatisk til alle miljøer. Der frigives to typer versioner af Personale:

- **Serviceopdateringer**: Ugentlige opdateringer, der omfatter fejlrettelser og nye funktioner. Serviceopdateringer omfatter også relevante platformsopdateringer, når de frigives. Du kan få en ide om, hvornår der udgives opdateringer af platformen i [Tabel 3: Platformsversioner](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). Ugentlige opdateringer frigives normalt om onsdagen. Du kan finde flere oplysninger om ugentlige opdateringer i [Nyheder eller ændringer i Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).

    Alle understøttede datacentre opdateres hver uge, medmindre andet er angivet. Ugentlige opdateringer starter typisk en onsdag og afsluttes søndag. Områderne USA, Australien, Europa, Storbritannien, Asien og Canada medtages i ugentlige opdateringer. 

- **Common Data Service-løsningsopdateringer**: Disse opdateringer forekommer ca. hver 6. uge efter behov. De omfatter nye enheder og ændringer af eksisterende objekter i Common Data Service. Disse opdateringer frigives til samme regioner som de ugentlige opdateringer, og de tager ca. seks uger at replikere gennem alle datacentre. Løsningsopdateringer kan muligvis blive justeret efter ugentlige serviceopdateringer.

Følgende tabel viser et eksempel på en tidsplan:

| Uge | Opdateringstype |
| --- | --- |
| 1 | Serviceopdatering (alle områder) |
| 2 | Serviceopdatering (alle områder) + løsningsopdatering (uge 1 regioner) |
| 3 | Serviceopdatering (alle områder) + løsningsopdatering (uge 2 regioner) |
| 4 | Serviceopdatering (alle områder) + løsningsopdatering (uge 3 regioner) |
| 5 | Serviceopdatering (alle områder) + løsningsopdatering (uge 4 regioner) |
| 6 | Serviceopdatering (alle områder) + løsningsopdatering (uge 5 regioner) |
| 7 | Serviceopdatering (alle områder) + løsningsopdatering (uge 6 regioner) |
| 8 | Serviceopdatering (alle områder) |

> [!NOTE]
> Løsningsopdateringer er tilgængelige i alle datacentre, når de er frigivet. Hvis du ikke vil vente på, at opdateringerne replikeres automatisk, kan du anvende disse opdateringer manuelt i alle miljøer i alle datacentre.

Når det er nødvendigt, leverer Personale også følgende typer rettelser:

- **Revision (hotfix)**: Fejlrettelser, der kan forekomme sammen med eller separat i forhold til en ugentlig serviceopdateringsversion

- **Fejlrettelse i nødstilfælde**: Proaktive og reaktive hotfixes, der er uafhængige af hinanden, kan indeholde ændringer, der kun vedrører konfiguration eller kode til at løse problemer med aktive websteder og kan forekomme uafhængigt af en ugentlig serviceopdateringsversion

Versioner gennemses, testes og valideres i et internt miljø. Når builds er godkendt, kan de installeres.

## <a name="exceptions-in-2019"></a>Undtagelser i 2019

Følgende datoer er undtagelser til den almindelige versionsplan:

| Dato | Beskrivelse |
| --- | --- |
| Uge med 25. november | Ingen opdateringer |
| Uge med 16. december | Kun mindre opdateringer |
| Uge med 23. december | Ingen opdateringer |
| Uge med 30. december | Ingen opdateringer |

## <a name="communications"></a>Kommunikation

Du kan finde ud af, hvad der planlægges for Personale, og hvad vi har udgivet på følgende placeringer:

- [Dynamics 365 Human Resources-oversigt](https://dynamics.microsoft.com/roadmap/talent/)

- [Dynamics 365-frigivelsesplaner](https://docs.microsoft.com/dynamics365/release-plans/)

- [Nyheder eller ændringer i Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Problemsøgning i Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (kun for platformsrelaterede fejl)

- [Personale-blog](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Personale Yammer-fællesskab](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Prøveversionsfunktioner i et sandkassemiljø

Du kan validere funktioner i prøveversioner i et sandkassemiljø, før du aktiverer dem i produktionsmiljøet. Du kan finde flere oplysninger om aktivering af nye funktioner under [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funktioner vises i forhåndsvisning i mindst 30 dage og typisk 30-60 dage. De vigtigste funktioner er normalt tilgængelige i oktober og april hvert år efter forhåndsvisningsperioden. Så snart du ser nye egenskaber i arbejdsområdet Administration af funktioner, kan du slå dem til. Nogle funktioner er muligvis som slået til som standard.

På visse tidspunkter er en integreret funktion som standard slået til og kan ikke slås fra (f.eks. arbejdsområdet Administration af funktioner).

Når en funktion er generelt tilgængelig, kan den slås til eller fra i produktionsmiljøer. Arbejdsområdet Administration af funktioner angiver, hvornår en visningsfunktion skal være obligatorisk. Denne dato er som regel den 1. oktober eller 1. april for at tilpasse det med de halvårlige frigivelsesplaner. Du kan ikke slå de obligatoriske funktioner fra. Indtil den bliver obligatorisk, kan du slå en funktion til og fra i alle miljøer.

Vi anbefaler, at du får vist funktioner i prøveversioner i et sandkassemiljø. Det er bedst at oprette en kopi af dit aktuelle produktionsmiljø eller database i et sandkassemiljø, så du kan få den fulde erfaring med de nye funktioner sammen med dine data.

Yderligere oplysninger om klargøring af et sandkassemiljø finder du [Klargøre et Personale-projekt](hr-admin-setup-provision.md). Hvis du skal fjerne et testmiljø, kan du se [Fjerne en forekomst](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Rapportere fejl

Under test af funktioner i prøveversion eller afprøvning af nye funktioner, kan du finde elementer, der ikke fungerer som forventet. Rapporter eventuelle fejl via [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Se også

- [Dynamics 365 og Power Platform frigivelsesplaner](https://docs.microsoft.com/dynamics365/release-plans)
- [Nyheder eller ændringer i Dynamics 365 Personale](hr-admin-whats-new.md)
- [Livscykluspolitik for software](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

