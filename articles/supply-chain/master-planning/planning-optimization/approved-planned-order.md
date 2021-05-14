---
title: Vise, administrere og godkende ordreforslag
description: Dette emne beskriver, hvordan du kan få vist, administrere og godkende ordreforslag i Planlægningsoptimering.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3b9b5274481e693f9fa05eb084ec5505ce5bc2eb
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935651"
---
# <a name="view-manage-and-approve-planned-orders"></a>Vise, administrere og godkende ordreforslag

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du kan få vist, administrere og godkende ordreforslag i Planlægningsoptimering.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Vise og administrere ordreforslag

Du kan få vist og administrere ordreforslag på enhver listeside med ordreforslag. Gå til et af følgende steder, afhængigt af hvilken type ordreforslag du vil arbejde med:

- Varedisponering \> Arbejdsområder \> Varedisponering
- Varedisponering \> Varedisponering \> Ordreforslag
- Produktionsstyring \> Produktionsordrer \> Produktionsordreforslag
- Indkøb og forsyning \> Indkøbsordrer \> Indkøbsordreforslag
- Lagerstyring \> Indgående ordrer \> Overførselsforslag
- Lagerstyring \> Udgående ordrer \> Overførselsforslag

## <a name="view-and-edit-the-status-of-planned-orders"></a>Få vist og redigere status for ordreforslag

Du kan bruge feltet **Status** i hvert ordreforslag til at spore forløbet eller ændre behandlingen af et ordreforslag. Følgende værdier for **Status** er tilgængelige:

- **Ubehandlet** – Når varedisponeringen opretter ordreforslag, tildeles de denne status. Ordreforslag med denne status vil blive slettet under næste planlægningskørsel.
- **Fuldført** – Denne status angiver, at ordreforslaget er fuldført. Hvis du vælger ikke at autorisere et ordreforslag, kan du ændre dets status manuelt til *Fuldført*. Bemærk, at systemet behandler statussen som *Ubehandlet* og *Fuldført* på samme måde.
- **Godkendt** – Denne status angiver, at ordreforslaget er godkendt til autorisation. Hvis du vil autorisere et ordreforslag, kan du ændre dets status til *Godkendt*. Hvis du vil bevare ændringerne af et ordreforslag, eller hvis du planlægger at autoriseret et ordreforslag, skal du ændre dets status til *Godkendt*. Ordreforslag med statussen *Godkendt* betragtes som fast og forventet forsyning gennem varedisponering. Derfor ændres eller slettes de ikke under senere kørsler af varedisponeringen. For at opnå dette kopierer planlægningslogikken ordreforslag med statussen *Godkendt* fra den gamle planversion til den nye planversion under varedisponeringen. Bemærk, at ordreforslag med statussen *Godkendt* kun betragtes som forsyning inden for den specifikke behovsplan.

Hvis du vil ændre statussen for et enkelt ordreforslag, skal du [åbne en listeside med ordreforslag](#view-planned-orders), åbne ordren og derefter benytte en af følgende fremgangsmåder:

- Rediger værdien i feltet **Status** i oversigtspanelet **Generelt**.
- Vælg **Skift status** i gruppen **Proces** under fanen **Ordreforslag** i handlingsruden.
- Hvis du vil markere ordren som godkendt, skal du vælge **Godkend** i handlingsruden.

Hvis du vil ændre statussen for flere ordreforslag på én gang, skal du [åbne en listeside med ordreforslag](#view-planned-orders), markere afkrydsningsfeltet for hver ordre, som du vil ændre, og derefter benytte en af følgende fremgangsmåder:

- Vælg **Skift status** i gruppen **Proces** under fanen **Ordreforslag** i handlingsruden.
- Hvis du vil markere ordrerne som godkendt, skal du vælge **Godkend** i handlingsruden.

## <a name="approve-planned-orders"></a>Godkende ordreforslag

Godkendelse af ordreforslag er et valgfrit trin i processen for oprettelse af en autoriseret ordre fra et ordreforslag.

Følgende illustration viser, hvordan du kan bruge den værdi for **Status**, som er tildelt det enkelte ordreforslag, til at implementere en arbejdsproces for godkendelse. Hvis du vil implementere en godkendelsesproces, skal dujustere værdien for **Status** manuelt for det enkelte ordreforslag som beskrevet i forrige afsnit.

![Ordreforslagsflow](media/approved-planned-orders-1.png)

> [!TIP]
> Det anbefales, at du godkender eventuelle ændrede ordreforslag. Ellers ignoreres og overskrives ændringerne i næste planlægningskørsel.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Autoriser ordreforslag](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
