---
title: Forespørgsel på Schedule of Expenditures of Federal Awards
description: Dette emne giver oplysninger om forespørgslen Schedule of Expenditures of Federal Awards.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-alpavk
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 0b4228a9592efb54714186fc6b36276e915dc122
ms.sourcegitcommit: be51e892003778e71b67fb409a8e16965c89b5ac
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/23/2020
ms.locfileid: "3618451"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Forespørgsel på Schedule of Expenditures of Federal Awards

[!include [banner](../includes/banner.md)]

Ifølge Office of Management og Budget Circular A-133 vil de agenturer, der modtager føderale midler, være underlagt revisionskrav, som også kaldes separate revisioner. Revisionsprocessen anvendes til at rapportere om indtægter og udgifter for føderale tilskud på tilbagevendende basis. En del af den separate revisionsrapport omfatter Schedule of Expenditures of Federal Awards (SEFA).

Forespørgslen Schedule of Expenditures of Federal Awards (SEFA) omfatter Catalog of Federal Domestic Assistance (CFDA) titel og nummer, tilskudsnummeret, tilskudsåret, navnet på den føderale myndighed, der udleverer midlerne, samt navnet på pass-through-enheden. Forespørgslen gælder for en bestemt periode. Denne periode er typisk den samme som regnskabsperioden, som er et regnskabsår.

Forespørgslen omfatter tilskud, der har projektionsdatoer i det valgte datointerval. I forespørgselskolonnen **Udstederagentur** vises tilskudskunden eller udstederagenturet for et pass-through-tilskud. I forbindelse med et pass-through-tilskud viser kolonnen **Pass-through-agentur** tilskudskunden. Hvis det ikke er et pass-through-tilskud, er kolonnen **Pass-through-agentur** tom.

## <a name="set-up-the-cfda-clusters"></a>Konfigurere CFDA-klynger

Du skal konfigurere de CFDA klynger, der kan knyttes til CFDA-numre i forespørgslen Schedule of Expenditures of Federal Awards.

1. Gå til **Projektstyring og regnskab \> Konfiguration \> Tilskud \> Catalog of Federal Domestic Assistance-klynger**.
2. Vælg **Ny** for at oprette en CFDA-klynge.
3. Angiv klyngens navn.
4. Vælg **Gem** for at gemme ændringerne.

## <a name="set-up-cfda-numbers"></a>Oprette CFDA-numre

Du skal konfigurere de CFDA-numre, der kan føjes til tiskud og medtages i forespørgslen Schedule of Expenditures of Federal Awards.

1. Gå til **Projektstyring og regnskab \> Konfiguration \> Tilskud \> Catalog of Federal Domestic Assistance-numre**.
2. Vælg **Nyt** for at oprette et CFDA-nummer.
3. Angiv CFDA-nummeret i feltet **Nummer**.
4. Tryk på **tabulatortasten**.
5. Angiv CFDA-titlen i feltet **Beskrivelse**.
6. Tryk på **tabulatortasten**.
7. Valgfrit: Tilføj den relevante CFDA-klynge i feltet **Programklynge**.
8. Vælg **Gem** for at gemme ændringerne.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Konfigurere tilskud der skal indberettes for Schedule of Expenditures of Federal Awards-forespørgsel

1. Gå til **Projektstyring og regnskab \> Tilskud \> Tilskud**, og vælg et eksisterende tilskud.
2. Tildel CFDA nummeret i feltet **Catalog of Federal Domestic Assistance** i oversigtspanelet **Konfiguration**. CFDA nummeret på tilskuddet bestemmer CFDA-klyngen til rapportering.
3. I oversigtspanelet **Kontaktoplysninger** skal du angive udstederoplysninger ved at følge disse trin:

    1. Angiv den kunde, der er ansvarlig for tilskuddet, i feltet **Tilskudskunde**. For et eksisterende tilskud kan disse oplysninger allerede være angivet.
    2. Angiv, om tilskudskunden er finansieringskilde. Hvis tilskudskunden er finansieringskilde, skal du fjerne markeringen i afkrydsningsfeltet **Pass-through**. Hvis en anden kunde er finansieringskilde, og tilskudskunden er ansvarlig for forbrug og sporing af penge, skal du markere afkrydsningsfeltet **Pass-through**.

4. Hvis du har markeret afkrydsningsfeltet **Pass-through** i det foregående trin, skal du angive den kunde, der har givet tilskuddet, i feltet **Udstederagentur**. Udstederagenturet og tilskudskunden må ikke være den samme kunde.

Her er et eksempel på et pass-through-tilskud:

Den føderale regering har finansieret et infrastrukturprojekt for en delstat. Den føderale regering gav pengene til delstatens forbrug. I dette tilfælde er den føderale regering udstederagenturet, og delstaten er tilskudskunden.

> [!NOTE] 
> Når du aktiverer funktionen første gang, vil de første CFDA-numre blive indsat ved hjælp af de eksisterende numre på tilskud.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Udelade tilskud i SEFA-rapportering baseret på tilskudstypen

1. Gå til **Projektstyring og regnskab \> Konfiguration \> Tilskud \> Tilskudstyper**.
2. I oversigtspanelet **Standardoplysninger** skal du markere afkrydsningsfeltet **Udelad i Schedule of Expenditures of Federal Awards**.
3. Vælg **Gem** for at gemme ændringerne.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Køre Schedule of Expenditures of Federal Awards-forespørgsel

1. Gå til **Projektstyring og regnskab \> Forespørgsler og rapporter \> Tilskudsforespørgsel \> Schedule of Expenditures of Federal Awards**.
2. Benyt følgende fremgangsmåde i afsnittet **Parametre**:

    1. Vælg koden for datointervallet i feltet **Datointerval**. Alternativt kan du i felterne **Fra dato** og **Til dato** definere datointervallet.
    2. Valgfrit: Hvis du kun vil medtage fakturerede posteringer som indtægt i forespørgslen, skal du angive indstillingen **Medtag kun fakturerede indtægter** til **Ja**.

## <a name="columns"></a>Søjler

Schedule of Expenditures of Federal Awards-forespørgsler omfatter følgende kolonner:

- Klyngenavn til Catalog of Federal Domestic Assistance
- Tildelerbureau
- Gå gennem bureau
- Tilskudsnavn
- Tilskuds-id
- Id for tilskudsansøgning
- Catalog of Federal Domestic Assistance
- Tilgange
- Udgifter
