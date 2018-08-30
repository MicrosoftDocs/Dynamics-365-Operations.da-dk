--- 
title: "Oprette formater i elektronisk rapportering til optælling og opsummering"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 7261a2324b61cacfca8d69ad52762aa545b70220
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="create-electronic-reporting-er-formats-to-do-counting-and-summing"></a>Oprette formater i elektronisk rapportering (ER) til optælling og opsummering

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet. Disse trin kan udføres i en hvilken som helst virksomhed.

Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.

Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Få adgang til listen over de konfigurationer, der leveres af Microsoft
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Sørg for, at udbyderen "Litware, Inc." er tilgængelig og markeret som aktiv.  
2. Vælg udbyderen "Litware, Inc." .
3. Klik på Lagre.
    * Hvis der allerede findes et lager af typen "Operationsressourcer", kan du springe over de resterende trin i den aktuelle underopgave.  
4. Klik på Tilføj for at åbne dialogboksen.
5. Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.
6. Klik på Opretlager.
7. Klik på OK.

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Få de Intrastat-konfigurationer, der leveres af Microsoft
1. Klik på Åbn.
2. Vælg 'Intrastat-model\Intrastat (DE)' i træet.
3. Klik på Importer.
    * Klik på Importer for version 1.1 af den valgte konfiguration.  
4. Klik på Ja.
5. Luk siden.
6. Luk siden.
7. Klik på Rapporteringskonfigurationer.
8. Udvid 'Intrastat-model' i træet.
9. Vælg 'Intrastat-model\Intrastat (DE)' i træet.


