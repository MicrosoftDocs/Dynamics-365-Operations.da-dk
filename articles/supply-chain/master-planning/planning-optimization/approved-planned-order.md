---
title: Godkend ordreforslag
description: I dette emne beskrives godkendelse af ordreforslag, der understøttes i planlægningsoptimering.
author: ChristianRytt
ms.date: 08/21/2020
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
ms.openlocfilehash: 6c215a89403f16336caae5c62cde6df469c4091c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825885"
---
# <a name="approve-planned-orders"></a>Godkend ordreforslag

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan status for ordreforslag opdateres i planlægningsoptimering.

Bemærk, at godkendelse af ordreforslag er et valgfrit trin, når du skal oprette en autoriseret ordre fra et ordreforslag. Det anbefales at godkende ændrede ordreforslag, for ellers ignoreres ændringerne, som overskrives af næste planlægningskørsel.

![Ordreforslagsflow](media/approved-planned-orders-1.png)

Feltet **Status** hjælper dig med at spore status ved hjælp af følgende værdier:

- **Ubehandlet:** Når varedisponering opretter ordreforslag, har ordreforslagene statussen *Ubehandlet*. Ordreforslag med denne status vil blive slettet under næste planlægningskørsel.
- **Fuldført:** Hvis du ikke vil autorisere et ordreforslag, kan du ændre status til *Fuldført* for at angive, at du har afsluttet evalueringen af ordreforslaget. Bemærk, at status som *Ubehandlet* og *Fuldført* håndteres på samme måde af systemet.
- **Godkendt:** Hvis du vil beholde redigeringer eller planlægger at autorisere et ordreforslag, skal du ændre status til *Godkendt*. Ordreforslag med statussen *Godkendt* regnes for fastlagte og forventede forsyninger i varedisponeringen, så de ikke ændres eller slettes, når varedisponeringen køres. For at opnå dette kopierer planlægningslogikken de *Godkendte* planlagte ordre fra den gamle planversion til den nye planversion under varedisponering. Bemærk, at *Godkendte* ordreforslag kun betragtes som forsyning inden for den specifikke behovsplan.

Du kan administrere ordreforslag fra arbejdsområdet **Varedisponering**, listen **Ordreforslag** eller listerne **Produktionsordreforslag**, **Planlagte indkøbsordrer** og **Planlagt overførsel**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]