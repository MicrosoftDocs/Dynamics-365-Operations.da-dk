---
title: Returnere serienummerstyrede produkter i POS
description: Dette emne indeholder en beskrivelse af funktionerne til validering af serienummerede varer som en del af returneringsprocessen i Microsoft Dynamics 365 Commerce POS-programmet.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e53c8ceb91a007775fa74f0c9598a65745f01cec
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638091"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Returnere serienummerstyrede produkter i POS

[!include [banner](includes/banner.md)]

Dette emne indeholder en beskrivelse af funktionerne til validering af serienummerede varer som en del af returneringsprocessen i Microsoft Dynamics 365 Commerce POS-programmet.

> [!NOTE]
> I Commerce version 10.0.20 og senere findes der en ny funktion med navnet **Samlet behandling af returneringer i POS**. Hvis du vil bruge serienummervalidering under behandling af returordre i POS, skal du aktivere denne funktion. Du kan finde oplysninger om andre egenskaber, som denne funktion har, når den er slået til, under [Oprette returneringer i POS](POS-returns.md).
>
> Når funktionen er aktiveret, kan den ikke deaktiveres.

## <a name="options-for-validating-serialized-returns"></a>Indstillinger til validering af serialiserede returneringer

Når funktionen **Samlet behandling af returneringer i POS** er aktiveret, kan organisationer udføre validering af returneringer af serienummerstyrede varer via POS. Denne egenskab kan advare brugerne, hvis det serienummer, der returneres, adskiller sig fra det oprindelige serienummer, der blev solgt. I Commerce version 10.0.20 og senere er den meddelelse, som brugerne modtager, kun en advarsel. Brugerne kan fortsætte med at behandle en returnering i forhold til et serienummer, der er forskelligt fra det serienummer, der oprindeligt blev solgt.

Hvis du vil konfigurere validering af serienummer for en organisation, efter at funktionen **Samlet returnering i POS** er aktiveret, skal du gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre** i Commerce Headquarters. Under fanen **Lager** i oversigtspanelet **Lagerbeholdningshandlinger** skal du angive indstillingen **Aktivér validering af serienumre på POS-returneringer** til **Ja**.

## <a name="process-returns-for-serialized-items-in-pos"></a>Behandle returneringer af serialiserede varer i POS

Hvis indstillingen **Aktivér validering af serienumre på POS-returneringer** er angivet til **Ja**, når en vare, der styres af et serienummer, returneres via POS, kan brugeren angive serienummeret for returlinjen i detaljeruden på siden **Produkter, der kan returneres**. Hvis det indtastede serienummer ikke svarer til det oprindelige serienummer, der blev solgt for salgstransaktionen, modtager brugeren en advarselsmeddelelse. Programmet forhindrer dog ikke brugeren i at fortsætte med at bogføre returneringen.

> [!NOTE]
> I øjeblikket understøtter POS kun validering af serienumre på returlinjer, hvor det oprindeligt bestilte antal ikke er mere end ét. Hvis den oprindelige salgsordrelinje er oprettet i en ikke-POS-kanal, og hvis det antal, der blev bestilt til den serialiserede vare på en bestemt salgslinje, er mere end én, kan varen ikke returneres korrekt via POS.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette returneringer i POS](POS-returns.md)
