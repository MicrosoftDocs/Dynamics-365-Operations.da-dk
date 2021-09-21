---
title: Der kan ikke indsættes aktiv version af stykliste- og rutenumre
description: Hvis På standard-websted og -lagersted allerede er defineret for et udvalgt produkt, bliver du ikke bedt om at indsætte den aktive version af stykliste- og rutenumre.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475857"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Stykliste og rute kan ikke indsættes, når der oprettes en ny produktionsordre

## <a name="symptoms"></a>Symptomer

Når du opretter en ny produktionsordre, når du angiver varenummeret, angives felterne **Lokation** og **Lagersted** automatisk til den standardlokation og det lagersted, der er defineret på siden **Standardordreindstillinger** for den færdige vare. Desuden angives det aktive styklistenummer og det aktive rutenummer automatisk, så du modtager ikke følgende meddelelse, der beder dig om følgende værdier:

> Vil du indsætte den aktive version af stykliste og rute?

## <a name="resolution"></a>Løsning

Du bliver ikke bedt om at indsætte stykliste- og rutenumre, hvis du vælger et produkt, som der allerede er defineret en lokation og et lagersted for, på siden **Standardordreindstillinger**. Du bliver kun spurgt, hvis disse værdier ikke er defineret for det valgte produkt.
