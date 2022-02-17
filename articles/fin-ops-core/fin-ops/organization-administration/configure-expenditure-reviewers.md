---
title: Konfigurere udgiftsvalidatorer
description: Dette emne beskriver, hvordan du bruger udgiftsvalidatorer til dynamisk valg af den bruger, som en arbejdsgangsopgave, godkendelse eller manuel beslutning er tildelt.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: ad980889247e0239ad743078cb013c1c5839f676
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070140"
---
# <a name="configure-expenditure-reviewers"></a>Konfigurere udgiftsvalidatorer
[!include[banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Du kan konfigurere dynamiske udgiftsvalidatorer for at dirigere udgifter til gennemsyn på basis af den bruger, der er knyttet til en projektrolle, eller den økonomiske dimension, hvor udgiften debiteres. Arbejdsgangen bruger den angivne projektrolle eller ejeren af den angivne økonomiske dimension til at afgøre, hvem udgiften skal sendes videre til.

Du kan definere én eller flere konfigurationer til udgiftsvalidatorer og derefter vælge en konfiguration, mens du opretter en arbejdsgang. Du kan konfigurere udgiftsvalidatorens værdier for hver enkelt juridisk enhed i organisationen. Når du har defineret udgiftsvalidatorens konfigurationer, kan du knytte en konfiguration til din arbejdsgangsopgave. Udgiftsvalidatoerer kan tildeles til arbejdsgangsopgaver, godkendelser og manuelle beslutninger.

> [!NOTE]
> Selvom udgiftsvalidatorer ikke er obligatoriske, kan de være med til at forenkle konfigurationen af arbejdsgangen. Du behøver f.eks. ikke oprette én betinget beslutning, der skal kontrolleres for hver bærerdimension, og derefter oprette et andet element for at tildele godkendelsen eller opgaven til en bestemt bruger eller grupper af brugere. I stedet kan du konfigurere ejeren af bærerdimensionen og bruge en udgiftsvalidator til dynamisk at vælge den rigtige bruger. På den måde skal du blot opdatere feltet **Ejer** for den økonomiske dimension, når ejerskabet eller tildelingen af ressourcer ændres.

## <a name="types-of-expenditure-reviewers"></a>Typer af udgiftsvalidatorer

Ikke alle arbejdsgange understøtter begrebet udgiftsvalidatorer. Du kan som standard konfigurere udgiftsvalidatorer for indkøbsrekvisitioner, indkøbsordrer, kreditorfakturaer og udgiftsrapporter. Hver af disse arbejdsgangstyper kræver, at du konfigurerer udgiftsvalidatorer på en separat side, der er specifik for funktionen og modulet. For hvert understøttet dokument kan udgiftsvalidatorer bruges sammen med arbejdsgange på overskriftsniveau eller arbejdsgange på linjeniveau.

I følgende tabel vises, hvor du går til konfiguration af en udgiftsvalidator til hvert understøttet dokument.

| Dokument | Navigationssti |
|----------|-----------------|
| Udgiftsrapporter | Udgiftsstyring \> Konfiguration \> Politikker \> Udgiftsvalidatorer |
| Indkøbsordrer | Indkøbs og forsyning \> Konfiguration \> Politikker \> Validatorer af indkøbsordreudgift |
| Indkøbsrekvisitioner | Indkøbs og forsyning \> Konfiguration \> Politikker \> Validatorer af indkøbsrekvisitionsudgift |
| Kreditorfakturaer | Kreditor \> Konfiguration af politik \> Validatorer af kreditorfakturaudgift |

## <a name="expenditure-reviewer-assignments"></a>Udgiftsevalueringstildelinger

Der er to typer tildelinger tilgængelige for hver udgiftsvalidatorer: *projektfordelinger* og *organisationsfordelinger*. Du kan vælge mellem projektmyndigheder og økonomiske dimensioner for en projektfordeling. Du kan vælge økonomiske dimensioner for en organisationsfordeling.

Projektlederen, projektcontrolleren og projektlederen er projektlederen. Du kan definere disse myndigheder direkte i projektet ved at vælge en arbejder i de relevante felter.

Økonomiske dimensioner styres af kontostrukturerne i de enkelte juridiske enheder. For hver juridisk enhed kan du vælge, hvilke økonomiske dimensioner der skal bruges sammen med udgiftsvalidatoren. Dimensionerne kan enten komme fra projektet (i dette tilfælde skal du vælge dimensionerne under fanen **Projektfordelinger**) eller dokumentet (i dette tilfælde skal du vælge dimensionerne under fanen **Organisationsfordelinger**). I feltet **Ejer** på siden **Værdier for økonomiske dimensioner** kan du vælge arbejderen for hver økonomisk dimension.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>Eksempel 1: Udgiftsvalidatorer baseret på organisationsfordelinger

Du arbejder for Contoso Appliances, og organisationen har seks afdelinger og 10 ressourcer. Når der sendes en ny indkøbsrekvisition, skal godkendelsen først godkendes fra afdelingschefen og derefter fra bærerchefen.

I dette eksempel konfigurerer du to *udgiftsevalueringer af indkøbsrekvisitioner*:

- For den første reviewer skal du navngive afdelingen og derefter vælge den økonomiske dimension **Afdeling** under fanen **Organisationsfordelinger**. 
- For den anden reviewer skal du navngive afdelingen og derefter vælge den økonomiske dimension **Afdeling** under fanen **Organisationsfordelinger**.

Når du konfigurerer arbejdsgangen, opretter du to godkendelsestrin. Det første er til afdelingen, og det andet er til bæreren. For hvert godkendelseselement kan du vælge **Deltager** i feltet **Tildelingstype** under fanen **Rollebaseret**, vælge **udgiftsdeltagere** i feltet **Deltagertype** og derefter vælge den relevante deltager i feltet **Deltager**.

Når indkøbsrekvisitionen oprettes, knyttes de økonomiske dimensioner afdeling og bærer til linjerne i indkøbsrekvisitionen. Når arbejdsgangen er sendt, evaluerer systemet først afdelingen i indkøbsrekvisitionen og tildeler godkendelseselementet til den bruger, der er relateret til den arbejder, du har valgt til afdelingen. Når det første godkendelsestrin er fuldført, evaluerer systemet andet godkendelsestrin og tildeler andet godkendelseselement til den bruger, der er relateret til den arbejder, du har valgt til afdelingen.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>Eksempel 2: Udgiftsvalidatorer baseret på projektfordelinger

Du arbejder i serviceafdelingen hos Contoso Appliances. Organisationen kræver, at projektlederen for hver indkøbsordre skal godkende udgiften. Desuden skal administratoren for projektet godkende den. Godkendelserne kan udføres på én gang. Under alle omstændigheder skal begge brugere godkende indkøbsordren, før arbejdsgangen kan fortsætte.

I dette eksempel kan du oprette en *udgiftsevaluering af indkøbsordrer* med navnet **INDKØBSORDRE og Bærer**. Du markerer afkrydsningsfeltet **Projektleder** og angiver indstillingen **Bærerdimension** til **Ja** under fanen **Projektfordelinger** på **udgiftsvalidator**-siden. Som en del af konfigurationen skal du sikre dig, at feltet **Projektleder** er angivet for alle projekter, og at der er angivet en ejer for alle ressourcer på siden **Økonomiske dimensionsværdier**.

Når du konfigurerer arbejdsgangen, skal du bruge et godkendelseselement. Du kan vælge **Deltager** i feltet **Tildelingstype**. På fanen **Rollebaseret** kan du derefter vælge **udgiftsdeltagere** i feltet **Deltagertype** og vælge projektlederen og bæreren i feltet **Deltager**. Hvis du vil sikre dig, at arbejdsgangen ikke fortsætter, før både projektlederen og ejeren af bæreren godkender arbejdsgangen, skal du indstille feltet **Færdiggørelsespolitik** til **Alle godkendere**.

Når indkøbsordren oprettes, skal feltet **Projekt** angives. Hvis du ikke kræver et projekt for alle indkøbsordrer, skal du føje en betinget beslutning til arbejdsgangen for at kontrollere, om der er et projekt, før godkendelsestrinnet køres. Systemet evaluerer derefter det projekt, der er angivet for indkøbsordren, og tildeler godkendelseselementet til den bruger, der er relateret til arbejderen, i feltet **Projektleder**. Systemet opretter desuden en opgave og tildeler den til den bruger, der er knyttet til den arbejder, som du vælger i feltet **Ejer** for bæreren fra projektet. Bemærk, at dette eksempel bruger bæreren for projektet, ikke bæreren for indkøbsordren.

## <a name="set-up-expenditure-reviewers"></a>Konfigurere udgiftsvalidatorer

Dette eksempel viser, hvordan du konfigurerer en udgiftsevaluering af en indkøbsrekvisition. Hvis du vil konfigurere andre typer udgiftsvalidatorer, skal du erstatte navigationsstien i trin 1 med den relevante sti fra tabellen i afsnittet [Udgiftsgennemsynstyper tidligere i dette emne](configure-expenditure-reviewers.md#types-of-expenditure-reviewers).

1. Gå til **Indkøb og forsyning \> Konfiguration \> Politikker \> Validatorer af indkøbsrekvisitionsudgift**.
2. Vælg **Ny** på siden **Udgiftsvalidatorer af indkøbsrekvisitioner**.
3. Angiv et navn i feltet **Navn** til udgiftsevalueringskonfigurationen, f.eks. **bærer**.
4. Vælg den juridiske enhed, der skal konfigureres i oversigtspanelet **Udgiftsgennemsyn efter juridisk enhed**.
5. Marker afkrydsningsfeltet for hver projektmyndighed for hver projektfordeling, og vælg **Ja** for hver økonomisk dimension, du vil aktivere. 
6. Vælg **Ja** for hver økonomisk dimension, du vil aktivere, under fanen **Organisationsfordelinger** for en organisationsfordeling.
7. Gentag trin 4 til 6 for hver ekstra juridiske enhed.

## <a name="assign-owners-to-financial-dimensions"></a>Tildele ejere til økonomiske dimensioner

Følg disse trin, hvis du vil tildele en ejer til en økonomisk dimension.

1. Gå til **Finans \> Kontoplan \> Dimensioner \> Økonomiske dimensioner**.
2. Vælg den økonomiske dimension, der skal tildeles ejere til, på listen.
3. Vælg **Dimensionsværdier**.
4. Vælg **Rediger** for at foretage ændringer af dimensionsværdierne.
5. Vælg den dimensionsværdi, der skal tildeles ejere til, på listen.
6. Vælg den arbejder, der skal tilknyttes dimensionsværdi, i feltet **Ejer**.

## <a name="configure-project-distributions"></a>Konfigurere projektfordelinger

Udfør følgende trin for at tildele projektautoritet til et projekt.

1. Gå til **Projektstyring og regnskab \> Projekter \> Alle projekter**.
2. Vælg det projekt, der skal tildeles autoritet til.
3. Vælg **Rediger** for at foretage ændringer af projektet.
4. I sektionen **Ansvarlig** i oversigtspanelet **Generelt** skal du vælge en arbejder til felterne **Salgschef**, **Projektleder** og **Projektcontroller** efter behov.
5. Vælg de nødvendige økonomiske dimensioner for projektet i oversigtspanelet **Økonomiske dimensioner**.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Tildele udgiftsvalidatorer til en arbejdsgangsopgave

I dette eksempel vises, hvordan du kan konfigurere en arbejdsgang for en indkøbsrekvisition, så den bruger en udgiftsevaluering af indkøbsrekvisitioner. Hvis du vil konfigurere andre typer arbejdsgange, kan den arbejdsgangsside, der skal åbnes i trin 1, være i modulet **Udgiftsstyring** eller **Kreditor** i stedet for modulet **Indkøb og forsyning**.

Du kan tildele validatorer til indkøbsrekvisitionsudgift til arbejdsprocesopgave på følgende måde.

1. Gå til **Indkøb og forsyning \> Opsætning \> Indkøbs- og forsyningsarbejdsgange**.
2. Dobbeltklik på en eksisterende arbejdsgang, eller opret en ny arbejdsgang.
3. I arbejdsgangseditoren i ruden **Arbejdsgang** skal du vælge den opgave, som udgiftsevalueringskonfigurationen skal tildeles til. Vælg derefter **Handlingsrude** i gruppen **Vis**, og vælg **Egenskaber**.
4. Vælg **Tildeling** i venstre rude på siden **Egenskaber**.
5. Vælg **Deltager** under fanen **Tildelingstype**.
6. Vælg **udgiftsdeltagere** i feltet **Deltagertype** under fanen **Rollebaseret**. Vælg konfigurationen til den udgiftsvalidator, som du vil bruge til arbejdsopgaven, i feltet **Deltager**.
