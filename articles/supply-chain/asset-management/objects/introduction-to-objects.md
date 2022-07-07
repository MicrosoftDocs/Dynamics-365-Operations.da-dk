---
title: Introduktion til aktiver
description: Denne artikel indeholder en oversigt over aktiver i Styring af aktiver.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetTimeline, EntAssetObjectTableLookup, EntAssetObjectTableParent, EntAssetObjectOverview, EntAssetObjectImage, EntAssetObjectTable, EntAssetLifecycleStateLog, EntAssetObjectWorkOrderActive, EntAssetObjectAttribute
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8498d6099112cea2c57a6387e7596adb5bcd84e
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015980"
---
# <a name="introduction-to-assets"></a>Introduktion til aktiver

[!include [banner](../../includes/banner.md)]

 

Denne artikel indeholder en oversigt over aktiver i Styring af aktiver. Et *aktiv* er enhver type udstyr, såsom en maskine eller en del til en maskine, der kræver vedligeholdelse, service eller reparation.

Et aktiv opdateres automatisk med relaterede oplysninger. Eksempelvis kan disse relaterede oplysninger vedrøre nye eller opdaterede arbejdsordrer. Du kan oprette aktiver ved hjælp af enten menupunktet **Alle aktiver** eller menupunktet **Afventende aktiver**. Denne artikel forklarer, hvordan du opretter aktiver ved hjælp af menupunktet **Alle aktiver**. Oplysninger om, hvordan du opretter aktiver ved hjælp af menupunktet **Afventende aktiver**, finder du under [Opret aktiver baseret på indkøbsordrer](../objects/create-objects-based-on-purchase-orders.md).

## <a name="all-assets"></a>Alle aktiver

Vælg **Styring af aktiver** \> **Aktiver** \> **Alle aktiver**. På listesiden **Alle aktiver** vises alle aktiver og nogle af de oplysninger, der er relateret til dem. Hvis du kun vil have vist aktive aktiver, skal du vælge **Aktive aktiver**. Hvis du kun vil have vist de aktiver, der er installeret på arbejdssteder, som du er relateret til som vedligeholdelsesarbejder, skal du vælge **Mine aktive aktiver**. (Denne relation er oprettet på siden **Arbejdere**. Du finder flere oplysninger i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).)

I gittervisningen **Alle aktiver** skal du vælge et link i kolonnen **Aktiver** for at få vist detaljerne for den valgte post. Hvis du vil redigere posten, skal du vælge knappen **Rediger**. Detaljeoversigten viser detaljerede oplysninger, der er relateret til aktivet. En rude med **Relaterede oplysninger** i højre side indeholder yderligere oplysninger relateret til aktivet. Udvid ruden for at se de relaterede oplysninger for det valgte aktiv.

Knapperne i Handlingsruden er organiseret på faner. Følgende tabel beskriver kort de knapper, der er relateret til Aktiv styring.

| Knapnavn          | Beskrivelse                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rediger                 | Rediger det valgte aktiv.                                                                                                                                         |
| Nyt                  | Oprette et nyt aktiv.                                                                                                                                                |
| Slet               | Slet det valgte aktiv.                                                                                                                                       |
| Flyt aktiv           | Flyt aktiver til en anden aktivstruktur eller til et andet sted i samme aktivstruktur.                                                                                         |
| Erstat aktiv        | Erstat et underordnet aktiv i et aktivhierarki med et andet aktiv.                                                                                                  |
| Installer aktiv        | Installer et aktiv på et arbejdssted.                                                                                                                          |
| Kopiér aktiv           | Kopiér et aktivhierarki til et andet aktiv.                                                                                                                          |
| Anmodninger             | Åbn listesiden **Aktive anmodninger**, hvor du kan se de vedligeholdelsesanmodninger, der er blevet oprettet for det valgte aktiv.                                                                         |
| Hændelseshistorik        | Få vist en oversigt over de forskellige registreringer, der er foretaget på aktivet.                                                                                                         |
| Aktivstykliste            | Få vist en oversigt over alle varer (reservedele og andre varer), der bruges på et aktiv.                                                                                  |
| Arbejdsordrer          | Åbn listesiden **Aktive arbejdsordrer**, hvor du kan se arbejdsordrerne for aktivet.                                                                                        |
| Kontrolliste            | Få vist en oversigt over vedligeholdelsestjeklister og målinger, der er registreret på aktivet.                                                                                                 |
| Vedligeholdelsesnedetid | Opret eller få vist registreringer af vedligeholdelsesnedetid på aktivet.                                                                                                       |
| Projektposteringer | Få vist alle bogførte transaktioner, der er relateret til arbejdsordrer, som er oprettet for aktivet.                                                                                       |
| Aktivmålinger       | Opret eller få vist aktivmålinger på aktivet.                                                                                                               |
| Vedligeholdelsestidsplan | Åbn listesiden **Åbn vedligeholdelsestidsplan**, hvor du kan se de vedligeholdelsesplaner, vedligeholdelsesanmodninger og vedligeholdelsesrunder, der er knyttet til aktivet, og som har statussen **Oprettet.** |
| Opdater aktivets tilstand   | Opdatere aktivets livscyklustilstand. Du kan vælge flere aktiver på listesiden **Alle aktiver**, og opdater dernæst aktivets livscyklustilstand for dem alle på samme tid.              |
| Log for livscyklustilstand  | Åbn en logfil, der viser livscyklustilstande for det valgte aktiv.                                                                                                                 |
| Aktivdokumenter      | Se en oversigt over de dokumenter, der er tilknyttet et aktiv. Disse dokumenter konfigureres i **Styring af aktiver** \> **Opsætning** \> **Aktivdokumenter**.                 |
| Egenskaber           | Opret eller se aktivattributter.                                                                                                                             |
| Billede                | Vælg et billede for aktivet.                                                                                                                                   |
| Overordnede aktiver        | Se historikken for de overordnede aktiver for det valgte aktiv.                                                                                                                |
| Arbejdssteder | Se arbejdsstedshistorikken for det valgte aktiv.                                                                                                          |
| Tilstandsvurdering | Registrer målinger af tilstandsvurderinger på aktivet.                                                                                                         |
| Fejl               | Åbn listesiden **Fejl på aktiver**, hvor du kan se de fejl, der er registreret på aktivet.                                                                                             |
| Omkostningsstyring         | Sammenlign budgetomkostninger og faktiske omkostninger på aktivet.                                                                                                              |
| Timestyring         | Sammenlign estimerede timer og faktiske timer på aktivet.                                                                                                              |
| KPI'er for aktiver           | Beregn og se KPI'er (Key Performance Indicators) for aktivet.                                                                                              |
| Jobtyper            | Se en oversigt over de aktuelle standardjobtyper for aktivet.                                                                                                            |
| Kritikalitetstyper    | Se eller opdater kritikalitetstyper for aktiver.                                                                                                                              |
| Reservedele          | Se en liste over godkendte og alternative reservedele, der kan bruges på aktivet.                                                                               |
| Aktivets forbrug    | Udskriv en rapport, der viser forbrugsregistreringer på aktivet.                                                                                                |
| Fejl for aktivet          | Udskriv en rapport, der viser registreringer af fejl på aktivet.                                                                                                      |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]