---
title: "Bruge Excel-tilføjelsesprogram"
description: "Dette emne forklarer, hvordan du åbner objektdata i Microsoft Excel, og derefter få vist, opdatere og redigere dataene ved hjælp af tilføjelsesprogrammet Microsoft Dynamics-kontor for Excel. For at åbne objektet dataene, kan du starte fra enten Microsoft Excel eller Microsoft Dynamics 365 for operationer."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Bruge Excel-tilføjelsesprogram

Dette emne forklarer, hvordan du åbner objektdata i Microsoft Excel, og derefter få vist, opdatere og redigere dataene ved hjælp af tilføjelsesprogrammet Microsoft Dynamics-kontor for Excel. For at åbne objektet dataene, kan du starte fra enten Microsoft Excel eller Microsoft Dynamics 365 for operationer.

Ved at åbne objektdata i Microsoft Excel, kan du hurtigt og nemt få vist og redigere dataene ved hjælp af tilføjelsesprogrammet Microsoft Dynamics-kontor for Excel. Dette tilføjelsesprogram kræver Microsoft Excel 2016. **Bemærk:** Hvis lejer din Microsoft Azure Active Directory (AD Azure) er konfigureret til at bruge Active Directory Federation Services (AD FS), skal du kontrollere, at opdateringen maj 2016 er anvendt, så Excel-tilføjelsesprogram kan korrekt logge dig på.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Åbn objektdata i Excel, når du starter fra Dynamics 365 for operationer
1.  Klik på en side i Microsoft Dynamics 365 for operationer, **åben i Microsoft Office**. Hvis roddatakilden (tabel) for siden, er det samme som roddatakilden for objekter, som standard **Åbn i Excel** indstillinger er oprettet for siden. **Åbn i Excel** indstillinger kan findes på ofte brugte sider, som f.eks. **alle leverandører** og **alle kunder**.
2.  Klik på en **åbnes i Excel** indstilling, og Åbn den projektmappe, der er genereret. Denne projektmappe har binding-oplysningerne for enheden, en pointer til dit miljø og en pointer til Excel-tilføjelsesprogrammet.
3.  I Excel, skal du klikke på **aktivere redigering** til at aktivere Excel-tilføjelsesprogrammet til at køre. Tilføjelsesprogrammet Excel kører i ruden til højre i Excel-vinduet.
4.  Hvis du kører Excel-tilføjelsesprogrammet for første gang, skal du klikke på **har tillid til dette tilføjelsesprogram**.
5.  Hvis du bliver bedt om at logge på, skal du klikke på **logge på**, og log derefter på ved hjælp af de samme legitimationsoplysninger, du brugte til at logge på Dynamics 365 for operationer. Excel-tilføjelsesprogram kan bruge en tidligere-i kontekst fra Internet Explorer og automatisk logge dig på, hvis det er muligt. Derfor kontrollere brugernavnet i øverste højre hjørne af Excel-tilføjelsesprogrammet.

Tilføjelsesprogrammet Excel læser automatisk data for den enhed, du har valgt. Bemærk, at der bliver ingen data i projektmappen indtil læser det i Excel-tilføjelsesprogrammet.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Åbn objektdata i Excel, når du starter fra Excel
1.  I Excel, på den **Indsæt** under fanen den **Add-ins** skal du klikke på **Store** til at åbne Office-butikken.
2.  I Office-butik, kan du søge på nøgleordet "Dynamics", og klik på **Tilføj** ud for den **tilføjelsesprogrammet Microsoft Dynamics-kontor** (Excel-tilføjelsesprogrammet).
3.  Hvis du kører Excel-tilføjelsesprogrammet for første gang, skal du klikke på **har tillid til dette tilføjelsesprogram** til at aktivere Excel-tilføjelsesprogrammet til at køre. Tilføjelsesprogrammet Excel kører i ruden til højre i Excel-vinduet.
4.  Klik på **tilføje serveroplysninger** at åbne den **indstillinger** rude.
5.  Kopiere browser URL-adressen fra din destination Dynamics 365 for forekomst af operationer, indsætte det i den **URL-adresse** felt, og derefter slette alt efter værtsnavnet (f.eks. **/? cmp = usmf & mi = CustTableListPage**). Den deraf følgende URL-adresse skal have blot værtsnavnet (for eksempel **https://xxx.dynamics.com**).
6.  Klik på **OK**, og klik derefter på **Ja** at bekræfte ændringen. Excel tilføjer genstarter og indlæses metadata. Den **Design** knap er nu tilgængelig. Hvis Excel-tilføjelsesprogram har en **indlæses applets** knap, du sandsynligvis ikke er logget på som den korrekte bruger. Yderligere oplysninger finder du i "knappen Indlæs applets vises" i afsnittet "Fejlfinding" i dette emne.
7.  Klik på **Design**. Tilføjelsesprogrammet Excel henter enhedsmetadata.
8.  Klik på **Tilføj tabel**. Der vises en liste over enheder. Enheder, der er angivet i "navn -" etiketformat.
9.  Vælg en enhed på listen, f.eks. **kunde - kunder**, og klik derefter på **næste**.
10. Føje et felt fra den **tilgængelige felter** på listen til den **markerede felter**, klikke på feltet, og klik derefter på **Tilføj**. Du kan også dobbeltklikke på feltet.
11. Når du har tilføjet de ønskede felter til den **markerede felter** på listen, skal du sørge for, at markøren er placeret på det rigtige sted i regnearket (for eksempel celle A1), og klik derefter på **gjort**. Klik derefter på **gjort** at afslutte designeren.
12. Klik på **Opdater** til at trække i et sæt af data.

## <a name="view-and-update-entity-data-in-excel"></a>Få vist og opdatere objektdata i Excel
Når du læser enhedsdata i projektmappen af Excel-tilføjelsesprogrammet, kan du opdatere dataene når som helst ved at klikke på **Opdater** i Excel-tilføjelsesprogrammet.

## <a name="edit-entity-data-in-excel"></a>Rediger objektdata i Excel
Du kan ændre enhedsdata, som du kræver, og derefter udgive den igen ved at klikke på **Udgiv** i Excel-tilføjelsesprogrammet. Hvis du vil redigere en post, markere en celle i regnearket og derefter ændre celleværdien. Hvis du vil tilføje en ny post, skal du benytte en af følgende fremgangsmåder:

-   Klik et vilkårligt sted i regnearket, og klik derefter på **ny** i Excel-tilføjelsesprogrammet.
-   Klik på den sidste række i regnearket, og tryk derefter på tabulatortasten, indtil markøren flyttes ud af den sidste kolonne i rækken, og der oprettes en ny række.
-   Klik i rækken umiddelbart under regnearket, og begynde at angive data i en celle. Når du flytter fokus fra cellen, udvides regnearket for at medtage den nye række.

Hvis du vil slette en post, skal du benytte en af følgende fremgangsmåder:

-   Højreklik på det række tal ud for rækken i regnearket for at slette, og klik derefter på **slette**.
-   Højreklik på rækken regneark for at slette, og klik derefter på **slette**&gt;**rækker i**.

## <a name="add-or-remove-columns"></a>Tilføj eller fjern kolonner
Du kan bruge designer til at justere de kolonner, der automatisk føjes til regnearket.

1.  Starte data source designeren af Excel-tilføjelsesprogrammet ved at klikke på den **indstillinger** knap (symbolet gear) og derefter vælge det **aktivere design** afkrydsningsfelt.
2.  Klik på **Design** i Excel-tilføjelsesprogrammet. Alle datakilder, er angivet.
3.  Ved siden af datakilden, skal du klikke på den **Rediger** knap (symbolet blyant).
4.  Tilpasse listen i den **markerede felter** på listen, som du har brug for:
    -   Føje et felt fra den **tilgængelige felter** på listen til den **markerede felter**, klikke på feltet, og klik derefter på **Tilføj**. Du kan også dobbeltklikke på feltet.
    -   Fjerne et felt fra den **markerede felter**, klikke på feltet, og klik derefter på **fjerner**. Du kan også dobbeltklikke på feltet.
    -   Hvis du vil ændre rækkefølgen af felter, skal du klikke på den **markerede felter** på listen, og klik derefter på **af** eller **ned**.

5.  Anvend ændringerne til datakilden ved at klikke på **opdatering**. Klik derefter på **gjort** at afslutte designeren. Hvis du har tilføjet et felt (kolonne), skal du klikke på **Opdater** til at trække i et sæt opdaterede data.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
Der er nogle problemer, der kan løses gennem nogle nemme trin.

-   **Knappen Indlæs applets vises.** Hvis Excel-tilføjelsesprogram har en **indlæses applets** knap efter-logon, skal du sandsynligvis ikke er logget på som den korrekte bruger. Du kan løse dette problem ved at kontrollere, at det rigtige brugernavn vises i øverste højre hjørne af Excel-tilføjelsesprogrammet. Hvis der vises et forkert brugernavn, skal du klikke på det, logge af og derefter logge på igen.
-   **Du modtager meddelelsen "Forbudt".** Hvis du modtager meddelelsen "Forbudt", mens Excel-tilføjelsesprogram indlæses metadata, har den konto, der er logget på Microsoft Excel-tilføjelsesprogram ikke tilladelse til at bruge den målrettede service, forekomst eller databasen. Du kan løse dette problem ved at kontrollere, at det rigtige brugernavn vises i øverste højre hjørne af Excel-tilføjelsesprogrammet. Hvis der vises et forkert brugernavn, skal du klikke på det, logge af og derefter logge på igen.
-   **En tom webside vises i Excel.** Hvis der åbnes en tom webside under logon processen, kontoen, der kræver AD FS, men versionen af Excel, der kører tilføjelsesprogrammet er ikke ny nok til at indlæse dialogboksen Log på. Du kan løse dette problem ved at opdatere versionen af Excel, du bruger. For at opdatere versionen af Excel, når du er i en virksomhed, der er på den udskudte kanal, kan du bruge den [Office deployment tool](https://technet.microsoft.com/library/jj219422.aspx) til [flyttes fra den udskudte kanal til den aktuelle kanal](https://technet.microsoft.com/library/mt455210.aspx).



