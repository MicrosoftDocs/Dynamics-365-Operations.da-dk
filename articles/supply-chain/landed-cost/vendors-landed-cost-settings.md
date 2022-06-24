---
title: Kreditorindstillinger tilføjet for omkostninger for Landingsomkostninger
description: Denne artikel beskriver de nye felter, der føjes til den eksisterende kreditorside, når du aktiverer modulet Landingsomkostninger. Du kan bruge disse felter til at konfigurere de kreditorer, du vil bruge sammen med funktionerne til Landingsomkostninger.
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
ms.openlocfilehash: 84d1dee0815b036a3d411eabff49d8a08249bed3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882570"
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
