---
title: Introduktion til arbejdsordrer
description: Denne artikel indeholder en oversigt over arbejdsordrer i Styring af aktiver.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5eb911ec4ba9655c4ecaea3bf9a4f8736fa036c2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016704"
---
# <a name="introduction-to-work-orders"></a>Introduktion til arbejdsordrer

[!include [banner](../../includes/banner.md)]



Arbejdsordrer bruges til at styre vedligeholdelsesjob, angive nødvendige oplysninger om dem og registrere forbrug på dem. Hver arbejdsordre kan indeholde et eller flere arbejdsordrejob, og et eller flere aktiver kan være tilknyttet hver arbejdsordre. Hvert arbejdsordrejob definerer et vedligeholdelsesjob, der er planlagt på aktivet.

Du kan oprette arbejdsordrer på følgende måder:

- Automatisk ved hjælp af [Planlægge vedligeholdelsesplaner](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md) til kalenderbaserede vedligeholdelsesplaner, der er angivet til "Automatisk oprettelse".

- Automatisk ved hjælp af [Planlægge vedligeholdelsesrunder](../preventive-and-reactive-maintenance/maintenance-rounds.md) til vedligeholdelsesrunder, der er angivet til "Automatisk oprettelse".

- Til præventive vedligeholdelsesjob eller vedligeholdelsesanmodninger fra [Vedligeholdelsestidsplan](../preventive-and-reactive-maintenance/maintenance-schedule.md).

- Manuelt

- Fra siden **Alle vedligeholdelsesanmodninger**, **Aktive vedligeholdelsesanmodninger** eller **Vedligeholdelsesanmodninger for mine arbejdssteder**.

>[!NOTE]
>Arbejdsordrejob, der er relateret til samme aktiv, er relateret til samme projekt-id.

## <a name="all-work-orders"></a>Alle arbejdsordrer

Vælg **Styring af aktiver** > **Arbejdsordrer** > **Alle arbejdsordrer** for at åbne listesiden **Alle arbejdsordrer**. Denne side viser alle arbejdsordrer og nogle af de oplysninger, der er relateret til hver.

I illustrationen nedenfor vises et eksempel på listesiden **Alle arbejdsordrer**.

![Figur 1.](media/01-work-orders.png)

Vælg **Styring af aktiver** > **Arbejdsordrer** > **Aktive arbejdsordrer** for at se en liste over ene aktive arbejdsordrer. 

Vælg **Styring af aktiver** > **Arbejdsordrer** > **Vedligeholdelsesjob med arbejdsordre for mit arbejdssted** for at få vist en liste over arbejdsordrejob, der indeholder aktiver, som er installeret på arbejdssteder, du er relateret til som arbejder. Relationen mellem arbejdere og arbejdssteder konfigureres på siden **Arbejdere**. Du finder flere oplysninger i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).)

Her er nogle måder, du kan bruge siden **Alle arbejdsordrer** på:

- I gittervisningen skal du vælge et link i kolonnen **Arbejdsordre** for at få vist detaljerne for den valgte post. Du kan derefter vælge **Rediger** for at åbne posten til redigering.

- I detaljeoversigten vises detaljerede oplysninger, der er relateret til arbejdsordren.  

- Vælg fanen **Linjer** i detaljevisningen for at få vist oplysninger om arbejdsordrejobbet, eller vælg fanen **Overskrift** for at få vist oplysninger om arbejdsordren.  

- Udvid ruden **Relaterede oplysninger** i højre side af siden for at få vist yderligere oplysninger, der vedrører den valgte arbejdsordre.

I illustrationen nedenfor vises et eksempel på detaljevisningen **Alle arbejdsordrer**.

![Figur 2.](media/02-work-orders.png)


Knapperne i Handlingsruden er organiseret på faner. Følgende tabel beskriver kort de knapper, der er relateret til Styring af aktiver:



| Knapnavn                     | Beskrivelse                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rediger                            | Rediger den valgte arbejdsordre.                                                                                                                                                                                                                                           |
| Nyt                             | Opret ny arbejdsordre.                                                                                                                                                                                                                                                  |
| Delete                          | Slet den valgte arbejdsordre.                                                                                                                                                                                                                                         |
| Arbejdsordrepulje                 | Føj den valgte arbejdsordre til en arbejdsordrepulje, eller fjern den fra arbejdsordrepuljen.                                                                                                                                                                                           |
| Juster                          | Juster oplysninger om forventet start og afslutning, serviceniveau, ansvarlig vedligeholdelsesarbejder eller ansvarlig vedligeholdelsesarbejdergruppe på udvalgte arbejdsordrer.                                                                                                                                     |
| Relateret arbejdsordre              | Opret en ny arbejdsordre, der er relateret til det valgte arbejdsordrejob. Dette er nyttigt, hvis du vil registrere primære og sekundære arbejdsordrer.                                                                                                                              |
| Kopiér arbejdsordre                 | Opret en ny arbejdsordre, der er baseret på en eksisterende arbejdsordre.                                                                                                                                                                                                               |
| Hændelseshistorik                   | Vis registreringshistorikken for arbejdsordren.                                                                                                                                                                                                                |
| Noter til vedligeholdelsesjob i arbejdsordre                           | Opret en beskrivelse af en arbejdsordre, eller indsæt noter eller bemærkninger til den. Start med at vælge **Tilføj tidsstempel** for at føje dit brugernavn og et tidsstempel til noten. Noter vises under fanen **Beskrivelse** i oversigtspanelet **Linjedetaljer** på siden **Arbejdsordre**.         |
| Værktøjer                           | Opret en liste over nødvendige værktøjer på en arbejdsordre. Værktøjer oprettes som ressourcer i **Virksomhedsadministration** > **Ressourcer** > **Ressourcer**.                                                                                                      |
| Vedligeholdelsestjekliste           | Se kontrolliste for det aktiv, der er tilknyttet arbejdsordren.                                                                                                                                                                                                              |
| Aktivfejl                     | Se eller registrer fejloplysninger for et aktiv. Disse oplysninger bruges til fejlhåndtering.                                                                                                                                                                                      |
| Vedligeholdelsesnedetid            | Angiv vedligeholdelsesnedetid for en arbejdsordre.                                                                                                                                                                                                                               |
| Betingelsesvurdering            | Registrer målinger af tilstandsvurderinger på en arbejdsordre.                                                                                                                                                                                                             |
| Aktivtællere                 | Opret eller se tællerregistreringer på aktivet.                                                                                                                                                                                                                     |
| Prognose                        | Se eller opret budgetter på en arbejdsordre.                                                                                                                                                                                                                               |
| Journaler                        | Se eller opret arbejdsordrekladder. Kladdelinjer kan kopieres fra budgetter.                                                                                                                                                                                         |
| Projektposteringer            | Se alle bogførte transaktioner, der er relateret til de arbejdsordrer, som er oprettet for aktivet.                                                                                                                                                                                             |
| Opdatere tilstand for arbejdsordre           | Opdater livscyklustilstanden for en arbejdsordre.                                                                                                                                                                                                                                                |
| Log for livscyklustilstand                      | Se en log, der viser livscyklustilstande for den valgte arbejdsordre.                                                                                                                                                                                                                   |
| Aktivdokumenter                | Se listen over dokumenter, der er tilknyttet aktiver, som er relateret til en arbejdsordre. Disse dokumenter konfigureres i **Styring af aktiver** > **Opsætning** > **Aktivdokumenter**.                                                                                                 |
| Plan                        | Planlæg de valgte arbejdsordrer.                                                                                                                                                                                                                                      |
| Udsend            | Planlæg den valgte arbejdsordre for én arbejder.                                                                                                                                                                                                                        |
| Slet tidsplan                 | Slet planlægningen for den valgte arbejdsordre.                                                                                                                                                                                                                          |
| Planlagte vedligeholdelsesjob i arbejdsordrer             | Åbn listesiden **Planlagte vedligeholdelsesjob i arbejdsordrer**.                                                                                                                                                                                                                             |
| Indkøbsrekvisition for arbejdsordre | Åbn listesiden **Indkøbsrekvisition i arbejdsordre**.                                                                                                                                                                                                                 |
| Arbejdsordreindkøb             | Åbn listesiden **Indkøb i arbejdsordre**.                                                                                                                                                                                                                             |
| Omkostningsstyring                    | Sammenlign budgetomkostninger og faktiske omkostninger på arbejdsordren.                                                                                                                                                                                                                |
| Timestyring                    | Sammenlign budgetterede timer og faktiske timer på arbejdsordren.                                                                                                                                                                                                                |
| Arbejdsordrerapport               | Udskriv en arbejdsordrerapport.                                                                                                                                                                                                                                                |
| Arbejdsordreforbrug          | Udskriv en forbrugsrapport.                                                                                                                                                                                                                                               |


Knapperne under i gruppen **Projekt** under fanen **Arbejdsordre** i handlingsruden er relateret til funktioner i modulet **Projektstyring og regnskab** til budgetter, kladder og fakturering.

>[!NOTE]
>Budgetter, der oprettes på en arbejdsordre, kan inkluderes, når du kører behovsplanlægning, ved hjælp af den budgetmodel, der er valgt på siden **Parametre til aktivstyring**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]