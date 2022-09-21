---
title: Kontrolelement til arbejderoverskrift
description: Denne artikel indeholder oplysninger om den header-kontrol, der kan tilpasses i Medarbejder selvbetjening, i Personben, og på siden Arbejder i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2867a952df79161aaee657dbc3df1f3298294dd5
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445943"
---
# <a name="worker-header-control"></a>Kontrolelement til arbejderoverskrift

Microsoft Dynamics 365 Human Resources indeholder oplysninger om den hovedkontrol, der kan tilpasses, i **Medarbejderselvbetjening**, i hubben **Personer**, og på den strømlinede side **Arbejder**. Overskriften indeholder nøgleoplysninger om arbejderen og handlinger med et enkelt klik, f.eks. e-mail, opkald eller meddelelse. Hovedet kan redigeres ved at fjerne felter eller tilføje felter, inklusive brugerdefinerede felter, for at få vist yderligere oplysninger. Hvis du vil bruge den nye hovedkontrol, skal du gå til **Funktionsstyring** og aktivere funktionen **overskriftskontrol for arbejder**.

## <a name="personalization"></a>Brugertilpasning

En af de vigtigste fordele ved arbejderens hovedkontrol er muligheden for at personalisere oplysninger, der vises i overskriften.

I øverste højre hjørne af hovedet er en gruppe på tre felter, der viser forskellige data, afhængigt af medarbejderens status. Denne gruppe af felter kaldes headerens Spotlight-del. Du kan personalisere Spotlight-delen af headeren ved at fjerne de aktuelle felter eller tilføje felter. De felter, der kan føjes til sidefoden i sidehovedet, er forskellige for **Medarbejderselvbetjening**, hubben **Personer** og siden **Arbejder**.

## <a name="employee-self-service"></a>Medarbejderselvbetjening

Headeren til arbejderen på siden **Medarbejderselvbetjening** indeholder følgende oplysninger:

- Arbejderens navn
- Personalenummer
- Stillingens titel
- Afdelinger
- Arbejdertype
- Juridiske enheds ansættelse
- Antal års tjeneste
- Rapporter til (leder)
- Stillingstype

Overskriften indeholder også en handling med et enkelt klik til redigering af personens personlige oplysninger. Vælg **Rediger personlige oplysninger** for at åbne siden **Personlige oplysninger** i **Medarbejderselvbetjening**.

## <a name="people-hub"></a>Personhub

Arbejder-header i **People**-hub (siden **Personer på arbejdsområdet**) indeholder følgende oplysninger:

- Arbejderens navn
- Personalenummer
- Stillingens titel
- Afdelinger
- Arbejdertype
- Juridiske enheds ansættelse
- Antal års tjeneste
- Rapporter til (leder)
- Stillingstype

Headeren indeholder også enkeltklikhandlinger, f.eks. e-mail, opkald eller onlinemeddelelse. Hvis en bruger får vist deres egne oplysninger på siden **arbejdsområdet for personer**, indeholder handlingssektionen **Rediger personlige oplysninger** med ét klik. Brugeren kan vælge denne knap for at åbne siden **Personlige oplysninger** i **Medarbejderselvbetjening**.

## <a name="streamlined-worker-page"></a>Siden Strømlinet arbejder

Headeren til arbejderen på siden **Strømlinet arbejder** indeholder følgende oplysninger:

- Arbejderens navn
- Personalenummer
- Stillingens titel
- Afdelinger
- Arbejdertype
- Juridiske enheds ansættelse

Afhængigt af medarbejderens status kan oplysningerne i hovedet ændres. Hvis medarbejderen f.eks. har forladt firmaet, indeholder header-kontrolelement et **Afsluttet** badge, slutdatoen for ansættelsen og årsagen til fratrædelse.

I tabellen nedenfor vises de data, der vises i overskriften til forskellige medarbejderstatusser.

| Medarbejderstatus | Det viste data | Note |
|-----------------|--------------------|------|
| Udestående | <ul><li>Name</li><li>Personalenummer</li><li>Stillingens titel</li><li>Afdeling</li><li>Arbejdertype</li><li>Juridisk enhed</li><li>Ventende kort</li><li>Igangsæt dato</li><li>Rapporterer til</li><li>Stillingstype</li></ul> | |
| Seneste ansættelse | <ul><li>Name</li><li>Personalenummer</li><li>Stillingens titel</li><li>Afdeling</li><li>Arbejdertype</li><li>Juridisk enhed</li><li>Seneste ansættelsesbadge</li><li>Antal års tjeneste</li><li>Rapporterer til</li><li>Stillingstype</li></ul> | Det seneste **Ansættelses-badge** vises som standard for medarbejdere, der er blevet ansat i løbet af de seneste syv dage. Hvis du vil ændre denne indstilling, skal du angive en tidsramme i feltet **Nye ansættelser i datoorden** på siden **Human Resources-parametre** under fanen **Generelt**. Hvis du for eksempel vil have vist **Seneste ansættelse**-listen over medarbejdere, der er ansat inden for de seneste 14 dage, skal du angive feltet **Periode** til **14** og feltet **Unit** til **Dage**. |
| Aktiv medarbejder | <ul><li>Name</li><li>Personalenummer</li><li>Stillingens titel</li><li>Afdeling</li><li>Arbejdertype</li><li>Juridisk enhed</li><li>Igangsæt dato</li><li>Rapporterer til</li><li>Stillingstype</li></ul> | |
| Fratræder | <ul><li>Name</li><li>Personalenummer</li><li>Stillingens titel</li><li>Afdeling</li><li>Arbejdertype</li><li>Juridisk enhed</li><li>Afslutter badge</li><li>Antal års tjeneste</li><li>Rapporterer til</li><li>Stillingstype</li></ul> | Som standard vises **Afsluttende** badge for medarbejdere, der forlader stedet inden for de næste syv dage. Hvis du vil ændre denne indstilling, skal du angive en tidsramme i feltet **Afsluttende arbejder, datorækkefølge** på siden **Human Resources-parametre** under fanen **Generelt**. Hvis du for eksempel vil have vist **Afsluttende**-listen over medarbejdere, der afslutter inden for de næste 14 dage, skal du angive feltet **Periode** til **14** og feltet **Enhed** til **Dage**. |
| Fratrådte | <ul><li>Afsluttet badge</li><li>Personalenummer</li><li>Slutdato for ansættelse</li><li>Årsagskode</li></ul> | Som standard vises **Afsluttet** badge for medarbejdere, der har forladt stedet inden for de sidste syv dage. Hvis du vil ændre denne indstilling, skal du angive en tidsramme i feltet **Afsluttet arbejder, datorækkefølge** på siden **Human Resources-parametre** under fanen **Generelt**. Hvis du for eksempel vil have vist **Afsluttet**-listen over medarbejdere, der har afsluttet inden for de sidste 14 dage, skal du angive feltet **Periode** til **14** og feltet **Enhed** til **Dage**. |
