---
title: Administrere ER-modeltilknytning i separate ER-konfigurationer
description: Følgende trin forklarer, hvordan en bruger, der er tildelt rollen som Systemadministrator eller Udvikler til elektronisk rapportering, kan administrere ER-modeltilknytninger i separate ER-konfigurationer.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e59e9f2dd5a0fa6d5955e3d93d25759a478ede7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684421"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a>Administrere ER-modeltilknytning i separate ER-konfigurationer

[!include [banner](../../includes/banner.md)]

Følgende trin forklarer, hvordan en bruger, der er tildelt rollen som Systemadministrator eller Udvikler til elektronisk rapportering, kan administrere ER-modeltilknytninger i separate ER-konfigurationer. I denne opgaveguide skal du oprette de nødvendige ER konfigurationer for eksempelfirmaet Litware, Inc. For at fuldføre denne opgaveguide skal du først fuldføre trinnene i opgaveguiden "ER Oprette en konfigurationsudbyder" og markere den som aktiv. 

Da ER-konfigurationer deles af firmaer, kan du fuldføre denne opgaveguide ved hjælp af et virksomhedsdatasæt efter eget valg. Funktionerne i denne opgaveguide er tilgængelig, hvis du har installeret et af følgende hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 til versionen Dynamics AX 7.0 eller https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 til versionen Dynamics 365 for Operations.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Kontrollér, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du først fuldføre trinnene i opgaveguiden Opret en konfigurationsudbyder, og markér den som aktiv.   

## <a name="add-a-new-er-model-configuration"></a>Tilføj en ny ER-modelkonfiguration
1. Klik på Rapporteringskonfigurationer.
    * Tilføj en ny modelkonfiguration. Navnet skal være entydigt i konfigurationstræet.  
2. Klik på Opret konfiguration for at åbne dialogboksen.
3. Skriv 'Eksempeldatamodel' i feltet Navn.
    * Eksempeldatamodel  
4. Klik på Opret konfiguration.
5. Klik på Designer.
6. Klik på Ny for at åbne dialogboksen Fjern.
7. Skriv 'Root' i feltet Navn.
    * Rod  
8. Klik på Tilføj.
9. Klik på Ny for at åbne dialogboksen Fjern.
10. Skriv "Firma" feltet Navn.
    * Regnskab  
11. Klik på Tilføj.
12. I feltet Beskrivelse skal du angive teksten, beskrivelsen af den juridiske enhed eller det firma, hvor en bruger er logget på på kørselstidspunktet. 
    * Beskrivelse af den juridiske enhed eller det firma, som en bruger loggede på på kørselstidspunktet.  
13. Klik på Rodreference.
14. Klik på OK.
15. Klik på Gem.
16. Luk siden.
17. Klik på Skift status.
18. Klik på Fuldført.
19. Klik på OK.

## <a name="add-a-new-er-model-mapping-configuration"></a>Tilføje en ny ER-modeltilknytningskonfiguration
1. Klik på Opret konfiguration for at åbne dialogboksen.
2. Skriv 'Modeltilknytning baseret på datamodel af typen Eksempeldatamodel' i feltet Ny.
3. Skriv 'Eksempeltilknytning' i feltet Navn.
    * Eksempeltilknytning  
4. Klik på Opret konfiguration.
5. Udvid eller skjul sektionen Forudsætninger.
    * Forudsætningsgruppen Implementeringer er tilføjet automatisk. Gruppen indeholder den påkrævede komponent, der refererer til den overordnede datamodelkonfiguration og er markeret som Implementering. Det betyder, at denne tilknytningskonfiguration for eksempeltilknytningsmodellen betragtes som implementeringen af datamodellen Eksempeldatamodel. Denne komponent tvinger derfor ER til at hente modeltilknytningskonfigurationen Eksempeltilknytning fra et ER-lager, når modelkonfigurationen Eksempeldatamodel hentes.   
6. Klik på Designer.
    * Den oprettede modeltilknytningskonfiguration indeholder en ny tom tilknytning med samme navn som den oprettede konfiguration. Når en valgt overordnet models konfiguration indeholder modeltilknytninger, kopieres de til en ny modeltilknytningskonfiguration.   
7. Klik på Designer.
8. Vælg 'Dynamics 365 for Operations\Tabel' i træet.
9. Klik på Tilføj rod.
10. Skriv "Firma" feltet Navn.
    * Regnskab  
11. Skriv "CompanyInfo" i feltet Tabel.
    * CompanyInfo  
12. Klik på OK.
13. Udvid 'Firma' i træet.
14. Udvid 'Firma\find()' i træet.
15. Vælg 'Firma\find()\Navn' i træet.
16. Klik på Bind.
17. Klik på Gem.
18. Luk siden.
19. Luk siden.
20. Klik på Konfigurationer i handlingsruden.
21. Klik på Brugerparametre.
22. Vælg Ja i feltet Indstillinger for kørsel.
23. Klik på OK.
24. Klik på Rediger.
25. Vælg Ja i feltet Udkast til kørsel.

## <a name="add-a-new-er-format-configuration"></a>Tilføje en ny ER-formatkonfiguration
1. Vælg 'Eksempeldatamodel' i træet.
2. Klik på Opret konfiguration for at åbne dialogboksen.
3. Skriv 'Format baseret på datamodel af typen Eksempeldatamodel' i feltet Ny.
4. Skriv 'Eksempelformat' i feltet Navn.
    * Eksempelformat  
5. Klik på Opret konfiguration.
6. Klik på Designer.
7. Klik på Tilføj rod for at åbne dialogboksen.
8. Vælg "Tekst\Streng" i træet.
9. Klik på OK.
10. Klik på fanen Tilknytning.
11. Udvid 'model' i træet.
12. Vælg 'model\Firma' i træet.
13. Klik på Bind.
14. Klik på Gem.
15. Luk siden.
    * Kør kladdeversionen af det oprettede format med henblik på test.  
16. Klik på Kør.
    * Klik på Kør i oversigtspanelet Versioner.  
17. Klik på OK.
    * Gennemse det output, der indeholder navnet på det firma, som den bruger, der kører denne formatkonfiguration, er logget på. Den oprettede modeltilknytningskonfiguration bruges af denne formatkonfiguration, fordi der kun er én tilgængelig konfiguration, der indeholder de nødvendige modeltilknytninger.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Tilføje en alternativ ER-modeltilknytningskonfiguration
1. Vælg 'Eksempeldatamodel' i træet.
2. Klik på Opret konfiguration for at åbne dialogboksen.
3. Skriv 'Modeltilknytning baseret på datamodel af typen Eksempeldatamodel' i feltet Ny.
4. Skriv 'Eksempeltilknytning (alternativ)' i feltet Navn.
    * Eksempeltilknytning (alternativ)  
5. Klik på Opret konfiguration.
6. Klik på Designer.
7. Klik på Designer.
8. Vælg 'Dynamics 365 for Operations\Tabel' i træet.
9. Klik på Tilføj rod.
10. Skriv "Firma" feltet Navn.
    * Regnskab  
11. Skriv "CompanyInfo" i feltet Tabel.
    * CompanyInfo  
12. Klik på OK.
13. Klik på Rediger.
14. Vælg '"Streng\SAMMENKÆD" i træet.
15. Klik på Tilføj funktion.
16. Udvid 'Firma' i træet.
17. Udvid 'Firma\find()' i træet.
18. Vælg 'Firma\find()\Navn' i træet.
19. Klik på Tilføj datakilde.
20. Skriv en værdi i feltet Formel.
    * CONCATENATE(Firma.'find()'.Navn, ";",  
21. Vælg 'Firma\find()\Firma(DataArea)' i træet.
22. Klik på Tilføj datakilde.
23. Skriv en værdi i feltet Formel.
    * CONCATENATE(Firma.'find()'. Navn, ";", Firma.'find()'.DataArea)  
24. Klik på Gem.
25. Luk siden.
26. Klik på Gem.
27. Luk siden.
28. Luk siden.
29. Vælg Ja i feltet Udkast til kørsel.

## <a name="use-an-existing-er-model-mapping-configuration"></a>Bruge en eksisterende ER-modeltilknytningskonfiguration
1. Vælg i træet 'Eksempeldatamodel\Eksempelformat'.
2. Klik på Kør.
    * Den valgte kladdeversion af ER-formatkonfigurationen ikke kan udføres, fordi der findes mere end én konfiguration af modeltilknytningen til den udefinerede datamodel, der er valgt som datakilde for det ER-format, der køres.   
    * Som det næste skal du definere den alternative modeltilknytningskonfiguration som den, hvorfra modeltilknytninger bliver brugt som datakilder ved kørsel af ER-format.   
3. Vælg i træet 'Eksempeldatamodel\Eksempeltilknytning (alternativ)'.
4. Vælg Ja i feltet Standard for modeltilknytning.
5. Vælg i træet 'Eksempeldatamodel\Eksempelformat'.
6. Klik på Kør.
7. Klik på OK.
    * Standardkonfigurationen for modeltilknytningen bruges af denne formatkonfiguration til oprettelse af det elektroniske dokument (det oprettede output indeholder firmakoden).  

