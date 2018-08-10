---
title: "Konfigurere forudsætninger for administration"
description: Brug denne procedure til at aktivere processer for styring af uoverensstemmelser.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4bb4af7cb7aff101a8b9e6162823515f63b12886
ms.openlocfilehash: 9b5b05a3c00f093066a2714964bb99146427c3bc
ms.contentlocale: da-dk
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-prerequisites-for-management"></a>Konfigurere forudsætninger for administration

[!include [task guide banner](../../includes/task-guide-banner.md)]

Brug denne procedure til at aktivere processer for styring af uoverensstemmelser. En uoverensstemmelse er en procedure eller vare, der har et kvalitetsproblem, hvor de beskrivende oplysninger omfatter årsagen til og typen af problemet. Proceduren bruger USMF-demodatafirmaet. Denne procedure udføres typisk af en kvalitetschef.


## <a name="enable-quality-management-processes-within-the-company"></a>Aktivere kvalitetsstyringsprocesser i virksomheden
1. Gå til lagerstyring > Opsætning > Parametre til lager- og lagerstedsstyring.
2. Klik på fanen Kvalitetsstyring.
3. Vælg Ja i feltet Brug kvalitetsstyring.
    * Vælg denne parameter for at aktivere kvalitetsstyringsprocesser for virksomheden.  
4. Angiv et tal i feltet Timepris.
    * Brug feltet Timepris til at angive en timepris for arbejdet i den lokale valuta. Timeprisen bruges til beregning af omkostningerne for operationer, der vedrører en uoverensstemmelse. Timeprisen og de beregnede omkostninger er referenceoplysninger for en uoverensstemmelse, og de påvirker ikke andre funktioner.  
5. Klik på Rapportopsætning.
    * På denne siden kan du definere notetyper for kvalitetsrapporter, der skal bruges til forskellige typer rapporter over kvalitetsstyring.  
6. Luk siden.
7. Luk siden.

## <a name="enable-user-for-nonconformance-processing"></a>Aktivere bruger til håndtering af uoverensstemmelser
1. Gå til Systemadministration > Brugere > Brugere.
    * For at behandle godkendelsen af en uoverensstemmelse skal den bruger, der godkender eller afviser uoverensstemmelser, have en "Navn"-værdi tildelt på siden Brugere. For at kunne bruge dokumentnoter skal brugeren også have Dokumenthåndtering aktiveret i brugerindstillingerne.  
2. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på feltet Navn med værdien 'Ricardo'.
    * Du kan bruge filteret til at finde den bruger, der skal godkende eller afvise uoverensstemmelsesposter.  
3. Klik op linket i den valgte række på listen.
    * For at behandle godkendelsen af en uoverensstemmelse skal du sørge for, at den bruger, der godkender eller afviser uoverensstemmelser, har en "Navn"-værdi tildelt på siden Brugere.  
4. Klik på Brugerindstillinger.
5. Klik på fanen Præferencer.
6. Vælg Ja i feltet Aktivér dokumenthåndtering.
    * For at kunne bruge dokumentnoter skal brugeren også have Dokumenthåndtering aktiveret i brugerindstillingerne.  
7. Luk siden.
8. Luk siden.
9. Luk siden.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Definere diagnosticeringstyper for håndtering af uoverensstemmelser
1. Gå til Lagerstyring > Konfiguration > Kvalitetsstyring > Diagnosticeringstyper.
    * Brug siden Diagnosticeringstyper til definere en klassifikation af diagnosticeringshandlinger. En rettelse angiver, hvilken type diagnosticeringshandling, der skal udføres for en godkendt uoverensstemmelse, hvem der skal udføre den og den ønskede og planlagte fuldførelsesdato.  
2. Klik på Ny.
3. Skriv en værdi i feltet Diagnosticering.
4. Skriv en værdi i feltet Beskrivelse.
5. Luk siden.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Definere kvalitetsgebyrer for håndtering af uoverensstemmelser
1. Gå til Lagerstyring > Konfiguration > Kvalitetsstyring > Kvalitetsgebyrer.
    * Brug siden Kvalitetsgebyrer til at definere en klassifikation af gebyrer, der skal bruges i handlinger, der vedrører uoverensstemmelser.  
2. Klik på Ny.
3. Skriv en værdi i feltet Gebyrkode.
4. Skriv en værdi i feltet Beskrivelse.
5. Luk siden.

## <a name="define-the-operations-for-nonconformance-processing"></a>Definere handlinger for håndtering af uoverensstemmelser
1. Gå til Lagerstyring > Konfiguration > Kvalitetsstyring > Handlinger.
    * Brug siden Handlinger til at definere en klassifikation af det arbejde, der kan blive udført for en godkendt uoverensstemmelse. Når du relaterer en handling til en uoverensstemmelse, kan du også definere detaljerede oplysninger om det tilknyttede materiale, arbejdstimer og tillæg, der kræves for at udføre handlingen. Disse oplysninger danner grundlaget for beregning af en forkalkuleret omkostning for udførelsen af handlingen.  
2. Klik på Ny.
3. Skriv en værdi i feltet Handling.
4. Skriv en værdi i feltet Beskrivelse.
5. Luk siden.

## <a name="define-problem-types-for-nonconformance-processing"></a>Definere problemtyper for håndtering af uoverensstemmelser
1. Gå til Lagerstyring > Konfiguration > Kvalitetsstyring > Problemtyper.
    * Brug siden Problemtyper til at definere en klassifikation for de kvalitetsproblemer, der kan forekomme for de forskellige uoverensstemmelsestyper. Uoverensstemmelsestyperne omfatter Intern, Debitor, Kreditor, Serviceanmodning, Produktion og Produktion af samprodukter. En enkelt problemtype kan tilknyttes flere uoverensstemmelsestyper.  
2. Klik på Ny.
3. Skriv en værdi i feltet Problem.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Uoverensstemmelsestyper.
    * Brug siden Uoverensstemmelsestyper til at autorisere brugen af en problemtype til en eller flere uoverensstemmelsestyper. En problemtype vedrørende en defektkode kunne f.eks. gælde for alle uoverensstemmelsestyper, mens en problemtype for kundeklager måske kun gælder for uoverensstemmelsestyperne Debitor eller Serviceanmodning.  
6. Klik på Ny.
7. Markér den valgte række på listen.
8. Vælg en indstilling i feltet Uoverensstemmelse.
9. Luk siden.
10. Luk siden.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Definere karantænezoner for håndtering af uoverensstemmelser
1. Gå til Lagerstyring > Konfiguration > Kvalitetsstyring > Karantænezoner.
2. Klik på Ny.
3. Skriv en værdi i feltet Karantænezone.
4. Skriv en værdi i feltet Beskrivelse.
5. Luk siden.

