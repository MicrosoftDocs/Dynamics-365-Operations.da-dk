---
title: Oprette en standarddebitor
description: Dette emne beskriver, hvordan du opretter en standarddebitor, der skal bruges, når der oprettes en kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ba1d10a897f349703737068d772423f7d0292944
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410994"
---
# <a name="create-a-default-customer"></a>Oprette en standarddebitor


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter en standarddebitor, der skal bruges, når der oprettes en kanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Når du opretter en kanal, skal du angive en standardkunde. Der kan nemt oprettes en standarddebitor, når kundegruppen og kundeadressekartoteket først er oprettet.

## <a name="create-a-customer-group"></a>Oprette en kundegruppe

Hvis der endnu ikke findes nogen kundegrupper, kan du oprette en. Eksempler på dette kan være grupper, der repræsenterer forskellige kundegrupper, f.eks. engros, detail, internet, medarbejdere osv.

Du kan oprette en kundegruppe ved at følge disse trin.

1. Gå til **Moduler \> Detail og handel \> Kunder \> Kundegrupper** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. I feltet **Kundegruppe** skal du indtaste et id for kundegruppen.
1. Angiv eventuelt en passende beskrivelse i feltet **Beskrivelse**.
1. Angiv eventuelt en passende beskrivelse i feltet **Betalingsbetingelser**.
1. Angiv en relevant værdi i feltet **Tid mellem fakturaens forfaldsdato og betalingsdato**.
1. Angiv en momsgruppe i feltet **Standardmomsgruppe**, hvis det er relevant.
1. Markér afkrydsningsfeltet **Priserne inkluderer moms**, hvis det er relevant.
1. I feltet **Standardårsag til afskrivning** skal du angive en passende værdi, hvis det er relevant.

Følgende billede viser flere konfigurerede kundegrupper.

![Debitorgrupper](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Opret et kundeadressekartotek

En kunde skal være knyttet et adressekartotek. Hvis der endnu ikke er oprettet et, skal du oprette det.

Du kan oprette et kundeadressekartotek ved at følge disse trin.

1. Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Adressekartoteker** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Indtast et navn i feltet **Navn**.
1. Indtast en beskrivelse i feltet **Beskrivelse**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på et adressekartotek.

![Adressebog](media/address-book.png)

## <a name="create-a-default-customer"></a>Oprette en standarddebitor

Du kan oprette en standarddebitor ved at følge disse trin.

1. Gå til **Moduler \> Detail og handel \> Kunder \> Alle kunder** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg "Person" på rullelisten **Type**.
1. Vælg eller indtast et kontonummer (f.eks "100001") på rullelisten **Kundekonto**.
1. Vælg eller indtast et navn (f.eks. "Standard") på rullelisten **Fornavn**.
1. Vælg eller indtast et navn (f.eks. "Detail") på rullelisten **Mellemnavn**.
1. Vælg eller indtast et navn (f.eks. "Kunde") på rullelisten **Efternavn**.
1. Vælg eller indtast en valuta (f.eks. "USD") på rullelisten **Valuta**.
1. Vælg den kundegruppe, du tidligere har oprettet, på rullelisten **Valuta**.
1. Vælg et eksisterende kundeadressekartotek på rullelisten **Adressekartoteker**.
1. Vælg **Gem** for at gemme og vende tilbage til skærmbilledet med kundedetaljer for den nye kunde.

> [!NOTE]
> Det er ikke nødvendigt at tilføje en adresse for en standardkunde.

Følgende billede viser et eksempel på kundeoprettelse.

![Standardkundeoprettelse](media/default-customer-creation.png)

Følgende billede viser en standardkonfiguration af kunde.

![Eksempelkonfiguration af kunde](media/default-customer-configuration1.png)

Du kan beholde de fleste af standardværdierne i skærmen kundedetaljer, men to værdier skal ændres.

1. Udvid **Salgsordrestandarder** i skærmen med kundedetaljer.
1. Vælg eller angiv et forudkonfigureret websted på rullelisten **Angiv**.
1. Vælg eller angiv et forudkonfigureret lagersted på rullelisten **Lagersted**.

Følgende billede viser et eksempel på konfiguration af kunde.

![Eksempel på konfiguration af kunde](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)
