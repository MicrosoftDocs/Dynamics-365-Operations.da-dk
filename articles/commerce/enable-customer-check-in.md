---
title: Aktivere beskeder om kunders indtjekning i POS
description: Denne artikel beskriver, hvordan du kan aktivere beskeder om kunders indtjekning i POS for Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ae53657c95128eae793f670bd9dbc31d9fac0fe4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885139"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Aktivere beskeder om kunders indtjekning i POS

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du kan aktivere beskeder om kunders indtjekning i POS for Microsoft Dynamics 365 Commerce.

I deres mails angående "ordre klar til afhentning" kan organisationer give et link eller en knap, så kunderne kan give butikken besked om, at de er på stedet og venter på, at pakken bliver bragt ud til dem. Kunderne modtager derefter en bekræftelse af deres indtjekning, og butikken modtager en besked som en opgave i POS-applikationen. Denne opgave fungerer som en besked om, at en salgsmedarbejder skal levere ordren til kundens køretøj. Derfor behøver kunden ikke at gå ind i butikken.

Arbejdsgangen for kundens indtjekning kan også konfigureres til at indsamle yderligere oplysninger fra kunder, f.eks. deres parkeringspladssnummer, mærket, modellen og farven på køretøjet samt leveringsinstruktionerne. Medarbejderen i detailbutikken kan bruge disse oplysninger til at lette ordrehåndteringen.

## <a name="enable-customer-check-in"></a>Aktivere kunders indtjekning

Når funktionen til kunders indtjekning er aktiveret, genererer Commerce et ordrebekræftelses-id (også kaldet kanalreference-id'et). Der genereres også ordrebekræftelses-d'er for ordrer, der oprettes via POS- eller callcenter-kanaler. 

Benyt denne fremgangsmåde for at aktivere funktionen til kunders indtjekning i Commerce headquarters.

1. Gå til **Arbejdsområder \> Funktionsstyring**.
2. Søg efter funktionen **Generer et konsistent kanalreference-id-format på tværs af kanaler**. 
3. Vælg funktionen, og vælg derefter **Aktiver nu** i egenskabsruden. 

## <a name="create-a-check-in-confirmation-page"></a>Oprette en side med bekræftelse af indtjekning

På dit e-handelswebsted skal du oprette en ny side, der kan bruges til bekræftelsen af indtjekning. Med yderligere konfiguration kan siden også omfatte en formular, der indsamler yderligere oplysninger fra kunder for at lette ordrehåndteringen. Du kan finde flere oplysninger om, hvordan du konfigurerer siden og modulet, i [Modul til kunders indtjekning](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Konfigurere mail-skabelonen til transaktioner

Du skal tilføje et link eller en knap for **Her er jeg** til skabelonen for den transaktionsmail, som kunder modtager, når deres ordre er klar til afhentning. Kunder kan bruge dette link eller denne knap til at give butikken besked om, at de er ankommet for at hente deres ordre. 

Tilføj linket eller knappen til den skabelon, der er knyttet til beskedtypen **Emballagering fuldført** og den leveringsmåde, du bruger til ordrehåndtering ved afhentning ved fortovskanten. I skabelonen skal du oprette et HTML-link eller en knap, der peger på URL-adressen for den side med bekræftelse af indtjekning, som du har oprettet, og som omfatter parameternavnene og -værdierne, som vist i følgende eksempel.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Du kan finde flere oplysninger om, hvordan du konfigurerer mailskabeloner, i [Tilpasse transkationsmails efter leveringsmåde](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>Der oprettes en opgave til bekræftelse af indtjekning i POS

Når en kunde har fortalt butikken, de er til stede for afhentning, viser siden til indtjekning en bekræftelse og en valgfri QR-kode, der indeholder kundens ordrebekræftelses-id. Samtidig oprettes der en opgave på opgavelisten i POS til den butik, hvor kunden afhenter ordren. Opgaven indeholder alle de kunde- og ordreoplysninger, der skal bruges til at opfylde ordren. I opgaven viser feltet med instruktioner alle de oplysninger, der er indsamlet fra kunden via formularen til ekstra oplysninger.

## <a name="end-to-end-testing"></a>Test fra ende til anden

Kundeindtjekning kræver, at bestemte parametre og værdier overføres til indtjekningssiden og derefter til kundens API til indtjekning. Det er derfor lettest at teste funktionen i et miljø, hvor en testordre kan oprettes og pakkes. På den måde kan der genereres en "ordre klar til afhentning"-mail med en URL-adresse, der indeholder de nødvendige parameternavne og værdier.

Hvis du vil teste kundens indtjekningsfunktion, skal du følge disse trin.

1. Opret siden til kundeindtjekning, og tilføj og konfigurer derefter modulet til kundeindtjekning. Du kan finde flere oplysninger i [Modul for indtjekning ved afhentning](check-in-pickup-module.md). 
1. Tjek siden ind, men publicer den ikke.
1. Tilføj følgende link i en mailskabelon, som aktiveres af beskedtypen om fuldført pakning for en afhentningsmåde. Du kan få flere oplysninger i [Oprette mailskabeloner til transaktionshændelser](email-templates-transactions.md).

    - **Til før-produktionsmiljøer (test af brugeraccept - UAT):** Tilføj kodestykket fra afsnittet [Konfigurere mail-skabelonen til transaktioner](#configure-the-transactional-email-template) tidligere i denne artikel.
    - **Til produktionsmiljøer:** Tilføj følgende kommentarkode, så eksisterende kunder ikke påvirkes.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Opret en ordre, hvor der er angivet afhentningsmåde.
1. Når du modtager den mail, der udløses af beskedtypen om fuldført pakning, skal du teste indtjekningsflowet ved at åbne den indtjekningsside, der har den URL-adresse, du har tilføjet tidligere. Da URL-adressen indeholder flaget `&preview=inprogress`, bliver du bedt om at godkende, før du kan få vist siden.
1. Angiv eventuelle supplerende oplysninger, der kræves for at konfigurere modulet.
1. Kontrollér, at visningen af bekræftelse ved indtjekning er vist korrekt.
1. Åbn en POS-klient for den butik, hvor ordren afhentes.
1. Vælg feltet **Ordrer, der skal afhentes**, og kontrollér, at ordren vises.
1. Kontrollér, at eventuelle yderligere oplysninger, der er konfigureret i modulet til indtjekning, vises i detaljeruden.

Når du har kontrolleret, at kundens indtjekning fungerer fra ende til anden, skal du følge disse trin.

1. Publicer siden til indtjekning.
1. Hvis du tester i et produktionsmiljø, skal du fjerne kommentaren til URL-adressen i mailskabelonen "ordre klar til afhentning", så linket eller knappen **Jeg er her** vises. Upload derefter skabelonen igen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modul for indtjekning ved afhentning](check-in-pickup-module.md)

[Tilpasse transaktionsmails efter leveringsmåde](customize-email-delivery-mode.md)

[Oprette e-mailskabeloner til transaktionshændelser](email-templates-transactions.md)
