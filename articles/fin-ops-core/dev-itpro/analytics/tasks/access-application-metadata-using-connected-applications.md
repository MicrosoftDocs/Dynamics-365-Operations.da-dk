---
title: Få adgang til programmetadata ved hjælp af tilsluttede programmer
description: Fremgangsmåden i denne artikel forklarer, hvordan en Regulatory Configuration Service-bruger kan designe en ny elektronisk rapporteringsmodel ved hjælp af metadata.
author: NickSelin
ms.date: 06/29/2019
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
ms.openlocfilehash: b24d865bff0e81f79e7edde360fd5115d8637b42
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111225"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Få adgang til programmetadata ved hjælp af tilsluttede programmer

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en RCS-bruger (Regulatory Configuration Service) i rollen Systemadministrator eller Udvikler til elektronisk rapportering kan designe en ny ER-modeltilknytning ved hjælp af metadataene i finans og drift. Du kan få adgang til programmetadata online ved hjælp af det RCS-tilsluttede program. Eksempel på ER-modeltilknytning konfigureres til at give adgang til udenrigshandelstransaktioner. For at fuldføre disse trin skal du i RCS først fuldføre trinnene i artiklen [Opret konfigurationsudbydere og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). Hvis du ikke har fuldført trinnene i artiklen [Få adgang til programmetadata ved hjælp af ER-konfiguration](access-application-metadata-er-configuration.md), skal du downloade [Eksempler for elektronisk rapportering](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) og gemme følgende ER-konfigurationer: Udenrigshandelmetadata.xml, Udenrigshandelmodel.xml, Tilknytning af udenrigshandel.xml og derefter udføre trinnene i proceduren.

## <a name="prerequisites"></a>Forudsætninger
1. Gå til **Alle arbejdsområder** > **Elektronisk rapportering**. 
2. Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret konfigurationsudbydere, og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="get-required-er-configurations"></a>Få de nødvendige ER-konfigurationer
1. Klik på **Rapporteringskonfigurationer**. 
2. Hvis du allerede har udført trinnene i proceduren [Få adgang til programmetadata ved hjælp af ER-konfiguration](access-application-metadata-er-configuration.md), har du allerede alle de nødvendige ER-konfigurationer (konfigurationer af metadata til udenrigshandel, model og tilknytning) i den aktuelle RCS-forekomst. Du kan springe over resten af trinnene i denne underordnede opgave. 
3. Klik på **Udveksling**. 
4. Klik på **Indlæs fra XML-fil**. 
5. Klik på **Gennemse**, og vælg filen **Udenrigshandelmetadata.xml**. 
6. Klik på **OK**. 
7. Klik på **Udveksling**. 
8. Klik på **Indlæs fra XML-fil**. 
9. Klik på **Gennemse**, og vælg filen **Udenrigshandelmodel.xml**. 
10. Klik på **OK**. 
11. Klik på **Udveksling**. 
12. Klik på **Indlæs fra XML-fil**. 
13. Klik på **Gennemse**, og vælg filen **Tilknytning af udenrigshandel.xml**. 
14. Klik på **OK**. 

## <a name="register-a-connected-application"></a>Registrere et tilsluttet program
1. Luk siden. 
2. Luk siden. 
3. Gå til **Alle arbejdsområder** > **Elektronisk rapportering**. 
4. Klik på **Tilsluttede programmer**. 
5. Sørg for, at det konfigurerede program er Azure-baseret og tilgængeligt for den aktuelle RCS-bruger. Det kræves også, at den aktuelle RCS-bruger har adgang til det valgte program og er registreret som bruger af dette program og dermed får en rolle, som giver adgangsrettigheder til programmets metadata. 
6. Klik på **Ny**. 
7. Skriv 'MyConnectedApp' i feltet **Navn**. 
8. I feltet **Program** skal du skrive 'https://mycompany.operations.dynamics.com'. 
9. Skriv 'mycompany.onmicrosoft.com' i feltet **Lejer**. 
10. Klik på **Gem**. 
11. Når du kontrollerer forbindelsen til det konfigurerede program, skal du på siden **Opret forbindelse til eksternt program** klikke på linket **Klik her for at oprette forbindelse til det valgte eksterne program**. 
12. Klik på **Kontrollér forbindelsen**. 
13. Klik på **Luk**. 
14. Når forbindelsen er valideret korrekt, opdateres versions- og lejeroplysningerne for det konfigurerede program i det aktuelle gitter. 

## <a name="review-existing-model-mapping-configuration"></a>Gennemgå eksisterende modeltilknytningskonfiguration
1. Luk siden. 
2. Klik på **Rapporteringskonfigurationer**. 
3. Udvid **Udenrigshandelmodel** i træet. 
4. I træet skal du vælge **Udenrigshandelmodel\Tilknytning af udenrigshandel**. 
5. Udvid sektionen **Forudsætninger**. 

    > [!NOTE]
    > I øjeblikket refererer denne tilknytning til metadatakonfigurationen. Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet. 

6. Klik på **Designer**. 
7. Klik på **Designer**. 
8. Vælg **Dynamics 365 for Operations\Tabelposter** i træet. 
9. Klik på **Tilføj rod**. 
10. Indtast eller vælg en værdi i feltet **Tabel**. 

    > [!NOTE]
    > I øjeblikket refererer denne tilknytning til metadatakonfigurationen. Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet. 

11. Klik på **Annuller**. 
12. Luk siden. 
13. Luk siden. 

## <a name="assign-connected-application-to-model-mapping"></a>Tildele modeltilknytning tilknyttet program 
1. Klik på **Rediger**. 
2. Vælg **MyConnectedApp**-program. 

    > [!NOTE]
    > I øjeblikket refererer denne tilknytning til metadataene for det valgte tilsluttede program. Når den samme tilknytning refererer til metadatakonfigurationen og det tilknyttede program samtidig, bruges metadata for det tilknyttede program. 

3. Klik på **Designer**. 
4. Klik på **Designer**. 
5. Vælg **Dynamics 365 for Operations\Tabelposter** i træet. 
6. Klik på **Tilføj rod**. 
7. Indtast eller vælg en værdi i feltet **Tabel**. 

    > [!NOTE]
    > Der tilbydes mere end to programtabeller nu, da denne tilknytning bruger alle de metadata, der er tildelt det tilknyttede program. 

8. Klik på **Annuller**. 
9. Klik på **Valider**. 

    > [!NOTE]
    > Vi har bundet elementer i datamodellen til elementer i de datakilder, der er beskrevet, ved hjælp af oplysninger om metadata for det tilsluttede program, der er tildelt denne tilknytning. 

10. Luk siden. 
11. Luk siden. 

Når du har brug for at evaluere denne modeltilknytning ved hjælp af metadata for et andet versionsprogram, skal du registrere et andet tilknyttet program, tildele det denne modeltilknytning og validere det mod nye metadata.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

