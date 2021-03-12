---
title: Godkend ordreforslag
description: I dette emne beskrives godkendelse af ordreforslag, der understøttes i planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: c29ede7ad8916a97b4a04b68f41961f79810e0c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983563"
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
