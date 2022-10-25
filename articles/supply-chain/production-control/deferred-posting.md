---
title: Gøre færdigvarer fysisk tilgængelige før bogføring i kladder
description: Når en produceret vare færdigmeldes, registreres den som tilgængelig til videre fysisk behandling, og en eller flere kladder bogføres. I denne artikel beskrives, hvordan du kan udskyde kladdebogføringer ved at gøre dem i stand til at blive behandlet af et batchjob i en meddelelseskø.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ee767a5d7c3dca2681861802ae42d7a07217c54d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689334"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Gøre færdigvarer fysisk tilgængelige før bogføring i kladder

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Når en arbejder færdigmelder en produceret vare, registreres den som tilgængelig til videre fysisk behandling (f.eks. forsendelse eller Læg på lager). Under denne proces bogføres der også en eller flere kladder (f.eks. færdigmeldingskladden, pluklistekladden og rutekortkladden). Hvis du vil gøre varerne fysisk tilgængelige, før alle posteringer er behandlet, kan du konfigurere systemet til at udskyde kladdeposteringerne. Udskudte posteringer administreres derefter af et batchjob, der behandler posteringerne, som systemressourcer tillader.

I følgende illustration vises, hvordan processer for bogføring af kladder aktiveres både med og uden udskudt bogføring.

![Færdigmeldingsprocessen med og uden udskudt kladdebogføring.](media/deferred-posting-flowchart.png "Færdigmeldingsprocessen med og uden udskudt kladdebogføring")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Aktivere udskudt kladdebogføring for systemet

Før du kan bruge udskudt kladdebogføring, skal den være slået til i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Produktionsstyring*
- **Funktionsnavn:** *(Forhåndsversion) Gør færdigvarer fysisk tilgængelige før bogføring i kladder*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Konfigurere kladdebogføringsindstillinger for færdigmelding

Arbejdere kan færdigmelde varer ved hjælp af en af følgende klienter:

- Webklient
- Warehouse Management-mobilapp
- Grænseflade til kørsel af produktion

Webklienten bruger samme posteringsmetodekonfiguration som Warehouse Management-mobilappen. Den bogføringsmetode, som grænsefladen til produktionsudførelse bruger, skal dog konfigureres separat.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Angive kladdebogføringsindstillinger for webklienten og Warehouse Management-mobilappen

I mobilappen færdigmelder arbejdere varer ved at åbne et menupunkt i mobilenheden, hvor værdien af **Arbejdsoprettelsesproces** er *Færdigmeld* eller *Færdigmeld, og læg på lager*. I webklienten rapporterer arbejdere færdigvarer fra listesiden **Alle produktionsordrer** eller siden **Produktionsordre (detaljer)**. Du kan konfigurere en standardmetode for hele firmaet, og du kan også konfigurere lagerstedsspecifikke tilsidesættelser efter behov.

Benyt følgende fremgangsmåde for at konfigurere standardposteringsmetoden for hele virksomheden til færdigmelding af varer fra webklienten eller Warehouse Management-mobilappen.

1. Gå til **Produktionsstyring \> Konfiguration \> Produktionsstyringsparametre**.
1. Under fanen **Kladder** i sektionen **Færdigmeldingskladde** skal du angive feltet **Bogføringsmetode** til en af følgende værdier:

    - *Øjeblikkelig* – Når en vare færdigmeldes, behandles alle relaterede kladdebogføringer i fuldt omfang, før den markerer færdigvaren som fysisk tilgængelig.
    - *Udskudt* – Når en vare færdigmeldes, markeres færdigvaren som fysisk tilgængelig, og kladdebogføring føjes til en meddelelseskø. Systemet venter ikke, indtil posteringerne behandles fuldt ud, før det markerer den færdige vare som fysisk til rådighed.

Benyt følgende fremgangsmåde for at konfigurere lagerstedsspecifikke tilsidesættelser for den standardkonteringsmetode, der er konfigureret på siden **Produktionsstyringsparametre**.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Lageropdeling \> Lagersteder**.
1. Vælg det lagersted, der skal konfigureres.
1. Vælg **Rediger** i handlingsruden.
1. I oversigtspanelet **Lagersted** i sektionen **Produktionsordrer** skal du angive feltet **Bogføringsmetode** til en af følgende værdier:

    - *Arv* – Det valgte lagersted nedarver indstillingen fra siden **Parametre for produktionsstyring**.
    - *Øjeblikkelig* – Når en vare færdigmeldes, behandles alle relaterede kladdebogføringer i fuldt omfang, før den markerer færdigvaren som fysisk tilgængelig.
    - *Udskudt* – Når en vare færdigmeldes, markeres færdigvaren som fysisk tilgængelig, og kladdebogføring føjes til en meddelelseskø. Systemet venter ikke, indtil posteringerne behandles fuldt ud, før det markerer den færdige vare som fysisk til rådighed.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Angive kladdebogføringsindstillinger til grænsefladen til produktionsudførelse

Benyt følgende fremgangsmåde for at konfigurere den bogføringsmetode, der bruges, når varer færdigmeldes fra grænsefladen til produktionsudførelse.

1. Gå til **Produktionskontrol \> Opsætning \> Produktionsudførelse \> Produktionsordrestandarder**.
1. Under fanen **Færdigmelding** i sektionen **Færdigmeldingskladde** skal du angive feltet **Bogføringsmetode** til en af følgende værdier:

    - *Øjeblikkelig* – Når en vare færdigmeldes, behandles alle relaterede kladdebogføringer i fuldt omfang, før den markerer færdigvaren som fysisk tilgængelig.
    - *Udskudt* – Når en vare færdigmeldes, markeres færdigvaren som fysisk tilgængelig, og kladdebogføring føjes til en meddelelseskø. Systemet venter ikke, indtil posteringerne behandles fuldt ud, før det markerer den færdige vare som fysisk til rådighed.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Planlægge batchjobbet for meddelelsesprocessoren til at behandle udskudte posteringer

Batchjobbet for meddelelsesprocessoren er ansvarlig for behandling af kladdeposteringerne, når de er blevet sat i kø. For at sikre, at kladdeposteringerne behandles, skal du konfigurere dette job til at køre med et regelmæssigt interval. Brug følgende procedure til at konfigurere det nødvendige batchjob.

1. Gå til **Systemadministration \> Meddelelsesprocessor \> Meddelelsesprocessor**.
1. Angiv feltet **Meddelelseskø** til **Produktion** i oversigtspanelet *Parametre*.
1. Angiv **Batchbehandling** til **Ja** i oversigtspanelet *Kør i baggrunden*. Opret derefter en tilbagevendende tidsplan, og konfigurer derefter andre indstillinger efter behov. Indstillingerne fungerer på samme måde som for andre typer af [baggrundsjob](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Microsoft Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>Spore status for udskudte posteringer

Udskudte kladdeposteringer sættes i kø som *meddelelsesprocessormeddelelser*, der venter, indtil de behandles af *meddelelsesprocessoren*. Meddelelsesprocessoren skal være konfigureret til at køre som et planlagt batchjob. Hvis du vil se de udskudte bogføringsmeddelelser, der er blevet eller vil blive behandlet af meddelelsesprocessoren, skal du gå til **Produktionsstyring \> Produktionsordrer \> Bogføring af udskudt produktionsordre**.

### <a name="message-grid-columns-and-filters"></a>Kolonner og filtre i meddelelsesgitteret

Du kan bruge felterne øverst på siden **Bogføring af udskudt produktionsordre** til at finde bestemte meddelelser, du søger efter.

Følgende filtre er tilgængelige:

- **Meddelelsestype** – Angiv den type meddelelser, der vises i gitteret.
- **Meddelelsestilstand** – Angiv tilstanden af de meddelelser, der vises i gitteret. Der findes følgende tilstande:

    - *Kø* – Meddelelsen er klar til at blive behandlet af meddelelsesprocessoren.
    - *Behandlet* – Meddelelsen er blevet behandlet af meddelelsesprocessoren.
    - *Annulleret* – Meddelelsen blev ikke behandlet under det endelige forsøg og blev derefter annulleret af brugeren.
    - *Ikke udført* – Meddelelsen blev ikke behandlet i sidste forsøg. Systemet gentager ikke udførte meddelelser tre gange. Derefter giver det op og lader meddelelsen være i tilstanden *Ikke udført*. Bemærk, at du ikke kan annullere eller redigere en meddelelse manuelt før efter det sidste af disse tre forsøg.

- **Meddelelses indhold** – Dette filter udfører en fuldtekstsøgning af meddelelsens indhold. (Meddelelses indhold vises ikke i gitteret.) Filteret behandler de fleste specialsymboler (f.eks. bindestreger) som mellemrum, og alle mellemrum behandles som booleske OR-operatorer. Hvis du f.eks. indtaster en specifik `journalid`-værdi, der er lig med *USMF-123456*, vil systemet finde alle meddelelser, der indeholder enten "USMF" eller "123456". I dette tilfælde vil listen med resultater sandsynligvis være lang. Det vil derfor være bedre kun at angive *123456*, fordi det vil returnere mere specifikke resultater.

Du kan også sortere og filtrere listen ved at vælge enhver af kolonneoverskrifterne og angive kriterier i dialogboksen med rullelisten.

### <a name="view-the-message-log-message-content-and-details"></a>Få vist meddelelsesloggen, meddelelses indhold og detaljer

Du kan finde detaljerede oplysninger om en meddelelse ved at markere den i gitteret og derefter åbne fanerne **Log** eller **Ubehandlet indhold** under meddelelsesgitteret, hvor hver enkelt behandlingshændelse vises.

Værktøjslinjen under fanen **Log** indeholder følgende knapper:

- **Log** – Vælg denne knap for at få vist behandlingsresultaterne. Denne knap er især nyttig, når meddelelser har **Behandlingsresultat**-værdien *Ikke udført*, og du vil finde årsagerne til, at behandlingen mislykkes.
- **Bundt** – Du kan køre flere operationer til behandling af meddelelser som en del af samme batchproces. Klik på denne knap for at få vist disse detaljerede data. Du kan f.eks. se, om der findes afhængigheder, som kræver, at systemet behandler bestemte meddelelser i en bestemt rækkefølge.

### <a name="manually-process-or-cancel-a-message"></a>Behandle eller annullere en meddelelse manuelt

Du kan efter behov behandle eller annullere en meddelelse manuelt, afhængigt af dens aktuelle tilstand. Vælg meddelelsen i gitteret og derefter **Behandl** eller **Annuller** i handlingsruden.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Konfigurere virksomhedshændelser for at give besked om mislykket behandling af data

Du kan konfigurere [forretningshændelser](../../fin-ops-core/dev-itpro/business-events/home-page.md), der giver dig besked om mislykket behandling. Gå til **Systemadministration \> Konfiguration \> Forretningshændelser \> Forretningshændelseskatalog**, og aktivér forretningshændelsen med navnet *Meddelelse behandlet i meddelelsesprocessor*.

Som en del af aktiveringsprocessen bliver du bedt om at angive, om hændelsen er specifik for en juridisk enhed eller gælder for alle juridiske enheder. Du bliver også bedt om at angive en værdi for **Slutpunktsnavn**. Denne værdi skal defineres først.

> [!NOTE]
> Hvis feltet **Når en virksomhedshændelse indtræffer** er angivet til *Microsoft Power Automate* (i stedet for f.eks. *HTTPS*), oprettes **Slutpunktsnavn** automatisk i Supply Chain Management baseret på opsætningen af *Microsoft Power Automate*.
