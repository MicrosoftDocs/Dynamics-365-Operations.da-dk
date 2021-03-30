---
title: Likviditetsbudget (prøveversion)
description: Dette emne beskriver likviditetsbudgetteringsfunktionen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3e9237980144ea65e1ff5135e277151970dbfdbb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208599"
---
# <a name="cash-flow-forecast-preview"></a>Likviditetsbudget (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Pengestrømmen er kritisk for alle virksomheder. Selv rentable virksomheder kan udgøre en pålydende insolvens, hvis de ikke bevarer pengestrømmen, så de opfylder de umiddelbare behov. Muligheden for likviditetsbudgettering i økonomiske indsigter kan hjælpe virksomheder med at overvåge og styre deres kassesaldi effektivt. Denne funktion bruger Machine Learning til at hjælpe virksomheder med at forudsige pengestrømme mere præcist, end de tidligere har haft. Den kan også hjælpe ledere med at træffe beslutninger om at optimere mulighederne i forbindelse med deres aktuelle kasseposition. 

For de fleste firmaer er administration af pengestrømme og kørsel af likviditetsbudget en kedelig, gentaget og manuel proces. De fleste firmaer anvender Microsoft Excel-løsninger med varierende grad af kompleksitet. Udfordringerne ved præcis prognosticering af likviditet omfatter følgende:

- Der er ingen tilgængelige data for beslutningstagere, da disse er spredt flere steder, herunder: 
  - Regnskabs- eller virksomhedsressourceplanlægningssystemet
  - Software til økonomisk planlægning
  - Excel
  - Yderligere programmer 
- Prognoser er baseret på en intern viden, der ligger i "siloer" inden for hvert domæne eller hver afdeling.
- Måling af nøjagtigheden af likviditetsbudgettering, efter at regnskaberne er realiseret, er usikker og svær.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Oplysninger om muligheden for likviditetsbudgetter
Funktionen til likviditetsbudgetter indeholder følgende funktioner. 

- Gør det nemt at integrere pengestrømsdata fra eksterne systemer med Dynamics 365 Finance. Likviditetsbudgetter kan også bruge dataimport-eksportstrukturen. Denne struktur gør det nemt at integrere med Excel OData. Du kan også kombinere data fra flere kilder for at oprette en omfattende likviditetsløsning. 

- Introducerer intelligent kasseposition. Der oprettes en kasseposition på baggrund af kundens betalingsmåde for at forudsige, hvornår et firma kan forvente at betale kontanter i deres konti. Den analyserer også de historiske mønstre for udbetalende kreditorer for at forudsige, hvornår de fremtidige fakturaer og ordrer vil blive betalt. 

- Introducerer intelligent likviditetsbudgettering ved langsigtet budgettering ved hjælp af tidsserieprognoser via automatiseret integration med AI Builder.

- Gør det muligt at gemme bestemte likviditetsposter eller -budgetter, redigere dem og derefter nemt sammenligne og måle prognosen for ydeevnen for de faktiske regnskaber.

- Aktiverer hvad hvis-analyse via snapshot-sammenligning. Du kan f. eks. oprette flere snapshots, der repræsenterer optimistiske, pessimistiske og de mest realistiske visninger af din likviditet og derefter sammenligne og få vist forskellene.

- Giver mulighed for at se likviditetsbudgettet i flere valutaer, på tværs af juridiske enheder og filtrere og få vist pengestrømme, der vedrører en bankkonto. 

- Giver dig mulighed for at filtrere og få vist bankkonti, der er knyttet til økonomiske dimensioner.

Funktionen til likviditetsbudget i Dynamics 365 Finance vil sætte organisationen i stand til at transformere den kedelige, komplekse, men gentagende likviditetsprojicering til en simpel, automatiseret proces. Automatisering af de mest kedelige aspekter ved likviditetsbudgettering giver dig mulighed for at fokusere på vigtig beslutning om at drive de ønskede firmaresultater.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Konfigurere dimensioner for likviditetsbudgettering
En ny fane på siden **Konfiguration af likviditetsbudgettering** giver dig mulighed for at styre, hvilke økonomiske dimensioner der skal bruges til filtrering i arbejdsområdet **Likviditetsbudgettering**. Denne fane vises kun, når funktionen Likviditetsbudgetter er aktiveret. 

Under fanen **Dimensioner** skal du vælge på den liste over dimensioner, der skal bruges til filtrering, og bruge piletasterne til at flytte dem til højre kolonne. Der kan kun vælges to dimensioner til filtrering af data i likviditetsbudgettet. 

#### <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]