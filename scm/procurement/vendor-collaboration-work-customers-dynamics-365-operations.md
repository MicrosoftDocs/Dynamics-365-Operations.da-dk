---
title: Kreditorsamarbejde med kunder
description: "Dette emne beskriver, hvordan du kan bruge kreditorsamarbejde til arbejde med indkøbsordrer og overvåge konsignationslager i Dynamics 365 for Operations."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 11cd2242b5a575ae87b0dbcf6f8ce268fcea5377
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-customers"></a>Kreditorsamarbejde med kunder

Dette emne beskriver, hvordan du kan bruge kreditorsamarbejde til arbejde med indkøbsordrer og overvåge konsignationslager i Dynamics 365 for Operations.

Dette emne beskriver, hvordan du kan bruge kreditorsamarbejde til arbejde med kunder i Microsoft Dynamics 365 for Operations. Den indeholder oplysninger om hvordan til at overvåge og reagere på indkøbsordrer og overvåge lageret til forsendelse. Du kan også bruge leverandør samarbejde til at arbejde med fakturaer. Yderligere oplysninger finder du [leverandør samarbejde fakturering arbejdsområde](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace).

## <a name="working-with-purchase-orders"></a>Arbejde med indkøbsordrer
I **Indkøbsordrebekræftelse**-arbejdsområdet kan du besvare de indkøbsordrer, der er sendt til gennemsyn. Det gør det også muligt at få vist oplysninger om indkøbsordrer, der afventer handling fra kunden, og indkøbsordrer, der er blevet bekræftet, men stadig er åbne. Der findes tre lister i **Indkøbsordrebekræftelse**-arbejdsområdet:

-   **Indkøbsordrer for revision** -denne liste viser POs, der er blevet sendt til dig og afventer et svar fra dig. Når du har reageret, forsvinder Indkøbsordren fra listen. Hvis kunden sender dig en ny version af indkøbsordren, før du har svaret på den foregående, vises kun den nyeste version.
-   **Afventer kundehandling** - På denne liste kan du se indkøbsordrer, du har besvaret, men endnu ikke er blevet bekræftet af kunden. Hvis du har accepteret indkøbsordren, kan du overvåge den på denne liste, indtil status skifter til **Bekræftet**. Hvis du har afvist indkøbsordren eller accepteret den med ændringer, kan du overvåge indkøbsordren her, indtil kunden sender en ny version.
-   **Åbn bekræftede indkøbsordrer** - Denne liste indeholder alle indkøbsordrer til din konto, der har status som **Bekræftet**. Når produkter eller tjenester er fuldt modtaget mod indkøbsordren, forsvinder indkøbsordren fra listen.

Følgende liste viser de fire sider, som du kan bruge til at arbejde med indkøbsordrer, hvoraf to indeholder de samme oplysninger som lister i arbejdsområdet:

-   **Indkøbsordrer til gennemsyn** (se ovenfor)
-   **Historik over bekræftelse af kreditor for indkøbsordre** - Denne side indeholder alle indkøbsordrer og alle versioner af indkøbsordrer, der er sendt til kreditoren, og alle de svar, der blev returneret fra kreditoren.
-   **Åbn bekræftede indkøbsordrer** (se ovenfor)
-   **Alle bekræftede indkøbsordrer** - Denne side indeholder alle indkøbsordrer, der er bekræftet, herunder dem, hvis produkter eller tjenester er modtaget. Du kan bruge denne liste til at overvåge, hvilke indkøbsordrer du kan sende fakturaer for.

### <a name="responding-to-purchase-orders"></a>Besvarelse af indkøbsordrer

De indkøbsordrer, som debitoren har sendt dig til at gennemlæse er synlige i den **købsordrebekræftelse** arbejdsområde og på den **købsordrer til gennemsyn** side. Når du åbner en Indkøbsordre, kan du acceptere det, afviser det eller acceptere den med ændringer. Der kan være vedhæftede filer på indkøbsordren eller på de enkelte linjer. Det er også muligt at tilknytte oplysninger til dit svar på indkøbsordrens hoved eller enkelte linjer. For eksempel kan du foreslå en erstatningsvare for en eller flere linjer. Du kan se og udskrive indkøbsordren som en PDF-fil ved hjælp af **Vis/Udskriv**-indstillingen. Du kan skjule eller se følgende dimensionskolonner ved hjælp af handlingen **Vis dimensioner**: Sted, lagersted, farve, størrelse, typografi, konfiguration. Hvis du bruger den **Accepter med ændringer** indstilling, kan du acceptere eller afvise individuelle linjer. Du kan også ændre de følgende linjer:

-   Ændre datoer eller antal. Hvis du vil opdatere den bekræftede leveringsdato på alle linjer, skal du bruge **Opdater leveringsdato**-indstillingen i indkøbsordrens hoved.
-   Opdele linjer for forskellige leveringsdatoer eller antal
-   Erstat en vare. Du kan gøre dette ved at angive en varebeskrivelse og et varenummer i feltet **Ekstern** i sektionen **Linjedetaljer**.

Du kan ikke ændre prisoplysninger eller gebyrer, men du kan komme med forslag til ændringer i disse ved hjælp af noter. Hvis din kunde sender dig en ny version af en indkøbsordre, har den et versionssuffiks, som angiver, at den er en ændret version af en tidligere omtalt indkøbsordre. På siden **Historik over bekræftelse af kreditor for indkøbsordre** kan du holde styr på historikken for hver ordre.

## <a name="monitoring-consignment-inventory"></a>Overvågning af konsignationslager
Hvis du bruger konsignationslager, kan du bruge kreditorsamarbejde til at få vist oplysninger på de følgende sider:

-   **Indkøbsordrer, der forbruger sending lager** -indkøbsordrer for forsendelse lager genereres, når kunden overtager ejerskabet af lageret. Disse konsignationindkøbsordrer vises kun på siden **Indkøbsordrer, der forbruger konsignationslager**. De er ikke medtaget på siden **Alle bekræftede indkøbsordrer**.
-   **Produkter, der er modtaget fra konsignationslager** - Denne side viser en liste over alle de transaktioner, hvor ejerskabet af produkter er blevet overført til den virksomhed, som forbruger af lageret. Du kan bruge disse oplysninger til at fakturere kunden.
-   **Disponibelt konsignationslager** - Denne side viser det disponible konsignationslager, der ejes af din virksomhed og er disponibelt på kundens lagersted.


<a name="see-also"></a>Se også
--------

[Administrere brugere af kreditorsamarbejde](manage-vendor-collaboration-users.md)


