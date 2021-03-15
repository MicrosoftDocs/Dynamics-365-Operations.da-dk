---
title: Oversigt over kanaler
description: Dette emne indeholder en oversigt over kanaler i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: e060fe2a578296f079653244ed4d5676313e5ea8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963054"
---
# <a name="channels-overview"></a>Oversigt over kanaler


[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over kanaler i Microsoft Dynamics 365 Commerce. Den indeholder oplysninger om de opgaver, du skal udføre, både før og efter du har oprettet hver kanal.

## <a name="types-of-channels"></a>Kanaltyper

Dynamics 365 Commerce understøtter tre forskellige kanaltyper: detail, callcenter og onlinekanaler.

### <a name="retail-channels"></a>Detailkanaler

Detailkanaler repræsenterer standardbutikker til fysisk produkter. Hver butik kan have sine egne POS-kasseapparater, indtægt- og udgiftskonti samt medarbejdere. 

### <a name="call-center-channels"></a>Call center-kanaler

Callcenter-kanaler viser callcenter-ordrer og kundestyring.

### <a name="online-channels"></a>Onlinekanaler

Onlinekanaler viser online e-handelsudstillingsvinduer. Når der er oprettet en onlinekanal, skal der oprettes et websted vha. værktøjet Microsoft Dynamics 365 Commerce Site Builder eller en anden tredjeparts e-handelsløsning.

## <a name="channel-setup-basics"></a>Grundlæggende konfiguration af kanal

Kanalopsætningen udføres i Commerce-værktøjet. Hver kanal kan have sine egne betalingsmetoder, prisgrupper, produkthierarkier, sortimenter og sæt af produkter. Når du har oprettet en kanal, kan du tildele de produkter, som skal føres i denne butik. Hver kanaltype har et unikt sæt funktioner, der evt. skal konfigureres. En detailkanal skal f.eks. have tildelt medarbejdere, kasseapparater og kunder. Når der er oprettet en ny kanal, skal den tildeles et organisationshierarki.

## <a name="channel-setup-prerequisites"></a>Forudsætninger for konfiguration af kanal

Før du kan konfigurere en kanal, skal du fuldføre nogle forudsætningsopgaver ud fra kanaltypen. Du kan finde flere oplysninger i [Forudsætninger for konfiguration af kanal](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Konfigurer en kanal

Når du har fuldført de nødvendige opgaver, skal du bruge følgende links for at få yderligere oplysninger.

- [Konfigurer en detailkanal](channel-setup-retail.md)
- [Konfigurere en callcenter-kanal](channel-setup-callcenter.md)
- [Konfigurere en onlinekanal](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Yderligere ressourcer

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Konfigurer en detailkanal](channel-setup-retail.md)
    
[Konfigurere en onlinekanal](channel-setup-online.md)

[Konfigurere en callcenter-kanal](channel-setup-callcenter.md)

[Konfigurer organisationshierarkier](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]