---
title: Introduktion til arbejdssteder
description: Denne artikel indeholder en oversigt over arbejdssteder i Styring af aktiver.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
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
ms.openlocfilehash: 4a1c8c4db9aee68584ab35949745132091a34a58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882831"
---
# <a name="introduction-to-functional-locations"></a>Introduktion til arbejdssteder

[!include [banner](../../includes/banner.md)]

 

Denne artikel indeholder en oversigt over arbejdssteder i Styring af aktiver. Arbejdssteder er elementer af en teknisk struktur, såsom de funktionelle enheder i et system. Arbejdssteder oprettes hierarkisk, og du installerer aktiver på dem. Opsætningen af arbejdssteder i din virksomhed afhænger af virksomhedens behov.

Her er nogle eksempler på, hvordan du kan bruge arbejdssteder:

- **Funktionel** – arbejdsstederne kan være brugerorienterede og bruges til at styre aktiver, der har lignende adfærd.
- **Procesrelateret** – arbejdsstederne kan være arbejdsgangsorienterede.
- **Spatial** – arbejdsstederne kan repræsentere geografiske placeringer eller websteder.

Hvert arbejdssted styres uafhængigt i Styring af aktiver. Her er nogle af de mest nyttige funktioner ved arbejdssteder:

- Opsætning af specifikationer for arbejdssteder.
- Konfigurer krav til aktivspecifikation.
- Konfigurer vedligeholdelsessekvenser til forebyggende og reaktiv vedligeholdelse.
- Administrer installerede aktiver.
- Spor aktive anmodninger og arbejdsordrer, der er relateret til installerede aktiver.
- Spor fejl, der er registreret på aktiver.
- Spor vedligeholdelsesomkostninger på de aktiver, der er relateret til et arbejdssted på et givent tidspunkt.

Arbejdssteder giver mulighed for at spore aktiver i relation til anmodninger, arbejdsordrer, fejlregistreringer, tilstandsvurderinger, registreringer af produktionsstop og registreringer af aktivtæller.

> [!NOTE]
> Selvom et aktiv er blevet installeret på forskellige arbejdssteder i løbet af dets levetid, kan omkostningerne relateres til hvert sted. Med andre ord er aktivets omkostninger altid relateret til det arbejdssted, som aktivet blev installeret på på et givet tidspunkt.

Arbejdssteder er **ikke** fleksible. Når du har oprettet et arbejdsstedshierarki, kan du derfor ikke flytte rundt på stederne i det. 

Når du har oprettet et arbejdsstedshierarki, er det næste trin at installere aktiver på det. Du kan finde flere oplysninger under [Installer aktiver på arbejdssteder](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Alle arbejdssteder

Vælg **Styring af aktiver** \> **Almindelig** \> **Arbejdssteder** \> **Alle arbejdssteder** for at åbne listesiden **Alle arbejdssteder**. Denne side viser alle arbejdssteder og nogle af de oplysninger, der er relateret til hver. Hvis du kun vil have vist aktive arbejdssteder, skal du vælge **Aktive arbejdssteder**. Hvis du kun vil have vist de arbejdssteder, du er relateret til som arbejder, skal du vælge **Mine aktive arbejdssteder**. (Denne relation er oprettet på siden **Arbejdere**. Du finder flere oplysninger i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).)

På listesiden **Alle arbejdssteder** skal du vælge et link i kolonnen **Arbejdssteder** for at få vist detaljerne for den valgte post. Hvis du vil redigere arbejdsstedet, skal du vælge knappen **Rediger**. Detaljeoversigten viser detaljerede oplysninger, der er relateret til stedet. Den indeholder også en rude for **Relaterede oplysninger** i højre side. I denne rude vises hierarkiet for arbejdsstedet. Du kan udvide og skjule ruden **Relaterede oplysninger**.

Knapperne i Handlingsruden er organiseret på faner. Følgende tabel beskriver kort de knapper, der er relateret til Aktiv styring.

| Knapnavn                         | Beskrivelse                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Rediger                                | Skift mellem redigeringstilstand og visningstilstand for siden.                                                                                         |
| Nyt                                 | Opret et nyt arbejdssted.                                                                                                            |
| Slet                              | Slet det valgte arbejdssted.                                                                                                     |
| Omdøb                              | Omdøb det valgte arbejdssted.                                                                                                     |
| Kopiér arbejdsstedets struktur  | Kopiér arbejdsstedets hierarki.                                                                                                      |
| Installer aktiv                       | Installer et aktiv, herunder underordnede aktiver, på arbejdsstedet.                                                                        |
| Erstat aktiv                       | Erstat aktivhierarkiet med et andet aktivhierarki på arbejdsstedet.                                                         |
| Omkostningsstyring                        | Åbn siden **Omkostningsstyring for arbejdssted**, hvor du kan foretage en omkostningsberegning for det valgte arbejdssted.                |
| Timestyring                        | Åbn siden **Timestyring for arbejdssted**, hvor du kan foretage en omkostningsberegning for det valgte arbejdssted.                |
| Aktiver                              | Åbn siden **Alle aktiver**, hvor du kan få vist en liste over aktiver, der er relateret til det valgte arbejdssted.                      |
| Anmodninger                            | Åbn siden **Aktive anmodninger**, hvor du kan få vist en liste over anmodninger, der er relateret til det valgte arbejdssted.               |
| Arbejdsordrer                         | Åbn siden **Aktive arbejdsordrer**, hvor du kan få vist en liste over arbejdsordrer, der er relateret til det valgte arbejdssted.         |
| Fejl                              | Åbn siden **Fejl på aktiver**, hvor du kan få vist en liste over fejlregistreringer for aktiver, der er relateret til det valgte arbejdssted. |
| Opdater arbejdsstedets tilstand    | Opdater stadiet for det valgte arbejdssted.                                                                                        |
| Log for livscyklustilstand                 | Få vist en logfil, der viser stadierne for det valgte arbejdssted.                                                                        |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]