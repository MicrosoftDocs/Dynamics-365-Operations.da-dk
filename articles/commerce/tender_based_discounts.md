---
title: Betalingsmiddelbaserede rabatter
description: Dette emne giver en oversigt over funktioner, som detailhandlere kan bruge til at konfigurere rabatter for bestemte betalingsmiddeltyper.
author: bebeale
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 4be0c9a6f0a32016e07b8e31d0aaff44b4a29623
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411194"
---
# <a name="tender-based-discounts"></a>Betalingsmiddelbaserede rabatter

[!include [banner](includes/banner.md)]


Det er en almindelig praksis blandt detailhandlere at udstede egne, brandede kreditkort. Detailhandlerne får fordel af de foretrukne satser fra bankerne. Da disse kreditkort også kan give opmuntre kunderne til at besøge butikken flere gange, er de også med til at forbedre forhandlerens bundlinje. Derfor har detailhandlere et incitament til at øge kundernes anvendelse af deres brandede kreditkort. For at nå dette mål giver de ofte ekstra rabatter til kunder, der bruger disse kreditkort.

Det kan også være, at forhandlere, der ikke tilbyder brandede kreditkort, vil opmuntre kunderne til at betale med andre betalingsmiddeltyper, f.eks. kontant, gavekort eller fordelskundepoint. På denne måde kan de hjælpe med at reducere udgiften af gebyrer til behandling af kreditkort. Derfor kan detailhandlere give rabatter til kunder, der bruger disse alternative betalingsmiddeltyper.

I Microsoft Dynamics 365 Commerce kan detailhandlere konfigurere en rabatprocent, der anvendes på kvalificerede linjer, hvis kunden betaler vha. den foretrukne betalingsmiddeltype. Kunden kan beslutte, om der skal udføres en delvis betaling eller en fuld betaling, og Commerce bestemmer det relevante rabatbeløb. Bemærk, at rabatten altid gives på beløbet før moms for de kvalificerede varer.

Betalingsmiddelbaserede rabatter konkurrerer ikke med varebaserede rabatter, f.eks. periodiske eller manuelle rabatter. De er altid sammensat over varerabatterne. Selv hvis der anvendes en eksklusiv periodisk rabat på en vare, anvendes den betalingsmiddelbaserede rabat stadig oven i den eksklusive periodiske rabat. På samme måde, hvis der anvendes en rabatgrænse på transaktionen, og den betalingsmiddelbaserede rabat reducerer totalen ned under grænsen, anvendes grænserabatten stadig på transaktionen.

Selvom betalingsmiddelbaserede rabatter reducerer subtotalen for transaktionen, påvirkes automatiske gebyrer, der gælder for transaktionen, ikke. Hvis f.eks. leveringsgebyr beregnes som kr. 5, fordi subtotalen var mere end kr. 100, og den betalingsmiddelbaserede rabat reducerer beløbet, så det er mindre end kr. 100, vil leveringsgebyrerne stadig være kr. 5 for ordren.


> [!NOTE]
> Betalingsmiddelbaserede rabatter fordeles forholdsmæssigt på de kvalificerede salgslinjer og reducerer beløbet før moms for de enkelte linjers. Hvis der er konfigureret flere betalingsmiddelbaserede rabatter for en betalingsmiddeltype (f.eks. kontant), er det kun den bedste betalingsmiddelbaserede rabat, der anvendes.

Betalingsmiddelbaserede rabatter kan kun anvendes på salgslinjer, hvor priserne ikke er låst. Hvis der føjes nye salgslinjer til en ordre, anvendes den betalingsmiddelbaserede rabat kun på de nye salgslinjer under betalingen. Mens en kundeordre til afhentning eller levering placeres, anvendes den betalingsmiddelbaserede rabat kun på indbetalingsbeløbet. Når ordren er afgivet, låses priserne på salgslinjerne under opfyldelsen. Derfor anvendes der ingen betalingsmiddelbaserede rabat på en saldo, der betales under afhentning eller godkendes under forsendelse. Den betalingsmiddelbaserede rabat kan kun anvendes på hele beløbet i en kundeordre, hvis forhandleren indsamler hele beløbet som et depositum, mens ordren afgives.

> [!IMPORTANT]
> I Commerce kan betalingsmiddelbaserede rabatter i øjeblikket begrænses til to betalingstyper: kreditkort og kontant.

## <a name="pos-user-experience"></a>POS-brugeroplevelse

Hvis den betalingsmiddelbaserede rabat er konfigureret til kontanter, og kassereren på salgsstedet (POS) vælger en knap, der er knyttet til kontantbetalingsoperationen, anvendes den betalingsmiddelbaserede rabat automatisk på transaktionen. Det reducerede beløb vises derefter som saldo. Men hvis kassereren vælger knappen **Tilbage** på betalingsskærmen, fjernes rabatten, og det oprindelige beløb vises på transaktionsskærmen. Den betalingsmiddelbaserede rabat fjernes, hvis betalingslinjen er afvist.

Ved kortbetalinger kan detailhandlerne angive den betalingsbaserede rabat på en eller flere typer kreditkort. Systemet kan dog ikke bekræfte, hvilken type kreditkort der bruges, medmindre kortet er godkendt. Hvis rabatten anvendes efter godkendelse, vil betalingsgodkendelsen være for et større beløb, mens betalingsregistreringen vil være for et mindre beløb.

For at undgå denne situation, hvis en kunde betaler med et kreditkort, får kassereren vist en dialogboks med en liste over kreditkort, der giver kunden yderligere besparelser. Kassereren kan derefter spørge, om kunden ønsker at bruge et af de foretrukne kort til at opnå en ekstra rabat. Hvis kassereren bruger et foretrukket kort, anvendes den betalingsmiddelbaserede rabat på transaktionen, og det reducerede beløb vises på betalingsskærmen. Godkendelsen vil være for det reducerede beløb. Hvis kunden indsætter et kort, der er forskelligt fra det kort, som kassereren har valgt, vises en fejlmeddelelse, og godkendelsen afvises.


## <a name="call-center-user-experience"></a>Brugeroplevelse for callcenter

Når brugeren vælger **Afsluttet** under en callcenter-ordre, vises skærmbilledet **Totaler**. I første omgang omfatter totalerne på dette skærmbillede ikke betalingsmiddelbaserede rabatter, da betalingsmetoden endnu ikke er valgt. Hvis brugeren vælger den betalingsmetode, som den betalingsmiddelbaserede rabat er konfigureret for, på skærmbilledet **Tilføj betaling**, reguleres betalingsbeløbet automatisk, så det afspejler rabatbeløbet. Ligesom kunden ved POS kan callcenter-kunden bestemme, om den fulde betaling eller en delbetaling skal foretages. På basis af det beløb, der betales, anvendes den betalingsmiddelbaserede rabat på salgsordren.

> [!NOTE]
> Der udføres ikke kortvalidering af callcenterordrer. Hvis callcenter-brugeren f.eks. vælger Visa som kreditkortet, men kunden bruger MasterCard, vil systemet stadig anvende rabatten.

## <a name="exclude-items-from-discounts"></a>Udelade varer fra rabatter

Detailhandlere vælger ofte at udelukke nogle produkter, f.eks. nye varer eller eftertragtede varer, fra rabatter. Det kan dog stadig være nyttigt at anvende betalingsmiddelbaserede rabatter. En detailhandler konfigurerer f.eks. Commerce, så den ikke tillader varebaserede rabatter eller manuelle rabatter. Men hvis kunden betaler ved hjælp af det foretrukne betalingsmiddel, anvender Commerce dog stadig den betalingsmiddelbaserede rabat. Hvis du vil konfigurere Commerce på denne måde, skal du gå til **Administration af produktoplysninger > Produkter > Frigivne produkter**, vælge varen, og derefter skal du i oversigtspanelet **Commerce** angive indstillingerne **Undgå alle rabatter** og **Undgå betalingsmiddelbaserede rabatter** til **Nej** og indstillingerne **Undgå rabatter til detailforhandlere** og **Undgå manuelle rabatter** til **Ja**.

> [!NOTE]
> Når konfigurationen **Undgå alle rabatter** er angivet til **Ja**, vil der ikke blive anvendt rabatter på produktet. Der vil heller ikke blive anvendt betalingsmiddelbaserede rabatter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]