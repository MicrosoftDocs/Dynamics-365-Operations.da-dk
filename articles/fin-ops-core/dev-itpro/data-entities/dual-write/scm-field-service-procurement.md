---
title: Integrere indkøb mellem Supply Chain Management og Field Service
description: Dette emne beskriver, hvordan integration med dobbeltskrivning understøtter oprettelse og opdateringer af indkøbsordrer fra både Supply Chain Management og Field Service.
author: RichardLuan
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: fcbede8b1a0a9a1dfcb9acbfd7cadb49eb48eecd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750684"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Integrere indkøb mellem Supply Chain Management og Field Service

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management leverer stabile indkøbsfunktionaliteter. Dynamics 365 Field Service tilbyder lignende funktioner, der understøtter de indkøbsprocesser, der er knyttet til serviceprocessen. Funktionerne i disse to apps er integreret via dobbeltskrivning, og de deraf tværfunktionelle use cases aktiveres via tabeltilknytninger, løsningslogik, visninger og formularer.

Denne integration understøtter oprettelse af indkøbsordrer og – i de fleste tilfælde – opdateringer fra begge apps. Supply Chain Management styrer dog prisfastsættelse, adresser og produktkvitteringer. Flere effektive tværfunktionelle use cases er aktiveret for organisationer, der både bruger Field Service og Supply Chain Management. Disse use cases gør det muligt at starte og spore indkøb på tværs af begge systemer.

I følgende illustration vises tabellerne i begge systemer, og hvordan de er knyttet til hinanden. Indkøbsordrer i Field Service henviser til en *kontorække*, mens indkøbsordrer i Supply Chain Management henviser til en *kreditorrække*. Dobbeltskrivning løser integrationen ved at bruge en henvisning til at sammenkæde *kreditorrækker* med *kontorækker*. Du kan finde flere oplysninger i [Integreret kreditormaster](vendor-mapping.md).

![Tilknytninger til indkøb](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Forudsætninger

Du kan integrere Supply Chain Management med Field Service ved at installere følgende komponenter:

- Field Service-version 8.8.31.60 eller nyere med henblik på omfattende integration af indkøbsordrer
- Supply Chain Management version 10.0.14 eller nyere
- Dobbeltskrivning for at køre OnePSSCM-løsningen

## <a name="installation-guidelines"></a>Installationsvejledning

### <a name="prerequisites"></a>Forudsætninger

- **Dobbeltskrivning** – Yderligere oplysninger finder du på [Startside for dobbeltskrivning](dual-write-home-page.md#dual-write-setup).
- **Dynamics 365 Field Service** – Du kan finde flere oplysninger i [Sådan installerer du Dynamics 365 Field Service](https://docs.microsoft.com/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service).

Når dobbeltskrivning og Field Service er aktiveret i Microsoft Dataverse, introducerer de flere løsningslag, der udvider miljøet med nye metadata, formularer, visninger og logik. Disse løsninger kan aktiveres i vilkårlig rækkefølge, selvom installationen typisk udføres i følgende rækkefølge:

1. **Field Service Common** – Field Service Common installeres, når Field Service er installeret i miljøet.
2. **Field Service (Anchor)** – Field Service (Anchor) installeres, når Field Service er installeret i miljøet. 
3. **Supply Chain Management Extended** – Supply Chain Management Extended installeres automatisk, når dobbeltskrivning er aktiveret i et miljø. 
4. **OneFSSCM-løsning** – OneFSSCM installeres automatisk af den løsning (Field Service eller Supply Chain Management), der installeres sidst.

    - Hvis Field Service allerede er installeret i miljøet, og du aktiverer dobbeltskrivning, som installerer Supply Chain Management Extended, installeres OneFSSCM.
    - Hvis Supply Chain Management Extended allerede er installeret i miljøet, og du installerer Field Service, installeres OneFSSCM.

## <a name="initial-synchronization"></a>Første synkronisering

Hvis du vil oprette nye indkøbsordrer og arbejde med eksisterende indkøbsordrer, skal du synkronisere referencedataene mellem Supply Chain Management og Dataverse. Du kan bruge den første skrivefunktion til at registrere tabelrelationer og finde de tabeller, du skal aktivere for et bestemt kort.

Du skal synkronisere følgende tabeller:

- Produktskabeloner

    Når du kører den første skrivning, får du en komplet liste over de tabeller, der kræves. Her er nogle eksempler på disse skabeloner:

    - Alle produkter
    - Frigivne produkter V2
    - Dataverse frigav specifikke produkter

- Steder
- Lagersteder
- Skabeloner til indkøbskategorier

    Her er nogle eksempler på disse skabeloner:

    - Indkøbskategorier
    - Pro
    - Hierarki for produktkategori
    - Tildelinger af produktkategori

- Kreditorskabeloner, f.eks. Kreditor V2
- Kontaktpersonskabeloner, f.eks. Dataverse kontakter V2
- Arbejderskabeloner, f.eks. Arbejder

Synkronisering af tabellerne sikrer, at alle dokumenter (indkøbsordrer og produktkvitteringer) i Supply Chain Management er tilgængelige i Dataverse.

### <a name="account-and-vendor-tables"></a>Konto- og kreditortabeller

Indkøbsordrer i Field Service er baseret på kontotabellen til sporing af kreditorer. Dataverse-tabellerne for indkøbsordrer bruger derfor konti til at spore kreditorer. For at tage højde for denne vigtige forskel skal følgende fire arbejdsgange være aktiveret, for at kontiene og kreditorerne kan synkroniseres: 

- Oprette kreditorer i tabellen Konti
- Oprette kreditorer i tabellen Kreditorer
- Opdatere kreditorer i tabellen Konti
- Opdatere kreditorer i tabellen Kreditorer

Hvis OneCMSCM er installeret, da både Field Service og Supply Chain Management Extended er installeret, aktiveres disse arbejdsgange automatisk. Hvis Field Service ikke er installeret, men du vil integrere indkøbsordretabellerne med Dataverse, skal du aktivere disse arbejdsgange. Medmindre du starter fra bunden, skal du i begge tilfælde sikre dig, at alle kreditorer oprettes som konti i Dataverse, før du opretter indkøbsordrer. Ellers kan der opstå fejl.

### <a name="initial-synchronization"></a>Første synkronisering

Når alle forudsætningerne er opfyldt, og hvis du ønsker, at eksisterende indkøbsordrer og produktkvitteringer skal være tilgængelige i begge systemer, skal du foretage en første synkronisering af følgende skabeloner:

- Indkøbsordrehoved V2
- CDS-indkøbsordrelinje
- Ikke-permanent sletning af CDS-indkøbsordrelinje
- Indkøbsordrekvittering
- Produkt på indkøbsordrekvittering

## <a name="mappings-with-logic"></a>Tilknytninger med logik

Indkøbsintegrationen udvider produkttilknytningen med følgende logik for at sikre, at kolonnen **Field Service-produkttype** er korrekt angivet i produkttabellen i Dataverse:

- Hvis **Produkttype** angives til *Produkt* og **Varemodelgruppe, produkt på lager** angives til *Sand*, angives **Field Service-produkttype** til *Lager*.
- Hvis **Produkttype** angives til *Produkt* og **Varemodelgruppe, produkt på lager** angives til *Falsk*, angives **Field Service-produkttype** til *Ikke på lager*.
- Hvis **Produkttype** angives til *Service*, angives **Field Service-produkttype** til *Service*.

Dataverse omfatter desuden logik, som knytter kreditorer til deres relaterede konti. Denne logik angiver standardfakturakreditorkontoen. Ved oprettelsen angiver plug-in-logikken på serversiden standardfakturakreditorkontoen ud fra den kreditor, der er relateret til kontoen. Kreditoren har en reference til den fakturakonto, der bruges til at angive denne værdi.

## <a name="supported-scenarios"></a>Understøttede scenarier

- Indkøbsordrer kan oprettes og opdateres af Dataverse-brugere. Processen og dataene styres dog af Supply Chain Management. Begrænsningerne for opdateringer af indkøbsordrekolonner i Supply Chain Management gælder, når opdateringer kommer fra Field Service. Du kan f.eks. ikke opdatere en indkøbsordre, hvis den er blevet færdiggjort. 
- Hvis indkøbsordren styres af ændringsstyring i Supply Chain Management, kan en Field Service-bruger kun opdatere indkøbsordren, når godkendelsesstatussen for Supply Chain Management er *Kladde*.
- Flere kolonner administreres kun af Supply Chain Management og kan ikke opdateres i Field Service. Hvis du vil vide, hvilke kolonner der ikke kan opdateres, kan du gennemse tilknytningstabellerne i produktet. For nemheds skyld er de fleste af disse kolonner angivet til skrivebeskyttet på Dataverse-sider. 

    Kolonnerne for prisoplysninger administreres f.eks. af Supply Chain Management. Supply Chain Management har samhandelsaftaler, som Field Service kan få fordel af. Kolonner som f.eks. **Enhedspris**, **Rabat** og **Nettobeløb** kommer kun fra Supply Chain Management. Hvis du vil sikre dig, at prisen synkroniseres med Field Service, skal du bruge funktionen **Synkronisering** på siderne **Indkøbsordre** og **Indkøbsordreprodukt** i Dataverse, når der er angivet indkøbsordredata. Du kan finde flere oplysninger under [Synkronisere med Dynamics 365 Supply Chain Management-indkøbsdata efter behov](#sync-procurement).

- Kolonnen **Totaler** er kun tilgængelig i Field Service, da der ikke er nogen opdaterede totaler for indkøbsordren i Supply Chain Management. Totalerne i Supply Chain Management beregnes ud fra flere parametre, der ikke er tilgængelige i Field Service.
- Indkøbsordrelinjer, for hvilke der kun er angivet en indkøbskategori, eller hvor det angivne produkt er en vare af produkttypen *Service* eller Field Service, kan kun startes i Supply Chain Management. Linjerne synkroniseres derefter til Dataverse og vises i Field Service.
- Hvis der kun er installeret Field Service, og ikke Supply Chain Management, er kolonnen **Lagersted** obligatorisk på indkøbsordren. Men hvis Supply Chain Management er installeret, er dette krav lempet, da Supply Chain Management tillader indkøbsordrelinjer, når der ikke er angivet et lagersted i bestemte situationer.
- Produktkvitteringerne (indkøbsordrekvitteringerne i Dataverse) administreres af Supply Chain Management og kan ikke oprettes fra Dataverse, hvis Supply Chain Management er installeret. Produktkvitteringerne fra Supply Chain Management synkroniseres fra Supply Chain Management til Dataverse.
- Underlevering er tilladt i Supply Chain Management. OneFSSCM-løsningen tilføjer logik, så når produktkvitteringslinjen (eller produktet på indkøbsordrekvitteringen i Dataverse) oprettes eller opdateres, oprettes der en lagerkladderække i Dataverse for at regulere det restantal, der er bestilt, for scenarier med underlevering.

## <a name="unsupported-scenarios"></a>Ikke-understøttede scenarier

- Field Service forhindrer, at der føjes linjer til en annulleret indkøbsordre i Supply Chain Management. Som en løsning kan du ændre systemstatus for indkøbsordren i Field Service og derefter tilføje den nye linje i enten Field Service eller Supply Chain Management.
- Selvom indkøbsrækker påvirker lagerniveauer i begge systemer, sikrer denne integration ikke lagerjustering på tværs af Supply Chain Management og Field Service. Både Field Service og Supply Chain Management har andre processer til opdatering af lagerniveauer. Disse processer ligger uden for indkøbsområdet.

## <a name="status-management"></a>Statusstyring

Statusserne for indkøbsordrer i Field Service er forskellige fra statusserne i Supply Chain Management.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Statusser for indkøbsordrer og indkøbsordreprodukter i Field Service

| Overskrift – systemstatus | Overskrift – godkendelsesstatus | Varestatus |
|---|---|---|
| <ul><li>Udkast</li><li>Sendt</li><li>Annulleret</li><li>Modtagne produkter</li><li>Faktureret</li></ul> | <ul><li>Null</li><li>Godkendt</li><li>Afvist</li></ul> | <ul><li>Udestående</li><li>Modtaget</li><li>Annulleret</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Statusser for indkøbsordrer og indkøbsordrelinjer i Supply Chain Management

Statusser for linjegodkendelse er kun aktive, når der er en linjearbejdsgang.

| Overskrift – dokumentstatus | Overskrift – godkendelsesstatus | Linjestatus | Status for linjegodkendelse |
|---|---|---|---|
| <ul><li>Åben ordre (restordre)</li><li>Modtaget</li><li>Er faktureret</li><li>Annulleret</li></ul> | <ul><li>Udkast</li><li>Til gennemsyn</li><li>Godkendt</li><li>Afvist</li><li>Til eksternt gennemsyn</li><li>Bekræftet</li><li>Færdiggjort</li></ul> | <ul><li>Åben ordre (restordre)</li><li>Modtaget</li><li>Er faktureret</li><li>Annulleret</li></ul> | <ul><li>Ikke sendt</li><li>Til gennemsyn</li><li>Godkendt</li><li>Afvist</li></ul> |

Følgende regler anvendes på statuskolonnerne:

- Statussen i Supply Chain Management kan ikke opdateres fra Field Service. I nogle tilfælde vil status i Field Service dog blive opdateret, når status for indkøbsordren i Supply Chain Management ændres.
- Hvis en indkøbsordre i Supply Chain Management er under ændringsstyring, og en ændring behandles, er godkendelsesstatussen *Kladde* eller *Til gennemsyn*. I dette tilfælde angives Field Service-godkendelsesstatussen til *Null*.
- Hvis godkendelsesstatussen for indkøbsordren i Supply Chain Management er angivet til *Godkendt*, *Til eksternt gennemsyn*, *Bekræftet* eller *Afsluttet*, angives godkendelsesstatussen for Field Service-indkøbsordren til *Godkendt*.
- Hvis godkendelsesstatussen for indkøbsordren i Supply Chain Management er angivet til *Afvist*, angives godkendelsesstatussen for Field Service-indkøbsordren til *Afvist*.
- Hvis dokumenthovedstatussen i Supply Chain Management ændres til *Åben ordre (restordre)*, og status for Field Service-indkøbsordren er *Kladde* eller *Annulleret*, ændres statussen for Field Service-indkøbsordren til *Sendt*.
- Hvis dokumenthovedstatussen i Supply Chain Management ændres til *Annulleret*, og der ikke er knyttet nogen produkter på indkøbsordrekvitteringen i Field Service til indkøbsordren (via indkøbsordreprodukter), angives Field Service-systemstatussen til *Annulleret*.
- Hvis statussen for indkøbsordrelinjen i Supply Chain Management er *Annulleret*, angives statussen for indkøbsordreprodukter i Field Service til *Annulleret*. Hvis statussen for indkøbsordrelinjen i Supply Chain Management derudover ændres fra *Annulleret* til *Restordre*, angives statussen for indkøbsordreproduktet i Field Service til *Afventer*.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Synkronisere med Supply Chain Management-indkøbsdata efter behov

Supply Chain Management omfatter indkøbsdata, der håndterer samhandelsaftaler, rabatter og andre scenarier, der er afhængige af sekundære processer i Supply Chain Management. Indkøbsprogrammet bruger komplekse regler til at bestemme den bedste pris for en given indkøbsordre. Når du bruger dobbeltskrivning, bevares datamængden ikke altid synkront på tværs af de to miljøer, især i scenarier, hvor rækken blev oprettet eller opdateret fra Dataverse, og kan udløse opfølgningsprocesser i Supply Chain Management.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Synkronisere indkøbsdataene fra Supply Chain Management

1. Gå til **Lager \> Indkøbsordre** i Dataverse.
2. Vælg **Ny** for at oprette en ny indkøbsordre eller vælg rækken for en eksisterende indkøbsordre.
3. Fra indkøbsordren eller indkøbsordrelinjen.
4. Vælg **Synkronisering** i handlingsruden.

Alle kolonner fra Dataverse og Field Service, som deles af Supply Chain Management, synkroniseres.

Her kan du se situationer, hvor du kan bruge funktionen **Synkronisering**:

- Hvis du foretager flere efterfølgende ændringer af samme række fra Dataverse, skal du køre funktionen **Synkronisering**.
- Hvis du ikke er sikker på, om en ændring er den sekundære efterfølgende ændring fra Dataverse, kan det give mening at køre funktionen **Synkronisering**.
- Hvis du modtager en fejlmeddelelse om opdatering af en værdi fra Supply Chain Management, skal du køre funktionen **Synkronisering** og derefter køre opdateringen igen i Dataverse.

## <a name="cancelling-the-posting-process"></a>Annullere bogføringsprocessen

Hvis bogføringsprocessen for produktkvitteringen annulleres under behandlingen, så kan dobbeltskrivning muligvis oprette en produktkvitteringsrække i Dataverse, men uden at oprette produktkvitteringsrække i Supply Chain Management. Denne situation opstår, fordi dobbeltskrivning ikke understøtter distribueret transaktioner.

## <a name="templates"></a>Skabeloner

Følgende skabeloner er tilgængelige for integrationen af indkøbsrelaterede dokumenter.

| Supply Chain Management | Field Service | Betegnelse |
|---|---|---|
| Indkøbsordrehoved V2 | msdyn\_Purchaseorders | Denne tabel indeholder de kolonner, der repræsenterer indkøbsordrehovedet. |
| Enhed for indkøbsordrelinje | msdyn\_PurchaseOrderProducts | Denne tabel indeholder de rækker, der repræsenterer linjer på en indkøbsordre. Produktnummeret bruges til synkronisering. Dette identificerer produktet som en lagerenhed (SKU), herunder produktdimensioner. Du kan finde flere oplysninger om produktintegration med Dataverse i [Samlet produktoplevelse](product-mapping.md). |
| Hoved til produktkvittering | msdyn\_purchaseorderreceipts | Denne tabel indeholder de produktkvitteringshoveder, der oprettes, når en produktkvittering bogføres i Supply Chain Management. |
| Produktkvitteringslinje | msdyn\_purchaseorderreceiptproducts | Denne tabel indeholder de produktkvitteringslinjer, der oprettes, når en produktkvittering bogføres i Supply Chain Management. |
| Ikke-permanent sletgtet enhed for indkøbsordrelinje | msdyn\_purchaseorderproducts | Denne tabel indeholder oplysninger om ikke-permanent slettede indkøbsordrelinjer. En indkøbsordrelinje i Supply Chain Management kan kun slettes ikke-permanent, når indkøbsordren er bekræftet eller godkendt, hvis ændringsstyring er slået til. Rækken findes i Supply Chain Management-databasen og er markeret som **IsDeleted**. Da begrebet for ikke-permanent sletning ikke findes i Dataverse, er det vigtigt, at disse oplysninger synkroniseres til Dataverse. På den måde kan linjer med ikke-permanent sletning i Supply Chain Management automatisk slettes fra Dataverse. I dette tilfælde findes logikken til sletning af en linje i Dataverse i Supply Chain Management Extended. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/productreceiptheader-msdyn-purchaseorderreceipts.md)]

[!include [Currency](includes/productreceiptline-msdyn-purchaseorderreceiptproducts.md)]

[!include [Currency](includes/purchaseorderheadersv2-msdyn-purchaseorders.md)]

[!include [Currency](includes/purchaseorderlinesoftdeletedtable-msdyn-purchaseorderproducts.md)]

[!include [Currency](includes/purchaseorderlinetable-msdyn-purchaseorderproducts.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]