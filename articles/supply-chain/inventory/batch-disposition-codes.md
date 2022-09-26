---
title: Bruge batchdispositionskoder til at markere batches som disponible eller ikke til rådighed
description: I denne artikel beskrives, hvordan du opretter og bruger batchdispositionskoder til at markere batches som tilgængelige eller ikke-tilgængelige til brug ved varedisponering, reservation, pluk og/eller forsendelse.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542466"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Bruge batchdispositionskoder til at markere batches som disponible eller ikke til rådighed

Denne artikel beskriver, hvordan du konfigurerer og bruger *batchdispositionskoder*. Hver batchdispositionskode har enten statussen *Disponibel* eller *Ikke til rådighed*. Du kan knytte batchdispositionskoder til lagerbatches for at angive, om alle batches er tilgængelige for varedisponering, reservation, pluk og/eller forsendelse.

Hvis du vil bruge batchdispositionskoder, skal du konfigurere koderne og knytte dem til de batches, du vil administrere.

## <a name="set-up-batch-disposition-codes"></a>Konfigurere batchdispositionskoder

Du skal konfigurere alle de batchdispositionskoder, du vil bruge i systemet. Du kan oprette lige så mange koder, som du vil. (Du kan f.eks. oprette koder for at identificere de forskellige årsager til, at et batch kan være tilgængeligt eller ikke til rådighed). Der er dog ofte kun to koder: én for *disponibel* og én for *ikke til rådighed*. Du kan også oprette brugerdefinerede koder, der gør det muligt at bruge et batch for nogle handlinger, men ikke for andre.

Benyt følgende fremgangsmåde for at konfigurere batchdispositionskoder.

1. Gå til **Lagerstyring \> Opsætning \> Batch \> Batchdispositionsmaster**.
1. På siden **Batchdispositionsmaster** vises de aktuelle batchdispositionskoder, og du kan oprette, slette og redigere dem. Udfør ét af følgende trin:

    - Hvis du vil redigere en eksisterende kode, skal du vælge den i listeruden.
    - Vælg **Ny** i handlingsruden for at oprette en ny kode.

1. Udfyld følgende felter i sidehovedet for den nye eller valgte kode:

    - **Batchdispositionskode** – Angiv det viste navn for koden.
    - **Beskrivelse** – Beskriv, hvordan koden skal anvendes.
    - **Batchdispositionsstatus** – Vælg den status, der gælder for de batches, som koden er tildelt:

        - *Ikke til rådighed* – Batchene kan ikke bruges til varedisponering, reservation, pluk eller forsendelse. Når du vælger denne værdi, er alle indstillingerne for **Bloker** i oversigtspanelet **Opsætning** angivet til *Ja*,og alle indstillinger for **Tilgængelig** er angivet til *Nej*. Du kan dog ændre nogle af disse indstillinger, hvis du vil tilføje undtagelser.
        - *Disponibel* – Batchene kan bruges til varedisponering, reservation, pluk og/eller forsendelse. Når du vælger denne værdi, er alle indstillingerne for **Bloker** i oversigtspanelet **Opsætning** angivet til *Nej*,og alle indstillinger for **Tilgængelig** er angivet til *Ja*. Disse indstillinger er skrivebeskyttede, når feltet **Batchdispositionsstatus** er angivet til *Disponibel*.

1. Hvis du angiver feltet **Batchdispositionsstatus** til *Ikke til rådighed*, kan du tilpasse blokstatus for hver handling (reservation, pluk og afsendelse) for hver ordretype (salg, flytning og produktion). I forbindelse med produktionsordrer kan du vælge at blokere eller fjerne blokeringen af produktionspluklistekladden. Du kan også vælge at blokere eller fjerne blokeringen af varedisponering. Brug indstillingerne i oversigtspanelet **Opsætning** til at blokere eller fjerne blokeringen af de enkelte handlinger efter behov. Angiv indstillingen **Tilgængelig** til *Ja* for at aktivere varedisponering, eller angiv den til *Nej* for at blokere varedisponering.

## <a name="assign-batch-disposition-codes-to-batches"></a>Tildele batchdispositionskoder til batches

Når du har defineret de batchdispositionskoder, du skal bruge, skal du følge disse trin for at tildele dem til batches.

1. Gå til **Lagerstedsstyring \> Opsætning \> Lagerbeholdning \> Batches**.
1. Vælg en eller flere batches, der skal tildeles en batchdispositionskode.
1. I handlingsruden skal du vælge **Nulstil batchdispositionskode** under fanen **Nulstil**.
1. Angiv feltet **Ny batchdispositionskode** field til navnet på den kode, du vil tildele, dialogboksen **Rediger begrænsningerne på lagerbatch**.
1. Vælg **OK** for at anvende den nye indstilling og gemme din ændring.

    På siden **Batches** opdateres værdierne i kolonnerne **Batchdispositionskode** og **Batchdispositionsstatus**, så de afspejler de nye indstillinger for de valgte batches.

## <a name="master-planning-example"></a>Eksempel på varedisponering

Dette eksempel viser, hvordan batchdispositionskoder kan påvirke varedisponering.

I dette eksempel konfigureres batchdispositionskoder på følgende måde:

- *P-Disponibel:*

    - **Batchdispositionsstatus:** *Disponibel*
    - **Tilgængelig:** *Ja*

- *P-Ikke til rådighed.*

    - **Batchdispositionsstatus:** *Ikke til rådighed*
    - **Tilgængelig:** *Nej*

Der findes et produkt (*Produkt-1*), der har to batches: *Batch-A* og *Batch-B*. Disse batches er konfigureret på følgende måde:

- *Batch-A:*

    - **Batchdispositionskode:** *P-Disponibel*
    - **Beholdningsantal:** 1

- *Batch-B:*

    - **Batchdispositionskode:** *P-Ikke til rådighed*
    - **Beholdningsantal:** 1

Der er en salgsordre (*SO1*) for et antal på 2 for produktet *Produkt-1*. Leveringsdatoen er tre dage fra i dag.

Du kan køre varedisponering og angive følgende værdier, der er relevante for dette eksempel:

- **Ordreforslag:** *Indkøbsordre*
- **Genbestillingsstrategi:** *Behov*
- **Leveringstid:** *0*

Som et resultat af varedisponeringskørslen bruger systemet den tilgængelige batch (*Batch-A*) til at dække et antal på 1 af *Produkt-1* for salgsordre *SO1*. Det kan dog ikke bruge batchen *Batch-B*, fordi denne batch er markeret som ikke til rådighed for disponering. Så for at dække det resterende antal opretter systemet et indkøbsordreforslag (*PPO1*) for en ny batch med produktet *Produkt-1*.

I følgende illustration vises, hvordan tidslinjen ser ud for disponeringsresultatet.

![Eksempel, der viser, hvordan batchdispositionskoder kan påvirke varedisponering.](media/batch-codes-planning-example.png "Eksempel, der viser, hvordan batchdispositionskoder kan påvirke varedisponering")
