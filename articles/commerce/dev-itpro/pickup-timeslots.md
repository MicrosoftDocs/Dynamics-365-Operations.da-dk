---
title: Oprette og opdatere tidsintervaller for kundeafhentning
description: I dette emne beskrives, hvordan du opretter, konfigurerer og opdaterer tidsintervaller for kundeafhentning i Commerce Headquarters.
author: anupamar-ms
manager: AnnBe
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: 6dc2be8a6f62ce13068ce2242f92ef17830c2447
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205741"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Oprette og opdatere tidsintervaller for kundeafhentning

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du opretter, konfigurerer og opdaterer tidsintervaller for kundeafhentning i Commerce Headquarters.

Tidsintervalfunktionen giver detailhandlere mulighed for at definere et tidsinterval for varer, som leveringsmåden ved kundeafhentning er slået til for. Med tidsintervaller kan detailhandlere definere dage og tidspunkter, hvor ordrer kan afhentes fra en butik. Detailhandlende kan også definere antallet af ordrer, der kan afhentes i en given periode. På denne måde kan detailhandlerne begrænse antallet af ordrer, der kan afhentes på en given dag og på et givent tidspunkt. Resultatet er en bedre oplevelse for kunderne.

> [!NOTE]
> Tidsintervalfunktionen er tilgængelig i Microsoft Dynamics 365 Commerce version 10.0.15 og nyere.

I følgende illustration vises et eksempel på valg af tidsinterval under betaling ved e-handel.

![Eksempel på valg af tidsinterval under betaling ved e-handel](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Egenskaber for tidsinterval

Et tidsinterval er et specifikt interval, hvor en kunde kan vælge at hente en ordre fra en bestemt butik eller lokalitet. Funktionen til styring af tidsintervaller er kun tilgængelig, når leveringsmåden ved kundeafhentning er konfigureret i Dynamics 365 Commerce.

Et tidsinterval defineres ved hjælp af følgende egenskaber:

- **Leveringsmåde** – Angiv den afhentningsmåde for leveringen, som tidsintervallet gælder for.
- **Minimum dage** og **Maksimum dage** – Angiv de tidligste og seneste datoer, der kan vælges for afhentning i forhold til den dato, hvor ordren er afgivet. 

    Egenskaben **Minimum dage** sikrer, at der er tilstrækkelig tid til, at forhandleren kan behandle ordren, før den er klar til afhentning. Egenskaben **Maksimum dage** sikrer, at brugeren ikke kan vælge en dato, der ligger for langt ude i fremtiden. Hvis minimumværdien f.eks. er **1**, og der afgives en ordre den 20. september, er den tidligste dag, hvor ordren vil være tilgængelig for afhentning, den næste dag, der kan vælges (21. september). På samme måde kan du definere det maksimale antal dage, en ordre kan afhentes, ved at angive en maksimumværdi. Når der er defineret minimum- og maksimumværdier, kan webstedets brugere kun se og vælge et bestemt interval af dage under betalingen.

    Du kan indstille minimumværdien til en decimalværdi, der er mindre end 1. Hvis f.eks. afhentning er tilgængelig i fire timer, efter at en ordre er afgivet, skal du indstille minimumværdien til **0,17** (= 4 ÷ 24, rundet op til to decimaler). Hvis du indstiller minimumværdien til en decimalværdi, der er større end 1, afrundes den dog altid op til det nærmeste hele tal. En værdi på **1,2** rundes f.eks. op til **2**. Hvis du tilsvarende indstiller maksimumværdien til en decimalværdi, afrundes den dog altid op til det nærmeste hele tal. 

- **Startdato** og **Slutdato** – Angiv start- og slutdatoer for tidsintervallet. Hvert tidsinterval har en startdato og en slutdato. Det gør det muligt for dig at tilføje forskellige tidsintervaller i løbet af hele året (f.eks. afhentning i løbet af ferier). Hvis start- og slutdatoer for et tidsinterval ændres, efter at en ordre er afgivet, gælder ændringerne ikke for den pågældende ordre. Når du definerer start-og slutdatoer, skal du overveje at gemme lukkedatoer (f.eks. juledag) og sikre, at der ikke defineres tidsintervaller for disse dage.
- **Aktive afhentningstimer** – Angiv den periode, hvor afhentning er tilladt. Afhentningstiden kan f.eks. være mellem kl. 14 og 17 hver dag. Med denne egenskab kan afhentningstiden være uafhængig af butikkens åbningstider. Derfor kan forhandleren konfigurere afhentningstider, der opfylder butikkens specifikke krav. Når du definerer de aktive timer for afhentning, skal du overveje at gemme tiderne og sikre, at der ikke defineres afhentningstider, når butikken er lukket.

    > [!NOTE]
    > Tiderne for afhentning i butikken skal defineres i tidszonen for den relevante butik.

- **Tidsinterval** – Angiv den varighed, der kan tildeles til hvert tidsinterval. Varigheden af hver tidsinterval kan f.eks. angives i trin på 15 minutter, 30 minutter eller en time. Hvis værdien for tidsinterval er 0, er tidsinterval tilgængeligt for hele varigheden mellem start- og sluttid.
- **Slots pr. interval** – Angiv det antal kunder eller ordrer, der kan betjenes ved afhentning i løbet af hvert tidsinterval. Du kan f.eks. angive **1,** **2**, **3** eller et andet helt tal.
- **Aktive dage** – Angiv de ugedage, hvor tidsintervaller for afhentning er aktive. Denne egenskab gør det muligt for forhandleren at definere de dage, hvor afhentning af ordrer kan understøttes.
- **Detailkanaler** – Angiv detailkanalerne. Hvert tidsinterval kan knyttes til en eller flere detailbutikker. Afhængigt af en butiks åbningstider, kan der oprettes en eller flere tidsintervalposter, som kan knyttes til en kanal. 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Der kan kun konfigureres én tidsintervalskabelon pr. kanal. Disse kanaler omfatter fysiske butikker, callcentre, mobilenheder og e-handelswebsteder.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Konfigurere tidsintervalfunktionen i Commerce Headquarters

Der skal defineres tidsintervaller for hver leveringsmåde for afhentning i Commerce Headquarters, så POS- og e-handelskanaler kan referere til dem.

- Der kan kun knyttes én tidsintervalskabelon til hver butik eller kanal.
- Hvert tidsinterval, der oprettes, skal være entydig for hver leveringsmåde i hver skabelon.
- Når tidsintervalfunktionen er konfigureret, vil tidsintervalkalenderen være tilgængelig for de valgte butikker eller butiksgrupper. Den vil også være synlig i POS, som reference.

Følg disse trin for at konfigurere tidsintervalfunktionen i Commerce Headquarters.

1. Gå til **Commerce** \> **Konfiguration af kanal** \> **Tidsinterval for afhentning i butik**.
1. Vælg **Ny** for at oprette en ny tidsintervalskabelon. Hvis du vil bruge en eksisterende skabelon, skal du vælge skabelonen i venstre rude.
1. Angiv værdier i felterne **Id for tidsinterval** og **Beskrivelse**.
1. Vælg **Tilføj** i oversigtspanelet **Ordreafhentning - Tidsindstillinger**.
1. I dialogboksen **Ordreafhentning - Tidsindstillinger** skal du definere datointervallet, leveringsmåde, aktive leveringstimer, antal aktive dage, tidsinterval, slots pr. interval og andre indstillinger.

    Hvis tidsintervaller er statiske i en overskuelig fremtid, skal du indstille feltet **Slutdato** til **Aldrig**.

    > [!NOTE]
    > Du kan oprette flere skabeloner, men kun én skabelon kan knyttes til en enkelt kanal eller butik.

    ![Dialogboksen Ordreafhentning - Tidsindstillinger](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Vælg **OK**, når du er færdig.
1. Hvis tidsintervallerne for en dag varierer, kan du oprette flere poster i oversigtspanelet **Ordreafhentning - Tidsindstillinger** for at sikre, at datoer og klokkeslæt ikke overlapper hinanden.
1. I oversigtspanelet **Detailkanaler** skal du vælge **Tilføj** for at knytte skabelonen for tidsrubrikken til de butikker eller kanaler, hvor den skal bruges.
1. Brug pileknapperne eller vælg (eller fjern markeringen af) de butikker, områder og organisationer, skabelonen skal knyttes til, i dialogboksen **Vælg organisationsnoder**.

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Vælg **OK**, når du er færdig.
1. På siden **Distributionstidsplan** skal du køre jobbene **1070** og **1135** for at synkronisere data til kanalerne.

## <a name="time-slot-selection-for-pos-orders"></a>Valg af tidsinterval for POS-ordrer

Når en ordre eller en ordrelinje identificeres for afhentning i POS, kan kassereren vælge afhentningsbutik eller -lokalitet samt et dato- og klokkeslætsinterval. Hvis en kunde har en afhentningsordre i en anden butik, kan kassereren vælge datoer, hvor varen til afhentning er tilgængelig i den pågældende butik. Butiksopslaget giver en reference til datoerne og åbningstiderne.

I følgende illustration vises et eksempel på valg af tidsinterval for en POS-ordre.

![Et eksempel på valg af tidsinterval for en POS-ordre](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>Valg af tidsinterval for e-handelsordrer

Du kan finde oplysninger om, hvordan du kan gøre tidsinterval tilgængelig for e-handelsordrer, i [modulet med afhentningsoplysninger](../pickup-info-module.md).

> [!NOTE]
> Brugere kan kun få vist eller redigere tidsintervaller for afhentning på betalingssiden for en Commerce-websted, hvis modulet med oplysninger om afhentning er føjet til den pågældende side. Hvis betalingssiden ikke indeholder modulet med afhentningsoplysninger, placeres ordrer, uden at brugerne får mulighed for at angive eller få vist oplysninger om tidsintervaller.

I følgende illustration vises et eksempel på en e-handelsordre, hvor der er valgt et tidsinterval for afhentning.

![Eksempel på en e-handelsordre, hvor der er valgt et tidsinterval for afhentning](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>Valg af tidsinterval for callcenter-ordrer

I callcenter-appen kan callcenter-medarbejdere vælge afhentningsbutik eller lokalitet samt en dato og et tidsrum, som er markeret i følgende illustration.

![Eksempel på en callcenter-ordre, hvor der er valgt et tidsinterval for afhentning](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Modul med afhentningsoplysninger](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]