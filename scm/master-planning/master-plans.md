---
title: Behovsplaner
description: "Du kan bruge forskellige behovsplaner til understøtter firmaets daglige arbejdsrutiner, simulere forskellige planlægningsstrategier, som du vil overvåge og implementere en firmapolitik, som en politik om intern performance eller kunde tilfredshed."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7911
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 29bb560c11e63938bea73ed8471c27563b546f8f
ms.lasthandoff: 03/31/2017


---

# <a name="master-plans"></a>Behovsplaner

Du kan bruge forskellige behovsplaner til understøtter firmaets daglige arbejdsrutiner, simulere forskellige planlægningsstrategier, som du vil overvåge og implementere en firmapolitik, som en politik om intern performance eller kunde tilfredshed. 

Du kan konfigurere behovsplaner på siden **Behovsplaner**.

Der findes to former for planer:
-   **Statisk plan** – Beregningen af varedisponering bruger de aktuelle data til at oprette en plan for nettobehov. Denne plan forbliver uændret, indtil næste gang du kører varedisponering. Det er en driftsplan, som forskellige medarbejdere i firmaet, f.eks. en indkøber eller produktionsplanlægger, kan bruge til at basere deres beslutninger på og udføre deres daglige opgaver og aktiviteter.
-   **Dynamisk plan** – Denne plan starter med den samme plan for nettobehov, der er genereret af varedisponeringen. Du kan dog opdatere den dynamiske plan, hver gang der ændres i masterdata. Dette skyldes muligvis, at du f.eks. opretter en ny salgsordre. Det giver dig mulighed for at overvåge netværket med ordreændringer og varetilgængelighed uden at forstyrre den statiske plan, som andre bruger i deres arbejdsprocesser.

Et firma kan vælge kun at arbejde med en dynamisk plan eller at bruge både en statisk og en dynamisk plan. Derudover kan du konfigurere en behovsplan, der skal afspejle en bestemt strategi eller løse et problem. Der er følgende eksempler:
-   Angiv højere lagerniveauer for at sikre sig mod manko.
-   Angiv længere sikkerhedsmargener for at beskytte sig mod upålidelige leverandører.

Du kan også angive, at den dynamiske startplan skal opdateres med den nye behovsplan, hver gang du kører varedisponering. Du kan angive disse indstillinger på siden **Varedisponeringsparametre**.



<a name="see-also"></a>Se også
--------

[Disponeringsindstillinger](coverage-settings.md)

[Adskille taktiske og udløsende planlægning for behovsplanlægning](http://blogs.msdn.com/b/axmfg/archive/2012/10/12/separating-tactical-and-operative-planning-for-master-scheduling.aspx)

[Overordnet planlægning: Brug en statisk og dynamisk behovsplan eller én plan?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)

