---
title: Følgeseddelopdateringer til returneringer
description: Før returnerede varer kan modtages på lager, skal følgesedlen til den ordre, de tilhører, være opdateret.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 021cf6c0ff606e4b5a7139285fe7508283fb9fe2
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675677"
---
# <a name="packing-slip-updates-for-returns"></a>Følgeseddelopdateringer til returneringer  

[!include [banner](../includes/banner.md)]


Før returnerede varer kan modtages på lager, skal følgesedlen til den ordre, de tilhører, være opdateret. Ligesom fakturaopdateringsprocessen er opdateringen af den økonomiske transaktion, er opdateringsprocessen for følgesedlen den fysiske opdatering af lagerposten, så ændringerne foretages på lageret. Ved returneringer bliver de trin, der tildeles dispositionshandlingen, implementeret under opdateringen af følgesedlen.

Opdateringen af følgesedlen kan behandles i varemodtagelseskladden eller returordren.

Som en del af posteringsprocessen for følgesedlen kan følgesedlens referencenummer fra kundens forsendelsesdokumenter knyttes til ordrelinjerne. Denne tilknytning er valgfri og kun til orientering. Den opretter ikke nogen transaktionsopdateringer.

Hvis ikke alle de forventede returvarer er ankommet, skal du kun medtage det antal, der er modtaget, i følgeseddelopdateringen. Lad de øvrige varer blive i ordren, indtil resten af returforsendelsen er ankommet.

Hvis en vare er sendt tilbage fra karantæne til forsendelses- og modtagelsesafdelingen, f.eks. når karantænekontrolløren ikke ved, hvor varen skal placeres på lageret, skal den tilsvarende følgeseddel opdateres for korrekt at registrere og udføre handlingen for den dispositionskode, der er anført som resultat af karantænen.

Når du opdaterer en følgeseddel for en returneret vare, der er fra en salgsaftale, opdateres salgsaftaleforpligtelsen for varen automatisk for at afspejle ændringer i antal eller beløb. 

## <a name="see-also"></a>Se også

[Udføre fakturaopdateringer til returneringer](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]