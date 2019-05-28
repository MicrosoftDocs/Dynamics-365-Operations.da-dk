---
title: Mobilapp til projekttimesedler
description: Dette emne indeholder oplysninger om mobilappen Microsoft Dynamics 365 Project Timesheet. Mobilappen Projekttimesedler gør det muligt for brugerne at indlevere og godkende timesedler for projekter på deres mobilenheder.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a475085001b8fa10814c864ef35129eb6ebfdfef
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529873"
---
# <a name="microsoft-dynamics-365-project-timesheet-mobile-application"></a>Mobilappen Microsoft Dynamics 365 Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Overblik

Mobilappen Microsoft Dynamics 365 Project Timesheet gør det muligt for brugerne at indlevere og godkende timesedler for projekter på deres mobilenheder (iPhone eller Android). Denne mobilapp berører timeseddelfunktionaliteten, som er indeholdt i området Projektstyring og regnskab i Microsoft Dynamics 365 for Finance and Operations og forbedrer brugernes produktivitet og effektivitet samt muliggør tidsregistrering og godkendelse af projekttimesedler.

## <a name="download-and-install-the-mobile-app"></a>Downloade og installere mobilappen

Download og installer mobilappen Microsoft Dynamics 365 Project Timesheet til Android eller iPhone fra din enheds mobilbutikken.

## <a name="enable-the-app"></a>Aktiver appen 

Mobilappen Projekttimesedler skal være aktiveret i Dynamics 365 for Finance and Operations. For at aktivere funktionen skal du gå til **Projektstyrings- og regnskabsparametrene \> Timeseddel** og vælge parametret **Aktiver Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Log på appen

1.  Start appen på din mobilenhed.

2.  Angiv URL-adressen for din Microsoft Dynamics 365 for Finance and Operations.

3.  Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode. Angiv dine legitimationsoplysninger.

4.  Du bliver logget ind på din standardvirksomhed.

## <a name="submit-a-project-timesheet"></a>Indsend en projekttimeseddel

Du kan oprette og indsende en projekttimeseddel i appen. Du kan basere en ny timeseddel på oplysninger fra en tidligere timeseddel, gemte linjer eller projekttildelinger. Hvis du er udpeget som stedfortræder, kan du også indtaste en timeseddel for en anden medarbejder. For at oprette en ny delegeret timeseddel skal du vælge **Menu**-knappen og dernæst vælge et ressourcenavn.

Timeseddelsiden opretter en ny timeseddel for timesedlens periode baseret på dags dato. Arbejdsugen vises. Hvis perioden for timesedlen strækker sig over flere uger, kan du vælge en anden arbejdsuge fra fanerne med arbejdsuger.
Hvis der allerede forefindes en timeseddel for dags dato, vises denne. Hvis du har brug for at oprette en ny timeseddel i en anden periode, skal du vælge **Menu**-knappen og dernæst vælge **Ny timeseddel**.

Du kan tilgå projektoplysninger ved at klikke på handlingen **Tilføj tid** eller handlingen **Kopiere tid fra**. Handlingen **Kopier tid fra** kopierer projektlinjeoplysninger, men ikke timerne. Menuen **Kopier tid fra** indeholder følgende indstillinger:

- **Kopier fra eksisterende timeseddel** – Kopier timeseddellinjer fra en eksisterende timeseddel.

- **Kopier fra foretrukne** – Opret nye timeseddellinjer ved hjælp af dine foretrukne timeseddelindstillinger.

- **Kopier fra tildeling** – Opret nye timeseddellinjer ud fra tildelte projekter.

De viste projektoplysninger er afhængige af de mobilparametre, som du definerede på siden **Projektstyrings- og regnskabsparametre**.

I feltet **Juridiske enhed** skal du vælge den juridiske enhed, som du udførte projektarbejde for. Feltet **Juridisk enhed** er kun tilgængeligt, hvis understøttelsen af interne timesedler er aktiveret for din juridiske enhed.

Vælg den kunde, der er knyttet til timeseddelprojektet. I den indledende udgivelse til Android er indtastninger i henhold til kunde ikke understøttet, da du først skal vælge projektet. Hvis du markerede projektet først, udfyldes feltet **Kunde** automatisk.

I feltet **Projekt** skal du vælge det projekt, som du indtaster tid for. Feltet **Kunde** udfyldes automatisk.

Opslag i kunde og projekt gør det muligt at søge blandt både kunder og projekter.

Vælg oplysninger i felterne **Kategori**, **Aktivitet**, **Linjeegenskab**, **Salgsmomsgruppe** og **Varesalgsmomsgruppe** efter behov. Disse felter kan overskrives.

Feltet **Linjeegenskaber** sættes til en standardværdi baseret på parametrene for projektstyring og regnskab. Når parametrene for projekt/kategori og kategori/ressource er aktive, bliver værdien **Linjeegenskab** sat til den standardværdi, du har defineret for denne validering. Når parametrene for projekt/kategori og kategori/ressource ikke er aktive, bliver værdien **Linjeegenskaber** nulstillet i henhold til feltet **Aktiver standardlinjeegenskaber** på siden **Projektstyrings- og regnskabsparametre**. Værdien **Linjeegenskaber** kan overskrives.

Vælg en dag for at tilføje tid. Angiv det antal timer, som du arbejdede hver dag.

Hvis du vil tilføje bemærkninger om de registrerede timer, skal du klikke på **Tilføj bemærkninger** og derefter skrive bemærkningerne til en intern målgruppe, en kunde eller begge.
Interne bemærkninger kan ses af projektledere. Kundernes bemærkninger fremgår af fakturaerne.

Hvis du vil gemme linjen som en foretrukken linje, skal du markere afkrydsningsfeltet og derefter klikke på **Gem som foretrukken**.

Den økonomiske dimension og vedhæftelse af filer understøttes ikke i mobilappen.

Fortsæt med at tilføje projektlinjer efter behov for at færdiggøre din timeseddel.

Klik på **Indsend** for at indsende timesedlen til godkendelsesarbejdsgangen.

## <a name="review-timesheets"></a>Gennemgå timesedler

Listen med timesedler, der skal gennemgås, er tilgængelig i menuen. Denne indstilling er kun tilgængelig, hvis du er angivet som arbejdsgangsgodkender. Både overskrift og linjegodkendelse understøttes. Godkendelse på linjeniveau tilbyder muligheden for at markere en eller flere linjer til godkendelse. Når du har gennemgået oplysningerne på timesedlen, skal du klikke **Godkend**, **Deleger** eller **Returner** for at forsætte arbejdsgangen.
