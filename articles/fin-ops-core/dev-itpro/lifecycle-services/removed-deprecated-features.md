---
title: Fjernede eller udfasede funktioner i Lifecycle Services (LCS)
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive udfaset fra Microsoft Dynamics Lifecycle Services (LCS).
author: sericks007
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c792d06e9b0aa42919de924bdcc9118358779b72
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885449"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a>Fjernede eller udfasede funktioner i Lifecycle Services (LCS)

[!include[banner](../includes/banner.md)]

I dette emne beskrives funktioner, der er blevet fjernet eller udfases for Microsoft Dynamics Lifecycle Services (LCS).

- En *fjernet* funktion er ikke længere tilgængelige i tjenesten.
- En *udfaset* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er stillet tilrådighed, så du kan tage disse fjernelser og udfasninger med i din egen planlægning.

## <a name="october-2019-announcements"></a>Meddelelser for oktober 2019

### <a name="flowchart-diagrams-in-business-process-modeler"></a>Rutediagrammer i forretningsmodeldesigneren

<table>
<tbody>
<tr>
<td><strong>Årsagen til forældelsen/fjernelsen</strong></td>
<td>Vi fraråder komponenten rutediagram i forretningsmodeldesigneren (BPM), fordi det forældre design forårsagede lavt forbrug.</td>
</tr>
<tr>
<td><strong>Erstattet af en anden funktion?</strong></td>
<td>Nr.</td>
</tr>
<tr>
<td><strong>Påvirkede områder</strong></td>
<td>Forretningsmodeldesigner</td>
</tr>
<tr>
<td><strong>Status</strong></td>
<td>Udfaset: Komponenten rutediagram i BPM forventes fjernet i begyndelsen af februar 2020. Følgende funktion fjernes:
<ul>
<li>Eksisterende rutediagrammer vil ikke være tilgængelige til visning eller redigering. De figuregenskaber, der er tilknyttet rutediagramaktiviteter, vil heller ikke være tilgængelige, fordi hele fanen <strong>Rutediagram</strong> vil blive fjernet. Disse rutediagrammer omfatter både standardrutediagrammer, der genereres automatisk, og tilpassede rutediagrammer, der er ændret på grundlag af disse standardrutediagrammer.</li>
<li>Funktionen legacy fit/Gab-analyse vil ikke være tilgængelig. Derfor vil der ikke automatisk blive oprettet en gab-liste, og den kan heller ikke eksporteres.
<p><strong>Bemærk:</strong> Denne funktion er tidligere blevet udfaset og erstattet af Microsoft Azure DevOps-integrationer.</p>
</li>
<li>Versionsoversigten for rutediagrammet vil ikke være tilgængelig.</li>
</ul>
</td>
</tr>
</tbody>
</table>
