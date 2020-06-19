---
title: Lagertilgængelighed i dobbeltskrivning
description: I dette emne får du oplysninger om kontrol af lagertilgængelighed i dobbeltskrivning.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426976"
---
# <a name="inventory-availability"></a>Lagertilgængelighed

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Ved hjælp af lagertilgængelighed kan du kontrollere dit lager, før du føjer et produkt til formularerne **Tilbud**, **Ordrer** eller **Fakturaer** i modelbaserede apps i Dynamics 365. Kontrol af lager og fastlæggelse af en opfyldelsesdato er f.eks. en hovedopgave i [processen for kundeemne til kontant](dual-write-prospect-to-cash.md). Hvis du ikke har tilstrækkelig lagerbeholdning, kan du estimere en leveringsdato ud fra projekterede lagertilgange og -afgange. Du kan også kontrollere produktets DTT-oplysninger (disponibelt til tilsagn), hvor du kan finde DTT-antallet i den foruddefinerede tidshorisont.

## <a name="on-hand-inventory"></a>Disponibel lagerbeholdning 

I sidehovedet for formularerne **Tilbud**, **Ordrer** eller **Fakturaer** i Dynamics 365 Sales er der tilføjet en ny knap **Disponibel lagerbeholdning**. Når du klikker på knappen, vises en dialogboks, og du kan angive det firma og det produkt, som den disponible lagerbeholdning skal kontrolleres for. Den returnerer lageroplysningerne fra Dynamics 365 Supply Chain Management og viser de samme oplysninger som [Disponibel lagerbeholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md). Oplysningerne omfatter disse antal:

- **Disponibelt antal**
- **Reserveret disponibelt antal**
- **Tilgængeligt disponibelt antal**
- **Bestilt antal**
- **Antal i bestilling**
- **Reserveret bestilt antal**
- **Disponibelt antal i alt**

## <a name="atp-information"></a>DTT-oplysninger

Til linjeelementerne på formularerne **Tilbud**, **Ordrer** eller **Fakturaer** i Dynamics 365 Sales er der føjet en ny knap **DTT-oplysninger**. Når du klikker på knappen, vises en dialogboks, og du kan angive firma, produkt, lagersted, lagervarehus og ordreantal. Den returnerer **DTT-oplysningerne** fra Supply Chain Management og viser indstillingerne beskrevet i [Ordretilsagn](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations). Oplysningerne omfatter **DTT-antal**, **Tilgangsantal**, **Afgangsantal** og **Disponibelt antal**.
