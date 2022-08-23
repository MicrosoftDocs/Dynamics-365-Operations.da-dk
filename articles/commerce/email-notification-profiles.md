---
title: Konfigurere en profil for mailbesked
description: Denne artikel beskriver, hvordan du opretter en mailbeskedprofil i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: db6c46d471e3b54982132df3e4819236833cf4a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292129"
---
# <a name="set-up-an-email-notification-profile"></a>Konfigurere en profil for mailbesked

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du opretter en mailbeskedprofil i Microsoft Dynamics 365 Commerce.

Når du opretter kanaler, kan du oprette en mailbeskedprofil. Mailbeskedprofilen definerer hændelserne i en salgstransaktion (f.eks. en ordre, der oprettes, pakkes eller faktureres), som du vil sende beskeder om til dine kunder. 

Du kan finde yderligere oplysninger om mailkonfiguration i [Konfigurere og sende e-mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).



## <a name="create-an-email-template"></a>Opret en mailskabelon

Før en type mailbesked kan aktiveres, skal du oprette en mailskabelon til organisationen i Commerce Headquarters for hver beskedtype, du vil understøtte. Denne skabelon definerer mailemnet, afsenderen, standardsproget og mailbrødteksten for hvert sprog, der understøttes.

Benyt følgende fremgangsmåde for at oprette en mailskabelon.

1. I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabelon til organisationsmail**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I feltet **Mail-id** sal du angive et id, der kan hjælpe med at identificere denne skabelon.
1. Indtast navnet på afsenderen i feltet **Afsenders e-mailadresse**.
1. Indtast en meningsfuld beskrivelse i feltet **E-mail-beskrivelse**.
1. I feltet **Afsenders e-mailadresse** skal du angive afsenderens mailadresse.
1. Vælg et standardsprog til mailskabelonen under **Generelt**. Standardsproget bruges, når der ikke findes en lokaliseret skabelon for det angivne sprog.
1. Udvid sektionen **E-mailbeskedens indhold**, og vælg **Ny** for at oprette skabelonindholdet. Vælg sproget for hvert indholdselement, og angiv emnelinjen i mailen. Hvis der skal være indhold i mailen, skal du sørge for at markere afkrydsningsfeltet **Har indhold**.
1. Vælg **E-mail-besked** i handlingsruden for at oprette en skabelon til mailindholdet.

Følgende billede viser eksempler på indstillinger for mailskabeloner.

![Mailskabelonindstillinger.](media/email-template.png)

Du kan finde flere oplysninger om, hvordan du opretter mailskabeloner, i [Oprette mailskabeloner til transaktionshændelser](email-templates-transactions.md). 

## <a name="create-an-email-notification-profile"></a>Oprette en mailbeskedprofil

Benyt følgende fremgangsmåde for at oprette en mailbeskedprofil i hovedkontoret.

1. I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-profil for mailbesked**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv et navn, der identificerer profilen, i feltet **Profil til e-mail-besked**.
1. Indtast en relevant beskrivelse i feltet **Beskrivelse**.
1. Angiv parameteren **Aktiv** til **Ja**.

## <a name="add-a-notification-type"></a>Tilføje en beskedtype

Benyt følgende fremgangsmåde for at oprette en mailhændelse.

1. I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-profil for mailbesked**.
1. Vælg **Ny** under **Indstilling for detailmailbesked**.
1. Vælg den relevante **E-mailbeskedtype** på rullelisten.
1. Vælg den mailskabelon, du har oprettet ovenfor, på rullelisten **Mail-id**.
1. Markér afkrydsningsfeltet **Aktiv**.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser eksempler på indstillinger for hændelsesbeskeder.

![Indstillinger for hændelsesbesked.](media/email-notification-profile.png)


## <a name="schedule-a-recurring-email-notification-process-job"></a>Planlægge et procesjob for en tilbagevendende mailmeddelelse

Hvis du vil sende mailbeskeder, skal du køre jobbet **Behandling af email-besked om detailordre**.

Hvis du vil oprette et batchjob i hovedkontoret til afsendelse af transaktionsmails, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Mail og beskeder \> Send mailbesked**.
1. Vælg **Gentagelse** i dialogboksen **Behandling af e-mail-besked om detailordre**.
1. Vælg **Ingen slutdato** i dialogboksen **Definer gentagelse**.
1. Vælg **Minutter** under **Gentagelsesmønster**, og angiv derefter feltet **Antal** til **1**. Med disse indstillinger sikres det, at mailbeskeder behandles så hurtigt som muligt.
1. Vælg **OK** for at returnere til dialogboksen **Behandling af e-mail-besked om detailordre**.
1. Vælg **OK** for at fuldføre jobopsætningen.

## <a name="next-steps"></a>Næste trin

Før du kan sende mails, skal du konfigurere tjenesten til udgående mail. Du kan få flere oplysninger under [Konfigurere og sende mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere og sende mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Oversigt over kanaler](channels-overview.md)

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Oversigt over organisationer og organisationshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
