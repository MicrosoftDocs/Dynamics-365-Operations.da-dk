---
title: Oprette en ny model for produktkonfiguration
description: Denne procedure viser, hvordan du opretter en produktkonfigurationsmodel og indsætter stamoplysninger som f.eks. attributter og underkomponenter.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921359"
---
# <a name="create-a-product-configuration-model"></a>Oprette en ny model for produktkonfiguration

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter en produktkonfigurationsmodel og indsætter stamoplysninger som f.eks. attributter og underkomponenter. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-a-product-model"></a>Oprette en produktmodel

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.
1. Vælg **Ny**.
1. Skriv en værdi i feltet **Navn**.
1. Indtast en værdi i feltet **Beskrivelse**.
1. Vælg en indstilling i feltet **Strategi for problemløser**.
    * Problemløserstrategien bestemmer, hvordan begrænsningerne i en begrænsningsbaseret model til produktkonfiguration behandles. Dette valg kan have indflydelse på produktkonfigurationsmodellens ydeevne.  
1. Skriv en værdi i feltet **Navn**.
    * Rodkomponenten repræsenterer produktkonfigurationsmodellen, men den kan også bruges i andre produktmodeller.  
1. Vælg **OK**.
1. I feltet **Genbrug konfigurationer** skal du vælge en indstilling.
    * Hvis genbrugskonfigurationsparameteren er indstillet til Ja, vil systemet søge efter identiske konfigurationer efter hver konfigurationssession, og genbruge, hvis der findes en nøjagtig match.  

## <a name="add-attributes"></a>Tilføj attributter

1. Udvid sektionen **Attributter**.
2. Vælg **Tilføj**.
3. Markér den valgte række på listen.
4. Skriv en værdi i feltet **Navn**.
5. Skriv en værdi i feltet **Navn på problemløser**.
    * Problemløserens navn bruges til løsning af begrænsningsproblemer i variantstyringen. Det må ikke indeholde mellemrum eller specialtegn, undtagen _ (understregning).  
6. Indtast en værdi i feltet **Beskrivelse**.
    * Beskrivelsesteksten vises til brugeren af konfigurationen og kan derfor fungere som hjælp til at vælge den rigtige attributværdi.  
7. Indtast eller vælg en værdi i feltet **Attributtype**.
    * Attributtypen bestemmer, hvilke værdier der er tilgængelige for attributten.  
8. Marker afkrydsningsfeltet **Medtag i genbrug**.
    * Denne indstilling er kun tilgængelig, når indstillingen Genbrug konfigurationer er valgt. Når attributten medtages i genbrugsafkrydsningsfeltet betyder det, at denne attribut medtages, når systemet søger efter et nøjagtigt match.  

## <a name="add-subcomponents"></a>Tilføj underkomponenter

1. Udvid sektionen **Underkomponenter**.
2. Vælg **Tilføj**.
3. Markér den valgte række på listen.
4. Skriv en værdi i feltet **Navn**.
5. Skriv en værdi i feltet **Navn på problemløser**.
6. Indtast en værdi i feltet **Beskrivelse**.
7. Indtast eller vælg en værdi i feltet **Komponent**.
    * Hver underkomponent skal referere til en komponent-definition. Dette design understøtter genanvendelige komponenter og sikrer, at når en komponent er defineret, kan den bruges i mange produktmodeller.  
8. Vælg **Gem**.
9. Vælg **Oplysninger om styklistelinjer**.
    * Formularen Linjedetaljer i stykliste gør det muligt for brugeren at vælge de nødvendige egenskaber for underkomponenten. Hver egenskab kan gives en fast værdi eller knyttes til en attribut. Tilknytning til en attribut medfører, at linjeegenskaben for styklisten få andre værdier, afhængigt af den valgte konfiguration.  
10. Indtast eller vælg en værdi i feltet **Varenummer**.
    * Hver underkomponent repræsenterer konfigurerbare produktmaster med begrænsningsbaseret konfigurationsteknologi. Referencen sker via varenummeret.  
11. Marker afkrydsningsfeltet **Indstil**.
12. Vælg **Ja** i feltet **Beregning**.
    * Indstilling af beregning sikrer, at produktet skal medtages, når du kører en omkostningsberegning for produktet.  
13. Vælg fanen **Opsætning**.
14. Marker afkrydsningsfeltet **Indstil**.
15. Angiv et tal i feltet **Antal**.
    * Antalsfeltet, der bestemmer, hvor meget af dette produkt, der forbruges i det konfigurerede produkt.  
16. Marker afkrydsningsfeltet **Indstil**.
17. Angiv et nummer i feltet **Pr. serie**.
18. Vælg **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]