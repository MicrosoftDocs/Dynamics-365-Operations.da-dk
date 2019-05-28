---
title: Vælge datamodeldefinitioner, når du opretter formater
description: For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Oprette en konfigurationsudbyder og markere den som aktiv.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc357db8acbdb98741a694a8a9d3c0c0625c50e4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551083"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a>Vælge datamodeldefinitioner, når du opretter formater

[!include [task guide banner](../../includes/task-guide-banner.md)]

For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Oprette en konfigurationsudbyder og markere den som aktiv. 

Denne fremgangsmåde viser, hvordan rodelementet i en model kan vælges som en datamodeldefinition til indsættelse af en ER-formatkonfiguration, der er designet til at generere elektroniske dokumenter. I denne procedure skal du tilføje en ny ER-formatkonfiguration til eksempelfirmaet Litware Inc. 

Denne procedure er beregnet til brugere, der har fået tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Trinnene kan udføres ved hjælp af et vilkårligt datasæt.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren Opret en konfigurationsudbyder, og markér den som aktiv.  
2. Klik på Rapporteringskonfigurationer.

## <a name="add-a-new-er-data-model-configuration"></a>Tilføj en ny ER-datamodelkonfiguration
1. Klik på Opret konfiguration for at åbne dialogboksen.
    * Vi tilføjer en ny ER-modelkonfiguration, der indeholder en datamodel, der skal bruges som datakilde ved oprettelse af ER-rapporter.  
2. Skriv 'Betalingsmodel (fiktiv)' i feltet Navn.
    * Betalingsmodel (fiktiv)  
3. Klik på Opret konfiguration.
4. Klik på Designer.
    * Åbn ER-designeren for at angive strukturen af datamodellen i denne konfiguration.  
    * Antag, at vi udvikler datamodellen for en betalings forretningsdomæne for at understøtte 2 betalingsmetoder – pengeoverførsel og direkte debitering.  
5. Klik på Ny for at åbne dialogboksen Fjern.
6. Skriv 'Betalinger – kreditoverførsel' i feltet Navn.
    * Betalinger – kreditoverførsel  
7. Klik på Tilføj.
8. Klik på Ny for at åbne dialogboksen Fjern.
9. Skriv "Modelrod" i feltet Ny node som felt.
10. Skriv 'Betalinger – direkte debitering' i feltet Navn.
    * Betalinger – direkte debitering  
11. Klik på Tilføj.
12. Klik på Gem.
13. Luk siden.
14. Klik på Skift status.
    * Fuldfør kladdeversionen af modellen for at gøre den tilgængelig i nye modeltilknytninger og formater.  
15. Klik på Fuldført.
16. Klik på OK.

## <a name="start-to-enter-a-new-er-format-configuration"></a>Begynde at angive en ny ER-formatkonfiguration
1. Klik på Opret konfiguration for at åbne dialogboksen.
2. Skriv 'Format baseret på datamodel af typen Betalingsmodel (fiktiv)' i feltet Ny.
3. Indtast eller vælg en værdi i feltet Definition af datamodel.
    * Bemærk, at alle rodelementer i den valgte datamodel aktuelt kan vælges som datamodeldefinition. Du kan fortsætte med at designe dit format ved at bruge et af de krævede rodelementer i datamodellen. En manglende modeltilknytning for det valgte rodelementet forhindrer ikke, at du kan fortsætte.  
4. Luk siden.

## <a name="add-a-new-er-model-mapping-configuration"></a>Tilføje en ny ER-modeltilknytningskonfiguration
1. Klik på Opret konfiguration for at åbne dialogboksen.
2. Skriv 'Modeltilknytning baseret på datamodel af typen Betalingsmodel (fiktiv)' i feltet Ny.
3. Skriv 'Betalingsmodeltilknytninger (fiktiv)' i feltet Navn.
    * Betalingsmodeltilknytninger (fiktive)  
4. Indtast eller vælg en værdi i feltet Definition af datamodel.
5. Klik på Opret konfiguration.

## <a name="design-er-model-mappings"></a>Designe ER-modeltilknytninger
1. Klik på Designer.
    * Brug ER-designeren til at angive modeltilknytningerne for de krævede rodelementer.  
2. Klik på Designer.
    * Simuler indstilling af den valgte modeltilknytning for rodelementet i den valgte model.  
3. Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.
4. Klik på Tilføj rod.
5. Skriv Finans i feltet Navn.
6. Skriv "LedgerJournalTrans" i feltet Tabel.
    * LedgerJournalTrans  
7. Klik på OK.
8. Klik på Gem.
9. Luk siden.
10. Luk siden.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Begynde at angive en anden ny ER-formatkonfiguration
1. Vælg 'Betalingsmodel (fiktiv)' i træet.
2. Klik på Opret konfiguration for at åbne dialogboksen.
3. Skriv 'Format baseret på datamodel af typen Betalingsmodel (fiktiv)' i feltet Ny.
4. Indtast eller vælg en værdi i feltet Definition af datamodel.
    * Bemærk, at der nu kun findes ét rodelementet, som kan tilknyttes programdatakilderne. Når der introduceres mindst én modeltilknytning, er det kun modellens rodelementer, som er knyttet til programdatakilder, der kan vælges som modeldefinition, mens ER-formatet er tilføjet.   
5. Luk siden.

