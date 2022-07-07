---
title: Vedligeholdelsesanmodninger
description: Denne artikel indeholder en oversigt over administration af vedligeholdelsesanmodninger i Styring af aktiver
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 488b6505aba246aa3a6ea69436514a274403bf49
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015632"
---
# <a name="maintenance-requests"></a>Vedligeholdelsesanmodninger

[!include [banner](../../includes/banner.md)]

Vedligeholdelsesanmodninger er noter eller erklæringer, som er oprettet med henblik på at underrette en leder eller planlægger om, at et aktiv muligvis kræver et vedligeholdelses-eller reparationsjob, men som ikke kræver, at der oprettes en arbejdsordre. Hvis indholdet af en vedligeholdelsesanmodning anses for at være gyldigt, kan der derefter oprettes en arbejdsordre på grundlag af vedligeholdelsesanmodningen.

Der kan oprettes vedligeholdelsesanmodninger for alle aktiver i Styring af aktiver. Der kan oprettes forskellige typer vedligeholdelsesanmodninger afhængigt af, hvordan din virksomhed anvender vedligeholdelsesanmodninger. Her er nogle eksempler:

- Vedligeholdelsesanmodninger
- Kommentarer
- Rettelser eller forbedringer
- Investeringer
- Reparation af depot (denne type anvendes, når du modtager aktiver fra et andet sted, for at gøre det muligt for dig at udføre et vedligeholdelses-eller reparationsjob, og du derefter returnerer aktivet, når jobbet er fuldført).

## <a name="view-maintenance-requests"></a>Vis vedligeholdelsesanmodninger

Hvis du have vist vedligeholdelsesanmodninger, skal vælge **Styring af aktiver** \> **Vedligeholdelsesanmodninger** \> **Alle vedligeholdelsesanmodninger**, **Aktive vedligeholdelsesanmodninger** eller **Vedligeholdelsesanmodninger for mine arbejdssteder**. Hver listeside viser nogle af de oplysninger, der er relateret til en vedligeholdelsesanmodning.

![Vis vedligeholdelsesanmodninger.](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Brug listesiden **Vedligeholdelsesanmodninger for mine arbejdssteder** for at få vist en liste over vedligeholdelsesanmodninger, der indeholder enten arbejdssteder, som du er relateret til som arbejder, eller aktiver, der er installeret på de arbejdssteder, som du er relateret til som arbejder. (Du finder oplysninger om, hvordan du konfigurerer arbejdssteder for vedligeholdelsesarbejdere, i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Selvom kundekontooplysninger er tilgængelige i Styring af tjenesten for aktiver (ekstern vedligeholdelse), er de ikke tilgængelig i Styring af aktiver (intern vedligeholdelse).

For at åbne detaljevisning for en post skal du i gittervisningen på listesiden **Alle vedligeholdelsesanmodninger** vælge et link i kolonnen **Vedligeholdelsesanmodning**.

![Se detaljer om vedligeholdelsesanmodning.](media/02-manage-maintenance-requests.png)

Knapperne i Handlingsruden er organiseret på faner. Følgende tabel beskriver kort de knapper, der er relateret til Aktiv styring.

| Knapnavn                      | Beskrivelse |
|----------------------------------|-------------|
| Rediger                             | Rediger den valgte vedligeholdelsesanmodning. |
| Nyt                              | Opret en ny vedligeholdelsesanmodning. |
| Slet                           | Slet den valgte vedligeholdelsesanmodning. |
| Arbejdsordrepulje                  | Knyt den valgte vedligeholdelsesanmodning til en arbejdsordrepulje. |
| Arbejdsordre                       | Opret en arbejdsordre på grundlag af den valgte vedligeholdelsesanmodning. |
| Fejl for aktivet                      | Klik på **Fejl for aktivet**, hvor du kan oprette en fejlregistrering på den valgte vedligeholdelsesanmodning. |
| Arbejdsordrer                      | Viser en liste over alle arbejdsordrer, der er knyttet til den valgte vedligeholdelsesanmodning. |
| Opdater tilstanden for vedligeholdelsesanmodningen | Opdater tilstanden for vedligeholdelsesanmodningen. |
| Log for livscyklustilstand              | Se en log, der viser livscyklustilstande for den valgte vedligeholdelsesanmodning. |
| Detaljer for vedligeholdelsesanmodning.      | Udskriv en rapport, der viser detaljerne for den valgte vedligeholdelsesanmodning. |
| Send udlånsaktiv                  | Vælg et udlånsaktiv, der skulle have været en midlertidig erstatning for det aktiv, der er valgt i den valgte vedligeholdelsesanmodning. |
| Returner udlånsaktivet                | Registrer udlånsaktivet som returneret. |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]