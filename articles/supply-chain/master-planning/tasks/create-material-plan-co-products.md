--- 
title: Oprette en materialeplan for samprodukter
description: "Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a>Oprette en materialeplan for samprodukter

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter. Det demodatafirma, der bruges til at oprette denne procedure, er USP2.


## <a name="create-requirement-for-a-co-product"></a>Opret krav om et samprodukt
1. Gå til Standarddashboard.
2. Klik på Salgsordrebehandling og -forespørgsel.
3. Klik på Ny.
4. Klik på Salgsordre.
5. Skriv en værdi i feltet Kundekonto.
    * Eksempel: US-001  
6. Klik på OK.
7. Indtast en værdi i feltet Varenummer.
    * Eksempel: P6003  
8. Angiv et tal i feltet Antal.
    * Eksempel: 50000  
9. Klik på Gem.

## <a name="create-a-material-plan-for-co-products"></a>Oprette en materialeplan for samprodukter
1. Klik på Varedisponering.
2. Klik på rullelisten i feltet Plan for at åbne opslaget.
3. Klik op linket i den valgte række på listen.
    * Eksempel: MasterPlan  
4. Klik på Kør.
5. Udvis eller skjul sektionen Poster, der skal indgå.
6. Klik på Filtrér.
7. Vælg rækken for Felt = Varenummer på listen.
8. Skriv en værdi i feltet Kriterier.
    * Eksempel: P6003  
9. Klik på OK.
10. Klik på OK.
11. Klik på Ordreforslag.
12. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Varenummer med værdien "P6000".
    * Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.  
13. Markér den valgte række på listen.
    * Vælg en af de rækker, der returneres af filteret.  
14. Klik op linket i den valgte række på listen.
15. Udvid eller skjul sektionen Udligning.
16. Klik op linket i den valgte række på listen.
    * Ordreforslaget er udlignet til salgsordren for samproduktet.  
17. Luk siden.


