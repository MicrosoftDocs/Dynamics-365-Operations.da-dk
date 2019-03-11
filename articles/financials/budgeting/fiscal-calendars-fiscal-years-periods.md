---
title: Regnskabskalendere, regnskabsår og perioder
description: I denne artikel beskrives regnskabskalendere, regnskabsår og -perioder, og hvordan du kan udnytte dem til juridiske enheder, anlægsaktiver og budgettering.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 360695ddfbcf1eab62dd5087e1b5bb34ccaf7c7f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "361653"
---
# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Regnskabskalendere, regnskabsår og perioder

[!include [banner](../includes/banner.md)]

I denne artikel beskrives regnskabskalendere, regnskabsår og -perioder, og hvordan du kan udnytte dem til juridiske enheder, anlægsaktiver og budgettering.

Regnskabskalendere danner rammen om en organisations økonomiske aktivitet. Hver regnskabskalender omfatter et eller flere regnskabsår, og hvert regnskabsår omfatter flere perioder. Regnskabskalendere kan være baseret på kalenderåret, fra 1. januar til 31. december, eller på vilkårlige andre datoer, som du vælger. Nogle organisationer kan f.eks. vælge en regnskabskalender, der begynder den 1. juli i et år og slutter den 30. juni det følgende år. 

Der er ingen grænser for, hvor mange regnskabskalendere du kan oprette, og ingen grænse for antallet af regnskabsår, der kan oprettes til en regnskabskalender. Hver regnskabskalender er uafhængig af din organisation og kan bruges af flere juridiske enheder i organisationen. En organisation har f.eks. otte afdelinger, og hver afdeling er en separat juridisk enhed. Fem af dem deler samme regnskabskalender, og tre bruger forskellige regnskabskalendere. Du kan oprette én regnskabskalender for de fem juridiske enheder, der deler den samme regnskabskalender, og derefter oprette separate regnskabskalendere for de andre juridiske enheder.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Oprette regnskabskalendere, regnskabsår og perioder
Du kan oprette og slette regnskabskalendere, regnskabsår og perioder på siden Regnskabskalender. Du kan også opdele eksisterende perioder og oprette ultimoperioder, der kan bruges til at lukke et regnskabsår. 

Formålet med en ultimoperiode er at adskille finansposteringer, der genereres, når et regnskabsår afsluttes. Når ultimoposterne indgår i én regnskabsperiode, er det lettere at oprette regnskaber, der enten omfatter eller ikke omfatter forskellige former for ultimoposter. Hvis et regnskabsår er inddelt i 12 regnskabsperioder, er ultimoperioden normalt den 13. periode. Men det er dog muligt at oprette en ultimoperiode på basis af en hvilken som helst periode med statusangivelsen Åben. 

Når du opretter en ultimoperiode, skal du vælge en periode med statusangivelsen Åben, som har de datoer, du vil bruge. Den nye ultimoperiode kopierer start- og slutdatoerne fra den eksisterende periode. Den oprindelige periode findes fortsat. Du kan f.eks. vælge Periode 12, som er sidste periode i regnskabsåret, og som har datoer fra 1. august til og med 31. august. Derefter angiver du et navn til ultimoperioden, f.eks. Ultimo. Når du har oprettet ultimoperioden, har du nu den oprindelige periode og ultimoperioden. Begge har datoer, der starter d. 1. august og slutter d. 31. august.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Vælge regnskabskalendere til finanskonti, anlægsaktiver og budgetcyklusser
Regnskabskalendere bruges sammen med afskrivning af anlægsaktiver, økonomiske bevægelser og budgetcyklusser. Når du opretter en regnskabskalender, kan du bruge den til flere formål. Du kan vælge en regnskabskalender til en værdimodel eller afskrivningsmodel for at gøre den til en kalender for anlægsaktiver. Du kan vælge en regnskabskalender til en finanskonto for at gøre den til en finanskalender. Og du kan vælge en regnskabskalender til en budgetcyklus for at gøre den til en budgetkalender. Du kan bruge samme regnskabskalender til alle disse.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Vælg en regnskabskalender til din juridiske enhed

Vælg den regnskabskalender, du vil bruge til finanskontoen til din juridiske enhed, i formen Finans. Der skal vælges et regnskabsår på siden Finans for hver juridisk enhed. Når der er valgt et regnskabsår, kan du oprette periodestatus og tilladelser på siden Finanskalender for en hvilken som helst af de perioder, der indgår i et regnskabsår.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Vælge en regnskabskalender til anlægsaktiver

Du kan vælge en regnskabskalender til en værdimodel eller afskrivningsmodel, og denne regnskabskalender bruges af de anlægsaktiver, der bruger den valgte værdimodel eller afskrivningsmodel. Du kan vælge blandt de regnskabskalendere, der er defineret på siden Regnskabskalendere.

### <a name="define-budget-cycle-time-spans"></a>Definere tidsperioder for budgetcyklus

Budgetcyklusser angiver, hvor længe et budget anvendes. Budgetcyklusser kan omfatte en del af et regnskabsår eller flere regnskabsår, f.eks. en toårig budgetcyklus eller en treårig budgetcyklus. En tidsperiode for budgetcyklus definerer antallet af perioder, der er medtaget i budgetcyklussen. Når du skal specificere tidsperioden for budgetcyklussen, skal du bruge siden Tidsperioder for budgetcyklus.

## <a name="maintain-periods-for-your-organization"></a>Vedligeholde perioder for organisationen
Du kan bruge siden Finanskalender til at få vist detaljer i regnskabskalenderen og de regnskabsår og -perioder, som bruges af organisationen. Du kan også ændre status for perioderne og vælge, hvilke brugere der kan bogføre regnskabstransaktioner i perioder. I starten af en ny periode kan det f.eks. være, at en gruppe brugere skal kunne afslutte bogføring af finansposteringer i forrige periode, mens andre grupper kun arbejder i den nye periode.





