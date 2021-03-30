---
title: Tilpasse transaktionsmails efter leveringsmåde
description: Dette emne beskriver, hvordan du konfigurerer brugerdefinerede mailskabeloner for specifikke beskedtyper og leveringsmåder i Microsoft Dynamics 365 Commerce.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: d0d96ddb20b2b09751d8c0c0bf8af713de35279a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222627"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Tilpasse transaktionsmails efter leveringsmåde

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer brugerdefinerede mailskabeloner for specifikke beskedtyper og leveringsmåder i Microsoft Dynamics 365 Commerce.

Transaktionsmails kan nu tilpasses til en kombination af en beskedtype (f.eks. **Ordre oprettet**, **Ordre pakket** eller **Ordre faktureret**) og en leveringsmåde (f.eks. i løbet af natten, in-afhentning i butikken eller ved fortovskanten). Brugerdefinerede transaktionsmails gør det muligt for detailhandlerne at give deres kunder ordrer med opfyldningsoplevelser, der er skræddersyet til ordrens leveringsmåde. Hændelsen "ordre pakket" kan f.eks. tilpasses, så den giver afhentningsinstruktioner til kunder, der vælger afhentning ved fortovskanten. Alternativt kan den give oplysninger om fragtmand og levering til kunder, der vælger, at deres ordre skal afsendes.

> [!NOTE]
> Hvis du vil bruge funktionaliteten til tilpassede transaktionsmails, skal du først aktivere funktionen **Tilpasse transaktionsmails efter leveringsmåde** ved at gå til **Arbejdsområder \> Funktionsstyring** i Commerce Headquarters.

E-mails kan tilpasses efter leveringsmåde for følgende beskedtyper:

- **Ordreannullering** – Denne mailbeskedtype er ny.
- **Der er oprettet en ordre**
- **Bekræftet ordre**
- **Ordre faktureret** – Denne mailbeskedtype er ny. Den kan bruges i stedet for beskedtypen **Ordre leveret**, der sender en besked om enhver fakturahændelse, der har en afsendelsesmåden levering (ikke afhentning eller elektronisk leveringsmåde).
- **Ordre afhentet**
- **Ordre pakket**
- **Ordre klar til afhentning** – Denne beskedtype kan kun tilpasses efter leveringsmåde, hvis funktionen **Understøttelse af flere leveringsmåder for afhentning** er aktiveret. I dette tilfælde har denne beskedtype samme funktion om beskedtypen **Ordre pakket**.
- **Betalingen blev ikke udført**
- **Erstatningsordre oprettet**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>Konfigurere mailskabeloner til bestemte leveringsmåder

I denne procedure antages det, at du allerede har oprettet de nye brugerdefinerede mailskabeloner og føjet dem til siden **Skabelon til organisationsmail**. Du kan finde oplysninger om, hvordan du opretter og overfører mailskabeloner, i [Oprette e-mailskabeloner til transaktionshændelser](email-templates-transactions.md).

Hvis du vil konfigurere mailskabeloner for bestemte leveringsmåder i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Commerce-profil for mailbesked**.
1. Vælg en eksisterende beskedtype under **Indstillinger for besked om detailhændelse**.
1. Mens beskedtypen stadig er valgt, skal du vælge **Konfigurere leveringsmetoder**.
1. I dialogboksen **Leveringsmåder** skal du vælge **Ny**.
1. I feltet **Leveringsmåde** i den nye række skal du vælge en leveringsmåde.
1. Vælg den mailskabelon, der skal knyttes til leveringsmåden, i feltet **E-mail-id**.
1. Marker afkrydsningsfeltet **Aktiv**.
1. Gentag trin 4 til 7 for at tilføje flere leveringsmåder.
1. Vælg **OK**, når du er færdig.

> [!NOTE]
> - Når der findes mere end én leveringsmåde på tværs af linjer i en salgsordre, bruges standardskabelonen. Standardskabelonen er den skabelon, der er knyttet til beskedtypen på siden **Commerce-profil for mailbesked**.
> - Hvis en salgsordre har en leveringsmåde, der ikke er konfigureret til en brugerdefineret mailskabelon, bruges e-mailstandardskabelonen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette callcenter-ordrer](tasks/create-call-center-orders.md)

[Skifte leveringsmåde til i POS](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]