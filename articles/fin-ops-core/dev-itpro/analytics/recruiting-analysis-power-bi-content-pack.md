---
title: Power BI indhold til Rekruttering
description: I dette emne beskrives Power BI-indhold til Rekruttering.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cc05e60b24ab82feb5ffccc4cdb662108b6b1534
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562922"
---
# <a name="recruiting-power-bi-content"></a>Power BI indhold til Rekruttering

[!include [banner](../includes/banner.md)]

I dette emne beskrives **Rekruttering** Microsoft Power BI-indhold. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet
Power BI-indholdet **Rekruttering** vises i arbejdsområdet **Administration af rekruttering**.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Rapporter og grafik i arbejdsområdet Administration af rekruttering
Arbejdsområdet **Administration af rekruttering** indeholder fanen **Analyser**. Denne fane indeholder integreret Power BI-indhold til rekruttering. Indholdet består af en fane med en oversigt og yderligere faner, der indeholder detaljer. Rapporterne er beskrevet under hver fane i følgende tabel.

| Rapport               | Indhold |
|----------------------|----------|
| Rekrutteringsoversigt | Opsummerer andre rapporter |
| Ansøgeranalyse   | Samlet antal ansøgere, ansøgere efter job, ansøgningskilder, kvindelige til mandlige ansøgere og ansøgere efter lokalitet |
| Ansøgerstatus     | Ansøgere efter type og status og ansøgerstatus |
| Rekrutteringsanalyse  | Nettoansættelsesforhold, gennemsnitlig antal dage til ansættelse, procentdel af dårlige ansættelser og rekrutteringsomkostninger, antal rekrutteringsprojekter, nyansat til anvendt og ansøgere vs. åbninger efter rekrutteringsprojekt |

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Følgende tabel viser de enheder, som Power BI-indholdspakken **Rekruttering** er baseret på.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]