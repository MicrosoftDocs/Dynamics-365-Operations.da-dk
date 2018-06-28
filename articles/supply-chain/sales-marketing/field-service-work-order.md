---
title: Synkronisere arbejdsordrer i Field Service med salgsordrer i Finance and Operations
description: Dette emne beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer i Field Service til salgsordrer i Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 8914723f6ef436bfc9e3a98cc82d5486042b0761
ms.openlocfilehash: 250b7caa1e1495140d0d4f688ecae4acb8814467
ms.contentlocale: da-dk
ms.lasthandoff: 06/07/2018

---

# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-finance-and-operations"></a>Synkronisere arbejdsordrer i Field Service med salgsordrer i Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer i Microsoft Dynamics 365 for Field Service til salgsordrer i Microsoft Dynamics 365 for Finance and Operations.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

Dette emne beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer i Field Service til salgsordrer i Finance and Operations.

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Følgende skabeloner og underliggende opgaver bruges til køre synkroniseringen af arbejdsordrer i Field Service til salgsordrer i Finance and Operations.

### <a name="names-of-the-templates-in-data-integration"></a>Navne på skabeloner i dataintegration:

Skabelonen **Arbejdsordrer til salgsordrer (Field Service til Fin and Ops)** bruges til at køre synkronisering.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Navnene på opgaverne i dataintegrationsprojekt

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Følgende synkroniseringsopgaver kræves, før salgsordrehoveder og -linjer kan synkroniseres:

- Field Service-produkter (Fin and Ops til Field Service)
- Konti (Sales til Finance and Operations) – Direkte

## <a name="entity-set"></a>Enhedssæt

| **Field Service** | **Finance and Operations** |
|-------------------------|-------------------------|
| msdyn_workorders        | CDS-salgsordrehoveder |
| msdyn_workorderservices | CDS-salgsordrelinjer   |
| msdyn_workorderproducts | CDS-salgsordrelinjer   |

## <a name="entity-flow"></a>Enhedsflow

Arbejdsordrer oprettes i Field Service. Hvis arbejdsordrer indeholder kun eksternt vedligeholdte produkter, og værdien **Status for arbejdsordre** adskiller sig fra **Åben – ikke planlagt** og **Lukket – Annulleret**, kan arbejdsordrer synkroniseres til Finance and Operations via et CDS-dataintegrationsprojekt Opdateringer af arbejdsordrer synkroniseres som salgsordrer i Finance and Operations. Disse opdateringer omfatter oplysninger om oprindelsestype og status.

## <a name="estimated-versus-used"></a>Estimeret vs. Brugt

I Field Service har produkter og tjenester på arbejdsordrer både værdier for **Estimeret** og **Brugt** for antal og beløb. I Finance and Operations har salgsordrer ikke samme opfattelse af værdier for **Estimeret** og **Brugt**. For at understøtte produktfordeling, der bruger det forventede antal på salgsordren i Finance and Operations, men bevarer det anvendte antal, der skal forbruges og faktureres, synkroniseres produkterne og tjenesterne på arbejdsordren i to sæt opgaver. Et sæt opgaver gælder værdier for **Estimeret** værdier, og et andet sæt af opgaver gælder værdier for **Brugt**.

Denne funktionsmåde muliggør scenarier, hvor estimerede værdier bruges til fordeling eller reservation i Finance and Operations, mens værder for brugte produkter og tjenester anvendes til forbrug og fakturering.

### <a name="estimated"></a>Estimeret

Til synkronisering af produktlinjer anvendes værdier for **Estimeret**, når værdien **Linjestatus** er **Estimeret**, **Fordelt** er angivet til **Ja**, og værdien for **Systemstatus** ikke er **Lukket – Bogført**.

Til synkronisering af servicelinjer anvendes værdier for **Estimeret**, når værdien **Linjestatus** er **Estimeret** og værdien for **Systemstatus** ikke er **Lukket – Bogført**.

### <a name="used"></a>Brugt

Værdierne for **Brugt** bruges til forbrug og fakturering. I disse tilfælde synkroniseres værdierne for **Brugt**.

Følgende tabel indeholder en oversigt over de forskellige kombinationer for produktlinjer.

| Systemstatus <br>(Field Service) | Linjestatus <br>(Field Service) | Fordelt <br>(Field Service) |Synkroniseret værdi <br>(Finance and Operations) |
|--------------------|-------------|-----------|---------------------------------|
| Åben - planlagt   | Estimeret   | Ja       | Estimeret                       |
| Åben - planlagt   | Estimeret   | Nr.        | Brugt                            |
| Åben - planlagt   | Brugt        | Ja       | Brugt                            |
| Åben - planlagt   | Brugt        | Nr.        | Brugt                            |
| Åben - i gang | Estimeret   | Ja       | Estimeret                       |
| Åben - i gang | Estimeret   | Nr.        | Brugt                            |
| Åben - i gang | Brugt        | Ja       | Brugt                            |
| Åben - i gang | Brugt        | Nr.        | Brugt                            |
| Åben - fuldført   | Estimeret   | Ja       | Estimeret                       |
| Åben - fuldført   | Estimeret   | Nr.        | Brugt                            |
| Åben - fuldført   | Brugt        | Ja       | Brugt                            |
| Åben - fuldført   | Brugt        | Nr.        | Brugt                            |
| Lukket - bogført    | Estimeret   | Ja       | Brugt                            |
| Lukket - bogført    | Estimeret   | Nr.        | Brugt                            |
| Lukket - bogført    | Brugt        | Ja       | Brugt                            |
| Lukket - bogført    | Brugt        | Nr.        | Brugt                            |

Følgende tabel indeholder en oversigt over de forskellige kombinationer for servicelinjer.

| Systemstatus <br>(Field Service) | Linjestatus <br>(Field Service) | Synkroniseret værdi <br>(Finance and Operations) |
|--------------------|-------------|-----------|
| Åben - planlagt   | Estimeret   | Estimeret |
| Åben - planlagt   | Brugt        | Brugt      |
| Åben - i gang | Estimeret   | Estimeret |
| Åben - i gang | Brugt        | Brugt      |
| Åben - fuldført   | Estimeret   | Estimeret |
| Åben - fuldført   | Brugt        | Brugt      |
| Lukket - bogført    | Estimeret   | Brugt      |
| Lukket - bogført    | Brugt        | Brugt      |

Synkronisering af værdier for **Estimeret** vs. **Brugt** administreres gennem de to sæt opgaver for produktlinjer og servicelinjer. Foruddefinerede filtre udløser den rette opgave, og den underliggende tilknytning er med til at sikre, at de rette værdier for **Forventet** vs. **Brugt** bliver synkroniseret.

### <a name="example"></a>Eksempel

1. En arbejdsordre er oprettet og planlagt i Field Service.

    Værdien for **Systemstatus** er **Åben – Planlagt**.

    - **Produktserie:** Estimeret antal = 5 styk, Brugt antal = 0 styk, Linjestatus = Estimeret, Fordelt = Nej
    - **Servicelinje:** Estimeret antal = 2 t, Brugt antal = 0 t, Linjestatus = Estimeret

    I dette eksempel bliver produktets værdi for **Brugt antal** på **0** (nul) og tjenestens værdi for **Estimeret antal** på **2 t** synkroniseret til Finance and Operations.

2. Produkter, der er fordelt i Field Service.

    Værdien for **Systemstatus** er **Åben – Planlagt**.

    - **Produktserie:** Estimeret antal = 5 styk, Brugt antal = 0 styk, Linjestatus = Estimeret, Fordelt = Ja
    - **Servicelinje:** Estimeret antal = 2 t, Brugt antal = 0 t, Linjestatus = Estimeret

    I dette eksempel bliver produktets værdi for **Estimeret antal** på **5 styk** og tjenestens værdi for **Estimeret antal** på **2 t** synkroniseret til Finance and Operations.

3. Serviceteknikeren begynder at arbejde på arbejdsordren og registrerer et materialeforbrug på 6.

    Værdien for **Systemstatus** er **Åben – I gang**.

    - **Produktserie:** Estimeret antal = 5 styk, Brugt antal = 6 styk, Linjestatus = Brugt, Fordelt = Ja
    - **Servicelinje:** Estimeret antal = 2 t, Brugt antal = 0 t, Linjestatus = Estimeret

    I dette eksempel bliver produktets værdi for **Brugt antal** på **6** og tjenestens værdi for **Estimeret antal** på **2 t** synkroniseret til Finance and Operations.

4. Serviceteknikeren fuldfører arbejdsordren og registrerer brugt tid til 1,5 timer.

    Værdien for **Systemstatus** er **Åben – Fuldført**.

    - **Produktserie:** Estimeret antal = 5 styk, Brugt antal = 6 styk, Linjestatus = Brugt, Fordelt = Ja
    - **Servicelinje:** Estimeret antal = 2 t, Brugt antal = 1,5 t, Linjestatus = Brugt

    I dette eksempel bliver produktets værdi for **Brugt antal** på **6** og tjenestens værdi for **Brugt antal** på **1,5 t** synkroniseret til Finance and Operations.

## <a name="sales-order-origin-and-status"></a>Salgsordres oprindelse og status

### <a name="sales-origin"></a>Ordreoprindelse

For at holde styr på salgsordrer i Finance and Operations, der stammer fra arbejdsordrer, kan du oprette en salgsoprindelse, hvor **Tildeling af oprindelsestype** er angivet til **Ja** og **Salgsoprindelsestype** er angivet til **Arbejdsordreintegration**.

Som standard vælger tilknytningen salgsoprindelsen for salgoprindelsestypen **Arbejdsordreintegration** for alle salgsordrer, der er oprettet ud fra arbejdsordrer. Denne funktionsmåde kan være nyttig, når du arbejder med salgsordren i Finance and Operations. Du skal sikre dig, at salgsordrer, der stammer fra arbejdsordrer, ikke synkroniseres tilbage til Field Service som arbejdsordrer.

Oplysninger om, hvordan du opsætter salgsoprindelse korrekte i Finance and Operations, finder du i afsnittet "Forudsætninger og tilknytningsopsætning" i dette emne.

### <a name="status"></a>Status

Når salgsordren stammer fra en arbejdsordre, vises feltet **Status for ordre på eksternt arbejde** på fanen **Opsætning** i salgsordrehovedet. Feltet viser systemstatus fra arbejdsordren i Field Service, så du kan spore status for synkroniserede arbejdesordrer for salgsordrer i Finance and Operations. Dette felt kan også hjælpe brugeren af Finance and Operations med at fastlægge, hvornår ordren skal leveres eller faktureres.

Feltet **Status for ordre på eksternt arbejde** kan have følgende værdier:

- Åben - planlagt
- Åben - i gang
- Åben - fuldført
- Lukket - bogført

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service

For at understøtte integrationen mellem Field Service og Finance and Operations, kræves yderligere funktioner fra CRM-løsningen i Field Service. Løsningen indeholder følgende ændringer.

### <a name="work-order-entity"></a>Arbejdsordreenhed

Feltet **Har kun eksternt vedligeholdte produkter** er blevet føjet til enheden **Arbejdsordre** og vises på siden. Den bruges til at spore, om en arbejdsordre, udelukkende består af eksternt vedligeholdte produkter. En arbejdsordre består udelukkende af eksternt vedligeholdte produkter, når alle relaterede produkter vedligeholdes i Finance and Operations. Dette felt er med til at sikre, at brugere ikke synkroniserer arbejdsordrer, der omfatter produkter, som er ukendte i Finance and Operations.

### <a name="work-order-product-entity"></a>Arbejdsordres produktenhed

- Feltet **Ordre har kun eksternt vedligeholdte produkter** er blevet føjet til enheden **Arbejdsordres produkt** og vises på siden. Den bruges til at sikre en ensartet sporing af, om arbejdsordrens produkt vedligeholdes i Finance and Operations. Dette felt er med til at sikre, at brugere ikke synkroniserer produkter for arbejdsordrer, som er ukendte i Finance and Operations.
- Feltet **Status for hovedsystem** er blevet føjet til enheden **Arbejdsordres produkt** og vises på siden. Den bruges til at sikre en ensartet sporing af systemstatus for arbejdsordren og korrekt filtrering, når arbejdsordrers produkter synkroniseres til Finance and Operations. Når der aktiveres filtre for integrationsopgaver, bruges oplysningerne for **Status for hovedsystem** også til at fastlægge, om de estimerede eller brugte værdier skal synkroniseres.
- Feltet **Faktureret enhedspris** viser det beløb, der faktureres pr. faktiske enhed, som bruges. Værdien beregnes som **Samlet beløb** divideret med værdien **Faktisk antal**. Feltet bruges til integration med systemer, der ikke understøtter forskellige værdier for det brugte antal og det fakturerede antal. Dette felt vises ikke på brugergrænsefladen (UI). 
- Feltet **Faktureret rabatbeløb** beregnes som værdien **Rabatbeløb** plus afrundingen fra beregningen af værdien for **Faktureret pris**. Dette felt bruges til integration og vises ikke på brugergrænsefladen.
- Feltet **Antal som decimal** gemmer værdien fra feltet **Antal** som et decimaltal. Dette felt bruges til integration og vises ikke på brugergrænsefladen. 
- Værdien i felterne **Brugt** nulstilles til **0** (nul), hvis værdien **Linjestatus** for arbejdsordrets produkt ændres fra **Brugt** til **Estimeret**. Denne ændring forebygger situationer, hvor et brugt antal, der er angivet ved en fejl, bruges til synkronisering, når værdien for **Linjestatus** er **Estimeret**, og indstillingen **Fordelt** er angivet til **Nej**.

### <a name="work-order-service-entity"></a>Arbejdsordres serviceenhed

- Feltet **Ordre har kun eksternt vedligeholdte produkter** er blevet føjet til enheden **Arbejdsordres service** og vises på siden. Den bruges til at sikre en ensartet sporing af, om arbejdsordrens service vedligeholdes i Finance and Operations. Dette felt er med til at sikre, at brugere ikke synkroniserer tjenester for arbejdsordrer, som er ukendte i Finance and Operations.
- Feltet **Status for hovedsystem** er blevet føjet til enheden **Arbejdsordres service** og vises på siden. Den bruges til at sikre en ensartet sporing af systemstatus for arbejdsordren og korrekt filtrering, når arbejdsordrers tjenester synkroniseres til Finance and Operations. Når der aktiveres filtre for integrationsopgaver, bruges oplysningerne for **Status for hovedsystem** også til at fastlægge, om de estimerede eller brugte værdier skal synkroniseres.
- Feltet **Varighed i timer** gemmer værdien fra feltet **Varighed**, når værdien konverteres fra minutter til timer. Dette felt bruges til integration og vises ikke på brugergrænsefladen.
- Feltet **Estimeret varighed i timer** gemmer værdien fra feltet **Estimeret varighed**, når værdien konverteres fra minutter til timer. Dette felt bruges til integration og vises ikke på brugergrænsefladen.
- Feltet **Faktureret enhedspris** gemmer det beløb, der faktureres pr. faktiske enhed, som bruges. Værdien beregnes som **Samlet beløb** divideret med værdien **Faktisk antal**. Dette felt bruges til integration med systemer, der ikke understøtter forskellige værdier for det brugte antal og det fakturerede antal. Feltet vises ikke på brugergrænsefladen.
- Feltet **Faktureret rabatbeløb** beregnes som værdien **Rabatbeløb** plus afrundingen fra beregningen af værdien for **Faktureret pris**. Dette felt bruges til integration og vises ikke på brugergrænsefladen.
- Feltet **Ekstern linjeordre** er et beregnet negativt linjeordrenummer, der kan bruges i eksterne systemer, hvor arbejdsordrens produkt og servicelinjerne kombineres. Dette felt gør det muligt, at indsatte produkter for arbejdsordrer får positive linjenumre, og at tjenester for arbejdsordrer får negative linjenumre. Værdien af dette feltet beregnes som værdien **Linjeordre** ganget med -1. Dette felt vises ikke på brugergrænsefladen.
- Værdien i felterne **Brugt** nulstilles til **0** (nul), hvis værdien **Linjestatus** for arbejdsordrets service af en eller anden grund ændres fra **Brugt** til **Estimeret**. Denne ændring forebygger situationer, hvor et brugt antal, der er angivet ved en fejl, bruges til synkronisering, når værdien for **Linjestatus** er **Estimeret**, og værdien for **Status for hovedsystem** er angivet til **Lukket – Bogført**.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

Før du synkroniserer arbejdsordrer, er det vigtigt, at du opdaterer følgende indstillinger i systemerne.

### <a name="setup-in-field-service"></a>Opsætning i Field Service

- Sørg for, at den nummerserie, der bruges til arbejdsordrer i Field Service ikke overlapper den nummerserie, der bruges til salgsordrer i Finance and Operations. Ellers kan eksisterende salgsordrer blive forkert opdateret i Field Service eller Finance and Operations.
- Feltet **Oprettelse af faktura for arbejdsordre** skal være angivet til **Aldrig**, da faktureringen udføres fra Finance and Operations. Gå til **Field Service** \> **Indstillinger** \> **Administration** \> **Indstillinger for Field Service**, og kontroller, at feltet **Oprettelse af faktura for arbejdsordre** er angivet til **Aldrig**.

### <a name="setup-in-finance-and-operations"></a>Konfiguration i Finance and Operations

Arbejdsordrens integration kræver, at du angiver salgsoprindelsen. Salgsoprindelsen bruges til at skelne salgsordrer i Finance and Operations, der er oprettet ud fra arbejdsordrer i Field Service. Når en salgsordre har en salgsoprindelse af typen **Arbejdsordreintegration**, vises feltet **Status for ordre på eksternt arbejde** i salgsordrehovedet. Desuden sikrer salgsoprindelsen, at salgsordrer, der er oprettet ud fra arbejdsordrer i Field Service, filtreres fra under synkronisering af salgsordrer fra Finance and Operations til Field Service.

1. Gå til **Salg og marketing** \> **Opsætning** \> **Salgsordrer** \> **Salgsoprindelse**.
2. Vælg **Ny** for at oprette en ny salgsoprindelse.
3. I feltet **Salgsoprindelse** skal du angive et navn til salgsoprindelsen, f.eks. **Arbejdsordre**.
4. Angiv en beskrivelse i feltet **Beskrivelse** som f.eks. **Arbejdsordre i Field Service**.
5. Markér afkrydsningsfeltet **Tildeling af oprindelsestype**.
6. Angiv feltet **Salgsoprindelsestype** til **Arbejdsordreintegration**.
7. Vælg **Gem**.


### <a name="setup-in-data-integration"></a>Opsætning i Dataintegration

Kontroller, at **Integrationsnøgle** findes for **msdyn_workorders**
1. Gå til Dataintegration
2. Vælg fanen **Forbindelsessæt**
3. Vælg det forbindelsessæt, der bruges til synkronisering af arbejdsordre
4. Vælg fanen **Integrationsnøgle**
5. Find msdyn_workorders, og kontroller, at nøglen **msdyn_name (Work Order Number)** er tilføjer. Hvis den ikke vises, kan du tilføje den ved at klikke på **Tilføj nøgle** og klikke på **Gem** øverst på siden

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderheader"></a>Arbejdsordrer til salgsordrer (Field Service til Fin and Ops): WorkOrderHeader

Filter: (msdyn_systemstatus ne 690970005) og (msdyn_systemstatus ne 690970000) og (msdynce_hasexternallymaintainedproductsonly eq true)

[![Skabelontilknytning i dataintegration](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineestimate"></a>Arbejdsordrer til salgsordrer (Field Service til Fin and Ops): WorkOrderServiceLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og (msdyn_linestatus eq 690970000) og (msdynce_headersystemstatus ne 690970004)

[![Skabelontilknytning i dataintegration](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineused"></a>Arbejdsordrer til salgsordrer (Field Service til Fin and Ops): WorkOrderServiceLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og ((msdyn_linestatus eq 690970001) eller (msdynce_headersystemstatus eq 690970004))

[![Skabelontilknytning i dataintegration](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineestimate"></a>Arbejdsordrer til salgsordrer (Field Service til Fin and Ops): WorkOrderProductLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og (msdyn_linestatus eq 690970000) og (msdynce_headersystemstatus ne 690970004) og (msdyn_allocated eq true)

[![Skabelontilknytning i dataintegration](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineused"></a>Arbejdsordrer til salgsordrer (Field Service til Fin and Ops): WorkOrderProductLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og ((msdyn_linestatus eq 690970001) eller (msdynce_headersystemstatus eq 690970004) eller (msdyn_allocated ne true))

[![Skabelontilknytning i dataintegration](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)

