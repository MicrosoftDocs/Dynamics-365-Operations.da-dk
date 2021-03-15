---
title: Konfigurere en onlinekanal
description: Dette emne beskriver, hvordan du opretter en ny onlinekanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 89a28d6d4f435b9cf0c39afc64c3caaf0b24ba19
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993622"
---
# <a name="set-up-an-online-channel"></a>Konfigurere en onlinekanal


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter en ny onlinekanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Dynamics 365 Commerce understøtter flere detailkanaler. Disse detailkanaler omfatter onlinebutikker, call centre og detailbutikker (også kaldet fysiske butikker). Onlinebutikker giver kunderne mulighed for at købe produkter fra detailhandlerens onlinebutik ud over fra detailhandlerens fysiske butik.

Hvis du vil oprette en onlinebutik i Commerce, skal du først oprette en onlinekanal. Før du opretter en ny onlinekanal, skal du sikre dig, at du har fuldført [forudsætningerne for kanalopsætning](channels-prerequisites.md).

Før du kan oprette et nyt websted, skal der oprettes mindst én onlinebutik i Commerce. Du kan finde flere oplysninger under [Oprette et websted for e-handel](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Oprette og konfigurere en ny onlinekanal

Følg disse trin for at oprette en ny onlinekanal.

1. Gå til **Moduler \> Kanaler \> Onlinebutikker** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Skriv et navn til den nye kanal i feltet **Navn**.
1. Angiv den relevante **Juridiske enhed** på rullelisten Juridisk enhed.
1. Angiv det relevante **Lagersted** på rullelisten Lagersted.
1. Vælg den relevante tidszone i feltet **Lagertidszone**.
1. Vælg den relevante valuta i feltet **Valuta**.
1. Angiv en gyldig standardkunde i feltet **Standardkunde**.
1. Angiv et gyldigt adressekartotek i feltet **Kundeadressekartotek**.
1. Vælg en funktionalitetsprofil i feltet **Funktionalitetsprofil**, hvis det er relevant.
1. Angiv en gyldig mailbeskedprofil i feltet **Profil til e-mail-besked**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser oprettelsen af en ny onlinekanal.

![Ny onlinekanal](media/channel-setup-online-1.png)

Følgende billede viser et eksempel på en onlinekanal.

![Eksempel på onlinekanal](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a>Konfigurer sprog

Hvis dit e-handels-websted skal understøtte flere sprog, skal du udvide afsnittet **Sprog** og tilføje flere sprog efter behov.

## <a name="set-up-payment-account"></a>Konfigurere betalingskonto

Du kan tilføje en tredjepartsbetalingsudbyder i sektionen **Betalingskonto**. Du kan få oplysninger om konfiguration af en Adyen-betalingsconnector i [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Yderligere kanalopsætning

Yderligere opgaver, der kræves til konfiguration af onlinekanalen, omfatter konfiguration af betalingsmetoder, leveringsmetoder og gruppetildeling for opfyldelse.

Følgende billede viser opsætningsindstillinger til **Leveringsmetoder**, **Betalingsmetoder** og **Gruppetildeling for opfyldelse** under fanen **Opsætning** .

![Yderligere handlinger til konfiguration af onlinekanal](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Oprette betalingsmåder

Hvis du vil oprette betalingsmetoder, skal du udføre disse trin for hver af de betalingstyper, der understøttes på denne kanal.

1. Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Betalingsmetoder**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg den ønskede betalingsmetode i navigationsruden.
1. Angiv et **Handlingsnavn** i sektionen **Generelt**, og konfigurer evt. andre ønskede indstillinger.
1. Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på en metode til kontantbetaling.

![Eksempel på betalingsmetoder](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Konfigurer leveringsmåder

Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmetoder** under fanen **Opsætning** i **Handlingsrude**.  

Udfør følgende trin for at ændre eller tilføje en leveringsmetode.

1. Gå til **Moduler \> Lagerstyring \> Leeringsmetoder** i navigationsruden.
1. Vælg **Ny** i handlingsruden for at oprette en ny leveringsmetode, eller vælg en eksisterende metode.
1. Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje kanalen. Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.

Følgende billede viser et eksempel på en leveringsmetode.

![Konfigurer leveringsmåder](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Konfigurer en gruppetildeling for opfyldelse

Gør følgende for at konfigurere en gruppetildeling for opfyldelse.

1. Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Gruppetildeling for opfyldelse**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg en opfyldelsesgruppe på rullelisten **Opfyldelsesgruppe**.
1. Indtast en beskrivelse i rullelisten **Beskrivelse**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på en opsætning af en gruppetildeling for opfyldelse.

![Konfigurer Gruppetildeling for opfyldelse](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Konfigurer en detailkanal](channel-setup-retail.md)

[Konfigurere en callcenter-kanal](channel-setup-callcenter.md)

[Dynamics 365-betalingsconnector til Adyen](../retail/dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]