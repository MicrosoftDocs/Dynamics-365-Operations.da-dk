---
title: Designe konfigurationer til at generere rapporter i Office-format, der har integrerede billeder
description: Dette emne beskriver, hvordan du designer konfigurationer for at generere elektroniske dokumenter i Excel- og Word-format, der indeholder integrerede billeder.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944551"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Designe konfigurationer til at generere rapporter i Office-format, der har integrerede billeder

[!include [banner](../../includes/banner.md)]

For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Oprette en konfigurationsudbyder og markere den som aktiv". Denne procedure forklarer, hvordan du designer elektroniske rapporteringskonfigurationer (ER) for at generere et Microsoft Excel- og Word-dokument, der indeholder integrerede billeder. I denne procedure, skal du oprette de nødvendige ER konfigurationer for eksempelvirksomheden Litware, Inc. Disse trin kan udføres ved hjælp af USMF-datasættet. Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Før du begynder, skal du hente og gemme følgende filer: 

| Betegnelse                                          | Filnavn                   |
|------------------------------------------------------|-----------------------------|
| ER-datamodelkonfiguration                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| Konfiguration af ER-format                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Billede af firmalogo                                   | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Signaturbillede                                      | [Signature image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternativt signaturbillede                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word-skabelon til udskrivning af betalingschecks  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a>Kontrollere forudsætninger  
 1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.  
 2. Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".   
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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
