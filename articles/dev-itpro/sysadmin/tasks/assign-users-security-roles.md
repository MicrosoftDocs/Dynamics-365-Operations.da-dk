--- 
title: Tildele brugere til sikkerhedsroller
description: "For at få adgang til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition skal brugerne være tildelt sikkerhedsroller."
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 551048af26f46d334c562d1968963aed262a5e03
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="assign-users-to-security-roles"></a>Tildele brugere til sikkerhedsroller

[!include [task guide banner](../../includes/task-guide-banner.md)]

For at få adgang til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition skal brugerne være tildelt sikkerhedsroller. Denne procedure forklarer, hvordan systemadministratorer kan tildele roller automatisk til brugerne ud fra forretningsdataene. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="automatically-assign-users-to-roles"></a>Tildele brugere automatisk til roller
1. Gå til Systemadministration > Sikkerhed > Tildel brugere roller.
2. Vælg 'Regnskabsansvarlig' i træet.
    * Vælg den rolle, du vil konfigurere reglen for. Vælg Regnskabsansvarlig i dette eksempel.  
3. Klik på Tilføj regel for at åbne dialogboksen.
4. Find og vælg den ønskede post på listen.
    * Vælg den forespørgsel, du vil bruge for denne regel.  
5. Klik op linket i den valgte række på listen.
6. Klik på Rediger forespørgsel.
    * Rediger forespørgslen efter behov.  
7. Klik på OK.

## <a name="exclude-users-from-automatic-role-assignment"></a>Udelukke brugere fra automatisk rolletildeling
1. Luk siden.
2. Gå til Systemadministration > Sikkerhed > Tildel brugere roller.
3. Vælg 'Regnskabsansvarlig' i træet.
    * Vælg en rolle. Vælg Regnskabsansvarlig for dette eksempel.  
4. Klik på Tildel brugere roller/udeluk brugere fra roller manuelt.
5. Markér den valgte række på listen.
    * Vælg en bruger.  
6. Klik på Udeluk fra rolle.
    * Klik på Udeluk fra rolle for at udelukke de valgte brugere fra rollen. Hvis du vil fjerne udelukkelser, skal du markere de brugere, hvor du vil fjerne udelukkelser, og derefter klikke på Nulstil status. Når du fjerner en udelukkelse ved at nulstille brugerens status, tildeles brugerens rolle igen automatisk. Brugeren bliver dog ikke tildelt eller udelukket fra rollen med det samme, når du nulstiller statussen. I stedet bliver brugeren enten tildelt eller fjernet fra rollen, næste gang reglerne for automatisk rolletildeling bliver kørt.  


