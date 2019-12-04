---
title: Designe konfigurationer til at generere rapporter i Office-format, der har integrerede billeder
description: Trinnene i dette emne giver dig oplysninger om, hvordan du designer elektroniske rapporteringskonfigurationer (ER), der genererer elektroniske dokumenter i Microsoft Office-formater (Excel og Word), der indeholder integrerede billeder.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
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
ms.openlocfilehash: 143782413359d87f3d4c46940f9a699fbf0e8f90
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769803"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Designe konfigurationer til at generere rapporter i Office-format, der har integrerede billeder

[!include [task guide banner](../../includes/task-guide-banner.md)]

For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Oprette en konfigurationsudbyder og markere den som aktiv". Denne procedure forklarer, hvordan du designer elektroniske rapporteringskonfigurationer (ER) for at generere et Microsoft Excel- og Word-dokument, der indeholder integrerede billeder. I denne procedure, skal du oprette de nødvendige ER konfigurationer for eksempelvirksomheden Litware, Inc. Disse trin kan udføres ved hjælp af USMF-datasættet. Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Før du går i gang, skal du hente og gemme filerne, der er vist i Hjælp-emnet [Integrer billeder og figurer i dokumenter, du har genereret ved hjælp af ER](../electronic-reporting-embed-images-shapes.md). Filerne er: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png og Cheque template Word.docx.

## <a name="verify-prerequisites"></a>Kontrollere forudsætninger  
 1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.  
 2. Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren "Oprette en konfigurationsudbyder og markere den som aktiv".   
 3. Klik på Rapporteringskonfigurationer.  
 
## <a name="add-a-new-er-model-configuration"></a>Tilføj en ny ER-modelkonfiguration  
 1. I stedet for at oprette en ny model, kan du indlæse ER-modellens konfigurationsfil (Model for checks.xml), som du har gemt tidligere. Denne fil indeholder eksempeldatamodellen for checkbetaling og tilknytning af datamodellen til datakomponenterne i Dynamics 365 for Operations-programmet.   
 2. Klik på Udveksling i oversigtspanelet Versioner.   
 3. Klik på Indlæs fra XML-fil.  
 4. Klik på Gennemse, og vælg derefter Model for checks.xml.   
 5. Klik på OK.  
 6. Den indlæste model bruges som datakilde for oplysninger til at oprette dokumenter, der indeholder billeder i Excel og Word.  

## <a name="add-a-new-er-format-configuration"></a>Tilføje en ny ER-formatkonfiguration  
 1. I stedet for at oprette er nyt format, kan du indlæse ER-formatets konfigurationsfil (Checkudskrivningsformat.xml), som du har gemt tidligere. Denne fil indeholder prøvelayoutet af formatet til udskrivning af checks ved hjælp af den fortrykte formular og tilknytningen af dette format til datamodellen 'Model for checks'.   
 2. Klik på Udveksling.  
 3. Klik på Indlæs fra XML-fil.  
 4. Klik på Gennemse, og vælg Checkudskrivningsformat.xml-filen.   
 5. Klik på OK.  
 6. Udvid 'Model for checks' i træet.  
 7. Vælg 'Model for checks\Checkudskrivningsformat' i træet.  
 8. Det indlæste format bruges til at oprette dokumenter, der indeholder billeder i Excel og Word.   

## <a name="configure-er-user-parameters"></a>Konfigurere ER-brugerparametre  
 1. Klik på Konfigurationer i handlingsruden.  
 2. Klik på Brugerparametre.  
 3. Vælg Ja i feltet Indstillinger for kørsel.  
  Aktivér flaget 'Udkast til kørsel' for at starte kladdeversionen af det valgte format i stedet for den, der er afsluttet.  
 4. Klik på OK.  

## <a name="configure-cash--bank-management-parameters"></a>Konfigurerer Likviditets- og bankstyringsparametre  
 1. Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.  
 2. Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "USMF OPER".  
 3. Klik på Konfigurer i handlingsruden.  
 4. Klik på Kontroller.  
 5. Udvid sektionen Konfiguration.  
 6. Klik på Rediger.  
 7. Vælg Ja i feltet Firmalogo.  
 8. Klik på Firmalogo.  
 9. Klik på Skift.  
 10. Klik på Gennemse, og vælg den fil, du tidligere har hentet, Firmalogo.png.   
 11. Klik på Gem.  
 12. Luk siden.  
 13. Udvid sektionen Signatur.  
 14. Vælg Ja i feltet Udskriv første underskrift.  
 15. Klik på Skift.  
 16. Klik på Gennemse, og vælg den fil, du tidligere har hentet, Signaturbillede.png.   
 17. Udvid sektionen Kopier.  
 18. Vælg en indstilling i feltet Vandmærke.  
 19. Vælg Ja i feltet Generisk elektronisk eksportformat.  
 20. Vælg konfiguration af 'Checkudskrivningsformat'.  
 21. Det valgte ER-format bliver nu brugt til udskrivning af checks.  
 22. Klik på Vedhæft.  
 23. Klik på Ny.  
 24. Klik på Filer.  
 25. Klik på Gennemse, og vælg den fil, du tidligere har hentet, Signaturbillede 2.png.   
 26. Luk siden.  
 27. Luk siden.  
 28. Luk siden.  
 29. Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre  
 30. Vælg Ja i feltet Tillad oprettelse af adviseringer for inaktive bankkonti:  
 31. Klik på Gem.  
 32. Luk siden.  
