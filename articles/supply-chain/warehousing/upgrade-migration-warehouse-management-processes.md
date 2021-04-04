---
title: Opgradere lokationsstyring fra Microsoft Dynamics AX 2012 til Supply Chain Management
description: Dette emne indeholder en oversigt over indstillinger for overflytning af produkt-og lagerstyring.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7cca089e424b617fe4075d0cdbdfd23ef0bb86be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248685"
---
# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-supply-chain-management"></a>Opgradere lokationsstyring fra Microsoft Dynamics AX 2012 til Supply Chain Management 


[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over processen for opgradering fra Microsoft Dynamics AX 2012 R3 til Supply Chain Management ved at køre modulet WMSII.

Supply Chain Management understøtter ikke længere det ældre **WMSII**-modul fra Microsoft Dynamics AX 2012. Du kan i stedet bruge modulet **Lokationsstyring**. I modulet WMSII kunne lokations- og palle-id-lagerdimensioner vælges for det økonomiske lager, men lagerdimensionen palle-id kan ikke bruges til økonomisk lager i Supply Chain Management.

Under en opgradering identificeres alle produkter, der er knyttet til en lagringsdimensionsgruppe, der bruger lagerdimensionen palle-ID, markeres som blokerede og behandles ikke til opgradering.

## <a name="upgrading-to-supply-chain-management-when-ax-2012-r3-wmsii-is-used"></a>Opgradering til Supply Chain Management, når AX 2012 R3 WMSII bruges
Efter opgraderingen kan du bruge et sæt af indstillinger i formularen **Ændre lagringsdimensionsgruppen for varer** for at fjerne blokeringen af produkter, der blev blokeret under opgraderingen, og derefter behandle transaktioner for disse produkter.

### <a name="enabling-items-in-supply-chain-management"></a>Aktivere varer i Supply Chain Management 
Denne ændring er påkrævet, fordi i Supply Chain Management er varesporing en del af processerne for lokationsstyring. For disse processer skal alle lagersteder og deres lokationer være tilknyttet en lokationsprofil. Hvis du vil bruge processer for lokationsstyring, skal følgende konfigureres:
-   Eksisterende lagersteder skal være aktiverede til at bruge lokationsstyringsprocesser 
-   Eksisterende frigivne produkter skal være tilknyttet en lagringsdimensionsgruppe, der bruger lokationsstyringsprocesser 

Hvis kildelagringsdimensionsgrupper bruger lagerdimensionen Palle-id, skal lokationen af eksisterende disponibel lagerbeholdning, der bruger Palle-id som lagerdimension, være tilknyttet en lokationsprofil, hvor **Brug nummerpladesporing**-parameteren markeres. Hvis de eksisterende lagersteder ikke skal bruges til lokationsstyringsprocesser, kan du ændre lagringsdimensionsgrupper for den eksisterende disponible lagerbeholdning til grupper, der kun håndterer Lokation-, Lagersted- og Sted-lagerdimensioner. 

> [!NOTE] 
>  Du kan ændre lagringsdimensionsgruppen for varer, også selv om åbne lagertransaktioner findes.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Finde produkter, der blev blokeret på grund af palle-ID
For at få vist oversigten over frigivne produkter, der blev blokeret under opgraderingen og ikke kan behandles, skal du klikke på **Lagerstyring** &gt; **Konfiguration** &gt; **Lager** &gt; **Varer, der er spærret for lageropdateringer**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Ændre lagringsdimensionsgruppen for spærrede produkter 
 
En vare, der skal bruges som en del af en proces for lokationsstyring, skal være tilknyttet en lagringsdimensionsgruppe, hvor Lokationslagerdimension er aktiv, og **Brug lokationsstyringsprocesser**-parameteren vælges. Når denne indstilling er valgt, aktiveres lagerdimensionerne for lokation, lagersted, lagerstatus, sted og nummerplade.

For at fjerne blokeringen af produkter, der blev blokeret under opgraderingen, skal du vælge en ny lagringsdimensionsgruppe for produkterne. Bemærk, at du kan ændre lagringsdimensionsgruppen, også selv om åbne lagertransaktioner findes. Hvis du vil bruge varer, der blev blokeret under opgraderingen, har du to muligheder:

-   Skift lagringsdimensionsgruppen for varen til en lagringsdimensionsgruppe, der kun bruger Sted, Lagersted og Lokation som lagerdimensioner. Efter denne ændring bruges lagerdimensionen Palle-id ikke længere.
-   Skift lagringsdimensionsgruppen for varen til en lagringsdimensionsgruppe, der bruger processer for lokationsstyring. Efter denne ændring bruges lagerdimensionen Nummerplade.

## <a name="configure-warehouse-management-processes"></a>Konfigurere lokationsstyringsprocesser
Før du kan bruge frigivne produkter i **Lokationsstyring**-modulet, skal produkterne bruge en llagringsdimensionsgruppe, hvor **Brug lokationsstyringsprocesser**-parameteren er valgt.

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Aktivere lagersteders brug af lokationsstyringsprocesser.

1.  Opret mindst én ny lokationsprofil.
2.  Klik på **Lokationsstyring** &gt; **Konfiguration** &gt; **Aktivér lokationsstyringsprocesser** &gt; **Aktivér opsætning af lagersted**.
3.  På siden **Aktivér opsætning af lagersted** skal du tilføje de lagersteder, der skal aktiveres. Du kan udføre dette trin enten direkte på siden eller ved hjælp af Microsoft Office-integration.
4.  Tildel alle lokationer en lokationsprofil. Du kan nemt udføre dette trin ved hjælp af Microsoft Office-integration direkte fra siden. Du kan eksportere og importere dataene, eller du kan bruge behandling af dataenhed i [Datastyring](../../dev-itpro/data-entities/data-entities.md).
5.  Valider ændringerne. Som en del af valideringsprocessen forekommer forskellige valideringer af dataintegriteten. Som en del af en større opgraderingsproces skal problemer, der måtte opstå, tilpasses på kildeimplementeringen. I så fald skal der foretages en yderligere dataopgradering.
6.  Få behandlet ændringerne.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Ændre lagringsdimensionsgruppen for varer, så der anvendes lokationsstyringsprocesser

1.  Opret en ny **Lagerstatus**-værdi, og tildel den som **Standard-id for lagerstatus**-værdi i **Parametre til lokationsstyring**-indstillinger.
2.  Opret en ny lagringsdimensionsgruppe, hvor **Brug lokationsstyringsprocesser**-parameteren vælges.
3.  På siden **Reservationshierarki** skal du definere et nyt hierarki til reservation i henhold til varens lagrings- og sporingsdimensionsgrupper.
4.  Opret en eller flere enhedsseriegrupper, der omfatter mindst samme enheder, der bruges til varens lagerenheder.
5.  Klik på **Lokationsstyring** &gt; **Konfiguration** &gt; **Aktivér lokationsstyringsprocesser** &gt; **Ændre lagringsdimensionsgruppen for varer**.
6.  På siden **Ændre lagringsdimensionsgruppen for varer** skal du tilføje varenumre, lagringsdimensionsgrupper og enhedsseriegrupper. Du kan udføre dette trin direkte på siden, ved at bruge Microsoft Office-integration eller ved hjælp af dataenhedsprocessen i [Datastyring](../../dev-itpro/data-entities/data-entities.md).
7.  Valider ændringerne. Som en del af valideringsprocessen forekommer forskellige valideringer af dataintegriteten. Som en del af en større opgraderingsproces skal problemer, der måtte opstå, tilpasses på kildeimplementeringen. I så fald skal der foretages en yderligere dataopgradering.
8.  Få behandlet ændringerne. En opdatering af alle lagerdimensionerne kan tage et stykke tid. Du kan overvåge status ved hjælp af batchjobopgaverne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]