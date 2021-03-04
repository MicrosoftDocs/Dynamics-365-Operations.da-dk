---
title: Strømlinet medarbejderangivelse og navigation
description: Dataindtastning for arbejdere i Dynamics 365 Talent er blevet forbedret for at tillade hurtig indtastning for alle medarbejdere, tidligere, aktive eller fremtidige. En forenklet/konsolideret navigationsmodel er blevet opdateret, så den hurtigt kan finde relaterede oplysninger og se og foretage de nødvendige opdateringer.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: b73b420c2eb75077814fbfeb6cd17404c7efc11e
ms.sourcegitcommit: 436731d8b3889bebfe6f17922b0a31b1994f6796
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/26/2020
ms.locfileid: "4460747"
---
# <a name="streamlined-employee-entry-and-navigation"></a>Strømlinet medarbejderangivelse og navigation

Dynamics 365 Talent giver mulighed for effektiv indtastning af medarbejder- og ansættelsesdata. Du kan hurtigt opdatere oplysninger om arbejdshistorik for tidligere, aktive og fremtidige medarbejdere og kontrahenter.

Du kan også få en forenklet navigationsoplevelse for hurtigt at finde relaterede oplysninger og foretage de nødvendige ændringer. Denne funktionalitet er nu tilgængelig i alle miljøer. Hvis du vil slå denne funktion til, skal du gå til **Systemadministration > Funktionsstyring > Ny > Strømlinet medarbejderpost > Aktiver**. Dette aktiverer disse ændringer for alle brugere. Du kan deaktivere denne indstilling på et hvilket som helst tidspunkt.

## <a name="view-options"></a>Indstillinger for visning

Du kan bruge **Visningsindstillinger** i arbejderformen til at vælge en kombination af medarbejdere og kontrahenter på en enkelt liste. Disse indstillinger giver dig mulighed for at få vist arbejdere på tværs af juridiske enheder eller for den juridiske enhed, du i øjeblikket er logget på. Du kan også se aktive, afventende og fratrådte arbejdere, og du kan begrænse resultaterne baseret på arbejdertypen (medarbejder eller kontrahent). Hvis avanceret sikkerhed er aktiveret, kan du kun se disse medarbejdere og kontrahenter i de juridiske enheder, du har adgang til.

Kolonner i listevisningen ændres ud fra dine valg. Når der f.eks. vises fratrådte medarbejdere, vises fratrædelsesdato og årsagskoder som ekstra kolonner på listen. 

[![Indstillinger for visning](./media/Worker-view-option.png)](./media/worker-view-option.png)

## <a name="navigation-and-banner"></a>Navigation og banner

Et banner viser vigtige oplysninger for hver arbejder. Banneret for de aktive arbejdere viser følgende felter:

- **Stilling**
- **Afdeling**
- **Stillingstype**
- **Arbejdertype**
- **Leder**
- **Juridisk enhed**

Banneret for de fratrådte arbejdere viser følgende felter:

- **Fratrædelsesdato**
- **Årsag**

Banneret for de ventende medarbejdere viser følgende felter:

- **Stilling**
- **Afdeling**
- **Stillingstype**
- **Leder**
- **Startdato**
- **Juridisk enhed**

Handlingsruden på arbejdersiden er blevet omorganiseret, så den indeholder færre muligheder. Oplysningerne er nu organiseret i følgende kategorier: 

- Arbejde
- Person
- Forlad
- Kompensation
- Personalegoder
- Compliance

Desuden giver den nye fane **Links** på hovedsiden for arbejdere et centralt sted, hvor de kan få adgang til alle relaterede oplysninger for en arbejder.

På grund af disse ændringer kan oplysningerne vises på et andet sted, end du er vant til. Lønoplysninger, der tidligere blev vist i arbejderformen, vises f.eks. nu i handlingsruden under **Kompensation > Løn**, og fanen **Personlige oplysninger** indeholder nu knappen **Flere oplysninger** for at skjule felter, der ikke bruges så ofte.

[![Banner](./media/Banner.png)](./media/Banner.png)

## <a name="work-history"></a>Arbejdshistorik

Fanen **Arbejdshistorik** viser arbejdshistorik på tværs af alle juridiske enheder, og den er tilgængelig for fratrådte, aktive og afventende medarbejdere og kontrahenter. Du kan nu få vist al arbejdshistorik på én gang for de juridiske enheder, du har adgang til. Du kan desuden redigere oplysninger for hver enkelt post i arbejdshistorikken uden at ændre datakonteksten. Du kan opdatere alle oplysninger direkte på siden. 

[![Arbejdshistorik](./media/Worker-work-history.png)](./media/Worker-work-history.png)

## <a name="position-history"></a>Stillingshistorik

Fanen **Stillinger** på hovedsiden for arbejdere indeholder en komplet visning af alle stillinger i organisationen, herunder tidligere, nuværende og eventuelle fremtidige tildelinger. Du kan stadig gå direkte til arbejderens stillingshistorik i handlingsruden.

[![Stillinger](./media/Worker-position-history.png)](./media/Worker-position-history.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]