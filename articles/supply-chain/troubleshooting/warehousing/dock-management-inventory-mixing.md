---
title: Lagertyper blandes, når der bruges en dock-styringsprofil
description: For at dokstyringsprofilen kan håndtere blanding af lager effektivt, skal der først konfigureres en pause i arbejdshovedet. Denne side indeholder en forklaring på, hvordan du gør det.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475888"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Lagertyper blandes, når der bruges en dock-styringsprofil

## <a name="symptoms"></a>Symptomer

Du bruger *forsendelseskonsolideringspolitikker*. Du har konfigureret en *dokstyringsprofil* for en *lokationsprofil*, men når der oprettes arbejde, blandes lagertyperne på den endelige lokation.

## <a name="resolution"></a>Løsning

Profiler for dokstyring kræver, at arbejdet opdeles i forvejen. Med andre ord forventer dokstyringsprofilen, at der ikke vil være flere læg-lokationer i et arbejdshoved.

For at dokstyringsprofilen kan håndtere blanding af lager effektivt, skal der konfigureres en pause i arbejdshovedet.

I dette eksempel er vores dokstyringsprofil konfigureret sådan, at **Lagertyper, der ikke skal blandes**, er angivet til *Forsendelses-id*, og vi konfigurerer en arbejdshovedpause for den:

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Vælg den **Arbejdsordretype**, der skal redigeres (f.eks. *Indkøbsordrer*).
1. Vælg den arbejdsskabelon, du vil redigere.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. Åbn fanen **Sortering**, og tilføj en række med følgende indstillinger:
    - **Tabel** - *Midlertidige arbejdstransaktioner*
    - **Afledt tabel** - *Midlertidige arbejdstransaktioner*
    - **Felt** - *Forsendelses-id*
1. Vælg **OK**.
1. Du vender tilbage til siden **Arbejdsskabeloner**. Vælg **Opgaveoverskriften skifter** i handlingsruden.
1. Vælg **Rediger** i handlingsruden.
1. Markér det afkrydsningsfelt, der er tilknyttet **Feltnavnet** *Forsendelses-id*.
1. Vælg **Gem** i handlingsruden.
