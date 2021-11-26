---
title: Bruge arbejdsprocesser til at administrere medarbejderoplysninger
description: I dette emne forklares, hvordan du kan bruge arbejdsgange til at administrere medarbejderoplysninger.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 18863ad12cc3b5ee328184da5ffb35e7f5958b52
ms.sourcegitcommit: 7e0e2a266d9a9473df72e207554d9bd150e17ce3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2021
ms.locfileid: "7771478"
---
# <a name="use-workflows-to-manage-employee-information"></a>Bruge arbejdsprocesser til at administrere medarbejderoplysninger

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne forklares, hvordan du kan bruge arbejdsgangsfunktionen i Personale til at administrere medarbejderoplysninger. Du kan f.eks. knytte en arbejdsgang til en stilling og konfigurere et godkendelsesforløb, der startes, når medarbejderne ændrer deres post.

Arbejdsgangsfunktionen til Human Resources indeholder adskillige arbejdsganger til administration af personaleaktiviteter. Desuden er der adgang til talrige indstillinger, så du kan ændre bestemte arbejdsgange og knytte dem til et rapporteringshierarki. Arbejdsgange er tilgængelige som en hjælp til at styre ændringer af flere standardtyper af medarbejderoplysninger. Du kan knytte en arbejdsgang til en stilling. Hvis medarbejderne derefter ændrer deres medarbejderpost, starter en arbejdsproces, der kræver godkendelse, før de nye oplysninger gemmes. Arbejdsgange er foruddefineret for følgende typer oplysninger for at hjælpe dig med effektivt at administrere ændringer og holde dine medarbejderdata nøjagtige:

-   Identifikationsnumre
-   Kurser
-   Uddannelser
-   Billede
-   Udlånte emner
-   Erhvervserfaring
-   Projekterfaring
-   Færdigheder
-   Tillidsposter
-   Handlinger for Human Resources
-   Kursustilmelding

Når medarbejdere ansættes, overføres eller fratræder, kan arbejdsgangen omfatter en revisionsproces. På denne måde kan et dokument blive evalueret, eller vilkårene for en handling kan defineres som en del af arbejdsgangen. Når evalueringsprocessen er fuldført, fuldføres dokumentet eller handlingen, og arbejdsgangen flyttes til et trin til endelig godkendelse.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Knyt en arbejdsgang til et stillingshierarki
Du kan knytte en arbejdsgang til ethvert hierarki, du konfigurerer. Hvis en stilling er tilknyttet et matrixrapporteringshierarki, kan du konfigurere en arbejdsgang, der dirigerer udgifter for et bestemt projekt til projektleder i stedet for til lederen af den medarbejder, der er tilknyttet den pågældende stilling. Vælg **Ny** på siden **Arbejdsgange for Human Resources** for at oprette en ny arbejdsgang eller ændre en eksisterende arbejdsgang. Vælg en arbejdsgang på listen for at starte arbejdsgangsdesigneren. Du kan bruge designeren til at oprette en ny arbejdsgang eller til at ændre trinnene i en eksisterende arbejdsgang. Når du ændrer en eksisterende arbejdsgang, gemmes ændringerne som en ny version. Derfor, du kan altid gå tilbage til en tidligere version, hvis det er nødvendigt.

## <a name="configure-a-human-resources-workflow"></a>Konfigurer en arbejdsgang for Human Resources
Følg disse trin for at konfigurere en grundlæggende arbejdsgang, der startes, når medarbejdere anmoder om ændringer i deres personlige id.

1.  På siden **Arbejdsgange for Human Resources** skal du klikke på **ny**.
2.  På listen over tilgængelige arbejdsgange skal du vælge **Identifikationsnumre**.
3.  Vælg **Kør** for at starte arbejdsgangsdesigneren, og indtast derefter dit brugernavn og din adgangskode, når du bliver bedt om det.
4.  Træk elementet **Godkend identifikationsnummer** fra listen over arbejdsgangselementer til designerlærredet.
5.  Tilslut godkendelseselementet til **Start** og **Afslut**.
6.  Dobbeltklik på (eller dobbeltklik) **Godkend element**, vælg og hold nede (eller højreklik), og vælg derefter **Egenskaber**.
7.  Følg disse trin for at tilføje arbejdsgangsinstruktioner:

    1.  Vælg **Tildeling**, og vælg derefter **Hierarki** under tildelingstypen.
    2.  Under valget **Hierarki** skal du vælge **Konfigurerbart hierarki**.
    3.  Tilføj en stopbetingelse, og luk siden.

8.  Fuldfør eventuelle yderligere instruktioner (der må ikke findes yderligere advarsler).
9.  Vælg **Gem og luk**. Aktivér den nye arbejdsproces, når dialogboksen åbnes, og vælg **Gør den aktiv**.
10. Gå til **Human Resources** &gt; **Stillinger** &gt; **Stillingshierarkityper**.
11. Vælg **Matrix**.
12. Tilføj arbejdsgangen **Identifikationsnummer på arbejder** til listen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Få vist og administrer adresseændringer](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]
