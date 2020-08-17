---
title: Oprette og administrere brugere af kundeportalen
description: Dette emne forklarer, hvordan du kan oprette brugerkonti til kundeportalen og indstille rettigheder for dem.
author: dasani-madipalli
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a751cbffd98b8d47ca7dad222f0ce374381a393d
ms.sourcegitcommit: 074fe7e77feb795148c3daf2e6ccbb8a88679343
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/31/2020
ms.locfileid: "3645307"
---
# <a name="create-and-manage-customer-portal-users"></a>Oprette og administrere brugere af kundeportalen

I out-of-box-implementeringen er der ingen måde, hvorpå brugere kan registrere sig selv for websteder, der er oprettet ved hjælp af kundeportalen. Brugere skal inviteres af administratoren for at kunne logge på og bruge et websted. Microsoft har bevidst blokeret brugernes mulighed for at registrere sig selv.

Før en bruger kan bruge et websted, skal der oprettes en kontaktpersonpost for den pågældende bruger. Denne post angiver, hvilken kundekonto og juridisk enhed brugeren tilhører. Disse oplysninger er vigtige for at sikre, at brugeren kan oprette og få vist salgsordrer.

Når brugerne selv registrerer, oprettes der automatisk kontaktposter for dem. Derfor kan du ikke sikre, at en bruger vælger den korrekte kundekonto og juridiske enhed. På den anden side giver invitationsprocessen en administrator mulighed for at tildele den korrekte kundekonto og juridiske enhed til kontaktpersonposten, før der sendes en invitation. Hvis du overvejer at tilpasse løsningen, så brugerne kan registrere sig selv, skal du huske på de mulige konsekvenser.

## <a name="video"></a>Video
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

Videoen [Inviter kunder til at registrere og bruge din tilpassede portal](https://youtu.be/drGUYHX9QIQ) (vist ovenfor) er inkluderet i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.

## <a name="prerequisite-setup"></a>Forudsætninger for opsætning

Kontaktpersoner i Power Apps-portaler gemmes som poster i enheden **Kontaktpersoner** i Common Data Service. Dobbeltskrivning synkroniserer derefter disse poster med Microsoft Dynamics 365 Supply Chain Management som påkrævet.

![Systemdiagram for kundeportal-kontaktpersoner](media/customer-portal-contacts.png "Systemdiagram for kundeportal-kontaktpersoner")

Før du begynder at invitere nye kunder, skal du sikre dig, at du har aktiveret enhedstilknytningen **Kontakt** i dobbeltskrivning.

## <a name="the-invitation-process"></a>Invitationsprocessen

Hvis du vil invitere en eksisterende kontaktperson til kundeportalen, skal du følge trinnene i [Inviter kontaktpersoner til dine portaler](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) i dokumentation for Power Apps-portaler.

Før du inviterer en kunde til at deltage i kundeportalen, skal du kontrollere, at kundens [kontaktpersonpost](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) er tilgængelig og konfigureret på følgende måde:

1. Angiv feltet til **Firma** for den juridiske enhed, som du ønsker, kunden skal tilhøre i Supply Chain Management.
2. Angiv feltet **Kontonummer** til det kundekontonummer, som du ønsker, kunden skal have i Supply Chain Management.

Når en kontakt er oprettet, skal du kunne se den i Supply Chain Management.

Du kan finde flere oplysninger under [Konfigurere en kontaktperson til brug på en portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) i dokumentationen for Power Apps-portaler.

## <a name="out-of-box-web-roles-and-entity-permissions"></a>Out-of-box-webroller og enhedstilladelser

Brugerroller i Power Apps-portaler defineres af [webroller](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) og [enhedstilladelser](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions). Der er defineret nogle få roller for kundeportalen lige fra starten. Du kan oprette nye roller, og du kan redigere eller fjerne eksisterende roller.

### <a name="out-of-box-web-roles"></a>Out-of-box-webroller

I dette afsnit beskrives de webroller, der leveres sammen med kundeportalen.

Du kan finde flere oplysninger om, hvordan du redigerer out-of-box-brugerrollerne under [Oprette webroller til portaler](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) og [Tilføje postbaseret sikkerhed ved at bruge enhedstilladelser til portaler](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) i dokumentationen for Power Apps-portaler.

#### <a name="administrator"></a>Administrator

Administratoren overvåger og vedligeholder webstedet. Denne person klargør og konfigurerer kundeportalen. Administratoren vedligeholder lT- og sikkerhedsmæssige aspekter ved portalen og sørger for, at alting fungerer problemfrit. Administratoren kan også tilpasse og/eller ændre portalen ved at tilføje nye funktioner, oprette nye roller og meget mere.

#### <a name="customer-representative"></a>Kundeservicerepræsentant

En kunderepræsentant arbejder for en kundevirksomhed og er ansvarlig for at administrere de ordrer, som firmaet afgiver. Kunderepræsentanten kan se alle de ordrer, der er bestilt til virksomheden, og de brugere, der har placeret dem. Desuden kan kunderepræsentanten se oplysninger om den overordnede konto, og hvilke kontaktpersoner der kan afgive ordrer på vegne af den pågældende konto.

#### <a name="authorized-users"></a>Autoriserede brugere

Godkendte brugere kan afgive ordrer og få vist statussen for de ordrer, de har afgivet. De kan dog ikke få vist status for ordrer, som andre brugere i firmaet har afgivet.

#### <a name="unauthorized-users"></a>Autoriserede brugere

Uautoriserede brugere kan ikke få vist nogen data. De kan kun se offentlige oplysninger, f.eks. vilkår og betingelser, samt oplysninger om det firma, der kører kundeportalen.

#### <a name="example"></a>Eksempel

Følgende tabel viser, hvilke salgsordrer brugerne i de enkelte webroller kan se i systemet.

| Salgsordre | Administrator | Kunderepræsentant for kunde&nbsp;X | Autoriseret bruger: Jane | Autoriseret bruger: Sam | Uautoriseret bruger: May |
|---|---|---|---|---|---|
| Kunde&nbsp;X-bestiller:&nbsp;Jane | Ja | Ja | Ja | Ingen | Ingen |
| Kunde&nbsp;X-bestiller:&nbsp;Sam | Ja | Ja | Ingen | Ja | Ingen |
| Kunde&nbsp;Y-bestiller:&nbsp;May | Ja | Ingen | Ingen | Ingen | Ingen |

> [!NOTE]
> Selvom både Sam og Jane er kontaktpersoner, der arbejder for kunde X, kan de kun se de ordrer, de selv har afgivet, og intet andet. Selvom May har en ordre i systemet, kan hun ikke se den pågældende ordre i kundeportalen, fordi hun er en uautoriseret bruger. (Desuden må hun have afgivet ordren via en anden kanal end kundeportalen).
