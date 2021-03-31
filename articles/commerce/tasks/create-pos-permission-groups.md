---
title: Oprette POS-rettighedsgrupper
description: Dette emner beskriver, hvordan du opretter en POS-rettighedsgruppe.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2439d1912b3ca013f4a524f3354923d2a3f76ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221275"
---
# <a name="create-pos-permission-groups"></a>Oprette POS-rettighedsgrupper

[!include [banner](../includes/banner.md)]

Dette emner beskriver, hvordan du opretter en POS-rettighedsgruppe. Det demodatafirma, der bruges til at oprette denne opgave, er USRT. Denne opgave er tiltænkt rollen Commerce-driftschef.

1. Gå i navigationsruden til **Moduler > Retail og Commerce > Medarbejdere > Rettighedsgrupper**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Id for POS-rettighedsgruppe**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Vælg **Ja** i feltet **Vis tidsursangivelser**. Du kan nu aktivere eller deaktivere forskellige rettigheder for din POS-rettighedsgruppe. For nogle rettigheder kan du angive en værdi, der skal bruges til at vurdere, om POS-brugeren kan udføre handlingen. Denne opgaveguide muliggør nogle få rettigheder, der kan gives til en kasseassistent.  
6. Vælg **Ja** i feltet **Tillad oprettelse af ordre**.
7. Vælg **Ja** i feltet **Tillad redigering af ordre**.
8. Vælg **Ja** i feltet **Tillad hentning af ordre**.
9. Vælg **Ja** i feltet **Tillad ændring af adgangskode**.
10. Vælg **Ja** i feltet **Tillad lukning uden kontrol**.
11. Vælg **Gem**. Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til handelskanalerne. 
12. Gå i navigationsruden til **Moduler > Human resources > Job > Job**.
13. Dernæst vil vi tildele POS-rettighedsgruppen til et Job. Find og vælg den ønskede post på listen.
14. Vælg **Rediger**.
15. Udvid sektionen **Jobklassificering**.
16. Indtast eller vælg en værdi i feltet POS-rettighedsgruppe. Alle arbejdere i positioner for dette job vil bruge indstillinger for denne POS-rettighedsgruppe, medmindre arbejdernes POS-rettigheder er blevet tilsidesat på deres positionsniveau.  
17. Vælg **Gem**. Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til kanalerne.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]