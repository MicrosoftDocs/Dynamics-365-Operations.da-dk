---
title: Installere, konfigurere og opdatere kundeportalen
description: Denne artikel indeholder licensoplysninger og opsætningsinstruktioner til kundeportalen.
author: Henrikan
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8344212e66cb57ea8c9d4e8c2cdfbf022bc199c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850577"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Installere, konfigurere og opdatere kundeportalen

[!include [banner](../includes/banner.md)]


## <a name="licensing-requirements"></a>Licenskrav

Hvis du vil implementere kundeportalen, skal du have følgende licenser:

- **Power Apps-portaler** – Denne licens kræves for at være vært for kundeportalen. Portaler gives i licens baseret på brug. Du kan finde flere oplysninger i [Licenskrav til Power Apps-portaler](/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Dobbeltskrivning** – Du skal have de nødvendige licenser for at kunne aktivere dobbeltskrivning til Supply Chain Management-tabeller. Du kan finde flere oplysninger under [Systemkrav til dobbeltskrivning](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Afhængigheder af dobbeltskrivning og Power Apps-portaler

Kundeportalen er afhængig af Power Apps-portaler og dobbeltskrivning som vist i følgende illustration.

![Kundeportalafhængigheder.](media/customer-portal-elements.png "Kundeportalafhængigheder")

I modsætning til andre funktioner i Supply Chain Management findes kundeportalskabelonen i Power Apps-portaler. Derfor er kundeportalen begrænset af den funktionalitet og de funktioner, der leveres af Power Apps-portal og tabeller i dobbelskrivning.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Krævet opsætning for at aktivere kundeportalen

Når du har fundet ud af, om du har de påkrævede licenser, kan du konfigurere dobbeltskrivning som beskrevet i [Instruktioner for indledende synkronisering af dobbeltskrivning](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-entity-map.md).

Sørg for at aktivere følgende tabeltilknytninger i dobbeltskrivning:

- Salgsordreoverskrift
- Salgsordredetaljer
- Konti
- Kontakter
- Produkter

Når denne konfiguration er fuldført, kan du klargøre kundeportalskabelonen.

## <a name="provision-the-customer-portal"></a>Klargøring af kundeportalen

Før du går i gang, skal du sikre dig, at du allerede har fuldført den [krævede opsætning](#required-setup). Udfør derefter følgende trin for at klargøre kundeportalen.

1. Gå til [make.powerapps.com](https://make.powerapps.com/).
2. Sørg for at bruge det miljø, hvor du aktiverede dobbeltskrivning.
3. Under fanen **Opret** skal du rulle ned til sektionen **Start fra skabelon** og vælge den skabelon, der har navnet **Kundeportal**.
4. Følg vejledningen på skærmen.

Når klargøring er fuldført, kan du få adgang til kundeportalen i sektionen **Dine apps** på **Startsiden**.

> [!NOTE]
> Hvis dobbeltskrivningsløsningen ikke er installeret i det miljø, du arbejder i, får du vist en fejlmeddelelse, og kundeportalen vil ikke være tilgængelig.

## <a name="update-the-customer-portal"></a>Opdatering af kundeportalen

Der kan blive føjet flere funktioner til kundeportalen senere. Eventuelle ændringer, som Microsoft foretager af de underliggende løsningskomponenter, vises automatisk i dit miljø. Det websted, der er klargjort i dit miljø, afspejler dog ikke automatisk ændringer, der er foretaget i konfigurationsdataene. Du skal anvende disse ændringer manuelt ved at hente koden fra den nye skabelon og flette den med det klargjorte websted.

## <a name="additional-resources"></a>Yderligere ressourcer

Hvis du vil vide, hvordan du kan konfigurere og tilpasse kundeportalen, skal du starte med at gennemgå følgende dokumentation for de underliggende teknologier:

- [Power Apps-dokumentationen til portaler](/powerapps/maker/portals/overview)
- [Dokumentationen til dobbeltskrivning](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

For at kunne styre dine portaler effektivt skal du forstå Power Apps-portalerne og Microsoft Dataverse-livscyklus. Du kan finde flere oplysninger i følgende ressourcer:

- [Om portalens livscyklus](/powerapps/maker/portals/admin/portal-lifecycle)
- [Opgradering af en portal](/powerapps/maker/portals/admin/upgrade-portal)
- [Overflytning af portalkonfiguration](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Solution Lifecycle Management: Dynamics 365 for Customer Engagement-apps](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]