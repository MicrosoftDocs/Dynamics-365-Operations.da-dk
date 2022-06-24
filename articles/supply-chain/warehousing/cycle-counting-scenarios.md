---
title: Eksempelscenarier for cyklusoptælling
description: Denne artikel indeholder en samling scenarier, der undersøger funktionerne til cyklusoptælling i Microsoft Dynamics 365 Supply Chain Management.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 90a3f132a96081b56ab60f5b0ba5cc328b820879
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899318"
---
# <a name="cycle-counting-example-scenarios"></a>Eksempelscenarier for cyklusoptælling

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en samling scenarier, der undersøger funktionerne til cyklusoptælling i Microsoft Dynamics 365 Supply Chain Management. Den beskriver først kravene til dit eksisterende Supply Chain Management-miljø. Derefter forklares det, hvordan du kan konfigurere cyklusoptælling, og alle cyklusoptællingsstadierne beskrives. Når du er færdig, vil du have en god forståelse af cyklusoptælling, herunder vejledt cyklusoptælling, skjult cyklusoptælling, spotcyklusoptælling, tærskler for cyklusantal og planer for cyklusantal.

## <a name="prerequisites"></a>Forudsætninger

### <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

De enkelte scenarier i denne artikel indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er leveret til Supply Chain Management. Hvis du vil bruge de værdier, der er angivet her, når du arbejder dig gennem scenarierne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed (firmaet) til **USMF**, før du går i gang.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>Slå understøttelse til for Warehouse Management-mobilappen

Hvis du vil bruge mobilappen Warehouse Management, skal funktionen *Brugerindstillinger, ikoner og trintitler til den nye lagerstedsapp* være aktiveret i systemet. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Brugerindstillinger, ikoner og trintitler til den nye lagerstedsapp* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Forberede demodata til scenarierne

Følg disse trin for at bekræfte, at alle de demodata, der kræves for scenarierne, er tilgængelige i USMF-firmaet i systemet. Opret poster eller værdier, der mangler.

1. Gå til **Lokationsstyring \> Konfiguration \> Arbejder**.
1. Vælg **Julia Funderburk** i listeruden.
1. Vælg rækken med følgende værdier i oversigtspanelet **Brugere**. Hvis der ikke allerede findes en række med disse værdier, skal du oprette den.

    - **Bruger-id:** *61*
    - **Brugernavn:** *WH61*
    - **Standardlagersted:** *61*
    - **Menunavn:** *Hoved*

1. Angiv følgende værdier for bruger *61* i oversigtspanelet **Arbejde**, hvis de ikke allerede er angivet:

    - **Er en cyklusoptællingssupervisor:** *Nej*
    - **Grænse for maks. procent:** *0*
    - **Grænse for maks. antal:** *0*
    - **Grænse for maks. værdi:** *0*

1. Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdspuljer**.
1. Arbejdspuljer bruges til at udskille lagerstedsarbejdet baseret på typen af arbejde (i dette tilfælde cyklusoptællingsarbejde). Kontrollér, at der findes en post med følgende indstillinger:

    - **Arbejdspulje-id:** *CycleCount*
    - **Beskrivelse:** *Cyklusantal*

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg den post, der hedder *Cyklusantal*, i listeruden. Hvis der ikke findes en eksisterende post med dette navn, skal du oprette den. Bekræft eller angiv følgende værdier for posten:

    - **Navn på menupunkt:** *Cyklusantal*
    - **Titel:** *Vejledt cyklusoptælling*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Ja*
    - **Ledet af:** *Systembaseret* (Denne værdi angiver, at Supply Chain Management tildeler et arbejds-id for cyklusoptælling til arbejderen).
    - **Vis lagerstatus:** *Ja*

1. Vælg **Cyklusoptælling** i handlingsruden.
1. Bekræft eller angiv følgende værdier i dialogboksen **Cyklusoptælling for mobilenhed**:

    - **Vis varenummer:** *Ja*
    - **Vis id:** *Ja*
    - **Antal forsøg:** *1*

1. Vælg **OK** for at lukke dialogboksen.
1. Vælg den post, der hedder *Blind cyklusoptælling*, i listeruden. Hvis der ikke findes en eksisterende post med dette navn, skal du oprette den. Bekræft eller angiv følgende værdier for posten:

    - **Navn på menupunkt:** *Blind cyklusoptælling*
    - **Titel:** *Blind cyklusoptælling*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Ja*
    - **Ledet af:** *Gruppering af cyklusoptælling* (Denne værdi angiver, at arbejderen kan gruppere id'er for cyklusoptællingsarbejde, der er specifikke for en lokation, zone eller arbejdspulje).

1. Vælg **Cyklusoptælling** i handlingsruden.
1. Bekræft eller angiv følgende værdier i dialogboksen **Cyklusoptælling for mobilenhed**:

    - **Vis varenummer:** *Nej*
    - **Vis id:** *Nej*
    - **Antal forsøg:** *0*

1. Vælg **OK** for at lukke dialogboksen.
1. Vælg den post, der hedder *Spotoptælling*, i listeruden. Hvis der ikke findes en eksisterende post med dette navn, skal du oprette den. Bekræft eller angiv følgende værdier for posten:

    - **Navn på menupunkt:** *Spotoptælling*
    - **Titel:** *Spotoptælling*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Nej*
    - **Arbejdsoprettelsesproces:** *Spotcyklusoptælling* Denne værdi angiver, at arbejderen til enhver tid kan tælle elementerne på en lagerlokation uden at oprette cyklusoptællingsarbejde. For at udføre spotcyklusoptælling på en lokation angiver arbejderen lokalitets-id'et.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Vælg den post, der hedder *Lager*, i listeruden. Hvis der ikke findes en eksisterende post med dette navn, skal du oprette den. Bekræft, at følgende menupunkter for cyklusoptælling vises i kolonnen **Menustruktur**:

    - Cyklusoptælling
    - Blind cyklusoptælling
    - Spotoptælling

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
1. På fanen **Cyklusoptælling** kan du angive følgende værdier:

    - **Standardreguleringstype for cyklusoptælling:** *Cyklusantal* (I dette felt angives den kladdetype, der bogføres, når cyklusoptælling er udført).
    - **Standardarbejdsklasse-id for cyklusoptælling:** *CCount* (I dette felt angives den arbejdsklasse, der bruges til cyklusoptælling).
    - **Standardarbejdsprioritet for cyklusoptælling:** *50* (I dette felt angives den prioritet, som arbejdet med cyklusoptælling har i forhold til andre arbejdstyper på lagerstedet. Du kan øge prioriteten af cyklusoptællingsarbejde ved at angive et tal, der er lavere end det tal, der er angivet, for andre typer arbejde.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Lager \> Reguleringstyper**.
1. På siden **Reguleringstyper** kan du oprette koder for de forskellige ind- og ud-reguleringer, der kan forekomme. Bekræft, at der findes en post med følgende indstillinger:

    - **Lagerreguleringstype:** *Cyklusantal*
    - **Beskrivelse:** *Cyklusantal*
    - **Navn:** *ICnt*

1. Gå til **Lagerstedsstyring \> Konfiguration \> Opsætning af lagersted \> Lagersteder**.
1. Vælg lagersted *61* i listeruden. Hvis der ikke findes en eksisterende post med dette navn, skal du oprette den.
1. I oversigtspanelet **Lagersted** kan du angive følgende værdier:

    - **Brug proces til lagerstyringssted:** *Ja* (Denne værdi aktiverer lagerstedet i processer for lagerstedsstyring).
    - **Tillad flytning af id under cyklusoptælling:** *Ja* (Denne værdi giver arbejdere mulighed for at flytte id'er under en cyklusoptælling).

## <a name="scenario-1-guided-cycle-counting"></a>Scenarie 1: Vejledt cyklusoptælling

Før der kan forekomme en vejledt cyklusoptælling, skal du oprette noget arbejde. Dette arbejde vil føre den tildelte person gennem lagerstedet, fra lokation til lokation, for at udføre de optællinger, der er konfigureret i arbejdet.

### <a name="create-cycle-counting-work-for-scenario-1"></a>Oprette cyklusoptællingsarbejde for scenarie 1

Benyt følgende fremgangsmåde for at oprette cyklusoptællingsarbejde for varens lokation *01A02R2S2B* (BULK-06) på lagersted *61*.

1. Gå til **Lagerstedsstyring \> Cyklusoptælling \> Cyklusoptællingsarbejde efter lokation**.
1. Angiv feltet **Id for arbejdspulje** til *CycleCount* i dialogboksen **Opret cyklusoptællingsarbejde efter lokation**.
1. I oversigtspanelet **Medtagne poster** skal du vælge **Filtrer**.
1. Benyt følgende fremgangsmåde under fanen **Område** i dialogboksen med forespørgselseditoren:

    - Angiv feltet **Kriterie** til *61* for den række, hvor feltet **Felt** er angivet til *Lagersted*.
    - Angiv feltet **Kriterie** til *01A02R2S2B* for den række, hvor feltet **Felt** er angivet til *Lokation*.

1. Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.
1. Vælg **OK** for at lukke dialogboksen **Opret cyklusoptællingsarbejde efter lokation**.

    Når processen til oprettelse af arbejde er fuldført, vises der en meddelelse i handlingscenteret.

1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.
1. Find det nyoprettede arbejde ved at angive et filter i kolonnen **Arbejdspulje-id** for at finde poster med værdien *CycleCount*.

### <a name="do-cycle-counting-work-for-scenario-1"></a>Udføre cyklusoptællingsarbejde for scenarie 1

Når du har oprettet cyklusoptællingsarbejdet, skal du udføre arbejdet med at optælle varer på et lagersted og derefter bruge en mobilenhed til at angive resultaterne i Supply Chain Management. Følg disse trin for at udføre arbejdet med cyklusoptælling i mobilappen Warehouse Management.

1. Log på Warehouse Management-mobilappen som den arbejdsbruger, du konfigurerede i afsnittet [Forberede demodata for scenarier](#prepare-demo-data) tidligere i denne artikel. I eksemplet i denne artikel hedder brugeren *Julia Funderburk* og er oprettet for lagersted *61*. (USMF-demodataene giver dig mulighed for at logge på som denne arbejdsbruger ved at angive *61* som bruger-id og *1* som adgangskode).
1. I hovedmenuen skal du vælge **Lager**.
1. Vælg **Vejledt cyklusoptælling** i menuen **Lager**.
1. Vælg feltet **Antal**, indtast *9* på det numeriske tastatur, og vælg derefter **OK** (knappen med markeringen).
1. Systemet forventede, at du indtastede en optælling på 10 styk for denne vare, denne lokation og dette id-nummer. Derfor bliver du bedt om at tælle igen. Vælg feltet **Antal**, indtast *9* på det numeriske tastatur igen, og vælg derefter **OK** (knappen med markeringen). I andet forsøg accepteres din optælling.

    > [!NOTE]
    > Da systemet registrerede en difference mellem det forventede disponible antal og det antal, du angav, blev du bedt om at tælle endnu en gang, fordi feltet **Antal forsøg** er angivet til *1* for menupunktet **Vejledt cyklusoptælling** på mobilenheden. Du blev ført til et bestemt varenummer og id-nummer, fordi både indstillingen **Vis varenummer** og indstillingen **Vis id-nummer** er angivet til *Ja* for menupunktet på mobilenheden.

1. Vælg knappen **OK** (markeringssymbol).

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>Gennemse forskellene i cyklusoptælling for scenarie 1

Følg disse trin for at gennemse forskellene i cyklusoptællingen.

1. Vende tilbage til Supply Chain Management.
1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.
1. Find og vælg det cyklusoptællingsarbejde, du så på tidligere. (Angiv for eksempel et filter i kolonnen **Arbejdspulje-id** for at finde poster med værdien *CycleCount*). Bemærk, at feltet **Arbejdsstatus** for dette arbejde nu er angivet til *Afventer gennemsyn*.

    > [!NOTE]
    > For den arbejdsbrugerkonto, du har brugt til optællingsarbejdet, angives indstillingen **Cyklusoptællingssupervisor** til *Nej*, og felterne **Grænse for maks. procent**, **Grænse for maks. antal** og **Grænse for maks. værdi** angives alle til *0* (nul). Derfor skal alle forskelle i optælling, som denne bruger rapporterer, godkendes manuelt, og feltet **Arbejdsstatus** for det relaterede arbejde er angivet til *Afventer gennemsyn*. Hvis den optalte værdi var inden for afvigelsesgrænsen (som angivet i felterne **Grænse for maks. procent** eller **Grænse for maks. antal** på siden **Arbejdsbrugere**), eller hvis indstillingen **Cyklusoptællingssupervisor** var angivet til *Ja* for brugeren, ville arbejdet automatisk være blevet lukket.

1. I handlingsruden skal du gå til fanen **Arbejde** og vælge **Cyklusoptælling**.
1. Vælg **Accepter antal** i handlingsruden.

    Forskellen bogføres ved hjælp af standardoptællingskladden, og der oprettes en ny arbejdsordre.

1. På siden **Cyklusoptællingstransaktioner** i handlingsruden skal du vælge **Afledt arbejde** for at finde det arbejde, der er oprettet for den godkendte forskel.

## <a name="scenario-2-blind-cycle-counting"></a>Scenarie 2: Blind cyklusoptælling

Dette scenarie kræver, at scenarie 1 allerede er fuldført i systemet.

### <a name="create-cycle-counting-work-for-scenario-2"></a>Oprette cyklusoptællingsarbejde for scenarie 2

Før der kan forekomme en blind cyklusoptælling, skal du oprette noget arbejde. Benyt følgende fremgangsmåde for at oprette cyklusoptællingsarbejde for varens lokation *01A02R2S2B* (BULK-06) på lagersted *61*.

1. Gå til **Lagerstedsstyring \> Cyklusoptælling \> Cyklusoptællingsarbejde efter vare**.
1. Angiv feltet **Id for arbejdspulje** til *CycleCount* i dialogboksen **Opret cyklusoptællingsarbejde efter vare**.
1. I oversigtspanelet **Medtagne poster** skal du vælge **Filtrer**.
1. I dialogboksen for forespørgselseditor skal du gå til fanen **Område** og tilføje tre rækker, der har følgende indstillinger:

    - Række 1:

        - **Tabel:** *Varer*
        - **Felt:** *Varenummer*
        - **Kriterier:** *L0101*

    - Række 2:

        - **Tabel:** *Lagerdimensioner*
        - **Felt:** *Lagersted*
        - **Afgrænsning:** *61*

    - Række 3:

        - **Tabel:** *Lagerdimensioner*
        - **Felt:** *Lokation*
        - **Kriterier:** *01A02R2S2B*

1. Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.
1. Vælg **OK** for at lukke dialogboksen **Opret cyklusoptællingsarbejde efter vare**.

    Når du er færdig med at oprette arbejdet, modtager du en meddelelse med oplysninger.

### <a name="do-cycle-counting-work-for-scenario-2"></a>Udføre cyklusoptællingsarbejde for scenarie 2

Når du er færdig med cyklusoptællingsarbejdet, skal du følge disse trin for at udføre arbejdet i mobilappen Warehouse Management.

1. Log på Warehouse Management-mobilappen som den arbejdsbruger, du konfigurerede i afsnittet [Forberede demodata for scenarier](#prepare-demo-data) tidligere i denne artikel. I eksemplet i denne artikel hedder brugeren *Julia Funderburk* og er oprettet for lagersted *61*. (USMF-demodataene giver dig mulighed for at logge på som denne arbejdsbruger ved at angive *61* som bruger-id og *1* som adgangskode).
1. I hovedmenuen skal du vælge **Lager**.
1. Vælg **Blind cyklusoptælling** i menuen **Lager**.
1. Vælg feltet **Zone-id**, angiv *BULK06*, og vælg derefter **OK** (knappen med markeringen).
1. Vælg feltet **Vare**, angiv *L0101*, og vælg derefter **OK** (knappen med markeringen).
1. Vælg feltet **Id**, angiv *LP\_BULK\_06\_01*, og vælg derefter **OK** (knappen med markeringen).
1. Vælg feltet **Antal**, angiv *10*, og vælg derefter **OK** (knappen med markeringen).

    > [!NOTE]
    > Selvom systemet har registreret en difference mellem det forventede disponible antal og det antal, du har scannet, blev du bedt om at tælle endnu en gang, fordi feltet **Antal forsøg** er angivet til *0* (nul) for menupunktet **Blind cyklusoptælling** på mobilenheden. Du blev bedt om at scanne varenummeret og id-nummeret, fordi både indstillingen **Vis varenummer** og indstillingen **Vis id-nummer** er angivet til *Nej* for menupunktet på mobilenheden.

1. Vælg knappen **OK** (markeringssymbol).

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>Gennemse forskellene i cyklusoptælling for scenarie 2

Følg disse trin for at gennemse forskellene i cyklusoptællingen.

1. Vende tilbage til Supply Chain Management.
1. Gå til **Lagerstedsstyring \> Fælles \> Arbejde \> Ventende gennemsyn af cyklusoptællingsarbejde**.
1. I handlingsruden skal du gå til fanen **Arbejde** og vælge **Cyklusoptælling**.
1. Vælg **Afvis antal** i handlingsruden.

    Da optællingsdifferencen blev afvist, er arbejdet lukket.

## <a name="scenario-3-spot-cycle-counting"></a>Scenarie 3: Spotcyklusoptælling

I den registrerede varebeholdning kan du se, at der er et disponibelt antal af vare *L0101* på lokation *01A02R2S2B*. Lagerarbejderen er på lokation *01A02R2S1B*. Selvom denne lokation bør være tom, er den fuld. Lagerarbejderen udfører derfor med det samme en spotoptælling for denne lokation.

### <a name="do-cycle-counting-work-for-scenario-3"></a>Udføre cyklusoptællingsarbejde for scenarie 3

Følg disse trin for at udføre arbejdet med cyklusoptælling i mobilappen Warehouse Management.

1. Log på Warehouse Management-mobilappen som den arbejdsbruger, du konfigurerede i afsnittet [Forberede demodata for scenarier](#prepare-demo-data) tidligere i denne artikel. I eksemplet i denne artikel hedder brugeren *Julia Funderburk* og er oprettet for lagersted *61*. (USMF-demodataene giver dig mulighed for at logge på som denne arbejdsbruger ved at angive *61* som bruger-id og *1* som adgangskode).
1. I hovedmenuen skal du vælge **Lager**.
1. Vælg **Spotoptælling** i menuen **Lager**.
1. Vælg feltet **Lokation**, angiv *01A02R2S1B*, og vælg derefter **OK** (knappen med markeringen).

    Det registreres, at lokationen er tom i Supply Chain Management.

1. Vælg **Tilføj LP eller vare**.
1. Vælg feltet **Vare**, angiv *L0101*, og vælg derefter **OK** (knappen med markeringen).
1. Vælg feltet **Id**, angiv *LP\_BULK\_06\_01*, og vælg derefter **OK** (knappen med markeringen).
1. Vælg feltet **Antal**, angiv *9*, og vælg derefter **OK** (knappen med markeringen).

    Da det registreres, at det angivne id allerede er tilgængeligt på en anden placering i Supply Chain Management, flyttes dette id til den aktuelle lokation. Systemet beder dig derfor om at bekræfte flytningen.

1. Vælg knappen **OK** (markeringssymbol).

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>Gennemse forskellene i cyklusoptælling for scenarie 3

Følg disse trin for at gennemse resultaterne af optællingen.

1. Vende tilbage til Supply Chain Management.
1. Gå til **Lagerstedsstyring \> Fælles \> Arbejdsdetaljer**.
1. Marker afkrydsningsfeltet **Vis lukket** øverst i gitteret.
1. Angiv filteret for kolonnen **Arbejdsordretype** til *Lagerbevægelse*.

    Systemet registrerede automatisk denne optælling som en lagerbevægelse. Denne bevægelse er tilladt, da indstillingen **Tillad flytning af id under cyklusoptælling** er angivet til *Ja* for lagersted *61* på siden **Lagersted**.

## <a name="scenario-4-define-cycle-count-thresholds"></a>Scenarie 4: Definere grænser for cyklusantal

Du kan blandt andet oprette cyklusoptællingsarbejde ved at bruge grænser. En grænse for cyklusoptælling angiver mængden eller den procentvise grænse for lagervarer. Cyklusoptællingsarbejde oprettes automatisk, når grænsen er nået.

For eksempel er der 60 varer på en lokalitet, der har en grænse på 40 for cyklusoptælling. Under en salgsordrepostering plukkes 25 varer fra lokaliteten og lægges på en midlertidig lokalitet. Da antallet af nye elementer på 35 er mindre end tærskelantallet, oprettes cyklusoptællingsarbejdet automatisk for lokationen.

Hvis du vil konfigurere en grænse for cyklusoptælling, skal du gøre følgende.

1. Gå til **Lagerstedsstyring \> Opsætning \> Cyklusoptælling \> Cyklusoptællingsgrænser**.
1. Vælg **Ny** i handlingsruden for at oprette en grænse, og angiv følgende værdier for den:

    - **Id for cyklusoptællingsgrænse:** *L0101*
    - **Beskrivelse:** *Grænse L0101*
    - **Grænseantal:** *2*
    - **Enhed:** *Styk*
    - **Kapacitetsgrænse baseret på procentdel:** *0,00*
    - **Type af grænse for cyklusoptælling:** *Antal*
    - **Hurtig behandling af cyklusoptælling:** *Ja*
    - **Dage mellem cyklusoptællinger:** *1*
    - **Arbejdspulje-id:** *CycleCount*

1. Vælg **Vælg varer** i handlingsruden.
1. Gå til dialogboksen til forespørgselseditoren under fanen **Område**, og find den række, hvor feltet **Felt** er indstillet til *Varenummer*. Angiv feltet **Kriterier** for denne række til *L0101*.
1. Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.

    Du har nu defineret en grænse for cyklusoptælling for vare *L0101*.

Der oprettes nu cyklusoptælling for vare *L0101* på en vilkårlig lokation, hvis det disponible antal er mindre end 2, og hvis datoen for den seneste cyklusoptælling for lokationen ikke er dags dato.

## <a name="scenario-5-define-cycle-count-plans"></a>Scenarie 5: Definere planer for cyklusoptælling

Du kan bruge planer for cyklusoptælling til at automatisere oprettelsen af cyklusoptællingsarbejde. Du kan konfigurere de enkelte cyklusoptællingsplaner med specifikke vare- og lokationsforespørgsler. Når batchjobbet køres, oprettes der cyklusoptællingsarbejde for alle lokationer, der opfylder kriterierne for varen og lokationen (op til det maksimale antal optællinger, der er angivet for planen). Når der oprettes cyklusoptællingsarbejde, indeholder optællingsarbejdslinjen oplysninger om, hvilken lokalitet der skal optælles. Den disponible beholdning, der er tilknyttet denne lokalitet, er ikke blokeret. Den er derfor tilgængelig til reservation og udgående behandling, også selvom der findes åbent optællingsarbejde.

Hvis du vil konfigurere en plan for cyklusoptælling, skal du gøre følgende.

1. Gå til **Lagerstedsstyring \> Opsætning \> Cyklusoptælling \> Cyklusoptællingsplaner**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret, og angiv derefter følgende værdier for den:

    - **Id for cyklusoptællingsplan:** *BULK06*
    - **Beskrivelse:** *Optælling af lokation for BULK06*
    - **Arbejdspulje-id:** *CycleCount*
    - **Maks. antal cyklusoptællinger:** *10*
    - **Dage mellem cyklusoptællinger:** *10*
    - **Tomme lokationer:** *Udeluk tomme*
    - **Arbejdsskabelon:** Lad feltet stå tomt.

1. Vælg **Vælg lokationer** i handlingsruden.
1. Der vises en standarddialogboks med forespørgselseditoren. Gå til fanen **Område**, tilføj en række, og angiv følgende værdier for den:

    - **Tabel:** *Lokationer*
    - **Felt:** *Zone-id*
    - **Kriterier:** *BULK06*

1. Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.
1. Vælg **Udfør behandling af cyklusoptællingsplan** i handlingsruden.
1. I dialogboksen **Cyklusoptællingsplaner** skal du gå til oversigtspanelet **Kør i baggrunden** og angive indstillingen **Batchbehandling** til *Ja*.
1. Vælg **Gentagelse**.
1. I dialogboksen **Definer gentagelse** skal du konfigurere batchjobbet, så det starter med det samme og kører én gang hvert minut, og så der ikke er en slutdato.
1. Vælg **OK** for at lukke dialogboksen **Definer gentagelse**.
1. Vælg **OK** for at lukke dialogboksen **Cyklusoptællingsplaner**.

    Der vises en meddelelse om, at jobbet er blevet føjet til batchkøen.

1. Gå til **Lagerstedsstyring \> Almindelig \> Planlægning af cyklusoptælling**. Planen starter med det samme, og der oprettes optællingsarbejde. Da optællingsarbejdet ikke er fuldført, er feltet **Status** angivet til *I gang*. Efter ét minut ændres værdien i kolonnen **Antal cyklusser i alt** til *1*.

    > [!NOTE]
    > Cyklusoptællingsarbejdet oprettes ikke, hvis antallet af dage siden sidste cyklusoptælling er mindre end den værdi, du har angivet for feltet **Dage mellem cyklusoptælling** for cyklusoptællingsplanen. Hvis for eksempel feltet **Dage mellem cyklusoptællinger** er indstillet til *5*, oprettes der cyklusoptællingsarbejde, hver gang der er gået fem dage. Men cyklusoptællingsarbejdet imidlertid behandles på dag 3, oprettes det næste cyklusoptællingsarbejde, fem dage efter at den seneste cyklusoptælling blev behandling, nemlig på dag 8.

1. Vælg **Arbejde** i handlingsruden for at få vist det optællingsarbejde, der er oprettet.
