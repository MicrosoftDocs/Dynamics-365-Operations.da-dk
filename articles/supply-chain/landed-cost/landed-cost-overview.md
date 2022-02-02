---
title: Modulet Landingsomkostninger
description: Modulet Landingsomkostninger hjælper virksomheder med at strømline indgående forsendelsesoperationer ved at give brugerne fuld økonomisk og logistikstyring over importeret fragt fra producenten til lagerstedet.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e4861c0e8b3680f3cd3229facf059b671a4fc765
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983411"
---
# <a name="landed-cost-module"></a>Modulet Landingsomkostninger

[!include [banner](../../includes/banner.md)]

Modulet **Landingsomkostninger** hjælper virksomheder med at strømline indgående forsendelsesoperationer ved at give brugerne fuld økonomisk og logistikstyring over importeret fragt fra producenten til lagerstedet. For importerede varer kan landingsomkostninger udgøre 40 procent eller mere af de samlede omkostninger for hver importerede vare. Det er derfor vigtigt at levere præcise estimater af landingsomkostninger.

Virksomheder kan bruge landingsomkostninger til at udføre følgende opgaver:

- Estimere landingsomkostninger ved oprettelse af fragt.
- Fordele landingsomkostninger på flere varer og indkøbsordrer eller flytteordrer i en enkelt fragt.
- Understøtte overførsel af varer mellem fysiske lokationer ved at genkende landringsomkostninger.
- Genkende periodiseringer for varer i transit.

Landringsomkostninger giver nøjagtige og rettidige omkostningsestimater for faste landingsomkostninger. Samtidig giver det øget økonomisk og logistisk synlighed af den udvidede forsyningskæde. Det er også med til at reducere administrationen af efterkalkulation og efterkalkulationsfejl.

## <a name="highlights"></a>Højdepunkter

### <a name="voyages"></a>Fragter

I landingsomkostninger er en fragt en særskilt flytning fra en udgående lokation via et bestemt sæt destinationer i en bestemt periode til en angivet indgående lagerstedslokation. Indkøbsordrer og ordrelinjer kan føjes til enten en enkelt container eller flere containere for en fragt, og omkostningerne fordeles korrekt tilbage til varelinjen. Ordrer og ordrelinjer kan også tilføjes på tværs af juridiske enheder for en enkelt fragt.

### <a name="item-ownership"></a>Vareejerskab

I Microsoft Dynamics 365 Supply Chain Management modtages varer typisk på lagerstedets destination og faktureres derefter. Men i henhold til de fleste internationale samhandelsaftaler tager et firma dog ejerskab over varer fra det tidspunkt, hvor de forlader den oprindelige havn, inden de fysisk er modtaget. Landingsomkostninger sætter virksomheder i stand til at fakturere varer, før de fysisk er modtaget. Dette begreb kaldes varer i transitordre. Der oprettes en ny ordretype til styring af varemodtagelsen, når den oprindelige indkøbsordre er faktureret.

### <a name="costs"></a>Omkostninger

Når du opretter en fragt i landingsomkostninger, kan der automatisk føjes omkostninger til den. Disse omkostninger konfigureres i Landingsomkostninger, og der findes forskellige omkostningsindstillinger og omkostningsgrundlag for dem. Hver omkostning kan konfigureres for forskellige niveauer af en fragt og fordeles til vareniveau via fordelingsregler, der understøtter antal, volumen, vægt, beløb og definerede volumendivisorer. Disse forkalkulerede omkostninger giver et nøjagtigt estimat af alle omkostninger for en fragt.

Landingsomkostninger kører derefter en foreløbig bogføring/periodisering af de forkalkulerede landingsomkostninger for at sikre, at der findes en præcis beregning af de forkalkulerede omkostninger ved oprettelsen af fragten. Når disse automatiske omkostninger faktureres, tilbageføres og erstattes de forkalkulerede omkostninger af de faktiske omkostninger baseret på omkostningsfakturaer.

Faktiske omkostninger er tilbageførte forkalkulerede omkostninger, der bogføres på tidspunktet for fakturering af omkostninger ved hjælp af clearingkonti, der er oprettet for hver omkostningstype (f.eks. told, fragt og forsikring). Disse bogføringer følger den bogføringsmåde, der er knyttet til den specifikke vare. Lagerbogføring opdateres automatisk, uanset om bogføringstypen først ind, først ud (FIFO), sidst ind, først ud (LIFO), flytning af vægtet gennemsnit eller glidende gennemsnit. Alle bogføringstyper for lagermodelgruppen understøttes. I forbindelse med bogføring af glidende gennemsnit og standardkostpris er der tilgængelige konti til afvigelse i indkøbspris til bogføring af forskelle mellem forkalkulerede omkostninger og faktiske omkostninger.

### <a name="item-and-order-tracking"></a>Sporing af varer og ordrer

Efterhånden som fragten flyttes fra den oprindelige udgående lokation til det endelige destinationslagersted, kan brugerne opdatere hvert trin, eller *etape*, af dens rejse efter behov. For hver etape identificeres en leveringstid og en forsendelsesstatus. Bekræftede leveringsdatoer for flytning til den næste etape af rejsen identificeres også. Tilsammen udgør disse leveringsdatoer en forventet leveringsdato for varerne til det indgående lagersted. Brugerne kan ændre disse leveringsdatoer. I dette tilfælde opdateres den forventede leveringsdato for varerne derefter automatisk på baggrund af leveringstiderne og rejsens etaper. Synligheden af varer i transit efter fragt og fartøj er tilgængelig på containerbasis, før varerne modtages. Da datoerne opdateres på de enkelte indkøbsordrelinjer, har virksomheder mere styring med logistik og lagerstedsplanlægningen.

## <a name="landed-cost-concepts"></a>Begreber for landingsomkostninger

Følgende tabel indeholder en opsummering af nogle kernebegreber for landingsomkostninger.

| Koncept | Beskrivelse |
|---|---|
| Fragt | En fragt er typisk ét fartøj. Afhængigt af dine fremgangsmåder og procedurer kan det dog være én leverandør eller én indkøbsordre. Der er ingen begrænsninger for brugen af dette begreb. |
| Folio | En folio bestemmes ofte af toldlovgivningen. Den kan bestå af en leverandørs varer for én enhed/ét firma pr. forsendelse. Varerne i en folio kan være i én container eller fordelt på flere containere. |
| Forsendelsescontainer | Forsendelsescontainere indeholder indkøbsordrelinjer. De er et niveau under forsendelsesniveauet. De bruges typisk, hvis omkostningerne er fordelt på varer pr. container, eller hvis der modtages pr. container. |
| Forsendelsescontainertype | Forsendelsescontainertyper kan bestemme prisen for en omkostningstype (f.eks. fragt). De giver også nyttige forsendelsesoplysninger. |
| Omkostningstype | Omkostningstyper identificerer omkostninger, der er knyttet til import, f.eks. told, fragt og forsikring. |
| Automatisk omkostning | Automatiske omkostninger fungerer på samme måde som samhandelsaftaler. En automatisk omkostning er knyttet til et fragtniveau. |
| Havn | Havne er områder, hvor der modtages og afsendes varer. |
| Fartøj | Et fartøj er det medie, der bruges til at transportere varer, f.eks. et skib eller et fly. |
| Varer i transit | Afhængigt af indstillingerne overføres varer til et lagersted i transit, når en faktura opdateres. |
| Aktivitet | Aktiviteterne kan bruges til at gemme hvert af de vigtige trin i rejsen mellem to havne. De kan bruges til opdatering af datoer. |
| Rejseskabelon | Rejseskabeloner er ruter, som varer følger mellem to havne. |

Du kan sammenligne terminologierne og funktionerne i modulerne **Landingsomkostninger** og **Transportstyring** (TMS) i [Landingsomkostninger sammenlignet med Transportstyring](landed-cost-vs-tms.md).
