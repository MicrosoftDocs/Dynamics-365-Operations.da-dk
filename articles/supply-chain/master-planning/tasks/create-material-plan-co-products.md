---
title: Oprette en materialeplan for samprodukter
description: Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14de9a1085ac1cae88ad93c35385dd43c60ed4d1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424648"
---
# <a name="create-a-material-plan-for-co-products"></a>Oprette en materialeplan for samprodukter

[!include [banner](../../includes/banner.md)]

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
1. Luk siden.
2. Luk siden.
3. Klik på Varedisponering.
4. Klik på rullelisten i feltet Plan for at åbne opslaget.
5. Klik op linket i den valgte række på listen.
    * Eksempel: MasterPlan  
6. Klik på Kør.
7. Udvis eller skjul sektionen Poster, der skal indgå.
8. Klik på Filtrér.
9. Vælg rækken for Felt = Varenummer på listen.
10. Skriv en værdi i feltet Kriterier.
    * Eksempel: P6003  
11. Klik på OK.
12. Klik på OK.
13. Klik på Ordreforslag.
14. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Varenummer med værdien "P6000".
    * Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.  
15. Markér den valgte række på listen.
    * Vælg en af de rækker, der returneres af filteret.  
16. Klik op linket i den valgte række på listen.
17. Udvid eller skjul sektionen Udligning.
18. Klik op linket i den valgte række på listen.
    * Ordreforslaget er udlignet til salgsordren for samproduktet.  
19. Luk siden.

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
1. Klik på rullelisten i feltet Plan for at åbne opslaget.
2. Klik op linket i den valgte række på listen.
    * Eksempel: MasterPlan  
3. Klik på Kør.
4. Udvis eller skjul sektionen Poster, der skal indgå.
5. Klik på Filtrér.
6. Vælg rækken for Felt = Varenummer på listen.
7. Skriv en værdi i feltet Kriterier.
    * Eksempel: P6003  
8. Klik på OK.
9. Klik på OK.
10. Klik på Ordreforslag.
11. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Varenummer med værdien "P6000".
    * Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.  
12. Markér den valgte række på listen.
    * Vælg en af de rækker, der returneres af filteret.  
13. Klik op linket i den valgte række på listen.
14. Udvid eller skjul sektionen Udligning.
15. Klik op linket i den valgte række på listen.
    * Ordreforslaget er udlignet til salgsordren for samproduktet.  
16. Luk siden.
17. Klik på Varedisponering.
18. Gå til Varedisponering > Konfiguration > Varedisponeringsparametre.
19. Vælg Nej i afkrydsningsfeltet Deaktiver alle planlægningsprocesser.
20. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]