---
title: Fejlfinding i Dynamics 365 Payment Connector for Adyen-problemer
description: Dette emne indeholder fejlfindingsvejledning, der kan hjælpe dig med at få support, når du har problemer med Microsoft Dynamics 365 Payment Connector for Adyen.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f01db3fa670355696c094be544775a3abc557a70
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585242"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a>Fejlfinding i Dynamics 365 Payment Connector for Adyen-problemer

[!include [banner](../../includes/banner.md)]

Dette emne indeholder fejlfindingsvejledning, der kan hjælpe dig med at få support, når du har problemer med Microsoft Dynamics 365 Payment Connector for Adyen.

## <a name="description"></a>Betegnelse

Du har problemer med Dynamics 365 Payment Connector for Adyen i følgende områder, og du har brug for support fra Adyen-teamet:

- POS (Configuration of Point of sale), MPOS (Modern Point of sale), call center eller Dynamics 365 Commerce
- Adyens betalingsserviceudbyders (PSP) referencenummer (f.eks. hvis du har spørgsmål om afvisning, herunder manuel indtastning af \[MKE\]-afvisning)
- Alt, hvad der ikke fungerer i testmiljøer eller live forhandlermiljøer

## <a name="resolution"></a>Løsning

Du kan bruge følgende mailskabelon til at starte supportprocessen med Adyen-teamet. Hvis du vil foretage fejlfinding, skal du sørge for, at mailen indeholder alle de nødvendige oplysninger.

| Felt        | Værdi |
|--------------|-------|
| Til           | `support@adyen.com` |
| Cc           | |
| Emnelinje | Microsoft Dynamics Supportanmodning |
| Tekst         | <p>Hej Support</p><p>Giv support til følgende problem:</p><ul><li>Handlendes konto</li><li>Miljø (Test/Prod)</li><li>Kanal (POS/callcenter/Handel e-handel)</li><li>PSP-referencenummer, hvis der indgår en bestemt transaktion i problemet (du kan finde PSP-referencenummeret på kvitteringen i kundeområdet Adyen eller i transaktionsmenuen på POS-terminalen.)</li><li>Skærmbillede eller billede af fejlmeddelelsen, hvis det er relevant</li><li>Logfiler til hændelsesvisning (i .txt-format)</li><li>Beskrivelse af de trin til problem- og fejlfinding, som du har forsøgt</li></ul> |

## <a name="additional-resources"></a>Yderligere ressourcer

[Accepter betalinger med Adyen-connector til Dynamics 365 Commerce](https://www.adyen.com/partners/dynamics-365-commerce)

[Dynamics 365-betalingsconnector til Adyen](../dev-itpro/adyen-connector.md)

[Konfigurer Adyen-betalingsconnector til Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
