---
title: Introduktion til arbejdsordrer
description: Dette emne indeholder en oversigt over arbejdsordrer i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875575"
---
# <a name="introduction-to-work-orders"></a>Introduktion til arbejdsordrer

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Arbejdsordrer bruges til at styre, angive nødvendige oplysninger for og registrere forbrug på vedligeholdelsesjob. En arbejdsordre kan indeholde et eller flere arbejdsordrejob, og et eller flere aktiver kan være tilknyttet en arbejdsordre. Hver arbejdsordrelinje definerer et vedligeholdelsesjob, der er planlagt på aktivet.

Arbejdsordrer kan være oprettet manuelt eller automatisk:

- Automatisk ved hjælp af formen **Planlægge vedligeholdelsesplaner** til kalenderbaserede vedligeholdelsesplaner, der er angivet til "Automatisk oprettelse".  

- Automatisk ved hjælp af formen **Planlæg vedligeholdelsesrunder** til vedligeholdelsesrunder, der er angivet til "Automatisk oprettelse".  

- Opret ud fra vedligeholdelsestidsplan, der kan være præventive vedligeholdelsesjob eller vedligeholdelsesanmodninger.  

- Opret en arbejdsordre manualt.  

- Opret en arbejdsordre ud fra **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger** eller **Vedligeholdelsesanmodninger for mine arbejdssteder**.

>[!NOTE]
>Arbejdsordrejob, der er relateret til samme aktiv, er relateret til samme projekt-id.

## <a name="all-work-orders"></a>Alle arbejdsordrer

Klik på **Styring af aktiver** > **Almindeligt** > **Arbejdsordrer** > **Alle arbejdsordrer** for at åbne listen. **Alle arbejdsordrer** indeholder en liste over alle arbejdsordrer og viser nogle af de oplysninger, der er relateret til en arbejdsordre.

![Figur 1](media/01-work-orders.png)

- Klik på **Styring af aktiver** > **Almindeligt** > **Arbejdsordrer** > **Aktive arbejdsordrer** for at se en liste over aktive arbejdsordrer.

- Klik på **Styring af aktiver** > **Almindeligt** > **Arbejdsordrer** > **Vedligeholdelsesjob med arbejdsordre for mit arbejdssted** for at få vist en liste over arbejdsordrejob, der indeholder aktiver, som er installeret på arbejdssteder, du er relateret til som arbejder (konfigureret i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md)).

- På listen (gittervisning) **Alle arbejdsordrer** skal du klikke på et link i kolonnen **Arbejdsordre** for at få vist detaljerne for den valgte post. Klik på knappen **Rediger** for at åbne den til redigering.  

- Detaljeoversigten viser detaljerede oplysninger, der er relateret til arbejdsordren.  

- Vælg linket **Linjer** i detaljevisningen for at få vist oplysninger om arbejdsordrejobbet, eller vælg linket **Overskrift** for at få vist oplysninger om arbejdsordren.  

- Den lodrette rude **Relaterede oplysninger** til højre på skærmen indeholder flere arbejdsordrerelaterede oplysninger. Udvid ruden for at se relaterede oplysninger om den valgte arbejdsordre.  


![Figur 2](media/02-work-orders.png)


Knapperne i handlingsruden er organiseret på faner. Her er en kort beskrivelse af de knapper, der er relateret til Styring af virksomhedsaktiv:



| Knapnavn                     | Beskrivelse                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rediger                            | Rediger den valgte arbejdsordre.                                                                                                                                                                                                                                           |
| Nyt                             | Opret ny arbejdsordre.                                                                                                                                                                                                                                                  |
| Slet                          | Slet den valgte arbejdsordre.                                                                                                                                                                                                                                         |
| Arbejdsordrepulje                 | Føj den valgte arbejdsordre til en arbejdsordrepulje, eller fjern den fra arbejdsordrepuljen.                                                                                                                                                                                           |
| Juster                          | Juster oplysninger om forventet start og afslutning, serviceniveau, ansvarlig vedligeholdelsesarbejder eller ansvarlig vedligeholdelsesarbejdergruppe på udvalgte arbejdsordrer.                                                                                                                                     |
| Relateret arbejdsordre              | Opret en ny arbejdsordre, der er relateret til det valgte arbejdsordrejob. Dette er nyttigt, hvis du vil registrere primære og sekundære arbejdsordrer.                                                                                                                              |
| Kopiér arbejdsordre                 | Opret en ny arbejdsordre ud fra en eksisterende arbejdsordre.                                                                                                                                                                                                                |
| Hændelseshistorik                   | Se registreringshistorikken på arbejdsordren.                                                                                                                                                                                                                |
| Noter til vedligeholdelsesjob i arbejdsordre                           | Opret en beskrivelse, eller Indsæt noter eller bemærkninger i en arbejdsordre. Start med at klikke på knappen **Tilføj tidsstempel** for at føje dit brugernavn og et tidsstempel til noten. Noter vises i formen **Arbejdsordre** > oversigtspanelet **Linjedetaljer** > fanen **Beskrivelse**. |
| Værktøjer                           | Opret en liste over nødvendige værktøjer på en arbejdsordre. Værktøjer oprettes som ressourcer i **Virksomhedsadministration** > **Generelt** > **Ressourcer** > **Ressourcer**.                                                                                                      |
| Vedligeholdelsestjekliste           | Se kontrolliste for det aktiv, der er tilknyttet arbejdsordren.                                                                                                                                                                                                              |
| Aktivfejl                     | Se eller registrer fejloplysninger om et aktiv, der skal bruges til fejlstyring.                                                                                                                                                                                        |
| Vedligeholdelsesnedetid            | Angiv vedligeholdelsesnedetid for en arbejdsordre.                                                                                                                                                                                                                               |
| Betingelsesvurdering            | Registrer målinger af tilstandsvurderinger på en arbejdsordre.                                                                                                                                                                                                             |
| Aktivtællere                 | Opret eller se tællerregistreringer på aktivet.                                                                                                                                                                                                                     |
| Prognose                        | Se eller opret budgetter på en arbejdsordre.                                                                                                                                                                                                                               |
| Journaler                        | Se eller opret arbejdsordrekladder. Kladdelinjer kan kopieres fra budgetter.                                                                                                                                                                                         |
| Projektposteringer            | Se alle bogførte transaktioner, der er relateret til de arbejdsordrer, som er oprettet for aktivet.                                                                                                                                                                                             |
| Opdatere tilstand for arbejdsordre                | Opdater livscyklustilstand for en arbejdsordre.                                                                                                                                                                                                                                                |
| Log for livscyklustilstand                       | Log, der viser livscyklustilstandene for den valgte arbejdsordre.                                                                                                                                                                                                                   |
| Aktivdokumenter                | Se en liste over dokumenter, der er tilknyttet aktiver, som er relateret til en arbejdsordre. Disse dokumenter konfigureres i **Styring af aktiver** > **Opsætning** > **Aktivdokumenter**.                                                                                                 |
| Plan                        | Planlæg de valgte arbejdsordrer.                                                                                                                                                                                                                                      |
| Udsend            | Planlæg den valgte arbejdsordre for én arbejder.                                                                                                                                                                                                                        |
| Slet tidsplan                 | Slet planlægning for den valgte arbejdsordre.                                                                                                                                                                                                                          |
| Planlagte vedligeholdelsesjob i arbejdsordrer             | Åbn listesiden **Planlagte vedligeholdelsesjob i arbejdsordrer**.                                                                                                                                                                                                                             |
| Indkøbsrekvisition for arbejdsordre | Åbn listesiden **Indkøbsrekvisition i arbejdsordre**.                                                                                                                                                                                                                 |
| Arbejdsordreindkøb             | Åbn listesiden **Indkøb i arbejdsordre**.                                                                                                                                                                                                                             |
| Omkostningsstyring                    | Sammenlign budgetomkostninger og faktiske omkostninger på arbejdsordren.                                                                                                                                                                                                                |
| Timestyring                    | Sammenlign budgetterede timer og faktiske timer på arbejdsordren.                                                                                                                                                                                                                |
| Arbejdsordrerapport               | Udskriv arbejdsordrerapport.                                                                                                                                                                                                                                                |
| Arbejdsordreforbrug          | Udskriv forbrugsrapport.                                                                                                                                                                                                                                               |


Knapperne under fanen **Arbejdsordre** > **Projektgruppe** er relateret til funktioner i modulet **Projektstyring og regnskab** i forbindelse med budgetter, kladder og fakturering.

>[!NOTE]
>Budgetter, der oprettes på en arbejdsordre, kan inkluderes, når der køres behovsplanlægning ved hjælp af den budgetmodel, der er valgt i formen **Parametre til aktivstyring**.

