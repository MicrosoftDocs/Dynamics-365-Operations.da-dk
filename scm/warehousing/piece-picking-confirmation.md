---
title: "Bekræftelse af stykplukning"
description: "I dette emne beskrives, hvordan du kan konfigurere og anvende bekræftelse af stykplukning fra en mobilenhed."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: c5340f4dacd743600ef955c8d5228d1e2d2d2fa9
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017


---

# <a name="piece-picking-confirmation"></a>Bekræftelse af stykplukning

[!include[banner](../includes/banner.md)]

Stykplukning gør det muligt for dig at bekræfte hver enkelt lagervare via pluk og optællingsarbejde på en mobilenhed. For pluk kan du bekræfte mængden af arbejde, der skal behandles, op til det antal, der er angivet på arbejde, der skal plukkes. For optællingsarbejde kan du scanne det lager, du optæller, og spore det samlede beløb.

Når du aktiverer stykpluk, vælges bekræftelse af produkt automatisk. Ved pluk af arbejdstypen er det maksimale antal styk aktiveret. På denne måde kan du angive et maksimum for det antal enheder, der skal bekræftes under arbejdet. Det maksimale antal er baseret på den aktuelle arbejdsenhed, der behandles. Optællingsarbejdstypen tillader ikke et maksimum.

Du kan også bruge det antal og den måleenhed, der er knyttet til en scannet stregkode. Dette fungerer ved modtagelse af indgående flows, herunder modtagelse af blandede id'er, vare på indkøbsordre, vare på overførselsordre og varelast. Det kan også bruges til stykplukning, hvor scanning af stregkoden føjer antallet til det samlede antal bekræftede styk og konverterer mellem måleenhed på stregkoden og arbejdsenheden. Hvis det ved optælling måleenheden på stregkoden kan bekræftes, at antallet er tilladt ved optælling af seriegruppen, føjes antallet til den samlede optælling.

## <a name="where-it-applies"></a>Hvor det er relevant

Stykpluk fungerer for alt optællingsarbejde og for det indledende pluk ved alle typer arbejde. Stykpluk gælder ikke, hvis varen styres af serienumre, eller hvis det er et produktions- eller kanban-pluk fra en id-lokalitet, og varen er indstillet til midlertidig placering.

## <a name="set-up-piece-picking"></a>Konfigurere stykplukning

1.  I et menupunkt på en mobilenhed skal du åbne opsætningsformularen for arbejdsbekræftelse: Lokationsstyring > **Lokationsstyring** > **Opsætning** > **Mobilenhed** > **Menupunkter i mobilenhed**. 
2. Åbn Konfiguration af arbejdsbekræftelse fra menupunktet på mobilenheden.

Følgende indstillinger kan vælges, når arbejdstype pluk eller optælling.

| Indstilling        | Betegnelse   | 
| ------------- | ------------- |
| Bekræftelse af stykplukning   | Arbejdstyper, der kan vælges til pluk og optælling. Bekræftelse af produkt vælges automatisk. Gør det muligt for dig at bekræfte hver enkelt vare på lageret fra mobilenheden. | 
| Maksimalt antal stykker     | Tilgængelig for plukarbejde, hvis bekræftelse af stykpluk er aktiveret. Angiver en grænse for det antal styk, du skal bekræfte. |  
