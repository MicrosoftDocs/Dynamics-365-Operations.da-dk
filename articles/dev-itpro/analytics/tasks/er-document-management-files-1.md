--- 
title: 'ER Brug dokumentstyringsfiler i formatoutput (del 1: Forbedret datamodel)'
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 00d366e61077e27a13b13e31a55acc89ae2b0cd0
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="er-use-document-management-files-in-format-outputs-part-1-prepare-data-model"></a>ER Brug dokumentstyringsfiler i formatoutput (del 1: Forberede datamodel)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER. Disse trin kan udføres i en hvilken som helst virksomhed.

Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.

Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Få adgang til listen over de konfigurationer, der leveres af Microsoft
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Sørg for, at udbyderen 'Litware, Inc.' er tilgængelig og markeret som aktiv.  
2. Vælg udbyderen Litware, Inc. .
3. Klik på Lagre.
    * Hvis der allerede findes et lager af typen "Operationsressourcer", kan du springe over de resterende trin i den aktuelle underopgave.  
4. Klik på Tilføj for at åbne dialogboksen.
5. Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.
6. Klik på Opretlager.
7. Klik på OK.

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Hent de konfigurationer for kundefakturamodelle, der leveres af Microsoft
1. Klik på Vis filtre.
2. Anvend følgende filtre: Angiv filterværdien "Operationsressourcer" i feltet "Navn" ved hjælp af filteroperatoren "starter med". Angiv filterværdien "" i feltet "Beskrivelse" ved hjælp af filteroperatoren "starter med"
3. Klik på Vis filtre.
4. Klik på Åbn.
5. Vælg 'Debitorfakturamodel' i træet.
    * Vælg modelkonfigurationen 'Debitorfakturamodel' for at importere den.  
6. Klik på Importer.
    * Klik på Importer for version 1 af den valgte konfiguration.  
7. Klik på Ja.
8. Luk siden.
9. Luk siden.
10. Klik på Rapporteringskonfigurationer.
11. Vælg 'Debitorfakturamodel' i træet.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Opret den afledte model for at understøtte adgang til filerne fra Dokumentstyring.
    * Du vil oprette vores egen konfiguration af kundens fakturamodel, der er afledt af den konfiguration, der leveres af Microsoft. Du skal bruge denne konfiguration til at implementere adgang til filerne fra Dokumentstyring og gøre dem tilgængelige for elektroniske dokumenter, som du opretter ud fra denne model.  
1. Klik på Opret konfiguration for at åbne dialogboksen.
2. Skriv 'Afled fra navn: Debitorfakturamodel, Microsoft' i feltet Ny.
3. Skriv "Debitorfakturamodel (brugerdefineret)" i feltet Navn.
    * Debitorfakturamodel (brugerdefineret)  
4. Klik på Opret konfiguration.


