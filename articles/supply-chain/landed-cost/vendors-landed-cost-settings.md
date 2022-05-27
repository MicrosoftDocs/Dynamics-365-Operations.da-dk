---
title: Kreditorindstillinger tilføjet for omkostninger for Landingsomkostninger
description: I dette emne beskrives de nye felter, der føjes til den eksisterende kreditorside, når du aktiverer modulet Landingsomkostninger. Du kan bruge disse felter til at konfigurere de kreditorer, du vil bruge sammen med funktionerne til Landingsomkostninger.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b4e02397f7a4cdeaa21b451268b16e4fbe773612
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690520"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Kreditorindstillinger tilføjet for omkostninger for Landingsomkostninger

[!include [banner](../../includes/banner.md)]

Når du aktiverer modulet **Landingsomkostninger**, føjes flere nye felter til den eksisterende **Kreditorer**-side. Du kan bruge disse felter til at konfigurere de kreditorer, du vil bruge sammen med funktionerne til Landingsomkostninger.

Hvis du vil angive de relevante felter, skal du gå til **Indkøb og forsyning \> Kreditorer \> Alle kreditorer**. Åbn en eksisterende kreditor, eller opret en ny kreditor, og vælg derefter oversigtspanelet **Diverse oplysninger**. Alle de nye felter, som modulet **Landingsomkostninger** tilføjer, vises under overskriften **Fragter**. I følgende tabel beskrives felterne.

| Felt | Beskrivelse |
|---|---|
| Forsendelsestype | <p>Vælg kreditorens rolle i forhold til Landingsomkostninger:</p><ul><li>**Ingen** – Kreditoren har ingen bestemt rolle, der er relateret til Landingsomkostninger. Denne værdi er standardindstillingen, da de fleste kreditorer sandsynligvis ikke har nogen bestemt rolle.</li><li>**Fragtfirma** – Kreditoren er et fragtfirma. Kreditorer, der har denne forsendelsestype, kan vælges i feltet **Fragtfirma** på siden **Fragter**.</li><li>**Toldagent** – Kreditoren er en toldagent. Kreditorer, der har denne forsendelsestype, kan vælges i feltet **Toldagent** på siden **Porteføljer**.</li><li>**Agent** – Kreditoren er en agent. Kreditorer, der har denne forsendelsestype, kan vælges i feltet **Agent** på siderne **Kreditorer** og **Indkøbsordrer**.</li></ul> |
| Omkostningstypegruppe | Knyt kreditoren til en omkostningstypegruppe for at vælge [automatiske omkostninger](auto-cost-setup.md). |
| Fra havn | Vælg oprindelseshavnen for fragten. |
| Agent | Standardagenten, når der foretages køb fra kreditoren. |
| Leverandør af importefterkalkulation | <p>Angiv, om kreditoren er for Landingsomkostninger.</p><p>**Tip:** Du kan bruge dette felt sammen med sikkerhed på postniveau til at begrænse de indkøbsordrer, der vises, når der oprettes en fragt.</p> |
| Fragtfirma | Vælg det standardfragtfirma, der bruges, når der oprettes indkøbsordrer for kreditoren. |
| Tjenesteudbyder | Angiv, om kreditoren er tjenesteudbyder. |
| Over/under-tolerancegruppe | Vælg standardtolerancegruppen for over/under for kreditoren. |
