---
title: Styring af arbejdstimer
description: I dette emne beskrives styring af arbejdstimer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0d2f4e86b5dec84d4a24db6a4f9f9f16f6a765bd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424522"
---
# <a name="work-hour-control"></a>Styring af arbejdstimer

[!include [banner](../../includes/banner.md)]

 

I Styring af arbejdstimer kan du beregne timer for at få et overblik over de faktiske timer i forhold til budgetterede timer på anlægsaktiver, arbejdssteder eller arbejdsordrer. De faktiske timer er baseret på bogførte transaktioner.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Styring af arbejdstimer for aktiver, arbejdssteder og arbejdsordrer

De beregninger, der foretages for aktiver, arbejdssteder og arbejdsordrer, er næsten identiske. Den eneste forskel er, at for aktiver og arbejdssteder kan du også medtage underaktiver og underordnede arbejdssteder i beregningen. Datoen er den transaktionsdato, da registreringen blev foretaget.

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Styring af aktivtimer** eller **Timestyring for arbejdssted** eller **Styring af aktiver** > **Forespørgsler** > **Arbejdsordrer** > **Styring arbejdsordretimer**.

2. I dialogboksen **Styring af aktivtimer**.

3. Vælg en periode, der skal beregnes, i felterne **Fra dato** og **Til dato**, i **Styring af aktivtimer** / **Timestyring for arbejdssted** / **Styring arbejdsordretimer**.

4. Hvis det er nødvendigt, skal du vælge en **Økonomisk dimensionsopsætning**, der skal medtages i beregningen.

5. Vælg "Ja" på til/fra-knappen **Spring over nul**, hvis du ikke vil have vist resultater, der indeholder nul timer.

6. Du kan bruge feltet **Niveau** til at angive, hvor detaljerede timestyringslinjerne skal være i forbindelse med arbejdssteder. 

    Hvis du f.eks. indsætter tallet "1" i feltet, og du har et arbejdsstedshierarki med flere niveauer, vises alle timestyringslinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. 
    
    Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle timestyringslinjer på alle de arbejdsstedsniveauer, de er relateret til.

7. Vælg "Ja" i til/fra-knappen **Medtag underaktiver** for at få vist omkostninger, der er relateret til underaktiver som separate linjer.

8. Hvis du vil begrænse søgningen, kan du vælge bestemte aktiver / arbejdssteder / arbejdsordrer i oversigtspanelet **Poster, der skal indgå**.

9. Klik på **OK** for at starte beregningen.

10. Klik på **Sammenlæg pr.**-knapperne på siden **Styring af aktivtimer** for at få vist det nødvendige detaljeringsniveau i beregningen. De valgte **Sammenlæg pr.**-knapper er fremhævet. Klik på en knap for at aktivere eller deaktivere den.

## <a name="example"></a>Eksempel

I skærmbilledet herunder vises et eksempel på en beregning af **Styring af aktivtimer**.

- I feltet **Oprindeligt budget** vises budgetterede timer fra arbejdsordrebudgettet. 
- I feltet **Faktiske timer** vises bogførte timer på arbejdsordrer. 
- I feltet **Bindende timer** vises det samlede antal timer, som dit firma er bundet til i forbindelse med arbejdsordrer.

![Eksempel på beregning af Styring af aktivtimer](media/04-controlling-and-reporting.png)

Du kan også foretage en timeberegning ved at vælge flere aktiver i **Alle aktiver** eller **Aktive aktiver**. Derefter skal du klikke på knappen **Timestyring** i oversigtspanelet **Generelt**. De valgte anlægsaktiver indsættes automatisk i feltet **Aktiv** i oversigtspanelet **Poster, der skal indgå**. Klik på **OK** i dialogboksen **Styring af aktivtimer**, hvorefter beregningen for de valgte aktiver vises. Den samme procedure kan udføres for arbejdssteder i **Alle arbejdssteder** eller **Aktive arbejdssteder** og for arbejdsordrer i **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]