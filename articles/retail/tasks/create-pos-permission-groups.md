---
title: " Oprette POS-rettighedsgrupper"
description: Denne procedure viser, hvordan du opretter en POS-rettighedsgruppe.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b30c9a1d7fe4598695423ba700ebc88a794a49c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "354454"
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

