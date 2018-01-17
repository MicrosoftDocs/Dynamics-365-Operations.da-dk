---
title: Levere en ordre fra en anden butik
description: Dette emne beskriver sendefunktionen Gebyr.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 986ec7835dac52c326085c47313205d08b1bafa8
ms.openlocfilehash: d217bc31ad9d93c5440e5329f7b7327d089137f4
ms.contentlocale: da-dk
ms.lasthandoff: 10/10/2017

---

# <a name="ship-an-order-from-a-different-store"></a>Levere en ordre fra en anden butik

Med sendefunktionen Gebyr i Dynamics 365 for Retail kan kundeordrer placeres i én butik og leveret fra en anden butik. Kundeordrer i POS-klienten understøtter flere indstillinger til ordreopfyldelse. Nogle eksempler på indstillinger for ordreopfyldelse omfatter:
-   Afhentning fra den samme butik på en anden dato.
-   Afhentning fra en anden butik på den samme dato eller en anden dato.
-   Afsendelse fra det standardforsendelseslagersted, der er tildelt til butikken, og levering på en bestemt dato.

Sendefunktionen Gebyr bruger følgende POS-handlinger: afsendelse af alle produkter og afsendelse af udvalgte produkter. Dette giver butiksmedarbejderen mulighed for at vælge den "afsend fra"-lokalitet, som ordren eller ordrelinjen kan opfyldes fra. Som standard er "afsend fra"-lokaliteten det forsendelseslagersted, der er knyttet til butikken. Butiksmedarbejderen kan dog ændre denne placering og vælge enhver butik, der er defineret i den butikssøgegruppe, der er tildelt til butikken. 

Muligheden for at vælge "levér til"-adresser forbliver uændret. 

De forsendelsesmetoder, der kan bruges til at opfylde ordrelinjen er baseret på konfigurationen af gyldige leveringsmåder for produkter og adresser. Da reglerne om gyldige leveringsmåder kun vedligeholdes i Retail Headquarters (Hovedkontoret), foretager POS-klienten et realtidsopkald for at hente de gyldige leveringsmåder for en forsendelseslinje. 


