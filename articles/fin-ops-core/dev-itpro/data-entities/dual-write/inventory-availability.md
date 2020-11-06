---
title: Lagertilgængelighed i dobbeltskrivning
description: I dette emne får du oplysninger om, hvordan du kontrollerer lagertilgængelighed i dobbeltskrivning.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997886"
---
# <a name="inventory-availability-in-dual-write"></a>Lagertilgængelighed i dobbeltskrivning

[!include [banner](../../includes/banner.md)]

Ved hjælp af lagertilgængelighed kan du kontrollere dit lager, før du føjer et produkt til siden **Tilbud** , **Ordrer** eller **Fakturaer** i Microsoft Dynamics 365 Sales. Kontrol af lager og fastlæggelse af en opfyldelsesdato er f.eks. en nøgleopgave i processen for [kundeemne til kontant](dual-write-prospect-to-cash.md).

Hvis du ikke har tilstrækkelig lagerbeholdning, kan du estimere en leveringsdato ud fra projekterede lagertilgange og -afgange. Du kan også kontrollere produktets DTT-oplysninger (disponibelt til tilsagn), hvor du kan finde DTT-antallet i den foruddefinerede tidshorisont.

## <a name="on-hand-inventory"></a>Disponibel lagerbeholdning

I sidehovedet for formularerne **Tilbud** , **Ordrer** og **Fakturaer** i Dynamics 365 Sales er der tilføjet en ny knap **Disponibel lagerbeholdning**. Når du vælger knappen, vises en dialogboks, hvor du kan angive det firma og det produkt, som den disponible lagerbeholdning skal kontrolleres for. I denne dialogboks vises de samme oplysninger som [disponibel lagerbeholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Dialogboksen returnerer lageroplysningerne fra Dynamics 365 Supply Chain Management. Disse oplysninger indeholder følgende antal:

- Beholdningsantal
- Reserveret disponibelt antal
- Tilgængeligt disponibelt antal
- Bestilt antal
- Antal i bestilling
- Reserveret bestilt mængde
- Disponibelt antal i alt

## <a name="atp-information"></a>DTT-oplysninger

I Sales er der føjet en ny knap for **DTT-oplysninger** til linjeelementer på siderne **Tilbud** , **Ordrer** og **Fakturaer**. Når du vælger knappen, vises en dialogboks, hvor du kan angive firma, produkt, lagerlokation, lagersted og ordreantal. Denne dialogboks har de samme indstillinger, som er beskrevet under [Ordretilsagn](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Dialogboksen returnerer DTT-oplysningerne fra Supply Chain Management. Disse oplysninger indeholder følgende antal:

- DTT-antal
- Tilgangsantal
- Afgangsantal
- Beholdningsantal
