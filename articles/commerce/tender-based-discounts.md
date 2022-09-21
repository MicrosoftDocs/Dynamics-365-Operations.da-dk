---
title: Betalingsmiddelbaserede rabatter
description: Denne artikel beskriver tilbudsbaseret rabatfunktionalitet, som detailhandlere kan bruge til at konfigurere rabatter for bestemte betalingsmiddeltyper i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/19/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: b11145c0c12f973b437ebf87921a5686d217d327
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473774"
---
# <a name="tender-based-discount"></a>Betalingsmiddelbaseret rabat

[!include [banner](includes/banner.md)]

Denne artikel beskriver tilbudsbaseret rabatfunktionalitet, som detailhandlere kan bruge til at konfigurere rabatter for bestemte betalingsmiddeltyper i Microsoft Dynamics 365 Commerce.

Det er en almindelig praksis blandt detailhandlere at udstede egne, brandede kreditkort. Detailhandlerne får fordel af de foretrukne satser fra bankerne. Da disse kreditkort også kan give opmuntre kunderne til at besøge butikken flere gange, er de også med til at forbedre forhandlerens bundlinje. Derfor har detailhandlere et incitament til at øge kundernes anvendelse af deres brandede kreditkort. For at nå dette mål giver de ofte ekstra rabatter til kunder, der bruger disse kreditkort.

Det kan også være, at forhandlere, der ikke tilbyder brandede kreditkort, vil opmuntre kunderne til at betale med andre betalingsmiddeltyper, f.eks. kontant, gavekort eller fordelskundepoint. På denne måde kan de hjælpe med at reducere udgiften af gebyrer til behandling af kreditkort. Derfor kan detailhandlere give rabatter til kunder, der bruger disse alternative betalingsmiddeltyper.

## <a name="tender-based-discount"></a>Betalingsmiddelbaseret rabat

Commerce understøtter en *betalingsmiddelbaseret rabat*, der giver detailforretningerne mulighed for at konfigurere en rabatprocent, der anvendes på en transaktion, hvis totalen for transaktionen overstiger et bestemt beløb, og kunden betaler ved hjælp af den foretrukne betalingstype. Den betalingsmiddelbaserede rabat er lagbaseret, så der kan knyttes forskellige rabatprocenter til forskellige beløbsgrænser. Kunden kan beslutte, om der skal udføres en delvis betaling eller en fuld betaling, og prisfastsættelsesmaskinen bestemmer det relevante rabatbeløb. Den betalingsmiddelbaserede rabat gives altid på salgslinjernes momsbeløb.

Betalingsmiddelbaseret rabat fordeles forholdsmæssigt på de kvalificerede salgslinjer, når priserne ikke låses og reducerer beløbet før moms for de enkelte linjer. Hvis der føjes nye salgslinjer til en ordre, anvendes den betalingsmiddelbaserede rabat kun på de nye salgslinjer under betalingen. Når en kundeordre til afhentning eller levering placeres, anvendes den betalingsmiddelbaserede rabat kun på indbetalingsbeløbet. Når ordren er afgivet, låses priserne på salgslinjerne under opfyldelsen. Ingen betalingsmiddelbaserede rabat på en saldo, der betales under afhentning eller godkendes under forsendelse. Den betalingsmiddelbaserede rabat kan kun anvendes på hele beløbet i en kundeordre, hvis forhandleren indsamler hele beløbet som et depositum, mens ordren afgives.

Betalingsmiddelbaserede rabatter konkurrerer ikke med varebaserede rabatter som f.eks. simple rabatter, antalsrabatter, grænserabatter, miks- og matchrabatter og manuelle rabatter. Betalingsmiddelbaserede rabatter sammensat altid over varebaserede rabatter. Selv hvis der anvendes en eksklusiv periodisk rabat på en vare, anvendes den betalingsmiddelbaserede rabat stadig oven i den eksklusive rabat. På samme måde, hvis der anvendes en rabatgrænse på transaktionen, og den betalingsmiddelbaserede rabat reducerer totalen ned under grænsen, anvendes grænserabatten stadig på transaktionen.

Selvom betalingsmiddelbaserede rabatter reducerer subtotalen for transaktionen, påvirkes automatiske gebyrer, der gælder for transaktionen, ikke. Hvis f.eks. leveringsgebyr beregnes som kr. 5, fordi subtotalen var mere end kr. 100, og den betalingsmiddelbaserede rabat reducerer beløbet, så det er mindre end kr. 100, vil leveringsgebyrerne stadig være kr. 5 for ordren.

Den betalingsmiddelbaserede rabat begrænses i øjeblikket til to betalingstyper: kreditkort og kontant. Hvis der er konfigureret flere betalingsmiddelbaserede rabatter for en betalingstype (f.eks. kontant), er det kun den bedste betalingsmiddelbaserede rabat, der anvendes.

## <a name="pos-user-experience"></a>POS-brugeroplevelse

Hvis den betalingsmiddelbaserede rabat er konfigureret til kontanter, og kassereren på salgsstedet (POS) vælger en knap **Kontantbetaling** til at håndtere en cash and carry-transaktion, anvendes den betalingsmiddelbaserede rabat automatisk på transaktionen. Det reducerede beløb vises derefter som saldo. Men hvis kassereren vælger knappen **Tilbage** på betalingsskærmen, fjernes rabatten, og det oprindelige beløb vises på transaktionsskærmen. Den betalingsmiddelbaserede rabat fjernes, hvis betalingslinjen er afvist.

Ved kreditkortbetalinger kan detailhandlerne angive den betalingsbaserede rabat på en eller flere typer kreditkort. Systemet kan dog ikke bekræfte, hvilken type kreditkort der bruges, medmindre kortet er godkendt. Hvis rabatten anvendes efter godkendelse, vil betalingsgodkendelsen være for et større beløb, mens betalingsregistreringen vil være for et mindre beløb. For at undgå denne situation, hvis en kunde betaler med et kreditkort, får kassereren vist en dialogboks med en liste over foretrukne kreditkort, der giver kunden yderligere besparelser. Kassereren kan derefter spørge, om kunden ønsker at bruge et af de foretrukne kort til at opnå en ekstra rabat. Hvis kassereren vælger et foretrukket kort, anvendes den betalingsmiddelbaserede rabat på transaktionen, og det reducerede beløb vises på betalingsskærmen. Godkendelsen vil være for det reducerede beløb. Hvis kunden indsætter et kort, der er forskelligt fra det kort, som kassereren har valgt, vises en fejlmeddelelse, og godkendelsen afvises.

## <a name="call-center-user-experience"></a>Brugeroplevelse for callcenter

Hvis en callcenter-bruger vælger **Afsluttet** under en callcenter-ordre, vises skærmbilledet **Totaler**. I første omgang omfatter totalerne på dette skærmbillede ikke betalingsmiddelbaserede rabatter, da betalingsmetoden endnu ikke er valgt. Hvis brugeren vælger den betalingsmetode, som den betalingsmiddelbaserede rabat er konfigureret for, på skærmbilledet **Tilføj betaling**, reguleres betalingsbeløbet automatisk, så det afspejler rabatbeløbet. Ligesom en kunde ved POS kan callcenter-kunden bestemme, om den fulde betaling eller en delbetaling skal foretages. På basis af det beløb, der betales, anvendes den betalingsmiddelbaserede rabat på salgsordren.

> [!NOTE]
> Der udføres ikke kortvalidering af callcenterordrer. Hvis callcenter-brugeren f.eks. vælger Visa som kreditkortet, men kunden bruger MasterCard, vil systemet stadig anvende rabatten.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
