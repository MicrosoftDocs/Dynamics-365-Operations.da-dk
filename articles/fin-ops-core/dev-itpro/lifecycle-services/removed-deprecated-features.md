---
title: Fjernede eller udfasede funktioner i Lifecycle Services (LCS)
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive udfaset fra Microsoft Dynamics Lifecycle Services (LCS).
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b49a6f26b4c2fa895fe0e49f716ce423c3c0057
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559079"
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
<td>Udfaset: Komponenten rutediagram i BPM forventes fjernet i 2020. Følgende funktion vil ikke være tilgængelig:
<ul>
<li>Alle rutediagrammer er skrivebeskyttede og kan ikke redigeres. De figuregenskaber, der er knyttet til rutediagramaktiviteter, vil også være tilgængelige. Disse rutediagrammer omfatter både standardrutediagrammer, der genereres automatisk, og tilpassede rutediagrammer, der er ændret på grundlag af disse standardrutediagrammer.</li>
<li>Procestrin er skrivebeskyttede og kan ikke redigeres.</li>     
<li>Funktionen legacy fit/Gab-analyse vil ikke være tilgængelig. Derfor vil der ikke automatisk blive oprettet en gab-liste, og den kan heller ikke eksporteres.
<p><strong>Bemærk:</strong> Denne funktion er tidligere blevet udfaset og erstattet af Microsoft Azure DevOps-integrationer.</p>
</li>
<li>Versionsoversigten for rutediagrammet vil ikke være tilgængelig.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]