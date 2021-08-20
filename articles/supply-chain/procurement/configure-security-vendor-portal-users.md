---
title: Brugersikkerhed på leverandørportal
description: Denne artikel beskriver, hvordan du konfigurerer sikkerhed for eksterne leverandører, der bruger leverandørportalen. Oplysningerne i dette emne gælder kun for versioner af Dynamics AX fra februar 2016 og maj 2016.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c99107483bd5f6901cd87897151b107d2e1fe12f277032f379b739fa10ad84c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771365"
---
# <a name="vendor-portal-user-security"></a>Brugersikkerhed på leverandørportal

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer sikkerhed for eksterne leverandører, der bruger leverandørportalen. Oplysningerne i dette emne gælder kun for versioner af Dynamics AX fra februar 2016 og maj 2016.

Kreditorportal-funktionaliteten er blevet erstattet af udvidede kreditorsamarbejdsfunktioner i Dynamics 365 for Operations version 1611. Du kan finde flere oplysninger om opsætning af sikkerhed for leverandørsamarbejde under [Konfigurere og vedligeholde kreditorsamarbejde](set-up-maintain-vendor-collaboration.md). Kreditorportalen viser et begrænset sæt oplysninger om indkøbsordrer (PO'er) til eksterne kreditorer. Det er vigtigt, at du har konfigureret brugertilladelserne for kreditorportalen i Microsoft Dynamics AX korrekt, så kreditorerne ikke utilsigtet har adgang til yderligere oplysninger i din Dynamics AX-installation. **Vigtigt!** I modsætning til andre brugere bør eksterne kreditorer ikke have rollen **Systembruger**. Rollen **Systembruger** giver adgang til et sæt rettigheder, der ikke er egnet til eksterne brugere.

## <a name="setting-up-a-vendor-portal-user"></a>Konfigurere en bruger til kreditorportalen
Før du opretter en brugerkonto til en person, der bruger kreditorportalen, skal du konfigurere kreditoren til at tillade samarbejde på kreditorportalen. Brug feltet **Indkøbsordresamarbejde** under fanen **Generelt** på siden **Kreditorer**. Eksterne kreditorer, der bruger kreditorportalen, skal have følgende opsætning:

-   En brugerkonto i Microsoft Azure Active Directory (AAD) skal være registreret for kreditoren på siden **Brugere** i Dynamics AX.
-   Kreditoren skal have sikkerhedsrollen **Kreditor (ekstern)**, ikke rollen **Systembruger**. **Bemærk!** Rollen **Systembruger** tildeles automatisk, når du opretter en ny brugerkonto i Dynamics AX. Du skal derfor fjerne denne rolle og acceptere den advarselsmeddelelse, du modtager.
-   Kreditorbrugeren bør ikke gives tilladelse til at tilføje flere felter fra PO-tabellerne til deres PO-visning. Under fanen **Brugertilpasning** skal du under fanen **Brugere** angive indstillingen **Eksplicit personlig tilpasning tilladt** for brugeren til **Nej**.
-   Brugerkontoen skal være tilknyttet en kontakt, der er registreret. Under fanen **Brugere** skal du vælge en kontakt i feltet **Navn**. Den person, du vælger, skal have rollen **Kontakt** for den pågældende kreditor.

Hvis den samme person skal have adgang til kreditorportalen for flere kreditorkonti (måske for forskellige juridiske enheder), skal hver af den pågældende persons brugerkonti være knyttet til den samme registrerede kontakt. Rollen **Kreditor (ekstern)** omfatter alle de grundlæggende funktioner, der er nødvendige for at kunne bruge de funktioner, der findes på kreditorportalen. Denne opsætning sikrer, at den brugergrænseflade, som den eksterne bruger ser, kun er fokuseret på det ønskede scenarie.

## <a name="additional-resources"></a>Yderligere ressourcer

[Samarbejde med kreditorer ved hjælp af kreditorportalen](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]