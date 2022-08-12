---
title: Tildele brugere til sikkerhedsroller
description: For at få adgang til programmer til finans og drift skal brugerne være tildelt sikkerhedsroller.
author: Peakerbl
ms.date: 02/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5e69a79f123daff3f85d0100647615ad818288e
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103862"
---
# <a name="manage-users-and-security-roles"></a>Administrere brugere og sikkerhedsroller

[!include [banner](../../includes/banner.md)]

Brugerne skal være tildelt sikkerhedsroller for at kunne bruge andet end almindelige egenskaber i programmer til finans og drift. Du kan tildele brugere roller automatisk baseret på regler og forretningsdata, udelukke brugere fra automatisk rolletildeling eller føje brugere til roller manuelt.

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
Denne procedure forklarer, hvordan du udelukker brugere fra automatisk rolletildeling.

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

## <a name="manually-remove-users-from-roles"></a>Manuelt fjerne brugere fra roller
Brugere, som manuelt tildeles sikkerhedsroller, skal også fjernes manuelt af administratoren. Disse brugere fjernes ikke fra rollerne efter regler for automatisk rolletildeling.

1. Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.
2. Hvis du vil fjerne én bruger, skal du benytte følgende fremgangsmåde:
   1. Vælg en rolle i træet. 
   2. Vælg den bruger, der skal fjernes, i området **Brugere, der er tildelt til rollen**.
   3. Vælg **Fjern**, så brugeren fjernes fra rollen.
3. Hvis du vil fjerne flere brugere, skal du benytte følgende fremgangsmåde:
   1. Vælg en rolle i træet. 
   2. Vælg **Tildel brugere roller/udeluk brugere fra roller manuelt** i området **Brugere, der er tildelt til rollen**.
   3. På siden **Tildel brugere til roller, eller udeluk brugere fra roller** har de brugere, der ikke er tildelt til rollen, kolonnen **Tildelingstilstand** angivet til **Ingen**. Vælg de brugere, der skal udelukkes fra rollen.
   4. Vælg **Udeluk fra rolle** i **Handlingsrude**. Kolonnen **Tildelingstilstand** opdateres nu til **Manuel**, og brugerne er nu udelukket fra rollen.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

