---
title: Foretage fejlfinding af konfiguration af lagersted
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du konfigurerer Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9bbe92627f53b3b4b04597be144d602b3cae7ed7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646101"
---
# <a name="troubleshoot-warehouse-configuration"></a>Foretage fejlfinding af konfiguration af lagersted

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du konfigurerer Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Jeg får vist følgende fejlmeddelelse: "Id'et eller lokationen er ikke gyldig".

### <a name="issue-description"></a>Problembeskrivelse

Du får vist denne fejlmeddelelse, når du scanner et nummerplade-id eller en lokation.

### <a name="issue-resolution"></a>Problemløsning

Kontrollér, at nummerplade-id'et ikke er reserveret af noget andet. Dette problem opstod, når den værdi, som en bruger scannede i lagerstedsappen, både var en gyldig lokation og et gyldigt nummerplade-id. Dette problem blev dog løst i version 10.0.11.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Jeg får vist følgende fejlmeddelelse: "Id skal være angivet for denne lokation".

### <a name="issue-description"></a>Problembeskrivelse

Du får vist denne fejlmeddelelse, hvis du opretter en flytteordre ved hjælp af et lagersted, der er aktiveret til avanceret lokationsstyring (WMS), og du derefter forsøger at bekræfte forsendelsen, efter at arbejdet er fuldført.

### <a name="issue-resolution"></a>Problemløsning

Feltet **Standardtilgangslokation** er tomt for et transitlagersted i "fra"-lagerstedet. Du kan løse dette problem ved at angive en standardtilgangslokation på transitlagerstedet. Kontrollér, at denne lokation er id-styret.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Jeg får vist følgende fejlmeddelelse: "Du kan ikke oprette en arbejdsskabelonlinje til ændring af lagerstatus, fordi arbejdstypen ikke er gyldig. Vælg en anden arbejdstype".

### <a name="issue-description"></a>Problembeskrivelse

I forbindelse med en arbejdsskabelon kan du ikke vælge *Ændring af lagerstatus* i kolonnen **Arbejdstype** i sektionen **Detaljer for arbejdsskabelon**.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde er tilsigtet. Arbejdstypen *Ændring af lagerstatus* bruges kun i forbindelse med systemprocesser. Den kan ikke konfigureres. Da listen over arbejdstyper er fastlagt som en fasttekst, kan de ekstra poster ikke filtreres fra rullemenuen **Arbejdstype**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Jeg får vist følgende fejlmeddelelse: "Antallet er ikke gyldigt for enheden 1%".

### <a name="issue-description"></a>Problembeskrivelse

Antallet er ikke gyldigt for *hver*-enheden, når der er plukarbejde, der har flere id'er på én lokation.

### <a name="issue-resolution"></a>Problemløsning

Kontrollér, at felterne **Enhedsseriegruppe-id** og **Enhedsomregninger** på det frigivne produkt eller den frigivne produktvariant er angivet korrekt.

Bemærk, at fejlmeddelelsen er blevet forbedret i version 10.0.15 (se [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Den nye fejlmeddelelse er "Antallet er ikke gyldigt. Forventede %1 %2".

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>I lokationsvejledninger for salgsordres læg på lager-arbejde, evaluerer indstillingen for flere SKU'er ikke flere handlinger for lokationsvejledninger.

### <a name="issue-description"></a>Problembeskrivelse

Lokationsvejledninger for arbejdsordretypen *Salgsordrer* og arbejdstypen *Læg på lager* evaluerer ikke flere handlinger for lokationsvejledninger, når indstillingen **Flere SKU'er** er valgt. Det er kun den første handling i lokationsvejledningen, der evalueres.

### <a name="issue-resolution"></a>Problemløsning

En ny funktion, *Evaluer alle handlinger for lokationsvejledninger med flere SKU'er*, er blevet tilføjet i version 10.0.15 (se [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Denne funktion evaluerer alle handlinger for lokationsvejledninger med flere SKU'er. Hvis du har brug for denne funktion, skal du bruge [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere den.

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a>Jeg kan ikke bruge lagerstedsappen til at foretage en delvis plukning.

### <a name="issue-description"></a>Problembeskrivelse

I forbindelse med salgs- og flytteordrer kan du ikke springe varer over og foretage delvis plukning.

### <a name="issue-resolution"></a>Problemløsning

På siden **Menupunkter i mobilenhed** skal du for hvert menupunkt, der er konfigureret til at behandle salgsordrer eller flytteordrer, angive **Ja** for indstillingen **Tillad opdeling af arbejde** i oversigtspanelet *Generelt*.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Hvordan kan jeg foretage en ændring af lagerstatus for delmængdearbejde?

### <a name="issue-description"></a>Problembeskrivelse

Du vil foretage en ændring af lagerstatus for et delvist antal af en batch.

### <a name="issue-resolution"></a>Problemløsning

Hvis du vil give arbejdere mulighed for at foretage denne ændring, kan du oprette et menupunkt til lagerstedsappen. Opret (eller rediger) et menupunkt med følgende indstillinger på siden **Menupunkter i mobilenhed**:

- **Tilstand:** *Arbejde*
- **Brug eksisterende arbejde:** *Nej*
- **Arbejdsoprettelsesproces:** *Bevægelse*
- **Vis lagerstatus:** *Ja*

Angiv de resterende felter på siden efter behov.
