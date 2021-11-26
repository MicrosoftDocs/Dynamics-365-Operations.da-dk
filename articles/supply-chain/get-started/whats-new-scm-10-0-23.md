---
title: Forhåndsversion af Dynamics 365 Supply Chain Management 10.0.23
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.23.
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 7950d225bd528c05c14df108f4d44cef3e348ebb
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777785"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10023"></a>Forhåndsversion af Dynamics 365 Supply Chain Management 10.0.23

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I dette emne vises funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management-prøveversionen af version 10.0.23. Denne version har et build-nummer på 10.0.1037 og er tilgængelig som følger:

- **Prøveversion:** oktober 2021
- **Generel tilgængelighed af version (selv-opdatering):** december 2021

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Kolonnen *Funktion* indeholder links til [frigivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), hvor du kan se de officielle frigivelsesdatoer for hver funktion. Kolonnen *Flere oplysninger* indeholder flere oplysninger og/eller links til relateret dokumentation. Se kolonnen *Aktiveret efter*, hvis du vil have oplysninger om, hvordan du aktiverer funktionen. Du kan finde flere oplysninger om brug af administration af funktioner under [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Vi opdaterer muligvis dette emne for at medtage funktioner i det build, som er foretaget, efter dette emne blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---|---|---|---|
| Globalt adressekartotek | Definere en standardstat/-provins for hvert land/område i adresseopsætning | Du kan nu definere en standardstat/-provins for hvert land/område i adresseopsætningen for det globale adressekartotek. Når der angives en standardstat/-provins, vil det være den standardværdi, der angives i felterne for stat/provins, når du opretter en ny post for amt eller by for det pågældende land/område. Se også [Adresseopsætning](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | Aktiveret som standard. |
| Lager&nbsp;og&nbsp;logistik | [Sætte opgaver på pause i Warehouse Management-mobilappen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [Konfigurere omveje til trin i menupunkter på mobilenheder](../warehousing/warehouse-app-detours.md) | Funktionsstyring: (*Omveje i Warehouse Management-app*) |
| Lager&nbsp;og&nbsp;logistik | [Hævede felter i lagerstedsapp](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Konfigurere hævede felter for trin i mobilenheden](../warehousing/warehouse-app-promoted-fields.md)| Funktionsstyring (*hævede felter i appen Warehouse*) |
| Fremstillingsvirksomhed | [Integration af produktionsudførelsessystemer](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-systems-integration) | [Integrere med produktionsudførelsessystemer fra tredjeparter](../production-control/mes-integration.md) | Funktionsstyring (*Integration af produktionsudførelsessystem*) |
| Fremstillingsvirksomhed | [Rapport over samprodukter og biprodukter fra grænsefladen for udførelse af produktion](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [Sådan anvender arbejdere grænsefladen til kørsel af produktion](../production-control/production-floor-execution-use.md) | Funktionsstyring (*Rapport over samprodukter og biprodukter fra grænsefladen for udførelse af produktion*) |
| Planlægning | [Understøttelse af planlægningsoptimering til prioritetsstyret planlægning](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-priority-based-planning) | [Prioritetsbaseret planlægning](../master-planning/planning-optimization/priority-based-planning.md) | Funktionsstyring (*Prioritetsstyret MRP-understøttelse af planlægningsoptimering*) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er nye i denne version. Hver af disse udvidelser giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet).

Hvis du vil slå nogen af disse funktioner til og fra, skal du gøre det i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), hvor de vises med deres navne i kolonnen *Funktionsnavn i funktionsstyring* i følgende tabel.

| Modul | Funktionsnavn i funktionsstyring | Flere oplysninger |
|---|---|---|
| Aktivstyring | Modkonti for udgifter i arbejdsordrekladder | Med denne funktion kan du angive en modkonto for hver udgift, der vises i en arbejdsordrekladde. Du vil typisk knytte en kreditorkonto til de enkelte udgifter, men andre kontotyper understøttes også. Den føjer to nye kolonner (**Modkontotype** og **Modkonto**) til oversigtspanalet **Udgift** på siden **Arbejdsordrekladde**.|
| Omkostningsstyring | Opret relaterede bilag til værdireguleringer af standardomkostningsafrunding | <p>Når der foretages en økonomisk lagerbogføring (f.eks. en salgsordrefaktura eller lagertransaktion), bevirker denne funktion, at systemet opretter et separat bilag til eventuelle relaterede værdireguleringer af standardomkostninger og knytter det til bilaget for økonomisk bogføring som et relateret bilag.</p><p>Uden denne funktion registrerer systemet standardomkostningsafrundingsreguleringer på samme bilagsbogføring. Denne funktionsmåde kan nogle gange medføre oplysninger om modstridende dato, fordi værdireguleringerne bruger sessionen eller systemdatoen, mens økonomiske posteringer bruger bogføringsdatoen.</p> |
| Lager- og lokationsstyring | \[Rusland\] Bogfør transaktioner for økonomisk lager for Storno i henhold til korrektionsflaget i det økonomiske bilag for salgsordrer | Denne funktion har indflydelse på funktionen til korrektion af kreditnotaer for Rusland. Den gør det muligt at bogføre lagertransaktioner for salgsfakturaer i overensstemmelse med korrektionsindstillingen i Finans. Når denne funktion er aktiveret, er der ikke flere uoverensstemmelser mellem flaget **Rettelse** på det økonomiske bilag for lagertransaktionen og flaget **Storno** på lagertransaktioner. |
| Lager- og lokationsstyring | (Rusland) Kør beregning af lagersaldoomsætningsrapport i batch | For russiske oversættelser af Supply Chain Management giver denne funktion mulighed for at køre rapporten *Omsætning for lagersaldo* i batch, lagre den og se de rapporter, der er genereret tidligere. |
| Lager- og lokationsstyring | (Rusland) Brug oversættelser til lokalt sprog i lande- eller områdespecifikke primære formularer i Lagerstyring | For russiske oversættelser af Supply Chain Management gør denne funktion det muligt at bruge russiske oversættelser af produkt-/varenavne og måleenheder i følgende russiske specifikke lagerudskrifter: Optællingsliste (INV-3), Optællingsliste (INV-5) og Optællingsliste (INV-6). |
| Indkøb og forsyning | Ryd op i historik for købsordreopdatering | Med denne funktion kan du rydde op i midlertidige historikposter, der er relateret til opdateringer af indkøbsordrer. Den tilføjer en ny knap med navnet **Ryd op i historik for købsordreopdatering** i handlingsruden på siden **Alle indkøbsordrer**. Denne funktion er som standard aktiveret. |
| Produktionsstyring | (Forhåndsversion) Automatisk pluk af materialer, der er aktiveret til lagersted, til automatisk bogførte pluklister | Med denne funktion kan du automatisk plukke og løse lagerdimensioner for automatisk bogførte og afledte/varetrækspluklistekladder. |
| Produktionsstyring | Valider udløb af råmaterialer i forhold til planlagt forbrugsdato | Denne funktion ændrer den måde, som batchudløbsdatoer valideres på, når der reserveres en råvarebatch, som skal bruges under produktionen. Når denne funktion er aktiveret, valideres batchudløbsdatoen i forhold til den planlagte forbrugsdato (råvaredatoen), som angivet på produktionsstyklistelinjen eller batchordreformellinjen. Når denne funktion er deaktiveret, valideres batchudløbsdatoen i forhold til den planlagte leveringsdato for produktionen eller batchordren (som tidligere). |
| Salg og marketing | Ryd op i historik for salgsopdatering baseret på alder | Med denne funktion kan du angive den maksimale alder for poster, der skal beholdes, når du kører den periodiske opgave **Oprydning af salgsopdateringshistorikken**. Ældre poster slettes. Dette er nyttigt, når du angiver, at opgaven skal køres periodisk, da alderen altid beregnes i forhold til den dato, hvor opgaven køres. Uden denne funktion kan du kun angive en bestemt dato for de ældste poster, der skal beholdes. |
| Salg og marketing | Forbedr ydeevne for rapport med "Top 100" kunder | Denne funktion forbedrer ydeevnen for rapporten med **Top 100**-kunder ved altid at køre rapporten på tværs af alle kunder (som den er beregnet til) i stedet for at tillade brugerdefinerede forespørgsler. Når denne funktion er aktiveret, deaktiveres alle indstillinger for **Poster, der skal indgå** i dialogboksen med **Top 100**-rapporten. |
| Lagerstedsstyring | Skaler enhedssupport til frigivelse til lagersted af udgående ordrer | Når funktionen er aktiveret, kan udgående ordrer frigives direkte fra hubben til skalaenheden, hvor ordrerne skal opfyldes. |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-emner. Disse emner er ikke nødvendigvis knyttet til de nye funktioner, der er tilføjet for denne version, som vist i forrige afsnit. De kan dog hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede emner |
|---|---|
| Styring af tekniske ændringer | [Tekniske attributter og søgning efter tekniske attributter](../engineering-change-management/engineering-attributes-and-search.md) beskriver nu, hvordan teknikerattributarv fungerer. |
| Varedisponering | [Varedisponering med behovsprognoser](../master-planning/planning-optimization/demand-forecast.md) og [Prognosereduktionsnøgler](../master-planning/reduction-keys.md) indeholder nu flere oplysninger om, hvordan du kan arbejde med reduktionsnøgler. |
| Varedisponering | [Opfyldning af sikkerhedslager for varer](../master-planning/safety-stock-replenishment.md) indeholder nu flere oplysninger om brug af minimums-/maksimumsnøgler. |
| Varedisponering | [Lagerbudgetter](../master-planning/inventory-forecast.md) indeholder nu flere oplysninger om tildeling af budgetter. |
| Varedisponering | [Forsyningsplan](../master-planning/supply-schedule.md) |
| Lagerstedsstyring | [Globale parametre for mobilenhed](../warehousing/mobile-device-parameters.md) |
| Lagerstedsstyring | [Forankring](../warehousing/anchoring.md) |
| Salg og marketing | Intern handel beskrives nu detaljeret med start fra [Konfigurere intern handel](../sales-marketing/intercompany-trade-set-up.md) og de relaterede emner. |
| Lagerstyring | Dokumentationen til Lagersynlighed er udvidet og opdateret med start fra [Oversigt over tilføjelsesprogram for lagersynlighed](../inventory/inventory-visibility.md) og de relaterede emner. |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformopdateringer til Finance and Operations-apps

Microsoft Dynamics 365 Supply Chain Management 10.0.23 indeholder platformopdateringer. Du kan få mere vide i [Platformopdateringer til version 10.0.23 af Finance and Operations-apps (november 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.23, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 og brancheskyer: 2021 frigivelsesplan bølge 2

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2021 frigivelsesplan bølge 2](/dynamics365-release-plan/2021wave2/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjernede og udfasede Supply Chain Management-funktioner

Emnet [Fjernede eller udfasede funktioner Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver de funktioner, der er planlagt eller skal fjernes eller udfases for Supply Chain Management.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i emnet [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
