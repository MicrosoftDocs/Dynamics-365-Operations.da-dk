---
title: Konfigurere en onlinekanal
description: Denne artikel beskriver, hvordan du opretter en ny onlinekanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: be9fafe8ece771ad6577db1cdb70af6f48e054cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272874"
---
# <a name="set-up-an-online-channel"></a>Konfigurere en onlinekanal

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du opretter en ny onlinekanal i Microsoft Dynamics 365 Commerce.

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

![Ny onlinekanal.](media/channel-setup-online-1.png)

Følgende billede viser et eksempel på en onlinekanal.

![Eksempel på onlinekanal.](media/channel-setup-online-2.png)

## <a name="assign-the-channel-to-a-commerce-scale-unit"></a>Tildele kanalen til en Commerce Scale Unit

Den nye kanal skal være tildelt til en Commerce Scale Unit. Du kan finde instruktioner under [Konfigurere kanaler til brug af Commerce Scale Unit](../fin-ops-core/dev-itpro/deployment/initialize-retail-channels.md#configure-channels-to-use-commerce-scale-unit).

## <a name="set-up-languages"></a>Konfigurer sprog

Hvis dit e-handels-websted skal understøtte flere sprog, skal du udvide afsnittet **Sprog** og tilføje flere sprog efter behov.

## <a name="set-up-payment-account"></a>Konfigurere betalingskonto

Du kan tilføje en tredjepartsbetalingsudbyder i sektionen **Betalingskonto**. Du kan få oplysninger om konfiguration af en Adyen-betalingsconnector i [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Yderligere kanalopsætning

Yderligere opgaver, der kræves til konfiguration af onlinekanalen, omfatter konfiguration af betalingsmetoder, leveringsmetoder og gruppetildeling for opfyldelse.

Følgende billede viser opsætningsindstillinger til **Leveringsmetoder**, **Betalingsmetoder** og **Gruppetildeling for opfyldelse** under fanen **Opsætning** .

![Yderligere handlinger til konfiguration af onlinekanal.](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Oprette betalingsmåder

Hvis du vil oprette betalingsmetoder, skal du udføre disse trin for hver af de betalingstyper, der understøttes på denne kanal.

1. Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Betalingsmetoder**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg den ønskede betalingsmetode i navigationsruden.
1. Angiv et **Handlingsnavn** i sektionen **Generelt**, og konfigurer evt. andre ønskede indstillinger.
1. Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på en metode til kontantbetaling.

![Eksempel på betalingsmetoder.](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Konfigurer leveringsmåder

Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmetoder** under fanen **Opsætning** i **Handlingsrude**.  

Udfør følgende trin for at ændre eller tilføje en leveringsmetode.

1. Gå til **Moduler \> Lagerstyring \> Leeringsmetoder** i navigationsruden.
1. Vælg **Ny** i handlingsruden for at oprette en ny leveringsmetode, eller vælg en eksisterende metode.
1. Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje kanalen. Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.

Følgende billede viser et eksempel på en leveringsmetode.

![Konfigurer leveringsmåder.](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Konfigurer en gruppetildeling for opfyldelse

Gør følgende for at konfigurere en gruppetildeling for opfyldelse.

1. Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Gruppetildeling for opfyldelse**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg en opfyldelsesgruppe på rullelisten **Opfyldelsesgruppe**.
1. Indtast en beskrivelse i rullelisten **Beskrivelse**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på en opsætning af en gruppetildeling for opfyldelse.

![Konfigurer Gruppetildeling for opfyldelse.](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Konfigurer en detailkanal](channel-setup-retail.md)

[Konfigurere en callcenter-kanal](channel-setup-callcenter.md)

[Dynamics 365-betalingsconnector til Adyen](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
