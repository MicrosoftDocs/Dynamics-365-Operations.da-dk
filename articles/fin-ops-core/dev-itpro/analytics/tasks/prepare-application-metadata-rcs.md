---
title: Klargøre programmetadata, der skal bruges i RCS
description: Dette emne beskriver, hvordan du opretter en ny rapporteringskonfiguration, der indeholder applikationsmetadata.
author: NickSelin
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71a33a69796b31c456bfcc5abbb3b18bcb1064be65c1c58b36656a9cebfbf47d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750568"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>Klargøre programmetadata, der skal bruges i RCS
[!include [banner](../../includes/banner.md)]

Følgende trin forklarer, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny elektronisk rapporteringskonfiguration (ER), der indeholder programmetadata til udformning af ER-modeltilknytningskonfigurationer i RCS (Regulatory Configuration Service). Denne konfiguration bruges til udformning af en eksempel-ER-modeltilknytningskonfiguration for at få adgang til udenlandske handelstransaktioner. I dette eksempel skal du oprette en konfiguration til eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i enhver virksomhed. For at fuldføre disse trin skal du først fuldføre trinnene i emnet [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="prerequisites"></a>Forudsætninger
1.    Gå til **Organisationsadministration** > **Arbejdsområder** > **Elektronisk rapportering**. 
2.    Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret konfigurationsudbydere, og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). 
3.    Klik på **Konfiguration af metadata**. 
4.    Antag, at RCS bruges til at designe en ER-løsning for et Finance and Operation-program, der vil generere elektroniske dokumenter, der indeholder oplysninger om forretningsdomæe til udenrigshandel. Hvis du vil angive tilknytningen mellem ER-datamodellen og kilderne til de påkrævede data, har vi behov for at få adgang til Finance and Operations i RCS. Som en del af designet af ER-løsningen konfigurerer vi en ny ER-metadatakonfiguration, der indeholder alle de metadata, der i øjeblikket er påkrævet for at generere ER-rapporter for det valgte forretningsdomæne. 

## <a name="add-metadata-configuration"></a>Tilføj konfiguration af metadata 
1.    Klik på **Opret konfiguration** for at åbne dialogboksen. 
2.    Skriv 'Udenrigshandelmetadata' i feltet **Navn**. 
3.    Klik på **Opret konfiguration**. 
4.    Klik på **Designer**. 
5.    Klik på **Tilføj**. 
  
> [!NOTE]
> Du kan enten vælge alle metadata for hele programmet eller for udvalgte modeller eller moduler. Bemærk i dette tilfælde, at følgende metadata vil blive tilføjet automatisk: tabeller over poster, fasttekster og udvidede datatyper (EDT'er). Når der kræves flere typer metadata, skal de tilføjes manuelt. 
 
Vi har nogle metadata, der er relateret til udenlandske handelstransaktioner, ved at vælge metadataelementer manuelt. 
  
6.    Klik på **Tilføj datakilde**. 
7.    Klik på **Tabelposter**. 
8.    Brug Quick Filter til at filtre på feltet **Navn** med værdien "Intrastat". 
9.    Vælg **Intrastat** -tabelposten. 
10.    Klik på **OK**.
  
Vi har tilføjet metadataoplysninger om Intrastat-tabellen med poster. 
  
11.    Gå til træet, og udvid **Tabelposter Intrastat**\>**Relationer**. 
12.    I træet skal du vælge **Tabelposter Intrastat**\>**Relationer\IntrastatCommodity (Tabelposter for EcoResCategory)**.     
13.    Klik på **Tilføj metadata**. 
  
> [!NOTE]
> Metadata om nødvendige relationer for den valgte tabel med poster skal tilføjes manuelt. 
  
16.    Klik på **Tilføj datakilde**. 
17.    Klik på **Fasttekst**. 
18.    Brug Quick Filter til at filtre på feltet **Navn** med værdien "IntrastatDirection". 
19.    Vælg posten **IntrastatDirection-fasttekst**. 
20.    Klik på **OK**. 
21.    Klik på **Gem**.  
22.    Luk siden. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>Fuldfør kladdeversionen af metadatakonfigurationen
1.    Klik på **Skift status**. 
2.    Klik på **Fuldfør**. 
3.    Klik på **OK**. 
4.    Vælg den fuldførte version **1**. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>Eksportér den fuldførte version af metadatakonfiguration fra program som en XML-fil
1.    Klik på **Udveksling**. 
2.    Klik på **Eksporter som XML-fil**. 
3.    Klik på **OK**. 
    
Den oprettede metadatakonfiguration er blevet gemt som en XML-fil, der kan importeres til RCS og bruges som kilden til oplysninger om metadata til forretningsdomænet for udenrigshandel. Baseret på disse oplysninger kan vi angive tilknytningen mellem programmetadata og ER-datamodel.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]