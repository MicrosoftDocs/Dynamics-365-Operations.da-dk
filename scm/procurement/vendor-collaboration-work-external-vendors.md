---
title: "Leverandørsamarbejde med eksterne leverandører"
description: "I dette emne forklares, hvordan indkøbere bruger leverandørportalen til at samarbejde med eksterne kreditorer for at udveksle data om indkøbsordrer og konsignationslager."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b141ed78306504949eae641377b5c5a2b0599572
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Leverandørsamarbejde med eksterne leverandører

[!include[banner](../includes/banner.md)]


I dette emne forklares, hvordan indkøbere bruger leverandørportalen til at samarbejde med eksterne kreditorer for at udveksle data om indkøbsordrer og konsignationslager.

Modulet **Kreditorsamarbejde** henvender sig til kreditorer, der ikke har EDI-integration (Electronic Data Interchange) med Microsoft Dynamics 365 for Operations. Det gør det muligt for kreditorer at arbejde med oplysninger om købsordrer, fakturaer og konsignationslager. Dette emne beskriver, hvordan du kan samarbejde med eksterne kreditorer, der bruger kreditorsamarbejde-grænsefladen til at arbejde med indkøbsordrer og konsignationslager. Det beskriver også, hvordan du aktiverer en bestemt kreditor til at bruge kreditorsamarbejde, og hvordan du definerer de oplysninger, som alle kreditorer får vist, når de svarer på en indkøbsordre. Der er flere oplysninger om, hvad eksterne kreditorer kan gøre i grænsefladen for kreditorsamarbejde, i [Kreditorsamarbejde med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Der er flere oplysninger om, hvordan kreditorerne kan bruge kreditorsamarbejde i faktureringsprocesser, i [Arbejdsområde for kreditorsamarbejdsfakturering](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Der er oplysninger om, hvordan du klargør nye brugere af kreditorsamarbejde, i [Administrere brugere af kreditorsamarbejde](manage-vendor-collaboration-users.md).

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>Definere de oplysninger, der vises for kreditorer, når de reagerer på indkøbsordrer
Når kreditorer besvarer en indkøbsordre, som du sender til dem, vises en dialogboks, hvor de skal bekræfte, at de vil acceptere, afvise eller acceptere indkøbsordren med ændringer. De oplysninger, der skal vises for kreditoren på dette tidspunkt, kan være specifikke for din virksomhed, så du kan angive den tekst, der vises på hver af de tre bekræftelsesmeddelelser. Teksten kunne meddele kreditoren om de næste trin i processen, eller vilkår og betingelser.  

Sådan angives den tekst, der vises i svar til indkøbsordrer:

1.  Åbn siden **Oplysninger til kreditorer, der reagerer på IO'er**.
2.  Vælg én af svartyperne:
3.  Klik på **Rediger**.
4.  Angiv de oplysninger, som kreditorer skal se, i feltet **Meddelelse med oplysninger**.

Hvis du vil tilføje meddelelser på mere end ét sprog, skal du oprette separate meddelelser med de relevante sprogkoder. Kreditoren får vist meddelelsen på det sprog, de bruger.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Angive kreditorens samarbejdsindstillinger for en bestemt kreditor
De generelle indstillinger for kreditorsamarbejde i Dynamics 365 for Operations er konfigureret af administratoren. For eksempel vil de bestemme, hvilke sikkerhedsroller der er tilgængelige for alle de kreditorer, du samarbejder med. Der er også nogle indstillinger, der kan være forskellige for hver kreditorkonto, og du skal angive disse:

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

Indkøbsordrer fremstilles i Dynamics 365 for Operations. Når IO'en har statussen **Godkendt**, sender du den til kreditoren ved hjælp af handlingen **Send til bekræftelse** på siden **Indkøbsordre**. Indkøbsordrens status ændres til **Til eksternt gennemsyn**. Når indkøbsordren er blevet sendt, kan kreditoren se den på siden **Indkøbsordrer til gennemsyn** i kreditorsamarbejdets grænseflade, hvor de kan acceptere, afvise eller foreslå ændringer til ordren. Leverandøren kan også tilføje kommentarer for at kommunikere oplysninger, f.eks. ændringer af IO'en. Hvis du vil henlede kreditorens opmærksomhed på den nye IO, kan du også bruge udskriftsstyringssystemet til at sende IO'en via e-mail.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Bekræftelse og accept af indkøbsordre hos kreditoren

Når en kreditor har accepteret en indkøbsordre, kan indkøbsordren bekræftes automatisk, eller det kan være nødvendigt at bekræfte den manuelt. Dette afhænger af, om feltet **Aktivering af kreditor** er angivet til **Aktiv (IO bekræftes automatisk)** for kreditoren eller til **Aktiv (IO bekræftes ikke automatisk)**.  

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
<td>Kreditoren <strong>accepterer</strong> ordren. Dynamics 365 for Operations er konfigureret til automatisk at bekræfte IO'er, når kreditoren accepterer.</td>
<td>Status for ordren opdateres til <strong>Bekræftet</strong>. Hvis noget forhindrer, at ordren opdateres, bliver kreditorens svar stadig registreret som <strong>Accepteret</strong>, men indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>.</td>
</tr>
<tr class="odd">
<td>Kreditoren <strong>accepterer</strong> ordren. Dynamics 365 for Operations er ikke konfigureret til automatisk at bekræfte IO'er, når kreditoren accepterer.</td>
<td>Kreditorens svar registreres som <strong>Accepteret</strong>, men indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>.</td>
</tr>
<tr class="even">
<td>Kreditoren <strong>afviser</strong> ordren.</td>
<td>Kreditorens svar registreres som <strong>Afvist</strong>, og indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>. Afvisningen modtages sammen med kreditornoten.</td>
</tr>
<tr class="odd">
<td>Leverandøren <strong>accepterer ordren med ændringer</strong>. Der foreslås ændringer på linjeniveau. Det er muligt at acceptere eller afvise individuelle linjer. Andre mulige ændringer omfatter:
<ul>
<li>Ændre datoer eller antal.</li>
<li>Opdele linjer for forskellige leveringsdatoer eller antal.</li>
<li>Udskifte en vare.</li>
</ul>
Oplysninger om pris og gebyrer kan ikke ændres af kreditoren. Forslag til ændringer af disse kan foretages ved hjælp af noter.</td>
<td>Kreditorens svar registreres som <strong>Accepteret med ændringer</strong>, <strong></strong> og indkøbsordrens status forbliver <strong>Til eksternt gennemsyn</strong>.</td>
</tr>
</tbody>
</table>

Du kan bruge **Indkøbsordre** arbejdsområdet **Forberedelse** til at overvåge, hvilke IO'er kreditoren har reageret på. Arbejdsområdet indeholder to lister, der indeholder indkøbsordrer med status **Til eksternt gennemsyn**:

-   Til eksternt gennemsyn kræver handling.
-   Til eksternt gennemsyn, der venter på svar fra kreditor.

### <a name="changing-a-po"></a>Ændring af en indkøbsordre

Når du vil ændre en indkøbsordre, der allerede er svaret på, kan du sende en ny version af indkøbsordren til kreditoren. Den nye IO har et versionssuffiks, som angiver, at det er en ændret version af en tidligere kommunikeret indkøbsordre. På siden **Historik over bekræftelse af kreditor for indkøbsordre** kan du og dine kreditorer holde styr på historikken for hver ordre. Den tidligere bekræftede version af indkøbsordren forbliver på listen over bekræftede indkøbsordrer, indtil den nye indkøbsordre er blevet bekræftet.

### <a name="cancelling-a-po"></a>Annullering af en indkøbsordre

Når du annullerer en indkøbsordre, ændres statussen til **Godkendt**. Du skal sende IO'en tilbage til kreditoren via kreditorportalen, så kreditoren kan bekræfte eller afvise annulleringen. Når annulleringen bekræftes, vises indkøbsordren på kreditorens liste over bekræftede indkøbsordrer som **Annulleret**.

### <a name="adding-attachments-to-a-po"></a>Tilføjelse af vedhæftede filer i en indkøbsordre

Du kan føje vedhæftede filer, f.eks. billeder og noter, til indkøbsordren ved hjælp af dokumentstyringssystemet. De vedhæftede filer, der er tilføjet med begrænsning af typen **Ekstern**, vil være synlig for kreditoren, når du sender indkøbsordren til dem.

## <a name="purchase-order-statuses-and-versions"></a>Købsordres statusser og versioner
I dette afsnit beskrives de forskellige statusser, som en indkøbsordre kan have op til det tidspunkt, når den er bekræftet, og hvornår nye versioner af indkøbsordren gøres tilgængelige for kreditoren. Der er forskelle heri, afhængigt af om du bruger ændringsstyring for indkøbsordrer. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versioner og statusser, hvis du ikke bruger ændringsstyring

I nedenstående tabel vises et eksempel på ændringerne i status og version, som en indkøbsordre kan gennemgå.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                                                               | **Status og version**                                                                                                                                       |
| Den første version af indkøbsordren oprettes i Dynamics 365 for Operations. | Status er **Godkendt**.                                                                                                                                  |
| Indløbsordren sendes til kreditoren.                                            | En version registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**.                                          |
| Kreditoren sender et **Accepteret med ændringer**-svar.                  | Status er stadig **Til eksternt gennemsyn**.                                                                                                                  |
| Du kan foretage nogle ændringer, som kreditoren har anmodet om.                  | Statussen ændres til **Godkendt**.                                                                                                                        |
| Du kan sende den nye version af indkøbsordren til kreditoren.                        | En ny version registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**.                                      |
| Kreditoren accepterer den nye version af indkøbsordren.                            | Status er stadig **Til eksternt gennemsyn,**medmindre kreditorkontoen er konfigureret til automatisk at angive indkøbsordren til tilstanden **Bekræftet**, når de accepterer. |

Kreditorer behøver ikke at bekræfte indkøbsordren i grænsefladen for kreditorsamarbejde. De kan også sende en e-mail eller kommunikere deres accept af en IO via andre kanaler. Derefter kan du bekræfte ordren manuelt i Dynamics 365 for Operations. I dette tilfælde modtager du en advarsel om, at ordren er blevet bekræftet, selv om der intet svar er fra kreditoren. Indkøbsordren vises derefter i oversigten over bekræftelser som en åben bekræftet ordre, som ikke har nogen svar. Kreditoren har ikke længere mulighed for at bekræfte eller afvise indkøbsordren.  

**Bemærk!** Den version af indkøbsordren, der er tilgængelig for andre processer i Dynamics 365 for Operations, er altid den nyeste version, selv om denne version endnu ikke er registreret i grænsefladen for kreditorsamarbejde.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versioner og statusser, hvis du bruger ændringsstyring

Hvis ændringsstyring er aktiveret for indkøbsordrer, gennemgår indkøbsordren en godkendelsesarbejdsgang for at nå frem til statussen **Godkendt**. Denne proces er ikke synlig for kreditoren.  

I følgende tabel vises et eksempel på ændringerne i status og version, som en indkøbsordre kan gennemgå, når ændringsstyring er slået til. Versionen registreres, når indkøbsordren er godkendt, og ikke når indkøbsordren sendes til kreditoren eller bekræftes.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                                                                                                    | **Status og version**                                                                                                                                                                                                                                                                                                                                                                      |
| Den første version af indkøbsordren oprettes i Dynamics 365 for Operations.                                      | Status er **Kladde**.                                                                                                                                                                                                                                                                                                                                                                    |
| Indkøbsordren sendes til godkendelsesprocessen. (Dette er en intern proces, som kreditoren ikke er involveret i). | Status ændres fra **Kladde** til **Til gennemsyn** til **Godkendelse**, hvis indkøbsordren ikke afvises under godkendelsesprocessen. Den godkendte indkøbsordre registreres som en version.                                                                                                                                                                                                                     |
| Indløbsordren sendes til kreditoren.                                                                                  | Versionen registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**.                                                                                                                                                                                                                                                                       |
| Du kan foretage nogle ændringer, som kreditoren har anmodet om.                                                       | Statussen ændres tilbage til **Kladde**.                                                                                                                                                                                                                                                                                                                                                    |
| Indkøbsordren sendes igen til godkendelsesprocessen.                                                            | Status ændres fra **Kladde** til **Til gennemsyn** til **Godkendelse**, hvis indkøbsordren ikke afvises under godkendelsesprocessen. Systemet kan også konfigureres, så specifikke feltændringer ikke kræver fornyet godkendelse. I dette tilfælde ændres status først til **Kladde** og derefter opdateres automatisk til **Godkendt**. Den godkendte indkøbsordre registreres som en ny version. |
| Du kan sende den nye version af indkøbsordren til kreditoren.                                                             | Den nye version registreres i grænsefladen for kreditorsamarbejde, og status ændres til **Til eksternt gennemsyn**.                                                                                                                                                                                                                                                                   |
| Kreditoren godkender den nye version af IO'en.                                                                | Statussen ændres til **Bekræftet**. Det sker enten automatisk, eller når du modtager svar fra kreditoren og derefter bekræfter indkøbsordren.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Dele oplysninger om konsignationslager
Hvis du bruger konsignationslager, kan kreditorer bruge kreditorsamarbejde til at få vist oplysninger på de følgende sider:

-   **Indkøbsordrer, der forbruger konsignationslager** - Indkøbsordrer for konsignationslager genereres, når ejerskabet af lageret ændres fra kreditoren til din virksomhed. En produktkvittering bogføres på samme tid. Disse konsignationindkøbsordrer vises kun på siden **Indkøbsordrer, der forbruger konsignationslager**. De er ikke inkluderet på siden **Alle bekræftede indkøbsordrer** i modulet **Kreditorsamarbejde**.
-   **Produkter, der er modtaget fra konsignationslager** - Denne side viser en liste over alle de transaktioner, hvor ejerskabet af produkter er blevet overført fra kreditoren til din virksomhed. Kreditorer kan bruge disse oplysninger til at fakturere kunden.
-   **Disponibelt konsignationslager** - Denne side viser kreditorejede disponible konsignationslager, der er modtaget på dit lagersted.





