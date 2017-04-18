---
title: Administration af uoverensstemmelse
description: "I denne artikel beskrives den grundlæggende konfiguration, der kræves for at kunne bruge uoverensstemmelser. Der kræves yderligere konfigurationer, hvis du vil bruge kvalitetsordrer."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 6f25e2930ff265df1f938cdf56e8a0f4993617af
ms.lasthandoff: 03/31/2017


---

# <a name="nonconformance-management"></a>Administration af uoverensstemmelse

I denne artikel beskrives den grundlæggende konfiguration, der kræves for at kunne bruge uoverensstemmelser. Der kræves yderligere konfigurationer, hvis du vil bruge kvalitetsordrer. 

Følg disse trin for at aktivere uoverensstemmelsesstyring:

1.  Angiv de parametre for lager- og lagerstedsstyring, der vedrører uoverensstemmelser:
    -   Angiv indstillingen **Brug kvalitetsstyring** til **Ja**.
    -   Brug feltet **Timepris** til at angive en timepris for arbejde i den lokale valuta. Timeprisen bruges til at beregne omkostningerne for operationer, der vedrører en uoverensstemmelse. Timeprisen og de beregnede omkostninger er referenceoplysninger for en uoverensstemmelse. De agerer ikke sammen med andre funktioner.
    -   Brug af **kvalitetsstyring** under fanen på den **rapportopsætning** siden for at definere typen dokument der skal udskrives. Du kan udskrive en uoverensstemmelsesrapport, et uoverensstemmelsesmærkat og en rettelsesrapport. Du kan definere mere end én post for at udskrive forskellige dokumenttyper i en rapport eller for at udskrive interne og eksterne bemærkninger. Det kan være nyttigt at bruge siden **Dokumenttype** til at definere en entydig dokumenttype for uoverensstemmelser og en entydig dokumenttype for rettelser. Det kan f.eks. være, at du vil skrive noter om en uoverensstemmelse ved hjælp af den entydige dokumenttype for uoverensstemmelser. I dette tilfælde skal du identificere den entydige dokumenttype i rapportindstillingerne.
    -   Aktivér nummerserier for uoverensstemmelse og korrektionsreferencer.

2.  Aktivér brugergodkendelse af uoverensstemmelser. Brug feltet **Navn** på siden **Brugere** til at tildele en medarbejder til hver bruger, der skal godkende en uoverensstemmelse. Systemet bruger de medarbejdere, der ændrer status for en uoverensstemmelse til at registrere historikken for uoverensstemmelsen. Brugere kan ikke godkende en uoverensstemmelse, medmindre de er blevet tildelt et medarbejder-id.
3.  Definer de problemtyper, der vil blive knyttet til uoverensstemmelser. Brug siden **Problemtyper** til at definere en klassifikation af de kvalitetsproblemer, der kan opstå for de forskellige uoverensstemmelsestyper. Du kan konfigurere følgende uoverensstemmelsestyper: **Intern**, **Debitor**, **Kreditor**, **Serviceanmodning**, **Produktion** og **Produktion af samprodukter**. Brug siden **Uoverensstemmelsestyper** til at autorisere en problemtype, der skal bruges i en eller flere uoverensstemmelsestyper. En problemtype, der vedrører en defektkode, kunne f.eks. gælde for alle uoverensstemmelsestyper, mens en problemtype, der er relateret til kundeklager, måske kun gælder for uoverensstemmelsestyperne **Debitor** og **Serviceanmodning**.
4.  Angiv karantænezonerne, der kan bruges som guide til håndtering af defekt materiale. Brug formen **Karantænezoner** til at definere de zoner, der kan tildeles til en uoverensstemmelse. Den udskrevne uoverensstemmelsesmærkat viser den tildelte karantænezone og oplysninger om brug for at vejlede om, hvordan defekt materiale skal håndteres. Zonerne kan svare til lagerlokationer eller operationsressourcer.
5.  Angiv de diagnosticeringstyper, der vil blive tildelt til rettelser. Brug siden **Diagnosticeringstyper** til definere en klassifikation af diagnosticeringshandlinger. En rettelse angiver, hvilken type diagnosticeringshandling der skal udføres for en godkendt uoverensstemmelse, og hvem der skal udføre den pågældende handling. Den angiver også den ønskede slutdato og den planlagte slutdato.
6.  Angiv de relaterede operationer, der vil blive knyttet til uoverensstemmelser. Brug siden **Operationer** til at definere en klassifikation af det arbejde, der kan udføres for en godkendt uoverensstemmelse. Når du knytter en relateret operation til en uoverensstemmelse, kan du angive detaljerede oplysninger, f.eks. oplysninger om det tilknyttede materiale, arbejdstimer og tillæg, der kræves for at udføre operationen. Disse oplysninger bruges til at beregne en forkalkuleret omkostning for operationen. De detaljerede oplysninger og forkalkulerede omkostninger er til reference. De relaterede operationer for kvalitet er ikke de samme som de operationer, der kan angives for en produktionsrute.


<a name="see-also"></a>Se også
--------

[Oprette og behandle en uoverensstemmelse (opgave guide)](https://ax.help.dynamics.com/en/wiki/create-and-process-a-nonconformance/)

[Quality management processes](quality-management-processes.md)

[Konfigurere forudsætninger for uoverensstemmelse management (opgave guide)](https://ax.help.dynamics.com/en/wiki/set-up-prequisites-for-nonconformance-management/)

