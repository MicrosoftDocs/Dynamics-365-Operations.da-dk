---
title: Definere og vedligeholde detailkanaler
description: "Denne artikel indeholder en oversigt over processen til opsætning af mursten og mørtel butikker, som kaldes detailbutikker i Microsoft Dynamics 365 for operationer. Den indeholder oplysninger om de opgaver, du skal udføre, både før og efter du har oprettet en detailbutik."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b775ba34ef7d88dd0b47904e4a3e9be79664f14b
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-retail-channels"></a>Definere og vedligeholde detailkanaler

Denne artikel indeholder en oversigt over processen til opsætning af mursten og mørtel butikker, som kaldes detailbutikker i Microsoft Dynamics 365 for operationer. Den indeholder oplysninger om de opgaver, du skal udføre, både før og efter du har oprettet en detailbutik.

Understøtter flere detailkanaler, som onlinebutikker, call-centre og mursten og mørtel butikker, detail- og handel i Dynamics 365 for operationer. Inden for detail og handels kaldes en fysisk butik en detailbutik. Hver detailbutik kan have sine egne betalingsmetoder, prisgrupper, POS-kasseapparater, indtægtskonti og udgiftskonti samt medarbejdere. Du skal oprette alle disse elementer for en detailbutik, før du opretter den. Når du har oprettet detailbutikken, kan du tildele de produkter, som skal føres i denne butik. Du skal også knytte medarbejdere, kasseapparater og kunder til butikken. Endelig kan føje den nye butik til et organisationshierarki.

## <a name="setting-up-retail-stores"></a>Konfigurere detailbutikker
Før du kan oprette en detailbutik i Dynamics 365 for operationer, skal du udføre nogle nødvendige opgaver. Du kan derefter oprette detailbutikken og tilføje oplysninger.

### <a name="prerequisites"></a>Forudsætninger

Du skal fuldføre følgende opgaver, før du kan konfigurere en detailbutik:

1.  Konfigurer organisationsstrukturen, og opret organisationshierarkier for detailudvalg, genopfyldning og rapportering.
2.  Opret et lager, der repræsenterer detailbutikken.
3.  Definer nummerserier til detailbutikker, butiksopgørelser og opgørelsesbilag.
4.  Konfigurer parametre til detail.
5.  Konfigurer betalingsmetoderne, som butikken accepterer.
6.  Hvis du vil behandle kreditkorttransaktioner på butikkens POS-kasseapparater, kan du også konfigurere betalingstjenester.
7.  Konfigurer momsgrupper.
8.  Konfigurer detailprodukter. Som en del af denne opgave skal du oprette detailprodukthierarkier, produktvarianter og produktudvalg.
9.  Konfigurer produktprisgrupper.
10. Konfigurer detailproduktpriser. Som en del af denne opgave skal du også konfigurere prisjusteringer, rabatter og rabatperioder.
11. Opsætning af medarbejdere. **Bemærk:** du skal også tildele relevante tilladelser for arbejdstagerne, så de kan logge på og udføre opgaver ved hjælp af Dynamics 365 for operationer for Retail POS-system.
12. Konfigurer de Retail POS-profiler, som du vil tildele til butikken. Denne opgave omfatter mange andre opgaver, f.eks. opsætning af registre, konfiguration af offlineprofiler samt opsætning af kvitteringsformater og -profiler.

Gennemse alle de opgaver, der er inkluderet i forudsætningen, og udfør kun de opgaver, der gælder for dig.

### <a name="set-up-a-retail-store"></a>Konfigurere en detailbutik

Når du har fuldført de nødvendige opgaver, skal du udføre disse opgaver for at konfigurere oplysninger til detailbutikken:

1.  Opret en detailbutik.
2.  Knyt en momsgruppe til butikken.
3.  Tildel de accepterede betalingsmetoder til butikken.
4.  Føj oplysninger til produktbeskrivelserne for de produkter, du tilbyder i dine detailbutikker. Du kan for eksempel tilføje RTF-tekst og billeder. Disse produktoplysninger vises i forskellige sammenhænge som på POS-kasseapparat eller på udskrevne etiketter.
5.  Føj butikken til det standardorganisationshierarki, der er tildelt med formålet **Detailudvalg**, **Detailgenopfyldning** eller **Detailrapportering**.

### <a name="after-you-set-up-a-retail-store"></a>Når du har oprettet en detailbutik

Når du har angivet oplysningerne om detailbutikken, skal du udføre disse opgaver for at sende de nye detailbutiksdata til Retail POS:

1.  Konfigurer POS-kasseapparaterne til butikken.
2.  Tildel produktudvalg til butikken.
3.  Du kan behandle udvalg for at oprette listen over produkter, der indgår i udvalget, og for at gøre produkterne tilgængelige i butikken.
4.  Send data som f.eks. nummerserier, hardwareprofiler og layout for POS-skærmen til Retail POS-kasseapparaterne.
5.  Udgiv detailbutikken for at sende lagringsdata til Retail POS.
6.  Kør jobbene for at sende lagringsdataene til Retail POS.

## <a name="organization-hierarchies"></a>Organisationshierarkier
Retail bruger organisationshierarkier i Microsoft Dynamics AX til at strukturere detailkanaler. Organisationshierarkier repræsenterer relationerne mellem de organisationer, som dit firma består af. Når du opretter butikker, kan du føje dem til et organisationshierarki. Butikkerne deler derefter data, der bruges til udvalg, genbestilling og rapportering.

