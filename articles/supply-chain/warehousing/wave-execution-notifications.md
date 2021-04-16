---
title: Beskeder om udførelse af bølge
description: Dette emne beskriver beskeder om bølgeudførelse og forklarer, hvordan du konfigurerer dem.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 0a61aff10234f40f14d603852be30fec3ba83647
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838076"
---
# <a name="wave-execution-notifications"></a>Beskeder om udførelse af bølge

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Funktionen *Beskeder om bølgeudførelse* bruger forretningshændelser og handlingscenteret til at levere beskeder, der vedrører bølgeudførelse. Den giver dig mulighed for at angive de hændelsestyper, der genererer beskeder, de lagersteder, der genererer dem, og de brugere, der modtager dem.

Knappen **Vis meddelelser** (klokkesymbol) i højre side af navigationslinjen angiver, hvornår en meddelelse fra handlingscenteret er tilgængelig for den aktuelle bruger. Brugeren kan vælge knappen **Vis meddelelser** for at åbne handlingscenteret og gennemse meddelelserne.

Forretningshændelser forekommer, når der køres forretningsprocesser. Forretningsprocesser består af opgaver. I løbet af en forretningsproces udfører de brugere, der deltager i den, forretningshandlinger for at udføre disse opgaver. Forretningshændelser udgør en mekanisme, der giver de eksterne systemer mulighed for at modtage beskeder fra Finance and Operations-programmer. På denne måde kan systemerne udføre forretningshandlinger som svar på forretningshændelser. Yderligere oplysninger finder du under [Oversigt over forretningshændelser](../../fin-ops-core/dev-itpro/business-events/home-page.md).

## <a name="turn-on-the-wave-execution-notifications-feature"></a>Slå funktionen Beskeder om bølgeudførelse til

Før du kan bruge funktionen *Beskeder om bølgeudførelse*, skal den være aktiveret i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Beskeder om bølgeudførelse*

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Scenario: Send beskeder om batchkørsel af bølger til handlingscenteret

Dette scenario viser hele flowet for afsendelse af beskeder om udførelsesfejl i bølgebatch til en bestemt rolle via handlingscenter.

### <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Sørg for, at der køres bølger i batchtilstand

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
1. Angiv **Udfør behandling af bølger i batch** til **Ja** i oversigtspanelet *Bølgebehandling*.

> [!NOTE]
> Hvis du vil deaktivere beskeder om udførelse af bølgebatch, skal du angive indstillingen **Deaktiver beskeder om udførelse af bølgebatch** til *Ja*.

### <a name="configure-a-wave-notification-policy"></a>Konfigurere en politik for bølgebeskeder

Politikker for bølgebeskeder definerer de typer beskeder, der sendes, og de brugere, der får besked.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Politikker for bølgebeskeder**.
1. Opret en post, der har følgende indstillinger:

    - **Politik for bølgebesked:** *24BatchError*
    - **Beskrivelse:** *Bølgebatchfejl på lagersted 24*
    - **Send besked om:** *Kun fejl*
    - **Til rolle:** *Systemadministrator*

        > [!NOTE]
        > Da der i dette scenario bruges demodata, er rollen *Systemadministrator* valgt for at gøre det enkelt. Derfor vil du modtage beskeder, fordi du er logget på som systemadministratorbruger. I praksis skal du dog normalt vælge en mere specifik rolle for at give besked om fejl i udførelse af bølgebatch, f.eks. *Lagerchef*.

1. Vælg **Gem** i handlingsruden.

### <a name="configure-a-wave-template"></a>Konfigurere en bølgeskabelon

Med bølgeskabeloner kan du knytte bestemte forekomster af bølgemetoder til tilsvarende bølgeetiketskabeloner.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
1. Angiv feltet **Bølgeskabelontype** til *Forsendelse* i listeruden, og vælg derefter *24 Standard for forsendelse* som bølgeskabelon til lagersted 24.
1. Gå til oversigtspanelet **Generelt**, og indstil feltet **Politik for bølgebesked** til *24BatchError*.

### <a name="configure-a-work-template"></a>Konfigurere en arbejdsskabelon

Arbejdsskabeloner bruges under udførelse af bølger til at generere arbejde. I dette scenario skal der udløses en fejl ved udførelse af bølger. Ved at indstille forespørgslen i arbejdsskabelonen til at bruge et ikke-eksisterende lagersted, sikrer du, at bølgeudførelse mislykkes og derfor sender en besked.

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Angiv feltet **Arbejdsskabelontype** til *Salgsordrer* i listeruden, og vælg derefter *24 Salgsordrestadie* som arbejdsskabelon til lagersted 24.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. I dialogboksen til forespørgselseditoren skal du under fanen **Område** redigere følgende række (eller tilføje den, hvis den ikke findes):

    - **Tabel:** *Midlertidige arbejdstransaktioner*
    - **Afledt tabel:** *Midlertidige arbejdstransaktioner*
    - **Felt:** *Lagersted*
    - **Kriterier:** Ret værdien fra *24* til *Fejl*.

1. Vælg **OK**, og bekræft ændringen.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Oprette en salgsordre og frigive den til lagerstedet

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *24*

1. I oversigtspanelet **Salgsordrelinjer** skal du tilføje en salgsordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001*
    - **Antal:** *10*

    > [!NOTE]
    > Disse varer og antal er kun eksempler. Det angivne lagersted skal have stort nok lagerbeholdning.

1. Mens den nye linje stadig er valgt i oversigtspanelet **Salgsordrelinjer**, skal du vælge **Lager \> Reservation** på værktøjslinjen.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserve parti**. Luk derefter siden.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

### <a name="notifications-from-wave-batch-job-execution"></a>Beskeder fra udførelse af batchjob for bølge

Afhængigt af opsætningen af dine forretningshændelser modtager du i sidste ende en besked om fejl i bølgeudførelse. Meddelelsen i handlingscenteret vil ligne følgende eksempel og indeholde et link til den bølge, der mislykkedes.

> **Fejl under udførelse af bølge**  
> Der opstod en fejl under udførelse af bølgen USMF-000000001.  
> Sidste meddelelser: Der er ikke oprettet noget arbejde for Bølge USMF-000000001.
>
> **STATUS**  
> Aktive
>
> Åbn bølgedetaljer

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
