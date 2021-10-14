---
title: Oprette en materialeplan for samprodukter
description: Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: deae0d7e0295aa02f5ad512f67e9e3d2148c2e33
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578290"
---
# <a name="create-a-material-plan-for-co-products"></a>Oprette en materialeplan for samprodukter

[!include [banner](../../includes/banner.md)]

Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter. Det demodatafirma, der bruges til at oprette denne procedure, er USP2.

## <a name="create-requirement-for-a-co-product"></a>Opret krav om et samprodukt

1. Gå til **Salg og marketing \> Arbejdsområder \> Salgsordrebehandling og -forespørgsel**.
1. Vælg **Ny**.
1. Vælg **Salgsordre**.
1. Skriv en værdi i feltet **Kundekonto**.
    * Eksempel: US-001  
1. Vælg **OK**.
1. Indtast en værdi i feltet **Varenummer**.
    * Eksempel: P6003  
1. Angiv et tal i feltet **Antal**.
    * Eksempel: 50000  
1. Vælg **Gem**.

## <a name="create-a-material-plan-for-co-products"></a>Oprette en materialeplan for samprodukter

1. Luk siden.
1. Luk siden.
1. Vælg **Varedisponering**.
1. Vælg rullelistens kap i feltet **Plan** for at åbne opslaget.
1. Vælg linket i den valgte række på listen.
    * Eksempel: MasterPlan  
1. Vælg **Kør**.
1. Udvid eller skjul sektionen **Poster, der skal indgå**.
1. Vælg **Filter**.
1. Vælg rækken for **Felt** = *Varenummer* på listen.
1. Skriv en værdi i feltet **Kriterier**.
    * Eksempel: P6003  
1. Vælg **OK**.
1. Vælg **OK**.
1. Vælg **Ordreforslag**.
1. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet **Varenummer** med værdien "P6000".
    * Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.  
1. Markér den valgte række på listen.
    * Vælg en af de rækker, der returneres af filteret.  
1. Vælg linket i den valgte række på listen.
1. Udvid sektionen **Udligning**.
1. Vælg linket i den valgte række på listen.
    * Ordreforslaget er udlignet til salgsordren for samproduktet.  
1. Luk siden.

## <a name="create-a-second-requirement-for-a-co-product"></a>Oprette et andet krav om et samprodukt

1. Gå til **Salg og marketing \> Arbejdsområder \> Salgsordrebehandling og -forespørgsel**.
1. Vælg **Ny**.
1. Vælg **Salgsordre**.
1. Skriv en værdi i feltet **Kundekonto**.
    * Eksempel: US-001  
1. Vælg **OK**.
1. Indtast en værdi i feltet **Varenummer**.
    * Eksempel: P6003  
1. Angiv et tal i feltet **Antal**.
    * Eksempel: 50000  
1. Vælg **Gem**.

## <a name="create-a-second-material-plan-for-co-products"></a>Oprette en anden materialeplan for samprodukter

1. Vælg rullelistens kap i feltet **Plan** for at åbne opslaget.
2. Vælg linket i den valgte række på listen.
    * Eksempel: MasterPlan  
3. Vælg **Kør**.
4. Udvid eller skjul sektionen **Poster, der skal indgå**.
5. Vælg **Filter**.
6. Vælg rækken for **Felt** = *Varenummer* på listen.
7. Skriv en værdi i feltet *Kriterier*.
    * Eksempel: P6003  
8. Vælg **OK**.
9. Vælg **OK**.
10. Vælg **Ordreforslag**.
11. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet **Varenummer** med værdien "P6000".
    * Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.  
12. Markér den valgte række på listen.
    * Vælg en af de rækker, der returneres af filteret.  
13. Vælg linket i den valgte række på listen.
14. Udvid eller skjul sektionen **Udligning**.
15. Vælg linket i den valgte række på listen.
    * Ordreforslaget er udlignet til salgsordren for samproduktet.  
16. Luk siden.
17. Vælg **Varedisponering**.
18. Gå til **Varedisponering \> Konfiguration \> Varedisponeringsparametre**.
19. Vælg *Nej* i feltet **Deaktiver alle planlægningsprocesser**.
20. Luk siden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]