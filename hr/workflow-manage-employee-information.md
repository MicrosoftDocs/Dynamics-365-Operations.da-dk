---
title: Brug af arbejdsprocesser til at administrere medarbejderoplysninger
description: "Dette emne forklarer, hvordan du kan bruge arbejdsprocessen mulighed for personale til at administrere medarbejderoplysninger. For eksempel kan du knytte en arbejdsgang til en stilling og konfigurere et godkendelsesforløb, der startes, når medarbejdere, der ændrer deres post."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Brug af arbejdsprocesser til at administrere medarbejderoplysninger

Dette emne forklarer, hvordan du kan bruge arbejdsprocessen mulighed for personale til at administrere medarbejderoplysninger. For eksempel kan du knytte en arbejdsgang til en stilling og konfigurere et godkendelsesforløb, der startes, når medarbejdere, der ændrer deres post.

Arbejdsprocessen muligheden for menneskelige ressourcer indeholder adskillige arbejdsprocesser til administration af personale-aktiviteter. Desuden er talrige indstillinger tilgængelige, så du kan ændre bestemte arbejdsgange og knytte dem til et rapporteringshierarki. Arbejdsprocesser er tilgængelige til at styre ændringer til standard typer medarbejderoplysninger. Du kan knytte en arbejdsgang til en stilling. Derefter, hvis medarbejdere ændrer deres medarbejderpost, starter en arbejdsproces, der kræver godkendelse, før de nye oplysninger gemmes. Arbejdsprocesser er foruddefineret for følgende typer oplysninger for at hjælpe dig med effektivt at administrere ændringer og holde dine medarbejderes data nøjagtige:

-   Identifikationsnumre
-   Kurser
-   Uddannelser
-   Billede
-   Udlånte emner
-   Erhvervserfaring
-   Projekterfaring
-   Færdigheder
-   Tillidsposter
-   Personale handlinger
-   Kursustilmelding

Når medarbejdere ansat, overført eller afsluttet, kan arbejdsgangen omfatter en revisionsproces. På denne måde kan ændres i et dokument eller vilkårene for en handling, der kan defineres som en del af arbejdsprocessen. Når evalueringsprocessen er fuldført, det dokument eller den handling er fuldført, og arbejdsprocessen skal flyttes til et trin til endelig godkendelse.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Knytte en arbejdsgang til en placering hierarkiet
Du kan knytte en arbejdsgang til et hvert hierarki, du konfigurerer. Hvis en stilling er tilknyttet matrix rapporteringshierarki, kan du konfigurere en arbejdsproces, der dirigerer udgifter for et bestemt projekt til projektleder i stedet for lederen af den medarbejder, der er tilknyttet stillingen. Til at oprette en ny arbejdsproces eller ændre en eksisterende arbejdsproces, på den **personale arbejdsprocessen** skal du klikke på **ny**. Vælg en arbejdsproces på listen for at starte en arbejdsproces. Du kan bruge designer til at oprette en ny arbejdsproces eller ændre trinnene i en eksisterende arbejdsgang. Når du ændrer en eksisterende arbejdsgang, gemmes ændringerne som en ny version. Derfor, du kan altid gå tilbage til en tidligere version, hvis du skulle.

## <a name="configure-a-human-resources-workflow"></a>Konfigurere en arbejdsgang for personale
Følg disse trin for at konfigurere en grundlæggende arbejdsproces, der startes, når medarbejdere anmode om ændringer i deres personlige id.

1.  På den **arbejdsgange for personale** skal du klikke på **ny**.
2.  Vælg på listen over tilgængelige arbejdsprocesser, **id-numre**.
3.  Klik på **køre** til at starte en arbejdsproces og derefter indtaste dit brugernavn og din adgangskode, når du bliver bedt om.
4.  Træk den **godkende identifikationsnummer** element på listen over elementer i arbejdsgang til designer lærred.
5.  Tilslut godkendelseselement til **Start** og **er færdig med**.
6.  Dobbeltklik på **Godkend element**, og derefter højreklikke og vælge **egenskaber**.
7.  Følg disse trin for at tilføje arbejdsinstruktioner for varen:
    1.  Vælg **tildeling**, og vælg derefter **hierarki** under Tildelingstypen.
    2.  Under den **hierarki** markering, vælge **konfigurerbare hierarki**.
    3.  Tilføj en stopbetingelse, og lukke siden.

8.  Udfyld eventuelle yderligere anvisninger (ingen yderligere advarsler bør findes).
9.  Klik på **Gem og luk**. Aktivere den nye arbejdsproces, når dialogboksen åbnes, og vælg **aktivere**.
10. Gå til **personale**&gt;**stillinger**&gt;**placere stillingshierarkityper**.
11. Vælg **Matrix**.
12. Tilføj den **arbejder-id-nummer** arbejdsproces på listen.



