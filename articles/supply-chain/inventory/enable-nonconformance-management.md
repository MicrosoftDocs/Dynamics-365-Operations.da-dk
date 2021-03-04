---
title: Administration af uoverensstemmelser
description: I denne artikel beskrives den grundlæggende konfiguration, der kræves for at kunne bruge uoverensstemmelser. Der kræves yderligere konfigurationer, hvis du vil bruge kvalitetsordrer.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e66353dc3a4b4b7d9ff3c5f63bf3d4b0c70bda0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424701"
---
# <a name="nonconformance-management"></a>Administration af uoverensstemmelser

[!include [banner](../includes/banner.md)]

I denne artikel beskrives den grundlæggende konfiguration, der kræves for at kunne bruge uoverensstemmelser. Der kræves yderligere konfigurationer, hvis du vil bruge kvalitetsordrer.

Følg disse trin for at aktivere uoverensstemmelsesstyring:

1.  Angiv de parametre for lager- og lagerstedsstyring, der vedrører uoverensstemmelser:
    -   Angiv indstillingen **Brug kvalitetsstyring** til **Ja**.
    -   Brug feltet **Timepris** til at angive en timepris for arbejde i den lokale valuta. Timeprisen bruges til at beregne omkostningerne for operationer, der vedrører en uoverensstemmelse. Timeprisen og de beregnede omkostninger er referenceoplysninger for en uoverensstemmelse. De agerer ikke sammen med andre funktioner.
    -   Brug fanen **Kvalitetsstyring** på siden **Rapportopsætning** til at definere den dokumenttype, der skal udskrives. Du kan udskrive en uoverensstemmelsesrapport, et uoverensstemmelsesmærkat eller en rettelsesrapport. Du kan definere mere end én post for at udskrive forskellige dokumenttyper i en rapport eller for at udskrive interne og eksterne bemærkninger. Det kan være nyttigt at bruge siden **Dokumenttype** til at definere en entydig dokumenttype for uoverensstemmelser og en entydig dokumenttype for rettelser. Det kan f.eks. være, at du vil skrive noter om en uoverensstemmelse ved hjælp af den entydige dokumenttype for uoverensstemmelser. I dette tilfælde skal du identificere den entydige dokumenttype i rapportindstillingerne.
    -   Aktivér nummerserier for uoverensstemmelse og korrektionsreferencer.

2.  Aktivér brugergodkendelse af uoverensstemmelser. Brug feltet **Navn** på siden **Brugere** til at tildele en medarbejder til hver bruger, der skal godkende en uoverensstemmelse. Systemet bruger de medarbejdere, der ændrer status for en uoverensstemmelse til at registrere historikken for uoverensstemmelsen. Brugere kan ikke godkende en uoverensstemmelse, medmindre de er blevet tildelt et medarbejder-id.
3.  Definer de problemtyper, der vil blive knyttet til uoverensstemmelser. Brug siden **Problemtyper** til at definere en klassifikation af de kvalitetsproblemer, der kan opstå for de forskellige uoverensstemmelsestyper. Du kan konfigurere følgende uoverensstemmelsestyper: **Intern**, **Debitor**, **Kreditor**, **Serviceanmodning**, **Produktion** og **Produktion af samprodukter**. Brug siden **Uoverensstemmelsestyper** til at autorisere en problemtype, der skal bruges i en eller flere uoverensstemmelsestyper. En problemtype, der vedrører en defektkode, kunne f.eks. gælde for alle uoverensstemmelsestyper, mens en problemtype, der er relateret til kundeklager, måske kun gælder for uoverensstemmelsestyperne **Debitor** og **Serviceanmodning**.
4.  Angiv karantænezonerne, der kan bruges som guide til håndtering af defekt materiale. Brug formen **Karantænezoner** til at definere de zoner, der kan tildeles til en uoverensstemmelse. Den udskrevne uoverensstemmelsesmærkat viser den tildelte karantænezone og oplysninger om brug for at vejlede om, hvordan defekt materiale skal håndteres. Zonerne kan svare til lagerlokationer eller operationsressourcer.
5.  Angiv de diagnosticeringstyper, der vil blive tildelt til rettelser. Brug siden **Diagnosticeringstyper** til definere en klassifikation af diagnosticeringshandlinger. En rettelse angiver, hvilken type diagnosticeringshandling der skal udføres for en godkendt uoverensstemmelse, og hvem der skal udføre den pågældende handling. Den angiver også den ønskede slutdato og den planlagte slutdato.
6.  Angiv de relaterede operationer, der vil blive knyttet til uoverensstemmelser. Brug siden **Operationer** til at definere en klassifikation af det arbejde, der kan udføres for en godkendt uoverensstemmelse. Når du knytter en relateret operation til en uoverensstemmelse, kan du angive detaljerede oplysninger, f.eks. oplysninger om det tilknyttede materiale, arbejdstimer og tillæg, der kræves for at udføre operationen. Disse oplysninger bruges til at beregne en forkalkuleret omkostning for operationen. De detaljerede oplysninger og forkalkulerede omkostninger er til reference. De relaterede operationer for kvalitet er ikke de samme som de operationer, der kan angives for en produktionsrute.


<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oprette og behandle en overensstemmelse](tasks/create-process-non-conformance.md)

[Processer for kvalitetsstyring](quality-management-processes.md)

[Konfigurere forudsætninger for uoverensstemmelsesstyring](tasks/set-up-prerequisites-nonconformance-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]