---
title: Ordreindtastningsfrister
description: "Denne artikel indeholder oplysninger om frister for ordreindtastning. En ordreindtastningsfrist er et cut-off-tidspunkt, der bestemmer, om en kundeordre skal behandles (og opfyldes), som om den blev modtaget på den aktuelle dag eller næste dag."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d865260679dac6196a69f3182f937df7f9fd8200
ms.lasthandoff: 03/31/2017


---

# <a name="order-entry-deadlines"></a>Ordreindtastningsfrister

Denne artikel indeholder oplysninger om frister for ordreindtastning. En ordreindtastningsfrist er et cut-off-tidspunkt, der bestemmer, om en kundeordre skal behandles (og opfyldes), som om den blev modtaget på den aktuelle dag eller næste dag.

I mange firmaer er det kun salgsordrer, der modtages før et bestemt tidspunkt på dagen, der behandles som modtaget den pågældende dag. Alle ordrer, der modtages efter dette tidspunkt, behandles, som om de modtages den næste arbejdsdag. Dette skæringstidspunkt for ordrer kaldes ordreindtastningsfristen.  

Ordreindtastningsfrister bruges som input for ordretilsagn. Derfor hjælper de dig med at administrere kundernes forventninger til levering af ordren. Kunderne kan for eksempel se, at hvis de afgiver en ordre hos dig inden et bestemt tidspunkt, giver du tilsagn om at levere varerne samme dag. Hvis de går glip af denne frist, kan de forvente levering kun på den næste arbejdsdag. Du kan angive ordreregistreringsfrister, der er baseret på dit lager faciliteter og levering luftfartsselskab tidsplaner.  

På siden **Ordreindtastningsfrister** kan du oprette ordreindtastningsfristerne for alle ugens dage. Hvis ordrer modtages efter det angivne tidspunkt, behandles de, som om de modtages den næste dag. Disse tider angives som standard til 23:59 (dvs. ét minut før midnat, inden den pågældende dag er gået). Du kan ændre standardtiderne, så de falder sammen med de faktiske tider for afsendelse eller tilgang.  

Du kan definere en ordreindtastningsfrist for en specifik kundegruppe. Du ønsker f.eks., at en bestemt gruppe kunder har ordreindtastningsfrister, der er senere end fristerne for andre kunder. I dette tilfælde skal du først definere grupper for ordreindtastningsfrister på siden **Ordreindtastningsfristgrupper**. Du tildeler derefter grupperne til kunder på siden **Kunder**.  

Hvis dit firma driver virksomhed fra flere adresser, kan du oprette ordreindtastningsfrister for de enkelte steder. Hvis disse steder er i forskellige tidszoner, oprettes ordreindtastningsfristerne i de enkelte steders tidszone. Men når du arbejder med salgsordrer og salgstilbud, omregnes ordreindtastningsfristen til din tidszone på siden **Mulige afsendelses- og modtagelsesdatoer**.  

På siden **Aktiver kombinationer af ordreindtastningsfrister** kan du definere kombinationer af steder og ordreindtastningsfristgrupper, der er tilladt.

## <a name="example-order-entry-deadline"></a>Eksempel: Ordreindtastningsfrist
Ordreindtastningsfristen på tirsdage er indstillet til 16:00. På en bestemt tirsdag kl. 17:00 forsøger du at indstille den aktuelle dato som afsendelsesdato. (Bemærk, at der ikke er nogen gennemløbstid i dette eksempel). Hvis de **Leveringsdatokontrol** er markeret, modtager du en advarsel, der angiver, at datoen ikke er gyldigt. Denne advarsel vises på siden **Mulige afsendelses- og modtagelsesdatoer**, hvor du kan vælge alternative datoer.

## <a name="example-different-order-entry-deadlines-per-site"></a>Eksempel: Forskellige ordreindtastningsfrister pr. sted
Dit firma udgøres af to steder. Stederne findes i forskellige tidszoner som vist i følgende tabel.

| Sted A                      | Sted B                      |
|-----------------------------|-----------------------------|
| Californien                  | Florida                     |
| PST (Pacific, normaltid) | EST (Eastern, normaltid) |

Der er angivet følgende ordreindtastningsfrister for sted A og B.

| Ugedag             | A: bestille ordreregistreringsfristerne (PST) | B: bestille ordreregistreringsfristerne (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Mandag                      | 13:00                          | 14:00                          |
| Tirsdag                     | 13:00                          | 14:00                          |
| Onsdag                   | 13:00                          | 14:00                          |
| Torsdag                    | 13:00                          | 14:00                          |
| Fredag                      | 13:00                          | 14:00                          |

Det er din opgave at behandle ordren i Utah, hvor tidszonen er MST (Mountain, normaltid). Det betyder, at hvis du afgiver ordrer hos sted A før kl. 14:00 MST og hos sted B før kl. 12:00 MST, overholder du ordreindtastningsfristerne for begge steder.  

I tabellen nedenfor vises, hvordan ordreindtastningsfristerne for sted A og B omregnet til MST-tidspunkter.

| Gruppe A: PST         | Gruppe A: MST        | Gruppe B: EST           | Gruppe B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00              | 14:00                 | 12:00              |

**Bemærk!** Hvis det er sommertid, justeres ordreindtastningsfristerne tilsvarende.

## <a name="example-same-order-entry-deadline-per-site"></a>Eksempel: Samme ordreregistreringsfrist pr. sted
Dit firma udgøres af to steder. Stederne findes i forskellige tidszoner som vist i følgende tabel.

| Sted A                      | Sted B                      |
|-----------------------------|-----------------------------|
| Californien                  | Florida                     |
| PST (Pacific, normaltid) | EST (Eastern, normaltid) |

Der er angivet følgende ordreindtastningsfrister for sted A og B.

| Ugedag | PST og EST |
|-----------------|-------------|
| Mandag          | 13:00       |
| Tirsdag         | 13:00       |
| Onsdag       | 13:00       |
| Torsdag        | 13:00       |
| Fredag          | 13:00       |

Det er din opgave at behandle ordren i Utah, hvor tidszonen er MST. Det betyder, at hvis du afgiver ordrer hos sted A før kl. 14:00 MST og hos sted B før kl. 11:00 MST, overholder du ordreindtastningsfristerne for begge steder. 

I tabellen nedenfor vises, hvordan ordreindtastningsfristerne for sted A og B omregnet til MST-tidspunkter.

| Gruppe A: PST         | Gruppe A: MST        | Gruppe B: EST           | Gruppe B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00              | 13:00                 | 11:00              |

**Bemærk!** Hvis det er sommertid, justeres ordreindtastningsfristerne tilsvarende.

<a name="see-also"></a>Se også
--------

[Delivery schedules](delivery-schedules.md)


