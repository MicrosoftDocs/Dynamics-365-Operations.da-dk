---
title: Synkronisere aftalefakturaer i Field Service med fritekstfakturaer i Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere aftalefakturaer i Microsoft Dynamics 365 for Field Service med fritekstfakturaer i Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560157"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Synkronisere aftalefakturaer i Field Service med fritekstfakturaer i Finance and Operations

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere aftalefakturaer i Microsoft Dynamics 365 for Field Service med fritekstfakturaer i Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

De følgende skabelon og underliggende opgaver bruges til at køre synkronisering af aftalefakturaer fra Field Service til fritekstfakturaer i Finans and Operations.

**Navnet på skabelonen i dataintegration:**

- Aftalefakturaer (Field Service til Finance and Operations)

**Navne på opgaverne i dataintegrationsprojektet:**

- Fakturahoveder
- Fakturalinjer

Følgende synkroniseringsopgaver kræves, før aftalefakturaer kan synkroniseres:

- Konti (Sales til Finance and Operations) – Direkte

## <a name="entity-set"></a>Enhedssæt

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| fakturaer       | CDS-debitorfakturahoveder i fri tekst |
| invoicedetails | CDS-debitorfakturalinjer i fri tekst   |

## <a name="entity-flow"></a>Enhedsflow

Fakturaer, der er oprettet ud fra en aftale i Field Service, kan synkroniseres til Finance and Operations via et Common Data Service (CDS)-dataintegrationsprojekt. Opdateringer til disse fakturaer synkroniseres til fritekstfakturaer i Finance and Operations, hvis fritekstfakturaers regnskabsstatus er **Igangværende**. Når fritekstfakturaerne er bogført i Finance and Operations, og regnskabsstatussen er opdateret til **Fuldført**, kan du ikke længere synkronisere opdateringer fra Field Service.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service

Feltet **Har linjer, der stammer fra aftale** er blevet føjet til enheden **Faktura**. Dette felt er med til at sikre, at kun fakturaer, der er oprettet ud fra en aftale, bliver synkroniseret. Værdien er **sand**, hvis fakturaen indeholder mindst en fakturalinje, der stammer fra en aftale.

Feltet **Stammer fra aftale** er blevet føjet til enheden **Fakturalinje**. Dette felt er med til at sikre, at kun fakturalinjer, der er oprettet ud fra en aftale, bliver synkroniseret. Værdien er **sand**, hvis fakturalinjen stammer fra en aftale.

**Fakturadato** er et obligatorisk felt i Finance and Operations. Derfor skal feltet have en værdi i Field Service, før synkroniseringen udføres. For at opfylde disse krav, tilføjes følgende logik:

- Hvis feltet **Fakturadato** er tomt i enheden **Faktura** (hvis det ingen værdi rummer), angives det til dags dato, når der tilføjes en fakturalinje, der stammer fra en aftale.
- Brugeren kan ændre feltet **Fakturadato**. Når brugeren forsøger at gemme en faktura, der stammer fra en aftale, modtager vedkommende imidlertid en fejl i forretningsprocessen, hvis feltet **Fakturadato** er tomt på fakturaen.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

### <a name="in-finance-and-operations"></a>I Finance and Operations

Fakturaens oprindelse skal konfigureres af hensyn til integration for at kunne skelne fritekstfakturaer i Finance and Operations, der er oprettet ud fra aftalefakturaer i Field Service. Når en faktura har en fakturaoprindelse af typen **Integration af aftalefaktura**, vises feltet **Eksternt fakturanummer** på hovedet **Salgsfaktura**.

Udover at blive vist i fakturahovedet kan oplysninger for **Eksternt fakturanummer** bruges til at sikre, at fakturaer, der er oprettet ud fra Field Service-aftalefakturaer, filtreres fra under fakturasynkroniseringen fra Finance and Operations til Field Service.

1. Gå til **Debitor** \> **Opsætning** \> **Oprindelseskoder for faktura**.
2. Vælg **Ny** til at oprette en ny fakturaoprindelse.
3. I feltet **Fakturaoprindelse** skal du angive et navn for fakturaoprindelsen, f.eks. **FS**.
4. Angiv en beskrivelse i feltet **Beskrivelse** som f.eks. **Aftalefaktura i Field Service**.
5. Markér afkrydsningsfeltet **Tildeling af oprindelsestype**.
6. Angiv feltet **Fakturaoprindelsestype** til **Integration af aftalefaktura**.
7. Vælg **Gem**.

### <a name="in-the-data-integration-project"></a>I dataintegrationsprojektet

Opgave: **Fakturalinjer**  

Sørg for, at standardværdien for feltet **Visningsværdi for hovedkonto** i Finance and Operations opdateres, så det svarer til den ønskede værdi.

Standardskabelonværdien er **401100**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a>Aftalefakturaer (Field Service til Fin and Ops): Fakturaoverskrifter

[![Skabelontilknytning i dataintegration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a>Aftalefakturaer (Field Service til Fin and Ops): Fakturalinjer

[![Skabelontilknytning i dataintegration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)
