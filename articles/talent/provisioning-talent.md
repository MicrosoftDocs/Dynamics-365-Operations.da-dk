---
title: "Klargøre Microsoft Dynamics 365 for Talent"
description: "Dette emne fører dig gennem processen med at klargøre et nyt miljø til Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a53c1997f74ebe572b17cc3090d2e236b6fe78f6
ms.openlocfilehash: 8a84cfe9b73f0c72f3cb0c3843749754c6b3d538
ms.contentlocale: da-dk
ms.lasthandoff: 01/31/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Klargøre Microsoft Dynamics 365 for Talent
Dette emne fører dig gennem processen med at klargøre et nyt miljø til Microsoft Dynamics 365 for Talent. Det antages i emnet, at du har købt Talent via en Cloud Solution Provider (CSP) eller EA-aftale (Enterprise Architecture). Hvis du har en eksisterende Microsoft Dynamics 365-licens, der allerede indeholder Talent-serviceplanen, og du ikke kan udføre trinnene i dette emne, kan du kontakte Support.

For at komme i gang skal den globale administrator logge på [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) og oprette et nyt Talent-projekt. Medmindre et problem med licensering forhindrer klargøring af Talent, skulle der ikke være brug for hjælp fra Support- eller DSE-medarbejdere (Dynamics Service Engineering).

## <a name="create-an-lcs-project"></a>Oprette et LCS-projekt
Når du vil bruge LCS til at administrere dine Talent-miljøer, skal du først oprette et LCS-projekt.

1. Log på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjælp af den konto, som du brugte til dit abonnement på Talent.
2. Markér plustegnet (**+**) for at oprette et projekt.
3. Vælg **Microsoft Dynamics 365 for Talent** som produktnavn og -version.
4. Vælg **Dynamics 365 for Talent**-metoden.
5. Vælg **Opret**.

Du kan finde oplysninger om, hvordan du kommer i gang med Talent, i den **Talent**-metode, du oprettede i det nye projekt. Når du er færdig med at oprette projektet, skal du udføre følgende procedure for at klargøre Talent-miljøet.

## <a name="provision-a-talent-project"></a>Klargøre et Talent-projekt
Når du har oprettet et LCS-projekt, kan du klargøre Talent i et miljø.

1. I LCS-projektet skal du vælge feltet **Administration af Talent-app**.
2. Talent klargøres altid i et Microsoft PowerApps-miljø for at aktivere PowerApps-integration og -udvidelse. Hvis du ikke allerede har et PowerApps-miljø, skal du følge trinnene i afsnittet "Oprette et nyt PowerApps-miljø (hvis nødvendigt)" i dette emne, før du fortsætter.

    > [!NOTE]
    > For at få vist eksisterende miljøer eller oprette nye miljøer skal den lejeradministrator, der klargør Talent, være tildelt til PowerApps P2-licensen. Hvis organisationen ikke har en PowerApps P2-licens, kan du få en fra din Cloud Solution Provider eller fra [PowerApps-prissætningssiden](https://powerapps.microsoft.com/en-us/pricing/).

3. Vælg **Tilføj**, og vælg derefter det miljø, Talent skal klargøres i.
4. Vælg **Ja** for at acceptere vilkårene og begynde installationen.

    Det nye miljø vises på listen over miljøer i navigationsruden til venstre. Men du kan ikke begynde at bruge miljøet, før installationsstatus er opdateret til **Installeret**. Dette tager normalt kun et par minutter. Hvis klargøringen mislykkes, skal du kontakte Support.

6. Vælg **Log på Talent** for at bruge det nye miljø.

> [!NOTE]
> Hvis du endnu ikke har godkendt de endelige krav, kan du installere en testforekomst af Talent i projektet. Du kan derefter bruge denne forekomst til at teste din løsning, indtil du kan godkende den. Hvis du bruger det nye miljø til test, skal du gentage denne procedure for at oprette et produktionsmiljø.

## <a name="create-a-new-powerapps-environment-if-required"></a>Oprette et nyt PowerApps-miljø (hvis nødvendigt)

Visionen bag Talent's integration med PowerApps-miljøer er at aktivere dataintegration og udvidelsesprocesser ved brug af værktøjer til PowerApps oven på Talent-data. Det er derfor vigtigt at forstå formålet med PowerApps-miljøer, når du vælger miljøet, der skal bruges til Talent. Yderligere oplysninger om PowerApps-miljøer, herunder omfanget af miljøet, adgang til miljøet, og oprettelse og valg af et miljø, finder du i [Annoncering af PowerApps-miljøer](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/).  Selv om hver lejer automatisk klargøres i et miljø med standard PowerApps, er det muligvis ikke det bedste miljø at bruge til Talent-installationen. Dataintegration og teststrategier skal overvejes i dette trin, så det anbefales, at du overvejer de forskellige konsekvenser for installationen, da det ikke er nemt at ændre senere.

1. Vælg **Administrer miljøer** i LCS. Du føres til [PowerApps Administration](https://preview.admin.powerapps.com/environments), hvor du kan se eksisterende miljøer og oprette nye miljøer.
2. Vælg knappen (**+**) **Nyt miljø**.
3. Angiv et entydigt navn til miljøet, og vælg en placering at installere det på.

    > [!NOTE]
    > Talent er ikke tilgængeligt i alle områder. Derfor skal du kontrollere for tilgængelighed, før du kan vælge en placering til dit miljø.

4. Når du bliver spurgt, om du vil oprette en database, skal du vælge **Opret database** for at oprette CDS-databasen (Common Data Service), der skal være vært for en del af dine Talent-data. Når du opretter en database, kan du også integrere PowerApps-programmer i Talent.
5. Du bliver spurgt, hvilket adgangsniveau du vil bruge til databasen. Det anbefales, at du vælger **Begræns adgang**, da denne indstilling forhindrer, at Talent-brugerne kan få direkte adgang til følsomme data ved hjælp af et PowerApps-program.
6. Den CDS-database, der oprettes, indeholder demo-data. Disse demodata er nyttige, fordi du kan bruge demodatafirmaet til test eller til at oprette opgaveregistreringer eller opgaveguider. Dog tilføjer demodata inaktive medarbejdere og fiktive adresser, blandt andre oplysninger, til produktionsmiljøet. Du kan fjerne demodataene ved at følge disse trin, når du er færdig med at oprette CDS-databasen:

    > [!IMPORTANT]
    > Hvis du tidligere har oprettet en CDS-database og angivet nogle af firmaets produktionsdata i den, skal du være opmærksom på, at disse trin fjerner **alle** data i den valgte database, selv dit firmas produktionsdata.

    1. Log på [PowerApps](https://preview.web.powerapps.com/home), og vælg det miljø, du oprettede i trin 2, på rullelisten i højre side af siden.
    2. Udvid **Common Data Service** i den venstre navigationsrude, og vælg **Enheder**.
    3. I højre side af siden skal du vælge ellipseknappen (**...**) og derefter vælge **Ryd alle data**.
    4. Vælg **Slet data** for at bekræfte, at du vil fjerne dataene. Denne handling fjerner som standard alle demodata, som indgår i CDS-databasen. Den fjerner også alle andre data, der er angivet i den valgte database.
    
Du kan nu bruge det nye miljø.

## <a name="granting-access-to-the-environment"></a>Give adgang til miljøet
Den globale administrator, der oprettede miljøet, skal have adgang som standard, men yderligere programbrugere skal eksplicit tildeles adgang. Dette kan gøres ved [tilføjelse af brugere](../dev-itpro/sysadmin/tasks/create-new-users.md) og [tildele dem de relevante roller](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) i HR-kernemiljøet. Desuden er det også nødvendigt at tilføje disse brugere til PowerApps-miljøet, så de kan få adgang til Attract- og Onboard-programmerne.  Blogindlægget, [Introduktion til PowerApps Administration](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) kan hjælpe dig med at følge disse trin, der beskrives her:

> 1.    Den globale administrator, der installerede Talent-miljøet, skal navigere til [PowerApps Administration](https://preview.admin.powerapps.com/environments).   
> 2.    Vælg de pågældende miljøer.
> 3.    Tilføj de nødvendige brugere til rollen"Miljøopretter" under fanen Sikkerhed.

Bemærk, at dette sidste trin for at føje brugere til PowerApps-miljøet er midlertidigt. Vi tilføjer senere funktionalitet for at aktivere dette automatisk, når brugeren tilføjes i kerne HR.


