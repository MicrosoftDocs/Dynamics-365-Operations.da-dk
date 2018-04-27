---
title: Kreditorsamarbejde med eksterne kreditorer
description: "I dette emne forklares, hvordan indkøbere bruger kreditorportalen til at samarbejde med eksterne kreditorer for at udveksle data om indkøbsordrer og konsignationslager."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 961f0bbc4bb66536d953fa5103f98fcd6924adba
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-collaboration-with-external-vendors"></a>Kreditorsamarbejde med eksterne kreditorer

[!INCLUDE [banner](../includes/banner.md)]

Modulet **Kreditorsamarbejde** henvender sig til kreditorer, der ikke har EDI-integration (Electronic Data Interchange) med Microsoft Dynamics 365 for Finance and Operations. Kreditorer kan arbejde med indkøbsordrer (IO'er), fakturaer, konsignationslageroplysninger og tilbudsanmodninger, og de kan også få adgang til dele af deres kreditormasterdata. Dette emne beskriver, hvordan du kan samarbejde med eksterne kreditorer, der bruger kreditorsamarbejde-grænsefladen til at arbejde med indkøbsordrer, tilbudsanmodninger og konsignationslager. Det beskriver også, hvordan du aktiverer en bestemt kreditor til at bruge kreditorsamarbejde, og hvordan du definerer de oplysninger, som alle kreditorer får vist, når de svarer på en indkøbsordre.

Der er flere oplysninger om, hvad eksterne kreditorer kan gøre i grænsefladen for kreditorsamarbejde, i [Kreditorsamarbejde med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).

> [!NOTE]
> Oplysningerne om kreditorsamarbejde i dette emne gælder kun for den aktuelle version af Finance and Operations. I Microsoft Dynamics AX 7.0 (februar 2016) og Microsoft Dynamics AX-programversion 7.0.1 (maj 2016), samarbejder du med kreditorer ved hjælp af modulet **Kreditorportal**. Du kan finde flere oplysninger om modulet **Kreditorportal** under [Samarbejde med kreditorer ved hjælp af leverandørportalen](collaborate-vendors-vendor-portal.md).

Der er flere oplysninger om, hvordan kreditorerne kan bruge kreditorsamarbejde i faktureringsprocesser, i [Arbejdsområde for kreditorsamarbejdsfakturering](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md). Der er oplysninger om, hvordan du klargør nye brugere af kreditorsamarbejde, i [Administrere brugere af kreditorsamarbejde](manage-vendor-collaboration-users.md).

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Definition af de oplysninger, der vises for kreditorer, når de reagerer på indkøbsordrer

Når kreditorer besvarer en indkøbsordre, som du sender til dem, vises et af tre meddelelsesfelter, hvor de skal bekræfte, at de vil acceptere, afvise eller acceptere indkøbsordren med ændringer. Da de oplysninger, der skal vises for kreditoren på dette tidspunkt, kan være specifikke for din virksomhed, kan du angive den tekst, der vises i hver bekræftelsesmeddelelse. Teksten kan meddele kreditoren om de næste trin i processen, eller vilkår og betingelser.

Du kan angive den tekst, der vises i svar til indkøbsordrer, ved at gøre følgende:

1. På siden **Oplysninger til kreditorer, der reagerer på IO'er** skal du vælg svartypen og derefter vælge **Rediger**.
2. I feltet **Meddelelse med oplysninger** skal du angive de oplysninger, der skal vises til kreditorer i meddelelsesfeltet.

Hvis du skal tilføje meddelelser på mere end ét sprog, skal du oprette separate meddelelser og angive den relevante sprogkode for dem hver. Kreditoren får vist meddelelsen på det sprog, som han eller hun bruger.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>Angivelse af kreditorens samarbejdsindstillinger for en bestemt kreditor

En administrator konfigurerer de generelle indstillinger for kreditorsamarbejdet i Finance and Operations, f.eks. de sikkerhedsroller, der er tilgængelige for alle kreditorer, du samarbejder med. Der er dog også nogle indstillinger, som kan være forskellige for hver kreditorkonto. Du skal konfigurere disse indstillinger.

- Aktivér kreditorsamarbejde.
- Angiv, om kreditoren skal se prisoplysninger.

### <a name="enabling-vendor-collaboration"></a>Aktivering af kreditorsamarbejde

Før du kan oprette brugerkonti til en ekstern kreditor, skal du konfigurere en kreditorkonto, så kreditoren kan bruge kreditorsamarbejde. Indstil feltet **Aktivering af samarbejde** under fanen **Generelt** på siden **Kreditorer**. Følgende valgmuligheder er tilgængelige:

- **Aktiv (IO bekræftes automatisk)**– Indkøbsordrer bekræftes automatisk, hvis kreditoren accepterer dem uden ændringer.
- **Aktiv (IO bekræftes ikke automatisk)**– Din organisation skal manuelt bekræfte indkøbsordrer, når kreditoren har godkendt dem.

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Angivelse af, om kreditoren skal se prisoplysninger

Hvis du vil dele prisoplysninger for indkøbsordrer via grænsefladen for kreditorsamarbejde, skal du indstille **Priser/beløb på indkøbsordre** under fanen **Standardindstillinger for indkøbsordrer** for kreditorkontoen til **Ja**. Prisoplysningerne omfatter enhedspris, rabatter og gebyrer.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>Arbejde med indkøbsordrer, når der bruges kreditorsamarbejde

### <a name="sending-a-po-to-a-vendor"></a>Afsendelse af en indkøbsordre til en kreditor

Indkøbsordrer fremstilles i Finance and Operations. Når en indkøbsordre har statussen **Godkendt**, sender du den til kreditoren ved at vælge **Send til bekræftelse** på siden **Indkøbsordre**. Indkøbsordrens status ændres derefter til **Til eksternt gennemsyn**. Når Indkøbsordren er sendt, kan kreditoren se den på siden **Indkøbsordrer til gennemsyn** i grænsefladen for kreditorsamarbejde. Kreditoren kan derefter acceptere indkøbsordren, afvise den eller foreslå ændringer til den. Leverandøren kan også tilføje kommentarer for at kommunikere oplysninger, f.eks. ændringer af IO'en. Hvis du vil henlede kreditorens opmærksomhed på den nye IO, kan du også bruge udskriftsstyringssystemet til at sende IO'en via e-mail.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>Bekræftelse og accept af en indkøbsordre hos en kreditor

Når en kreditoren har accepteret en indkøbsordre, kan indkøbsordren bekræftes automatisk, eller den skal evt godkendes manuelt. Dette afhænger af, om feltet **Aktivering af samarbejde** er indstillet til **Aktiv (IO bekræftes automatisk)** eller **Aktiv (IO bekræftes ikke automatisk)** for kreditoren.

I nedenstående tabel viser den typiske udveksling af oplysninger, afhængigt af kreditorens svar, når du sender dem en indkøbsordre, der skal bekræftes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Kreditorsvar</th>
<th>Resultat</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>Kreditoren <strong>accepterer</strong> ordren, og Finance and Operations er konfigureret til automatisk at bekræfte IO'er, som kreditoren accepterer.</td>
<td>Status for ordren opdateres til <strong>Bekræftet</strong>. Hvis ordren af en eller anden årsag ikke kan opdateres, bliver kreditorens svar stadig registreret som <strong>Accepteret</strong>, men indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>. 

Den indkøbsordre, der er sendt til kreditoren og har status <strong>Til eksternt gennemsyn</strong>, opdateres med bekræftede leveringsdatoer på linjerne. Denne opdatering starter en ny version, der automatisk indstilles til <strong>Bekræftet</strong>-status. Når indkøbsordren er bekræftet, vises den i brugergrænsefladen for kreditorens samarbejde.</td>
</tr>
<tr class="odd">
<td>Kreditoren <strong>accepterer</strong> ordren, men Finance and Operations er ikke konfigureret til automatisk at bekræfte indkøbsordrer, som kreditoren accepterer.</td>
<td>Kreditorens svar registreres som <strong>Accepteret</strong>, men indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>.

Den indkøbsordre, der er sendt til kreditoren og har status <strong>Til eksternt gennemsyn</strong>, opdateres med bekræftede leveringsdatoer på linjerne. Denne opdatering starter en ny version, der automatisk indstilles til <strong>Til eksternt gennemsyn</strong>-status. Derefter kan du manuelt bekræfte indkøbsordren.</td>
</tr>
<tr class="even">
<td>Kreditoren <strong>afviser</strong> ordren.</td>
<td>Kreditorens svar registreres som <strong>Afvist</strong>, og indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>. Afvisningen modtages sammen med kreditorens note.</td>
</tr>
<tr class="odd">
<td>Kreditoren <strong>accepterer</strong> ordren <strong>med ændringer</strong>. Der foreslås ændringer på linjeniveau. Kreditoren kan acceptere eller afvise individuelle linjer. Her er nogle andre ændringer, kreditoren kan foreslå:
<ul>
<li>Ændre datoer eller antal.</li>
<li>Opdel linjer for forskellige leveringsdatoer eller antal.</li>
<li>Erstat en vare.</li>
</ul>
Kreditoren kan ikke ændre oplysninger om pris og gebyrer. Kreditoren kan dog foreslå disse ændringer ved hjælp af noter.</td>
<td>Kreditorens svar registreres som <strong>Accepteret med ændringer</strong>, og indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>. Statusangivelser viser de typer af ændringer kreditoren har foreslået. Oplysninger om automatisk forbrug af ændringerne kan du se i afsnittet &quot;Opdatere indkøbsordren, når en kreditor foreslår ændringer&quot; senere i dette emne. </td>
</tr>
</tbody>
</table>

Du kan bruge arbejdsområdet **Klargøring af indkøbsordrer** til at overvåge, hvilke IO'er kreditoren har reageret på. Arbejdsområdet indeholder to lister, der indeholder indkøbsordrer, der har status **Til eksternt gennemsyn**:

- Til eksternt gennemsyn kræver handling
- Til ekstern gennemgang, venter på svar fra leverandør

### <a name="changing-a-po"></a>Ændring af en indkøbsordre

Når du vil ændre en indkøbsordre, som en kreditor allerede er svaret på, skal du sende kreditoren en ny version af indkøbsordren. Den nye IO har et versionssuffiks, som angiver, at det er en ændret version af en tidligere sendt indkøbsordre. På siden **Historik over bekræftelse af kreditor for indkøbsordre** kan du og dine kreditorer registrere historikken for hver ordre. Den tidligere bekræftede version af en indkøbsordre forbliver på listen over bekræftede indkøbsordrer, indtil den nye indkøbsordre er bekræftet.

### <a name="canceling-a-po"></a>Annullering af en indkøbsordre

Når du annullerer en indkøbsordre, ændres statussen til **Godkendt**. Du skal sende indkøbsordren tilbage til leverandøren, så de kan bekræfte eller afvise annulleringen. Når annulleringen bekræftes, vises indkøbsordren på kreditorens liste over bekræftede IO'er som **Annulleret**.

### <a name="adding-attachments-to-a-po"></a>Tilføjelse af vedhæftede filer i en indkøbsordre

Du kan føje vedhæftede filer, f.eks. billeder og noter, til indkøbsordren ved at bruge dokumentstyringssystemet. Vedhæftede filer af typen **Ekstern** vil være synlige for kreditoren, når du sender indkøbsordren.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>Opdatering af en indkøbsordre, når en kreditor foreslår ændringer

Hvis en kreditor har reageret på en indkøbsordre og foreslået ændringer, er næste trin at behandle svaret.

I arbejdsområdet **Klargøring af indkøbsordrer** kan du på listen **Til eksternt gennemsyn** identificere indkøbsordrer, som en kreditor har accepteret med ændringer. Fra denne liste kan du også navigere til kreditorens svar.

En kreditor kan ændre følgende oplysninger i hovedet på et svar:
 
- Reference til kreditordokument
- Leveringsmåde
- Leveringsbetingelse
- Bekræftet leveringsdato

Kreditoren kan også tilføje en note eller vedhæftet fil.

På linjerne kan leverandøren ændre antallet og leveringsdatoerne, tilføje noter og vedhæftede filer, afvise en linje, erstatte en linje med et andet produkt, der angives som tekst, og opdele en linje i flere leverancer. Status for en linje varierer, afhængigt af de ændringer som kreditoren har foreslået:
    
- **Accepteret med ændringer**
- **Afvist**
- **Erstattet** – I dette tilfælde tilføjes en ekstra linje med statussen **Erstat**.
- **Bekræftet**
- **Opdel i tidsplan** – I dette tilfælde tilføjes ekstra linjer, der har statussen **Planlæg linjer**.

Hvis en linje ikke har nogen ændringer, angives linjestatus til **Accepteret**.

I svaret angiver linjestatusserne de typer af ændringer, som er foretaget af kreditoren. Desuden vises alle felter, der er blevet ændret, med fed skrift, så du let kan identificere ændringer.

Du kan opdatere en indkøbsordre ved at vælge **Udfør opdatering af indkøbsordre** på svaret eller én linje ad gangen. Et felt af typen **Er opdatering af indkøbsordre behandlet?** i hovedet og på linjerne viser, om systemet har behandlet hovedet eller linjerne for at opdatere indkøbsordren med eventuelle ændringer, der stammer fra svaret. Du kan kun køre handlingen **Udfør opdatering af indkøbsordre** én gang pr. hoved eller linje.

Ikke alle foreslåede ændringer kan opdateres på en indkøbsordre. Det er kun opdateringer i hovedet og opdateringer af datoer og antal på linjerne, der kan opdateres automatisk på indkøbsordren. Andre ændringer skal du manuelt opdatere på indkøbsordren. I dette tilfælde er værdien i feltet **Er opdatering af indkøbsordre behandlet?** **Manuel opdatering**. F.eks. hvis en kreditor foreslår, at en linje skal opdeles i en tidsplan, skal denne ændring angives manuelt.

Hver linje, der har statussen **Godkendt**, har en bekræftet leveringsdato. Når du kører handlingen **Udfør opdatering af indkøbsordre**, opdateres datoen på indkøbsordren. Noter og vedhæftede filer bliver ikke automatisk overført til den aktuelle indkøbsordre. Handelsaftaler bliver ikke vurderet på ny på linjerne i indkøbsordren, når du opdaterer den aktuelle indkøbsordre via handlingen **Udfør opdatering af indkøbsordre**.

## <a name="po-statuses-and-versions"></a>Status for indkøbsordren og versioner

Dette afsnit beskrives de forskellige statusser, som en indkøbsordre kan have op til det tidspunkt, hvor den bekræftes. Det beskriver også, når nye versioner af en indkøbsordre bliver gjort tilgængelig for kreditoren. Funktionaliteten varierer, afhængigt af om du bruger ændringsstyring for indkøbsordrer. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versioner og statusser, hvis du ikke bruger ændringsstyring

I nedenstående tabel vises et eksempel på ændringerne i status og version, som en indkøbsordre kan gennemgå.

| Handling | Status og version |
|--------|--------------------|
| Den første version af indkøbsordren oprettes i Finance and Operations. | Status er **Godkendt**. |
| Indløbsordren sendes til kreditoren. | En version registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**. |
| Kreditoren sender et **Accepteret med ændringer**-svar. | Status er stadig **Til eksternt gennemsyn**. |
| Du kan foretage nogle ændringer, som kreditoren har anmodet om. | Statussen ændres til **Godkendt**. |
| Du kan sende den nye version af indkøbsordren til kreditoren. | En ny version registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**. |
| Kreditoren accepterer den nye version af indkøbsordren. | Status er stadig **Til eksternt gennemsyn,** medmindre kreditorkontoen er konfigureret til automatisk at indstille indkøbsordrernes status til **Bekræftet**, når kreditoren accepterer dem. |

Kreditorer behøver ikke at bekræfte en indkøbsordre via grænsefladen for kreditorsamarbejde. De kan også sende en e-mail eller kommunikere deres accept af en IO via andre kanaler. Derefter kan du bekræfte ordren manuelt i Finance and Operations. I dette tilfælde får du en advarsel om, at ordren er blevet bekræftet, selv om der intet svar er fra kreditoren. Indkøbsordren vises derefter i oversigten over bekræftelser som en åben bekræftet ordre, som ikke har nogen svar. På dette tidspunkt har kreditoren ikke længere mulighed for at bekræfte eller afvise indkøbsordren.

> [!NOTE]
> Den version af indkøbsordren, der er tilgængelig for andre processer i Finance and Operations, er altid den nyeste version, selv om denne version endnu ikke er registreret i grænsefladen for kreditorsamarbejde.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versioner og statusser, hvis du bruger ændringsstyring

Hvis ændringsstyring er aktiveret for indkøbsordrer, gennemgår indkøbsordrerne en godkendelsesarbejdsgang for at nå frem til statussen **Godkendt**. Denne proces er ikke synlig for kreditoren.

I følgende tabel vises et eksempel på ændringerne i status og version, som en indkøbsordre kan gennemgå, når ændringsstyring er slået til. En version registreres, når indkøbsordren er godkendt, og ikke når indkøbsordren sendes til kreditoren eller bekræftes.

| Handling | Status og version |
|--------|--------------------|
| Den første version af indkøbsordren oprettes i Finance and Operations. | Status er **Kladde**. |
| Indkøbsordren sendes til godkendelsesprocessen. (Godkendelsesprocessen er en intern proces, som kreditoren ikke er involveret i). | Status ændres fra **Kladde** til **Til gennemsyn** til **Godkendelse**, hvis indkøbsordren ikke afvises under godkendelsesprocessen. Den godkendte indkøbsordre registreres som en version. | 
| Indløbsordren sendes til kreditoren. | Versionen registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**. |
| Du kan foretage de ændringer, som kreditoren har anmodet om, enten manuelt eller ved hjælp af handlingen **Udfør opdatering af indkøbsordre** i svaret for at opdatere indkøbsordren. | Statussen ændres tilbage til **Kladde**. |
| Indkøbsordren sendes igen til godkendelsesprocessen. | Status ændres fra **Kladde** til **Til gennemsyn** til **Godkendelse**, hvis indkøbsordren ikke afvises under godkendelsesprocessen. Systemet kan også konfigureres, så specifikke feltændringer ikke kræver fornyet godkendelse. I dette tilfælde ændres status først til **Kladde** og derefter opdateres automatisk til **Godkendt**. Den godkendte indkøbsordre registreres som en ny version. |
| Du kan sende den nye version af indkøbsordren til kreditoren. | Den nye version registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**. |
| Kreditoren godkender den nye version af IO'en. | Statussen ændres til **Bekræftet**. Det sker enten automatisk, eller når du modtager svar fra kreditoren og derefter bekræfter indkøbsordren. |

## <a name="sharing-information-about-consignment-inventory"></a>Deling af oplysninger om konsignationslager

Hvis du bruger konsignationslager, kan kreditorer bruge kreditorsamarbejde til at få vist oplysninger på de følgende sider:

- **Indkøbsordrer, der forbruger konsignationslager** – Indkøbsordrer for konsignationslager genereres, når ejerskabet af lageret ændres fra kreditoren til din virksomhed. En produktkvittering bogføres på samme tid. Disse konsignationsindkøbsordrer vises kun på siden **Indkøbsordrer, der forbruger konsignationslager**. De er ikke inkluderet på siden **Alle bekræftede indkøbsordrer** i modulet **Kreditorsamarbejde**.
- **Produkter, der er modtaget fra konsignationslager** – Denne side viser en liste over alle de transaktioner, hvor ejerskabet af produkter er blevet overført fra kreditoren til din virksomhed. Kreditorer kan bruge disse oplysninger til at fakturere kunden.
- **Disponibelt konsignationslager** – Denne side viser kreditorejede disponible konsignationslager, der er modtaget på dit lagersted.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Arbejde med tilbudsanmodninger, når du bruger kreditorsamarbejde

I dette afsnit beskrives interaktionerne mellem debitorer og kreditorer under tilbudsanmodningsprocessen. Det beskrives også, hvordan oplysningerne videresendes til kreditorer. En grundlæggende oversigt over understøttelse af tilbudsanmodningsprocessen finder du i [Tilbudsanmodninger](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Alternativer, vedhæftede filer, ændringer og returneringer

- **Alternativer** – I hovedet af en tilbudsanmodningssag kan du angive, at alternativer er tilladt for linjer med varer uden for katalog. Når alternativer er aktiveret, kan kreditorer tilføje en anden linje for hver linje, der blev anmodet om.
- **Vedhæftede filer** – Vedhæftede filer kan tilføjes på både hovedniveau og linjeniveau i en tilbudsanmodningssag. Vedhæftede sider kan klassificeres som enten interne eller eksterne. Interne vedhæftede filer kan kun vises på kundesiden, mens kreditorer kan få vist eksterne vedhæftede filer, når de sendes.

    Leverandører kan også tilføje vedhæftede filer i deres budsvar. Disse vedhæftede filer kan ses på kundesiden, når en kreditor har sendt budsvaret. Vedhæftede filer, som kreditorer tilføjer klassificeres altid som eksterne. Du kan åbne en vedhæftet fil, som en kreditor har sendt sammen med et bud, ved at vælge **Bud i vedhæftede filer** eller **Budlinjer i vedhæftede filer**.
    
    Når du vil åbne vedhæftede filer, der blev sendt sammen med tilbudsanmodningssagen, skal du bruge papirklips til dokumenthåndtering i svaret.

- **Ændringer** – Når en ændring er færdig, fjernes de eksisterende budsvar, så de kan erstattes af opdaterede værdier. Oplysninger som linjepris og antal fra tidligere budsvar kan ses via kladderne i tilbudsanmodningssagen.

    At gennemtvinge ændringsbehandling skal du på siden **Indkøbs- og forsyningsparametre** i oversigtspanelet **Tilbudsanmodning** indstille **Lås tilbudsanmodninger, når de er sendt** til **Ja**. (Denne indstilling er angivet og kræves til den offentlige sektor).

- **Returneringer** – Hvis en kreditor har sendt et bud, men flere eller ændrede oplysninger er nødvendige for tilbudsanmodningssagen, kan kunden returnere et bud til kreditoren. Dataene fra det bud, der blev sendt tidligere, bevares, og kreditoren kan foretage de ønskede ændringer uden at genstarte budprocessen.

## <a name="public-sector-extensions"></a>Udvidelser til den offentlige sektor

For den offentlige sektor muliggør de udvidede funktioner, at en tilbudsanmodningssag bliver sendt til kreditorer og publiceret. Når du udgiver en tilbudsanmodning, kan alle, der anmoder om oplysningerne, kan få vist det arbejde, der er i overensstemmelse med lovgivningen for den offentlige sektor. Alt arbejde, der er tilgængeligt, afspejles på listesiden **Åbne publicerede tilbudsanmodninger**, og de annullerede, ventende eller tildelte tilbudsanmodninger kan ses på listesiden **Lukkede publicerede tilbudsanmodninger**. Disse dokumenter kan også ses på et websted uden for Finance and Operations gennem integration med følgende dataenheder:

- Publicerede tilbudsanmodninger
- Linje i publicerede tilbudsanmodninger
- Vedhæftede filer i overskrifter til publicerede tilbudsanmodninger

Med disse enheder kan folk, der ikke er klargjorte brugere i Finance and Operations, men har anonym adgang til det eksterne websted, få vist tilgængeligt og lukket arbejdet. Desuden gør de udvidede funktioner i **Send og publicer** det muligt for den bruger, der konfigurerer parametre for tilbudsanmodningsprocessen, at definere en e-mailskabelon. Derefter, når indkøberen opretter tilbudsanmodningssagen, skal han eller hun vælge e-mailskabelonen for at sende de nødvendige oplysninger til kreditorerne i tilbudsanmodningssagen. 

Den bruger, der konfigurerer parametre for tilbudsanmodningsprocessen, kan oprette flere e-mailskabeloner. Disse e-mailskabeloner kan indeholde både statisk tekst og følgende erstatningstokens. Tokenerne erstattes med kontekstafhængige værdier, når der oprettes en e-mail.

- %RFQCase%
- %RFQCaseName%
- %bidType%
- %inviteOnly%
- %expiryDateTime%
- %requester%
- %requestingDepartment%
- %accountnum%
- %todaysdate%
- %createddate%

Hvis der kræves en ændring, og den sendes, når tilbudsanmodningen er sendt, vil tilbudsanmodningen blive sendt igen for alle kreditorer, der inviteret. Det publicerede dokument opdateres også på siden **Åbne publicerede tilbudsanmodninger**.

