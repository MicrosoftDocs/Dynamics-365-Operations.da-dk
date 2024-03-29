---
title: Arbejdsområdet Kontrolliste for datavalidering
description: I arbejdsområdet Kontrolliste for datavalidering kan du spore processer til validering af data på tværs af firmaer, områder og personer.
author: bking
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: bking
ms.assetid: ''
ms.search.form: DataValidationWorkspace
ms.openlocfilehash: fb8999815e96c0aa7d1a054073de77a382c14263
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272476"
---
# <a name="data-validation-checklist-workspace"></a>Arbejdsområdet Kontrolliste for datavalidering

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikel indeholder en oversigt over **Arbejdsområdet Kontrolliste for datavalidering** og den tilknyttede konfiguration.

I arbejdsområdet **Kontrolliste for datavalidering** kan du spore processer til validering af data på tværs af firmaer, områder og personer. Kontrollisten kan bruges under en ny implementering efter en opgradering eller efter en overførsel. Afhængigt af visningen af arbejdsområdet **Kontrolliste for datavalidering** kan du se enten alle opgaver og statusser for et datavalideringsprojekt eller blot de opgaver, der er tildelt til dig.

Du skal først vælge datavalideringsprojekt øverst i arbejdsområdet. Alle data, der vises i arbejdsområdet, filtreres derefter ud fra det valgte datavalideringsprojekt.

## <a name="summary-tiles"></a>Oversigt over felter

Feltet **Oversigt** giver et overblik over processen, og indikatorer hjælper dig med at holde datavalideringsprocessen på sporet. Du kan se de resterende opgaver, fuldførte opgaver, igangværende opgaver og ikke-startede opgaver for processen. Disse oplysninger er for alle firmaer, der er inkluderet i det valgte datavalideringsprojekt.

## <a name="tasks-and-status-section"></a>Opgaver og statussektion

I afsnittet **Opgaver og status** vises status for det samlede datavalideringsprojekt på forskellige måder: status efter juridisk enhed, efter område og efter opgaveliste. Du kan vælge filteret for at få vist status for en bestemt virksomhed. Hver statusfane viser en opdeling efter den procentdel, som er afsluttet, og antallet af opgaver, der er tilbage.

Den sidste fane er for den detaljerede opgaveliste. Denne liste viser den fuldstændige opgaveliste. Du kan filtrere opgavelisten på flere måder. Klik på **Rediger opgave** for at ændre status for en opgave eller tildele en opgave. Klik på **Vedhæftede filer** for at få vist vedhæftede filer for en opgave.

Opgavenavnet er et hyperlink til siden, som brugeren skal gå til for at fuldføre arbejdet. Du kan angive dette hyperlink ved hjælp af feltet **Menupunktnavn**, når du redigerer eller opretter en opgave fra formularen **Konfigurer datavalideringsprojekt**.

Du kan vedhæfte filer, noter, billeder og URL-adresser til en opgave ved hjælp af handlingen **Vedhæftede filer**. Du kan f.eks. tilknytte en rapportfil, som blev udskrevet for en opgave. Der vises et ikon i kolonnen **Vedhæftet fil** for opgaven, hvis der findes en vedhæftet fil.

Indstillingen **Fuldført af** bliver udfyldt automatisk, når opgaven er fuldført, med navnet på den arbejder, der har fuldført opgaven. Når en opgave er markeret som fuldført, opdateres feltet **Fuldførelsesdato** automatisk med den aktuelle dato og klokkeslæt.

## <a name="configure-data-validation-project-page"></a>Siden Konfigurer datavalideringsprojekt

Før du kan bruge arbejdsområdet **Kontrolliste for datavalidering**, skal du konfigurere processen ved hjælp af siden **Konfigurer datavalideringsprojekt**. (Klik på **Arbejdsområder** \> **Kontrolliste for datavalidering** \> **Konfigurer datavalideringsprojekt**).

## <a name="task-areas"></a>Opgaveområder

Du bruger opgaveområder til at gruppere datavalideringsopgaver i logiske ejerskabsområder i organisationen. Kreditor, Debitor eller Finans kan eksempelvis bruges som opgaveområder.

**Menupunktnavn** er knyttet til arbejdsindsatsen for opgaven og kan bruges til at gå direkte til den tilknyttede side fra opgavelinket i arbejdsområdet. F.eks. kan en datavalideringsopgave, der skal køre rapporten **Kreditor aldersfordelt** for Kreditor, knyttes til siden **Rapport over Kreditor aldersfordelt**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
