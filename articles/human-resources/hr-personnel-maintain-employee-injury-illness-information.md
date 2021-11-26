---
title: Vedligeholde oplysninger om skade og sygdom for medarbejder
description: Denne opgave beskriver, hvordan du opretter et skades- eller sygdomstilfælde.
author: twheeloc
ms.date: 11/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c351919616c8ab5cf15d14c6cc79a5097e248fc
ms.sourcegitcommit: 7e0e2a266d9a9473df72e207554d9bd150e17ce3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2021
ms.locfileid: "7771237"
---
# <a name="maintain-employee-injury-and-illness-information"></a>Vedligeholde oplysninger om skade og sygdom for medarbejder

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Det anbefales at fuldføre opgaveguiden "Konfiguration af skade og sygdom" først, fordi nogle af konfigurationsoplysningerne bruges her. 



Denne opgaveregistrering beskriver de grundlæggende trin til oprettelse af en skades- eller sygdomssag. Foruden detaljer om skaden eller sygdommen spores en sagsstatus. Sager har som standard statussen **Åben**. Statusserne kan administreres fra menupunktet **Sagsstatus** øverst på siden.

1. Gå til **Human Resources \> Arbejdere \> Skade og sygdom \> Skades- eller sygdomshændelser**.
2. Vælg **Ny**.
3. Indtast en værdi (f.eks. **Håndledsskade**) i feltet **Sagsbeskrivelse**.
4. Indtast eller vælge en værdi i feltet **Arbejder** (f.eks. **Ana Bowman**).
5. I feltet **Dato og klokkeslæt for hændelsen** skal du angive en dato og et klokkeslæt (f.eks. 20. januar 2016 kl. 10:00).
6. Indtast eller vælg en værdi i feltet **Skades- eller sygdomstype** (f.eks. **Brud**).
7. Indtast eller vælg en værdi (f.eks. **Håndled**) i feltet **Legemsdel**.
8. Indtast eller vælg en værdi (f.eks. **Terapi**) i feltet **Udfaldstype**.
9. Angiv en dato og et klokkeslæt i feltet **Dato og klokkeslæt rapporteret**.

    Datoen og klokkeslættet, der rapporteres, skal være senere end datoen og klokkeslættet for hændelsen.

10. Angiv eller vælg en værdi i feltet **Person, der har rapporteret sagen** (f.eks. **Ana Bowman**).

    Personen kan være medarbejderen eller et andet vidne til hændelsen.

11. I sektionen **Hændelse** skal du i feltet **Hvor hændelsen forekom** angive en værdi (f.eks. **Lagersted**).
12. Vælg **Ja** i feltet **På arbejdssted**, hvis hændelsen forekom på arbejdsstedet.
13. I feltet **Dato og klokkeslæt for arbejdets begyndelse** skal du angive den dato og det klokkeslæt, hvor den berørte person begyndte at arbejde, før hændelsen forekom.
14. I feltet **Medarbejderjob eller -opgave** skal du angive det job eller den opgave, medarbejderen udførte, da hændelsen forekom (f.eks. **Læsning af kasser**). 
15. I feltet **Årsag til hændelse** skal du angive årsagen til hændelsen (f.eks. **Gled på vådt gulv**).
16. Indtast eller vælg en værdi i feltet **Alvorlighedsniveau**.
17. I feltet **Handling, der skal udføres** skal du angive en værdi (f.eks. **Fjern spildte væsker straks**).
18. Angiv det antal dage, personen forventes at være væk fra arbejdet, i feltet **Forventede dage væk fra arbejdet**.

    Når personen vender tilbage til sit arbejde, skal du opdatere feltet **Dage væk fra arbejdet** med det faktiske antal fraværsdage.

19. Vælg **Tilføj** i sektionen **Omkostninger i forbindelse med skade eller sygdom**.
20. Indtast en dato i feltet **Dato**.
21. Indtast eller vælg en værdi (f.eks. **Terapi**) i feltet **Omkostningstype**.

    Du kan også indtaste et beløb og vedhæfte understøttende dokumentation for omkostningen (f.eks. faktura eller lægeerklæring).

22. Vælg **Tilføj**.
23. Indtast en dato i feltet **Dato**.
24. Indtast eller vælg en værdi (f.eks. **Læge**) i feltet **Omkostningstype**.
25. Vælg **Tilføj** i sektionen **Behandlinger af skade eller sygdom**.
26. Angiv en dato og et klokkeslæt i feltet **Behandlingsdato**.
27. Indtast eller vælg en værdi (f.eks. **Skinne**) i feltet **Behandlingstype**.
28. Valgfrit: Angiv afsnittet **Hospitalsbesøg på skadestue** til **Ja**.
29. Indtast en værdi (f.eks. **Skinne i 2 uger**) i feltet **Kommentarer til behandling**.
30. Angiv en værdi i feltet **Lægens navn** (f.eks. **Dr. Westermann**).
31. I feltet **Behandlingsfacilitet og -sted** skal du angive en værdi (f.eks. **Elm St. Emergency**).
32. I feltet **Behandlingsdetaljer** skal du angive en værdi (f.eks. **Røntgen bekræfter brud, brug skinne**).
33. Vælg **Gem**.

Sagsstatus kan altid opdateres. Indstil sagen til **Igangværende**, hvis behandlingen af en skade eller sygdom er i gang. Når du har lukket hændelsen, kan du kun tilføje eller fjerne omkostninger, behandlinger eller registreringer, der er knyttet til hændelsen. Hvis du vil ændre andre oplysninger, skal du genåbne sagen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
