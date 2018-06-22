---
title: Project Service Automation-integrationsparametre
description: Du kan konfigurere standardindstillinger for data ved integration af Project Service Automation med Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: da-dk
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Project Service Automation-integrationsparametre

På siden med **Integrationsparametre for Project Service Automation** kan konfigurere indstillinger, der skal bruges som standard for data, når Project Service Automation integreres med Finance and Operations. Følgende skal konfigureres, for at projekter kan synkroniseres korrekt fra Project Service Automation i Finance and Operations.

> [!NOTE]
> Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelige i Dynamics 365 for Finance and Operations version 8.0.




| **Fane**                      | **Felt**                          | **Beskrivelse**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Generelt**                  | **Standardprojekttype**               | Vælg standarden for **Projekttype**, hvilket er, når projekter synkroniseres fra Project Service Automation, hvis du ikke har angivet en standardværdi i integrationsskabelonen. Under synkroniseringen får nye projekter denne værdi i **Projekttype** og kan opdateres, når projektkontraktlinjerne synkroniseres fra Project Service Automation.               |
| **Generelt**                  | **Tidskategori**                      | Vælg standarden for **Tidskategori**, hvilket er, når timeestimater synkroniseres fra Project Service Automation. Under synkroniseringen har nye projekttimebudgetter i Finance and Operations **Kategori** indstillet til denne værdi, når timeestimaterne og de faktiske timeoplysninger synkroniseres fra Project Service Automation.   |
| **Generelt**                  | **Gebyrkategori**                       | Vælg standarden for **Gebyrkategori**, hvilket er, når faktiske gebyrer synkroniseres fra Project Service Automation. Under synkroniseringen har nye gebyrtransaktioner i Finance and Operations **Kategori** indstillet til denne værdi, når de faktiske gebyrer synkroniseres fra Project Service Automation.          |
| **Projektgruppestandarder**   | **Projekttype** | Klik på **Ny** for at tilføje en række, hvor du kan vælge den projekttype, som standardprojektgruppen skal angives for. En bestemt projekttype kan kun vælges én gang i konfigurationen.              
|                              | **Projektgruppe**          | Vælg standardprojektgruppen for den angivne projekttype. Når nye projekter synkroniseres fra Project Service Automation, er **Projekttype** standarden baseret på projekttypen, hvis du ikke har angivet en standardværdi i integrationsskabelonen.  |
| **Faktureringstypestandarder**    | **Faktureringstype** | Klik på **Ny** for at tilføje en række, hvor du kan vælge den faktureringstype, som standardlinjeegenskaben skal angives for. En bestemt faktureringstype kan kun vælges én gang i konfigurationen.          |
|                              | **Linjeegenskab**| Vælg standardlinjeegenskaben for den angivne faktureringstype. Når nye timeestimater, nye udgiftsestimater eller nye faktiske oplysninger synkroniseres fra Project Service Automation, er **Linjeegenskab** standarden baseret på faktureringstypen.          |
| **Låsning af funktonalitet**    |                   | Vælg den funktion, der skal deaktiveres i Finance and Operations for projekter og kontrakter, der stammer fra Project Service Automation. Du kan for eksempel vælge at deaktivere muligheden for at redigere kontrakter og projekter, oprette arbejdsopgavehierarkier og indtaste timesedler i Finance and Operations. Regnskabsrelaterede felter vil fortsat være aktiverede, selvom de ikke er tilgængelige med parameterindstillingen. Som standard er alle funktioner aktiveret.           |

