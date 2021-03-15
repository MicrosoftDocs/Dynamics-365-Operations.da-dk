---
title: Konfigurere en mailbeskedprofil
description: Dette emne beskriver, hvordan du opretter en mailbeskedprofil i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
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
ms.openlocfilehash: 9378fb200a239433f2023bb90f72840dace1c0eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000818"
---
# <a name="set-up-an-email-notification-profile"></a>Konfigurere en mailbeskedprofil


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter en mailbeskedprofil i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Før du opretter kanaler, skal du oprette en profil for at sikre, at mailbeskeder kan sendes ud fra forskellige hændelser, f.eks. ordreoprettelse, ordreforsendelsesstatus og betalingsfejl.

Du kan finde yderligere oplysninger om mailkonfiguration i [Konfigurere og sende e-mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Oprette en mailbeskedprofil

Benyt følgende fremgangsmåde for at oprette en mailbeskedprofil.

1. I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-profil for mailbesked**.
1. Klik på **Ny** i handlingsruden.
1. Angiv et navn, der identificerer profilen, i feltet **Profil til e-mail-besked**.
1. Indtast en relevant beskrivelse i feltet **Beskrivelse**.
1. Angiv parameteren **Aktiv** til **Ja**.

### <a name="create-an-email-template"></a>Opret en mailskabelon

Før du kan oprette en mailbesked, skal du oprette en mailskabelon for organisationen, der indeholder oplysninger om afsenderens mail og mailskabelonen.

Benyt følgende fremgangsmåde for at oprette en mailskabelon.

1. I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabelon til organisationsmail**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I feltet **Mail-id** sal du angive et id, der kan hjælpe med at identificere denne skabelon.
1. Indtast navnet på afsenderen i feltet **Afsenders e-mailadresse**.
1. Indtast en meningsfuld beskrivelse i feltet **E-mail-beskrivelse**.
1. I feltet **Afsenders e-mailadresse** skal du angive afsenderens mailadresse.
1. I sektionen **Generelt** kan du angive eventuelle valgfrie oplysninger, der er nødvendige (f.eks. prioriteringen af mail).
1. Udvid sektionen **E-mailbeskedens indhold**, og vælg **Ny** for at oprette skabelonindholdet. Vælg sproget for hvert indholdselement, og angiv emnelinjen i mailen. Hvis der skal være indhold i mailen, skal du sørge for at markere afkrydsningsfeltet **Har indhold**.
1. Vælg **E-mail-besked** i handlingsruden for at oprette en skabelon til mailindholdet.

Følgende billede viser eksempler på indstillinger for mailskabeloner.

![Mailskabelonindstillinger](media/email-template.png)

### <a name="create-an-email-event"></a>Opret en mailhændelse

Benyt følgende fremgangsmåde for at oprette en mailhændelse.

1. I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-profil for mailbesked**.
1. Find og vælg den ønskede post på listen. 
1. Vælg mailskabelonen fra rullelisten **Mail-id**.
1. Vælg den relevante **E-mailbeskedtype** på rullelisten.
1. Marker afkrydsningsfeltet **Aktiv**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser eksempler på indstillinger for hændelsesbeskeder.

![Indstillinger for hændelsesbesked](media/email-notification-profile.png)

### <a name="next-steps"></a>Næste trin

Før du kan sende mails, skal du konfigurere tjenesten til udgående mail og konfigurere et batchjob. Du kan få flere oplysninger under [Konfigurere og sende mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).


## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere og sende mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Oversigt over organisationer og organisationshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]