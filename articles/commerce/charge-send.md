---
title: Afsende ordrer fra en anden butik ved hjælp af sendefunktionen Gebyr
description: Dette emne beskriver sendefunktionen Gebyr.
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 8c9c435c9ef8f692551a216d72a76f8a71b4ce6dc03dc6b13c23364a0aa81662
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746693"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Afsende ordrer fra en anden butik ved hjælp af sendefunktionen Gebyr

[!include [banner](includes/banner.md)]

Med sendefunktionen Gebyr i Commerce kan kundeordrer placeres i én butik og leveres fra en anden butik.

Kundeordrer i POS-klienten understøtter flere indstillinger til ordreopfyldelse. Nogle eksempler på indstillinger for ordreopfyldelse omfatter:

- Afhentning fra den samme butik på en anden dato.
- Afhentning fra en anden butik på den samme dato eller en anden dato.
- Afsendelse fra det standardforsendelseslagersted, der er tildelt til butikken, og levering på en bestemt dato.

Sendefunktionen Gebyr bruger følgende POS-handlinger: afsendelse af alle produkter og afsendelse af udvalgte produkter. Dette giver butiksmedarbejderen mulighed for at vælge den "afsend fra"-lokalitet, som ordren eller ordrelinjen kan opfyldes fra. Som standard er "afsend fra"-lokaliteten det forsendelseslagersted, der er knyttet til butikken. Butiksmedarbejderen kan dog ændre denne placering og vælge enhver butik, der er defineret i den butikssøgegruppe, der er tildelt til butikken.

Muligheden for at vælge "levér til"-adresser forbliver uændret.

De forsendelsesmetoder, der kan bruges til at opfylde ordrelinjen er baseret på konfigurationen af gyldige leveringsmåder for produkter og adresser. Da reglerne om gyldige leveringsmåder kun vedligeholdes i Headquarters (Hovedkontoret), foretager POS-klienten et realtidsopkald for at hente de gyldige leveringsmåder for en forsendelseslinje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]