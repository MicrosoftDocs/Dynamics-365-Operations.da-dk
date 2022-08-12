---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.28 (august 2022)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.28.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 7e17127ff6ef6c52034b8aa5e0c8404772363ca9
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186513"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.28 (august 2022)

[!include [banner](../includes/banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management version 10.0.28. Denne version har et build-nummer på 10.0.1264 og er tilgængelig i følgende plan:

- **Forhåndsversion:** maj 2022
- **Generel tilgængelighed af version (selvopdatering):** juli 2022
- **Generel tilgængelighed af version (automatisk opdatering):** juli 2022

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---|---|---|---|
| Lager og logistik | [Enheder til integration af landingsomkostninger for tredjepartsspeditører](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Oversigt over enheder til landingsomkostninger](../landed-cost/landed-cost-entities-overview.md) | Aktiveret som standard |
| Planlægning | [Planlægning af efterspørgselsbaseret materialebehov (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [Oversigt over planlægning af efterspørgselsbaseret materialebehov](../master-planning/planning-optimization/ddmrp-overview.md) | Funktionsstyring:<br>*(Forhåndsversion) DDMRP til planlægningsoptimering* |
| Planlægning | [Planlægningsoptimerings-understøttelse af CTP (leveringsevne)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | Kommer snart | Funktionsstyring:<br>*(Forhåndsversion) CTP til planlægningsoptimering* |
| Planlægning | [Understøttelse af hyldelevetid i planlægningsoptimering](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | Kommer snart | Aktiveret som standard |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse udvidelser giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet).

Hvis du vil slå en af disse funktioner til eller fra, skal du gøre det i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktionsnavn i funktionsstyring | Flere oplysninger |
|---|---|---|
| Lager- og Warehouse management | Aktivér intern beholdning, så den kun viser beholdninger, der ikke er nul | Du kan bruge denne funktion til at vælge, om varer med en beholdning på nul skal medtages på den interne beholdningsliste. Du kan styre denne indstilling ved hjælp af indstillingen **Vis ikke varer med en beholdning på nul på den interne lagerbeholdningsliste**, som denne funktion tilføjer på siden **Parametre til lager- og lokationsstyring**. |
| Lager- og Warehouse management | (Indien) Ignorer lokation for regler for overførselspris, når "Fra lagerstedskode" er indstillet til "Alle" | <p>Denne funktion gælder kun for lokaliseringer til Indien. Det gør det nemmere at oprette overførselspriser for varer i lageroverførsler.</p><p>Du kan oprette overførselspriser ved at konfigurere hver vare med regler for overførselsprissætning. Du kan f.eks. oprette denne konfiguration ved at medtage en regellinje, hvor feltet **Fra-lagerstedskode** er angivet til *Alle*. Denne indstilling angiver, at overførselsprisen, der defineres af linjen, skal gælde, uanset hvilket lagersted varen plukkes fra. Når denne funktion er aktiveret, ignoreres **Lokation**-indstillingen i regler for overførselspris, hvor feltet *Fra lagerstedskode* er angivet til **Alle**. Derfor gælder reglen, uanset hvilken lokation der er angivet i flytteordren. Denne funktionsmåde er sandsynligvis forventet, fordi lokationen ligger under lagerstedet i hierarkiet for lagringsdimensionen.</p><p>Uden denne funktion vil systemet kun anvende regler af denne type, når lokationen på flytteordren svarer nøjagtigt til den lokation, der er angivet for reglen. (Hvis reglen indeholder en tom lokation, anvender systemet kun reglen på flytteordrer, der også har en tom værdi for lokationen).</p> |
| Lager- og Warehouse management | Rapporten Disponibelt lager – oprydning i data | Denne funktion gør det muligt at rydde op i data, der bruges til at oprette *Lagring af rapporten Disponibelt lager*-rapporter. |
| Produktionsstyring | Tildel projektaktiviteter for serviceaftale og serviceordrelinjer | Denne funktion føjer et felt med navnet **Projektaktivitet** til serviceaftale- og serviceordrelinjer, så du kan angive en projektaktivitet for dem. Denne funktion kan hjælpe med at forhindre blokeringsfejl, når du bogfører projektkladder under servicestyring, der kræver, at der angives en projektaktivitet.  |
| Warehouse management | Manuel udvalgstjeneste for overførselslinjer for administratorer eller lignende betroede brugere | Denne funktion giver administratorer mulighed for manuelt at plukke lagertransaktioner, der er relateret til flyttelinjer. Disse linjer omfatter linjer, der allerede er frigivet til lagerstedet. Administratorer bør kun foretage dette pluk i særlige tilfælde, f.eks. hvis systemet er i ødelagt tilstand. |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-artikler. Disse artikler er ikke nødvendigvis knyttet til de nye funktioner, der er tilføjet for denne version, som vist i forrige afsnit. De kan dog hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede artikler |
|---|---|
| Omkostningsstyring | [Fast tilgangspris](../cost-management/fixed-receipt-price.md) |
| Omkostningsstyring | [Ofte stillede spørgsmål om lagerefterkalkulation](../cost-management/inventory-costing-faq.md) |
| Omkostningsstyring | [Regnskabsprincippet for bogføring på omkostningskonto](../cost-management/post-to-charge-account-accounting-principle.md) |
| Lagerstyring | [Detaljer om lagertransaktion](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til programmer til finans og drift

Microsoft Dynamics 365 Supply Chain Management 10.0.28 indeholder platformopdateringer. Du kan få mere at vide i [Platformsopdateringer til version 10.0.28 af programmer til finans og drift (juni 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.28, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 1

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 1](/dynamics365-release-plan/2022wave1/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Artiklen [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i artiklen [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

