--- 
title: Vedligeholde oplysninger om skade og sygdom for medarbejder
description: "Det anbefales at fuldføre opgaveguiden \"Konfiguration af skade og sygdom\" først, fordi nogle af konfigurationsoplysningerne bruges her."
author: ShielaSogge
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: e22ce4950b065e7e80bace3fcd5c0f7d6627d124
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-employee-injury-and-illness-information"></a>Vedligeholde oplysninger om skade og sygdom for medarbejder

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Det anbefales at fuldføre opgaveguiden "Konfiguration af skade og sygdom" først, fordi nogle af konfigurationsoplysningerne bruges her. 



Denne opgaveregistrering omfatter de grundlæggende trin til oprettelse af en skades- eller sygdomssag. Ud over at spore oplysninger om skaden eller sygdommen, er der en sagsstatus, som spores også.  Sagen har som standard med statussen "åben".  Statusserne kan administreres fra menupunktet "Sagsstatus" på programlinjen øverst i formularen.

1. Gå til personale > Arbejdere > Skade og sygdom > Skades- eller sygdomshændelser.
2. Klik på Ny.
3. Indtast en værdi i feltet Sagsbeskrivelse.
    * Eksempel: Håndledsskade  
4. Indtast eller vælg en værdi i feltet Arbejder.
    * Eksempel: Ahmed Barnett  
5. Angiv en dato og et klokkeslæt i feltet Dato og klokkeslæt for hændelsen.
    * Eksempel: 20-01-2016 kl. 10:00  
6. Indtast eller vælg en værdi i feltet Skades- eller sygdomstype.
    * Eksempel: Brud  
7. Indtast eller vælg en værdi i feltet Legemsdel.
    * Eksempel: Håndled  
8. Indtast eller vælg en værdi i feltet Udfaldstype.
    * Eksempel: Terapi  
9. Angiv en dato og et klokkeslæt i feltet Dato og klokkeslæt rapporteret.
    * Datoen og klokkeslættet, der rapporteres, skal være senere end datoen og klokkeslættet for hændelsen.  
10. Angiv eller vælg en værdi i feltet Person, der har rapporteret sagen.
    * Dette kan være medarbejderen eller et andet vidne til hændelsen.  Eksempel: Ahmed Barnett  
11. Udvid afsnittet Hændelse.
12. I feltet Det sted, hændelsen fandt sted, skal du skrive en værdi.
    * Eksempel: lagersted  
13. Vælg Ja i feltet På arbejdssted.
    * Hvis hændelsen fandt sted på et arbejdssted, skal du vælge ja.  
14. Angiv en dato og et klokkeslæt i feltet Dato og klokkeslæt for arbejdets begyndelse.
    * Angiv dato og klokkeslæt, hvor den berørte person begyndte at arbejde, før hændelsen forekom.  
15. Skriv en værdi i feltet Medarbejderjob eller -opgave.
    * Indtast det job eller den opgave, medarbejderen udførte, da hændelsen forekom.  Eksempel: Indlæsning af bokse  
16. Skriv en værdi i feltet Årsag til hændelsen.
    * Angiv årsagen til hændelsen.  Eksempel: Gled på vådt gulv  
17. Indtast eller vælg en værdi i feltet Alvorlighedsniveau.
18. Skriv en værdi i feltet Handling, der skal udføres.
    * Eksempel: Fjern spildte væsker straks  
19. Skriv et tal i feltet Forventede dage væk fra arbejdet.
    * Angiv det antal dage, personen forventes at være fraværende.  Når han eller hun vender tilbage til sit arbejde, kan du opdatere feltet "Dage væk fra arbejdet" med det faktiske antal fraværsdage.  
20. Udvid sektionen Omkostninger i forbindelse med skade eller sygdom.
21. Klik på Tilføj.
22. Indtast en dato i feltet Dato.
23. Indtast eller vælg en værdi i feltet Omkostningstype.
    * Eksempel: Terapi. Du kan også indtaste et beløb og vedhæfte understøttende dokumentation som fakturaer eller lægens bemærkninger til omkostningen.  
24. Klik på Tilføj.
25. Indtast en dato i feltet Dato.
26. Indtast eller vælg en værdi i feltet Omkostningstype.
    * Eksempel: Læge  
27. Udvid sektionen Behandlinger af skade eller sygdom.
28. Klik på Tilføj.
29. Angiv en dato og et klokkeslæt i feltet Behandlingsdato.
30. Indtast eller vælg en værdi i feltet Behandlingstype.
    * Eksempel: Skinne  
31. Du kan eventuelt indstille afsnittet Hospitalsbesøg på skadestue til Ja.
32. Indtast en værdi i feltet Kommentarer til behandling.
    * Eksempel: Skinne i 2 uger  
33. Skriv en værdi i feltet Lægens navn.
    * Eksempel: Dr. Westermann  
34. Indtast en værdi i feltet Behandlingsfacilitet og -sted.
    * Eksempel: Elm St. Emergency  
35. Indtast en værdi i feltet Oplysninger om behandling.
    * Eksempel: Røntgen bekræfter brud, brug skinne  
36. Klik på Gem.
    * Sagsstatus kan altid opdateres.  Indstil sagen til Igangværende, hvis behandlingen af en skade eller sygdom er i gang.  Når du lukker hændelsen, kan du kun tilføje eller fjerne omkostninger, behandlinger eller registreringer, der er knyttet til hændelsen.  Hvis du vil ændre andre oplysninger, skal du genåbne sagen.  


