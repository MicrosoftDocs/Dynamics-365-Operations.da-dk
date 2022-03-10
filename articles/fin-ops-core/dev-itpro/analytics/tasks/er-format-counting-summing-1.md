---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 1: Oprettelsesformat)'
description: Dette emne beskriver, hvordan du konfigurerer et format for elektronisk rapportering til optælling og opsummering baseret på data fra det allerede genererede tekstoutput. (Del 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d1a90c0949e98b4c1e9ccb356d39de9c23b670c518ad14a99974ae2aed7301
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728183"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>ER Konfigurere format for at udføre optælling og sammenlægning (del 1: Oprettelsesformat)

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet. Disse trin kan udføres i en hvilken som helst virksomhed.

Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.

Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]