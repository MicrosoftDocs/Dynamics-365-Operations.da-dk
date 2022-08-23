---
title: Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.26. (maj 2022)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management 10.0.26.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: b44b044bf10115a7fcaf347a3b6f1759c2a68cb6
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219058"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10026-may-2022"></a>Nyheder eller ændringer i Dynamics 365 Supply Chain Management 10.0.26. (maj 2022)

[!include [banner](../includes/banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Supply Chain Management version 10.0.26. Denne version har et build-nummer på 10.0.1192 og er tilgængelig som følger:

- **Forhåndsversion:** marts 2022
- **Generel tilgængelighed af version (selvopdatering):** april 2022
- **Generel tilgængelighed af version (automatisk opdatering):** maj 2022

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---|---|---|---|
| Lager og logistik | [Forespørgsel om lagerbeholdning med lagersynlighed for at understøtte avancerede varer i Warehouse management](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [Understøttelse af lagersynlighed for WMS-varer](../inventory/inventory-visibility-whs-support.md) | Funktionsstyring:<br>*Aktivér lagerstedsvarer i lagersynlighed* |
| Lager og logistik | [Disponibel til tilsagn for tilføjelsesprogrammet Lagersynlighed](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Ændringsplaner for disponibelt antal og disponibel til tilsagn i lagersynlighed](../inventory/inventory-visibility-available-to-promise.md) | Aktiveret af servicekonfiguration |
| Fremstillingsvirksomhed | [Fastvægtvarer til udførelse af grænsefladen til produktionen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Sådan anvender arbejdere grænsefladen til kørsel af produktion](../production-control/production-floor-execution-use.md) | Funktionsstyring:<br>*Rapport over fastvægtvarer fra grænsefladen for udførelse af produktionsgulv* |
| Fremstillingsvirksomhed | Fanen Mine job i grænsefladen til produktionsudførelse <!-- KFM: Add link to release plan when available --> | [Sådan anvender arbejdere grænsefladen til kørsel af produktion](../production-control/production-floor-execution-use.md) | Funktionsstyring:<br>*Fanen Mine job i grænsefladen til produktionsudførelse* |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsforbedringer, der er inkluderet i denne version

Følgende tabel indeholder de funktionsforbedringer, der er inkluderet i denne version. Hver af disse udvidelser giver en trinvis forbedring af en eksisterende funktion. Da det kun er forbedringer, er de ikke angivet i [udgivelsesplanen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Men for at sikre, at disse forbedringer ikke er i konflikt med dine eksisterende tilpasninger eller præferencer, er hver af dem som standard deaktiveret (medmindre andet er angivet).

Hvis du vil slå en af disse funktioner til eller fra, skal du gøre det i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktionsnavn i funktionsstyring | Flere oplysninger |
|---|---|---|
| Indkøb og forsyning | Bogfør registrerede antal lagerbaserede produkter og rester af ikke-lagerbaserede produkter for modtagelser og kreditorfakturaer | Denne funktion ændrer, hvordan antal ikke-lagerbaserede produkter (som f.eks. tjenester) bogføres, når der behandles kreditorfakturaer og indgående forsendelser i forhold til indkøbsordrer. Funktionen ændrer funktionsmåden for indstillingen af *Registreret antal og tjenester* for bogføring af tilgange og kreditorfakturaer ved at ændre den, så den stemmer overens med funktionaliteten af *Registreret antal og ikke-lagerførte produkter* der allerede er angivet, når der bogføres antal for salgsfølgesedler.<br><br>Når du bogfører en produktkvittering eller kreditorfaktura ved hjælp af indstillingen *Registreret antal og tjenester*, bogfører systemet det registrerede antal lagervarer og bogfører det resterende antal ikke-lagerbaserede produkter (herunder både tjenester og ikke-tjenester). Uden denne funktion bogfører systemet stadig den registrerede mængde lagervarer (herunder tjenester, der er konfigureret som lagervarer), men bogfører altid det fulde bestilte antal ikke-lagerførte serviceprodukter (og ignorerer ikke-lagerførte produkter, der ikke er af typen *Service*). |
| Indkøb og forsyning | Synkronisere sporingsdimensioner på interne salgs- og indkøbsordrelinjer | Denne funktion giver dig mulighed for at styre, om sporingsdimensionerne for serienumre og batchnumre synkroniseres på tværs af interne salgs- og indkøbsordrelinjer. Den føjer nye indstillinger til både **Politikker for indkøbsordrer** og fanerne **Salgsordrepolitikker** på siden **Intern** opsætning for debitorer og kreditorer. Det opdaterer også navnene på nogle få relaterede, nærliggende indstillinger for klarheds skyld.<br><br>Hvis du bruger avanceret lokationsstyringsprocesser (WMS), skal du være opmærksom på, at denne funktion kun synkroniserer batch- og serienumre, når disse dimensioner ligger over lokationen i hierarkiet for destinationsreservationer. |
| Administration af produktoplysninger | Ryd op i produktattributværdier | Denne funktion tilføjer en periodisk opgave med navnet **Ryd op i produktattributværdier**, der rydder op i poster for produktattributværdier, som ikke længere er knyttet til et produkt via en produktkategori. |
| Lager- og Warehouse management | (Rusland) Undgå afvigelser ved udstedelse af GTD'er for indkøbsordrer, der omfatter WMS-aktiverede varer | Denne funktion er kun til russisk lokalisering. Det forhindrer uoverensstemmelse, der opstår, når der udstedes russiske tolddeklarationsnumre (GTD'er) til import af indkøbsordrer, der omfatter varer, der er aktiveret til lokationsstyringsprocesser (WMS). GTD-processen til udstedelse ændrer nogle lagerdimensionsværdier for de relaterede lagertransaktioner for fakturaer, der er medtaget i den brugerdefinerede kladde, hvilket medfører uoverensstemmelser mellem arbejdsposterne for indkøbsordren og lagertransaktionerne for indkøbet. Når denne funktion er aktiveret, genererer GTD-udstedelsesprocessen reguleringsarbejde, der eliminerer sådanne uoverensstemmelser. |
| Warehouse management | Udvidet parser til GS1-stregkoder | Denne funktion tilføjer en forbedret parser til GS1-symboldata. Den nye parser implementerer GS1-algoritmen Generel specifikation til fortolkning af GS1-symboler og giver stærkere validering af data. Du kan finde flere oplysninger under [GS1-stregkodescanning](../warehousing/gs1-barcodes.md). |
| Warehouse management | Nye sider med lastplanlægningspanel | Tilføjer to nye sider i lastplanlægningspanelet: **Indgående lastplanlægningspanel** og **Udgående lastplanlægningspanel**. |
| Warehouse management | Applikation til Warehouse management – tom GTD | Denne funktion er kun til russisk lokalisering. Det giver arbejdere, der bruger mobilappen Warehouse Management, mulighed for at lade russiske tolddeklarationsnumre (GTD'er) være tomme, hvis det er nødvendigt. Hvis GTD-sporingsdimensionen er konfigureret til at tillade tomme værdier, accepterer systemet tomme værdier til GTD for lageroperationer, hvis den disponible lagerbeholdning er tilgængelig. |

## <a name="new-and-updated-documentation-resources"></a>Nye og opdaterede dokumentationsressourcer

Vi har for nylig tilføjet eller væsentligt opdateret følgende Hjælp-artikler. Disse artikler er ikke nødvendigvis knyttet til de nye funktioner, der er tilføjet for denne version, som vist i forrige afsnit. De kan dog hjælpe dig med at få mere ud af eksisterende funktioner.

| Funktionsområde | Nye eller opdaterede artikler |
|---|---|
| Omkostningsstyring | Der er føjet opdaterede eksempler og diagrammer til hvert af følgende artikler:<ul><li>[FIFO med fysisk værdi og afmærkning](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO med fysisk værdi og afmærkning](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO-dato med fysisk værdi og mærkning](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Løbende gennemsnitskostpris](../cost-management/running-average-cost-price.md)</li><li>[Vægtet gennemsnit med fysisk værdi og afmærkning](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til programmer til finans og drift

Microsoft Dynamics 365 Supply Chain Management 10.0.26 indeholder platformopdateringer. Du kan få mere vide i [Platformsopdateringer til version 10.0.26 af programmer til finans og drift (maj 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md).

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af 10.0.26, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

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

