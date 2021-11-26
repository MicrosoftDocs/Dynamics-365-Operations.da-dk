---
title: Problemfrit offline skift til gavekort- og kreditnotahandlinger
description: Dette emne indeholder en oversigt over forbedringer, der giver en problemfri offline skift til bestemte betalingstyper.
author: BrianShook
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 59f1a0b213bd22906ba8b2c3e7da38a9818f6d4f
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779486"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Problemfrit offline skift til gavekort- og kreditnotahandlinger

[!include [banner](../includes/banner.md)]

Hvis en kasse enhed mister forbindelsen til kanaldatabasen, kan de fleste POS-handlinger og -transaktioner, der var i gang, fortsætte, når kassereren har modtaget en advarselsmeddelelse om tab af forbindelsen. I nogle tilfælde har transaktioner dog elementer, der er afhængige af realtids-service, og disse elementer understøttes ikke, når kasseapparatet er offline. I dette emne beskrives nogle funktioner, der hjælper med at reducere virkningen af tabte forbindelser i disse scenarier.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>Afslutning af gavekorttransaktioner i offlinetilstand

Interne gavekort afhænger af realtidsservice, fordi saldoen for gavekortene skal vedligeholdes centralt i Microsoft Dynamics 365 Commerce Headquarters. Gavekort låses, så snart de føjes til en transaktion, for at hjælpe med at forhindre svindel eller andre synkroniseringsproblemer. Låsningsfunktionen sikrer, at et gavekort ikke kan bruges på flere terminaler på samme tid. Når en transaktion er gennemført, opdateres og låses gavekortet op.

Hvis kasseapparatet imidlertid mister forbindelsen, når et gavekort er blevet føjet til en transaktion, kan gavekortet måske ikke bruges. Dynamics 365 Commerce har en parameter, der gør det muligt at fuldføre transaktioner, der omfatter en gavekortserie, mens kasseapparatet er offline, så denne situation forhindres. Når denne parameter er slået til, vil gavekorttransaktioner, der er tvunget offline, blive gemt sammen med offline transaktioner, og de vil blive synkroniseret til Commerce Headquarters, når offline transaktionerne synkroniseres. Synkroniseringen låser også gavekortet, så det kan bruges i en anden terminal.

Hvis du vil aktivere funktionaliteten til at indgå gavekorttransaktioner efter skift til offlinetilstand, skal du gå til fanen **Bogføring** på siden **Commerce-parametre**. Under denne fane skal du finde oversigtspanelet **Gavekort** og indstille **Tillad afslutning af gavekorttransaktioner i offlinetilstand** til **Ja**.

![Indstillinger for et offline gavekort.](../media/gift.png)

Commerce-parametrene lagres typisk i cachen. Når indstillingen af denne parameter opdateres, og distributionsplanen er startet for at synkronisere ændringen til kanalen, kan ændringen derfor tage op til 24 timer for at træde i kraft. Hvis ændringen skal træde i kraft øjeblikkeligt, skal du nulstille Microsoft Internet Information Services (IIS).

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>Afslutning af kreditnotatransaktioner i offlinetilstand

Ligesom interne gavekort vedligeholdes kreditnotaer centralt i Commerce Headquarters. Commerce har en parameter, der giver mulighed for, at kreditnotatransaktioner kan afsluttes, mens kasseapparatet er offline. Denne parameter fungerer på samme måde som den gavekortparameter, der blev nævnt i forrige afsnit. Når parameteren er aktiveret, vil kreditnotatransaktioner, der er tvunget offline, blive synkroniseret tilbage til kanaldatabasen sammen med andre transaktioner, der blev udført, mens kasseapparatet var offline.

Hvis du vil aktivere funktionaliteten til at indgå kreditnotatransaktioner efter skift til offlinetilstand, skal du gå til fanen **Bogføring** på siden **Commerce-parametre**. Under denne fane skal du finde oversigtspanelet **Kreditnota** og indstille **Tillad afslutning af kreditnotatransaktioner i offlinetilstand** til **Ja**.

![Indstilling for offline kreditnota.](../media/creditmemo.png)

Commerce-parametrene lagres typisk i cachen. Når indstillingen af denne parameter opdateres, og distributionsplanen er startet for at synkronisere ændringen til kanalen, kan ændringen derfor tage op til 24 timer for at træde i kraft. Nulstil IIS, hvis ændringen skal træde i kraft øjeblikkeligt.

## <a name="related-topics"></a>Relaterede emner

- [Offline POS-funktionalitet (Point Of Sale)](../pos-offline-functionality.md)
- [POS-handlinger, online og offline](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]