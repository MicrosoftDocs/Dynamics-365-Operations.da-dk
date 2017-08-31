---
title: Overflytte fra AX 2012 til Finance and Operations
description: "Denne artikel indeholder en oversigt over overførselsindstillinger for produkt- og lokationsstyring i Dynamics 365 for Finance and Operations."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cacf48bc10be5c06154816c2f9951ab4bbaee1c1
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="migrate-from-ax-2012-to-finance-and-operations"></a>Overflytte fra AX 2012 til Finance and Operations

Dette emne indeholder en oversigt over overførselsindstillinger for produkt- og lokationsstyring i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

<a name="introduction"></a>Introduktion
------------

Under en opgradering til Finance and Operations blokeres produkter, hvis de er knyttet til en lagringsdimensionsgruppe, der har indstillinger, som ikke opfylder kravene til lagringsdimensionsgruppen i Finance and Operations. Efter opgraderingen kan du dog bruge et sæt af overførselsindstillinger i processen **Ændre lagringsdimensionsgruppen for varer** for at fjerne blokeringen af produkter, der blev blokeret under opgraderingen. Du kan derefter behandle transaktioner for disse produkter. Nogle af varerne kan allerede være tilknyttet lagringsdimensionsgrupper, hvor lokations-, lagersteds- og lokationslagerdimensioner er aktive og fysisk registrerede. I så fald kan du bruge processen **Ændre lagringsdimensionsgruppen for varer** til at aktivere varerne, der skal bruges i lokationsstyringsprocesser. Denne funktion er nyttig, hvis du vil bruge lokationsstyringsfunktionen for eksisterende varer.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Opgradering til Finance and Operations, når AX 2012 R3 WMSII bruges.
Finance and Operations understøtter ikke længere det ældre **WMSII**-modul fra Microsoft Dynamics AX 2012. Du kan i stedet bruge det nye **Lokationsstyring**-modul. I tidligere versioner kunne lagerdimensionerne Lokation og Palle-id vælges for økonomisk lager. Men som en del af opgraderingsprocessen kan lagerdimensionen Palle-id ikke længere aktiveres for økonomisk lager. Alle produkter, der er knyttet til en lagringsdimensionsgruppe, der bruger lagerdimensionen Palle-id, vil blive blokeret og ikke blive behandlet.

### <a name="enabling-items-in-finance-and-operations"></a>Aktivering af varer i Finance and Operations

Varer, der skal bruges som en del af processer for lokationsstyring, skal være tilknyttet en lagringsdimensionsgruppe i Finance and Operations, hvor **Brug lokationsstyringsprocesser**-parameteren vælges. Når denne indstilling er valgt, aktiveres lagerdimensionerne for lokation, lagersted, lagerstatus, sted og nummerplade. Du kan skifte til denne type lagringsdimensionsgruppe alene for varer, der allerede er tilknyttet lagringsdimensionsgrupper, hvor lagerdimensionen Lokation er aktiv.

### <a name="items-that-are-blocked-for-inventory-updates"></a>Varer, der er spærret for lageropdateringer

For at få vist oversigten over frigivne produkter, der blev blokeret under opgraderingen og ikke kan behandles, skal du klikke på **Lagerstyring** &gt; **Konfiguration** &gt; **Lager** &gt; **Varer, der er spærret for lageropdateringer**.

### <a name="reapplying-blocked-products"></a>Genanvendelse af spærrede produkter

For at fjerne blokeringen af produkter, der blev blokeret under opgraderingen, skal du vælge en ny lagringsdimensionsgruppe for produkterne. Bemærk, at du kan ændre lagringsdimensionsgruppen, også selv om åbne lagertransaktioner findes. Hvis du vil bruge varer, der blev blokeret under opgraderingen, har du to muligheder:

-   Skift lagringsdimensionsgruppen for varen til en lagringsdimensionsgruppe, der kun bruger Sted, Lagersted og Lokation som lagerdimensioner. Efter denne ændring bruges lagerdimensionen Palle-id ikke længere.
-   Skift lagringsdimensionsgruppen for varen til en lagringsdimensionsgruppe, der bruger processer for lokationsstyring. Efter denne ændring bruges lagerdimensionen Nummerplade.

### <a name="migration-processes"></a>Overførselsproces

I Finance and Operations er varesporing en del af processerne for lokationsstyring. For disse processer skal alle lagersteder og deres lokationer være tilknyttet en lokationsprofil. Hvis du vil bruge processer for lokationsstyring, skal der håndteres to processer:

-   Eksisterende lagersteder skal være aktiverede til at bruge lokationsstyringsprocesser.
-   Eksisterende frigivne produkter skal være tilknyttet en ny lagringsdimensionsgruppe, der bruger lokationsstyringsprocesser.

Hvis kildelagringsdimensionsgrupper bruger lagerdimensionen Palle-id, skal lokationen af eksisterende disponibel lagerbeholdning, der bruger Palle-id som lagerdimension, være tilknyttet en lokationsprofil, hvor **Brug nummerpladesporing**-parameteren markeres. Hvis de eksisterende lagersteder ikke skal bruges til lokationsstyringsprocesser, kan du ændre lagringsdimensionsgrupper for den eksisterende disponible lagerbeholdning til grupper, der kun håndterer Lokation-, Lagersted- og Sted-lagerdimensioner.

### <a name="using-the-warehouse-management-processes"></a>Brug af lokationsstyringsprocesser

Før du kan bruge frigivne produkter i **Lokationsstyring**-modulet, skal produkterne bruge en llagringsdimensionsgruppe, hvor **Brug lokationsstyringsprocesser**-parameteren er valgt.

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Aktivere lagersteders brug af lokationsstyringsprocesser.

1.  Opret mindst én ny lokationsprofil.
2.  Klik på **Lokationsstyring** &gt; **Konfiguration** &gt; **Aktivér lokationsstyringsprocesser** &gt; **Aktivér opsætning af lagersted**.
3.  På siden **Aktivér opsætning af lagersted** skal du tilføje de lagersteder, der skal aktiveres. Du kan udføre dette trin enten direkte på siden eller ved hjælp af Microsoft Office-integration.
4.  Tildel alle lokationer en lokationsprofil. Du kan nemt udføre dette trin ved hjælp af Microsoft Office-integration direkte fra siden. Du kan eksportere og importere dataene, eller du kan bruge behandling af dataenhed i [Datastyring](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities).
5.  Valider ændringerne. Som en del af valideringsprocessen forekommer forskellige valideringer af dataintegriteten. Som en del af en større opgraderingsproces skal problemer, der måtte opstå, tilpasses på kildeimplementeringen. I så fald skal der foretages en yderligere dataopgradering.
6.  Få behandlet ændringerne.

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Ændre lagringsdimensionsgruppen for varer, så der anvendes lokationsstyringsprocesser

1.  Opret en ny **Lagerstatus**-værdi, og tildel den som **Standard-id for lagerstatus**-værdi i **Parametre til lokationsstyring**-indstillinger.
2.  Opret en ny lagringsdimensionsgruppe, hvor **Brug lokationsstyringsprocesser**-parameteren vælges.
3.  På siden **Reservationshierarki** skal du definere et nyt hierarki til reservation i henhold til varens lagrings- og sporingsdimensionsgrupper.
4.  Opret en eller flere enhedsseriegrupper, der omfatter mindst samme enheder, der bruges til varens lagerenheder.
5.  Klik på **Lokationsstyring** &gt; **Konfiguration** &gt; **Aktivér lokationsstyringsprocesser** &gt; **Ændre lagringsdimensionsgruppen for varer**.
6.  På siden **Ændre lagringsdimensionsgruppen for varer** skal du tilføje varenumre, lagringsdimensionsgrupper og enhedsseriegrupper. Du kan udføre dette trin direkte på siden, ved at bruge Microsoft Office-integration eller ved hjælp af dataenhedsprocessen i [Datastyring](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities).
7.  Valider ændringerne. Som en del af valideringsprocessen forekommer forskellige valideringer af dataintegriteten. Som en del af en større opgraderingsproces skal problemer, der måtte opstå, tilpasses på kildeimplementeringen. I så fald skal der foretages en yderligere dataopgradering.
8.  Få behandlet ændringerne. En opdatering af alle lagerdimensionerne kan tage et stykke tid. Du kan overvåge status ved hjælp af batchjobopgaverne.



