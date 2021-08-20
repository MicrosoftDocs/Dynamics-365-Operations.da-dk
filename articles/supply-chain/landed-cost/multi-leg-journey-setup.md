---
title: Opsætning af rejse i flere etaper
description: Dette emne beskriver, hvordan du konfigurerer rejser i flere etaper for modulet Landingsomkostninger.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 045ded1fb881b0572f4490ab3a5d4ca1cb8c341a4d245e6d98991228a90aadb7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774072"
---
# <a name="multi-leg-journey-setup"></a>Opsætning af rejse i flere etaper

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer rejser i flere etaper for modulet **Landingsomkostninger**.

## <a name="legs"></a>Etaper

Etaper bruges til at identificere forskellige dele af en rejse. De enkelte etaper opbygges ved at vælge forsendelseshavnene "til" og "fra" samt den transportmetode, der bruges til den pågældende etape. Leveringstiderne kan knyttes til hver enkelte etape. Leveringstiderne kan være med til at spore en forsendelse og kan også bruges til at beregne den forventede leveringsdato for varerne i en fragt. Når en etape af en rejse er fuldført, kan statussen for fragten, forsendelsescontaineren og tilknyttede indkøbsordrelinjer desuden opdateres via opsætningen af sporingskontrol. Etaper kan benyttes af en enkelt rejseskabelon, eller de kan genbruges af flere rejseskabeloner. Containerlastning, told og lokal transport er normalt konfigureret som etaper, og der bruges en ikke-specifik forsendelseshavn til dem.

Du kan arbejde med etaper ved at gå til **Landingsomkostninger \> Opsætning af rejse i flere etaper \> Etaper**. Her kan du se, åbne, oprette og slette poster til etaper. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Etape | Angiv et entydigt id-navn/-nummer for rejseetapen. |
| Beskrivelse | Angiv en beskrivelse af rejseetapen. Denne beskrivelse identificerer typisk portene "til" og "fra" eller trinnet i rejsen. |
| Fra havn | Angiv varernes oprindelsessted for etapen. |
| Til havn | Angiv varernes destinationssted for etapen. |
| Leveringsmetode | Angiv transportmetoden for etapen. |

## <a name="journey-templates"></a>Ruteskabeloner

En rejseskabelon definerer rejsen med flere etaper mellem to havne, hvor varerne rejser under en fragt. Rejsens etaper kombineres med det formål at identificere, hvor længe varerne skal rejse fra leverandørens oprindelsessted til den endelige lagerdestination. Når etaperne angives på rejseskabelonen i en bestemt rækkefølge, vil leveringstiderne identificere datoen for hver etape og status for fragten, containeren og indkøbslinjerne til fragten. Du kan bruge [centeret for sporingskontrol](delivery-information-setup.md) til at konfigurere de leveringstider, der er knyttet til hver enkelt etape, som udgør rejseskabelonen. Rejseskabelonen bruges også, når de automatiske omkostninger for en fragt konfigureres. Når der er defineret en rejse, kan den omkostning, der er knyttet til transporten af varerne, defineres på siden med automatiske omkostninger.

Du kan arbejde med rejseskabeloner ved at gå til **Landingsomkostninger \> Opsætning af rejse i flere etaper \> Rejseskabeloner**. Her kan du se, åbne, oprette og slette rejseskabeloner.

Angiv følgende felter i overskriften for hver rejseskabelon.

| Felt | Beskrivelse |
|---|---|
| Ruteskabelon | Angiv et entydigt id-navn/-nummer for rejseskabelonen. Rejseskabelonen beskriver typisk oprindelsesstedet og destinationsstedet for rejsen. |
| Beskrivelse | Angiv en beskrivelse af rejseskabelonen. Beskrivelsen angiver typisk "til"- og "fra"-havne og rejsetypen. |

I sektionen **Linjer** skal du tilføje en linje for hver etape af rejsen og sætte linjerne i rækkefølge. Brug pilene **Op** og **Ned** på værktøjslinjen til at ændre linjerækkefølgen. I følgende tabel forklares de felter, der er tilgængelige for hver linje.

| Felt | Beskrivelse |
|---|---|
| Etape | Vælg en etape, der skal føjes til rejsen. |
| Beskrivelse | Beskrivelsen af etapen. |
| Fra havn | Den havn, der er varernes oprindelsessted for etapen. Denne havn er den "til"-havn, der bruges til at bestemme de automatiske omkostninger for en fragt. |
| Til havn | Varernes endelige destinationshavn for etapen. |
| Leveringsmåde | Den leveringsmåde, der bruges til etapen. |
| Rute fra havn | Hvis den havn, der er angivet for etapen, bruges til at bestemme de automatiske omkostninger, skal du markere dette afkrydsningsfelt for at identificere den som "rejse fra"-havnen. Denne havn vises i fragthovedet. |
| Rute til havn | Hvis den havn, der er angivet for etapen, bruges til at bestemme de automatiske omkostninger, skal du markere dette afkrydsningsfelt for at identificere den som "rejse til"-havnen. Denne havn vises i fragthovedet. |
| Fragtfirma | Vælg det fragtfirma, der bruges til etapen. |

## <a name="activities"></a>Aktiviteter

Indstillingerne på siden **Aktiviteter** fastlægger de typer aktiviteter, der kan forekomme på destinationshavnen for en etape. Brugere, der arbejder på siden **Alle forsendelsescontainere**, kan vælge mellem disse værdier, når de estimerer varigheden af hver aktivitet og registrerer den faktiske varighed til sammenligningsformål.

Hvis du vil konfigurere dine aktiviteter, skal du gå til **Landingsomkostninger \> Opsætning af rejse i flere etaper \> Aktiviteter**. Her kan du tilføje, fjerne og redigere aktiviteter ved at bruge knapperne i handlingsruden.

I følgende tabel forklares de felter, der er tilgængelige for hver aktivitet i gitteret.

| Felt | Beskrivelse |
|---|---|
| Aktivitet | Navnet på aktiviteten. |
| Beskrivelse | Aktivitetens beskrivelse. |
| Fragtfirma | Leverandørkontoen for det fragtfirma, der er knyttet til aktiviteten. |
