---
title: Foretage manuelle justeringer af prognosegrundlaget
description: "I denne artikel forklares, hvordan du kan foretage manuelle justeringer af et prognosegrundlag og få vist detaljer om prognosen."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 218374cdb6b5588648422d97c04fb60f26e47ac7
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Foretage manuelle justeringer af prognosegrundlaget

[!include[banner](../includes/banner.md)]


I denne artikel forklares, hvordan du kan foretage manuelle justeringer af et prognosegrundlag og få vist detaljer om prognosen. 

Før du foretager manuelle justeringer, er det vigtigt at forstå nogle begreber på forskellige sider.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Gitter på siden Justeret behovsprognose
Siden **Justeret behovsprognose** indeholder et gitter, der har følgende struktur:

-   Den første kolonne viser varerne, varefordelingsnøgler, virksomheder osv., der er genereret en prognose for. Undertitlen på siden indeholder en beskrivelse af de aktuelle prognosedimensioner, der vises i matrixen. Hvis undertitlen på siden for eksempel er **firma/websteder/varefordelingsnøgle**, og en af rækkeoverskrifterne i matrixen er **USMF/1/D\_Alloc**, viser rækken budgettet for USMF-firmaet, webstedet 1 og varefordelingsnøglen **D\_Alloc**.
-   Efterfølgende kolonnerne repræsenterer de prognosefilsæt, som prognosen er oprettet for. Hver enkelt kolonneoverskrift er den første dato i det prognosefilsæt, der vises i kolonnen.
-   Værdierne i cellerne repræsenterer prognosen for ét element, varefordelingsnøgle osv. for det specifikke prognosefilsæt.

## <a name="forecast-aggregation-and-deaggregation"></a>Aggregering og de-aggregering af prognose
Undertitlen på siden viser niveauet af prognoseaggregering. 

Hvis sidens undertitel f.eks. er **Firma/Sted/Fordelingsnøgle/Varenummer/Farve/Størrelse/Konfiguration/Typografi**, er der ingen prognoseaggregering, og prognosen vises på niveauet for varen og dens dimensioner. Hvis du vil ændre aggregeringen, skal du bruge siden **Skift prognosedimensioner**, som du kan åbne fra programmenuen. 

Hvis du vil ændre prognosen, skal du klikke i en af de celler, der er tilgængelige, og skrive den justerede prognoseværdi. Den redigerede celle bliver straks fed for at angive, at den prognose, som den viser, ikke er den prognose, som den efterspørgsel som behovsprognosetjenesten har oprettet, men er blevet justeret manuelt. 

Hvis du ændrer aggregeringen for at få siden til at vise mere aggregerede data, kan du bruge siden **Behovsprognoselinjer** til at se de individuelle budgetlinjer, der udgør den aggregerede prognose. 

Hvis du f.eks. har genereret prognosen på vareniveauet, men du ved, at behovet for denne vare vil stige på tværs af alle steder på grund af en kampagne eller en lignende hændelse. I dette tilfælde kan du angive aggregering til **Firma/Varefordelingsnøgle/Vare** på siden **Skift prognosedimensioner**. Du kan justere den globale prognose for varen på tværs af alle steder i matrixen **Justeret behovsprognose**. Du kan se virkningen af ændringen på alle steder ved at åbne siden **Behovsprognoselinjer**. På denne side kan du se en linje for varen for hvert sted, det justerede prognoseantal og det oprindelige prognoseantal. 

Når der foretages justering af prognoseantallet på et aggregeret niveau, bruger systemet vægtet fordeling til at distribuere ændringen mellem de linjer, der skaber aggregeringen. 

Du kan også foretage manuelle justeringer på siden **Behovsprognoselinjer** ved at ændre enten værdien **Samlet antal** eller cellerne **Antal** i de-aggregeringsmatrixen.

## <a name="viewing-details-of-the-forecast"></a>Få vist detaljer om prognosen
Du kan åbne siden **Detaljer om behovsprognose** for at få vist yderligere oplysninger om prognosen. 

Siden **Detaljer om behovsprognose** side viser følgende oplysninger i grafisk format og tabelformat:

-   Det historiske behov, som de prognoseforudsigelserne er baseret på.
-   Den aktuelle prognose, der bruges ved varedisponering.
-   De nye behovsprognoseværdier og de beløb, de justeres for manuelt.
-   Konfidensintervallet for prognoseværdierne.
-   Den prognosemodel, der blev brugt til at oprette prognosen. Hvis du får vist aggregerede data, kan du se listen over alle de metoder, der blev brugt til den aggregerede tidsserie.
-   Nøjagtigheden af den interne model (MAPE). Du kan få flere oplysninger om prognosenøjagtighed under [Overvåge prognosenøjagtighed](monitor-forecast-accuracy.md).

**Bemærkninger:**

-   De konfidensinterval, der vises i sektionen **Prognose** på siden, der repræsenterer forskellen mellem den øvre grænse for konfidensintervallet og den nedre grænse for konfidensintervallet. For at få vist værdierne for de øvre og nedre grænser skal du holde markøren over diagrammet i sektionen **Historisk efterspørgsel og prognose grafisk**.
-   Hvis du bruger Finance and Operations-tjenesten til behovsprognoser med Microsoft Azure Machine Learning, kan du angive det konfidensniveau i procent, som den generede prognose, skal have. Et konfidensinterval består af en række værdier, der fungerer som gode estimater for behovsprognosen. En konfidensinternval på 95 procent angiver, at der er 5 procent risiko for, at behovsprognosen falder uden for konfidensintervalområdet.

Du kan også foretage manuelle justeringer af prognosen på siden **Detaljer om behovsprognose** ved at ændre værdierne i rækken **Prognose** i sektionen **Prognose**.

<a name="see-also"></a>Se også
--------

[Overvågning af prognosenøjagtighed](monitor-forecast-accuracy.md)

[Generere et statistisk budgetgrundlag](generate-statistical-baseline-forecast.md)




