---
title: Aktivere ensartet leveringsmåde for håndtering i e-handelskanaler
description: Dette emne beskriver, hvordan du kan aktivere håndtering af ensartet leveringsmåde for at løse eventuelle problemer, der er relateret til gebyrflow i Microsoft Dynamics 365 Commerce-e-handelskanaler.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 4cecd70dacd72572afc8e6cb65530bf2be4cc93d
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349942"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Aktivere ensartet leveringsmåde for håndtering i e-handelskanaler 

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du kan aktivere håndtering af ensartet leveringsmåde for at løse eventuelle problemer, der er relateret til gebyrflow i Microsoft Dynamics 365 Commerce-e-handelskanaler.

I Dynamics 365 Commerce anvendes der ikke som standard gebyrer på ikke-forholdsmæssigt overskriftsniveau i e-handelskanaler. Denne funktionsmåde kan forårsage en eller begge disse problemer i e-handelskanaler:

- Gebyrer på ikke-forholdsmæssigt overskriftsniveau vises ikke.
- Gebyrer for leveringsmåder er ikke ensartede mellem den valgte leveringsmåde og oversigten over ordrer ved kassen.

Du kan løse disse problemer ved at aktivere funktionen **Aktivér ensartet håndtering af leveringsmåde i kanal**. Denne funktion sikrer, at der vises gebyrer på ikke-forholdsmæssigt overskriftsniveau i e-handelskanaler, og at leveringsoplysninger for salgsordrer håndteres konsistent af samme arbejdsproces for anmodninger.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Aktivere funktionen Aktivér ensartet håndtering af leveringsmåde i kanal

Hvis du vil aktivere funktionen **Aktivér ensartet håndtering af leveringsmåde i kanal** i Commerce-hovedkontoret, skal du følge disse trin.

1. Åbn arbejdsområdet **Funktionsstyring** (**Systemadministration \> Arbejdsområder \> Funktionsstyring**).
1. Søg efter og vælg **Aktivér ensartet håndtering af leveringsmåde i kanal** på listen over tilgængelige funktioner.
1. Vælg **Aktivér nu** i højre rude.
