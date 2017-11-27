---
title: Konfigurere udvidede logonfunktioner for Cloud POS og MPOS
description: "Dette emne dækker dine muligheder for at konfigurere udvidet logon til Cloud POS og Retail Modern POS (MPOS)."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e9ce03dfdc5dc027344186e0334b2ac2bc9341e
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Konfigurere udvidede logonfunktioner for Cloud POS og MPOS

[!include[banner](includes/banner.md)]


Dette emne dækker dine muligheder for at konfigurere udvidet logon til Cloud POS og Retail Modern POS (MPOS).

<a name="setting-up-extended-logon"></a>Konfigurere udvidet logon
=========================

Du kan finde opsætningen af stregkodemasker på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Funktionalitetsprofiler**. Oversigtspanelet **Funktioner** indeholder følgende indstillinger, der er relateret til udvidet logon.

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

Som standard er det kun chefer, der kan tildele udvidet logon til medarbejdere. Hvis du vil tildele udvidet logon, skal du gå til **Udvidet logon** i POS. Søg derefter efter en medarbejder ved at angive hans eller hendes operatør-id i søgefeltet. Vælg medarbejderen, og klik derefter på **Tildel**. På næste side skal det udvidede logon stryges eller scannes for at tildele medarbejderen. Hvis strygningen eller scanning indlæses, bliver knappen **OK** tilgængelig. Klik på **OK** for at gemme det udvidede logon for den medarbejder.

<a name="deleting-an-extended-logon"></a>Slette et udvidet logon
==========================

Hvis du vil slette det udvidede logon, der er tildelt til en medarbejder, søger du efter medarbejderen ved hjælp af handlingen **Udvidet logon**. Vælg medarbejderen, og klik derefter på **Fjern tildeling**. Alle udvidede logonoplysninger, som er knyttet til medarbejderen, er fjernet.

<a name="extending-extended-logon"></a>Udvide udvidet logon
========================

Logontjenesten kan udvides til at understøtte yderligere enheder med udvidet logon, f.eks. håndfladescannere. Yderligere oplysninger finder du i dokumentationen om POS-udvidelsesmuligheder.

<a name="using-extended-logon"></a>Brug af udvidet logon
====================

Når Udvidet logon er konfigureret, og en medarbejder har fået tildelt en stregkode eller magnetstribe, skal medarbejderen har blot stryge eller scanne sit kort, mens POS-logonsiden vises. Hvis der også kræves en adgangskode, før logon kan fortsætte, kan medarbejderen indtaste sin adgangskode.




