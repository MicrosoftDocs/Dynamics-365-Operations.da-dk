---
title: Konfigurere grænsefladen til produktionsudførelse
description: Denne artikel beskriver, hvordan du opretter en eller flere konfigurationer til grænsefladen til kørsel af produktionsudstyr. Når du åbner grænsefladen til kørsel af produktionsudstyr, indlæser den automatisk en udvalgt konfiguration og et jobfilter, der er specifikt for browseren og enheden. I konfigurationen skal du angive de politikker, der skal gælde for en bestemt anvendelse.
author: johanhoffmann
ms.date: 11/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 641b293617df608bc07b97c077dbcd05664f8e2a
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748680"
---
# <a name="configure-the-production-floor-execution-interface"></a>Konfigurere grænsefladen til kørsel af produktionsudstyr

[!include [banner](../includes/banner.md)]

Arbejderne i produktionen bruger grænsefladen til kørsel af produktionsudstyr til at registrere deres daglige arbejde, f.eks. hvornår de påbegynder et job, rapportere feedback om job, registrere indirekte aktiviteter og rapportere fravær. Disse registreringer er grundlaget for sporing af fremskridt og omkostninger ved produktionsordrer og til beregning af grundlaget for arbejdernes løn.

Når du åbner grænsefladen til kørsel af produktionsudstyr, indlæser den automatisk en udvalgt konfiguration og et jobfilter, der er specifikt for browseren og enheden. I konfigurationen skal du angive de politikker, der skal gælde for en bestemt anvendelse. Her er nogle anvendelseseksempler:

- På en enhed i firmaets ankomsthallen stempler medarbejderne ind, når de ankommer til kontoret, og ud, når de går hjem.
- På en enhed i produktionshallen registrerer maskinoperatørerne, hvornår de starter og afslutter job. De registrerer også pauser og indirekte aktiviteter.

Denne artikel beskriver de forskellige indstillinger til konfiguration af en grænseflade til produktionsudførelse for hver enhed, der bruges på dit sted.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Aktivere grænsefladen til kørsel af produktion og dens relaterede valgfrie funktioner

Selve grænsefladen til kørsel af produktion, plus flere af de valgfrie indstillinger, der er beskrevet i denne artikel, skal være aktiveret for systemet, før du kan bruge dem. Brug siden [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere nogle af eller alle de funktioner, der er beskrevet i følgende underafsnit, efter behov.

### <a name="the-production-floor-execution-interface"></a>Grænsefladen til kørsel af produktion

Dette er den primære funktion, der er beskrevet i denne artikel, og som er en forudsætning for alle de andre funktioner, der nævnes i dette afsnit. Fra og med Supply Chain Management version 10.0.25 er den obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Produktionsudførelse* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="generate-license-plates"></a>Generere nummerplader

Disse funktioner gør nummerpladefunktioner tilgængelig for grænsefladen til kørsel af produktion. Hvis du vil bruge dem, skal du aktivere følgende funktioner i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rækkefølge):

1. *Id for færdigmelding tilføjet i jobkortenheden*<br>(Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk.)
1. *Aktivér automatisk generering af id-nummer ved færdigmelding i jobkortenheden*<br>(Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk.)

### <a name="print-labels"></a>Udskriv labels

Disse funktioner gør etiketudskrivning tilgængelig for grænsefladen til kørsel af produktion. Hvis du vil bruge dem, skal du aktivere følgende funktioner i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rækkefølge):

1. *Id for færdigmelding tilføjet i jobkortenheden*<br>(Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk.)
1. *Udskriv etiket fra jobkortenhed*<br>(Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk.)

### <a name="allow-locking-the-touch-screen"></a>Tillad låsning af berøringsskærmen

Denne funktion gør det muligt at give arbejdere mulighed for at låse berøringsskærmen, så de kan desinficere den.

Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan administratorer slå denne funktionalitet til eller fra ved at søge efter *Funktion til låsning af jobkortenhed og jobkortterminal, så de kan renses.* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Funktion til aktivstyring af grænsefladen til produktionsudførelse

Denne funktion føjer en fane for aktivstyring til grænsefladen for produktionsudførelse. Arbejdere kan bruge denne fane til at vælge et aktiv, der er tilknyttet en maskinressource, som findes inden for det valgte filter på joblisten. For det valgte maskinaktiv kan arbejderen få vist aktivets tilstand fra tællerværdier for op til fire udvalgte tællere.

Fra og med Supply Chain Management version 10.0.25 er denne funktion som standard aktiveret. Fra og med Supply Chain Management version 10.0.29 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.29, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Funktion til aktivstyring af grænsefladen til produktionsudførelse* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="job-search"></a>Jobsøgning

Denne funktion gør det muligt at føje et søgefelt til joblisten. Arbejdere kan finde et bestemt job ved at angive job-id'et eller finde alle job for en bestemt ordre ved at angive ordre-id'et. Arbejdere kan angive id'et ved hjælp af et tastatur eller ved at scanne en stregkode.

Fra og med Supply Chain Management version 10.0.25 er denne funktion som standard aktiveret. Fra og med Supply Chain Management version 10.0.29 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.29, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Jobsøgning til grænsefladen til produktionen* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="report-on-co-products-and-by-products"></a>Rapportere om samprodukter og biprodukter

Denne funktion giver medarbejderne mulighed for at bruge grænsefladen til produktionsudførelse til at rapportere status for batchordrer. Denne rapportering inkluderer rapportering af samprodukter og biprodukter.

Før du kan bruge denne funktion, skal den være aktiveret i dit system. Fra og med Supply Chain Management version 10.0.29 er funktionen som standard aktiveret. Administratorer kan slå denne funktion til eller fra ved at søge efter funktionen *Rapport over samprodukter og biprodukter fra grænsefladen for udførelse af produktion* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="display-full-serial-batch-and-license-plate-numbers"></a>Vise komplette serie-, batch- og id-numre

Denne funktion giver en forbedret ydeevne, når du får vist lister over serie-, batch- og nummerpladenumre i brugergrænsefladen til produktionsudførelse. Visningen ændres fra en kortvisning med et begrænset antal tegn til en listevisning, der giver tilstrækkelig plads til at vise de fulde værdier. Listen giver dig også mulighed for at søge efter bestemte numre.

Før du kan bruge denne funktion, skal den være aktiveret i dit system. Fra og med Supply Chain Management version 10.0.25 er funktionen som standard aktiveret. Fra og med Supply Chain Management version 10.0.29 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.29, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Vis fulde serie-, batch- og id-numre i grænsefladen til produktionsudførelse* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Fra og med Supply Chain Management version 10.0.25 er denne funktion som standard aktiveret. Administratorer kan slå denne funktion til eller fra ved at søge efter funktionen *Vis fulde serie-, batch- og id-numre i grænsefladen til produktionsudførelse* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="register-material-consumption"></a>Registrer materialeforbrug

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Denne funktion giver arbejdere mulighed for at bruge brugergrænsefladen til produktionsudførelse til at registrere materialeforbrug, batchnumre og serienumre. Visse producenter, især dem inden for procesindustrien, skal udtrykkeligt kunne registrere den mængde materiale, der forbruges for de enkelte batch- eller produktionsordrer. Arbejdere kan for eksempel bruge en vægt til at veje mængden af materiale, der forbruges, når de arbejder. For at sikre fuld sporbarhed af materialer skal disse organisationer også registrere, hvilke batchnumre der blev forbrugt ved fremstillingen af de enkelte produkter.

Der er to versioner af denne funktion. Den ene understøtter varer, der *ikke er* aktiveret til brug af lokationsstyringsprocesser (WMS). Den anden understøtter varer, der *er* aktiveret til at bruge WMS. Hvis du vil bruge denne funktion, skal du aktivere en af eller begge følgende funktioner i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rækkefølge), afhængigt af om du har varer, der er aktiveret for WMS:

- *Registrer materialeforbrug i grænsefladen for produktionsudførelse (ikke-WMS)*
- *(Forhåndsversion) Registrer materialeforbrug i grænsefladen for produktionsudførelse (WMS-aktiveret)*

> [!IMPORTANT]
> Du kan bruge funktionen ikke-WMS alene. Hvis du bruger WMS, skal du dog aktivere begge funktioner.

### <a name="report-on-catch-weight-items"></a>Rapportering om fastvægtvarer

Medarbejdere kan bruge grænsefladen til produktionsudførelse til at rapportere status for fastvægtvarer i batchordrer. Batchordrer oprettes ud fra formler, som kan defineres til at have fastvægtvarer som formelvarer, samprodukter og biprodukter. En formel kan også defineres, så den indeholder formellinjer til ingredienser, der er defineret for fastvægt. Fastvægtvarer bruger to måleenheder til at spore lagerbeholdning: fastvægtantal og lagerantal. I fødevarebranchen kan kød i kasser f.eks. defineres som en fastvægtvare, hvor fastvægtantallet bruges til at spore antallet af kasser, og lagerantallet bruges til at spore kassernes vægt.

Hvis du vil bruge denne funktion, skal du aktivere følgende funktion i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Rapport over fastvægtvarer fra grænsefladen for udførelse af produktionsgulv*

### <a name="the-my-day-dialog"></a>Dialogboksen "Min dag"

Dialogboksen **Min dag** giver arbejdere et overblik over deres daglige registreringer og aktuelle saldi for betalt tid, betalt overtid, fravær og betalt fravær.

Før du kan bruge denne funktion, skal den være aktiveret i dit system. Fra og med Supply Chain Management version 10.0.29 er funktionen som standard aktiveret. Administratorer kan slå denne funktion til eller fra ved at søge efter funktionen *Visningen "Min dag" til grænsefladen til produktionsudførelse* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="teams"></a>Teams

På denne måde kan flere arbejdere arbejde som et team på samme produktionsjob. Teamet kan udpege én arbejder som pilot. De øvrige arbejdere bliver derefter automatisk assistenter for den pågældende pilot. Det er kun piloten, der skal registrere jobstatus for det resulterende team. Tidsposter gælder for alle teammedlemmer.

Hvis du vil bruge denne funktion, skal du aktivere følgende funktion i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Grænsefladen til produktionsteam i produktionsudførelse*

### <a name="additional-configuration-in-the-production-floor-execution-interface"></a>Yderligere konfiguration af grænsefladen i produktionsudførelse

Denne funktion føjer indstillinger til følgende funktioner på siden **Konfigurer produktionsudførelse**:

- Åbn automatisk dialogboksen **Start job**, når en søgning er fuldført.
- Åbn automatisk dialogboksen **Rapport i gang**, når en søgning er fuldført.
- Udfyld det resterende antal på forhånd i dialogboksen **Rapportstatus**.
- Aktiver materialeforbrugsjusteringer fra dialogboksen **Rapporter status**. (Denne funktion kræver også *Registrere materialeforbrug i produktionsudførelsesgrænsefladen (ikke-WMS)-funktionen*).
- Aktivér søgninger efter projekt-id.

Denne artikel indeholder oplysninger om, hvordan du konfigurerer udbyderen senere.

Hvis du vil bruge denne funktion, skal du aktivere følgende funktion i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Yderligere konfiguration af grænsefladen til produktionsudførelse*

### <a name="enable-the-my-jobs-tab"></a>Aktivere fanen Mine job

Fanen **Mine job** giver arbejderne mulighed for nemt at se alle ikke-startede og ikke-færdigmeldte job, der er tildelt specifikt til dem. Den er nyttig i firmaer, hvor job nogle gange eller altid tildeles bestemte arbejdere (personale) i stedet for andre typer ressourcer (f.eks. maskiner).

Hvis du vil bruge denne funktion, skal du aktivere følgende funktion i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Fanen Mine job i grænsefladen til produktionsudførelse*

### <a name="enable-use-of-a-numpad-on-the-sign-in-page"></a>Aktivér brugen af et numerisk tastatur på logonsiden

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until 10.0.31 GA -->

Med denne funktion kan administratorer tilføje et numerisk tastatur på logonsiden i grænsefladen til produktionsudførelse. Arbejdere kan derefter logge på ved at bruge det numeriske tastatur til at angive deres kort-id eller personlige nummer.

Hvis du vil bruge denne funktion, skal du aktivere følgende funktion i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Aktivér brugen af et numerisk tastatur på loginsiden*

## <a name="work-with-production-floor-execution-configurations"></a>Arbejde med kørselskonfigurationer for produktionsudstyr

Når du vil oprette og vedligeholde konfigurationer af produktionsudførelse, skal du gå til **Produktionsstyring \> Konfiguration \> Produktionsudførelse \> Konfigurer kørsel af produktionsudstyr**. På siden **Konfigurer kørsel af produktionsudstyr** vises en liste over eksisterende konfigurationer. Du kan udføre følgende opgaver på denne side:

- Vælg en konfiguration for produktionsudstyr, der er angivet i venstre kolonne, for at få vist og redigere den.
- Vælg **Ny** i handlingsruden for at føje en ny konfiguration til listen. Angiv et navn i feltet **Konfiguration** for at identificere den nye konfiguration. Det navn, du angiver, skal være entydigt blandt alle konfigurationer, og du kan ikke redigere det senere. Angiv en detaljeret beskrivelse af transaktionen i feltet **Beskrivelse**.

Konfigurer derefter de forskellige indstillinger for den valgte konfiguration som beskrevet i følgende undersektioner.

### <a name="the-general-fasttab"></a>Oversigtspanelet Generelt

Følgende oplysninger er tilgængelige under oversigtspanelet **Generelt**:

- **Kun komme og gå-tid** – Angiv denne indstilling til *Ja* for at oprette en forenklet grænseflade, der kun indeholder en komme- og gå-funktion. Denne indstilling deaktiverer de fleste andre indstillinger på denne side. Du skal fjerne alle linjer i oversigtspanelet **Fanevalg**, før du kan aktivere denne indstilling.
- **Aktivér søgning** – Angiv denne indstilling til *Ja* for at medtage et søgefelt på joblisten. Arbejdere kan finde et bestemt job ved at angive job-id'et eller finde alle job for en bestemt ordre ved at angive ordre-id'et. Arbejdere kan angive id'et ved hjælp af et tastatur eller ved at scanne en stregkode.
- **Aktiver søgning efter projekt-id** – Angiv denne indstilling til *Ja* for at give arbejdere mulighed for at søge efter projekt-id (ud over job-id og ordre-id) i søgefeltet i brugergrænsefladen til produktionsudførelse. Du kan kun angive denne indstilling til *Ja*, hvis indstillingen **Aktiver søgning** er angivet til *Ja*.
- **Dialogboks til automatisk åbning af start** – Når denne indstilling er angivet til *Ja*, åbnes dialogboksen **Start job** automatisk, når arbejdere bruger søgelinjen til at finde jobbet.
- **Automatisk åbning af dialogboksen Rapportér status** – Når denne indstilling er angivet til *Ja*, åbnes dialogboksen **Rapportér status** automatisk, når arbejdere bruger søgelinjen til at finde jobbet.
- **Aktiver justering af** materiale – Angiv denne indstilling til *Ja* for at **aktivere knappen** Juster materiale i dialogboksen **Rapport** status. Arbejderne kan justere materialeforbruget for hvert produktionsjob.
- **Afmelding ved gå** – Vælg *Ja* i denne indstilling for at bede arbejdere om at rapportere feedback om igangværende job, når de stempler ud. Når der er valgt *Nej* i denne indstilling, bliver arbejderne ikke bedt om at gøre dette.
- **Lås medarbejder** – Når der er valgt *Nej* i denne indstilling, bliver arbejderne logget af umiddelbart efter, at de har foretaget en registrering (f.eks. et nyt job). Grænsefladen vender derefter tilbage til logonsiden. Når der er valgt *Ja* i denne indstilling, forbliver arbejderne logget på grænsefladen til produktionsudførelse. Men en arbejder kan logge af manuelt, så en anden arbejder kan logge på, mens grænsefladen til produktionsudførelse fortsætter med at køre under den samme systembrugerkonto. Du kan finde flere oplysninger om disse typer konti under [Tildelte brugere](config-job-card-device.md#assigned-users).
- **Brug det faktiske registreringstidspunkt** – Vælg *Ja* i denne indstilling for at indstille tidspunktet for hver ny registrering til netop det tidspunkt, hvor arbejderen afsendte registreringen. Når der er valgt *Nej* i denne indstilling, bruges logontidspunktet i stedet. Du skal normalt vælge *Ja* i denne indstilling, hvis du har valgt **Ja** i indstillingerne **Lås medarbejder** og/eller *Enkelt arbejder*, i de tilfælde hvor arbejderne ofte forbliver logget ind i længere perioder.
- **Enkelt arbejder** – Vælg *Ja* i denne indstilling, hvis kun én arbejder bruger en grænseflade til produktionsudførelse, hvor denne konfiguration er aktiv. Når der er valgt *Ja* i denne indstilling, er **Lås medarbejder** også automatisk indstillet til *Ja*. Derudover fjerner denne indstilling kravet (og muligheden) for, at arbejderen logger på ved hjælp af et kort-ID (eller anden lignende id). I stedet logger medarbejderen på Microsoft Dynamics 365 Supply Chain Management ved hjælp af en systembrugerkonto, der er knyttet til en *tidsregistreret arbejder* (fra tabellen *arbejdere*), og som bliver logget på grænsefladen til produktionsudførelse som den pågældende arbejder på samme tid.
- **Aktivér numerisk tastatur** – Angiv denne indstilling til *Ja*, hvis du vil føje et numerisk tastatur til logonskærmen, der gør det muligt for arbejderne at angive deres kort-id eller personlige nummer på et numerisk tastatur med berøringsskærm. Angiv denne indstilling til *Nej* for at skjule det numeriske tastatur.
- **Tillad låsning af berøringsskærm** – Angiv denne indstilling til *Ja* for at give arbejderne mulighed for at låse berøringsskærmen på grænsefladen til produktionsudførelse, så de kan rense den. Når denne indstilling er angivet til *Ja*, tilføjes knappen **Lås skærm for rensning** på logonsiden. Når en arbejder vælger denne knap, låses berøringsskærmen midlertidigt for at forhindre utilsigtet input. Der vises også en nedtællingstimer. Arbejderen kan derefter rense enheden og skærmen på sikker vis. Når nedtællingen er fuldført, låses berøringsskærmen automatisk op.
- **Varighed af låst skærm** – Når indstillingen **Tillad låsning af berøringsskærm** er sat til *Ja*, kan du bruge denne indstilling til at angive, hvor mange sekunder berøringsskærmen skal låses for rensning. Varigheden skal være mellem 5 og 120 sekunder.
- **Generér nummerplade** – Angiv denne indstilling til *Ja* for at generere en ny nummerplade, hver gang en arbejder bruger grænsefladen til produktionsudførelse til færdigmelding. Nummeret på nummerpladen genereres ud fra en nummerserie, der er konfigureret på siden **Parametre til Warehouse management**. Når der er valgt *Nej* i denne indstilling, skal arbejderne angive en eksisterende nummerplade, når de rapporterer færdigmeldt.
- **Udskriv label** – Angiv denne indstilling til *Ja* for at udskrive en nummerpladelabel, når en arbejder bruger grænsefladen til produktionsudførelse til færdigmelding. Konfigurationen af labelen foretages i dokumentruteplanlægning som beskrevet i [Labellayout i dokumentruteplanlægning](../warehousing/document-routing-layout-for-license-plates.md).

### <a name="the-tab-selection-fasttab"></a>Vælg Fane i oversigtspanelet

Brug indstillingerne i oversigtspanelet **Valg af fane** til at vælge, hvilke faner der skal vises i grænsefladen til kørsel af produktion, når den aktuelle konfiguration er aktiv. Du kan designe lige så mange faner, du har brug for, og derefter tilføje og arrangere dem efter behov ved hjælp af knapperne på værktøjslinjen i oversigtspanelet. Du kan finde flere oplysninger om, hvordan du designer faner og arbejder med indstillingerne, under [Designe grænsefladen til kørsel af produktion](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Oversigtspanelet Status for rapport

Følgende oplysninger er tilgængelige under oversigtspanelet **Rapportér status**:

- **Aktiver justering af materiale** – Angiv denne indstilling til *Ja* for at inkludere knappen **Juster materiale** i dialogboksen **Rapporter status**. Arbejderne kan justere materialeforbruget for hvert produktionsjob.
- **Standard-restantal** – Angiv denne indstilling til *Ja* for at udfylde det forventede restantal for et produktionsjob i dialogboksen **Rapportér status**.

## <a name="clean-up-job-configurations"></a>Rydde op i jobkonfigurationer

Når shop floor-supervisor konfigurerer grænsefladen til kørsel af produktionsudstyr, vælger han eller hun en konfiguration og et jobfilter. Disse valg gemmes i en referencetabel i Supply Chain Management, og browseren bruger et id, der er gemt i en lokal cookie, til at finde den rigtige række i den pågældende tabel. Tabellen registrerer også den dato og det klokkeslæt, hvor en arbejder senest loggede på hver enkelt enhed.

Et batchjob renser regelmæssigt poster i referencetabellen for enheder, der ikke har logget nogen aktiviteter i de sidste 60 dage. Du kan også til enhver tid manuelt rense posterne ved at følge disse trin.

1. Gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurer kørsel af produktionsudstyr**.
1. Vælg **Ryd op i klientkonfigurationer** i handlingsruden.
1. I dialogboksen **Ryd op i klientkonfigurationer** skal du indstille feltet **Antal dage** til det antal dage uden aktivitet (før i dag), der skal tages i betragtning. Du vil fjerne alle konfigurationer og logonposter for enheder, der ikke har været aktive i den pågældende periode.
1. Vælg **OK** for at rydde op i de relevante konfigurationer baseret på indstillingen **Antal dage**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
