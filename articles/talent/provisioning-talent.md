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
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: e4459e8be4bfab8e0789744eacd533286b6c05e0
ms.contentlocale: da-dk
ms.lasthandoff: 03/07/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Klargøre Microsoft Dynamics 365 for Talent

[!include[banner](includes/banner.md)]

Dette emne fører dig gennem processen med at klargøre et nyt produktionsmiljø til Microsoft Dynamics 365 for Talent. Det antages i emnet, at du har købt Talent via en Cloud Solution Provider (CSP) eller EA-aftale (Enterprise Architecture). Hvis du har en eksisterende Microsoft Dynamics 365-licens, der allerede indeholder Talent-serviceplanen, og du ikke kan udføre trinnene i dette emne, kan du kontakte Support.

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

    Det nye miljø vises på listen over miljøer i navigationsruden til venstre. Men du kan ikke begynde at bruge miljøet, før installationsstatus er opdateret til **Installeret**. Dette tager normalt kun et par minutter. Hvis klargøringsprocessen mislykkes, skal du kontakte Support.

6. Vælg **Log på Talent** for at bruge det nye miljø.

> [!NOTE]
> Hvis du endnu ikke har godkendt de endelige krav, kan du installere en testforekomst af Talent i projektet. Du kan derefter bruge denne forekomst til at teste din løsning, indtil du kan godkende den. Hvis du bruger det nye miljø til test, skal du gentage denne procedure for at oprette et produktionsmiljø.

> [!NOTE]
> Talent-miljøer, der klargøres via LCS, indeholder ikke demodata, der er konfigureret til personaleopgaver (HR), eller der er specifikke for Talent. Hvis du har brug for et miljø, der indeholder demodata, anbefales det, at du tilmelder dig et gratis 60-dages [Talent-forsøgsmiljø](https://dynamics.microsoft.com/en-us/talent/overview/). Selvom et forsøgsmiljø ejes af den bruger, der har anmodet om det, kan andre brugere inviteres gennem systemadministrationsoplevelsen i det centrale HR-miljø. Forsøgsmiljøer indeholder fiktive data, der kan bruges til at udforske programmet på en sikker måde. De ikke er beregnet til brug som produktionsmiljøer. Bemærk, at når forsøgsmiljøet udløber efter 60 dage, slettes alle data i det, og de kan ikke gendannes. Du kan tilmelde dig til et nyt forsøgsmiljø, når det eksisterende miljø udløber.

## <a name="create-a-new-powerapps-environment-if-required"></a>Oprette et nyt PowerApps-miljø (hvis nødvendigt)
Integrationen mellem Talent- og PowerApps-miljøerne gør det muligt for dig at integrere og udvide brugen af Talent-data ved hjælp af PowerApps-værktøjer. Når du forstår formålet med PowerApps-miljøer, kan du bedre bygge programmer, der opfylder dine behov for at udvide Talent. Du kan finde flere oplysninger om PowerApps-miljøer, herunder omfanget af miljøet, adgang til miljøet og oprettelse og valg af et miljø, under [Annoncering af PowerApps-miljøer](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). Selv om hver lejer automatisk klargøres i et PowerApps-standardmiljø, er dette miljø muligvis ikke det bedste at bruge til Talent-installationen. Du skal overveje dataintegration og teststrategier i dette trin, og vi anbefaler, at du overvejer de mulige konsekvenser af dette for installationen, da nogle handlinger ikke er nemme at ændre senere. 

Selvom hver lejer automatisk klargøres i et PowerApps-standardmiljø, er dette miljø muligvis ikke det bedste til din Talent-installation. Du skal overveje dataintegrations- og teststrategier i dette trin. Derfor anbefaler vi, at du overvejer, hvilke forskellige konsekvenser det har for din installation, fordi det ikke er let at ændre PowerApps-miljøet senere.

1. I LCS skal du vælge **Administrer miljøer**. Du kommer til [PowerApps Administration](https://preview.admin.powerapps.com/environments), hvor du kan se eksisterende miljøer og oprette nye miljøer.
2. Vælg **Nyt miljø**.
3. Angiv et entydigt navn til miljøet, og vælg en placering at installere det på.

    > [!NOTE]
    > Talent er ikke tilgængeligt i alle områder. Derfor skal du kontrollere for tilgængelighed, før du kan vælge en placering til dit miljø.

4. Når du bliver spurgt, om du vil oprette en database, skal du vælge **Opret database** for at oprette CDS-databasen (Common Data Service), der skal være vært for en del af dine Talent-data. Når du opretter en database, kan du også integrere PowerApps-programmer i Talent.
5. Du bliver spurgt, hvilket adgangsniveau du vil bruge til databasen. Det anbefales, at du vælger **Begræns adgang**, da denne indstilling forhindrer, at Talent-brugerne kan få direkte adgang til følsomme data ved hjælp af et PowerApps-program.
6. Den CDS-database, der oprettes, indeholder demodata, som tilføjer inaktive medarbejdere og fiktive adresser, blandt andre oplysninger, til produktionsmiljøet. Du kan fjerne demodataene ved at følge disse trin, når du er færdig med at oprette CDS-databasen:

    > [!IMPORTANT]
    > Hvis du tidligere har oprettet en CDS-database og angivet nogle af firmaets produktionsdata i den, fjerner disse trin **alle** data i den valgte database, selv dit firmas produktionsdata.

    1. Log på [PowerApps](https://preview.web.powerapps.com/home).
    2. Vælg det miljø, som du oprettede i trin 2, i rullelisten øverst til højre.
    3. Udvid **Common Data Service** i navigationsruden til venstre, og vælg derefter **Enheder**.
    4. I højre side af siden skal du vælge ellipseknappen (**...**) og derefter vælge **Ryd alle data**.
    5. Vælg **Slet data** for at bekræfte, at du vil fjerne dataene. Denne handling fjerner som standard alle demodata, som indgår i CDS-databasen. Den fjerner også alle andre data, der er angivet i den valgte database.

Du kan nu bruge det nye miljø.

## <a name="grant-access-to-the-environment"></a>Give adgang til miljøet
Som standard har den globale administrator, der oprettede miljøet, adgang til det. Men andre programbrugere skal eksplicit tildeles adgang. Når du vil give adgang, skal du [tilføje brugere](../dev-itpro/sysadmin/tasks/create-new-users.md) og [tildele de relevante roller til dem](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) i det centrale HR-miljø. Du skal også tilføje disse brugere i PowerApps-miljøet, så de kan få adgang til Attract- og Onboard-programmerne. Proceduren er beskrevet her. Hvis du har brug for hjælp til at udføre trinnene, kan du se blogindlægget [Introduktion til PowerApps Administration](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Denne procedure fuldføres af den globale administrator, der installerede Talent-miljøet.

1. Åbn [PowerApps Administration](https://preview.admin.powerapps.com/environments).
2. Vælg de relevante miljøer.
3. Tilføj de nødvendige brugere til rollen **Miljøopretter** under fanen **Sikkerhed**.

Bemærk, at dette sidste trin, hvor du manuelt føjer brugere til PowerApps-miljøet, er midlertidigt. Det bliver udfyldt automatisk til sidst, når der tilføjes brugere i det centrale HR-miljø.

