---
title: Modul til afhentningsoplysninger
description: Denne artikel beskriver afhentningsoplysningsmodulet, og det beskriver, hvordan du kan føje det til betalingssider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 57633b7a23e581278ec0bc09ea146f5453570c4e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288400"
---
# <a name="pickup-information-module"></a>Modul til afhentningsoplysninger

[!include [banner](includes/banner.md)]

Denne artikel beskriver afhentningsoplysningsmodulet, og det beskriver, hvordan du kan føje det til betalingssider i Microsoft Dynamics 365 Commerce.

Modulet med afhentningsoplysninger kan bruges i betalingsmodulet til at vise oplysninger om ordreafhentning. Kunder kan få vist de tilgængelige afhentningsdatoer og tidsintervaller og derefter vælge et passende tidspunkt at afhente ordren. En kunde kan f.eks. vælge at afhente en ordre kl. 15 den 21. marts i en butik i Slagelse.

Afhentningstider for de relevante butikker skal konfigureres i Commerce Headquarters. Du kan finde flere oplysninger under [Oprette og opdatere tidsintervaller for kundeafhentning](dev-itpro/pickup-timeslots.md).

Hvis der oprettes et afhentningsoplysningsmodul på en betalingsside, men der ikke er defineret nogen tidsintervaller for den butik, der er valgt til afhentning, vises der oplysninger i modulet, men brugeren kan ikke vælge nogen tidsintervaller. Tidsintervaller er valgfrie og er ikke påkrævede ved afgivelse af en ordre.

Hvis der er valgt flere varer til afhentning på tværs af flere butikker, vil brugeren have mulighed for at vælge et tidsinterval i afhentningsmodulet for hver butik, hvis der er tilgængelige tidsintervaller for den.

> [!NOTE]
> Understøttelse af tidsintervaller og afhentningsoplysningsmodulet på betalingssiden er tilgængelige i Dynamics 365 Commerce version 10.0.15 og nyere versioner.

I følgende illustration vises et eksempel på valg af tidsinterval via modulet med afhentningsoplysninger på en betalingsside.

![Eksempel på et afhentningsoplysningsmodul på en betalingsside.](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Modulegenskaber

- **Overskrift** – Angiv en overskrift til modulet.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Vise tidsintervaloplysninger, når en ordre er afgivet

Når en ordre er afgivet, kan oplysninger om det valgte tidsinterval ses i [ordrebekræftelsesmodulet](order-confirmation-module.md) og [ordreoplysningsmodulet](account-management.md#order-details-page). Begge disse moduler har egenskaben **Vis tidsintervaloplysninger**. Hvis du vil have vist det valgte tidsinterval under ordreprocessen, skal denne egenskab være indstillet til **Sand**.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Føje et afhentningsoplysningsmodul for betaling til en side

Du kan få flere oplysninger om, hvordan du føjer et afhentningsoplysningsmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).

I følgende illustration vises et eksempel på en e-handelsbetalingside, der indeholder tidsintervaller for afhentningslinjevarer.

![Eksempel på en e-handelsbetalingsside, der indeholder tidsintervaller for linjevarer til afhentning.](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette og opdatere tidsrubrikker for kundeafhentning](dev-itpro/pickup-timeslots.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Ordredetaljer-modul](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
