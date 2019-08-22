---
title: Vedligeholdelsesanmodninger
description: Dette emne indeholder en oversigt over administration af vedligeholdelsesanmodninger i Styring af aktiver
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 56d4abee451e6e22b9b9cc2fd36a13648202e7df
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847430"
---
# <a name="maintenance-requests"></a>Vedligeholdelsesanmodninger

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Vedligeholdelsesanmodninger er noter eller erklæringer, som er oprettet med henblik på at underrette en leder eller planlægger om, at et aktiv muligvis kræver et vedligeholdelses-eller reparationsjob, men som ikke kræver, at der oprettes en arbejdsordre. Hvis indholdet af en vedligeholdelsesanmodning anses for at være gyldigt, kan der derefter oprettes en arbejdsordre på grundlag af vedligeholdelsesanmodningen.

Der kan oprettes vedligeholdelsesanmodninger for alle aktiver i Styring af aktiver. Der kan oprettes forskellige typer vedligeholdelsesanmodninger afhængigt af, hvordan din virksomhed anvender vedligeholdelsesanmodninger. Her er nogle eksempler:

- Vedligeholdelsesanmodninger
- Kommentarer
- Rettelser eller forbedringer
- Investeringer
- Reparation af depot (denne type anvendes, når du modtager aktiver fra et andet sted, for at gøre det muligt for dig at udføre et vedligeholdelses-eller reparationsjob, og du derefter returnerer aktivet, når jobbet er fuldført).

## <a name="view-maintenance-requests"></a>Se vedligeholdelsesanmodninger

Hvis du have vist vedligeholdelsesanmodninger, skal vælge **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Alle vedligeholdelsesanmodninger**, **Aktive vedligeholdelsesanmodninger** eller **Vedligeholdelsesanmodninger for mine arbejdssteder**. Hver listeside viser nogle af de oplysninger, der er relateret til en vedligeholdelsesanmodning.

![Figur 1](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Brug listesiden **Vedligeholdelsesanmodninger for mine arbejdssteder** for at få vist en liste over vedligeholdelsesanmodninger, der indeholder enten arbejdssteder, som du er relateret til som arbejder, eller aktiver, der er installeret på de arbejdssteder, som du er relateret til som arbejder. (Du finder oplysninger om, hvordan du konfigurerer arbejdssteder for vedligeholdelsesarbejdere, i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Selvom kundekontooplysninger er tilgængelige i Styring af tjenesten for aktiver (ekstern vedligeholdelse), er de ikke tilgængelig i Styring af aktiver (intern vedligeholdelse).

For at åbne detaljevisning for en post skal du i gittervisningen på listesiden **Alle vedligeholdelsesanmodninger** vælge et link i kolonnen **Vedligeholdelsesanmodning**.

![Figur 2](media/02-manage-maintenance-requests.png)

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

