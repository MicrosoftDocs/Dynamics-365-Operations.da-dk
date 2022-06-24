---
title: Aktivere ensartet leveringsmåde for håndtering i e-handelskanaler
description: Denne artikel beskriver, hvordan du kan aktivere håndtering af ensartet leveringsmåde for at løse eventuelle problemer, der er relateret til gebyrflow i Microsoft Dynamics 365 Commerce-e-handelskanaler.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: f32f1915f8f7de1d5536b69b05bc74c6149dfda6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885579"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Aktivere ensartet leveringsmåde for håndtering i e-handelskanaler 

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du kan aktivere håndtering af ensartet leveringsmåde for at løse eventuelle problemer, der er relateret til gebyrflow i Microsoft Dynamics 365 Commerce-e-handelskanaler.

I Dynamics 365 Commerce anvendes der ikke som standard gebyrer på ikke-forholdsmæssigt overskriftsniveau i e-handelskanaler. Denne funktionsmåde kan forårsage en eller begge disse problemer i e-handelskanaler:

- Gebyrer på ikke-forholdsmæssigt overskriftsniveau vises ikke.
- Gebyrer for leveringsmåder er ikke ensartede mellem den valgte leveringsmåde og oversigten over ordrer ved kassen.

Du kan løse disse problemer ved at aktivere funktionen **Aktivér ensartet håndtering af leveringsmåde i kanal**. Denne funktion sikrer, at der vises gebyrer på ikke-forholdsmæssigt overskriftsniveau i e-handelskanaler, og at leveringsoplysninger for salgsordrer håndteres konsistent af samme arbejdsproces for anmodninger.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Aktivere funktionen Aktivér ensartet håndtering af leveringsmåde i kanal

Hvis du vil aktivere funktionen **Aktivér ensartet håndtering af leveringsmåde i kanal** i Commerce Headquarters, skal du følge disse trin.

1. Åbn arbejdsområdet **Funktionsstyring** (**Systemadministration \> Arbejdsområder \> Funktionsstyring**).
1. Søg efter og vælg **Aktivér ensartet håndtering af leveringsmåde i kanal** på listen over tilgængelige funktioner.
1. Vælg **Aktivér nu** i højre rude.
