---
title: Vedligehold ordreforslag
description: Denne artikel indeholder oplysninger om, hvordan du administrerer planlagte ordrer. Den beskriver, hvordan du kan opdatere status for planlagte ordrer, autorisere dem og filtrere for planlagte ordre, der har samme status som en valgte planlagt ordre.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8931908fbf643a8154da70d2ad065ea47d2aa4e6
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="maintain-planned-orders"></a>Vedligehold ordreforslag

[!INCLUDE [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om, hvordan du administrerer planlagte ordrer. Den beskriver, hvordan du kan opdatere status for planlagte ordrer, autorisere dem og filtrere for planlagte ordre, der har samme status som en valgte planlagt ordre.

Du kan administrere ordreforslag fra arbejdsområdet **Varedisponering**, listen **Ordreforslag** eller listerne **Produktionsordreforslag**, **Planlagte indkøbsordrer** og **Planlagt overførsel**. Du kan bruge feltet **Status** til at registrere status. Følgende værdier bruges:

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

[Behovsplaner](master-plans.md)




