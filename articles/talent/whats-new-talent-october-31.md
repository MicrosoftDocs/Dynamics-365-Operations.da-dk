---
title: "Hvad er nyt eller ændret i Dynamics 365 for Talent Core HR (31. oktober 2018)"
description: "Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c5acd09e25ecd5fefa637342f83d0ee0f1891402
ms.contentlocale: da-dk
ms.lasthandoff: 11/01/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a>Hvad er nyt eller ændret i Dynamics 365 for Talent Core HR (31. oktober 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.2031**

Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.

## <a name="create-links-from-talent-to-finance-and-operations"></a>Oprette links fra Talent til Finance and Operations
Med denne nye navigationsfunktion kan du oprette en tilknytning fra Talent til Finance and Operations, så du kan navigere direkte på Finance and Operations-sider. Når links er konfigureret, kan du angive navn og gruppe for linket, hvor linket skal vises i Talent, og den destinationsside, der skal åbnes i Finance and Operations.

#### <a name="coming-soon"></a>Kommer snart
Feltkontekst tilføjes senere, så det bliver muligt at navigere direkte til de tilsvarende poster i Finance and Operations. Du kan f.eks. bruge **Link til felt** til at angive konteksten, så du kan gå direkte til en bestemt medarbejder eller placering i Finance and Operations.

### <a name="configure-target-systems"></a>Konfigurere destinationssystemer

I Talent kan systemadministratorer definere links, som de kan få vist via arbejdsområdet Systemadministration. En del af konfigurationen er Finance and Operations-miljøer, som du vil navigere til som linkets "mål". Det gør du ved at give målsystemet et navn og angive URL-adressen til Finance and Operations-miljøet. Her er et eksempel på en Finance and Operations URL-adresse, som du kan angive: https://devax00124aos.cloud.test.dynamics.com/. Når du har konfigureret dine målsystemer, kan du definere dine links.

### <a name="configure-links"></a>Konfigurer links

Hvert link, der oprettes, har følgende definerede oplysninger.

- Link - Navnet på det link, der kun bruges til identifikation.

- Aktivér dette link - Indstil til **Ja**, hvis linket skal kunne ses af brugere af Talent.

- Vist navn – Angiv det navn, der skal vises som et link til Finance and Operations. Disse data oversættes ikke i øjeblikket.

- Overfladelink i formular - Vælg, hvilken side linket skal vises på.

- Gruppe - Grupper er ikke påkrævet, men hvis du vil organisere dine links ved hjælp af grupper, skal du vælge en eksisterende gruppe eller oprette en ny ved hjælp af feltet **Gruppe**.

- Destinationssystem - Vælg det destinationssystem, der blev oprettet ved hjælp af indstillingen **Konfigurer destinationssystem**. Det er dette Finance and Operations-miljø, der bliver brugt, når du navigerer ved hjælp af linket.

- Brug brugerens aktuelle firma - Vælg **Ja**, hvis du vil bruge brugerens aktuelle regnskabskontekst, når du navigerer til Finance and Operations. Hvis **Nej** er markeret, kan du vælge det regnskab, der skal bruges.

- Menupunktet Mål – Angiv det menupunkt fra Finance and Operations, som linket skal bruge til navigation. De menupunkter, du direkte kan navigere til, er tilgængelige. Du kan finde det ønskede menupunkt ved at åbne Finance and Operations og åbne den side, der er målet for navigationen. Kopiér menupunktet fra URL-adressen. F.eks. hvis linket skal gå til listen over medarbejdere i Finance and Operations, skal du angive den værdi, der vises efter "&mi" i URL-adressen. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Menupunktet, der bruges til at navigere til listesiden over medarbejdere, er i dette eksempel: HcmWorkerListPage_Employees.

- Link til datakilde – Vælg datakilden, som linket refererer til. De mest almindelige kilder som f.eks. **Arbejder** og **Stilling** er tilgængelige.

- Link til felt - (kommer snart) Dette felt gør det muligt at navigere direkte fra en enkelt post i Talent til en enkelt post i Finance and Operations.

### <a name="access-to-links"></a>Adgang til links

Systemadministratorer ser de nyoprettede links på de definerede sider, også selvom der i indstillingen **Aktivér dette link** er valgt **Nej**. Dette kan bruges til test af links, før de bliver gjort synlige for andre medarbejdere. Alle andre roller kan kun se de konfigurerede links, når der i indstillingen **Aktivér dette link** er valgt **Ja**. Medarbejdere, der har adgang til de sider, hvor linkene vises, har adgang til linksene.

Brugere kan også have sikkerhedsrettigheder i Finance and Operations, der er defineret, så de giver adgang til sider i Finance and Operations. Hvis ikke, vises en sikkerhedsdialogboks, når linket bruges.


## <a name="other-changesfixes"></a>Andre ændringer/rettelser

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>Stillinger med en fremtidig startdato kan ikke tildeles til en ny medarbejder

Der er foretaget ændringer for at tillade medarbejdertildelinger til stillinger, der er dateret i fremtiden. Stillinger, der har startdatoer i fremtiden, kan vælges, og medarbejdertildelingen kan foretages, når arbejdsgangen (hvis arbejdsgangen er aktiveret) gemmes eller fuldføres.

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Ny medarbejder kan ikke tildeles eksisterende stilling

Er der foretaget ændringer, så nye medarbejdertildelinger nu kan tildeles til eksisterende stillinger.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Anciennitetsdato/kontorlokation forsvinder, når ansættelsesstartdatoen er passeret, og posten gemmes

Der er foretaget ændringer af synligheden af **Anciennitetsdato** og **Kontorlokation**, når ændringer for tidligere medarbejdere gemmes.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Det er ikke muligt at angive data for ansættelser, der er dateret ud i fremtiden, på siden Arbejder

Ansættelsesoplysninger for ansættelser, der er dateret i fremtiden, er blevet deaktiveret på hovedsiden over arbejdere. Ansættelsesdata kan angives via **Datoadministrator**-siderne. Der vil blive foretage yderligere ændringer i fremtidige versioner, så ansættelsesdata kan angives direkte under arbejdsgangen.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>Føje ValidFrom og ValidTo til HcmPersonalContactPersonEntity

DMF-objektet (Data Management Framework) HcmPersonalContactPersonEntity er blevet opdateret, så det indeholder "gyldig fra"- og "gyldig til"-datoer og muliggør integration af frynsegoder i bestemte situationer. 

## <a name="known-issue"></a>Kendt problem
- **Problem**: Når du føjer en ny vedhæftet fil til en arbejder, bliver knapperne **Ny** og **Rediger** nedtonet. 
- **Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukket. Hvis faktaboksene lukkes, når siden **Arbejder** indlæses, vil knapperne for vedhæftede filer blive aktiveret. (Dette problem vil blive løst i den næste platformsopdatering).

