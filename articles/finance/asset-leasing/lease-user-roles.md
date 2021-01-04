---
title: Tildele leasingbrugerroller
description: I dette emne beskrives de sikkerhedsroller, der bruges til aktivleasing. Det forklarer også, hvordan du kan tildele brugere til disse roller.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b31d0880d4f2cd2b8ad2dffcfe279421f935ed35
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441768"
---
# <a name="assign-lease-user-roles"></a>Tildele leasingbrugerroller

[!include [banner](../includes/banner.md)]

I dette emne beskrives de sikkerhedsroller, der bruges til aktivleasing. Det forklarer også, hvordan du kan tildele brugere til disse roller.

Tre brugerroller skelner adgang til aktivleasing. En rolle er velegnet til vedligeholdelse af leasingaftaler, en er velegnet til visning af leasingaftaler, en er relevant for udførelsen af en leasingassistentsopgaver. Hver rolle har specifikke rettigheder til alle leasingsider, og de enkelte giver brugerne mulighed for at få vist, oprette, redigere eller slette rettigheder i henhold til deres arbejdsopgaver.

| Rolle           | Betegnelse |
|----------------|-------------|
| Vedligehold leasingaftale | Brugere i denne rolle kan tilføje, redigere, slette og få vist leasingaftaler. Denne rolle er udviklet til daglige brugere, hvis opgaver omfatter oprettelse og bogføring af månedlige kladdeposter og tilføjelse af nye leasingaftaler. Denne rolle giver adgang til alle aktivleasingfunktioner. |
| Vis leasingaftale     | Brugere i denne rolle kan kun få vist leasingposter, tidsplaner og køre rapporter. De kan ikke oprette nye leasingaftaler, redigere eksisterende leasingaftaler eller oprette kladdeposteringer ud fra leasingaftaler. Rollen er beregnet til brugere, der blot skal have vist leasingaftaler, leasingplaner og de transaktioner, der finder sted i forhold til disse leasingaftaler. |
| Leasingassistent    | Brugere i denne rolle kan kun oprette nye leasingaftaler. De kan hverken redigere eller slette eksisterende leasingaftaler, få vist leasing planer eller bogføre leasingkladdeposteringer. Denne rolle er beregnet til brugere, der arbejder i en dataindtastningskapacitet. |

Udfør følgende trin for at tildele brugere til de roller, der bruges i aktivleasing.

1. Gå til **Systemadministration \> Sikkerhed \> Tildel brugere roller**.
2. Vælg rollen **Vedligehold leasingaftale**, **Leasingassistent** eller **Vis leasingaftale**, og vælg derefter **Tildel/Udeluk manuelt**.
3. Vælg den bruger, der skal tildeles til rollen, og vælg derefter **Tildel til rolle**.
