---
title: Vedligeholdelsestjeklister
description: Dette emne beskriver vedligeholdelsestjeklister i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderChecklist, EntAssetMobileWorkOrderLineChecklistDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 01b05b9df81d8d812d107a1c5b91ba368e9e737e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263632"
---
# <a name="maintenance-checklists"></a>Vedligeholdelsestjeklister

[!include [banner](../../includes/banner.md)]



Vedligeholdelsestjeklister defineres for vedligeholdelsesjobtyper. Udfyldelse af vedligeholdelsestjeklister er en del af færdiggørelsen af en arbejdsordre. Du kan få flere oplysninger om, hvordan du konfigurerer vedligeholdelsestjeklister på vedligeholdelsesjobtyper på siden **Standarder for vedligeholdelsesjobtype** under [Kategorier af vedligeholdelsesjobtyper og vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper, vedligeholdelsesjobfag og vedligeholdelsestjeklister](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Når du arbejder med vedligeholdelsestjeklister på en arbejdsordre, kan du udfylde de foruddefinerede vedligeholdelsestjeklister, der vedrører vedligeholdelsesjobtyper. Du kan også tilføje flere vedligeholdelsestjeklister.


## <a name="fill-in-a-maintenance-checklist"></a>Udfylde en vedligeholdelsestjekliste

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg arbejdsordren, og vælg derefter **Vedligeholdelsestjekliste** i gruppen **Linjer** under fanen **Arbejdsordre** i handlingsruden.

3. I **Vedligeholdelsestjeklisten for arbejdsordrejob** kan du se lister for alle arbejdsordrejob. Hvis arbejdsordrejob har forskellige vedligeholdelsesjobtyper, kan vedligeholdelsestjeklisterne være forskellige på hvert arbejdsordrejob. Vælg et arbejdsordrejob for at arbejde med den relaterede vedligeholdelsestjekliste. Der vises oplysninger om en valgt linje i vedligeholdelsestjeklisten i oversigtspanelet **Linjedetaljer**.

4. Udfyld alle linjer i vedligeholdelsestjeklisten én ad gangen i den rækkefølge, de vises i. Du udfylder en linje på en vedligeholdelsestjekliste ved at udfylde felterne i oversigtspanelet **Linjedetaljer**. De oplysninger, der skal bruges til at udføre en linje, kan variere afhængigt af linjetypen. På en linje af typen **Tekst** tilføjer du f.eks. en note, der forklarer resultatet af tjekket. På en linje af typen **Måling** tilføjer du den tællerværdi, du har aflæst på udstyret, og du kan også tilføje en note, hvis det er nødvendigt. En vedligeholdelsestjeklistelinje af typen **Overskrift** bruges som en overskrift til at gruppere vedligeholdelsestjeklistens linjer under den. Du behøver ikke udfylde en overskrift. Som ved alle andre typer vedligeholdelsestjeklistelinjer kan du føje en note til en linje af typen **Overskrift**.

5. Hvis instruktioner er relateret til en vedligeholdelsestjeklistelinje, er afkrydsningsfeltet **Instruktioner** markeret. Læs instruktioner for den valgte linje på vedligeholdelsestjeklisten i oversigtspanelet **Linjedetaljer** i feltet **Instruktioner**.

6. Når du har fuldført en linje på vedligeholdelsestjeklisten, skal du markere afkrydsningsfeltet **Kontrolleret** på linjen for at markere den som fuldført. Hvis du vil kassere en vedligeholdelsestjeklistelinje, fordi den ikke er relevant for arbejdsordrejobbet, skal du markere afkrydsningsfeltet **I/T** på linjen. Hvis afkrydsningsfeltet **Obligatorisk** er markeret på en vedligeholdelsestjeklistelinje, skal du enten markere afkrydsningsfeltet **Markeret** eller **I/T**.

>[!NOTE]
>Du kan kun opdatere registreringer på vedligeholdelsestjeklister, hvis arbejdsordren har [Aktiv](../setup-for-work-orders/work-order-lifecycle-states.md) livscyklustilstand.  


## <a name="add-a-maintenance-checklist-line"></a>Tilføje en linje på en vedligeholdelsestjekliste

Vedligeholdelsestjeklister oprettes ud fra definitionen af vedligeholdelsesjobtypens standard og overføres til et arbejdsordrejob. Hvis det er nødvendigt, kan du tilføje linjer på vedligeholdelsestjeklister for et arbejdsordrejob. Manuelt tilføjede vedligeholdelsestjeklistelinjer får referencen **Manuel**.

1. På siden **Vedligeholdelsestjeklisten for arbejdsordrejob** skal du vælge det arbejdsordrejob, hvor du vil tilføje en vedligeholdelsestjekliste.

2. Vælg en vedligeholdelsestjeklistelinje i oversigtspanelet **Vedligeholdelsestjeklinjer**. Tryk derefter på **Pil ned**-tasten for at indsætte en ny linje efter den valgte linje. Det næste nummer i serien indsættes automatisk i feltet **Linjenummer**. Hvis du vil indsætte en ny linje før den valgte linje, skal du vælge **Tilføj linje**. 

3. Angiv et navn til vedligeholdelsestjeklistelinjen i feltet **Navn**.

4. Angiv en type for vedligeholdelsestjeklistelinjen i feltet **Type**. For hver vedligeholdelsestjeklistetype indeholder oversigtspanelet **Linjedetaljer** relaterede felter.
    - **Tekst** - Brug denne type til at tilføje en vedligeholdelsestjeklistelinje, der indeholder tekst, som beskriver, hvad der skal gøres. Brug f.eks. denne type af vedligeholdelsestjekliste, hvis du vil have, at en arbejder skal kontrollere eller inspicere noget, uden at du forventer et specifikt (målbart) resultat. Når du har valgt denne type, skal du indtaste tekst i feltet **Instruktioner** i oversigtspanelet **Linjedetaljer**, der beskriver, hvad der skal gøres.
    - **Overskrift** - En vedligeholdelsestjeklistelinje af denne type bruges som en overskrift til at gruppere vedligeholdelsestjeklistens linjer under den. Denne type er nyttig, hvis du har flere vedligeholdelsestjeklistelinjer, der kan inddeles i bestemte områder. Når du har valgt denne type, skal du indtaste et sigende navn i feltet **Navn**.
    - **Skabelon** - Denne type kan ikke anvendes, når du manuelt tilføjer en vedligeholdelsestjeklistelinje på et arbejdsordrejob.  
    - **Variabel** - Brug denne type til at definere et muligt resultat i et interval på en vedligeholdelsestjeklistelinje. Opsætningen af variabler til vedligeholdelsestjeklister er beskrevet under [Kategorier af vedligeholdelsesjobtyper og vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper, vedligeholdelsesjobfag og vedligeholdelsestjeklister](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Når du har valgt denne type, skal du indtaste et sigende navn til variablen i feltet **Navn**. Vælg variablen i feltet **Variabel** i oversigtspanelet **Linjedetaljer**. Indtast en beskrivelse af, hvad der skal gøres, i feltet **Instruktioner**.
    - **Mål** - Brug denne type til at registrere et bestemt mål på vedligeholdelsestjeklistelinjen. Når du har valgt denne type, skal du indtaste et navn til målet i feltet **Navn**. Vælg relevante værdier i felterne **Tæller** og **Enhed** i oversigtspanelet **Linjedetaljer**. Indtast en beskrivelse af, hvad der skal gøres, i feltet **Instruktioner**.

5. Når du er færdig med at tilføje vedligeholdelsestjeklistelinjer manuelt, skal du udfylde linjerne som beskrevet i afsnittet **Udfylde en vedligeholdelsestjekliste** ovenfor.

>[!NOTE]
>På siden **Vedligeholdelsestjeklisten for arbejdsordrejob** kan du ikke slette vedligeholdelsestjeklistelinjer med referencen **Jobtype**. Du kan kun slette linjer i vedligeholdelsestjeklisten med referencen **Manuel**, som du eller andre vedligeholdelsesarbejdere har oprettet manuelt.

Følgende illustration viser et eksempel på en vedligeholdelsestjekliste.

![Figur 1](media/14-work-orders.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]