---
title: Tildele brugere til sikkerhedsroller
description: Brugerne skal være tildelt sikkerhedsroller for at få adgang til Finance and Operations.
author: Peakerbl
manager: AnnBe
ms.date: 05/06/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f78c24e8c2ffe5418ce119e19b7c0193f01f64b8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679858"
---
# <a name="assign-users-to-security-roles"></a>Tildele brugere til sikkerhedsroller

[!include [banner](../../includes/banner.md)]

Brugerne skal være tildelt sikkerhedsroller for at kunne bruge andet end almindelige egenskaber i Finance and Operations-apps. Du kan tildele brugere roller automatisk baseret på regler og forretningsdata, udelukke brugere fra automatisk rolletildeling eller føje brugere til roller manuelt.

## <a name="automatically-assign-users-to-roles"></a>Tildele brugere automatisk til roller
Denne procedure forklarer, hvordan systemadministratorer automatisk kan tildele roller til brugerne ud fra forretningsdataene. 
1. Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.
2. Vælg 'Regnskabsansvarlig' i træet. Vælg den rolle, du vil konfigurere reglen for. Vælg Regnskabsansvarlig i dette eksempel. 
3. Vælg **Tilføj regel** for at åbne dialogmenuen.
4. Find og vælg den ønskede post på listen **Vælg en forespørgsel**. Vælg den forespørgsel, du vil bruge for denne regel.  
5. Klik på linket i den valgte række på listen **Navn på medlemskabsregel**.
6. Vælg **Rediger forespørgsel**. Rediger forespørgslen efter behov.  
7. Vælg **OK**.
8. Vælg **Kør automatisk rolletildeling**.
9. Gå til **Navigationsrude > Moduler > Systemadministration > Brugere > Brugere** (helst i en separat fane i browseren).
10. Gennemse de roller, der er tildelt de forskellige brugere, for at bekræfte, at forespørgslen om rolletildeling er korrekt. Tilpas, og kør den igen, hvis det er nødvendigt.

## <a name="exclude-users-from-automatic-role-assignment"></a>Udelukke brugere fra automatisk rolletildeling
1. Luk siden.
2. Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.
3. Vælg 'Regnskabsansvarlig' i træet. Vælg en rolle. Vælg Regnskabsansvarlig for dette eksempel.  
4. Vælg **Tildel brugere roller/udeluk brugere fra roller manuelt** i menuen **Brugere, der er tildelt til rollen**.
5. Markér den valgte række på listen **Tildel en rolle til brugere, eller udeluk brugere fra rollen**. Vælg en bruger.  
6. Vælg **Udeluk fra rolle** i **Handlingsrude**.
7. Vælg **Udeluk fra rolle** for at udelukke de valgte brugere fra rollen. Hvis du vil fjerne udelukkelser, skal du markere de brugere, hvor du vil fjerne udelukkelser, og derefter klikke på **Nulstil status**. Når du fjerner en udelukkelse ved at nulstille brugerens status, tildeles brugerens rolle automatisk. Brugeren bliver dog ikke tildelt eller udelukket fra rollen med det samme, når du nulstiller statussen. I stedet bliver brugeren enten tildelt eller fjernet fra rollen, næste gang reglerne for automatisk rolletildeling bliver kørt.  

## <a name="manually-assign-users-to-roles"></a>Tildele brugere til roller manuelt
Brugere, som manuelt tildeles sikkerhedsroller, skal også fjernes manuelt af administratoren. Disse brugere fjernes ikke fra rollerne efter regler for automatisk rolletildeling.

1. Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.
2. Vælg en rolle i træet, og vælg **Tildel brugere roller/udeluk brugere fra roller manuelt** i menuen **Brugere, der er tildelt til rollen**.
4. I **Tildel brugere til roller, eller udeluk brugere fra roller** vises de brugere, der ikke er tildelt til rollen, med **Tildelingstilstand** angivet til **Ingen**. Vælg en eller flere brugere, der skal have tildelt rollen.
5. Vælg **Tildel til rolle** i **handlingsruden**. **Tildelingstilstand** opdateres til **Manuel**, og brugerne har nu fået tildelt en ny rolle.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]