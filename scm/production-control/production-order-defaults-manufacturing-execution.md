---
title: "Produktionsordrestandarder i produktionsudførelse"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: cc12a8d75ead1577cf0b31a0dbf3ac072c47dc08
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>Produktionsordrestandarder i produktionsudførelse

[!include[banner](../includes/banner.md)]




Overvej nøje alle indstillinger på siden **Produktionsordrestandarder**, før arbejdere går i gang med at foretage registreringer på produktionsjob. Hvis dit firma bruger funktionalitet med flere steder, skal du måske konfigurere forskellige standarder for produktionsordrer for hvert sted. Ordrestandarden for integration med Produktionsstyring er angivet under følgende faner på siden **Produktionsordrestandarder**:

-   **Generelt** – Generelle ordrestandarder for produktionsjob i produktionsudførelse.
-   **Start** – Ordrestandarder, der bruges, når produktionsjob eller operationer er startet.
-   **Operationer** – Ordrestandarder, der anvendes på produktionsjob og -operationer og tilbagemeldinger på operationer i produktionsprocessen.
-   **Færdigmeld** – Ordrestandarder, der bruges, når varer færdigmeldes i den sidste operation i en produktionsordre.
-   **Validering af antal** – Ordrestandarder til validering af start- og tilbagemeldingsantal på produktionsordrer.

## <a name="types-of-production-jobs"></a>Typer af produktionsjob
På fanen **Operationer** skal du vælge typerne af produktionsjob, der kræver registrering på siden **Jobregistrering**. Arbejderne foretager typisk registreringer på opstillingsjob og procesjob. Men hvis der anvendes finplanlægning, kan du vælge andre jobtyper, som f.eks. transportjob, hvor arbejderne også skal foretage registreringer for, hvornår en produktionsordre behandles. **Vigtigt:** Sørg for, at alle relevante jobtyper er valgt. Ellers er job muligvis ikke tilgængelige til registrering på siden **Jobregistrering**. Juster dine valg med de valg, der foretages i kolonnen **Jobstyring** på siden **Rutegrupper**. Hvis **Jobstyring** er valgt i rutegruppen, færdigmeldes denne jobtype på produktionsordren. Denne rapportering forekommer, når jobbet færdigmeldes i Produktionsudførelse. Når alle jobtyper, som **Jobstyring** er valgt til, er færdigmeldt på en operation, færdigmelder Produktionsudførelse også operationen. **Bemærk:** Visse jobtyper kan færdigmeldes manuelt via produktionskladder. I dette tilfælde skal du vælge **Jobstyring** for jobtypen, men ikke vælge jobtypen for registrering på fanen **Operationer** på siden **Produktionsordrestandarder**.

## <a name="bom-consumption-and-picking-list-journals"></a>Styklisteforbrug og pluklistekladder
Materialer kan konfigureres, så de forbruges automatisk eller manuelt under produktionen. Automatisk forbrug styres ved varetrækprincippet, der er angivet på styklistelinjerne og ved at konfigurere feltet **Auto-styklisteforbrug** under produktionsordrestandarderne. Automatisk forbrug kan konfigureres, så det forekommer, når en produktionsordre startes eller færdigmeldes. Alternativt kan det forekommer på jobniveau, når et job startes eller afsluttes.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Kontrol af materialeforbrug, når en produktionsordre startes

Materialeforbrug under start af en produktionsordre styres af feltet **Auto-styklisteforbrug** på fanen **Start**. Følgende værdier er tilgængelige:

-   **Varetrækprincip** – Når en produktionsordre startes, forbruges mængder af materialer i overensstemmelse med varetrækprincippet, der konfigureres på produktionsstyklistelinjerne. Kun styklistelinjerne, hvor varetrækprincippet er indstillet til **Start** forbruges under produktionsstart.
-   **Altid** – Mængder af materialer, der er proportionel med den igangsatte mængde vil altid blive brugt.
-   **Aldrig** – Mængder af materialer vil aldrig blive brugt.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Kontrol af materialeforbrug, når en produktionsordre startes eller fuldføres

Materialeforbrug under start eller fuldførelse af en produktionsordre styres af feltet **Auto-styklisteforbrug** på fanen **Start**. Følgende værdier er tilgængelige:

-   **Varetrækprincip** – Når en mængde på et produktionsjob startes eller fuldføres, forbruges mængder af materialer i overensstemmelse med varetrækprincippet, der konfigureres på produktionsstyklistelinjerne. Kun styklistelinjerne, hvor varetrækprincippet er indstillet til **Start** eller **Slut**, forbruges.
-   **Altid** – Mængder af materialer, der er proportionel med den igangsatte mængde på jobbet vil altid blive brugt.
-   **Aldrig** – Mængder af materialer vil aldrig blive brugt.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Kontrollere materialeforbrug, når en produktionsordre færdigmeldes

Materialeforbrug under færdigmeldingsprocessen for en produktionsordre styres af feltet **Auto-styklisteforbrug** på fanen **Færdigmeld**. Følgende værdier er tilgængelige:

-   **Varetrækprincip** – Når en produktionsordre færdigmeldes, forbruges mængder af materialer i overensstemmelse med varetrækprincippet, der konfigureres på produktionsstyklistelinjerne. Kun styklistelinjerne, hvor varetrækprincippet er indstillet til **Slut**, forbruges.
-   **Altid** – Mængder af materialer, der er proportionel med den mængde, der færdigmeldes, vil altid blive brugt.
-   **Aldrig** – Mængder af materialer vil aldrig blive brugt.





