---
title: Oversigt over forudsætninger for standardomkostninger
description: Denne artikel beskriver de grundlæggende trin til brug af standardomkostninger.
author: JennySong-SH
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf02653b1d1a2cf5ed45f0fc6bd9affe098e7396
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895780"
---
# <a name="prerequisites-for-standard-costs-overview"></a>Oversigt over forudsætninger for standardomkostninger

[!include [banner](../includes/banner.md)]

Denne artikel beskriver de grundlæggende trin til brug af standardomkostninger. Efterfølgende trin afhænger af virksomhedens aktiviteter. Trinene er f.eks. forskellige i et ikke-produktionsmiljø, et produktionsmiljø, der ikke bruger ruter, eller et produktionsmiljø, der bruges ruter. 

Benyt følgende fremgangsmåde for at konfigurere standardomkostninger.

**1. Opret en varemodelgruppe for standardomkostninger.**

Brug siden **Varemodelgrupper** til at oprette en ny gruppe for standardomkostninger, og tildel en lagermodel med **Standardomkostning**. Identifikationen for varemodelgruppen skal give mening, f.eks. **Std.omk**. Markér afkrydsningsfelterne for at angive, at økonomisk negativ lagerbeholdning skal være tilladt for gruppen, at der skal bogføres fysisk og økonomisk lager. Varer tildeles denne standardkostgruppe.

**2. Definer finanskonti, der vedrører standardomkostningsafvigelser.** 

Brug siden **Kontoplan** til at definere finanskonti, der er knyttet til standardomkostningsafvigelser. Disse finanskonti skal defineres, før de kan tildeles på siden **Bogføring**. Finanskontiene kan afspejle varegrupper og omkostningsgrupper.

**3. Tildel finanskonti til varebogføringer, der er knyttet til standardomkostningsafvigelser.** 

Brug siden **Bogføring** til at tildele de finanskonti, der er knyttet til standardomkostningsafvigelser. Du kan angive en finanskonto for afvigelser for de enkelte varer (eller varegrupper) og for de enkelte omkostningsgrupper (eller omkostningsgruppetyper), eller du kan angive, at finanskontoen gælder for alle varer og alle omkostningsgrupper. Disse indstillinger svarer til omkostningsrelationer for tabeller, grupper og alle. 

Før du definerer reglerne for varekontering, skal du bruge siden **Transaktionskombinationer** til at aktivere omkostningsrelationer (for tabeller, grupper og alle).

**4. Definer lagerparametre, der er knyttet til standardomkostninger.** 

-  Brug fanen **Lagerregnskab** på siden **Konfiguration af regnskabspolitik for lager > Parametre** til at definere to parametre for omkostningsstyring, der er knyttet til standardomkostninger.

    -  I feltet **Kostprisopdeling** skal du vælge **Ingen** eller **Underfinanskonto**. Hvis du vælger **Underfinanskonto**, er kostprisopdelingen en *aktiv* kostprisopdeling. En aktiv kostprisopdeling er vigtig for beregning, bevarelse og visning af segmentering af omkostningsgrupper på tværs af en produktstruktur med flere niveauer for standardomkostningsvarer. Når kostprisopdelingen er aktiv, kan du rapportere og analysere lager, IGVA (igangværende arbejde) og vareforbrug for de enkelte omkostningsgrupper på et enkelt niveau, flere niveauer eller i det samlede format. Når kostprisopdelingen er aktiv, og du aktiverer omkostninger for en produceret vare, lagres segmenteringen af omkostningsgruppen i varens kostprispost. 

    -  Hvis du vælger **Ingen**, vedligeholdes kostgruppesegmenteringen ikke for varer med standardkostpriser. Med andre ord beregnes og vedligeholdes en produceret vares standardkostpris som et enkelt beløb uden segmentering af omkostningsgrupper. Kostbidraget for producerede komponenter samles i dette enkeltbeløb.

-  I feltet **Afvigelser fra standard** skal du vælge **Opsummeret** eller **Pr. kostgruppe**. Hvis du vælger **Pr. kostgruppe**, kan du identificere afvigelser i indkøbsprisen og produktionsafvigelser pr. omkostningsgruppe. Du kan også identificere de fire typer produktionsafvigelser: afvigelse i partistørrelse, antal, pris og erstatning. Hvis du vælger **Opsummeret**, kan du ikke identificere afgivelser for de enkelte omkostningsgrupper, og du kan ikke identificere de fire typer produktionsafvigelser. Du kan kun se en opsummeret produktionsafvigelse.

-  Reglerne for afvigelser fra standarden fungerer uafhængigt af reglerne for kostprisopdeling. Du kan med andre ord vælge en regel for kostprisopdeling som **Ingen** og vælge afvigelser for de enkelte omkostningsgrupper, så du stadig kan registrere produktionsafvigelser for de enkelte omkostningsgrupper.

**5. Opret efterkalkulationsversioner for standardomkostninger.** 

Brug siden **Opsætning af efterkalkulationsversion** til at oprette en eller flere omkostningsversioner for standardomkostninger. De enkelte omkostningsversioner skal oprettes med omkostningstypen **Standardomkostninger** og skal tillade, at der må være omkostningsoplysninger i indholdet.

**6. Konfigurer en eksisterende kunde til at bruge standardomkostninger.** 

Kunder, der vil ændre deres eksisterende varer til en lagermodel med standardomkostninger, skal bruge siden **Standardomkostningskonverteringer**.


## <a name="related-articles"></a>Relaterede artikler

[Oversigt over standardomkostningskonvertering](standard-cost-conversion-overview.md)

### <a name="blogs"></a>Blogs

#### <a name="community-blogs"></a>Fællesskabsblogge

- [Sådan opsættes standardomkostninger for direkte materialer i Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [Direkte standardlønomkostninger i Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]