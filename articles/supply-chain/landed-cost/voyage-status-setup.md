---
title: Opsætning af fragtstatus
description: Denne artikel beskriver, hvordan du kan fastlægge de statusværdier, som brugerne kan tildele fragt.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1cec728f2fa49175c063818ee7f188b441945647
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907313"
---
# <a name="voyage-status-setup"></a>Opsætning af fragtstatus

[!include [banner](../../includes/banner.md)]

På siden **Fragtstatusser** skal du oprette det sæt statusværdier, som brugerne kan tildele fragt. Brugerne kan tildele fragtstatusværdier til alle niveauer af en fragt: fragt, forsendelsescontainer, folio, indkøbsordre og vare (indkøbslinjer og flytteordrelinjer). De bruges til to formål:

- Oplyse brugeren om status for fragten, forsendelsescontainer, folio, indkøbsordre eller vare (indkøbslinjer og flytteordrelinjer).
- Begrænse brugen af omkostningsområdet ved at forhindre ændringer eller sletninger.

Du kan konfigurere fragtstatusserne ved at gå til **Landingsomkostninger \> Opsætning \> Fragtstatusser**. Her kan du tilføje, fjerne og redigere statusser ved at bruge knapperne i handlingsruden.

Hvert omkostningsområde har sit eget sæt og hierarki over fragtstatusser. På siden **Fragtstatusser** skal du derfor først vælge det omkostningsområde, du vil se eller oprette fragtstatusser for, i feltet **Kostprisområde**. Angiv derefter de felter, der er beskrevet i følgende tabel, efter behov for hver fragtstatus. Bemærk, at status for en fragt også kan ændres automatisk af systemhændelser, f.eks. regler, der er oprettet ved hjælp af sporingskontrolcenteret.

| Felt | Beskrivelse |
|---|---|
| Fragtstatus | Angiv navnet på fragtstatus. |
| Beskrivelse | Indtast en beskrivelse af fragtstatussen. |
| Rediger | Markér dette afkrydsningsfelt, hvis brugere skal have tilladelse til at redigere fragt, der har denne status. |
| Delete | Markér dette afkrydsningsfelt, hvis brugere skal have tilladelse til at slette fragt, der har denne status. |
| Obligatorisk | Markér dette afkrydsningsfelt for at gøre fragtstatus obligatorisk, så den ikke kan springes over. |
| Overordnet | Brug dette felt til at oprette et hierarki mellem statusværdierne. Fragtstatusser kan kun ændres (enten manuelt eller automatisk) nedad i hierarkiet, fra en overordnet status til en af dets underordnede statusser.

> [!NOTE]
> Du skal kun konfigurere de specifikke fragtstatusser, som din organisation bruger. Af typiske fragtstatusser kan nævnes *Bekræftet*, *Varer i transit*, *Modtaget*, *Klar til efterkalkulation* og *Efterkalkuleret*. Der kan dog være andre statusser.
