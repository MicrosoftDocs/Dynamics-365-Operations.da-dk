---
title: Efterberegn genanskaffelsespriser og forsikrede værdier for anlægsaktivgrupper
description: Denne artikel beskriver processen til opdatering af genanskaffelsespriser og forsikrede værdier for anlægsaktiver.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c66f51a513524cfad7fb5382efa748197f9b4bac
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990508"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Efterberegn genanskaffelsespriser og forsikrede værdier for anlægsaktivgrupper

[!include [banner](../includes/banner.md)]

Denne artikel beskriver processen til opdatering af genanskaffelsespriser og forsikrede værdier for anlægsaktiver.

Måske får du jævnligt besked om, at de omkostninger, der skal bruges til at genanskaffe eller forsikre bestemte anlægsaktiver, er ændret. Din chef meddeler dig f.eks., at der var en inflation på 3 % sidste år, så du skal øge genanskaffelsesprisen for alle anlægsaktiver med 3 %. 

Selvom du kan redigere genanskaffelsesprisen og den forsikrede værdi for de enkelte anlægsaktiver på siden **Anlægsaktiver**, kan du bruge siden **Opdater genanskaffelsespriser og forsikrede værdier** til at opdatere disse værdier for en gruppe af aktiver på én gang. Disse oplysninger beskriver, hvordan værdier opdateres for anlægsaktiver eller for specifikke aktiver i grupperne.

## <a name="how-values-are-updated"></a>Sådan opdateres værdier
Hvis du vil genberegne genanskaffelsesprisen og den forsikrede værdi af anlægsaktivgrupper, skal du først angive den procentdel, du vil ændre de eksisterende genanskaffelsespriser og de forsikrede værdier med, og derefter udføre den periodiske opdatering for at genberegne værdierne. Du kan angive procentdelen i felterne **Faktor for genanskaffelsespris** og **Faktor for forsikret værdi** på siden **Anlægsaktivgrupper**. Selvom du angiver disse faktorer for anlægsaktivgruppen, når du bruger siden **Opdater genanskaffelsespriser og forsikrede værdier**, kan du vælge at genberegne genanskaffelsesprisen og den forsikrede værdi for angivne anlægsaktiver i en gruppe. 

Når du bruger siden **Opdater genanskaffelsespriser og forsikrede værdier** til at genberegne genanskaffelsesprisen og den forsikrede værdi for aktiverne anvendes følgende formler:

-   \[(Anlægsaktivgruppens genanskaffelsesprisfaktor/100) + 1\] \* Anlægsaktivets eksisterende genanskaffelsespris
-   \[(Anlægsaktivgruppens forsikrede værdifaktor/100) + 1\] \* Anlægsaktivets eksisterende forsikrede værdi

> [!NOTE] 
> Når du bruger siden **Opdater genanskaffelsespriser og forsikrede værdier** opdateres både genanskaffelsesprisen og den forsikrede værdi for de valgte aktiver. Du kan ikke angive, at der kun skal opdateres én værdi. Hvis du vil lade én værdi forblive den samme, mens den anden værdi opdateres, skal du skrive 0 (nul) som faktoren på siden **Anlægsaktivgruppen**. En nulfaktor eller en tom faktor medfører, at beregningen springes over i den periodiske opdatering. Den bogførte værdi og den bogførte nettoværdi for anlægsaktiver påvirkes ikke af den periodiske opdatering. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a>Sådan bruges en dato til at vælge, hvilke varer der skal opdateres
Opdateringsprocessen opdaterer som standard de valgte aktiver, der ikke har været opdateret på den aktuelle dag, men som kan være blevet opdateret de foregående dage. For eksempel betyder &lt; dags dato "før i dag". Du kan ændre datoen på siden **Opdater genanskaffelsespriser og forsikrede værdier** ved at klikke på knappen **Vælg**. De datokriterier, du angiver, sammenlignes med datoen for den sidste periodiske opdatering for aktivet (feltet **Sidste opdatering af periodiseret værdi/omkostning** på siden **Anlægsaktiver**). Hver gang det lykkes dig at opdatere genanskaffelsesprisen eller den forsikrede værdi for et anlægsaktiv, opdateres feltet **Sidste opdatering af periodiseret værdi/omkostning** automatisk med den aktuelle dato. 

Eksempel 

Du opdaterede genanskaffelsesprisen for køretøjer, kontormøbler og bygningsgrupper med 5 procent i går, og nu overvejer du, om disse aktiver skal opdateres nøjagtigt. Hvis du vil udelade disse aktiver, når du opdaterer alle andre anlægsaktiver i dag, skal du angive en dato i feltet **Sidste opdatering af periodiseret værdi/omkostning**, der ligger før i går (&lt; i går), da den seneste periodiske opdatering for **køretøjer**, **kontormøbler** og **bygninger** er sket uden for det datoområde, du har angivet.

## <a name="cumulative-effect-of-each-update"></a>Akkumuleret effekt af de enkelte opdateringer
Hver opdatering har en akkumuleret effekt. Du skal derfor planlægge din opdateringer omhyggeligt. Hvis du f.eks. øger alle aktiver med 3 % tirsdag og derefter øger kontormøbler med 4 % fredag, skal du være sikker på, at din hensigt er at foretage en stigning for kontormøbler på 7,12 %.

## <a name="scenario"></a>Eksempel
Din chef giver dig besked om følgende ændringer af anlægsaktiver:
-   Forøg genanskaffelsesprisen for alle anlægsaktiver, undtagen computere, med 3,25 %.
-   Forøg genanskaffelsesprisen for alle kontormøbler med yderligere 1 %.
-   Reducer genanskaffelsesprisen og den forsikrede værdi for alle computere med 10 %.

Du foretager følgende ændringer:
1.  På siden **Anlægsaktivgruppe** skal du skrive 3,25 i feltet **Genanskaffelsesprisfaktor** og 0 i feltet **Faktor for forsikret værdi** for alle anlægsaktivgrupper, undtagen gruppen med **kontormøbler** og gruppen med **computere**.
2.  For gruppen med **kontormøbler** skal du skrive 4,25 i feltet **Genanskaffelsesprisfaktor** og 0 i feltet **Faktor for forsikret værdi**.
3.  For gruppen med **computere** skal du skrive -10 i feltet **Genanskaffelsesprisfaktor** og -10 i feltet **Faktor for forsikret værdi**.
4.  På siden **Opdater genanskaffelsespriser og forsikrede værdier** skal du klikke på **OK** for at udføre genberegningen for alle anlægsaktiver.

Næste dag får du besked fra chefen om, at værdien på computere er formindsket med 8 % i stedet for 10 %, så du skal rette genanskaffelsesprisen og den forsikrede værdi. Du kan rette fejlen ved at bruge en af to metoder:
-   Rediger felterne **Forsikret værdi** og **Genanskaffelsespris** manuelt på siden **Anlægsaktiver** for de enkelte anlægsaktiver i anlægsaktivgruppen med **computere**. Beregn og angiv manuelt værdierne, som om du havde reduceret det oprindelige beløb med 8 %. Ved at følge denne metode bruger du ikke siden **Opdater genanskaffelsespriser og forsikrede værdier**.
-   Angiv faktorer for genanskaffelsespris og forsikret værdi for gruppen med **computere** i felterne **Genanskaffelsesprisfaktor** og **Faktor for forsikret værdi** på siden **Anlægsaktivgrupper**. Derved nulstilles aktiverne til deres oprindelige værdi (før reduktionen på 10 %), samtidig med at der anvendes en reduktion på 8 % på den oprindelige værdi. Brug derefter siden **Opdater genanskaffelsespriser og forsikrede værdier** til at genberegne værdierne, afhængigt af de faktorer, du har angivet.

> [!NOTE]  
> Du kan ikke tilbageføre faktoren -10 ved at angive en positiv faktor på 10 (eller en faktor på 2, som er differencen mellem -10 og -8), da beløbene ikke beregnes som forventet. 







[!INCLUDE[footer-include](../../includes/footer-banner.md)]