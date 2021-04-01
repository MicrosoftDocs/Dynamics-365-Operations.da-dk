---
title: Konfigurer jobkort for enheder
description: I dette emne beskrives de forskellige indstillinger for konfiguration af jobkortenheden.
author: johanhoffmann
manager: tfehr
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: c139fb7daa0f40b6b7afb0a707f714502d3146d1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246351"
---
# <a name="configure-job-card-for-devices"></a>Konfigurer jobkort for enheder

[!include [banner](../includes/banner.md)]

Jobkortenheden bruges af medarbejdere i produktionen til at registrere deres daglige arbejde, f.eks. hvornår arbejdet påbegyndes, feedbackrapportering om job, registrering af indirekte aktiviteter og fraværsrapportering. Disse registreringer er grundlaget for sporing af fremskridt og omkostninger ved produktionsordrer og til beregning af grundlaget for arbejdernes løn. I dette emne beskrives de forskellige indstillinger for konfiguration af jobkortenhederne.

## <a name="enable-new-features-in-feature-management"></a>Aktivér nye funktioner i funktionsstyring

Nogle få af de indstillinger, der er beskrevet i dette emne, skal være aktiveret i systemet, før de bliver tilgængelige for dig. Brug siden [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere en eller flere af de følgende funktioner efter behov.

### <a name="generate-license-plate"></a>Generér nummerplade

Hvis du vil gøre denne funktion tilgængelig, skal du aktivere følgende funktioner i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i rækkefølge):

1. Id for færdigmelding tilføjet i jobkortenheden
1. Aktivér automatisk generering af id-nummer ved færdigmelding i jobkortenheden

### <a name="print-label"></a>Udskriv label

Hvis du vil gøre denne funktion tilgængelig, skal du aktivere følgende funktioner i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i rækkefølge):

1. Id for færdigmelding tilføjet i jobkortenheden
1. Udskriv etiket fra jobkortenhed

### <a name="allow-locking-of-touch-screen"></a>Tillad låsning af berøringsskærm

Hvis du vil gøre denne funktion tilgængelig, skal du aktivere den følgende funktion i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- (Prøveversion) Funktion til låsning af jobkortenhed og jobkortterminal, så de kan renses

## <a name="manage-your-device-configurations"></a>Administrer konfigurationen af din enhed

Du kan konfigurere din enhed ved at gå til **Produktionsstyring > Opsætning > Produktionsudførelse > Konfigurer jobkort for enheder**. Siden **Konfigurer jobkort for enheder** åbnes. Den indeholder en liste over eksisterende konfigurationer. Herfra kan du evt. benytte følgende fremgangsmåde: 

- Vælg en enhedskonfiguration, der er angivet i venstre kolonne, for at få vist og redigere den.
- Vælg **Ny** i handlingsruden for at føje en ny enhedskonfiguration til listen. Angiv derefter et navn i feltet **Konfiguration** for at identificere den nye konfiguration. Den værdi, du angiver her, skal være entydig blandt alle enhedskonfigurationer, og du kan ikke redigere den senere.

Se følgende afsnit, hvis du vil have oplysninger om de enkelte indstillinger til konfiguration af jobkortenheder.

## <a name="general-settings"></a>Generelle indstillinger

I oversigtspanelet **Generelt** kan du konfigurere hver af de forskellige indstillinger, der er tilgængelige for den valgte enhedskonfiguration. Følgende indstillinger er tilgængelige:

- **Afmelding ved gå** – Her angives **Ja** for at bede arbejdere om at rapportere tilbagemeldinger om igangværende job, når der stemples ud. Når denne indstilling angives til **Nej**, bliver arbejderne ikke bedt om at gøre dette.
- **Lås medarbejder** – Når denne indstilling er angivet til **Nej**, logges arbejderen af, umiddelbart efter at der er foretaget en registrering (f.eks. et nyt job), og derefter vender enheden tilbage til logonsiden. Når denne indstilling er angivet til **Ja**, logges arbejderen på jobkortenheden. Arbejderen vil dog stadig kunne logge af manuelt, så en anden arbejder kan logge på, mens jobkortenheden stadig kører under den samme systembrugerkonto. Du kan finde flere oplysninger om disse typer konti under [Tildelte brugere](#assigned-users).
- **Stregkodescanner** – Angiv dette til **Ja** for at give arbejderne mulighed for på jobkortenheden at registrere start på et nyt job ved at scanne en stregkode.
- **Brug det faktiske registreringstidspunkt** – Angiv **Ja** for at indstille det tidspunkt for hver ny registrering, der skal være lig med det nøjagtige tidspunkt, da registreringen blev sendt af en arbejder. Angiv **Nej** for at bruge logontidspunktet i stedet for. Du skal normalt angive dette til **Ja**, hvis du har aktiveret **Lås medarbejder** og/eller **Enkelt arbejder**, i de tilfælde hvor arbejderne ofte er logget ind i længere perioder.
- **Enkelt arbejder** – Angiv denne indstilling til **Ja**, hvis kun én arbejder bruger en jobkortenhed, hvor denne konfiguration er aktiv. Når denne indstilling er valgt, angives indstillingen **Lås medarbejder** automatisk til **Ja**. Derudover fjerner denne indstilling kravet (og muligheden) for, at arbejderen logger på ved hjælp af et kort-ID (eller lignende). I stedet logger medarbejderen på Supply Chain Management ved hjælp af en systembrugerkonto, der er knyttet til en *tidsregistreret arbejder* (fra tabellen *arbejdere*), og som bliver logget på jobkortenheden som den pågældende arbejder på samme tid.  Du kan finde flere oplysninger om disse typer konti under [Tildelte brugere](#assigned-users).
- **Tillad, at arbejdere angiver personlige filtre** – Angiv denne indstilling til **Ja** for at give arbejderne mulighed for at filtrere de job, der vises for dem, på enheden. Arbejderen kan redigere værdierne for et af de tre filterkriterier: **Produktionsenhed**, **Ressourcegruppe** og **Ressource**. Det er kun job, der er planlagt til ressourcer, som svarer til de valgte filterkriterier, der vises på enheden. Du kan også tildele standardværdier for et eller flere af disse kriterier, og de vil gælde, selvom denne indstilling ikke er valgt.
- **Tillad låsning af berøringsskærm** – Angiv denne indstilling til **Ja** for at give arbejderne mulighed for at låse berøringsskærmens jobkortenhed, så de kan rense den. Når indstillingen er aktiveret, føjes der en knap for **Lås skærm for rensning** til enhedens logonside. Når en arbejder vælger denne knap, låses berøringsskærmen midlertidigt for at forhindre utilsigtet input, og der vises en nedtællingstimer. Arbejderen kan nu rense enheden og skærmen på sikker vis. Når nedtællingen er fuldført, låses berøringsskærmen automatisk igen.
- **Varighed af låst skærm** – Når indstillingen **Tillad låsning af berøringsskærm** er aktiveret, kan du bruge denne indstilling til at angive, hvor mange sekunder berøringsskærmen skal låses for rensning. Varigheden skal være mellem 5 og 120 sekunder.
- **Produktionsenhed** – Vælg en produktionsenhed, der skal anvendes som standardfilterkriterium for den liste over job, der vises for hver arbejder. Det er kun job, der er planlagt på ressourcer, som er grupperet under den valgte produktionsenhed, der vises af enheden til at begynde med. Hvis **Tillad, at arbejdere angiver personlige filtre** er aktiveret, vil arbejderne kunne redigere denne værdi, ellers vil dette filter altid gælde, når denne enhedskonfiguration er aktiv.
- **Ressourcegruppe** – Vælg en ressourcegruppe, der skal anvendes som standardfilterkriterium for den liste over job, der vises for hver arbejder. Det er kun job, der er planlagt på ressourcer, som er grupperet under den valgte ressourcegruppe, der vises af enheden til at begynde med. Hvis **Tillad, at arbejdere angiver personlige filtre** er aktiveret, vil arbejderne kunne redigere denne værdi, ellers vil dette filter altid gælde, når denne enhedskonfiguration er aktiv.
- **Ressource** – Vælg en ressource, der skal anvendes som standardfilterkriterium for den liste over job, der vises for hver arbejder. Det er kun job, der er planlagt på den valgte ressource, der vises af enheden til at begynde med. Hvis **Tillad, at arbejdere angiver personlige filtre** er aktiveret, vil arbejderne kunne redigere denne værdi, ellers vil dette filter altid gælde, når denne enhedskonfiguration er aktiv.
- **Generér nummerplade** – Angiv denne indstilling til **Ja** for at generere en ny nummerplade, hver gang en arbejder bruger jobkortenheden til færdigmelding. Nummeret på nummerpladen genereres ud fra en nummerserie, der er konfigureret på siden **Parametre til lokationsstyring**. Når den er angivet til **Nej**, skal arbejderne angive en eksisterende nummerplade, når de er færdigmeldt.
- **Udskriv label** – Angiv denne indstilling til **Ja** for at udskrive en nummerpladelabel, når en arbejder bruger jobkortenheden til færdigmelding. Konfigurationen af labelen foretages i dokumentruten som beskrevet i [Dokumentrutelayout for nummerpladelabels](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Tildelte brugere

Brug oversigtspanelet **Tildelte brugere** til at knytte en eller flere systembrugere til den aktuelle enhedskonfiguration. Hver systembruger kan kun tildeles én jobenhedskonfiguration.

Når en enhed konfigureres, logges en IT-medarbejder typisk på Supply Chain Management ved hjælp af en systembrugerkonto. Derefter gælder den enhedskonfiguration for enheden, der er knyttet til den pågældende systembruger, så længe systembrugeren fortsat er logget på. Disse systembrugerkonti er normalt begrænset til kun at give adgang til siden med jobkortenheder, og ikke til andre dele af Supply Chain Management.

Når systembrugeren er logget på, og konfigurationen af jobenheden er indlæst, kan arbejderne logge på jobkortenheden ved hjælp af deres konto som *tidsregistreret arbejder* (f.eks. ved at scanne en stregkode på deres id-kort), så de kan starte nye job og foretage andre former for registreringer. Flere forskellige arbejdere kan logge ind og ud i løbet af dagen, mens den samme enhedskonfiguration fungerer på den pågældende maskine, fordi systembrugeren stadig er logget på Supply Chain Management resten af dagen.

Men som tidligere nævnt, når du bruger en enhedskonfiguration med indstillingen **Enkelt arbejder**, logger arbejderne som regel selv på Supply Chain Management ved hjælp af en systembruger, der er knyttet til deres egen konto som *tidsregistreret arbejder*, så de indlæser enhedskonfigurationen og logger på som arbejder på jobkortenheden på samme tid.

## <a name="additional-resources"></a>Yderligere ressourcer

[Færdigmeld fra jobkortenheden](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]