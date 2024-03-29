---
title: Oversigt over serviceniveauaftaler
description: I en serviceniveauaftale accepterer kunden en minimumsvartid baseret på det tidspunkt, hvor servicefirmaet registrerer problemet, og hvornår problemet er løst.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b90618d5d283b16ac8374f3b8b2df48611ba270
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014653"
---
# <a name="service-level-agreements-overview"></a>Oversigt over serviceniveauaftaler       

[!include [banner](../includes/banner.md)]


En serviceniveauaftale er en aftale mellem et servicefirma og en servicekunde. I en SLA accepterer kunden en minimumsvartid baseret på det tidspunkt, hvor servicefirmaet registrerer problemet, og hvornår problemet er løst.

En SLA fastlægger et standardserviceniveau, der tilbydes kunder, og gør det nemt for et servicefirma at overskue, hvornår en serviceopgave skal være fuldført.

Der kan oprettes ethvert antal serviceniveauaftaler for at tilbyde forskellige niveauer af service til servicekunder.

## <a name="create-a-service-level-agreement"></a>Oprette en serviceniveauaftale

1.  Klik på **Servicestyring** \> **Opsætning** \> **Serviceaftaler** \> **Serviceniveauaftaler**.

2.  Skriv et navn til serviceniveauaftalen i feltet **Serviceniveauaftale**.

3.  Skriv den tid, du vil tillade til afslutning af servicekald, der er tilknyttet serviceaftaleniveauet. Vælg derefter en kalender, hvis du vil basere serviceaftalen på en bestemt kalender.

## <a name="apply-a-service-level-agreement"></a>Anvende en serviceniveauaftale

Serviceniveauaftalen anvendes direkte på en serviceaftale.

Serviceordrer, som du opretter manuelt og knytter til en serviceaftale, som har en SLA, måles i forhold til denne SLA.

Serviceordrer, som du opretter automatisk, knyttes ikke til en serviceniveauaftale.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Anvende serviceniveauaftalen på serviceaftalen

1.  Klik på **Servicestyring** \> **Serviceaftaler** \> **Serviceaftaler**. Vælg den serviceaftale, du vil anvende SLA'en til, og klik derefter på **Rediger** i **handlingsruden**.

2.  I feltet **Serviceniveauaftale** skal du vælge den SLA, du vil tildele.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Anvende serviceniveauaftalen på serviceaftalegruppen

1.  Klik på **Servicestyring** \> **Opsætning** \> **Serviceaftaler** \> **Serviceaftalegrupper**.

2.  I feltet **Serviceniveauaftale** skal du vælge den SLA, du vil tildele.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Spore tidsforbrug på en serviceordre i forhold til en serviceniveauaftale

Når du opretter en ny serviceordre til en serviceaftale, som en SLA er tildelt til, startes tidsintervallet for levering af servicen, og systemet begynder at spore leveringstidspunktet. Du kan desuden angive følgende indstillinger:

  - Du kan starte og stoppe tidsregistreringen for serviceordren for at registrere det samlede tidsforbrug på serviceordrer.

  - Du kan overvåge overholdelsen af det tidsinterval, der er afsat i serviceaftalen.

  - Du kan definere årsagskoder, der skal angives, hvis tidsintervallet for serviceaftalen overskrides.

## <a name="see-also"></a>Se også

[Få vist overholdelse af serviceaftaler](view-compliance-with-service-level-agreements.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]