---
title: Konfigurere forudsætninger for uoverensstemmelsesstyring
description: Brug dette emne til at aktivere processer for styring af uoverensstemmelser.
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80a7ae2249179c561d03f7b729ebb942ba856046
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961500"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Konfigurere forudsætninger for uoverensstemmelsesstyring

[!include [banner](../../includes/banner.md)]

Brug dette emne til at aktivere processer for styring af uoverensstemmelser. En uoverensstemmelse er en procedure eller vare, der har et kvalitetsproblem, hvor de beskrivende oplysninger omfatter årsagen til og typen af problemet. Proceduren bruger USMF-demodatafirmaet. Denne procedure udføres typisk af en kvalitetschef.


## <a name="enable-quality-management-processes-within-the-company"></a>Aktivere kvalitetsstyringsprocesser i virksomheden
1. Gå i navigationsruden til **Moduler > Lagerstyring > Opsætning > Parametre til lager- og lokationsstyring**.
2. Vælg fanen **Kvalitetsstyring**.
3. Vælg **Ja** i feltet **Brug kvalitetsstyring** for at aktivere processer for kvalitetsstyring for firmaet.
4. Angiv et tal i den lokale valuta i feltet **Timepris**. Timeprisen bruges til beregning af omkostningerne for operationer, der vedrører en uoverensstemmelse. Timeprisen og de beregnede omkostninger er referenceoplysninger for en uoverensstemmelse, og de påvirker ikke andre funktioner.  
5. Vælg **Rapportopsætning** for at definere notetyper for kvalitetsrapporter, der skal bruges til forskellige typer rapporter over kvalitetsstyring.

## <a name="enable-user-for-nonconformance-processing"></a>Aktivere bruger til håndtering af uoverensstemmelser
1. Gå i navigationsruden til **Moduler > Systemadministration > Brugere > Brugere**. 
2. Du kan bruge Quick Filter til at finde den bruger, der skal godkende eller afvise uoverensstemmelsesposter. For eksempel kan du filtrere på feltet **Navn** med værdien `Ricardo`. For at behandle godkendelsen af en uoverensstemmelse skal den bruger, der godkender eller afviser uoverensstemmelser, have en "Navn"-værdi tildelt på siden **Brugere**. For at kunne bruge dokumentnoter skal brugeren også have Dokumenthåndtering aktiveret i brugerindstillingerne.  
3. Marker rækken for den ønskede post.
4. Vælg **Brugerindstillinger**.
5. Vælg fanen **Præferencer**.
6. Vælg **Ja** i feltet **Aktivér dokumenthåndtering**.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Definere diagnosticeringstyper for håndtering af uoverensstemmelser
1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Kvalitetsstyring > Diagnosticeringstyper**. Brug siden **Diagnosticeringstyper** til definere en klassifikation af diagnosticeringshandlinger. En rettelse angiver, hvilken type diagnosticeringshandling, der skal udføres for en godkendt uoverensstemmelse, hvem der skal udføre den og den ønskede og planlagte fuldførelsesdato.  
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Diagnosticering**.
4. Indtast en værdi i feltet **Beskrivelse**.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Definere kvalitetsgebyrer for håndtering af uoverensstemmelser
1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Kvalitetsstyring > Kvalitetsgebyrer**. Brug siden **Kvalitetsgebyrer** til at definere en klassifikation af gebyrer, der skal bruges i handlinger, der vedrører uoverensstemmelser.  
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Gebyrkode**.
4. Indtast en værdi i feltet **Beskrivelse**.

## <a name="define-the-operations-for-nonconformance-processing"></a>Definere handlinger for håndtering af uoverensstemmelser
1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Kvalitetsstyring > Handlinger**. Brug siden **Handlinger** til at definere en klassifikation af det arbejde, der kan blive udført for en godkendt uoverensstemmelse. Når du relaterer en handling til en uoverensstemmelse, kan du også definere detaljerede oplysninger om det tilknyttede materiale, arbejdstimer og tillæg, der kræves for at udføre handlingen. Disse oplysninger danner grundlaget for beregning af en forkalkuleret omkostning for udførelsen af handlingen.  
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Handling**.
4. Indtast en værdi i feltet **Beskrivelse**.

## <a name="define-problem-types-for-nonconformance-processing"></a>Definere problemtyper for håndtering af uoverensstemmelser
1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Kvalitetsstyring > Problemtyper**. Brug siden **Problemtyper** til at definere en klassifikation for de kvalitetsproblemer, der kan forekomme for de forskellige uoverensstemmelsestyper. Uoverensstemmelsestyperne omfatter **Intern**, **Debitor**, **Kreditor**, **Serviceanmodning**, **Produktion** og **Produktion af samprodukter**. En enkelt problemtype kan tilknyttes flere uoverensstemmelsestyper.  
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Problemtype**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Vælg **Uoverensstemmelsestyper**. Brug siden **Uoverensstemmelsestyper** til at autorisere brugen af en problemtype til en eller flere uoverensstemmelsestyper. En problemtype vedrørende en defektkode kunne f.eks. gælde for alle uoverensstemmelsestyper, mens en problemtype for kundeklager måske kun gælder for uoverensstemmelsestyperne Debitor eller Serviceanmodning.  
6. Vælg **Ny**.
7. Vælg en indstilling i feltet for rækken **Uoverensstemmelsestype**.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Definere karantænezoner for håndtering af uoverensstemmelser
1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Kvalitetsstyring > Karantænezoner**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Karantænezone**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]