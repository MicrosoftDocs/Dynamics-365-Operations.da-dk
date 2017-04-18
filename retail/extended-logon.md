---
title: Konfigurere logon udvidede funktioner for sky POS og MPOS
description: "Denne wiki dækker dine muligheder for at konfigurere udvidet logon til sky-POS og Retail Modern POS (MPOS)."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 0dc80784a5c9a7de6009826284cb68f1aee83f70
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Konfigurere logon udvidede funktioner for sky POS og MPOS

Denne wiki dækker dine muligheder for at konfigurere udvidet logon til sky-POS og Retail Modern POS (MPOS).

<a name="setting-up-extended-logon"></a>Konfigurere udvidet logon
=========================

Du kan finde installationsprogrammet til stregkodemasker på **detail- og commerce**&gt;**kanal setup**&gt;**POS installationsprogrammet**&gt;**profiler for POS**&gt;**funktionalitetsprofiler**. Oversigtspanelet **Funktioner** indeholder følgende indstillinger, der er relateret til udvidet logon.

### <a name="staff-bar-code-logon"></a>Logon med medarbejderstregkode

Når indstillingen **Logon med medarbejderstregkode** er aktiveret, kan medarbejdere, der har fået tildelt udvidet logon til deres POS-legitimationsoplysninger, logge på ved hjælp af en stregkode.

### <a name="staff-bar-code-logon-requires-password"></a>Medarbejderlogon med stregkode kræver adgangskode

Når indstillingen **Medarbejderlogon med stregkode kræver adgangskode** er aktiveret, vælger logon med medarbejderstregkode kun den medarbejder, der er tildelt til det udvidede logon, der vises. Medarbejdere skal stadig angive deres adgangskode, når denne indstilling er aktiveret.

### <a name="staff-card-logon"></a>Logon med medarbejderkort

Når indstillingen **Logon med medarbejderkort** er aktiveret, kan medarbejdere, der har fået tildelt udvidet logon til deres POS-legitimationsoplysninger, logge på ved hjælp af en magnetstribe.

### <a name="staff-card-logon-requires-password"></a>Logon med medarbejderkort kræver adgangskode

Når indstillingen **Logon med medarbejderkort kræver adgangskode** er aktiveret, vælges ved logon med medarbejderkort kun den medarbejder, der er tildelt til det udvidede logon, der vises. Medarbejdere skal stadig angive deres adgangskode, når denne indstilling er aktiveret.

<a name="assigning-an-extended-logon"></a>Tildele et udvidet logon
===========================

Som standard er det kun chefer, der kan tildele udvidet logon til medarbejdere. Hvis du vil tildele udvidet logon, kan du gå til **Extended log på** i POS. Derefter søge efter en arbejder ved at angive hans eller hendes operatør-ID i søgefeltet. Vælg medarbejderen, og klik derefter på **Tildel**. På næste side skal det udvidede logon stryges eller scannes for at tildele medarbejderen. Hvis strygningen eller scanning indlæses, bliver knappen **OK **tilgængelig. Klik på **OK** for at gemme det udvidede logon for den medarbejder.

<a name="deleting-an-extended-logon"></a>Slette et udvidet logon
==========================

Hvis du vil slette det udvidede logon, der er tildelt til en medarbejder, søger du efter medarbejderen ved hjælp af handlingen **Udvidet logon**. Vælg medarbejderen, og klik derefter på **Fjern tildeling**. Alle udvidede logonoplysninger, som er knyttet til medarbejderen, er fjernet.

<a name="extending-extended-logon"></a>Udvide udvidet logon
========================

Logontjenesten kan udvides til at understøtte yderligere enheder med udvidet logon, f.eks. håndfladescannere. Yderligere oplysninger finder du i dokumentationen om POS-udvidelsesmuligheder.

<a name="using-extended-logon"></a>Brug af udvidet logon
====================

Når Udvidet logon er konfigureret, og en medarbejder har fået tildelt en stregkode eller magnetstribe, skal medarbejderen har blot stryge eller scanne sit kort, mens POS-logonsiden vises. Hvis der også kræves en adgangskode, før logon kan fortsætte, kan medarbejderen indtaste sin adgangskode.

