---
title: Behovsplaner
description: "Brug forskellige behovsplaner, der understøtter firmaets daglige arbejdsrutiner, simulere forskellige planlægningsstrategier, som du vil overvåge, og implementer en firmapolitik, der f.eks. vedrører intern performance eller kundetilfredshed."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: bf73ae6653cf5100e70d3ca9891c81f1a24e3574
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="master-plans"></a>Behovsplaner

[!include[banner](../includes/banner.md)]


Brug forskellige behovsplaner, der understøtter firmaets daglige arbejdsrutiner, simulere forskellige planlægningsstrategier, som du vil overvåge, og implementer en firmapolitik, der f.eks. vedrører intern performance eller kundetilfredshed. 

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

[Adskille taktisk og operativ planlægning for behovsplanlægning](http://blogs.msdn.com/b/axmfg/archive/2012/10/12/separating-tactical-and-operative-planning-for-master-scheduling.aspx)

[Varedisponering: Bruge en statisk og dynamisk behovsplan eller bruge én plan?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)




