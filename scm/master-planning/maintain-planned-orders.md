---
title: Vedligehold ordreforslag
description: Denne artikel indeholder oplysninger om, hvordan du administrerer planlagte ordrer. Den beskriver, hvordan du kan opdatere status for planlagte ordrer, autorisere dem og filtrere for planlagte ordre, der har samme status som en valgte planlagt ordre.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c01a192e637bfe74a60370290db72c439faf40d0
ms.lasthandoff: 03/31/2017


---

# <a name="maintain-planned-orders"></a>Vedligehold ordreforslag

Denne artikel indeholder oplysninger om, hvordan du administrerer planlagte ordrer. Den beskriver, hvordan du kan opdatere status for planlagte ordrer, autorisere dem og filtrere for planlagte ordre, der har samme status som en valgte planlagt ordre.

Du kan administrere ordreforslag fra arbejdsområdet **Varedisponering**, listen **Ordreforslag** eller listerne **Produktionsordreforslag**, **Planlagte indkøbsordrer** og **Planlagt overførsel**. Du kan bruge feltet **Status ** til at registrere status. Følgende værdier bruges:

-   Når varedisponering opretter ordreforslag, har ordreforslagene statussen **Ubehandlet**.
-   Hvis du vælger ikke at autorisere et ordreforslag, kan du tildele det statussen **Fuldført**.
-   Når du vælger ikke at autorisere et ordreforslag, kan du tildele det statussen **Godkendt**. Denne status angiver, at du godkender autorisation af ordreforslaget, men det er ikke autoriseret endnu.

**Bemærk!** Et godkendt ordreforslag overføres i den aktuelle tilstand til næste beregning af varedisponering. Du kan autorisere ordreforslag ved at klikke på **Autoriser**. Du kan autorisere følgende ordreforslag:

-   Det ordreforslag, der er valgt.
-   Flere ordreforslag.
-   Ordreforslag oprettes via en udfoldning fra siden **Udfoldning**. Klik på **Ordreforslag**, vælg ordreforslaget, og klik derefter på **Autoriser**.

Når et ordreforslag er autoriseret, flyttes det til ordresektionen i det relevante modul. **Bemærk!** Du kan højreklikke på et ordreforslag, der har en bestemt status, og filtrere efter andre ordreforslag med samme status. Denne funktionalitet kan f.eks. være nyttig, hvis du vil filtrere efter alle ordreforslag, der har statussen **Godkendt**, så du kan autorisere dem.

<a name="see-also"></a>Se også
--------

[Master plans](master-plans.md)


