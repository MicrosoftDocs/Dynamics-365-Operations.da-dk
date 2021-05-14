---
title: Aktivere beskeder om kunders indtjekning i POS
description: Dette emne beskriver, hvordan du kan aktivere beskeder om kunders indtjekning i POS for Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
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
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937570"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Aktivere beskeder om kunders indtjekning i POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne beskriver, hvordan du kan aktivere beskeder om kunders indtjekning i POS for Microsoft Dynamics 365 Commerce.

I deres mails angående "ordre klar til afhentning" kan organisationer give et link eller en knap, så kunderne kan give butikken besked om, at de er på stedet og venter på, at pakken bliver bragt ud til dem. Kunderne modtager derefter en bekræftelse af deres indtjekning, og butikken modtager en besked som en opgave i POS-applikationen. Denne opgave fungerer som en besked om, at en salgsmedarbejder skal levere ordren til kundens køretøj. Derfor behøver kunden ikke at gå ind i butikken.

Arbejdsgangen for kundens indtjekning kan også konfigureres til at indsamle yderligere oplysninger fra kunder, f.eks. deres parkeringspladssnummer, mærket, modellen og farven på køretøjet samt leveringsinstruktionerne. Medarbejderen i detailbutikken kan bruge disse oplysninger til at lette ordrehåndteringen.

## <a name="enable-customer-check-in"></a>Aktivere kunders indtjekning

Når funktionen til kunders indtjekning er aktiveret, genererer Commerce et ordrebekræftelses-id (også kaldet kanalreference-id'et). Der genereres også ordrebekræftelses-d'er for ordrer, der oprettes via POS- eller callcenter-kanaler. 

Benyt denne fremgangsmåde for at aktivere funktionen til kunders indtjekning i Commerce-hovedkvarteret.

1. Gå til **Arbejdsområder \> Funktionsstyring**.
2. Søg efter funktionen **Generer et konsistent kanalreference-id-format på tværs af kanaler**. 
3. Vælg funktionen, og vælg derefter **Aktiver nu** i egenskabsruden. 

## <a name="create-a-check-in-confirmation-page"></a>Oprette en side med bekræftelse af indtjekning

På dit e-handelswebsted skal du oprette en ny side, der kan bruges til bekræftelsen af indtjekning. Med yderligere konfiguration kan siden også omfatte en formular, der indsamler yderligere oplysninger fra kunder for at lette ordrehåndteringen. Du kan finde flere oplysninger om, hvordan du konfigurerer siden og modulet, i [Modul til kunders indtjekning](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Konfigurere mail-skabelonen til transaktioner

Du skal tilføje et link eller en knap for **Her er jeg** til skabelonen for den transaktionsmail, som kunder modtager, når deres ordre er klar til afhentning. Kunder kan bruge dette link eller denne knap til at give butikken besked om, at de er ankommet for at hente deres ordre. 

Tilføj linket eller knappen til den skabelon, der er knyttet til beskedtypen **Emballagering fuldført** og den leveringsmåde, du bruger til ordrehåndtering ved afhentning ved fortovskanten. I skabelonen skal du oprette et HTML-link eller en knap, der peger på URL-adressen til den oprettede side for bekræftelsen af indtjekning. Her er et eksempel.

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
Du kan finde flere oplysninger om, hvordan du konfigurerer mailskabeloner, i [Tilpasse transkationsmails efter leveringsmåde](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>Der oprettes en opgave til bekræftelse af indtjekning i POS

Når en kunde giver butikken besked om, at kunden er klar afhentningen, modtager kunden en beskræftelse af indtjekningen, og der oprettes en opgave på opgavelisten i POS for den butik, hvor kunden afhenter ordren. Opgaven indeholder alle de kunde- og ordreoplysninger, der skal bruges til at opfylde ordren. I opgaven viser feltet med instruktioner alle de oplysninger, der er indsamlet fra kunden via formularen til ekstra oplysninger. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Modul for indtjekning ved afhentning](check-in-pickup-module.md)
