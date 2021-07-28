---
title: Momsoversigt
description: Dette emne indeholder en oversigt over momssystemet. Det forklarer elementerne i moms, og hvordan de fungerer sammen.
author: ShylaThompson
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12e776a83e00c669984a278ab06b913743d6e544
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348932"
---
# <a name="sales-tax-overview"></a>Momsoversigt

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over momssystemet. Det forklarer elementerne i moms, og hvordan de fungerer sammen.

## <a name="overview"></a>Overblik

Momsstrukturen understøtter mange typer af indirekte skatter, som f.eks. moms, moms af varer og ydelser (GST), stykbaseret gebyrer og indeholdt skat. Disse skatter beregnes og dokumenteres under indkøbs- og salgstransaktioner. Med jævne mellemrum skal de rapporteres og betales til skattemyndighederne. 

I følgende diagram vises enheder på opsætning af skat, og hvordan de er relateret.

[![Diagram, der viser oversigt over enheder til momsopsætning.](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

For hver type moms, en virksomhed skal redegøre for, skal der defineres en momskode. En momskode gemmer afgiftssatser og reglerne for beregning af moms. 

Hver momskode skal være knyttet til en momsafregningsperiode. Momsafregningsperioder definerer de intervaller, hvorved moms skal rapporteres og betales til momsmyndighederne. Hver momsafregningsperiode skal være knyttet til en momsmyndighed. En momsmyndighed repræsenterer den enhed, som moms rapporteres og betales til. Den definerer også momsrapportens layout. Skattemyndighederne kan være relateret til kreditorkonti. Du kan finde flere oplysninger i [Konfigurere momsafregningsperioder](tasks/set-up-sales-tax-settlement-periods.md).

Hver momskode skal også være knyttet til en finanskonteringsgruppe. En finanskonteringsgruppe angiver de hovedkonti, som beløb for momskoderne bogføres til. 

Du kan også definere valgfri momsrapporteringskoder. Disse kan tildeles på momskoder for de forskellige beløb, der beregnes til momskoden. Rapporten **Momsbetaling efter kode** viser totaler pr. momsrapporteringskode for en bestemt momsafregningsperiode og et bestemt interval. 

Hver transaktion, som momsen skal beregnes og bogføres til, skal have en momsgruppe og en varemomsgruppe. Momsgrupper er relateret til parten (f.eks., debitor eller kreditor) for transaktionen, hvorimod varemomsgrupper er relateret til ressourcen (f.eks, vare- eller indkøbskategori) for transaktionen. Momsgrupper indeholder en liste over momskoder. De momskoder, der findes i både momsgruppen og varemomsgruppen for en transaktion, er den momskode, der gælder for den pågældende transaktion. 

I følgende tabel beskrives enheder og sekvensen for opsætningen af skat.

| Opsætningsopgave                                                  | Krævet/Valgfri og beskrivelse                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opret hovedkonti.                                           | Påkrævet. Før du kan konfigurere momsfunktionen, skal de hovedkonti, firmaet bruger til at betale og registrere skatter, være oprettet.                                                                                                                                                                             |
| Oprette finanskonteringsgrupper til moms.                     | Påkrævet. Finanskonteringsgrupperne definerer hovedkontiene for registrering og betaling af moms.   Du kan finde flere oplysninger i [Opsætning af finanskonteringsgrupper til moms](tasks/set-up-ledger-posting-groups-sales-tax.md).                                                                                 |
| Opret momsmyndigheder.                                   | Påkrævet. Momsmyndighederne er de enheder, som moms skal rapporteres og betales til.    Du kan finde flere oplysninger i [Opsætte momsmyndigheder](tasks/set-up-sales-tax-authorities.md).                                                                                                                                          |
| Opret momsafregningsperioder.                            | Påkrævet. Momsafregningsperioder indeholder oplysninger om, hvornår og hvor ofte momsen skal rapporteres og betales. De er relateret til en momsmyndighed.                                                                                                                                                       |
| Konfigurer momsrapporteringskoder.                               | Valgfrit. Momsrapporteringskoder kan tildeles til momskoder til rapportbeløbene for flere momskoder i én momsrapporteringskode. Du kan finde flere oplysninger i [Konfigurere momsrapporteringskoder](tasks/set-up-sales-tax-reporting-codes.md).                                         |
| Opret momskoder.                                         | Påkrævet. Momskoder indeholder afgiftssatserne og reglerne for beregning af hver type moms. Momskoder er relateret til en momsudligningsperiode og en finanskonteringsgruppe. Du kan finde flere oplysninger i [Konfigurere momskoder](tasks/set-up-sales-tax-codes.md).                                |
| Konfigurer momsgrupper.                                        | Påkrævet. Momsgrupper indeholder en liste over de salgskoder, der gælder for parten (debitor eller kreditor) for en transaktion. For en bestemt transaktion vil skæringspunktet mellem momskoden i momsgruppen og varemomsgruppen fastlægge de momskoder, der skal anvendes i den pågældende transaktion.                  |
| Konfigurer varemomsgrupper.                                   | Påkrævet. Varemomsgrupper indeholder en liste over de salgskoder, der gælder for ressourcen (produkt, service osv.) af en transaktion. For en bestemt transaktion vil skæringspunktet mellem momskoden i momsgruppen og varemomsgruppen fastlægge de momskoder, der skal anvendes i den pågældende transaktion. Du kan finde flere oplysninger under [Konfigurere momsgrupper og varemomsgrupper](tasks/set-up-sales-tax-groups-item-sales-tax-groups.md). |
| Konfigurer parametre for moms på siderne med programparametre. | Påkrævet. Forskellige områder som Finans, debitor og kreditor skal angive parametre for korrekt beregning af de indirekte skatter. Selvom de fleste af disse parametre har standardværdier, skal de ændres for at tilpasses hver enkelt virksomheds krav.                                          |

## <a name="sales-tax-on-transactions"></a>Moms på transaktioner
For hver transaktion (salgs-/indkøbsdokumentlinjer, kladder osv.) skal du angive en momsgruppe og en varemomsgruppe for at beregne moms. Standardgrupper angives i masterdata (for eksempel debitor, kreditor, vare og indkøbskategori), men du kan ændre grupper på en transaktion manuelt, hvis det er nødvendigt. Begge grupper indeholder en liste over momskoder, og skæringspunktet mellem de to lister over momskoder bestemmer listen over relevante momskoder for posteringen. 

For hver transaktion kan du slå den beregnede moms op ved at åbne siden **Momspostering**. Du kan søge efter moms for en dokumentlinje eller hele dokumentet. Du kan justere den beregnede moms for visse dokumenter (f.eks kreditorfakturaen og finanskladder), hvis det oprindelige dokument viser beløb, der afviger.

## <a name="sales-tax-settlement-and-reporting"></a>Udligning og rapportering af moms
Momsen skal rapporteres og betales til momsmyndighederne i regulerede intervaller (månedlig, kvartalsvis, og så videre). Du kan afregne momskonti for intervallet og forskyde saldi til momsafregningskontoen, som angivet i finanskonteringsgrupperne. Du kan få adgang til denne funktion på siden **Afregn og bogfør moms**. Du skal angive den momsafregningsperiode, der skal afregnes moms for. 

Når momsen er blevet betalt, bør saldoen på momsafregningskontoen opvejes mod bankkontoen. Hvis den momsmyndighed, der er angivet i momsafregningsperioden, er relateret til en kreditorkonto, bogføres momssaldoen som en åben kreditorfaktura og kan tages med i det regelmæssige betalingsforslag.

## <a name="conditional-sales-tax"></a>Betinget moms
Betinget moms er en moms, der betales proportionalt med det faktiske beløb, der betales på en faktura. Derimod beregnes standardmoms på faktureringstidspunktet. Betinget moms skal betales til skattemyndighederne, når betalingen bogføres, ikke når fakturaen bogføres. Når fakturaen bogføres, skal posteringen registreres i momsrapporten. Dog skal posteringen udelades fra momsafregningsrapporten. 

Hvis du markerer afkrydsningsfeltet Betinget moms i formularen Finansparametre, kan der ikke fratrækkes moms, før du har betalt fakturaen. Dette er et lovkrav i visse lande/områder.

> [!NOTE]
> Når du markerer afkrydsningsfeltet Betinget moms, skal du konfigurere momskoder og momsgrupper samt oprette finanskonteringsgrupper til understøttelse af funktionaliteten. |

###  <a name="example"></a>Eksempel

Du afregner moms hver måned. Den 15. juni opretter du en debitorfaktura på EUR 10.000 plus moms.
-   Momsen er på 25 % eller kr. 25,00.
-   Fakturabetalingen forfalder den 30. juli.

Normalt skal du afregne og betale 2.500 til skattemyndighederne, når fakturaen bogføres i juni, selvom du ikke har modtaget betalingen fra debitor. 

Hvis du imidlertid bruger en betinget moms, afregner du med skattemyndighederne, når du modtager betalingen fra debitor den 30. juli.

### <a name="postdated-check"></a>Fremdateret check

Hvis du bruger fremdateret check som betalingsmåde, når betalingen oprettes, cleares bankkontoen ikke. I nogle lande/områder vil moms blive 'realiseret' passiv, når betalingen cleares i banken, hvilket betyder, at den fremdaterede check udlignes. Du kan aktivere den ved at vælge **Realiserer den betingede moms, når der trækkes fremdaterede checks** i **Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre > fremdaterede checks**

Du kan finde flere oplysninger i [Konfigurere A-skat](tasks/set-up-withholding-tax.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]