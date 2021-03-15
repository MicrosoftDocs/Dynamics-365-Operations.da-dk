---
title: Synkroniser arbejdsordrer i Field Service til salgsordrer i Supply Chain Management
description: Dette emne beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer i Field Service til salgsordrer i Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: f9395d39a68cd11f57262c791dd7646975c5e516
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998497"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-supply-chain-management"></a>Synkroniser arbejdsordrer i Field Service til salgsordrer i Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer i Dynamics 365 Field Service med salgsordrer i Dynamics 365 Supply Chain Management.

[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)


## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Følgende skabeloner og underliggende opgaver bruges til køre synkroniseringen af arbejdsordrer i Field Service til salgsordrer i Supply Chain Management.

### <a name="names-of-the-templates-in-data-integration"></a>Navne på skabeloner i dataintegration:

Skabelonen **Arbejdsordrer til salgsordrer (Field Service til Supply Chain Management)** bruges til at køre synkronisering.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Navnene på opgaverne i dataintegrationsprojekt

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Følgende synkroniseringsopgaver kræves, før salgsordrehoveder og -linjer kan synkroniseres:

- Field Service-produkter (Supply Chain Management til Field Service).
- Konti (Sales til Supply Chain Management) - Direkte

## <a name="entity-set"></a>Enhedssæt

| **Field Service** | **Supply Chain Management** |
|-------------------------|-------------------------|
| msdyn_workorders        | Dataverse-salgsordrehoveder |
| msdyn_workorderservices | Dataverse-salgsordrelinjer   |
| msdyn_workorderproducts | Dataverse-salgsordrelinjer   |

## <a name="entity-flow"></a>Enhedsflow

Arbejdsordrer oprettes i Field Service. Hvis arbejdsordrer kun indeholder eksternt vedligeholdte produkter, og værdien **Status for arbejdsordre** adskiller sig fra **Åben – ikke planlagt** og **Lukket – Annulleret**, kan arbejdsordrer synkroniseres til Supply Chain Management via et Microsoft Dataverse-dataintegrationsprojekt. Opdateringer af arbejdsordrer synkroniseres som salgsordrer i Supply Chain Management. Disse opdateringer omfatter oplysninger om oprindelsestype og status.

## <a name="estimated-versus-used"></a>Estimeret vs. Brugt

I Field Service har produkter og tjenester på arbejdsordrer både værdier for **Estimeret** og **Brugt** for antal og beløb. I Supply Chain Management gælder der ikke de samme værdier for **Estimeret** og **Brugt** for salgsordrer. For at understøtte produktfordeling, der bruger det forventede antal på salgsordren i Supply Chain Management, men bevarer det anvendte antal, der skal forbruges og faktureres, synkroniseres produkterne og tjenesterne på arbejdsordren i to sæt opgaver. Et sæt opgaver gælder værdier for **Estimeret** værdier, og et andet sæt af opgaver gælder værdier for **Brugt**.

Denne funktionsmåde muliggør scenarier, hvor estimerede værdier bruges til fordeling eller reservation i Supply Chain Management, mens værdier for brugte produkter anvendes til forbrug og fakturering.

### <a name="estimated"></a>Estimeret

Til synkronisering af produktlinjer anvendes værdier for **Estimeret**, når værdien **Linjestatus** er **Estimeret**, **Fordelt** er angivet til **Ja**, og værdien for **Systemstatus** ikke er **Lukket – Bogført**.

Til synkronisering af servicelinjer anvendes værdier for **Estimeret**, når værdien **Linjestatus** er **Estimeret** og værdien for **Systemstatus** ikke er **Lukket – Bogført**.

### <a name="used"></a>Brugt

Værdierne for **Brugt** bruges til forbrug og fakturering. I disse tilfælde synkroniseres værdierne for **Brugt**.

Følgende tabel indeholder en oversigt over de forskellige kombinationer for produktlinjer.

| Systemstatus <br>(Field Service) | Linjestatus <br>(Field Service) | Fordelt <br>(Field Service) |Synkroniseret værdi <br>(Supply Chain Management) |
|--------------------|-------------|-----------|---------------------------------|
| Åben - planlagt   | Forkalkuleret   | Ja       | Forkalkuleret                       |
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

| Systemstatus <br>(Field Service) | Linjestatus <br>(Field Service) | Synkroniseret værdi <br>(Supply Chain Management) |
|--------------------|-------------|-----------|
| Åben - planlagt   | Forkalkuleret   | Forkalkuleret |
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

    I dette eksempel bliver produktets værdi for **Brugt antal** på **0** (nul) og tjenestens værdi for **Estimeret antal** på **2 t** synkroniseret til Supply Chain Management.

2. Produkter, der er fordelt i Field Service.

    Værdien for **Systemstatus** er **Åben – Planlagt**.

    - **Produktserie:** Estimeret antal = 5 styk, Brugt antal = 0 styk, Linjestatus = Estimeret, Fordelt = Ja
    - **Servicelinje:** Estimeret antal = 2 t, Brugt antal = 0 t, Linjestatus = Estimeret

    I dette eksempel bliver produktets værdi for **Estimeret antal** på **5ea** og tjenestens værdi for **Estimeret antal** på **2 t** synkroniseret til Supply Chain Management.

3. Serviceteknikeren begynder at arbejde på arbejdsordren og registrerer et materialeforbrug på 6.

    Værdien for **Systemstatus** er **Åben – I gang**.

    - **Produktserie:** Estimeret antal = 5 styk, Brugt antal = 6 styk, Linjestatus = Brugt, Fordelt = Ja
    - **Servicelinje:** Estimeret antal = 2 t, Brugt antal = 0 t, Linjestatus = Estimeret

    I dette eksempel bliver produktets værdi for **Brugt antal** på **6** og tjenestens værdi for **Estimeret antal** på **2 t** synkroniseret til Supply Chain Management.

4. Serviceteknikeren fuldfører arbejdsordren og registrerer brugt tid til 1,5 timer.

    Værdien for **Systemstatus** er **Åben – Fuldført**.

    - **Produktserie:** Estimeret antal = 5 styk, Brugt antal = 6 styk, Linjestatus = Brugt, Fordelt = Ja
    - **Servicelinje:** Estimeret antal = 2 t, Brugt antal = 1,5 t, Linjestatus = Brugt

    I dette eksempel bliver produktets værdi for **Brugt antal** på **6** og tjenestens værdi for **Brugt antal** på **1,5 t** synkroniseret til Supply Chain Management.

## <a name="sales-order-origin-and-status"></a>Salgsordres oprindelse og status

### <a name="sales-origin"></a>Ordreoprindelse

For at holde styr på salgsordrer, der stammer fra arbejdsordrer, kan du oprette en salgsoprindelse, hvor **Tildeling af oprindelsestype** er angivet til **Ja**, og **Salgsoprindelsestype** er angivet til **Arbejdsordreintegration**.

Som standard vælger tilknytningen salgsoprindelsen for salgoprindelsestypen **Arbejdsordreintegration** for alle salgsordrer, der er oprettet ud fra arbejdsordrer. Denne funktionsmåde kan være nyttig, når du arbejder med salgsordren i Supply Chain Management. Du skal sikre dig, at salgsordrer, der stammer fra arbejdsordrer, ikke synkroniseres tilbage til Field Service som arbejdsordrer.

Oplysninger om, hvordan du opsætter salgsoprindelse korrekt i Supply Chain Management, finder du i afsnittet "Betingelserne og tilknytningsopsætning" i dette emne.

### <a name="status"></a>Status

Når salgsordren stammer fra en arbejdsordre, vises feltet **Status for ordre på eksternt arbejde** på fanen **Opsætning** i salgsordrehovedet. Feltet viser systemstatussen fra arbejdsordren i Field Service, så du kan spore status for synkroniserede arbejdsordrer for salgsordrer i Supply Chain Management. Dette felt kan også hjælpe brugeren med at fastlægge, hvornår ordren skal leveres eller faktureres.

Feltet **Status for ordre på eksternt arbejde** kan have følgende værdier:

- Åben - planlagt
- Åben - i gang
- Åben - fuldført
- Lukket - bogført

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service

For at understøtte integrationen mellem Field Service og Supply Chain Management kræves der yderligere funktionalitet fra CRM-løsningen i Field Service. Løsningen indeholder følgende ændringer.

### <a name="work-order-entity"></a>Arbejdsordreenhed

Feltet **Har kun eksternt vedligeholdte produkter** er blevet føjet til enheden **Arbejdsordre** og vises på siden. Den bruges til at spore, om en arbejdsordre, udelukkende består af eksternt vedligeholdte produkter. En arbejdsordre består udelukkende af eksternt vedligeholdte produkter, når alle relaterede produkter vedligeholdes i Supply Chain Management. Dette felt er med til at sikre, at brugere ikke synkroniserer arbejdsordrer, der omfatter produkter, som er ukendte.

### <a name="work-order-product-entity"></a>Arbejdsordres produktenhed

- Feltet **Ordre har kun eksternt vedligeholdte produkter** er blevet føjet til enheden **Arbejdsordres produkt** og vises på siden. Det bruges til at sikre en ensartet sporing af, om arbejdsordrens produkt vedligeholdes i Supply Chain Management. Dette felt er med til at sikre, at brugere ikke synkroniserer produkter for arbejdsordrer, som er ukendte i Supply Chain Management.
- Feltet **Status for hovedsystem** er blevet føjet til enheden **Arbejdsordres produkt** og vises på siden. Det bruges til at sikre en ensartet sporing af systemstatus for arbejdsordren og korrekt filtrering, når arbejdsordrers produkter synkroniseres til Supply Chain Management. Når der aktiveres filtre for integrationsopgaver, bruges oplysningerne for **Status for hovedsystem** også til at fastlægge, om de estimerede eller brugte værdier skal synkroniseres.
- Feltet **Faktureret enhedspris** viser det beløb, der faktureres pr. faktiske enhed, som bruges. Værdien beregnes som **Samlet beløb** divideret med værdien **Faktisk antal**. Feltet bruges til integration med systemer, der ikke understøtter forskellige værdier for det brugte antal og det fakturerede antal. Dette felt vises ikke på brugergrænsefladen (UI). 
- Feltet **Faktureret rabatbeløb** beregnes som værdien **Rabatbeløb** plus afrundingen fra beregningen af værdien for **Faktureret pris**. Dette felt bruges til integration og vises ikke på brugergrænsefladen.
- Feltet **Antal som decimal** gemmer værdien fra feltet **Antal** som et decimaltal. Dette felt bruges til integration og vises ikke på brugergrænsefladen. 
- Værdien i felterne **Brugt** nulstilles til **0** (nul), hvis værdien **Linjestatus** for arbejdsordrets produkt ændres fra **Brugt** til **Estimeret**. Denne ændring forebygger situationer, hvor et brugt antal, der er angivet ved en fejl, bruges til synkronisering, når værdien for **Linjestatus** er **Estimeret**, og indstillingen **Fordelt** er angivet til **Nej**.

### <a name="work-order-service-entity"></a>Arbejdsordres serviceenhed

- Feltet **Ordre har kun eksternt vedligeholdte produkter** er blevet føjet til enheden **Arbejdsordres service** og vises på siden. Det bruges til at sikre en ensartet sporing af, om arbejdsordretjenesten vedligeholdes i Supply Chain Management. Dette felt er med til at sikre, at brugere ikke synkroniserer produkter for arbejdsordretjenester, som er ukendte i Supply Chain Management.
- Feltet **Status for hovedsystem** er blevet føjet til enheden **Arbejdsordres service** og vises på siden. Det bruges til at sikre en ensartet sporing af systemstatus for arbejdsordren og korrekt filtrering, når arbejdsordretjenester synkroniseres til Supply Chain Management. Når der aktiveres filtre for integrationsopgaver, bruges oplysningerne for **Status for hovedsystem** også til at fastlægge, om de estimerede eller brugte værdier skal synkroniseres.
- Feltet **Varighed i timer** gemmer værdien fra feltet **Varighed**, når værdien konverteres fra minutter til timer. Dette felt bruges til integration og vises ikke på brugergrænsefladen.
- Feltet **Estimeret varighed i timer** gemmer værdien fra feltet **Estimeret varighed**, når værdien konverteres fra minutter til timer. Dette felt bruges til integration og vises ikke på brugergrænsefladen.
- Feltet **Faktureret enhedspris** gemmer det beløb, der faktureres pr. faktiske enhed, som bruges. Værdien beregnes som **Samlet beløb** divideret med værdien **Faktisk antal**. Dette felt bruges til integration med systemer, der ikke understøtter forskellige værdier for det brugte antal og det fakturerede antal. Feltet vises ikke på brugergrænsefladen.
- Feltet **Faktureret rabatbeløb** beregnes som værdien **Rabatbeløb** plus afrundingen fra beregningen af værdien for **Faktureret pris**. Dette felt bruges til integration og vises ikke på brugergrænsefladen.
- Feltet **Ekstern linjeordre** er et beregnet negativt linjeordrenummer, der kan bruges i eksterne systemer, hvor arbejdsordrens produkt og servicelinjerne kombineres. Dette felt gør det muligt, at indsatte produkter for arbejdsordrer får positive linjenumre, og at tjenester for arbejdsordrer får negative linjenumre. Værdien af dette feltet beregnes som værdien **Linjeordre** ganget med -1. Dette felt vises ikke på brugergrænsefladen.
- Værdien i felterne **Brugt** nulstilles til **0** (nul), hvis værdien **Linjestatus** for arbejdsordrets service af en eller anden grund ændres fra **Brugt** til **Estimeret**. Denne ændring forebygger situationer, hvor et brugt antal, der er angivet ved en fejl, bruges til synkronisering, når værdien for **Linjestatus** er **Estimeret**, og værdien for **Status for hovedsystem** er angivet til **Lukket – Bogført**.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

Før du synkroniserer arbejdsordrer, er det vigtigt, at du opdaterer følgende indstillinger i systemerne.

### <a name="setup-in-field-service"></a>Opsætning i Field Service

- Sørg for, at den nummerserie, der bruges til arbejdsordrer i Field Service, ikke overlapper den nummerserie, der bruges til salgsordrer i Supply Chain Management. Ellers kan eksisterende salgsordrer blive forkert opdateret i Field Service eller Supply Chain Management.
- Feltet **Oprettelse af faktura for arbejdsordre** skal være angivet til **Aldrig**, da faktureringen udføres fra Supply Chain Management. Gå til **Field Service** \> **Indstillinger** \> **Administration** \> **Indstillinger for Field Service**, og kontroller, at feltet **Oprettelse af faktura for arbejdsordre** er angivet til **Aldrig**.

### <a name="setup-in-supply-chain-management"></a>Opsætning i Supply Chain Management

Arbejdsordrens integration kræver, at du angiver salgsoprindelsen. Salgsoprindelsen bruges til at skelne salgsordrer i Supply Chain Management, der er oprettet ud fra arbejdsordrer i Field Service. Når en salgsordre har en salgsoprindelse af typen **Arbejdsordreintegration**, vises feltet **Status for ordre på eksternt arbejde** i salgsordrehovedet. Desuden sikrer salgsoprindelsen, at salgsordrer, der er oprettet ud fra arbejdsordrer i Field Service, filtreres fra under synkronisering af salgsordrer fra Supply Chain Management til Field Service.

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

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderheader"></a>Arbejdsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderHeader

Filter: (msdyn_systemstatus ne 690970005) og (msdyn_systemstatus ne 690970000) og (msdynce_hasexternallymaintainedproductsonly eq true)

[![Skabelontilknytning i dataintegration](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineestimate"></a>Arbejdsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderServiceLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og (msdyn_linestatus eq 690970000) og (msdynce_headersystemstatus ne 690970004)

[![Skabelontilknytning i dataintegration](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineused"></a>Arbejdsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderServiceLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og ((msdyn_linestatus eq 690970001) eller (msdynce_headersystemstatus eq 690970004))

[![Skabelontilknytning i dataintegration](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineestimate"></a>Arbejdsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderServiceLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og (msdyn_linestatus eq 690970000) og (msdynce_headersystemstatus ne 690970004) og (msdyn_allocated eq true)

[![Skabelontilknytning i dataintegration](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineused"></a>Arbejdsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderProductLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og ((msdyn_linestatus eq 690970001) eller (msdynce_headersystemstatus eq 690970004) eller (msdyn_allocated ne true))

[![Skabelontilknytning i dataintegration](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]