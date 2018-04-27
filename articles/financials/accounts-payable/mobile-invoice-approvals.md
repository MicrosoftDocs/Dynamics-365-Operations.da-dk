---
title: Mobilfakturagodkendelser
description: Dette emne er beregnet til at give en praktisk tilgang til design af scenarier for mobilenheder i Dynamics 365 for Finance and Operations via en brugssag om godkendelser af kreditorfakturaer til mobilenheder.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a44e5d04edf327da2b3ba4676c8b823291801abe
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="mobile-invoice-approvals"></a>Mobilfakturagodkendelser

[!INCLUDE [banner](../includes/banner.md)]

Med mobilfunktionaliteten i Microsoft Dynamics 365 for Finance and Operations kan forretningsbruger designe oplevelser til mobilenheder. I avancerede scenarier kan udviklere også udvide funktionerne, som de ønsker. Den mest effektive måde at lære nogle af de nye begreber til mobilenheder på er ved at gennemgå processen med at designe et par scenarier. Dette emne er beregnet til at give en praktisk tilgang til design af scenarier for mobilenheder via en brugssag om godkendelser af kreditorfakturaer til mobilenheder. Dette emne kan hjælpe dig med at designe andre variationer af scenarier og kan også anvendes til andre scenarier, der ikke er relateret til kreditorfakturaer.

<a name="prerequisites"></a>Forudsætninger
-------------

| Forudsætning                                                                                            | Betegnelse                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Håndbog til forhåndslæsning om brug af mobilenhed                                                                                |[Mobilplatform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| Dynamics 365 for Finance and Operations                                                                             | Et miljø, der har Microsoft Dynamics 365 for Operations version 1611 og Microsoft Dynamics for Operations platformsopdatering 3 (november 2016)                   |
| Installer hotfix-KB 3204341.                                                                              | Arbejdsrutineoptager kan fejlagtigt optage to Luk-kommandoer til rullelistedialogbokse. Dette er medtaget i Dynamics 365 for Operations platformsopdatering 3 (november 2016 opdatering) |
| Installer hotfix-KB 3207800.                                                                              | Dette hotfix gør det muligt at se vedhæftede filer på mobilklienten. Dette er medtaget i Dynamics 365 for Operations platformsopdatering 3 (november 2016 opdatering).           |
| Installer hotfix-KB 3208224.                                                                              | Programkode til applikationen til godkendelse af kreditorfakturaer på mobilenheder. Dette er inkluderet i Microsoft Dynamics AX-programversion 7.0.1 (maj 2016).                          |
| En Android eller iOS eller en Windows-enhed, hvor mobilappen til Finance and Operations er installeret | Søg efter appen i den relevante appbutik.                                                                                                                     |

## <a name="introduction"></a>Introduktion
Godkendelser af kreditorfakturaer på mobilenheder kræver tre de hotfixes, der er nævnt i afsnittet "Forudsætninger". Disse hotfixes giver ikke et arbejdsområde til godkendelse af fakturaer. Hvis du vil vide, hvad er et arbejdsområde er i forbindelse med mobilenheder, skal du læse håndbogen til mobilenheder, der er nævnt i afsnittet "Forudsætninger". Arbejdsområdet til godkendelse af fakturaer skal udformes. 

Hver organisation organiserer og definerer sin forretningsproces for kreditorfakturaer på sin egen måde. Før du designer en mobiloplevelse til godkendelse af kreditorfakturaer, skal du overveje følgende aspekter af forretningsprocessen. Ideen er at bruge disse datapunkter så meget som muligt for at optimere brugeroplevelsen på enheden.

-   Hvilke felter fra fakturahovedet ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?
-   Hvilke felter fra fakturalinjer ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?
-   Hvor mange fakturalinjer er der i en faktura? Anvend 80-20-reglen her, og optimer til 80 procent.
-   Ønsker brugerne at se regnskabsfordelinger (fakturakodning) på mobilenheden under gennemsyn? Hvis svaret på dette spørgsmål er ja, skal du overveje følgende spørgsmål:
    -   Hvor mange regnskabsfordelinger (udvidet pris, moms, gebyrer, opdelinger osv.) er der for en fakturalinje? Igen anvend 80-20-reglen.
    -   Har fakturaerne også regnskabsfordelinger i fakturahovedet? I så fald, skal disse regnskabsfordelinger være tilgængelige på enheden?

> [!NOTE]
> Dette emne forklarer ikke, hvordan du redigerer regnskabsfordelinger, fordi denne funktion i øjeblikket ikke understøttes for mobilscenarier.

-   Ønsker brugere at se vedhæftede filer til fakturaen på enheden?

Hvilke mobilfunktioner der skal bruges til godkendelse af fakturaer, afhænger af svarene på disse spørgsmål. Målet er at optimere brugeroplevelsen af forretningsprocessen på mobilenhederne i en organisation. I resten af dette emne ser vi på to scenarievariationer, der er baseret på forskellige svar på de foregående spørgsmål. 

Som hovedregel når du arbejder med designeren til mobilenheder skal du sørge for at "publicere" ændringerne for at undgå at miste opdateringerne.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Designe et simpelt fakturagodkendelsesscenario til Contoso
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
<td>Hvilke felter fra fakturahovedet ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</td>
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
<td>Hvilke felter fra fakturalinjer ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</td>
<td><ol>
<li>Indkøbskategori</li>
<li>Mængde</li>
<li>Enhedspris</li>
<li>Linjenettobeløb</li>
<li>1099-beløb</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hvor mange fakturalinjer er der i en faktura? Anvend 80-20-reglen her, og optimer til 80 procent.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Ønsker brugerne at se regnskabsfordelinger (fakturakodning) på mobilenheden under gennemsyn?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Hvor mange regnskabsfordelinger (udvidet pris, moms, gebyrer osv.) er der for en fakturalinje? Igen anvend 80-20-reglen.</td>
<td>Udvidet pris: 2 Moms: 0 Gebyrer: 0</td>
</tr>
<tr class="even">
<td>Har fakturaerne også regnskabsfordelinger i fakturahovedet? I så fald, skal disse regnskabsfordelinger være tilgængelige på enheden?</td>
<td>Bruges ikke</td>
</tr>
<tr class="odd">
<td>Ønsker brugere at se vedhæftede filer til fakturaen på enheden?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Oprette arbejdsområdet

1.  Åbn Finance and Operations i en webbrowser, og log på.
2.  Når du har logget på, kan du tilføje **&mode=mobile** til URL-adressen som vist i følgende eksempel og opdatere siden: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**
3.  Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne af siden, og klik derefter på **Mobilapp**. Mobilappdesigneren skal vises på samme måde som Arbejdsrutineoptager vises.
4.  Klik på **Tilføj** for at oprette et nyt arbejdsområde. I dette eksempel skal du navngive arbejdsområdet **Mine godkendelser**.
5.  Angiv en beskrivelse.
6.  Vælg en farve til arbejdsområdet. Arbejdsområdets farve skal bruges til mobilfunktionernes overordnede udseende i dette arbejdsområde.
7.  Vælg et ikon til arbejdsområdet.
8.  Klik på **Udført**.
9.  Klik på **Publicer arbejdsområde** for at gemme ændringerne.

### <a name="vendor-invoices-assigned-to-me"></a>Kreditorfakturaer, der er tildelt til mig

Den første mobilenhedsside, du skal designe, er listen over de fakturaer, der er tildelt til brugeren til gennemsyn. For at udforme denne mobilenhedsside skal du bruge siden **VendMobileInvoiceAssignedToMeListPage** i Finance and Operations. Før du kan udføre denne procedure skal du sørge for, at mindst én kreditorfaktura er tildelt til dig til gennemsyn, og at fakturalinjen har to fordelinger. Denne opsætning opfylder kravene i dette scenarie.

1.  I URL-adressen til Finance and Operations skal du erstatte navnet på menupunktet med **VendMobileInvoiceAssignedToMeListPage** for at åbne mobilversionen af listesiden **Afventende kreditorfakturaer tildelt til mig** i **Kreditor**-modulet. Afhængigt af antallet af fakturaer, der er tildelt til dig i dit system, viser denne side fakturaerne. Når du vil finde en bestemt faktura, kan du bruge filteret til venstre. Men vi har ikke brug for en bestemt faktura i dette eksempel. Vi skal bare bruge en faktura, der er tildelt til dig, så du kan få adgang til at designe siden til mobilenheden. De nye sider, der er tilgængelige, er designet specifikt til udvikling af scenarier for kreditorfakturaer på mobilenheder. Derfor skal du bruge disse sider. URL-adressen skal ligne følgende URL-adresse, og når du har angivet den, skal den side, der er vist i illustrationen, vises: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Afventende kreditorfakturaer, der er tildelt mig](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne af siden, og klik derefter på **Mobilapp**.
3.  Vælg dit arbejdsområde, og klik på **Rediger**.
4.  Klik på **Tilføj side** for at oprette den første side til mobilenheden.
5.  Angiv et navn, f.eks. **Mine kreditorfakturaer**, og en beskrivelse, f.eks. **Kreditorfakturaer, der er tildelt til mig til gennemsyn**.
6.  Klik på **Udført**.
7.  I designeren til mobilenheder skal du under fanen **Felter** klikke på **Vælg felter**. Kolonnerne på listesiden skal ligne den følgende illustration. [![Kolonner i de afventende kreditorfakturaer, der er tildelt mig](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Tilføj de kolonner, der kræves, fra den listeside, der skal vises for brugere på mobilenhedssiden. Den rækkefølge, som du tilføjer i, er den rækkefølge, som felterne bliver vist i for slutbrugeren. Den eneste måde at ændre rækkefølgen af felterne er ved igen at vælge alle felter. Baseret på kravene til dette scenario er de følgende otte felter obligatoriske. Men nogle brugere vil mene, at otte felter er for mange oplysninger på en mobilenhed. Derfor vil vi kun vise de vigtigste felter i listevisningen til mobilenheder. De resterende felter vises i detaljevisningen, som vi udformer senere. Nu skal vi tilføje følgende felter. Klik på plustegnet (**+**) i disse kolonner for at føje dem til siden på mobilenheden.
    - Navn på kreditor
    - Fakturatotal
    - Fakturakonto
    - Fakturanummer
    - Fakturadato

    Når felterne er tilføjet, skal siden ligne følgende illustration. 
    [![Side, efter at der er tilføjet felter](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Du skal også tilføje følgende kolonner nu, så vi senere kan aktivere arbejdsganghandlinger.
    - Vis fuldført opgave
    - Vis delegeret opgave
    - Vis tilbagekaldelsesopgave
    - Vis afvist opgave
    - Vis anmodningsfuldførelsesopgave
    - Vis send igen-opgave

10. Klik på **Udført** for at afslutte redigeringstilstand.
11. Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet
12. Klik på **Publicer arbejdsområde** for at gemme dit arbejde.
13. Aktiver **Vis fakturatotal på ventende kreditorfakturaliste** i formen med kreditorparametre under **Faktura**. Bemærk, at kun hvis denne parameter aktiveres, beregnes fakturatotaler og vises på listesiden over ventende kreditorfakturaer. Dette er en ny funktion som en del af det nødvendige hot fix 3208224.

### <a name="vendor-invoice-details"></a>Detaljer i kreditorfaktura

Når du vil designe siden med fakturadetaljer til mobilenheder, skal du bruge siden **VendMobileInvoiceHeaderDetails** i Finance and Operations. Bemærk, at afhængigt af antallet af fakturaer, du har i dit system, viser denne side den ældste faktura (faktura, der blev oprettet først). Når du vil finde en bestemt faktura, kan du bruge filteret til venstre. Men vi har ikke brug for en bestemt faktura i dette eksempel. Vi skal blot bruge nogle fakturadata, så vi kan designe siden. [![Siden Arbejdsgang](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1. I URL-adressen til Finance and Operations skal du erstatte navnet på menupunktet med **VendMobileInvoiceHeaderDetails** for at åbne formen
2. Åbn designeren til mobilenheder fra knappen **Indstillinger** (tandhjulsymbolet).
3. Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.
4. Vælg siden <strong>Mine kreditorfakturaer**, som du oprettede tidligere, og klik derefter på **Rediger</strong>.
5. Under fanen **Felter** skal du klikke på kolonneoverskriften **Gitter**.
6. Klik på **Egenskaber** &gt; **Tilføj side**. **Bemærk:** Når du klikker på overskriften **Gitter** og tilføjer en side, oprettes relationen med detaljesiden automatisk.
7. Angiv en sidetitel, f.eks. **Fakturadetaljer** og en beskrivelse som **Vis fakturahoved og linjedetaljer**.
8. Klik på **Vælg felter**. Bemærk, at den rækkefølge, som du tilføjer i, er den rækkefølge, som felterne bliver vist i for slutbrugeren. Den eneste måde at ændre rækkefølgen af felterne er ved igen at vælge alle felter. 
9. Baseret på kravene til dette scenario skal du tilføje følgende felter fra hovedet:
   - Navn på kreditor
   - Fakturatotal
   - Fakturakonto
   - Fakturanummer
   - Fakturadato
   - Fakturabeskrivelse
   - Forfaldsdato
   - Fakturavaluta

10. Tilføj følgende felter fra gitterlinjerne på siden:
    - Indkøbskategori
    - Mængde
    - Enhedspris
    - Linjenettobeløb
    - 1099-beløb

11. Når alle felter fra de forrige to trin er tilføjet, skal du klikke på **Udført**. Siden skal ligne følgende illustration.
    [![Side, efter at der er tilføjet felter](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Klik på **Udført** for at afslutte redigeringstilstand.
13. Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet
14. Klik på **Publicer arbejdsområde** for at gemme dit arbejde.

### <a name="workflow-actions"></a>Arbejdsgangshandlinger

Brug siden **VendMobileInvoiceHeaderDetails** i Finance and Operations til at føje arbejdsgangshandlinger. Erstat navnet på menupunktet i URL-adressen, hvis du vil åbne denne side, som du gjorde tidligere. Åbn derefter designeren til mobilenheder fra knappen **Indstillinger** (tandhjulsymbolet). Følg disse trin for at føje arbejdsgangshandlinger til detaljesiden. Der skal være tildelt fakturaer til dig, der er i en tilstand, der kan gøre de arbejdsgangshandlinger, du skal udforme, tilgængelige for dig.

#### <a name="record-workflow-actions"></a>Registrere arbejdsgangshandlinger
1.  Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.
2.  Vælg siden **Fakturadetaljer**, som du oprettede tidligere, og klik derefter på **Rediger**.
3.  Klik på **Tilføj handling** under fanen **Handlinger**.
4.  Angiv en titel til handlingen, f.eks. **Godkend**, og en beskrivelse, f.eks. **Godkend faktura**. Bemærk, at den handlingstitel, du angiver her, bliver navnet på den handling, der vises for brugeren i mobilappen.
5.  Klik på **Udført**.
6.  Klik på **Vælg felter**.
7.  Gennemgå arbejdsgangen på siden **VendMobileInvoiceHeaderDetails**, og udfør den handling, du ønskede at registrere. Sørg for at indtaste kommentarer til arbejdsgangen under denne proces, så et kommentarfelt også er inkluderet i mobiloplevelsen.
8.  Når du har kørt arbejdsgangshandlingen, skal du klikke på **Udført** for at fuldføre opgaven Vælg felter.
9.  Klik på **Udført** for at afslutte redigeringstilstand.
10. Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet
11. Klik på **Publicer arbejdsområde** for at gemme dit arbejde.
12. Gentag de foregående trin for at registrere de påkrævede arbejdsgangshandlinger. 

#### <a name="create-a-js-file"></a>Oprette en .js-fil
1. Åbn Notesblok eller Microsoft Visual Studio, og indsæt følgende kode. Gem filen som en .js-fil. Denne kode gør følgende:
    - Den skjuler de ekstra arbejdsgang-relaterede kolonner, som vi tidligere tilføjede på listeside til mobilenheden. Vi tilføjede disse kolonner, så appen har disse oplysninger i den rette sammenhæng og kan udføre det næste trin.
    - Baseret på, hvilket trin i arbejdsgangen der er aktivt, anvender den regler, så kun disse handlinger viser.

> [!NOTE]
> Navnet på siderne og andre kontrolelementer i koden skal være det samme som navnene i arbejdsområdet.

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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

2.  Overfør kodefilen til arbejdsområdet ved at vælge fanen **Regel**
3.  Klik på **Udført** for at afslutte redigeringstilstand.
4.  Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet
5.  Klik på **Publicer arbejdsområde** for at gemme dit arbejde.

### <a name="vendor-invoice-attachments"></a>Vedhæftede filer i kreditorfakturaer

1. Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne af siden, og klik derefter på **Mobilapp**.
2. Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.
3. Vælg siden <strong>Fakturadetaljer**, som du oprettede tidligere, og klik derefter på **Rediger</strong>.
4. Indstil **Dokumentstyring** til **Ja** som vist nedenfor. **Bemærk:** Hvis der er ikke er krav om at vise vedhæftede filer på mobilenheden, kan du lade denne indstilling være sat til **Nej**, som er standardindstillingen.
   ![Dokumentstyring](./media/docmanagement-216x300.png)
5. Klik på **Udført** for at afslutte redigeringstilstand.
6. Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet
7. Klik på **Publicer arbejdsområde** for at gemme dit arbejde.

### <a name="vendor-invoice-line-distributions"></a>Fordelinger af kreditorfakturalinjer

Kravene til dette scenario bekræfter, at der kun skal være fordelinger på linjeniveau, og at en faktura har altid kun én linje. Da dette scenario er enkelt, skal brugeroplevelsen på mobilenheden også være så enkel, at brugeren ikke behøver at foretage detaljeopløftning på flere niveauer for at få vist fordelingerne. Kreditorfakturaer i Finance and Operations omfatter muligheden for at vise alle fordelinger fra fakturahovedet. Det er denne oplevelse, vi har brug for til scenariet på mobilenheden. Derfor benytter vi siden **VendMobileInvoiceAllDistributionTree** til at designe denne del af scenariet. 

> [!NOTE] 
> Når vi kender kravene, hjælper det os med at afgøre, hvilken specifik side vi skal bruge, og hvordan nøjagtigt vi skal optimere mobiloplevelsen for brugeren, når vi udformer scenariet. I det andet scenario bruger vi en anden side til at vise fordelingerne, da kravene til dette scenario er anderledes.

1.  I URL-adressen skal du erstatte navnet på menupunktet, som du gjorde tidligere. Den side, der vises, skal ligne følgende illustration.
[![Siden Alle fordelinger](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Åbn designeren til mobilenheder fra knappen **Indstillinger** (tandhjulsymbolet).
3.  Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet. **Bemærk:** Du kan se, at to nye sider blev oprettet automatisk. Systemet opretter disse sider, fordi du aktiverede dokumentstyring i forrige afsnit. Du kan ignorere disse nye sider.
4.  Klik på **Tilføj side**.
5.  Angiv en titel som **Vis regnskab** og en beskrivelse som **Vis regnskab for fakturaen**.
6.  Klik på **Udført**.
7.  Under fanen **Felter** skal du klikke på **Vælg felter** og vælge følgende felter fra fordelingssiden og derefter klikke på **Udført**:
    1.  Beløb
    2.  Valuta
    3.  Finanskonto

    > [!NOTE] 
    > Vi ikke har valgt kolonnen **Beskrivelse** fra fordelingsgitteret, fordi kravene til dette scenario bekræftede, at den udvidede pris er det eneste beløb, vil der være fordelinger for. Brugeren har derfor ikke brug et andet felt til at bestemme den beløbstype, som vedrører fordelingen. Men i det næste scenario **bruger** vi disse oplysninger, fordi kravene til dette scenarie angiver, at andre beløbstyper har fordelinger (for eksempel moms).
8.  Klik på **Udført** for at afslutte redigeringstilstand.
9.  Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet
10. Klik på **Publicer arbejdsområde** for at gemme dit arbejde.

> [!NOTE] 
> Siden **Vis regnskab** til mobilenheder er ikke aktuelt knyttet til nogen af de sider til mobilenheder, vi har udviklet indtil videre. Da brugeren skal kunne navigere til siden **Vis regnskab** fra siden **Fakturaoplysninger** på mobilenheden, skal vi sørge for navigation fra siden **Fakturadetaljer** til siden **Vis regnskab**. Vi opretter denne navigation ved hjælp af yderligere logik via JavaScript.

1.  Åbn den .js-fil, du oprettede tidligere, og tilføj de linjer, der er fremhævet i følgende kode. Denne kode gør to ting:
    1.  Det hjælper med at sikre, at brugerne ikke kan navigere direkte fra arbejdsområdet til siden **Vis regnskab**.
    2.  Det etablerer et navigationskontrolelement fra siden **Fakturadetaljer** til siden **Vis regnskab**.

> [!NOTE] 
> Navnet på siderne og andre kontrolelementer i koden skal være det samme som navnene i arbejdsområdet.

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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

2.  Overfør kodefilen til arbejdsområdett ved at vælge fanen **Regel** for at overskrive den tidligere kode
3.  Klik på **Udført** for at afslutte redigeringstilstand.
4.  Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet
5.  Klik på **Publicer arbejdsområde** for at gemme dit arbejde.

### <a name="validation"></a>Validering

Åbn appen fra din mobilenhed, og opret forbindelse til din Finance and Operations-forekomst. Sørg for at logge på det firma, hvor kreditorfakturaerne er tildelt til dig til gennemsyn. Du skal kunne udføre følgende handlinger:

-   Se arbejdsområdet **Mine godkendelser**.
-   Foretage detailudledning i arbejdsområdet **Mine godkendelser** og se siden **Mine kreditorfakturaer**.
-   Foretage detailudledning på siden **Mine kreditorfakturaer** og se listen over fakturaer, der er tildelt til dig.
-   Foretage detailudledning i en af fakturaerne, og se fakturahovedets detaljer og linjedetaljer.
-   På detaljesiden kan du se et link til vedhæftede filer, som du kan bruge til at gå til listen over vedhæftede filer for at få vist filerne.
-   På detaljesiden kan du se et link til siden **Vis regnskab**. Du kan bruge linket til at gå til siden over fordelinger og se fordelingerne.
-   På detaljesiden skal du klikke på menuen **Handlinger** forneden og udføre handlinger for arbejdsgange, der gælder for trinnet i arbejdsgangen.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Designe et komplekst fakturagodkendelsesscenario til Fabrikam
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
<td>Hvilke felter fra fakturahovedet ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</td>
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
<td>Hvilke felter fra fakturalinjer ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</td>
<td><ol>
<li>Indkøbskategori</li>
<li>Mængde</li>
<li>Enhedspris</li>
<li>Linjenettobeløb</li>
<li>1099-beløb</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hvor mange fakturalinjer er der i en faktura? Anvend 80-20-reglen her, og optimer til 80 procent.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Ønsker brugerne at se regnskabsfordelinger (fakturakodning) på mobilenheden under gennemsyn?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Hvor mange regnskabsfordelinger (udvidet pris, moms, gebyrer osv.) er der for en fakturalinje? Igen anvend 80-20-reglen.</td>
<td>Udvidet pris: 2 Moms: 2 Gebyrer: 2</td>
</tr>
<tr class="even">
<td>Har fakturaerne også regnskabsfordelinger i fakturahovedet? I så fald, skal disse regnskabsfordelinger være tilgængelige på enheden?</td>
<td>Bruges ikke</td>
</tr>
<tr class="odd">
<td>Ønsker brugere at se vedhæftede filer til fakturaen på enheden?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>Næste trin

Kan du udføre følgende variationer i scenario 1, baseret på kravene til scenario 2. Du kan bruge dette afsnit til at forbedre din mobilappoplevelse.

1.  Fordi der forventes flere fakturalinjer i scenario 2, hjælper følgende ændringer i designet med at optimere brugeroplevelsen på mobilenheden:
    1.  I stedet for at få vist fakturalinjer på siden med detaljer (som i eksempel 1), kan brugerne vælge at få vist linjer på en separat mobilenhedsside.
    2.  Da der forventes mere end én fakturalinje i dette scenario, hvis siden **VendMobileInvoiceAllDistributionTree** bruges til at designe fordelingssiden for mobilenheder (som i eksempel 1), kan det være forvirrende for brugeren at koordinere linjer til fordeling. Derfor skal du bruge siden **VendMobileInvoiceLineDistributionTree** til at designe fordelingssiden.
    3.  Ideelt set skal fordelingerne vises i forbindelse med en fakturalinje i dette scenario. Sørg derfor for, at brugeren kan dykke ned i en linje for at se fordelingssiden. Brug sidelinkfunktionen til at oprette detaljeadgang, ligesom du gjorde for hoved- og detaljesiderne i scenario 1.

2.  Da mere end én beløbstype forventes for fordelinger i scenario 2 (moms, gebyrer osv.), vil det være nyttigt at få vist beskrivelsen af beløbstypen. (Vi har udeladt disse oplysninger i scenario 1).





