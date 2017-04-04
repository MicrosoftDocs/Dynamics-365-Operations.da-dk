---
title: Mobile kladdegodkendelser
description: "Mobilfunktionalitet i Microsoft Dynamics 365 for operationer, hvor business brugeren designe mobile oplevelser. Om avancerede scenarier platform også Lad os udviklere udvider mulighederne som de ønsker. Den mest effektive måde at lære nogle af de nye begreber på mobile er at gå gennem processen med at designe et par scenarier. Dette emne er beregnet til at give en praktisk tilgang til design af mobile scenarier ved at tage kreditor kladdegodkendelser for mobile som en use case. Dette emne skal hjælpe dig med at designe andre variationer af scenarier og kan også anvendes til andre scenarier, der ikke er relateret til kreditorfakturaer."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Mobile kladdegodkendelser

Mobilfunktionalitet i Microsoft Dynamics 365 for operationer, hvor business brugeren designe mobile oplevelser. Om avancerede scenarier platform også Lad os udviklere udvider mulighederne som de ønsker. Den mest effektive måde at lære nogle af de nye begreber på mobile er at gå gennem processen med at designe et par scenarier. Dette emne er beregnet til at give en praktisk tilgang til design af mobile scenarier ved at tage kreditor kladdegodkendelser for mobile som en use case. Dette emne skal hjælpe dig med at designe andre variationer af scenarier og kan også anvendes til andre scenarier, der ikke er relateret til kreditorfakturaer.

<a name="prerequisites"></a>Forudsætninger
-------------

| Forudsætning                                                                                            | Betegnelse                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobile håndbog forhånd læse                                                                                |(/ dynamics365/operationer/dev-itpro/mobil-apps / mobile-platform.md)                                                                                                  |
| Dynamics 365 til operationer                                                                             | Et miljø, der har Microsoft Dynamics 365 for operationer version 1611 opdager og Microsoft Dynamics for operationer platform update 3 (November 2016)                   |
| Installere hotfix KB 3204341.                                                                              | Arbejdsrutineoptager kan fejlagtigt optage to Luk kommandoer til rullelisten dialoger, dette er medtaget i Dynamics 365 for Operation platformsopdatering 3 (November 2016 opdatering) |
| Installere hotfix KB 3207800.                                                                              | Dette hotfix gør det muligt for vedhæftede filer kan ses på den mobile klient dette er medtaget i Dynamics 365 for Operation platformsopdatering 3 (November 2016 opdatering).           |
| Installere hotfix KB 3208224.                                                                              | Programkoden til programmet mobile kreditors faktura godkendelse dette er inkluderet i Microsoft Dynamics AX-programmet 7.0.1 (maj 2016).                          |
| En Android eller iOS eller en Windows-enhed, der er installeret til Dynamics 365 for operationer i mobil-app'en | Søge efter programmet i den relevante app butik.                                                                                                                     |

## <a name="introduction"></a>Introduktion
Mobile godkendelser for kreditorfakturaer kræver tre hotfixes, der er nævnt i afsnittet "Forudsætninger". Disse hotfixes give ikke et arbejdsområde til godkendelse af fakturaer. Hvis du vil vide, hvad er et arbejdsområde i forbindelse med mobile, læse mobile håndbogen, der er nævnt i afsnittet "Forudsætninger". Arbejdsområdet faktura godkendelser skal udformes. 

Hver organisation orchestrates og definerer dens forretningsprocessen for kreditorfakturaer forskelligt. Før du designer en mobilfunktioner til godkendelse af fakturaer for kreditor, skal du overveje følgende aspekter af forretningsprocessen. Ideen er at bruge disse datapunkter, der er så meget som muligt at optimere brugeroplevelsen på enheden.

-   Hvilke felter fra fakturahovedet vil brugeren se i mobilfunktioner og i hvilken rækkefølge?
-   Hvilke felter fra fakturaens linjer vil brugeren se i mobilfunktioner og i hvilken rækkefølge?
-   Hvor mange fakturalinjerne er der i en faktura? Anvende 80-20 reglen her, og Optimer til 80 procent.
-   Vil brugerne se regnskabsfordelinger (faktura coding) på den mobile enhed under anmeldelser? Hvis svaret på dette spørgsmål er Ja, skal du overveje følgende spørgsmål:
    -   Hvor mange regnskabsfordelinger (udvidede pris, moms, gebyrer, opdelinger osv.) er der for en fakturalinje? Igen gælde reglen 80-20.
    -   Fakturaerne, der også har regnskabsfordelinger på fakturahovedet? I så fald skal disse regnskabsfordelinger være tilgængelig på enheden?

> [!NOTE]
> Dette emne forklarer ikke, hvordan du redigere regnskabsfordelinger, fordi denne funktion ikke understøttes i øjeblikket for mobile scenarier.

-   Brugere skal se vedhæftede filer for fakturaen på enheden?

Designet af mobilfunktioner til godkendelse af fakturaer, afhænger af svarene på disse spørgsmål. Målet er at optimere brugeroplevelsen af forretningsprocessen på mobile i en organisation. I resten af dette emne ser vi på to scenario variationer, der er baseret på forskellige svar på de foregående spørgsmål. 

Som en generel vejledning, når du arbejder med mobile designer, Sørg for at "Udgiv" ændringer for at undgå at miste opdateringerne.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Designe en simpel faktura godkendelse scenario for Contoso
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenarieattribut</th>
<th>Besvar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hvilke felter fra fakturahovedet vil brugeren se i mobilfunktioner og i hvilken rækkefølge?</td>
<td><ol>
<li>Navn på kreditor</li>
<li>Fakturatotal</li>
<li>Fakturakonto</li>
<li>Fakturanummer</li>
<li>Fakturadato</li>
<li>Fakturabeskrivelse</li>
<li>Forfaldsdato</li>
<li>Fakturavaluta</li>
</ol></td>
</tr>
<tr class="even">
<td>Hvilke felter fra fakturaens linjer vil brugeren se i mobilfunktioner og i hvilken rækkefølge?</td>
<td><ol>
<li>Indkøbskategori</li>
<li>Mængde</li>
<li>Enhedspris</li>
<li>Linjenettobeløb</li>
<li>1099-beløb</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hvor mange fakturalinjerne er der i en faktura? Anvende 80-20 reglen her, og Optimer til 80 procent.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Vil brugerne se regnskabsfordelinger (faktura coding) på den mobile enhed under anmeldelser?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Hvor mange regnskabsfordelinger (udvidede pris, moms, gebyrer osv.) er der for en fakturalinje? Igen gælde reglen 80-20.</td>
<td>Varetotal: 2 moms: 0 gebyrer: 0</td>
</tr>
<tr class="even">
<td>Fakturaerne, der også har regnskabsfordelinger på fakturahovedet? I så fald skal disse regnskabsfordelinger være tilgængelig på enheden?</td>
<td>Bruges ikke</td>
</tr>
<tr class="odd">
<td>Brugere skal se vedhæftede filer for fakturaen på enheden?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Oprette arbejdsområdet

1.  Åbn Dynamics 365 for operationer i en webbrowser, og log på.
2.  Når du har logget, kan du tilføje **& mode = mobile** til URL-adressen, som vist i følgende eksempel og opdatere siden: https://&lt;yoururl&gt;/? cmp = usmf & mi = DefaultDashboard**& tilstand = mobile**
3.  Klik på den **indstillinger for** (gear)-knappen i øverste højre hjørne af siden, og klik derefter på **mobil-app'en**. Designeren af mobil-APP'en skal vises på samme måde som opgaven optageren vises.
4.  Klik på **Tilføj** til at oprette et nyt arbejdsområde. I dette eksempel skal du navngive arbejdsområdet **Mine godkendelser**.
5.  Angiv en beskrivelse.
6.  Vælg en farve i arbejdsområdet. Workspace-farve, der skal bruges til det overordnede format af mobilfunktioner for dette arbejdsområde.
7.  Vælg et ikon til arbejdsområdet.
8.  Klik på **gjort**
9.  Klik på **udgive arbejdsområde** til at gemme ændringerne

### <a name="vendor-invoices-assigned-to-me"></a>Kreditorfakturaer, der er tildelt til mig

Den første mobile side, du skal udforme er listen over fakturaer, der er tildelt til brugeren til gennemsyn. For at udforme denne mobil side, bruge den **VendMobileInvoiceAssignedToMeListPage** side i Dynamics 365 for operationer. Før du kan udføre denne procedure, Sørg for, at mindst en kreditorfaktura, der er tildelt til dig til korrektur, og at fakturalinjen har to fordelinger. Denne opsætning opfylder kravene i dette scenarie.

1.  I Dynamics 365 for operationer URL-adresse, skal du erstatte navnet på menupunktet med **VendMobileInvoiceAssignedToMeListPage** at åbne den mobile version af den **afventende kreditorfakturaer, der er tildelt til mig** listeside i den **gæld** modul. Afhængigt af antallet af fakturaer, du har i dit system tildelt til dig, viser denne side fakturaerne. Du kan finde en bestemt faktura, kan du bruge filteret til venstre. Men vi kræver ikke en bestemt faktura i dette eksempel. Vi kræver blot nogle faktura, der er tildelt til dig, som skal til at designe siden. De nye sider, der er tilgængelige er udviklet specifikt til udvikling af mobile scenarier for kreditorfakturaen. Derfor skal du bruge disse sider. URL-adressen skal ligne følgende URL-adresse, og når du har angivet den side, der er vist i illustrationen skal vises: https://&lt;yourURL&gt;/? cmp = usmf & mi =**VendMobileInvoiceAssignedToMeListPage**& mode = mobile [![side afventende kreditorfakturaer, der er tildelt mig](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Klik på den **indstillinger for** (gear)-knappen i øverste højre hjørne af siden, og klik derefter på **mobil-app'en**
3.  Vælg dit arbejdsområde, og klik på **Rediger**
4.  Klik på **Tilføj side** til at oprette den første mobile side.
5.  Angiv et navn, som **min kreditorfakturaer**, og en beskrivelse, som **kreditorfakturaer, der er tildelt til mig til gennemsyn**.
6.  Click **Done**.
7.  I mobile designer på den **felter**, og klik på **Vælg felter**. Kolonnerne på listesiden skal ligne den følgende illustration. [![Kolonner i de ventende kreditorfakturaer, der er tildelt til mig siden](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Tilføj de kolonner, der kræves fra siden, der skal vises for brugere på siden Mobil. Den rækkefølge, som du tilføjer, er den rækkefølge, hvori felterne vises for slutbrugeren. Den eneste måde at ændre rækkefølgen af felterne bliver ved igen at vælge alle felter. Baseret på kravene til dette scenario, er de følgende otte felter obligatoriske. Men nogle brugere kan overveje at otte felter for meget information på en mobil enhed. Derfor får du vist de vigtigste felter i mobile listevisningen. De resterende felter vises i visningen detaljer, som vi udformer senere. Nu skal tilføjer vi følgende felter. Klik på plustegnet (**+**) i disse kolonner, der skal føjes til siden.
    1.  Navn på kreditor
    2.  Fakturatotal
    3.  Fakturakonto
    4.  Fakturanummer
    5.  Fakturadato

    Når felterne er tilføjet, skal siden ligner den følgende illustration. [![Side, når der tilføjes felter](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Du skal også tilføje følgende kolonner nu, så vi kan senere aktivere arbejdsproceshandlinger.
    1.  Vis fuldført opgave
    2.  Vis Uddeleger opgaver
    3.  Vis tilbagekaldelse opgave
    4.  Vis Afvis opgave
    5.  Vis anmodning udfyldelsesopgave
    6.  Vis opgave igen

10. Klik på **gjort** at afslutte redigeringstilstand.
11. Klik på **tilbage** og derefter **gjort** at afslutte arbejdsområdet
12. Klik på **udgive arbejdsområde** at gemme dit arbejde.
13. Aktiver **skærm fakturatotal på ventende leverandør fakturaer liste** i formen med Kreditorparametre under **faktura**. Bemærk, at kun ved at aktivere denne parameter fakturatotaler beregnes der skal vises på den ventende listesiden for kreditorfakturaer. Dette er en ny funktion som en del af denne systemsoftwarefunktioner hot fix 3208224.

### <a name="vendor-invoice-details"></a>Leverandør af Fakturadetaljer

Hvis du vil designe siden faktura detaljer til mobile, kan du bruge den **VendMobileInvoiceHeaderDetails** side i Dynamics 365 for operationer. Bemærk, at afhængigt af antallet af fakturaer, du har på dit system, denne side viser de ældste faktura (faktura, der blev oprettet først). Du kan finde en bestemt faktura, kan du bruge filteret til venstre. Men vi kræver ikke en bestemt faktura i dette eksempel. Vi kræver blot nogle fakturadata, så vi kan designe siden. [![Arbejdsproces](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  I Dynamics 365 for operationer URL-adresse, skal du erstatte navnet på menupunktet med **VendMobileInvoiceHeaderDetails** til at åbne formen
2.  Åbne mobile designeren fra den **indstillinger for** (gear) knappen.
3.  Klik på den **Rediger** for at starte redigeringstilstand i arbejdsområdet.
4.  Vælg den ** min kreditorfakturaer ** side, du har oprettet tidligere, og klik derefter på **Rediger**.
5.  På den **felter**, og klik på den **gitter** kolonneoverskrift.
6.  Klik på **egenskaber**&gt;**Tilføj side**. **Bemærk:** når du klikker på den **gitter** overskrift og tilføje en side, relationen med de oplysninger, der siden er oprettet automatisk.
7.  Angiv en titel, som **fakturaoplysninger**, og en beskrivelse, som **se fakturahovedet og detaljer om**.
8.  Klik på **Vælg felter**. Bemærk, at den rækkefølge, som du føjer den rækkefølge, hvori felterne vises for slutbrugeren. Den eneste måde at ændre rækkefølgen af felterne bliver ved igen at vælge alle felter.
9.  Tilføj følgende felter fra hovedet, baseret på kravene til dette scenario:
    1.  Navn på kreditor
    2.  Fakturatotal
    3.  Fakturakonto
    4.  Fakturanummer
    5.  Fakturadato
    6.  Fakturabeskrivelse
    7.  Forfaldsdato
    8.  Fakturavaluta

10. Tilføj følgende felter fra gitteret linjer på siden:
    1.  Indkøbskategori
    2.  Mængde
    3.  Enhedspris
    4.  Linjenettobeløb
    5.  1099-beløb

11. Når du har tilføjet alle felter fra de forrige to trin, skal du klikke på **gjort**. Siden skal ligne den følgende illustration. [![Side, når der tilføjes felter](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Klik på **gjort** at afslutte redigeringstilstand.
13. Klik på **tilbage** og derefter **gjort** at afslutte arbejdsområdet
14. Klik på **udgive arbejdsområde** at gemme dit arbejde

### <a name="workflow-actions"></a>Arbejdsgangshandlinger

Brug til at føje arbejdsproceshandlinger til **VendMobileInvoiceHeaderDetails** side i Dynamics 365 for operationer. Erstat navnet på menupunktet i URL-adressen, hvis du vil åbne denne side, som du gjorde tidligere. Åbn derefter den mobile designer fra den **indstillinger** (gear) knappen. Følg disse trin for at føje arbejdsproceshandlinger på siden detaljer.

1.  Klik på den **Rediger** for at starte redigeringstilstand i arbejdsområdet.
2.  Vælg den **fakturaoplysninger** side, du har oprettet tidligere, og klik derefter på **Rediger**.
3.  På den **handlinger**, og klik på **Tilføj handling**.
4.  Angiv en titel for handling, som **Godkend**, og en beskrivelse, som **Godkend faktura**. Bemærk, at titlen handling, du angiver her, bliver navnet på den handling, der vises til brugeren i mobil-app'en.
5.  Click **Done**.
6.  Klik på **Vælg felter**.
7.  Gennemgå arbejdsgangen på den **VendMobileInvoiceHeaderDetails** side og udføre den handling, du ønsker at registrere. Sørg for, at du indtaster arbejdsgang kommentarer under denne proces, så et kommentarfelt er også inkluderet i mobilfunktioner.
8.  Når du har kørt arbejdsproceshandlingen, skal du klikke på **gjort** at fuldføre opgaven Vælg felter.
9.  Klik på **gjort** at afslutte redigeringstilstand.
10. Klik på **tilbage** og derefter **gjort** at afslutte arbejdsområdet
11. Klik på **udgive arbejdsområde** at gemme dit arbejde
12. Gentag trin 3 til 11 for at registrere de påkrævede arbejdsproceshandlinger. Bemærk, at det er et krav om fakturaer, der er tildelt til dig, der er i stand til at fremlægge de arbejdsganghandlinger, der skal designe til.
13. Åbn Notesblok eller Microsoft Visual Studio, og Indsæt følgende kode. Gem filen som en .js-fil. Denne kode gør to ting:
    1.  Skjuler de ekstra arbejdsproces-relaterede kolonner, som vi tidligere har tilføjet på siden Mobil. Vi har tilføjet disse kolonner, så app har disse oplysninger i sammenhæng og kan gøre det næste trin.
    2.  Baseret på det trin i arbejdsgangen, der er aktiv, gælder den logik, der viser kun disse handlinger.

Bemærk, at navnet på siderne og andre kontrolelementer i JS-koden skal være det samme fra arbejdsområdet.

1.  Funktion vigtigste (metadataService dataService cacheService, og $q) {returnere {appInit: funktion (appMetadata) {/ / Skjul indstillinger, som skal være til stede, men ikke synlige metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowAccept' {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowApprove', {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowReject' {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowDelegate', {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowRequestChange', {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowRecall', {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowComplete', {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowResubmit' { skjulte: SAND}); }, pageInit: funktion (pageMetadata, ' params ') {Hvis (pageMetadata.Name == 'Fakturadetaljer') {/ / Vis/Skjul arbejdsproceshandlinger, der er baseret på arbejdsgangen trin metadataService.configureAction ('Accepter' {synlige: true}); metadataService.configureAction ("Godkend" {synlige: SAND}); metadataService.configureAction ('Afvise' {synlige: SAND}); metadataService.configureAction ('Delegate' {synlige: SAND}); metadataService.configureAction (' Anmod om ændring ', {synlige: SAND}); metadataService.configureAction («Tilbagekaldelse» {synlige: SAND}); metadataService.configureAction ('Fuldført', {synlige: SAND}); metadataService.configureAction ('Send' {synlige: SAND});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  Overfør filen kode til arbejdsområdet ved at vælge den **Logic** under fanen
3.  Klik på **gjort** at afslutte redigeringstilstand.
4.  Klik på **tilbage** og derefter **gjort** at afslutte arbejdsområdet
5.  Klik på **udgive arbejdsområde** at gemme dit arbejde

### <a name="vendor-invoice-attachments"></a>Kreditors faktura vedhæftede filer

1.  Klik på den **indstillinger for** (gear)-knappen i øverste højre hjørne af siden, og klik derefter på **mobil-app'en**
2.  Klik på den **Rediger** for at starte redigeringstilstand i arbejdsområdet.
3.  Vælg den ** fakturaoplysninger ** side, du har oprettet tidligere, og klik derefter på **Rediger**.
4.  Angiv den **dokumentstyring** at **Ja** som vist nedenfor. **Bemærk:** Hvis der er ingen krav til at få vist vedhæftede filer på den mobile enhed, kan du lade denne indstilling sat til **ingen**, som er standardindstillingen.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Klik på **gjort** at afslutte redigeringstilstand.
7.  Klik på **tilbage** og derefter **gjort** at afslutte arbejdsområdet
8.  Klik på **udgive arbejdsområde** at gemme dit arbejde

### <a name="vendor-invoice-line-distributions"></a>Fordeling af kreditorfakturaer linje

Kravene til dette scenario bekræfte, at der bliver kun på linjeniveau fordelinger, og at en faktura har altid kun én linje. Da denne situation er simple, skal brugeroplevelse på den mobile enhed simple, at brugeren behøver at foretage detaljeopløftning på flere niveauer til at få vist fordelingerne. Kreditorfakturaer i Dynamics 365 for operationer omfatter mulighed for at vise alle fordelinger fra fakturahovedet. Denne oplevelse er, hvad vi har brug for til det bærbare scenarie. Derfor vil vi benytte de **VendMobileInvoiceAllDistributionTree** side til at designe denne del af det mobile scenario. 

> [!NOTE] 
> At kende kravene, der hjælper os med at afgøre, hvilken specifik side til at bruge, og hvordan nøjagtigt at optimere den mobile oplevelse for brugeren, når vi udvikler scenariet. I det andet scenario bruger vi en anden side til at få vist fordelingerne, da kravene til dette scenario er forskellige.

1.  Erstat navnet på menupunktet i URL-adressen, som du gjorde før. Den side, der vises, skal ligne følgende illustration. [![Alle fordelinger side](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Åbne mobile designeren fra den **indstillinger for** (gear) knappen.
3.  Klik på den **Rediger** for at starte redigeringstilstand i arbejdsområdet. **Bemærk:** kan du se, at to nye sider blev oprettet automatisk. Systemet opretter disse sider, da du tændte for dokumentstyring i forrige afsnit. Du kan ignorere disse nye sider.
4.  Klik på **Tilføj side**.
5.  Angiv en titel, som **Vis regnskab**, og en beskrivelse, som **Vis regnskab for fakturaen**.
6.  Click **Done**.
7.  På den **felter**, og klik på **Vælg felter**, og vælg følgende felter fra siden fordelinger, og klik derefter på **gjort**:
    1.  Beløb
    2.  Valuta
    3.  Finanskonto

> [!NOTE] 
> Vi ikke har valgt den **beskrivelse** kolonne fra gitteret fordelinger, fordi kravene til dette scenario bekræftet, at den udvidede pris er det eneste beløb, vil der være fordelinger for. Brugeren kan derfor ikke kræver et andet felt til at bestemme den beløbstype, som vedrører fordelingen. Men i det næste scenario vi **vil** du kan bruge disse oplysninger, fordi kravene til dette scenarie angiver, at øvrige beløbstyper har fordelinger (for eksempel moms).
8.  Klik på **gjort** at afslutte redigeringstilstand.
9.  Klik på **tilbage** og derefter **gjort** at afslutte arbejdsområdet
10. Klik på **udgive arbejdsområde** at gemme dit arbejde

**Bemærk:** de **Vis regnskab** siden er ikke aktuelt er knyttet til nogen af de mobile sider, vi har udviklet indtil videre. Da brugeren skal kunne navigere til den **Vis regnskab** siden fra den **fakturaoplysninger** side på den mobile enhed, skal vi give navigation fra den **fakturaoplysninger** side til den **Vis regnskab** side. Vi opretter denne navigation ved hjælp af yderligere logik via JavaScript.

1.  Åbn *.js-fil, du oprettede tidligere, og Tilføj de linjer, der er fremhævet i den følgende kode. Denne kode gør to ting:
    1.  Det hjælper med at sikre, at brugerne ikke kan navigere direkte fra arbejdsområdet til den **Vis regnskab** side.
    2.  Det fastlægger navigationsknappen fra den **fakturaoplysninger** side til den **Vis regnskab** side.

> [!NOTE] 
> Navnet på siderne og andre kontrolelementer i JS-koden skal være det samme fra arbejdsområdet.

1.  Funktion vigtigste (metadataService dataService cacheService, og $q) {returnere {appInit: funktion (appMetadata) {/ / Skjul indstillinger, som skal være til stede, men ikke synlige metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowAccept' {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowApprove', {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowReject' {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowDelegate', {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowRequestChange', {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowRecall', {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowComplete', {skjult: SAND}); metadataService.configureControl (' Mine--kreditorfakturaer, 'ShowResubmit' { skjulte: SAND}); Skjule sider er ikke tilgængelig for rod navigation metadataService.hideNavigation('View-accounting'); Link til at få vist regnskab metadataService.addLink ('-Fakturadetaljer, ' Vis regnskab ', ' View-regnskab-nav-control', 'Vis regnskab', true); }, pageInit: funktion (pageMetadata, ' params ') {Hvis (pageMetadata.Name == 'Fakturadetaljer') {/ / Vis/Skjul arbejdsproceshandlinger, der er baseret på arbejdsgangen trin metadataService.configureAction ('Accepter' {synlige: true}); metadataService.configureAction ("Godkend" {synlige: SAND}); metadataService.configureAction ('Afvise' {synlige: SAND}); metadataService.configureAction ('Delegate' {synlige: SAND}); metadataService.configureAction (' Anmod om ændring ', {synlige: SAND}); metadataService.configureAction («Tilbagekaldelse» {synlige: SAND}); metadataService.configureAction ('Fuldført', {synlige: SAND}); metadataService.configureAction ('Send' {synlige: SAND});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  Overfør filen kode til arbejdsområdet ved at vælge den **Logic** tab for at overskrive den forrige kode
3.  Klik på **gjort** at afslutte redigeringstilstand.
4.  Klik på **tilbage** og derefter **gjort** at afslutte arbejdsområdet
5.  Klik på **udgive arbejdsområde** at gemme dit arbejde

### <a name="validation"></a>Validering

Åbn programmet fra din mobilenhed, og oprette forbindelse til din Dynamics 365 for forekomst af operationer. Sørg for, at du logger på firmaet hvor kreditorfakturaer er tildelt til dig til korrektur. Du bør være i stand til at udføre følgende handlinger:

-   Se den **Mine godkendelser** arbejdsområde.
-   Dykke ind i den **Mine godkendelser** arbejdsområde og se de **min kreditorfakturaer** side.
-   Dykke ind i den **min kreditorfakturaer** side, og se en liste over fakturaer, der er tildelt til dig.
-   Dykke ind i en af fakturaerne, og se Fakturadetaljer hovedet og linjedetaljer.
-   Se et link til vedhæftede filer på siden detaljer, og bruge dette link for at gå til listen over vedhæftede filer og få vist de vedhæftede filer.
-   På siden detaljer kan du se et link til den **se regnskab** side og bruge dette link for at gå til siden fordelinger og få vist fordelingerne.
-   Klik på på siden oplysninger om den **handlinger** i menuen i bunden, og udføre handlinger for arbejdsprocesser, der gælder for trinnet i arbejdsprocessen.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Designe et scenario for godkendelse af komplekse faktura for Fabrikam
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenarieattribut</th>
<th>Besvar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hvilke felter fra fakturahovedet vil brugeren se i mobilfunktioner og i hvilken rækkefølge?</td>
<td><ol>
<li>Navn på kreditor</li>
<li>Fakturabeløb</li>
<li>Fakturakonto</li>
<li>Fakturanummer</li>
<li>Fakturadato</li>
<li>Fakturabeskrivelse</li>
<li>Forfaldsdato</li>
<li>Fakturavaluta</li>
</ol></td>
</tr>
<tr class="even">
<td>Hvilke felter fra fakturaens linjer vil brugeren se i mobilfunktioner og i hvilken rækkefølge?</td>
<td><ol>
<li>Indkøbskategori</li>
<li>Mængde</li>
<li>Enhedspris</li>
<li>Linjenettobeløb</li>
<li>1099-beløb</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hvor mange fakturalinjerne er der i en faktura? Anvende 80-20 reglen her, og Optimer til 80 procent.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Vil brugerne se regnskabsfordelinger (faktura coding) på den mobile enhed under anmeldelser?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Hvor mange regnskabsfordelinger (udvidede pris, moms, gebyrer osv.) er der for en fakturalinje? Igen gælde reglen 80-20.</td>
<td>Varetotal: 2 moms: tillæg 2: 2</td>
</tr>
<tr class="even">
<td>Fakturaerne, der også har regnskabsfordelinger på fakturahovedet? I så fald skal disse regnskabsfordelinger være tilgængelig på enheden?</td>
<td>Bruges ikke</td>
</tr>
<tr class="odd">
<td>Brugere skal se vedhæftede filer for fakturaen på enheden?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Opgave

Kan du gøre følgende variationer i scenario 1, baseret på kravene til scenario 2. Brug denne sektion som en øvelse, som du kan udføre for indlæringsformål.

1.  Fordi der forventes flere fakturalinjer i scenario 2, hjælper optimere brugeroplevelsen på den mobile enhed med følgende ændringer i designet:
    1.  I stedet for at få vist fakturalinjer på siden detaljer (som i eksempel 1), kan brugerne vælge at få vist linjer på en mobil side.
    2.  Da mere end én fakturalinje forventes i denne situation, hvis de **VendMobileInvoiceAllDistributionTree** side bruges til at designe siden fordelinger for mobile (som i eksempel 1), kan det være forvirrende for brugeren at koordinere linjer til fordeling. Derfor skal du bruge den **VendMobileInvoiceLineDistributionTree** side til at designe siden fordelinger.
    3.  Ideelt set bør blive vist fordelingerne i forbindelse med en fakturalinje i dette scenario. Sørg derfor for, at brugeren kan dykke ind i en linje for at se siden fordelinger. Bruge mulighed for link side til at oprette detaljeadgang, ligesom du gjorde for siderne sidehoved og detaljer i scenario 1.

2.  Da mere end en beløbstype forventes på fordelinger i scenario 2 (moms, gebyrer osv.), vil det være nyttigt at få vist beskrivelsen af beløbstypen. (Vi har udeladt disse oplysninger i scenario 1.)

## <a name="conclusion"></a>Konklusion
Den mobile platform og funktionerne i programmet kan du designe mobile scenarier, der er optimeret til en brugerbase i en organisation. Baseret på de eksempler, der findes i dette emne, kan du prøve andre variationer og oprette forskellige oplevelser, der opfylder specifikke behov.


