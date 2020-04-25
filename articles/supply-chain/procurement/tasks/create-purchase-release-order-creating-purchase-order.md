---
title: Oprette en købsaftræksordre ved oprettelse af indkøbsordren
description: Denne fremgangsmåde viser, hvordan du bruger en købsaftale, når du opretter en indkøbsordre.
author: mkirknel
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3e02bd4aaef8da7838c92199c28b1e298078c57
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204855"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a>Oprette en købsaftræksordre ved oprettelse af indkøbsordren

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du bruger en købsaftale, når du opretter en indkøbsordre. Købsaftalen skal anvendes, når du opretter indkøbsordren, fordi der er generelle betingelser, der skal kopieres til indkøbsordrehovedet. Denne opgave vil typisk blive foretaget af en indkøber. Du skal have en gyldig købsaftale med et tilsagn om produktantal for en kreditor og varer som en forudsætning for denne vejledning. Samme fremgangsmåde kan bruges, hvis du har en købsaftale med andre typer forpligtelser. Du kan køre denne guide i USMF-demodatafirmaet. Hvis du bruger USMF, kan du køre guiden "Opret en købsaftale" først for at konfigurere de nødvendige forudsætninger for denne vejledning.


## <a name="create-a-purchase-order"></a>Oprette en indkøbsordre
1. Åbn arbejdsområdet til klargøring af indkøbsordre.
2. Klik på Ny indkøbsordre.
3. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Slå udvidelsen af sektionen Generelt til/fra.
7. Klik på rullelisten i feltet Købsaftale for at åbne opslaget.
    * Alle aftaler, der er tilgængelige for kreditoren, er anført her. Find den gældende aftale, du vil bruge.  
8. Klik op linket i den valgte række på listen.
9. Klik på Ja.
10. Klik på OK.

## <a name="add-a-line"></a>Tilføj en linje
1. Indtast en værdi i feltet Varenummer.
    * Hvis der er bestemte lager- eller lokalitetsdimensioner på tilsagnet, skal du angive de samme værdier på indkøbsordrelinjen for at gøre brug af aftalen.  
2. Klik på rullelisten i feltet Sted for at åbne opslaget.
    * Stedet er muligvis allerede udfyldt med standardværdien fra ordren eller fra kreditoren. Hvis det er tilfældet, kan du springe dette trin over.  
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Angiv et tal i feltet Antal.
    * Kontrollér, at prisen er kopieret fra tilsagnet.  

## <a name="look-up-the-commitment"></a>Slå tilsagnet op
1. Klik på Opdater linje.
2. Klik på Vedhæftet.
    * Her kan du få oplysninger om for købsaftalen. For eksempel kan du se prisen og om pris og rabat er fast, hvilket betyder, at hvis du ændrer pris eller rabat på indkøbsordren til en anden værdi end på forpligtelsen, systemet vil fjerne linket, så indkøbsordrelinjen ikke opfylde forpligtelsen. Du kan også se hvis Maks gennemtvinges indstilling er markeret, hvilket betyder, at antallet på forpligtelsen, der ikke kan overskrides ved at sammenlægge alle de køb, der skal opfylde forpligtelsen.  
3. Luk siden.

## <a name="look-up-the-purchase-agreement"></a>Slå købsaftalen op
1. Klik på Generelt i handlingsruden.
2. Klik på Indkøbsaftale.
3. Luk siden.
4. Luk siden.

