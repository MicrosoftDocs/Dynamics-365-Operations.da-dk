---
title: Konfigurere tillægstildelinger
description: Denne procedure viser, hvordan du opretter en tilbehørstildeling.
author: Weijiesa
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAccessorialAssignment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca82b403439495106151387b73548aeb30e8da46
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678032"
---
# <a name="set-up-accessorial-assignments"></a>Konfigurere tillægstildelinger

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter en tilbehørstildeling. Denne konfiguration vil normalt blive udført af en transportkoordinator. Før du kan bruge denne vejledning skal du køre guiden "Konfigurer gebyrer for hubtillæg og tillægsmastere".


## <a name="set-up-accessorial-assignment"></a>Konfigurer Tilbehørstildeling
1. Gå til Transportstyring > Opsætning > Klassificering > Tildelinger af tillæg.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Slå udvidelsen af sektionen afsnittet Detaljer til/fra.
5. Klik på rullelisten i feltet Hub for at åbne opslaget.
6. Vælg den pågældende Hub, du har oprettet en tillægsmaster for, når du har kørt guiden "Konfigurer gebyrer for hubtillæg og tillægsmastere" på listen. 
7. Klik på rullelisten i feltet Id for hubtilbehør for at åbne opslaget.
8. Klik op linket i den valgte række på listen.
9. Slå udvidelsen af Sektionen Kriterier til/fra.
    * I sektionen Kriterier kan du vælge de nøjagtige kriterier for, hvornår gebyret skal gælde, baseret på de forskellige værdier, der tilbydes her.  
10. Angiv indstillingen Anvend altid til Ja.
11. Vælg en indstilling i feltet Tilbehørstildelingsniveau.
12. Slå udvidelsen af sektionen Beregning til/fra.
13. Vælg "Fast" i feltet Gebyrtype for tillæg.
    * Gebyrtype for tillæg bestemmer, hvordan det faktiske gebyr beregnes. I dette eksempel er det et fast gebyr.  
14. Angiv et tal i feltet Gebyr for tillæg.
15. Klik på Gem.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]