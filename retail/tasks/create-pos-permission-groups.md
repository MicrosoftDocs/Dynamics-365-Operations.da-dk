--- 
title: " Oprette POS-rettighedsgrupper"
description: Denne procedure viser, hvordan du opretter en POS-rettighedsgruppe.
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b0c930e3722d1d0b1fff8efad7a785a153436b6d
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="create-pos-permission-groups"></a> Oprette POS-rettighedsgrupper

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en POS-rettighedsgruppe. Det demodatafirma, der bruges til at oprette denne opgave, er USRT. Denne opgave er tiltænkt rollen Retail driftschef.

1. Gå til Rettighedsgrupper.
2. Klik på Ny.
3. Skriv en værdi i feltet Id for POS-rettighedsgruppe.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg Ja i feltet Vis tidsursangivelser.
    * Du kan nu aktivere eller deaktivere forskellige rettigheder for din POS-rettighedsgruppe. For nogle rettigheder kan du angive en værdi, der skal bruges til at vurdere, om POS-brugeren kan udføre handlingen.  Denne opgaveguide muliggør nogle få rettigheder, der kan gives til en kasseassistent.  
6. Vælg Ja i feltet Tillad oprettelse af ordre.
7. Vælg Ja i feltet Tillad redigering af ordre.
8. Vælg Ja i feltet Tillad hentning af ordre.
9. Vælg Ja i feltet Tillad ændring af adgangskode.
10. Vælg Ja i feltet Tillad lukning uden kontrol.
11. Klik på Gem.
    * Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til detailkanaler.  
12. Luk siden.
13. Gå til job.
    * Dernæst vil vi tildele POS-rettighedsgruppen til et Job.  
14. Find og vælg den ønskede post på listen.
15. Klik op linket i den valgte række på listen.
16. Klik på Rediger.
17. Udvid sektionen Jobklassificering.
18. Indtast eller vælg en værdi i feltet POS-rettighedsgruppe.
    * Alle arbejdere i positioner for dette job vil bruge indstillinger for denne POS-rettighedsgruppe, medmindre arbejdernes POS-rettigheder er blevet tilsidesat på deres positionsniveau.  
19. Klik på Gem.
    * Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til detailkanaler.  


