---
title: Synkroniser aftalefakturaer i Field Service til fritekstfakturaer i Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere aftalefakturaer i Dynamics 365 Field Service med fritekstfakturaer i Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 21a77a0289055285f47323803a484c012e662e3a
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102728"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Synkroniser aftalefakturaer i Field Service til fritekstfakturaer i Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere aftalefakturaer i Dynamics 365 Field Service med fritekstfakturaer i Dynamics 365 Supply Chain Management.

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af aftalefakturaer fra Field Service til fritekstfakturaer i Supply Chain Management.

**Navnet på skabelonen i Dataintegration**

- Aftalefakturaer (Field Service til Supply Chain Management)

**Navnene på opgaverne i dataintegrationsprojekt**

- Fakturahoveder
- Fakturalinjer

Følgende synkroniseringsopgaver kræves, før aftalefakturaer kan synkroniseres:

- Konti (Sales til Supply Chain Management) - Direkte

## <a name="entity-set"></a>Enhedssæt

| Field Service  | Supply Chain Management                 |
|----------------|----------------------------------------|
| fakturaer       | Dataverse-debitorfakturahoveder i fri tekst |
| invoicedetails | Dataverse-debitorfakturalinjer i fri tekst   |

## <a name="entity-flow"></a>Enhedsflow

Fakturaer, der er oprettet ud fra en aftale i Field Service, kan synkroniseres til Supply Chain Management via et Microsoft Dataverse-dataintegrationsprojekt. Opdateringer til disse fakturaer synkroniseres til fritekstfakturaer i Supply Chain Management, hvis fritekstfakturaers regnskabsstatus er **Igangværende**. Når fritekstfakturaerne er bogført i Supply Chain Management, og regnskabsstatussen er opdateret til **Fuldført**, kan du ikke længere synkronisere opdateringer fra Field Service.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service

Kolonnen **Har linjer, der stammer fra aftale** er blevet føjet til tabellen **Faktura**. Denne kolonne er med til at sikre, at kun fakturaer, der er oprettet ud fra en aftale, bliver synkroniseret. Værdien er **sand**, hvis fakturaen indeholder mindst en fakturalinje, der stammer fra en aftale.

Kolonnen **Har linjer, der stammer fra aftale** er blevet føjet til tabellen **Fakturalinje**. Denne kolonne er med til at sikre, at kun fakturalinjer, der er oprettet ud fra en aftale, bliver synkroniseret. Værdien er **sand**, hvis fakturalinjen stammer fra en aftale.

**Fakturadato** er et obligatorisk felt i Supply Chain Management. Derfor skal kolonnen have en værdi i Field Service, før synkroniseringen udføres. For at opfylde disse krav, tilføjes følgende logik:

- Hvis kolonnen **Fakturadato** er tom i tabellen **Faktura** (hvis det ingen værdi rummer), angives det til dags dato, når der tilføjes en fakturalinje, der stammer fra en aftale.
- Brugeren kan ændre kolonnen **Fakturadato**. Når brugeren forsøger at gemme en faktura, der stammer fra en aftale, modtager vedkommende imidlertid en fejl i forretningsprocessen, hvis kolonnen **Fakturadato** er tom på fakturaen.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

### <a name="in-supply-chain-management"></a>I Supply Chain Management

Fakturaens oprindelse skal konfigureres af hensyn til integration for at kunne skelne fritekstfakturaer i Supply Chain Management, der er oprettet ud fra aftalefakturaer i Field Service. Når en faktura har en fakturaoprindelse af typen **Integration af aftalefaktura**, vises feltet **Eksternt fakturanummer** på hovedet **Salgsfaktura**.

Udover at blive vist i fakturahovedet kan oplysninger for **Eksternt fakturanummer** bruges til at sikre, at fakturaer, der er oprettet ud fra Field Service-aftalefakturaer, filtreres fra under fakturasynkroniseringen fra Supply Chain Management til Field Service.

1. Gå til **Debitor** \> **Opsætning** \> **Oprindelseskoder for faktura**.
2. Vælg **Ny** til at oprette en ny fakturaoprindelse.
3. I feltet **Fakturaoprindelse** skal du angive et navn for fakturaoprindelsen, f.eks. **FS**.
4. Angiv en beskrivelse i feltet **Beskrivelse** som f.eks. **Aftalefaktura i Field Service**.
5. Markér afkrydsningsfeltet **Tildeling af oprindelsestype**.
6. Angiv feltet **Fakturaoprindelsestype** til **Integration af aftalefaktura**.
7. Vælg **Gem**.

### <a name="in-the-data-integration-project"></a>I dataintegrationsprojektet

Opgave: **Fakturalinjer**  

Sørg for, at standardværdien for feltet **Visningsværdi for hovedkonto** i Supply Chain Management opdateres, så det svarer til den ønskede værdi.

Standardskabelonværdien er **401100**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Aftalefakturaer (Field Service til Supply Chain Management): Fakturaoverskrifter

[![Tilknytning af skabelon i Dataintegration for fakturahoveder](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Aftalefakturaer (Field Service til Supply Chain Management): Fakturalinjer

[![Tilknytning af skabelon i Dataintegration for fakturalinjer](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]