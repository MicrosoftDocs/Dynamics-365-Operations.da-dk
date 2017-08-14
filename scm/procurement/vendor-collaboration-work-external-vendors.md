---
title: "Leverandørsamarbejde med eksterne leverandører"
description: "I dette emne forklares, hvordan indkøbere bruger leverandørportalen til at samarbejde med eksterne kreditorer for at udveksle data om indkøbsordrer og konsignationslager."
author: BibiSp
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: cbd099403f48b502ca74bcb38ae12decedb8f2da
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="vendor-collaboration-with-external-vendors"></a>Leverandørsamarbejde med eksterne leverandører

[!include[banner](../includes/banner.md)]


I dette emne forklares, hvordan indkøbere bruger leverandørportalen til at samarbejde med eksterne kreditorer for at udveksle data om indkøbsordrer og konsignationslager.

Modulet **Kreditorsamarbejde** henvender sig til kreditorer, der ikke har EDI-integration (Electronic Data Interchange) med Microsoft Dynamics 365 for Finance and Operations. Det gør det muligt for kreditorer at arbejde med oplysninger om købsordrer, fakturaer og konsignationslager. Dette emne beskriver, hvordan du kan samarbejde med eksterne kreditorer, der bruger kreditorsamarbejde-grænsefladen til at arbejde med indkøbsordrer og konsignationslager. Det beskriver også, hvordan du aktiverer en bestemt kreditor til at bruge kreditorsamarbejde, og hvordan du definerer de oplysninger, som alle kreditorer får vist, når de svarer på en indkøbsordre. Der er flere oplysninger om, hvad eksterne kreditorer kan gøre i grænsefladen for kreditorsamarbejde, i [Kreditorsamarbejde med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Der er flere oplysninger om, hvordan kreditorerne kan bruge kreditorsamarbejde i faktureringsprocesser, i [Arbejdsområde for kreditorsamarbejdsfakturering](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Der er oplysninger om, hvordan du klargør nye brugere af kreditorsamarbejde, i [Administrere brugere af kreditorsamarbejde](manage-vendor-collaboration-users.md).

Der er flere oplysninger om, hvordan kreditorerne kan bruge kreditorsamarbejde i faktureringsprocesser, i [Arbejdsområde for kreditorsamarbejdsfakturering](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). 

Der er oplysninger om, hvordan du klargør nye brugere af kreditorsamarbejde, i [Administrere brugere af kreditorsamarbejde](manage-vendor-collaboration-users.md).

## <a name="define-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Definere de oplysninger, der vises for kreditorer, når de reagerer på indkøbsordrer
Når kreditorer besvarer en indkøbsordre, som du sender til dem, vises en meddelelsesboks, hvor de skal bekræfte, at de vil acceptere, afvise eller acceptere indkøbsordren med ændringer. Da de oplysninger, der skal vises for kreditoren på dette tidspunkt, kan være specifikke for din virksomhed, kan du angive den tekst, der vises på hver af de tre bekræftelsesmeddelelser. Teksten kan meddele kreditoren om de næste trin i processen, eller vilkår og betingelser.  

Sådan angives den tekst, der vises i svar til indkøbsordrer:

1.  Åbn siden **Oplysninger til kreditorer, der reagerer på IO'er**.
2.  Vælg én af svartyperne:
3.  Klik på **Rediger**.
4.  Angiv de oplysninger, som kreditorer skal se, i feltet **Meddelelse med oplysninger**.

Hvis du skal tilføje meddelelser på mere end ét sprog, skal du oprette separate meddelelser og angive de relevante sprogkoder for dem hver. Kreditoren får vist meddelelsen på det sprog, som kreditoren bruger.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Angive kreditorens samarbejdsindstillinger for en bestemt kreditor
De generelle indstillinger for kreditorsamarbejde i Finance and Operations er konfigureret af en administrator. For eksempel vil en administrator bestemme, hvilke sikkerhedsroller der er tilgængelige for alle de kreditorer, du samarbejder med. Der er også nogle indstillinger, som kan være forskellige for hver kreditorkonto, og du skal angive disse:
-   Aktivér kreditorsamarbejde.
-   Beslut, om kreditoren skal se oplysninger om pris.

### <a name="enable-vendor-collaboration"></a>Aktivere kreditorsamarbejde

Før du kan oprette brugerkonti til en ekstern kreditor, skal du konfigurere en kreditorkonto for at tillade dem at bruge kreditorsamarbejde. For at gøre dette skal du angive feltet **Aktivering af samarbejde** til aktivt under fanen **Generelt** på siden **Kreditorer**. Der er to indstillinger, du kan vælge:

-   **Aktiv (IO bekræftes automatisk)**- Indkøbsordrer bekræftes automatisk, når kreditoren accepterer dem uden ændringer.
-   **Aktiv (IO bekræftes ikke automatisk)**- Indkøbsordrer skal bekræftes manuelt af din organisation, når kreditoren har godkendt dem.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Beslut, om kreditoren skal se oplysninger om pris.

Hvis du vil dele prisoplysninger såsom enhedspris, rabatter og gebyrer via brugergrænsefladen for samarbejde, skal du angive **Priser/beløb på indkøbsordre** til **Ja** på kreditorkontoen. Denne indstilling er tilgængelig under fanen **Standardindstillinger for indkøbsordrer**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Arbejde med indkøbsordrer, når du bruger kreditorsamarbejde
### <a name="sending-a-po-to-the-vendor"></a>Afsendelse af en indkøbsordre til kreditoren

Indkøbsordrer fremstilles i Finance and Operations. Når indkøbsordren har statussen **Godkendt**, sender du den til kreditoren ved hjælp af handlingen **Send til bekræftelse** på siden **Indkøbsordre**. Indkøbsordrens status ændres til **Til eksternt gennemsyn**. Når Indkøbsordren er sendt, kan kreditoren se den på siden **Indkøbsordrer til gennemsyn** i grænsefladen for kreditorsamarbejde. Kreditoren kan derefter acceptere ordren, afvise den eller foreslå ændringer til den. Leverandøren kan også tilføje kommentarer for at kommunikere oplysninger, f.eks. ændringer af IO'en. Hvis du vil henlede kreditorens opmærksomhed på den nye IO, kan du også bruge udskriftsstyringssystemet til at sende IO'en via e-mail.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Bekræftelse og accept af indkøbsordre hos kreditoren

Når en kreditor har accepteret en indkøbsordre, kan indkøbsordren bekræftes automatisk, eller det kan være nødvendigt at bekræfte den manuelt. Dette afhænger af, om feltet **Aktivering af kreditor** er angivet til **Aktiv (IO bekræftes automatisk)** eller til **Aktiv (IO bekræftes ikke automatisk)** for kreditoren.  

I nedenstående tabel viser den typiske udveksling af oplysninger, afhængigt af hvordan kreditoren reagerer, når du sender dem en indkøbsordre, der skal bekræftes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Kreditorsvar</strong></td>
<td><strong>Resultat</strong></td>
</tr>
<tr class="even">
<td>Kreditoren <strong>accepterer</strong> ordren. Finance and Operations er konfigureret til automatisk at bekræfte indkøbsordrer, når kreditoren accepterer.</td>

<td>Status for ordren opdateres til <strong>Bekræftet</strong>. Hvis noget forhindrer, at ordren opdateres, bliver kreditorens svar stadig registreret som <strong>Accepteret</strong>, men indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>. 

Den indkøbsordre, der er sendt til kreditoren, og som har **Til eksternt gennemsyn** som status, opdateres med bekræftede leveringsdatoer på linjerne. Opdateringen starter en ny version, der opdateres automatisk til **Bekræftet**-status. Når indkøbsordren er bekræftet, vises den i brugergrænsefladen for kreditorens samarbejde.</td>
</tr>
<tr class="odd">
<td>Kreditoren <strong>accepterer</strong> ordren. Finance and Operations er ikke konfigureret til automatisk at bekræfte indkøbsordrer, når kreditoren accepterer.</td>
<td>Kreditorens svar registreres som <strong>Accepteret</strong>, men indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>.

Den indkøbsordre, der er sendt til kreditoren, og som er i **Til eksternt gennemsyn**-status, opdateres med bekræftede leveringsdatoer på linjerne. Opdateringen starter en ny version, der angives som **Til eksternt gennemsyn**. Du kan derefter manuelt bekræfte indkøbsordren.</td>

</tr>
<tr class="even">
<td>Kreditoren <strong>afviser</strong> ordren.</td>
<td>Kreditorens svar registreres som <strong>Afvist</strong>, og indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>. Afvisningen modtages sammen med kreditorens note.</td>
</tr>
<tr class="odd">
<td>Leverandøren <strong>accepterer ordren med ændringer</strong>. Der foreslås ændringer på linjeniveau. Det er muligt at acceptere eller afvise individuelle linjer. Andre mulige ændringer omfatter:
<ul>
<li>Ændre datoer eller antal.</li>
<li>Opdele linjer for forskellige leveringsdatoer eller antal.</li>
<li>Udskifte en vare.</li>
</ul>
Oplysninger om pris og gebyrer kan ikke ændres af kreditoren. Forslag til ændringer af disse kan foretages ved hjælp af noter.</td>
<td>Kreditorens svar registreres som <strong>Accepteret med ændringer</strong>, og indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>. Statusangivelser viser, hvilke typer ændringer leverandøren har foreslået. Oplysninger om automatisk forbrug af ændringerne kan du se i afsnittet nedenfor om at opdatere indkøbsordren, når en kreditor foreslår ændringer. </td>
</tr>
</tbody>
</table>

Du kan bruge **Indkøbsordre** arbejdsområdet **Forberedelse** til at overvåge, hvilke IO'er kreditoren har reageret på. Arbejdsområdet indeholder to lister, der indeholder indkøbsordrer med status **Til eksternt gennemsyn**:

-   Til eksternt gennemsyn kræver handling.
-   Til eksternt gennemsyn, der venter på svar fra kreditor.

### <a name="changing-a-po"></a>Ændring af en indkøbsordre

Når du vil ændre en indkøbsordre, der allerede er svaret på, skal du sende en ny version af indkøbsordren til kreditoren. Den nye IO har et versionssuffiks, som angiver, at det er en ændret version af en tidligere kommunikeret indkøbsordre. På siden **Historik over bekræftelse af kreditor for indkøbsordre** kan du og dine kreditorer registrere historikken for hver ordre. Den tidligere bekræftede version af en indkøbsordre forbliver på listen over bekræftede indkøbsordrer, indtil den nye indkøbsordre er bekræftet.

### <a name="cancelling-a-po"></a>Annullering af en indkøbsordre

Når du annullerer en indkøbsordre, ændres statussen til **Godkendt**. Du skal sende IO'en tilbage til kreditoren via kreditorportalen, så kreditoren kan bekræfte eller afvise annulleringen. Når annulleringen bekræftes, vises indkøbsordren på kreditorens liste over bekræftede indkøbsordrer som **Annulleret**.

### <a name="adding-attachments-to-a-po"></a>Tilføjelse af vedhæftede filer i en indkøbsordre

Du kan føje vedhæftede filer, f.eks. billeder og noter, til indkøbsordren ved at bruge dokumentstyringssystemet. Vedhæftede filer af typen **Ekstern** vil være synlige for kreditoren, når du sender indkøbsordren.

## <a name="update-the-po-when-a-vendor-suggests-changes"></a>Opdatere indkøbsordren, når en kreditor foreslår ændringer
Når en kreditor har reageret på indkøbsordren og foreslået ændringer, er næste trin at behandle svaret.
I arbejdsområdet **Klargøring af indkøbsordrer** kan du på listen Til eksternt gennemsyn kræver handling identificere en indkøbsordre, som en kreditor har svaret på med 'accepteret med ændringer'. På listen Til eksternt gennemsyn kræver handling kan du også navigere til kreditorens svar. En kreditor kan ændre følgende oplysninger i hovedet på et svar.
 
-   Reference til kreditordokument
-   Leveringsmåde
-   Leveringsbetingelse
-   Bekræftet leveringsdato

Kreditoren kan også tilføje en note eller vedhæftet fil

På linjerne kan kreditoren ændre antallet og leveringsdatoerne, tilføje noter og vedhæftede filer, afvise en linje, erstatte en linje med et andet produkt, der indtastes som tekst, og opdele en linje i flere leverancer. Afhængigt af hvilke ændringer, der foreslås af kreditoren, vil linjestatus have forskellige statusser:
    
-   **Accepteret med ændringer**
-   **Afvist**
-   **Erstattet** I dette tilfælde tilføjes en ekstra linje med statussen **Erstat**.
-   **Bekræftet** Opdel i tidsplan. I dette tilfælde tilføjes ekstra linjer, der har statussen **Planlæg linjer**.

Hvis en linje ikke har nogen ændringer, angives linjestatus til **Accepteret**.

I svaret kan du se de tidligere nævnte linjestatusser, der angiver typerne af ændringer, som er foretaget af kreditoren. Desuden vises alle ændrede felter med fed skrift, så du let kan identificere ændringer.

Du kan opdatere en indkøbsordre ved at klikke på handlingen **Udfør opdatering af indkøbsordre** på svaret eller én linje ad gangen. En indikator, **Er opdatering af indkøbsordre behandlet?**, i hovedet og på linjerne viser, om systemet har behandlet hovedet eller linjerne for at opdatere indkøbsordren med eventuelle ændringer, der stammer fra svaret. Du kan kun køre processen **Udfør opdatering af indkøbsordre** én gang pr. hoved eller linje.

Ikke alle foreslåede ændringer kan opdateres på en indkøbsordre. Det er kun opdateringer i hovedet og opdateringer af datoer og antal på linjerne, der kan opdateres automatisk på indkøbsordren. Andre ændringer skal du manuelt opdatere på indkøbsordren. I dette tilfælde viser indikatoren **Er opdatering af indkøbsordre behandlet?** **Manuel opdatering**. Når en kreditor foreslår at opdele en linje i en tidsplan, skal denne ændring for eksempel håndteres manuelt.

En linje med statussen **Accepteret** har en bekræftet leveringsdato, der skal opdateres på indkøbsordren, når du afvikler **Udfør opdatering af indkøbsordre**. Noter og vedhæftede filer bliver ikke automatisk overført til den aktuelle indkøbsordre. Bemærk, at når du opdaterer den aktuelle indkøbsordre via **Udfør opdatering af indkøbsordre**-handlingen, bliver handelsaftaler ikke vurderet på ny på linjerne i indkøbsordren.


## <a name="po-statuses-and-versions"></a>Status for indkøbsordren og versioner
Dette afsnit beskrives de forskellige statusser, som en indkøbsordre kan have op til det tidspunkt, hvor den bekræftes. Det beskriver også, på hvilket tidspunkt nye versioner af indkøbsordren bliver gjort tilgængelige for kreditoren. Funktionaliteten varierer, afhængigt af om du bruger ændringsstyring for indkøbsordrer. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versioner og statusser, hvis du ikke bruger ændringsstyring

I nedenstående tabel vises et eksempel på ændringerne i status og version, som en indkøbsordre kan gennemgå.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                                                               | **Status og version**                                                                                                                                       |
| Den første version af indkøbsordren oprettes i Finance and Operations. | Status er **Godkendt**.                                                                                                                                  |
| Indløbsordren sendes til kreditoren.                                            | En version registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**.                                          |
| Kreditoren sender et **Accepteret med ændringer**-svar.                  | Status er stadig **Til eksternt gennemsyn**.                                                                                                                  |
| Du kan foretage nogle ændringer, som kreditoren har anmodet om.                  | Statussen ændres til **Godkendt**.                                                                                                                        |
| Du kan sende den nye version af indkøbsordren til kreditoren.                        | En ny version registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**.                                      |
| Kreditoren accepterer den nye version af indkøbsordren.                            | Status er stadig **Til eksternt gennemsyn,** medmindre kreditorkontoen er konfigureret til automatisk at angive indkøbsordren til tilstanden **Bekræftet**, når de accepterer. |


Kreditorer behøver ikke at bekræfte indkøbsordren via grænsefladen for kreditorsamarbejde. De kan også sende en e-mail eller kommunikere deres accept af en IO via andre kanaler. Derefter kan du bekræfte ordren manuelt i Finance and Operations. I dette tilfælde får du en advarsel om, at ordren er blevet bekræftet, selv om der intet svar er fra kreditoren. Indkøbsordren vises derefter i oversigten over bekræftelser som en åben bekræftet ordre, som ikke har nogen svar. Kreditoren har ikke længere mulighed for at bekræfte eller afvise indkøbsordren.  


>[!NOTE]
>Den version af indkøbsordren, der er tilgængelig for andre processer i Dynamics 365 Finance and Operations, er altid den nyeste version, selv om denne version endnu ikke er registreret i grænsefladen for kreditorsamarbejde.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versioner og statusser, hvis du bruger ændringsstyring

Hvis ændringsstyring er aktiveret for indkøbsordrer, gennemgår indkøbsordren en godkendelsesarbejdsgang for at nå frem til statussen **Godkendt**. Denne proces er ikke synlig for kreditoren.  

I følgende tabel vises et eksempel på ændringerne i status og version, som en indkøbsordre kan gennemgå, når ændringsstyring er slået til. Versionen registreres, når indkøbsordren er godkendt, og ikke når indkøbsordren sendes til kreditoren eller bekræftes.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                                                               | **Status og version**                                                                                                                                       |
| Den første version af indkøbsordren oprettes i Finance and Operations.      | Status er **Kladde**.  |
| Indkøbsordren sendes til godkendelsesprocessen. (Godkendelsesprocessen er en intern proces, som kreditoren ikke er involveret i).                                                           | Status ændres fra **Kladde** til **Til gennemsyn** til **Godkendelse**, hvis indkøbsordren ikke afvises under godkendelsesprocessen. Den godkendte indkøbsordre registreres som en version.           | 
| Indløbsordren sendes til kreditoren.                                                            | Versionen registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**.      |
| Du kan foretage ændringer, som kreditoren har anmodet om, enten manuelt eller ved hjælp af handlingen på svaret til opdatering af indkøbsordren.                                                            | Statussen ændres tilbage til **Kladde**.     |
|Indkøbsordren sendes igen til godkendelsesprocessen.                                                |  Status ændres fra **Kladde** til **Til gennemsyn** til **Godkendelse**, hvis indkøbsordren ikke afvises under godkendelsesprocessen. Systemet kan også konfigureres, så specifikke feltændringer ikke kræver fornyet godkendelse. I dette tilfælde ændres status først til **Kladde** og derefter opdateres automatisk til **Godkendt**. Den godkendte indkøbsordre registreres som en ny version.                                         |
|Du kan sende den nye version af indkøbsordren til kreditoren.                                                |  Den nye version registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**.                                         |
|Kreditoren godkender den nye version af IO'en.                                                |  Statussen ændres til **Bekræftet**. Det sker enten automatisk, eller når du modtager svar fra kreditoren og derefter bekræfter indkøbsordren. |

## <a name="share-information-about-consignment-inventory"></a>Dele oplysninger om konsignationslager
Hvis du bruger konsignationslager, kan kreditorer bruge kreditorsamarbejde til at få vist oplysninger på de følgende sider:

-   **Indkøbsordrer, der forbruger konsignationslager** - Indkøbsordrer for konsignationslager genereres, når ejerskabet af lageret ændres fra kreditoren til din virksomhed. En produktkvittering bogføres på samme tid. Disse konsignationindkøbsordrer vises kun på siden **Indkøbsordrer, der forbruger konsignationslager**. De er ikke inkluderet på siden **Alle bekræftede indkøbsordrer** i modulet **Kreditorsamarbejde**.
-   **Produkter, der er modtaget fra konsignationslager** - Denne side viser en liste over alle de transaktioner, hvor ejerskabet af produkter er blevet overført fra kreditoren til din virksomhed. Kreditorer kan bruge disse oplysninger til at fakturere kunden.
-   **Disponibelt konsignationslager** - Denne side viser kreditorejede disponible konsignationslager, der er modtaget på dit lagersted.





