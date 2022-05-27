---
title: Oprette link fra Human Resources til et andet miljø
description: Dette emne forklarer, hvordan du opretter et link fra Microsoft Dynamics 365 Human Resources til et andet Dynamics 365-miljø.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d20eef4b4861d85ead1d47ca493c3a5c2d2d85e8
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712622"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Oprette link fra Human Resources til et andet Finance-miljø

En kunde kan have to Dynamics 365-miljøer, som de arbejder i. Kunden kan f.eks. have et Dynamics 365 Human Resources-miljø i Finance-infrastrukturen og har brug for at oprette forbindelse til et andet Dynamics 365 Finance-miljø. 

Denne funktion giver mulighed for links fra en Human Resources-side til en bestemt side i et andet Finance-miljø. Når linkene er konfigureret, kan du angive, hvor linket skal være tilgængeligt i Human Resources, og den målside, der åbnes i det andet miljø.

> [!Note] 
> Du skal aktivere **Forbedringer af brugeroplevelsen med Human Resources** i **Funktionsstyring** for at få denne funktion.

## <a name="configure-target-systems"></a>Konfigurere destinationssystemer

I Human Resources kan systemadministratorer definere links, der vises på sider i **Human Resources**. En del af konfigurationen er Finance-miljøer, som du vil navigere til som linkets destination. 

Sådan konfigureres destinationssystemet:
1. Vælg **Konfigurer destinationssystem** på siden **Konfigurer links**.  
2. Angiv destinationssystemets navn og URL-adressen til Finance-miljøet. Når du har konfigureret dine destinationssystemer, kan du definere dine links.

## <a name="configure-links"></a>Konfigurer links

Hvert link, du opretter, har følgende definerede oplysninger:
 - **Link**: Navnet på linket. Bruges kun til identifikation.
 - **Aktivér dette link**: Indstil til **Ja**, hvis linket skal kunne ses af Human Resources-brugere.
 - **Vist navn**: Angiv det navn, der skal vises som et link til det sekundære miljø. 
 - **Overfladelink i formular**: Vælg, hvilken side linket skal vises på. Links kan kun ses på arbejdsområdet til **Medarbejderselvbetjening** og siderne **Job**, **Stilling**, **Arbejder** og **Strømlinet arbejder**.
 - **Gruppe**: Du kan organisere dine links ved hjælp af grupper. Vælg en eksisterende gruppe, eller opret en ny i kolonnen **Gruppe**.
 - **Destinationssystem**: Vælg det destinationssystem, der blev oprettet ved hjælp af indstillingen **Konfigurer destinationssystem**. Det bliver det sekundære miljø, der bliver brugt, når du navigerer ved hjælp af linket.
 - **Brug brugerens aktuelle firma**: Vælg **Ja**, hvis du vil bruge brugerens aktuelle firma, når du navigerer til Finance. Vælg **Nej** for at vælge det firma, der skal bruges.
 - Menupunktet **Destination**: Angiv det menupunkt fra Finance-miljøet, som linket skal bruge til navigation. De menupunkter, du direkte kan navigere til, er tilgængelige. 

   Sådan finder du det påkrævede menupunkt:
   1. Gå til Finance-miljøet, og åbn den side, der er destinationen for navigationen. 
   2. Kopiér menupunktet fra URL-adressen. F.eks. hvis linket skal gå til listen over medarbejdere i Finance and Operations, skal du angive den værdi, der vises efter "&mi" i URL-adressen. 
   3. Menupunktet, der bruges til at navigere til listesiden over medarbejdere, er i dette eksempel: HcmWorkerListPage_Employees.

 - **Link til datakilde**: Vælg datakilden, som linket refererer til. De mest almindelige kilder som f.eks. **Arbejder** og **Stilling** er tilgængelige.

### <a name="access-to-links"></a>Adgang til links

Systemadministratorer ser de nyoprettede links på de definerede sider, også selvom der i indstillingen **Aktivér dette link** er valgt **Nej**. Dette kan bruges til test af links, før de bliver gjort synlige for andre medarbejdere. Alle andre roller kan kun se de konfigurerede links, når der i indstillingen **Aktivér dette link** er valgt **Ja**. Medarbejdere, der har adgang til de sider, hvor linkene vises, har adgang til linksene.

Brugere skal også have sikkerhedsrettigheder i det sekundære miljø defineret for at få adgang til siderne i det pågældende miljø. Hvis ikke, vises en sikkerhedsdialogboks, når linket bruges.

