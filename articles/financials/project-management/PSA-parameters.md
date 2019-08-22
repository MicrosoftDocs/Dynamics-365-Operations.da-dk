---
title: Project Service Automation-integrationsparametre
description: I dette emne beskrives, hvordan du konfigurerer, hvordan standarddata indtastes, når du integrerer Microsoft Dynamics 365 for Project Service Automation med Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b58d2de323395db97d1f8ea146da55bba4e0f9c6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838974"
---
# <a name="project-service-automation-integration-parameters"></a>Integrationsparametre for Project Service Automation

[!include[banner](../includes/banner.md)]

På siden **Integrationsparametre for Project Service Automation** kan du konfigurere, hvordan standarddata skal indtastes, når du integrerer Microsoft Dynamics 365 for Project Service Automation med Microsoft Dynamics 365 for Finance and Operations. For at projekter kan synkroniseres korrekt fra Project Service Automation til Finance and Operations, skal du konfigurere følgende felter.

> [!NOTE]
> - Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.0.
> - Integration af faktiske oplysninger er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.0.1 eller nyere.
> - Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet. Hvis du skal nulstille regnskabsfordelingerne, anbefalede vi, at du også installerer KB 4131710.

| Fane                    | Felt                | Betegnelse |
|------------------------|----------------------|-------------|
| Almindelig                | Standardprojekttype | Vælg standardprojekttypen. Når projekter synkroniseres fra Project Service Automation, bruges denne værdi, hvis du ikke har angivet en standardværdi i integrationsskabelonen. Under synkronisering angives feltet **Projekttype** for nye projekter til denne værdi. Værdien kan dog opdateres, når projektkontraktlinjerne synkroniseres fra Project Service Automation. |
|                        | Tidskategori        | Vælg standardtidskategorien. Denne værdi bruges, når timeestimater synkroniseres fra Project Service Automation. Når timeestimaterne og de faktiske timeoplysninger synkroniseres fra Project Service Automation, angives feltet **Kategori** for nye projekttimeestimater i Finance and Operations til denne værdi. |
|                        | Gebyrkategori         | Vælg standardgebyrkategorien. Denne værdi bruges, når faktiske gebyrer synkroniseres fra Project Service Automation. Når de faktiske gebyrer synkroniseres fra Project Service Automation, angives feltet **Kategori** i nye gebyrtransaktioner i Finance and Operations til denne værdi. |
| Projektgruppestandarder | Projekttype         | Klik på **Ny** for at tilføje en række, hvor du kan vælge den projekttype, som standardprojektgruppen skal angives for. En bestemt projekttype kan kun vælges én gang i konfigurationen. |
|                        | Projektgruppe        | Vælg standardprojektgruppen for den valgte projekttype. Når nye projekter synkroniseres fra Project Service Automation, angives feltet **Projektgruppe** til standardværdien for projekttypen, hvis du ikke har angivet en standardværdi i integrationsskabelonen. |
| Faktureringstypestandarder  | Faktureringstype         | Klik på **Ny** for at tilføje en række, hvor du kan vælge den faktureringstype, som standardlinjeegenskaben skal angives for. En bestemt faktureringstype kan kun vælges én gang i konfigurationen. |
|                        | Linjeegenskab        | Vælg standardlinjeegenskaben for den valgte faktureringstype. Når nye timeestimater, nye udgiftsestimater eller nye faktiske tal synkroniseres fra Project Service Automation, angives feltet **Linjeegenskab** til standardværdien for faktureringstypen. |
| Låsning af funktonalitet  | Ikke tilgængelig       | Vælg den funktion, der skal deaktiveres i Finance and Operations for projekter og kontrakter, der stammer fra Project Service Automation. Du kan for eksempel deaktivere muligheden for at redigere kontrakter og projekter, oprette arbejdsopgavehierarkier og indtaste timesedler i Finance and Operations. Regnskabsrelaterede felter vil fortsat være aktiverede, selvom de ikke er tilgængelige med parameterindstillingen. Som standard er alle funktioner aktiveret. |
