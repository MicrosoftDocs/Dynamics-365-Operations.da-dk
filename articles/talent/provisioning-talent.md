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
ms.sourcegitcommit: ba1a3a78d59f3aec91473ba9bb20bda4804ec92e
ms.openlocfilehash: 0a43f5ff0987ede9f0cb80e5b4854f78e19e329b
ms.contentlocale: da-dk
ms.lasthandoff: 03/23/2018

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
2. Talent klargøres altid i et Microsoft PowerApps-miljø for at aktivere PowerApps-integration og -udvidelse. Læs afsnittet "Valg af et PowerApps miljø" i dette emne, før du fortsætter. 
3. Hvis du ikke allerede har et PowerApps-miljø, skal du følge trinnene i afsnittet "Oprette et nyt PowerApps-miljø (hvis nødvendigt)" i dette emne, før du fortsætter.

    > [!NOTE]
    > For at få vist eksisterende miljøer eller oprette nye miljøer skal den lejeradministrator, der klargør Talent, være tildelt til PowerApps P2-licensen. Hvis organisationen ikke har en PowerApps P2-licens, kan du få en fra din Cloud Solution Provider eller fra [PowerApps-prissætningssiden](https://powerapps.microsoft.com/en-us/pricing/).

4. Vælg **Tilføj**, og vælg derefter det miljø, Talent skal klargøres i.
5. Vælg **Ja** for at acceptere vilkårene og begynde installationen.

    Det nye miljø vises på listen over miljøer i navigationsruden til venstre. Men du kan ikke begynde at bruge miljøet, før installationsstatus er opdateret til **Installeret**. Dette tager normalt kun et par minutter. Hvis klargøringsprocessen mislykkes, skal du kontakte Support.

6. Vælg **Log på Talent** for at bruge det nye miljø.

> [!NOTE]
> Hvis du endnu ikke har godkendt de endelige krav, kan du installere en testforekomst af Talent i projektet. Du kan derefter bruge denne forekomst til at teste din løsning, indtil du kan godkende den. Hvis du bruger det nye miljø til test, skal du gentage denne procedure for at oprette et produktionsmiljø.

> [!NOTE]
> Talent-miljøer, der klargøres via LCS, indeholder ikke demodata, der er konfigureret til personaleopgaver (HR), eller der er specifikke for Talent. Hvis du har brug for et miljø, der indeholder demodata, anbefales det, at du tilmelder dig et gratis 60-dages [Talent-forsøgsmiljø](https://dynamics.microsoft.com/en-us/talent/overview/). Selvom et forsøgsmiljø ejes af den bruger, der har anmodet om det, kan andre brugere inviteres gennem systemadministrationsoplevelsen i det centrale HR-miljø. Forsøgsmiljøer indeholder fiktive data, der kan bruges til at udforske programmet på en sikker måde. De ikke er beregnet til brug som produktionsmiljøer. Bemærk, at når forsøgsmiljøet udløber efter 60 dage, slettes alle data i det, og de kan ikke gendannes. Du kan tilmelde dig til et nyt forsøgsmiljø, når det eksisterende miljø udløber.

## <a name="select-a-powerapps-environment"></a>Vælg et PowerApps-miljø

Integrationen mellem Talent- og PowerApps-miljøerne gør det muligt for dig at integrere og udvide brugen af Talent-data ved hjælp af PowerApps-værktøjer. Forståelse af formålet med PowerApps-miljøer vil ikke blot at hjælpe dig med at opbygge apps for at udvide Talent, men den vil også hjælpe dig med at vælge det korrekte miljø ved klargøring af Talent. Du kan finde flere oplysninger om PowerApps-miljøer, herunder omfanget af miljøet, adgang til miljøet og oprettelse og valg af et miljø, under [Annoncering af PowerApps-miljøer](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Brug følgende retningslinjer til fastsættelse af, hvilket PowerApps-miljø til Talent skal installeres i: 
1. I LCS skal du vælge Administrer miljøer, eller du kan gå direkte til PowerApps Administration, hvor du kan få vist eksisterende miljøer og oprette nye miljøer.
2. Der er knyttet et enkelt Talent-miljø til et enkelt PowerApps-miljø.
3. Et PowerApps-miljø "indeholder" Talent-programmet, sammen med de tilsvarende PowerApps-, Flow- og CDS-programmer. Hvis PowerApps-miljøet slettes, så slettes apps i det samtidig.
4. Dataintegration og teststrategier bør tages i betragtning, f.eks. sandkasse, UAT, produktion. Derfor anbefaler vi, at du overvejer, hvilke forskellige konsekvenser det har for din installation, fordi det ikke er let at ændre tilknytningen af Talent-miljøer til et PowerApps-miljø senere.
5. Følgende PowerApps-miljøer kan ikke bruges til Talent og filtreres fra valglisten i LCS:
 
    **CDS 2.0-miljøer** CDS 2.0 bliver offentligt tilgængelige den 21. marts 2018, men Talent understøtter endnu ikke CDS 2.0. Selvom du kan få vist og oprette CDS 2.0-databaser i PowerApps Administration, kan de ikke bruges i Talent. Muligheden for at bruge CDS 2.0-miljøer i Talent-installationer bliver tilgængelig på et senere tidspunkt.
   
 > [!Note]
 > Hvis du vil skelne mellem CDS 1.0 og 2.0-miljøer på administrationsportalen, skal du vælge et miljø, og se på **Oplysninger**. CDS 2.0-miljøer refererer alle til det forhold, at "Du kan styre disse indstillinger i Dynamics 365 Administration", du kan pege på en forekomst, og der er fane med navnet Database. 
 
   **Power Apps-standardmiljøer** Selvom hver lejer automatisk klargøres med et PowerApps-standardmiljø, anbefales det ikke at bruge dem sammen med Talent, da alle lejerbrugere har adgang til PowerApps-miljøet og derfor utilsigtet kan beskadige produktionsdata i forbindelse med test og gennemsyn af PowerApps- eller Flow-integrationer.
   
   **Miljøer til testkørsel** Miljøer med et navn, som f.eks. 'TestDrive – alias@domain' oprettes med en 60-dages udløbsperiode og udløber efter dette tidspunkt, og det medfører, at dit miljø fjernes automatisk.
   
   **Ikke-understøttede områder** I øjeblikket understøttes Talent kun i følgende områder: USA, Europa eller Australien.
  
6. Der er ingen specifikke handling, der skal udføres, når du har valgt det korrekte miljø, der skal bruges. Fortsæt klargøringsprocessen. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Oprette et nyt PowerApps-miljø (hvis nødvendigt)

Køre et PowerShell-script for at oprette et nyt PowerApps-miljø til Talent i forbindelse med den lejeradministrator, der har PowerApps Plan 2-licensen. Scriptet automatiserer følgende trin:


 + Oprettelse af et PowerApps-miljø
 + Oprettelse af en CDS 1.0-database
 + Fjernelse af alle eksempeldata i CDS 1.0-databasen


Udfør følgende instruktioner for at køre scriptet:

1. Hent filen ProvisionCDSEnvironment.zip fra følgende placering: [ProvisionCDSEnvironment scripts](https://go.microsoft.com/fwlink/?linkid=870436)  

2. Udpak hele indholdet af filen ProvisionCDSEnviroinment.zip til en mappe.

3. Kør Windows PowerShell- eller Windows PowerShell ISE-programmet som administrator.

   Besøg emnet [Angiv udførelsespolitik](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) for at lære mere om at angive udførelsespolitikken, så scripts kan køres.
  
4. I PowerShell skal du navigere til den mappe, hvor du udpakkede filen, og køre følgende kommando, idet du erstatter værdier, som angivet nedenfor:
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **EnvironmentName** skal erstattes med navnet på dit miljø. Dette navn vises i LCS og kan ses, når brugere vælge, hvilket Talent-miljø der skal bruges. 

   **YourLocation** skal erstattes med et af de områder, hvor Talent understøttes: unitedsates, europe, australia. 

   **-Verbose** er valgfrit og giver detaljerede oplysninger, der kan sendes til support, hvis der opstår problemer.

5. Fortsæt klargøringsprocessen.
 


## <a name="grant-access-to-the-environment"></a>Give adgang til miljøet
Som standard har den globale administrator, der oprettede miljøet, adgang til det. Men andre programbrugere skal eksplicit tildeles adgang. Når du vil give adgang, skal du [tilføje brugere](../dev-itpro/sysadmin/tasks/create-new-users.md) og [tildele de relevante roller til dem](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) i det centrale HR-miljø. Du skal også tilføje disse brugere i PowerApps-miljøet, så de kan få adgang til Attract- og Onboard-programmerne. Proceduren er beskrevet her. Hvis du har brug for hjælp til at udføre trinnene, kan du se blogindlægget [Introduktion til PowerApps Administration](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Denne procedure fuldføres af den globale administrator, der installerede Talent-miljøet.

1. Åbn [PowerApps Administration](https://preview.admin.powerapps.com/environments).
2. Vælg de relevante miljøer.
3. Tilføj de nødvendige brugere til rollen **Miljøopretter** under fanen **Sikkerhed**.

    Bemærk, at dette sidste trin, hvor du manuelt føjer brugere til PowerApps-miljøet, er midlertidigt. Det bliver udfyldt automatisk til sidst, når der tilføjes brugere i det centrale HR-miljø.

