---
title: Anvende en købsaftale, når der oprettes en indkøbsordre
description: Denne fremgangsmåde viser, hvordan du bruger en købsaftale, når du opretter en indkøbsordre.
author: kamaybac
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1913181e85929951ce240ac31a0ac3f1351f6ae51f6ed2790bae577b2100b308
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731241"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Anvende en købsaftale, når der oprettes en indkøbsordre

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du bruger en købsaftale, når du opretter en indkøbsordre. Købsaftalen skal anvendes, når du opretter indkøbsordren, fordi der er generelle betingelser, der skal kopieres til indkøbsordrehovedet. Denne opgave vil typisk blive foretaget af en indkøber. Du skal have en gyldig købsaftale med et tilsagn om produktantal for en kreditor og varer som en forudsætning for denne vejledning. Samme fremgangsmåde kan bruges, hvis du har en købsaftale med andre typer forpligtelser.

## <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

1. Gå til **Produktion og forsyning \> Arbejdsområder \> Klargøring af indkøbsordrer**.
1. Vælg **Ny indkøbsordre** i handlingsruden.
1. Dialogboksen **Opret indkøbsordre** åbnes. Vælg en **Kreditorkonto**. Kontrollér og juster de andre adressefelter efter behov.
1. Udvid oversigtspanelet **Generelt**.
1. Find og vælg den gældende aftale, du vil bruge, i feltet **Købsaftale**. Alle aftaler, der er tilgængelige for kreditoren, er anført her.  
1. Vælg **Ja**.
1. Vælg **OK**.

## <a name="add-a-line"></a>Tilføj en linje

1. Indtast en værdi i feltet **Varenummer**. Hvis der er bestemte lager- eller lokalitetsdimensioner på tilsagnet, skal du angive de samme værdier på indkøbsordrelinjen for at gøre brug af aftalen.
1. Vælg rulleknappen i feltet **Sted** for at åbne opslaget. Stedet er muligvis allerede udfyldt med standardværdien fra ordren eller fra kreditoren. Hvis det er tilfældet, kan du springe dette trin over.  
1. Find og vælg den ønskede post på listen.
1. Vælg linket i den valgte række på listen.
1. Angiv et tal i feltet **Antal**. Kontrollér, at prisen er kopieret fra tilsagnet.  

## <a name="look-up-the-commitment"></a>Slå tilsagnet op

1. Vælg **Opdater linje**.
1. Vælg **Vedhæftet**. Her kan du få oplysninger om for købsaftalen. For eksempel kan du se prisen og om pris og rabat er fast, hvilket betyder, at hvis du ændrer pris eller rabat på indkøbsordren til en anden værdi end på forpligtelsen, systemet vil fjerne linket, så indkøbsordrelinjen ikke opfylde forpligtelsen. Du kan også se hvis Maks gennemtvinges indstilling er markeret, hvilket betyder, at antallet på forpligtelsen, der ikke kan overskrides ved at sammenlægge alle de køb, der skal opfylde forpligtelsen.  
1. Luk siden.

## <a name="look-up-the-purchase-agreement"></a>Slå købsaftalen op

1. Vælg **Generelt** i **handlingsruden**.
1. Vælg **Købsaftale**.
1. Luk siden.
1. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]