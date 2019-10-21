---
title: Power BI-indhold til Læring
description: I dette emne beskrives Power BI-indhold til Læring.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f4752c4b61c396db82e5804292607f142bfbe691
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184318"
---
# <a name="learning-power-bi-content"></a>Power BI-indhold til Læring

[!include [banner](../includes/banner.md)]

Dette emne beskriver Microsoft Power BI-indhold til **Læring**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet

De rapporter, der er inkluderet i Power BI-indholdet til **Læring**, har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                | Indhold |
|-----------------------|----------|
| Oversigt over læring     | Oversigt over andre rapporter |
| Analyse af kursus       | Registrering af lokalitet, deltager efter status, kurser efter type pr. firma og kursusdeltager efter job |
| Tilmeldingsanalyse | Tilmeldingsliste |
| Kursustyper          | Kursustyper efter færdighed |
| Instruktøranalyse   | Forholdet mellem kurser og instruktører, antal instruktører, kurser efter instruktør, kurser pr. instruktør og kursusagenda efter instruktør |
| Udbudte kurser       | Kursusliste |
| Kursusdesign        | Kursusagenda |

Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder

Følgende data bruges til at udfylde rapporterne i Power BI-indhold til **Læring**. Denne tabel viser de enheder, som indholdet er baseret på.

| Enhed           | Indhold                                                         | Relationer med andre enheder |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Kalenderforskydning  | Kalenderforskydninger for at opdele rapporter                                | Kursusagenda, kursusdeltagere |
| Regnskab          | Virksomheder, som rapporter kan filtreres efter                                   | Kursusagenda, kursusdeltagere |
| Kursus           | Kursus, beskrivelse, instruktørnavn, lokalitet, værelse og status | Kursusagenda, kursusdeltagere, kursusfærdighed |
| Kursusagenda    | Agenda, kursus og start- og sluttidspunkter                          | Firma, kalenderforskydning, dato, kursus |
| Kursusdeltagere | Navn, status, job og registreringsdato                         | Firma, kalenderforskydning, dato, kursus, demografi, ansættelse, kursus, medarbejdernavn, medarbejdertitel, job, stilling |
| Kursusfærdighed     | Færdighed, færdighedstype og niveau                                     | Kursus |
| Dato             | Dage, uger, måneder og år                                   | Kursusagenda, kursusdeltagere |
| Demografi     | Fødselsdato, køn, etnisk oprindelse og civilstand         | Kursusagenda, kursusdeltagere |
| Ansættelse       | Startdato, slutdato og overførselsdato                        | Kursusagenda, kursusdeltagere |
| Stilling              | Funktion, type og titel                                        | Kursusagenda, kursusdeltagere |
| Stilling         | Stilling, titel og tilsvarende fuld tid (fuldtidsansat)                  | Kursusagenda, kursusdeltagere |
| Medarbejdernavn    | Fornavn, efternavn og fulde navn                             | Kursusdeltagere |
| Medarbejdertitel   | Titel og anciennitetsdato                                         | Kursusdeltagere |
