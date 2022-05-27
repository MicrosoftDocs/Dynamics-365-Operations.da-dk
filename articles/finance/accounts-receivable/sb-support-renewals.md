---
title: Support og fornyelser
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere og bruge support- og fornyelsesprocessen for salgsordrer til at oprette en faktureringsplan for fornyelse af varer.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 7de74f2b12e8e7201663ba78d936131b301b1ff9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685764"
---
# <a name="support-and-renewals"></a>Support og fornyelser 

Dette emne forklarer, hvordan du angiver supportvarer eller fornyelsesvarer, når du angiver salgsordrer. Disse elementer bruges til at beregne gebyrbeløbet for den oprindelige supportkontrakt og/eller det fornyelsesbeløb, der bruges, når der oprettes en faktureringsplan i abonnementsfakturering. Dit firma sælger f.eks. en server til en kunde, og du tilbyder et abonnement på databackup det første år og mulighed for at forny abonnementet hvert år. *Supportvaren* er abonnementet for det første år, og *fornyelsesvaren* er fornyelse for hvert efterfølgende år.

Du kan angive oplysninger om supportkontrakten, fornyelseskontrakten eller begge dele. Når du angiver oplysninger om supportkontrakten, er det kun supportvaren, der føjes til salgsordren. Når du angiver oplysninger om fornyelseskontrakten, bruges fornyelsesvaren til at oprette en faktureringsplan.

## <a name="support-and-renewal-setup"></a>Konfiguration af support og fornyelse

På siden **Support og fornyelsesniveauer** kan du konfigurere forskellige supportniveauer for varer til support og fornyelse. Supporten eller fornyelsen kan være en procentdel af det oprindelige varebeløb, eller det kan være et standardbeløb.

Du kan vælge standardsupportniveauer på siden **Parametre for tilbagevendende kontraktfakturering**.

Et firma kan f.eks. tilbyde følgende niveauer af support og fornyelse.

| Supportniveau | Supportprocent | Fornyelsesprocent |
|---|---|---|
| Ubegrænset | 40 % | 30 % |
| Guld | 25 % | 18 % |
| Sølv | 20 % | 14 % |
| Bronze | 15 % | 10 % |

Benyt følgende fremgangsmåde for at oprette et support- eller fornyelsesniveau.

1. Vælg **Ny** på siden **Support- og fornyelsesniveauer**.
2. Angiv et entydigt navn i feltet **Supportniveau**.
3. Indtast en beskrivelse i feltet **Beskrivelse**.
4. Vælg supportberegningsmetoden i feltet **Supportberegningsmetode**. Hvis du vælger **Procent**, skal du angive en supportprocent i feltet **Supportprocent**.
5. Vælg beregningsmetoden for fornyelse i feltet **Metode til fornyelsesberegning**. Hvis du vælger **Procent**, skal du angive en fornyelsesprocent i feltet **Fornyelsesprocent**.
6. Vælg **Gem**.

### <a name="fields"></a>Felter

Siden **Support- og fornyelsesniveauer** indeholder følgende felter.

| Felt | Beskrivelse |
|---|---|
| Supportniveau | Et entydigt id for support- eller fornyelsesniveauet (f.eks. **Guld** eller **Sølv**). |
| Beskrivelse | En beskrivelse af support- eller fornyelsesniveauet. |
| Metode til supportberegning | Vælg supportberegningsmetoden for niveauet: **Procent** eller **Standardbeløb**. |
| Supportprocent | Hvis du har valgt **Procent** som beregningsmetode for support, skal du angive den procent, der skal bruges til beregning af prisen på supportvaren. Hvis du har valgt **Standardbeløb** som beregningsmetode, angives beløbet, når transaktionen oprettes. |
| Metode til fornyelsesberegning | Vælg fornyelsesberegningsmetoden for niveauet: **Procent** eller **Standardbeløb**. |
| Fornyelsesprocent | Hvis du har valgt **Procent** som beregningsmetode for fornyelse, skal du angive den procent, der skal bruges til beregning af prisen på fornyelsesvaren. Hvis du har valgt **Standardbeløb** som beregningsmetode, angives beløbet, når transaktionen oprettes. |

## <a name="support-and-renewal-process"></a>Support- og fornyelsesproces

Funktionaliteten af support og fornyelse kan anvende forskellige supportniveauer på varer og opdatere oplysninger om fornyelse i abonnementsfakturering.

Før du bruger funktionen til support og fornyelse, skal følgende opgaver udføres.

1. Opret mindst ét support- eller fornyelsesniveau på siden **Support- og fornyelsesniveauer**.
2. På siden **Vareopsætning** skal du tilknytte en vare med support- og fornyelsesvarer. Denne opgave er kun påkrævet, hvis du vil konfigurere standardværdier for support- og/eller fornyelsesvarer.
3. På siden **Parametre for tilbagevendende kontraktfakturering** skal du angive standardindstillingerne for support og fornyelse af nye faktureringsplaner.

Hvis du vil anvende forskellige supportniveauer på varer og opdatere oplysninger om fornyelse, skal du følge disse trin.

1. Opret en salgsordre på siden **Alle salgsordrer**.
2. I oversigtspanelet **Salgsordrelinjer** skal du tilføje en vare.
3. Vælg **Support og fornyelse \> Tilføj support og fornyelse** under fanen **Faktura**.
4. På siden **Support- og fornyelsesproces** opdateres hovedsektionen med indstillingerne fra siden **Parametre for tilbagevendende kontraktfakturering**. Disse værdier gælder for alle support- og fornyelsesvarer. (Hvis f.eks. faktureringsfrekvensen er angivet til **Årlig**, har alle de salgslinjer, der oprettes med en fornyelsesvare, en årsfrekvens). Hvis du vil knytte salgsordren til en eksisterende faktureringsplan, skal du vælge en værdi i feltet **Faktureringsplannummer**.
5. Hvis du vil ændre startdatoen for support eller fornyelse, skal du angive indstillingen **Tilsidesæt startdato** til **Ja**.
6. Hvis du vil tilføje eller redigere supportvaren, skal du markere afkrydsningsfeltet **Support** og derefter angive en supportvare i feltet **Supportvare**. Varen føjes til salgsordren.
7. Hvis du vil tilføje eller redigere fornyelsesvaren, skal du markere afkrydsningsfeltet **Fornyelse** og derefter angive en fornyelsesvare i feltet **Fornyelsesvare**. Når salgsordren faktureres, oprettes der en faktureringsplan, der omfatter varen.
8. Vælg **OK**.
9. Under fanen **Generelt** skal du vælge **Faktura**. Når salgsordren er bogført, oprettes faktureringsplanen. Der vises en besked i meddelelsesoplysningerne, herunder oplysningerne om faktureringsplanen.
10. Vælg nummeret på faktureringsplanen på siden **Faktureringsplaner** på listen **Alle/Aktive faktureringsplaner** for at se detaljer om faktureringsplanen.
11. Vælg **Support og fornyelse** i oversigtspanelet **Faktureringsplanlinjer** for at gennemse oplysningerne om de linjer, der er oprettet.

> [!NOTE]
> Hvis startdatoen for fornyelse af en faktureringsplanlinje skal ændres, kan du redigere værdien af **Startdato** for linjen på siden **Faktureringsplaner**. Når du åbner siden **Vis faktureringsdetaljer** for linjen, opdateres feltet **Faktureringsstartdato** med den nye dato. Værdien af **Faktureringens slutdato** genberegnes på baggrund af faktureringsfrekvensen. Startdatoen for fornyelse kan kun opdateres, hvis den første faktura til faktureringsplanen for fornyelse ikke er oprettet og bogført. Når den første faktura er oprettet og bogført, kan startdatoen ikke redigeres.

Processen til support og fornyelse er kun tilgængelig for salgsordren. Når du føjer support- og fornyelsesvarer til en salgsordre, kan du oprette en ny faktureringsplan eller føje fornyelsesvaren til en eksisterende faktureringsplan.

## <a name="support-and-renewal-audit"></a>Revision af support og fornyelse

På siden **Revision af support og fornyelse** du gennemse detaljerne for de faktureringsplanlinjer, der oprettes ud fra fornyelsesvaren på en salgsordre. Denne indstilling er tilgængelig, når varen i faktureringsplanlinjen er en fornyelsesvare.

Hvis du vil redigere oplysninger om support og fornyelse for en faktureringsplanlinje, skal du følge disse trin.

1. Vælg faktureringsplannummeret på siden **Alle faktureringsplaner**.
2. Vælg en linje i sektionen **Faktureringsplanlinjer**, og vælg derefter **Support og fornyelse**.
3. Gennemse alle oplysninger om support- eller fornyelsesvaren.
4. Foretag eventuelle nødvendige ændringer af supportniveauet eller fornyelsesprocenten eller -beløbet, og angiv derefter en værdi i feltet **Årsag til ændring**.
5. Vælg **Behandling**.

### <a name="fields"></a>Felter

Siden **Revision af support og fornyelse** indeholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------|
| Varenummer | Varenummeret til faktureringsplanlinjen. |
| Produktnavn | Produktnavnet. |
| Supportplanniveau | Se eller ret supportniveauet for fornyelsesvaren. |
| Fornyelsesprocent | Angiv den fornyelsesprocent, der bruges, når enhedsprisen beregnes for en fornyelsesvare i en faktureringsplan. |
| Fornyelsesbeløb | Angiv det fornyelsesbeløb, der bruges, når enhedsprisen beregnes for en fornyelsesvare i en faktureringsplan. |
| Årsag til ændring | Angiv årsagen til at ændre oplysningerne om support og fornyelse. Du skal angive en årsag, når du ændrer værdien af **Fornyelsesprocent**, **Fornyelsesbeløb** eller **Supportplanniveau**. |
| Oprindelig salgsvare | Det oprindelige salgsvarenummer fra salgsordren. |
| Oprindeligt nettobeløb | Det oprindelige nettobeløb for varen. |
| Oprindeligt supportniveau | Det oprindelige supportniveau for varen. |
| Oprindelig fornyelsesprocent | Den oprindelige fornyelsesprocent for varen. |
| Oprindeligt fornyelsesbeløb | Det oprindelige fornyelsesbeløb for varen. |
| **Gitter** | |
| Oprindeligt supportniveau | Det tidligere supportniveau. |
| Oprindelig fornyelsesprocent | Den tidligere fornyelsesprocent. |
| Oprindeligt fornyelsesbeløb | Det tidligere fornyelsesbeløb. |
| Ændret af | Brugernavnet for den bruger, som udførte ændringen. |
| Dato og klokkeslæt for ændring | Dato for, hvornår ændringen opstod. |
| Årsag | Årsagen til ændringen. |
