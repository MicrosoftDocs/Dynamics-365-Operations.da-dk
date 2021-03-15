---
title: Produktionsudlagringslokation
description: I dette emne beskrives det hierarki, der bruges til at identificere produktionsudlagringslokationen.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d8d28b9670d8752c1039684551d56b1779a10b20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001593"
---
# <a name="production-output-location"></a>Produktionsudlagringslokation

[!include [banner](../includes/banner.md)]

I dette emne beskrives det hierarki, der bruges til at identificere produktionsudlagringslokationen.

Produktionsudlagringslokationen er det sted, hvor en færdigvare er først gemmes, når den er produceret. Normalt er dette sted tæt på den produktionsproces, der fremstiller færdigvaren. Produktionsudlagringslokationen bruges som mellemoplagring for materialet, før det flyttes området for forsendelsen, en lagerlokation, en produktionsindlagringslokation for en downstream-produktionsproces osv. 

En standardproduktionsudlagringslokation angives, når færdigvarer er rapporteret for en produktionsordre eller en batchordre. Følgende hierarki bruges til at identificere denne udlagringslokation:

1. Brug den udlagringslokation, der er defineret i produktionsordre- eller batchordrehovedet.
2. Hvis der ikke findes en lokation der, kan du bruge den udlagringslokation, der er defineret i den ressource, der bruges af den sidste handling, der er defineret i produktionsruten.
3. Hvis der ikke findes en lokation der, kan du bruge den udlagringslokation, der er defineret i den ressourcegruppe, der bruges af ressourcen for den sidste handling, der er defineret i produktionsruten.
4. Hvis der ikke findes en lokation der, kan du bruge den udlagringslokation, der er defineret for det lagersted, der er defineret for produktionsordren.

En standardproduktionsudlagringslokation angives kun for produkter, der er oprettet ved hjælp af avancerede lagerprocesser. Når denne varetype er færdigmeldt, oprettes lagerstedsarbejde af typen **Færdige varer, læg på lager** eller **Samprodukt og biprodukt, læg på lager**. Denne type arbejde bruger produktionsudlagringslokationen som pluklokation. Læg-på-lager-lokationen bestemmes af lokationsvejledningerne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]