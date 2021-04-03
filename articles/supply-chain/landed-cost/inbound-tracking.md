---
title: Spore rejser for indgående fragt og forsendelsescontainere
description: Dette emne forklarer, hvordan du kan bruge siden Indgående sporing til at spore status for dine fragt- og forsendelsescontainerrejser.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 678f2b6cda0592e0393bb15f372cb4be84778932
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501240"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Spore rejser for indgående fragt og forsendelsescontainere

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

På siden **Indgående sporing** kan du spore status for dine fragt- og forsendelsescontainerrejser. Hver fragt og rejse opdeles efter *aktiviteter*, som hver har sin egen række på siden. Du kan bruge siden til at se og angive forventede datoer og faktiske datoer efter aktivitet.

Afhængigt af opsætningen i [Sporingskontrolcenter](delivery-information-setup.md#tracking-control-center) viser disse aktiviteter typisk automatisk den forventede landingsdato på den endelige destination. Afhængigt af opsætningen opdaterer den endelige dato normalt leveringsdatoen eller den bekræftede dato på indkøbsordrelinjerne. I forbindelse med flytteordrelinjer kan du konfigurere systemet til at opdatere modtagelsesdatoen.

Du kan åbne siden **Indgående sporing** ved at gå til **Landingsomkostninger \> Sporing \> Indgående sporing**.

## <a name="filter-the-activities-list"></a>Filtrere aktivitetslisten

Du kan bruge felterne **Fragt** og **Forsendelsescontainer** øverst på siden **Indgående sporing** til at filtrere siden, så den kun viser aktiviteter, der er knyttet til den valgte fragt og/eller forsendelsescontainer.

## <a name="update-tracking-information"></a>Opdatere sporingsoplysninger

Hvis du vil opdatere tidsplanen for en fragt eller rejse, skal du angive startdatoen for den første aktivitet. Den forventede slutdato for den sidste aktivitet opdateres derefter. Opsætningen af hver enkelt etape og rejseskabelon i [Sporingskontrolcenter](delivery-information-setup.md#tracking-control-center) bestemmer de forventede leveringstider. De forventede slutdatoer bruger leveringstiden fra aktivitetens startdato. Når den faktiske slutdato registreres, opdateres startdatoen for den næste aktivitet til samme dato som den faktiske slutdato for den forrige aktivitet. Den faktiske leveringstid opdateres, så der kan foretages sammenligning og analyse. Der kan angives yderligere bemærkninger i feltet **Note**.

Rækkefølgen af aktiviteterne i gitteret bestemmes af rækkefølgen af etaperne i den relevante rejseskabelon. Hvis rækkefølgen af etaperne i den tilknyttede rejse ændres, ændres sporingskontrollen også.

Du kan opdatere datoerne for alle containere ved at vælge **Opdater startdato** eller **Opdater faktisk slutdato** i handlingsruden. Du kan også angive datoerne pr. container på forsendelsen. Denne metode giver større fleksibilitet, da containere kan opdeles i et miljø med flere rejser.

## <a name="buttons-on-the-action-pane"></a>Knapper i handlingsruden

Du kan bruge knapperne i handlingsruden på siden **indgående sporing** til at arbejde med indgående fragter og rejser. I følgende tabel forklares de knapper, der er tilgængelige.

| Knap | Beskrivelse |
|---|---|
| Redigér | Rediger en rejse for fragt eller forsendelsescontainer. |
| Nye | Opret en ny rejse for fragt eller forsendelsescontainer. |
| Delete | Slet en valgt rejse for fragt eller forsendelsescontainer. |
| Opdater startdato | Opdater startdatoen for en aktivitet for alle containere i en fragt. Når startdatoen for en bestemt aktivitet eller et bestemt rejse opdateres, opdateres de efterfølgende forkalkulerede startdatoer på basis af den angivne leveringstid. |
| Opdater faktisk slutdato | Opdater slutdatoen for en aktivitet for alle containere i en fragt. Når slutdatoen for en bestemt aktivitet opdateres, opdateres de efterfølgende aktiviteter på basis af den angivne leveringstid. |
| Tilføj aktiviteter | Føj manuelt en aktivitet til en fragt. Du kan f.eks. tilføje en fumigeringsaktivitet. Tilføjelsen kan medføre, at den bekræftede leveringsdato for varerne i fartøjet eller fragten ændres. Når der føjes en aktivitet til rejsen, angives de forventede dage først, når startdatoen for en rejseetape opdateres. |

## <a name="information-and-settings-on-the-overview-tab"></a>Oplysninger og indstillinger under fanen Oversigt

Fanen **Oversigt** viser en liste over alle de aktiviteter, der tilhører fragten og/eller forsendelsescontaineren, der er valgt øverst på siden. I følgende tabel forklares de felter, der er tilgængelige for hver aktivitet.

| Felt | Beskrivelse |
|---|---|
| Etape | Etape-id'et for aktiviteten, som den defineres af rejseskabelonen. |
| Leveringsmåde | Aktivitetens forventede leveringsmetode. |
| Aktivitet | Dette felt identificerer normalt det job eller den opgave, der er tilknyttet aktiviteten. Af typiske eksempler kan nævnes *Sejlads* og *Fortoldning*. |
| Beskrivelse | En længere beskrivelse af aktiviteten. |
| Igangsæt dato | I dette felt vises først den forventede startdato for aktiviteten. Når den forrige aktivitets faktiske slutdato er angivet, vises imidlertid den faktiske startdato. Dette felt bruges til at bestemme den forventede slutdato baseret på leveringstiden. |
| Forventet slutdato | Værdien i dette felt beregnes på basis af startdatoen og leveringstiden. Du redigerer som regel ikke værdien direkte. |
| Faktisk slutdato | En bruger bør opdatere dette felt så hurtigt som muligt, efter at aktiviteten har fundet sted. Den faktiske leveringstid opdateres derefter. |
| Forventede dage | Den forventede tid (i antal dage), der kræves for at fuldføre aktiviteten. |
| Faktiske dage | Den faktiske tid (i antal dage), der kræves for at fuldføre aktiviteten. |
| Bemærk! | Du kan bruge dette felt til at tilføje diverse noter og detaljer om aktiviteten. |

## <a name="information-and-settings-on-the-general-tab"></a>Oplysninger og indstillinger under fanen Generelt

Fanen **Generelt** viser oplysninger om den etape, der er valgt under fanen **Oversigt**. Selvom nogle af de oplysninger, der vises under fanen **Oversigt**, gentages, indeholder den også flere oplysninger om den valgte etape.
