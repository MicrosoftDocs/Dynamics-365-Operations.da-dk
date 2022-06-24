---
title: Beregning af kildeskat på fakturaer
description: Denne artikel omhandler transaktioner, hvor kildeskatten (TDS – Tax Deducted at Source) beregnes på fakturaniveau.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855357"
---
# <a name="tds-calculation-on-invoices"></a>Beregning af kildeskat på fakturaer

[!include [banner](../includes/banner.md)]

Denne artikel omhandler transaktioner, hvor kildeskatten (TDS – Tax Deducted at Source) beregnes på fakturaniveau.

| Serienummer | Transaktionstype                                 | Transaktionsbeløb | Sidenavn og sti for valg                                 | Kontotype og modkontotype                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Køb foretaget fra kreditor/registrering af udgifter   | Debet eller Kredit  | Siden Finanskladder (Finans > Kladdeposter > Finanskladder), siden Godkendelseskladde (Kreditor > Fakturaer > Fakturagodkendelse), siden Fakturakladde (Kreditor > Fakturaer > Fakturakladde) | Finans (Dr.)  Kreditor (Kr.).  A-skat beregnes kun for kombinationen Kreditor-Finans, når finanskontoen har bogføringstypen **Køb** **kontant**. |
| 2.            | Køb foretaget fra kunde/registrering af udgifter | Debet eller Kredit  | Siden Finanskladder (Finans > Kladdeposter > Finanskladder), Siden Fakturakladde (Kreditor > Fakturaer > Fakturakladde) | Finans (Dr.)  Debitor (Kr.).                                 |
| 3.            | Indkøb af anlægsaktiv fra kreditor              | Debet eller Kredit  | Siden Finanskladder (Finans > Kladdeposter > Finanskladder), siden Indgangsbogkladde (Kreditor > Fakturaer > Fakturagodkendelse), siden Fakturakladde (Kreditor > Fakturaer > Indgangsbog) | Anlægsaktiver (Dr.)  Kreditor (Kr.)                             |
| 4.            | Indkøb af anlægsaktiv fra kunde            | Debet eller Kredit  | Siden Finanskladder (Finans > Kladdeposter > Finanskladder), Siden Fakturakladde (Kreditor > Fakturaer > Fakturakladde) | Anlægsaktiver (Dr.)  Debitor (Kr.)                           |
| 5            | Indkøbsfaktura (skyldig kildeskat)                  |                    | Siden Indkøbsordre (Kreditor > Indkøbsordrer > Alle indkøbsordrer) |                                                              |
| 6            | Salgsfaktura (skyldig kildeskat)                  |                    | Siden Salgsordre (Debitor > Ordrer > Alle salgsordrer), siden Fritekstfaktura (Debitor > Fakturaer > Alle fritekstfakturaer) |                                                              |
