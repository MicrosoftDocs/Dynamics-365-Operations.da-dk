---
title: Grænseværdi og grænseværdi for undtagelse
description: Dette emne beskriver grænsen og undtagelsesgrænserne for afgifter fratrukket ved kilden (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1bf0d3a01ede559d288581d3b58b3777d0e608dc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023112"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Grænseværdi og grænseværdi for undtagelse

[!include [banner](../includes/banner.md)]

Dette emne beskriver grænsen og undtagelsesgrænserne for afgifter fratrukket ved kilden (TDS). TDS på fakturaer og betalinger beregnes altid under hensyntagen til den grænseværdi og grænse for undtagelse, der er defineret for TDS-afgiftskomponenterne på siden **A-skat-komponenter**. TDS-afgiftskomponenterne er knyttet til TDS-afgiftskoder, som indgår i TDS-afgiftsgrupperne. TDS-afgiftsgrupperne er knyttet til leverandører og kunder, så TDS kan beregnes på faktura- eller betalingsniveau.

TDS beregnes, hvis beløbet for en postering eller de akkumulerede transaktioner, der er bogført med en bestemt TDS-gruppe for en kreditor, overskrider den grænse, der er angivet på siden for **A-skat-komponenter**. TDS beregnes ikke, før det akkumulerede transaktionsbeløb overskrider den angivne grænse.

Hvis der er angivet en grænse for undtagelsesgrænsen sammen med grænsen for en TDS-komponent, beregnes TDS, når et bestemt transaktionsbeløb overstiger grænseværdi for undtagelsen, selvom det akkumulerede transaktionsbeløb ikke overstiger den angivne grænseværdi.

### <a name="example"></a>Eksempel
En afgiftskomponent, der kaldes TDS, oprettes og tilknyttes TDS-afgiftsgruppen med navnet Kontrahent. Grænseværdien er defineret som 50.000, og undtagelsesgrænsen er defineret som 20.000 for TDS-afgiftskomponenten. TDS-gruppekontrahenten er defineret som standard-TDS-gruppen for kreditor 1.

En indkøbsfaktura, 001, bogføres for kreditor 1 for 10000. TDS beregnes ikke for fakturaen, da fakturabeløbet ikke overstiger grænseværdien eller grænseværdien for undtagelsen. En indkøbsfaktura, 002, bogføres for kreditor 1 for 25.000. TDS beregnes for fakturaen, da fakturabeløbet overstiger grænseværdien for undtagelsen. En indkøbsfaktura, 003, bogføres for kreditor 1 for 20.000. TDS beregnes for fakturaen, fordi det samlede fakturabeløb for de tre fakturaer, der er udstedt for kreditoren, har nået grænseværdien. TDS beregnes på alle de fakturaer, der er udstedt for den kreditor, som TDS ikke er beregnet for tidligere. TDS beregnes derfor af 30.000, hvilket er det samlede fakturabeløb af faktura 001 og 003.

Der tages ikke hensyn til grænseværdien og grænsen for undtagelsen i TDS-beregningen, hvis afkrydsningsfeltet **Ignorer grænseværdi** er markeret for TDS-afgiftskoder i den TDS-gruppe, der er knyttet til transaktionen. Grænseværdien bruges ikke i TDS-afgiftskoderne i TDS-gruppen, som afkrydsningsfeltet **Ignorer grænseværdi** er aktiveret.

Hvis afkrydsningsfeltet **Ignorer grænseværdi** er markeret for en bestemt TDS-gruppe for nogle fakturaer, men ikke er markeret for andre fakturaer, der er oprettet for en bestemt kreditor/kunde, finder beregningen af TDS, uden at grænseværdien ignoreres, måske sted for nogle få fakturaer under hensyntagen til det akkumulerede beløb på alle fakturaer, hvor TDS ikke er blevet beregnet tidligere.

Grænseværdien er f.eks. 25000. Følgende fakturaer er oprettet for kreditor A.

- Faktura 1 – 2.0000 – (afkrydsningsfeltet **Ignorer grænseværdi** er ikke markeret): TDS beregnes ikke.

- Faktura 2 – 4.000 – (afkrydsningsfeltet **Ignorer grænseværdi** er markeret): TDS beregnes af 4.000.

- Faktura 2 – 3.000 – (afkrydsningsfeltet **Ignorer grænseværdi** er ikke markeret): TDS beregnes som det akkumulerede fakturabeløb, dvs. 27.000 (20000+4000+3000) overstiger grænseværdien. TDS beregnes ud fra det akkumulerede beløb på fakturaer, hvor TDS ikke er beregnet på tidligere, dvs. 23.000 (20000+3000).
