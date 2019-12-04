---
title: Tildele brugere til sikkerhedsroller
description: For at få adgang til Finance and Operations-apps skal brugerne være tildelt sikkerhedsroller.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2019
ms.locfileid: "2807990"
---
# <a name="assign-users-to-security-roles"></a>Tildele brugere til sikkerhedsroller

[!include [task guide banner](../../includes/task-guide-banner.md)]

Brugerne skal være tildelt sikkerhedsroller for at kunne bruge andet end almindelige egenskaber. Denne procedure forklarer, hvordan systemadministratorer automatisk kan tildele roller til brugerne ud fra forretningsdataene. 

## <a name="automatically-assign-users-to-roles"></a>Tildele brugere automatisk til roller
1. Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.
2. Vælg 'Regnskabsansvarlig' i træet. Vælg den rolle, du vil konfigurere reglen for. Vælg Regnskabsansvarlig i dette eksempel. 
3. Klik på **Tilføj regel** for at åbne dialogboksen.
4. Find og vælg den ønskede post på listen **Vælg en forespørgsel**. Vælg den forespørgsel, du vil bruge for denne regel.  
5. Klik på linket i den valgte række på listen **Navn på medlemskabsregel**.
6. Klik på **Rediger forespørgsel**. Rediger forespørgslen efter behov.  
7. Klik på **OK**.
8. Klik på **Kør automatisk rolletildeling**.
9. Gå til **Navigationsrude > Moduler > Systemadministration > Brugere > Brugere** (helst i en separat fane i browseren).
10. Gennemse de roller, der er tildelt de forskellige brugere, for at bekræfte, at forespørgslen om rolletildeling er korrekt. Tilpas, og kør den igen, hvis det er nødvendigt.

## <a name="exclude-users-from-automatic-role-assignment"></a>Udelukke brugere fra automatisk rolletildeling
1. Luk siden.
2. Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.
3. Vælg 'Regnskabsansvarlig' i træet. Vælg en rolle. Vælg Regnskabsansvarlig for dette eksempel.  
4. Vælg **Tildel brugere roller/udeluk brugere fra roller manuelt** i menuen **Brugere, der er tildelt til rollen**.
5. Markér den valgte række på listen **Tildel en rolle til brugere, eller udeluk brugere fra rollen**. Vælg en bruger.  
6. Vælg **Udeluk fra rolle** i **Handlingsrude**.
    
    Klik på **Udeluk fra rolle** for at udelukke de valgte brugere fra rollen. Hvis du vil fjerne udelukkelser, skal du markere de brugere, hvor du vil fjerne udelukkelser, og derefter klikke på **Nulstil status**. Når du fjerner en udelukkelse ved at nulstille brugerens status, tildeles brugerens rolle igen automatisk. Brugeren bliver dog ikke tildelt eller udelukket fra rollen med det samme, når du nulstiller statussen. I stedet bliver brugeren enten tildelt eller fjernet fra rollen, næste gang reglerne for automatisk rolletildeling bliver kørt.  
