---
title: Konfigurere samhandel internt i firmaet
description: Denne artikel forklarer, hvordan du konfigurerer samhandel internt
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8d956c60db9f3acf2f1759dc3e1922da40d8a514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905625"
---
# <a name="set-up-intercompany-trade"></a>Konfigurere samhandel internt i firmaet

[!include [banner](../../includes/banner.md)]

Hvis du vil bruge Microsoft Dynamics 365 Supply Chain Management til intern handel, skal du konfigurere debitorer og kreditorer til at benytte intern handel. Du skal også konfigurere Kreditor, Debitor, Indkøb og forsyning, samt Salg og marketing.

## <a name="before-you-set-up-intercompany-trade"></a>Før opsætning af intern handel

Før du konfigurerer intern handel, skal du beslutte, hvilke debitorer er interne debitorer, og hvilke kreditorer er interne kreditorer. For hver juridisk enhed i Microsoft Dynamics 365 Supply Chain Management skal du beslutte, hvilken samhandelspolitik der skal anvendes i forbindelse med den enkelte interne debitor eller kreditor.

Det anbefales specielt, at du og din organisation får kendskab til de interne parametre.

- Diskuter konsekvenserne af konfigurationen med de ledere, der er ansvarlige for intern handel i de enkelte juridiske enheder.
- Konfigurer de relevante værdier for hver enkelt juridisk enhed.

## <a name="set-up-trading-relations"></a>Konfigurere handelsforhold

Brug følgende fremgangsmåde for at konfigurere intern handel for kreditorer og debitorer.

1. Gå til **Debitorer \> Kunder \> Alle kunder**.
1. Vælg en debitorkonto.
1. I handlingsruden skal du under fanen **Generelt** vælge **Intern**.
1. Angiv parametre for intern opsætning for kundekontoen. Disse parametre omfatter den juridiske enhed, der indeholder den tilsvarende kreditor og kreditorkonto. Parametrene omfatter også politikker for oprettelse af indkøbsordre, politikker for salgstilbud, værditilknytning og politikker for salgsaftaler og købsaftaler. Du også angive, om der skal bruges stamdataværdier fra kundekontoen eller fra leverandørkontoen i den anden juridiske enhed.
1. Gentag trin 1 til 4 for de resterende interne debitorer i den juridiske enhed.
1. Gå til **Kreditor \> Kreditorer \> Alle kreditorer**.
1. Vælg en kreditorkonto.
1. I handlingsruden skal du under fanen **Generelt** vælge **Intern**.
1. Angiv parametre for intern opsætning for leverandørkontoen. Disse parametre omfatter den juridiske enhed, der indeholder den tilsvarende debitor og debitorkonto. Parametrene omfatter også politik for salgstilbud, politik for oprettelse af indkøbsordre, værditilknytning og politikker for købsaftaler og salgsaftaler. Du også angive, om der skal bruges stamdataværdier fra leverandørkontoen eller fra kundekontoen i den anden juridiske enhed.
1. Gentag trin 6 til 9 for de resterende interne kreditorer i den juridiske enhed.

## <a name="set-up-products"></a>Konfigurere produkter

Brug følgende fremgangsmåde for at konfigurere intern handel for kreditorer og debitorer.

1. Gå til **Administration af produktoplysninger \> Produkter \> Alle produkter og produktmastere**.
1. Definer de produkter, der er frigivet til de juridiske enheder, hvor der skal være intern handel.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
