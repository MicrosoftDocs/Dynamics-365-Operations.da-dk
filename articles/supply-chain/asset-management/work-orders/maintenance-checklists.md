---
title: Vedligeholdelsestjeklister
description: Dette emne beskriver vedligeholdelsestjeklister i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875573"
---
# <a name="maintenance-checklists"></a>Vedligeholdelsestjeklister


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Vedligeholdelsestjeklister defineres for vedligeholdelsesjobtyper og bruges, når du arbejder på en arbejdsordre. Udfyldelse af vedligeholdelsestjeklister er en del af færdiggørelsen af en arbejdsordre. Se afsnittet [Kategorier af vedligeholdelsesjobtyper og vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper, vedligeholdelsesjobfag og vedligeholdelsestjeklister](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) for at få flere oplysninger om, hvordan du konfigurerer vedligeholdelsestjeklister på vedligeholdelsesjobtyper i formen **Standarder for vedligeholdelsesjobtype**.

Når du arbejder med vedligeholdelsestjeklister på en arbejdsordre, kan du udfylde de foruddefinerede vedligeholdelsestjeklister, der vedrører vedligeholdelsesjobtyper. Du kan også tilføje yderligere vedligeholdelsestjeklister.

## <a name="fill-out-a-maintenance-checklist"></a>Udfylde en vedligeholdelsestjekliste

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg arbejdsordren, og klik på **Vedligeholdelsestjekliste**.

3. I **Vedligeholdelsestjeklisten for arbejdsordrejob** kan du se vedligeholdelsestjeklister for alle arbejdsordrejob. Hvis arbejdsordrejob har forskellige vedligeholdelsesjobtyper, kan vedligeholdelsestjeklisterne være forskellige på hvert arbejdsordrejob. Vælg et arbejdsordrejob for at arbejde med den relaterede vedligeholdelsestjekliste. Der vises oplysninger om en valgt linje i vedligeholdelsestjeklisten i oversigtspanelet **Linjedetaljer**.

4. Udfyld alle linjer i vedligeholdelsestjeklisten én ad gangen i den rækkefølge, de vises. En vedligeholdelsestjeklistelinje af typen "Overskrift" bruges som en overskrift til at gruppere vedligeholdelsestjeklistens linjer nedenfor. Du behøver ikke udfylde en overskrift, men for alle linjetyper på vedligeholdelsestjeklisten er det muligt at føje en **Note** til overskriften.

5. Hvis instruktioner er relateret til en vedligeholdelsestjeklistelinje, er afkrydsningsfeltet **Instruktioner** markeret. Læs instruktioner for den valgte linje på vedligeholdelsestjeklisten i oversigtspanelet **Linjedetaljer** sektionen **Instruktioner**.

6. De oplysninger, der kræves for at udfylde en linje på en vedligeholdelsestjekliste, kan variere afhængigt af den relaterede type af vedligeholdelsestjekliste. Du udfylder en linje på en vedligeholdelsestjekliste ved at udfylde felterne i oversigtspanelet **Linjedetaljer**. På en linje af typen "Tekst" tilføjer du f.eks. en **Note**, der forklarer, hvad der er resultatet af den pågældende tjeklistelinje. På en linje af typen "Måling" tilføjer du den **Tællerværdi**, du har aflæst på udstyret, og du kan også tilføje en **Note**, hvis det er nødvendigt.

- Når du har fuldført en linje på vedligeholdelsestjeklisten, skal du markere afkrydsningsfeltet **Kontrolleret** på linjen for at markere den som fuldført. Hvis du vil kassere en vedligeholdelsestjeklistelinje, fordi den ikke er relevant for arbejdsordrejobbet, skal du markere afkrydsningsfeltet **(I/T)** på linjen. Hvis en linje på vedligeholdelsestjeklisten er **Obligatorisk**, skal du markere den som enten "Kontrolleret" eller "I/T".  
- Du kan kun opdatere registreringer på vedligeholdelsestjeklister, hvis arbejdsordren har [Aktiv](../setup-for-work-orders/work-order-lifecycle-states.md) livscyklustilstand.  


## <a name="add-a-maintenance-checklist-line"></a>Tilføje en linje på en vedligeholdelsestjekliste

Vedligeholdelsestjeklister oprettes ud fra definitionen af vedligeholdelsesjobtypens standard og overføres til et arbejdsordrejob. Hvis det er nødvendigt, kan du tilføje linjer på vedligeholdelsestjeklister for et arbejdsordrejob. Manuelt tilføjede vedligeholdelsestjeklistelinjer får referencen "Manuel".

1. I **Vedligeholdelsestjeklisten for arbejdsordrejob** skal du vælge det arbejdsordrejob, hvor du vil tilføje en vedligeholdelsestjekliste.

2. I oversigtspanelet **Vedligeholdelsestjeklistelinjer** skal du vælge en linje for vedligeholdelsestjeklisten og trykke på pil ned-knappen på tastaturet, hvis du vil indsætte en ny linje efter den valgte linje på vedligeholdelsestjeklisten. Det næste nummer i serien indsættes automatisk i feltet **Linjenummer**. Du kan også vælge en vedligeholdelsestjeklistelinje og klikke på knappen **Tilføj linje**, hvis du vil indsætte en ny linje over den valgte vedligeholdelsestjeklistelinje.

3. Angiv et navn til vedligeholdelsestjeklistelinjen i feltet **Navn**.

4. Angiv en type for vedligeholdelsestjeklistelinjen i feltet **Type**. For hver vedligeholdelsestjeklistetype vises de relaterede felter i oversigtspanelet **Linjedetaljer**.  
  a. "Tekst" bruges til at tilføje en vedligeholdelsestjeklistelinje med en tekstbeskrivelse af, hvad der skal gøres. Denne type af vedligeholdelsestjekliste kan bruges, hvis du vil have, at en arbejder skal kontrollere eller inspicere noget uden at have forventet et specifikt (målbart) resultat. Indsæt en beskrivelse af, hvad der skal gøres, i **Instruktioner** i oversigtspanelet **Linjedetaljer**. b. "Hoved" bruges som en overskrift til at gruppere vedligeholdelsestjeklinjer, der vises under overskriften. Dette er nyttigt, hvis du har flere vedligeholdelsestjeklistelinjer, der kan inddeles i bestemte områder. Indsæt et sigende navn i feltet **Navn**.  
  c. "Skabelon" kan ikke anvendes, når du manuelt tilføjer en vedligeholdelsestjeklistelinje på et arbejdsordrejob.  
  d. "Variabel" bruges til at definere et muligt resultat i et interval på en vedligeholdelsestjeklistelinje. Opsætningen af variabler til vedligeholdelsestjeklister er beskrevet under [Kategorier af vedligeholdelsesjobtyper og vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper, vedligeholdelsesjobfag og vedligeholdelsestjeklister](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Angiv et navn for at beskrive variablen i feltet **Navn**. Vælg variablen i feltet **Variabel**. Indsæt en beskrivelse af, hvad der skal gøres, i **Instruktioner** i oversigtspanelet **Linjedetaljer**.  
  e. "Mål" bruges til at registrere et bestemt mål. Angiv et navn til målet i feltet **Navn**. Vælg **Tæller** og **Enhed** i oversigtspanelet **Linjedetaljer**. Angiv en beskrivelse af, hvad der skal gøres, i afsnittet **Instruktioner**.  

5. Når du er færdig med at tilføje vedligeholdelsestjeklistelinjer manuelt, skal du udfylde linjerne som beskrevet i afsnittet ovenfor.

>[!NOTE]
>I **Vedligeholdelsestjeklisten for arbejdsordrejob**kan du ikke slette vedligeholdelsestjeklistelinjer med referencen "Jobtype". Du kan kun slette linjer i vedligeholdelsestjeklisten med referencen "Manuel", som du eller andre vedligeholdelsesarbejdere har oprettet manuelt.


![Figur 1](media/14-work-orders.png)

