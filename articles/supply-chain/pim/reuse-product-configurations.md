---
title: Genbrug produktkonfigurationer
description: "Du kan angive, at du vil automatisk vil genbruge en eksisterende konfiguration for et produkt. Når en brugeren har fuldført en konfigurationssession, kontrollerer systemet, om der allerede findes en konfiguration, der svarer til brugerens valg. Hvis der findes en tilsvarende konfiguration, genbruges konfigurations-id, stykliste og rute."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4d61c869577a3e18d1ac951f32dae286937a51c
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="reuse-product-configurations"></a>Genbrug produktkonfigurationer

[!include[banner](../includes/banner.md)]


Du kan angive, at du vil automatisk vil genbruge en eksisterende konfiguration for et produkt. Når en brugeren har fuldført en konfigurationssession, kontrollerer systemet, om der allerede findes en konfiguration, der svarer til brugerens valg. Hvis der findes en tilsvarende konfiguration, genbruges konfigurations-id, stykliste og rute.

<a name="requirements-for-reusing-configurations"></a>Krav til genbrug af konfigurationer
---------------------------------------

Hvis du vil aktivere konfigurationer, der kan genbruges, skal du angive følgende oplysninger for komponenter og attributter på siden **Oplysninger om produktkonfigurationsmodel**:

-   **Komponenter og underkomponenter** – I oversigtspanelet **Generelt** skal du vælge **Ja** i feltet **Genbrug konfigurationer**.
-   **Attributter** – I **Attributter**-oversigtspanelet skal du vælge **Medtag i genbrug**-indstillingen. Denne indstilling vises kun, når den relaterede komponent er aktiveret til genbrug. Hvis du ikke vælger nogen attributter til genbrug, genbruges konfigurationen altid, uanset brugerens valg under en konfigurationssession. Attributværdierne i den eksisterende konfiguration skal svare til brugerens valg. Hvis brugeren f.eks. vælger farven **Blå** under en konfigurationssession, kontrollerer systemet, om en eksisterende konfiguration af den pågældende komponent har en attribut for blå farve.

## <a name="resetting-configuration-reuse"></a>Nulstilling af konfigurationsgenbrug
Når du nulstiller konfigurationsgenbrug, bruges tidligere oprettede konfigurationer ikke længere. Du kan nulstille konfigurationsgenbrug, hvis styklisten eller ruten er ændret, men ingen relaterede attributter blev ændret. Du nulstiller konfigurationsgenbrug i **Generelt**-oversigtspanelet for komponenten.




