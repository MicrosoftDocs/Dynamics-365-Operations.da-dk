---
title: "Afsende ordrer fra en anden butik ved hjælp af sendefunktionen Gebyr"
description: Dette emne beskriver sendefunktionen Gebyr.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: e5351086c56d13ef98937aec066be00cdf88fd37
ms.contentlocale: da-dk
ms.lasthandoff: 01/04/2019

---

# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Afsende ordrer fra en anden butik ved hjælp af sendefunktionen Gebyr

[!include [banner](includes/banner.md)]

Med sendefunktionen Gebyr i Dynamics 365 for Retail kan kundeordrer placeres i én butik og leveret fra en anden butik.

Kundeordrer i POS-klienten understøtter flere indstillinger til ordreopfyldelse. Nogle eksempler på indstillinger for ordreopfyldelse omfatter:

- Afhentning fra den samme butik på en anden dato.
- Afhentning fra en anden butik på den samme dato eller en anden dato.
- Afsendelse fra det standardforsendelseslagersted, der er tildelt til butikken, og levering på en bestemt dato.

Sendefunktionen Gebyr bruger følgende POS-handlinger: afsendelse af alle produkter og afsendelse af udvalgte produkter. Dette giver butiksmedarbejderen mulighed for at vælge den "afsend fra"-lokalitet, som ordren eller ordrelinjen kan opfyldes fra. Som standard er "afsend fra"-lokaliteten det forsendelseslagersted, der er knyttet til butikken. Butiksmedarbejderen kan dog ændre denne placering og vælge enhver butik, der er defineret i den butikssøgegruppe, der er tildelt til butikken.

Muligheden for at vælge "levér til"-adresser forbliver uændret.

De forsendelsesmetoder, der kan bruges til at opfylde ordrelinjen er baseret på konfigurationen af gyldige leveringsmåder for produkter og adresser. Da reglerne om gyldige leveringsmåder kun vedligeholdes i Retail Headquarters (Hovedkontoret), foretager POS-klienten et realtidsopkald for at hente de gyldige leveringsmåder for en forsendelseslinje.

