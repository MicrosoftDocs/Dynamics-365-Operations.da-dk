---
title: "Planlægning i blandet tilstand: kombinere separate, proces og lean forsyning"
description: "Denne artikel indeholder oplysninger om planlægning i blandet tilstand. Du kan udforme din forsyningskæde ud fra materialeflowet i planlægning i blandet tilstand. Microsoft Dynamics 365 for Finance and Operations sørger for, at materialeflowet følger dine modeller, uanset den valgte forsyningspoliti (kanbans, produktionsordrer, indkøbsordrer, batchordrer eller overflytningsordrer)."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 9dbbe540c919d27bafcc10614f308e5b6ba313f1
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Planlægning i blandet tilstand: kombinere separate, proces og lean forsyning

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om planlægning i blandet tilstand. Du kan udforme din forsyningskæde ud fra materialeflowet i planlægning i blandet tilstand. Microsoft Dynamics 365 for Finance and Operations sørger for, at materialeflowet følger dine modeller, uanset den valgte forsyningspoliti (kanbans, produktionsordrer, indkøbsordrer, batchordrer eller overflytningsordrer). 

Du kan vælge din overordnede strategi for at levere et produkt, uanset produktstrukturen.  

For eksempel kan du få kontrol over kanban i montagen, hvor materialer hentes fra for montageområdet for produktionsordrer, kanbans, overførsler, batchordrer, eller kombinationer, der passer til egenskaberne for din forsyningskæde, men du kan stadig have fuld synlighed på tværs af forsyninger. Denne funktion giver optimeret forsyningskædeprocesser og forbedret synlighed i forsyningskæden.  

Granulariteten for de forsyningspolitikker, der bruges til behovsplanlægning, afhænger af den lagringsdimension, der er aktiveret som disponeringsdimensioner. Hvis du vil aktivere behovsplanlægningen til at styre genopfyldning og levering af forskellige typer placeringer (for eksempel ved at adskille produktionsanlægget for forskellige produktionsenheder eller ved at adskille de forskellige typer af materiale og lagre med færdigvarer), anbefaler vi, at du aktiverer Sted og Lagersted som disponeringsdimensioner. Du kan også udelade Lagersted som disponeringsdimension. I dette tilfælde, hvis du bruger avanceret lokationsstyring, styres alle bevægelser på et lagersted af lagerstedsarbejde, hvorimod alle bevægelser på tværs af lagersteder kan kontrolleres ved udbetalingskanbans.

## <a name="supply-policies"></a>Forsyningspolitikker
Planlægningskontroller for blandet tilstand i Finance and Operations styrer, hvordan et produkt er leveret på baggrund af forsyning, hvordan afledte behov (forbrug af varer fra en \[stykliste\]) er udstedt. Baseret på ordretype henter systemet automatisk materialer for at imødekomme behov.  

Forsyningspolitikker kan defineres på niveauet for produktet eller på en granularitet, der understøtter dine krav. Du definerer granulariteten af forsyningspolitikker på siden **Standardindstillinger for ordre**.  

Forsyningspolitikker kan styres af produkt, varedimensioner (konfiguration, farve og størrelse), sted og lagersted. Denne opsætning er udføres på siden **Varedisponering**.  

Standardordretypen bestemmer, hvilken ordre varedisponering genererer.  

Uanset hvordan forsyningskæden er udformet, understøtter Finance and Operations din blanding af leveringspolitikker. Du kan få produktionsordrer, der er hentet fra kanbans. Du kan også have en batchordre, der kræver et produkt, der leveres af overførsler eller kanbans.  

Finance and Operations sørger for, at materialeflowet følger modellen.  

Lageret til plukning af materiale er tildelt dynamisk under kørsel, når forsyningspolitikken er defineret.  

Typisk oprettes kanbans ikke for fremtidige datoer, da en kanban har en kort levetid. For at opretholde fuld synlighed i forsyningskæde har vi introduceret det nye planlægningskoncept "planlagt kanban," der bruges til at beregne afledte behov og hjælper med at sikre, at kravene er hentet baseret på den samme logik, der bruges, når den aktuelle kanban er oprettet.  

Den samme logik er til stede ved alle øvrige typer forsyningspolitikker. Derfor er langsigtet planlægning for materialer baseret på den samme logik, som du forventer at køre med de faktiske ordrer, når produktion og forsyning er blevet godkendt.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Krydsforsyningspolitik for materialefordeling – ressourceforbrug på styklister
Ressourceforbrug er en vigtig funktion. Ressourceforbrug giver et lagersted til plukning materialer mulighed for at blive valgt, baseret på forsyningspolitikken (ordretype) og også letter vedligeholdelsen af stamdata.  

Ressourceforbrug kræver, at det lagersted, der er plukket materialer fra, tildeles baseret på den måde, produktet leveres. Med andre ord, på kørselstidspunktet finder systemet de ressourcer, der skal bruges til produktion. Baseret på disse ressourcer finder systemet derefter pluklagerstedet.  

For arbejde der er uafhængig af en forsyningspolitikken, skal du ikke ændre oplysningerne på styklisten, hvis leveringen er ændret. For ad hoc-ændringer sikrer Finance and Operations, at materialer er hentet fra det rigtige lagersted.

## <a name="process-manufacturing--the-production-type"></a>Procesproduktion – produktionstypen
For fuld fleksibilitet i blandet tilstand anbefaler vi, at du bruger produktionstypestyklister for alle produkter. Du kan derefter bruge produktionsordrer, kanbans, overførselsordrer eller produktionsordrer til forsyning af et produkt. For procesproduktion skal du bruge en produktionstype af **Formel**, **Samprodukt**, **Biprodukt** eller **Planlægningsvare**. Kanbans og produktionsordrer kan ikke bruges til disse produktionstyper.



