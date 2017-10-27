---
title: Power BI-indhold til rekruttering
description: "I dette emne beskrives Power BI-indholdet til Rekruttering. Det beskrives, hvordan du får adgang til rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a02dab349da0709b8d9250dba0a2ca1e03b6a527
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="recruiting-power-bi-content"></a>Power BI-indhold til rekruttering

[!include[banner](../includes/banner.md)]

I dette emne beskrives Microsoft Power BI-indholdet til **Rekruttering**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold
Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), vises Power BI-indholdet til **Rekruttering** i arbejdsområdet **Administration af rekruttering**. 

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Rapporter og grafik i arbejdsområdet Administration af rekruttering
Arbejdsområdet **Administration af rekruttering** indeholder fanen **Analyser**. Denne fane indeholder integreret Power BI-indhold til rekruttering. Indholdet består af en fane med en oversigt og yderligere faner, der indeholder detaljer. Rapporterne er beskrevet under hver fane i følgende tabel.

| Rapport               | Indhold |
|----------------------|----------|
| Rekrutteringsoversigt | Opsummerer andre rapporter |
| Ansøgeranalyse   | Samlet antal ansøgere, ansøgere efter job, ansøgningskilder, kvindelige til mandlige ansøgere og ansøgere efter lokalitet |
| Ansøgerstatus     | Ansøgere efter type og status og ansøgerstatus |
| Rekrutteringsanalyse  | Nettoansættelsesforhold, gennemsnitlig antal dage til ansættelse, procentdel af dårlige ansættelser og rekrutteringsomkostninger, antal rekrutteringsprojekter, nyansat til anvendt og ansøgere vs. åbninger efter rekrutteringsprojekt |

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Følgende tabel viser de enheder, som Power BI-indholdet til **Rekruttering** var baseret på.

| Enhed               | Indhold                                                         | Relationer med andre enheder |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Ansøger            | Ansøgere, ansatte ansøgere, nettoansættelsesforhold og omkostninger          | Ansøgerens navn, firma, kalenderforskydning, dato, geografisk placering, demografi, job, medier, rekrutteringsprojekt |
| Ansøgers navn       | Ansøgers fornavn, efternavn og fulde navn                   | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Kalenderforskydning      | Kalenderforskydninger for at opdele rapporter                                | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Regnskab              | Virksomheder, som rapporter kan filtreres efter                                   | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Dato                 | Dage, uger, måneder og år                                   | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Demografi         | Fødselsdato, køn, etnisk oprindelse og civilstand         | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Ansøger blev ansat   | Ansøger, performance, startdato og ansøgertype           | Firma, kalenderforskydning, dato, geografisk placering, ansøgers navn, ansættelse, performance, job, medier, rekrutteringsprojekt |
| Ansættelse           | Startdato, slutdato og overførselsdato                        | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Geografisk placering  | By, landsdel, postkode og stat eller provins                 | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Stilling                  | Funktion, type og titel                                        | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Medier                | Kilde for ansøgere                                             | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Ydeevne          | Klassifikation, beskrivelse og klassifikationsmodel                            | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Rekrutteringsprojekt  | Projektbeskrivelse, projektstatus og åbninger                | Ansøger, ansøgeren blev ansat, afsluttet ansøger |
| Afsluttet ansøger | Afsluttede ansøgere, årsag, performance og fratrædelsesdato | Firma, kalenderforskydning, dato, geografisk placering, performance, demografi, ansættelse, medier, rekrutteringsprojekt, ansøgers navn |

Disse enheder blev brugt til at oprette beregnede målinger. Disse beregnede mål bruges derefter til at beregne nøgletal (KPI'er) og rapporter, der bruges i indholdet. Hvis du vil medtage yderligere beregninger på rapporter og dashboard, kan du hente og redigere filen Recruiting.pbix fra Microsoft Dynamics Lifecycle Services (LCS). Denne fil er den standarddatamodel, der blev brugt til at oprette indholdet. Når du har foretaget ændringerne, kan du oprette en indholdspakke og et dashboard for organisationen, som indeholder de oplysninger, du har tilføjet.
