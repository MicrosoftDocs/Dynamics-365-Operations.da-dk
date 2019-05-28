---
title: Finanskladdetyper
description: Dette emne beskriver de kladdetyper, du har angivet for økonomikladder.
author: ShylaThompson
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fff557d20a230922b5512aea9e49aa9993a694dd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543669"
---
# <a name="ledger-journal-types"></a>Finanskladdetyper

[!include [banner](../includes/banner.md)]

Dette emne beskriver de kladdetyper, du har angivet for økonomikladder. Brug siden **Kladdenavne** til at konfigurere kladder, som du kan bruge i hele Microsoft Dynamics 365 for Finance and Operations.

| Kladdetype                      | Formål                       | Angive posteringer på denne side                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Tildeling                        | Opret fordelingsposter i en fordelingskladde. Før du kan oprette en fordelingskladde, skal du oprette en fordelingsregel på siden **Finansfordelingsregel**.      | Udfør fordelingsanmodning             |
| Godkendelse                          | Bogfør kreditorfakturaer, der er godkendt, på de relevante finanskonti.  | Godkendelseskladde                                       |
| Tilbageførsel af bankcheck               | Tilbagefør en bogført check. For at bruge denne kladdetype skal du vælge indstillingen **Brug evalueringsprocessen til annullering af checks** på siden **Likviditets- og bankstyringsparametre**.   | Tilbageførsel af checks, Annullering af checks                   |
| Annullering af bankindbetalingsbildrag    | Annuller et indbetalingsbilag. For at bruge denne kladdetype skal du vælge indstillingen **Brug evalueringsprocessen til annullering af indbetalingsbilag** på siden **Likviditets- og bankstyringsparametre**.   | Annulleringer af betalinger af indbetalingsbilag            |
| Budget                            | Behandl budgetbevillinger. For at bruge denne kladdetype skal du vælge indstillingen **Aktivér budgetdisponering** på siden **Økonomiparametre**. Budgetkladdeposterne omfatter oplysninger, der er baseret på de finanskonti, der er defineret på siden **Bogføringsdefinitioner**.                                                        |                                                                |
| Debitoraccept af veksel  | Opret debitoracceptposter for veksler.             | Udsted vekseljournal, Genudsted vekseljournal |
| Debitorbankremittering          | Opret en vekselremitteringsfil, der kan sendes til virksomhedens bank. Du kan bruge denne kladdetype ved at fjerne indstillingen **Automatisk udligning** på siden **Debitor** **parametre**.            | Remittering                                                     |
| Debitorudstedelse af veksel    | Opret debitortransaktioner for udstedelse af veksel. For at bruge denne kladdetype skal du fjerne indstillingen **Opret og bogfør automatisk udstedelseskladde ved bogføring af fakturaer** på siden **Betalingsmåder - debitorer**.   | Kladde til udstedelse af veksel                                  |
| Debitorbetaling                  | Opret debitorbetalingsposter.                             | Betalingskladde             |
| Debitorprotest af veksel | Opret debitortransaktioner for protest af veksel.                    | Protester vekseljournal                               |
| Debitorgenudstedelse af veksel  | Opret transaktioner for debitorgenudstedelse af veksler.                     | Genudsted vekseljournal                                |
| Debitorudligning af veksel  | Opret debitortransaktioner for udligning af veksel.                       | Udlign vekseljournal                                |
| Dagligt                             | Opret daglige posteringer i en finanskladde.                          | Finanskladde                                                |
| Eliminering                       | Opret elimineringsposter i en elimineringskladde. For at bruge denne kladdetype skal du vælge indstillingerne **Brug til økonomisk eliminering** og **Brug til økonomisk konsolidering** på siden **Juridiske enheder**. Før du kan bruge denne kladdetype skal du oprette en finanselimineringsregel på siden **Elimineringsregel i Finans**. | Eliminering                                                    |
| Anlægsaktivbudget                | Opret poster i budgetregisteret for anlægsaktiver.                                                                                                                                                                                                                                                                                                                 | Anlægsaktivbudget                                             |
| Godkendelseskladde                  | Registrer grundlæggende oplysninger om kreditorfakturaer.                                                                                                                                                                                                                                                                                                           | Godkendelseskladde                                               |
| Lønudbetaling              | Udsted betalinger, der er baseret på lønafdelingens lønsedler. Du kan ikke angive transaktioner manuelt i denne kladde. Du skal generere lønsedler og derefter sende disse lønsedler til betaling.                                                                                                                                                              |                                                                |
| Periodisk                          | Opret posteringer i den periodiske kladde.                                                                                                                                                                                                                                                                                                      | Periodiske kladder                                              |
| Bogføring af anlægsaktiver                 | Bogfør anlægsaktivposter.                                                                                                                                                                                                                                                                                                                              | Anlægsaktiver                                                   |
| Projekt - udgifter                | Opret projektets udgiftsposter.                                                                                                                                                                                                                                                                                                                        | Expense                                                        |
| Regulering af rapporteringsvaluta     | Opret reguleringer i rapporteringsvalutaen saldi på finanskonti.               | Reguleringskladder for rapporteringsvaluta                         |
| Statistikposter            | Opret statistikposter.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Kreditorbankremittering            | Opret en egenvekselremitteringsfil, der kan sendes til virksomhedens bank.                                                                                                                                                                                                                                                                      | Remitteringskladde                                             |
| Kreditorbetaling               | Opret kreditorbetalingsposter.                                                                                                                                                                                                                                                                                                                    | Betalingskladde                                                |
| Kreditorudstedelse af egenveksel       | Tegn egenveksler til leverandøren som en metode til betaling. For at bruge denne kladdetype skal du fjerne indstillingen **Opret og bogfør automatisk udstedelseskladde ved bogføring af fakturaer** på siden **Betalingsmåder - kreditorer**.                                                                                                                                          | Kladde for udstedelse af egenveksel                                   |
| Kreditorfakturapulje uden bogføring | Opret kreditorfakturaposteringer, der endnu ikke er bogført til en midlertidig ankomstkonto.                                                                                                                                                                                                                                                             | Kreditorfakturapulje ekskl. bogføringsdetaljer                  |
| Kreditorfakturapulje               | Opret kreditorfakturapuljetransaktioner.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Kreditorfaktura, registrering          | Bogfør kreditorfakturaer, der er i en kladde.                                                                                                                                                                                                                                                                                                                 | Fakturajournal                                                |
| Kreditorgenudstedelse af egenveksel     | Genudsted en egenveksel, der tidligere er blevet accepteret af organisationens bank.                                                                                                                                                                                                                                                                      | kladde for genudstedelse af egenveksel                                 |
| Kreditorudligning af egenveksel     | Opret kreditortransaktioner til udligning af egenveksel.                                                                                                                                                                                                                                                                                                          | Kladde for udligning af egenveksel                                 |





