---
title: Dato for kreditormomsregistrering
description: Denne artikel indeholder oplysninger om en funktion til aktivering af dato for kreditormomsregistrering
author: anasyash
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: global
ms.author: anasyash
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: b1368e0c7764bed42aa7549f36a6f4bcbb96eff4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849770"
---
# <a name="date-of-vendor-vat-register"></a>Dato for kreditormomsregistrering

I Microsoft Dynamics 365 Finance version 10.0.24 findes det nye felt **Dato for kreditormomsregistrering** til kreditorfakturaer. Dette felt angiver datoen for den momspligtige levering for et køb.

Du kan aktivere det nye felt ved at gå til arbejdsområdet **Funktionsstyring**, finde og vælge funktionen **Aktivér dato for kreditormomsregistrering på kreditorfakturaer** og derefter vælge **Aktivér nu**.

Indgående fakturaer fra leverandørerne kan have to datoer: den dato, hvor kreditoren udstedte fakturaen, og datoen for den momspligtige levering (dvs. den dato, hvor kreditoren opkrævede moms). I nogle tilfælde kan disse to datoer være forskellige.

Du kan trække det indgående momsbeløb for en indkøbsfaktura fra og senere medtage fakturaen i momsrapporter på en dato, der afviger fra begge tidligere nævnte datoer. Denne dato styres af lokale lovgivningsregler om udskudt indgående momsfradrag for visse scenarier. Det varierer efter land eller område.

I visse momsrapporter, f.eks. [momsopgørelsen](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) i Tjekkiet, kræves det, at datoen for den momspligtige levering indberettes til et købsdokument. Denne dato skal rapporteres, så skattemyndighederne kan afstemme momsrapportering mellem modparter.

I Finance kan du definere datoer i følgende felter:

- **Fakturadato** – Den dato, hvor fakturaen blev udstedt af leverandøren.
- **Dato for momsregistrering** – Datoen for momsfradraget for købsfakturaen.
- **Dato for kreditormomsregistrering** – Datoen for leverandørens momspligtige levering.
- **Dato for dokumentmodtagelse** – Den dato, hvor du modtog fakturaen.

Disse felter vises på følgende sider:

- Kreditorfaktura
- Kreditorindgangsbog
- Godkendelse af kreditorfaktura
- kreditorfakturakladde

Når kreditorfakturaen er bogført, kan du gennemgå datoerne på siderne **Fakturajournal** og **Kreditorposteringer**.
