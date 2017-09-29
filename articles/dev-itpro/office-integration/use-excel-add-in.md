---
title: "Brug af Excel-tilføjelsesprogrammet"
description: "Dette emne forklarer, hvordan du åbner enhedsdata i Microsoft Excel, og derefter får vist, opdaterer og redigerer dataene ved hjælp af Microsoft Dynamics Office-tilføjelsesprogrammet til Excel."
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 06fc9f8dda83fddea9ae331bb82c8874b15d76b9
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="use-the-excel-add-in"></a>Brug af Excel-tilføjelsesprogrammet

[!include[banner](../includes/banner.md)]


Dette emne forklarer, hvordan du åbner enhedsdata i Microsoft Excel, og derefter får vist, opdaterer og redigerer dataene ved hjælp af Microsoft Dynamics Office-tilføjelsesprogrammet til Excel. For at åbne enhedsdataene kan du enten starte fra Microsoft Excel eller Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

Ved at åbne enhedsdata i Microsoft Excel, kan du hurtigt og let få vist og redigere dataene ved hjælp af Microsoft Dynamics Office-tilføjelsesprogrammet til Excel. Dette tilføjelsesprogram kræver Microsoft Excel 2016. **Bemærk!** Hvis din Microsoft Azure Active Directory (AD Azure)-lejer er konfigureret til at bruge Active Directory Federation Services (AD FS), skal du kontrollere, at opdateringen fra maj 2016 er anvendt, så Excel-tilføjelsesprogrammet kan logge dig korrekt på.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-finance-and-operations"></a>Åbn objektdata i Excel, når du starter fra Dynamics 365 for Finance and Operations
1.  Klik på **Åbn i Microsoft Office** på en side i Microsoft Dynamics 365 for Finance and Operations. Hvis roddatakilden (tabel) for siden er den samme som roddatakilden for alle enheder, genereres standardindstillingerne **Åbn i Excel** for siden. **Åbn i Excel**-indstillinger kan findes på ofte brugte sider, f.eks. **Alle leverandører** og **Alle kunder**.
2.  Klik på en **Åbn i Excel**-indstilling, og åbn den projektmappe, der er genereret. Denne projektmappe har binding-oplysningerne for enheden, en pointer til dit miljø og en pointer til Excel-tilføjelsesprogrammet.
3.  I Excel skal du klikke på **Aktivér redigering** for at aktivere Excel-tilføjelsesprogrammet til at køre. Excel-tilføjelsesprogrammet kører i ruden til højre i Excel-vinduet.
4.  Hvis du kører Excel-tilføjelsesprogrammet for første gang, skal du klikke på **Har tillid til dette tilføjelsesprogram**.
5.  Hvis du bliver bedt om at logge på, skal du klikke på **Log på** og derefter logge på ved hjælp af de samme legitimationsoplysninger, du brugte til at logge på Dynamics 365 for Finance and Operations. Excel-tilføjelsesprogrammet bruger en tidligere logon-kontekst fra Internet Explorer og logger dig automatisk på, hvis det er muligt. Derfor skal du kontrollere brugernavnet i øverste højre hjørne af Excel-tilføjelsesprogrammet.

Excel-tilføjelsesprogrammet læser automatisk dataene for den enhed, du har valgt. Bemærk, at der ikke er nogen data i projektmappen, før Excel-tilføjelsesprogrammet læser dem ind.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Åbn enhedsdata i Excel, når du starter fra Excel
1.  I Excel skal du under fanen **Indsæt** i gruppen **Tilføjelsesprogrammer** klikke på **Store** for at åbne Office Store.
2.  I Office Store kan du søge på nøgleordet "Dynamics" og klikke på **Tilføj** ud for **Microsoft Dynamics Office-tilføjelsesprogram** (Excel-tilføjelsesprogrammet).
3.  Hvis du kører Excel-tilføjelsesprogrammet for første gang, skal du klikke på **Har tillid til dette tilføjelsesprogram** for at aktivere Excel-tilføjelsesprogrammet til at køre. Excel-tilføjelsesprogrammet kører i ruden til højre i Excel-vinduet.
4.  Klik på **Tilføj serveroplysninger** for at åbne ruden **Indstillinger**.
5.  Kopiér browser-URL-adressen fra din destinationsforekomst af Dynamics 365 for Finance and Operations, indsæt den i feltet **Serverens URL-adresse**, og slet derefter alt efter værtsnavnet. Den resulterende URL-adresse skal have blot værtsnavnet.
Hvis URL-adressen f.eks. er https://xxx.dynamics.com/?cmp=usmf&amp;mi = CustTableListPage, skal du slette alt undtagen **https://xxx.dynamics.com**.
6.  Klik på **OK**, og klik derefter på **Ja** for at bekræfte ændringen. Excel-tilføjelsesprogrammet genstarter og indlæser metadata. Knappen **Design** er nu tilgængelig. Hvis Excel-tilføjelsesprogrammet har en knap med teksten **Indlæs applets**, er du sandsynligvis ikke er logget på som den korrekte bruger. Du kan finde yderligere oplysninger i "Knappen Indlæs applets vises" i afsnittet "Fejlfinding" i dette emne.
7.  Klik på **Design**. Excel-tilføjelsesprogrammet henter enhedsmetadata.
8.  Klik på **Tilføj tabel**. Der vises en liste over enheder. Enhederne er angivet i formatet "Navn – label".
9.  Vælg en enhed på listen, f.eks. **Kunde - kunder**, og klik derefter på **Næste**.
10. Hvis du vil føje et felt fra listen **Tilgængelige felter** til listen **Valgte felter**, skal du klikke på feltet, og derefter klikke på **Tilføj**. Du kan også dobbeltklikke på feltet.
11. Når du har tilføjet felterne til listen **Valgte felter**, skal du sørge for, at markøren er placeret på det rigtige sted i regnearket (f.eks. celle A1) og derefter klikke på **Udført**. Klik derefter på **Udført** for at lukke designeren.
12. Klik på **Opdater** for at trække i et sæt data ind.

## <a name="view-and-update-entity-data-in-excel"></a>Få vist og opdater enhedsdata i Excel
Når Excel-tilføjelsesprogrammet har indlæst enhedsdata i projektmappen, kan du opdatere dataene når som helst ved at klikke på **Opdater** i Excel-tilføjelsesprogrammet.

## <a name="edit-entity-data-in-excel"></a>Rediger enhedsdata i Excel
Du kan ændre enhedsdata efter behov, og derefter udgive dem tilbage igen ved at klikke på **Udgiv** i Excel-tilføjelsesprogrammet. Hvis du vil redigere en post, skal du markere en celle i regnearket og derefter ændre celleværdien. Hvis du vil tilføje en ny post, skal du benytte en af følgende fremgangsmåder:

-   Klik et vilkårligt sted i datakildetabellen, og klik derefter på **Ny** i Excel-tilføjelsesprogrammet.
-   Klik på den sidste række i datakildetabellen, og tryk derefter på tabulatortasten, indtil markøren flyttes ud af den sidste kolonne i rækken, og der oprettes en ny række.
-   Klik i rækken umiddelbart under datakildetabellen, og begynd at angive data i en celle. Når du flytter fokus fra cellen, udvides tabellen for at medtage den nye række.
-   Ved feltbindinger i overskriftsposter skal du klikke på et af felterne, og derefter klikke på **Ny** i Excel-tilføjelsesprogrammet.

Bemærk, at der kun kan oprettes en ny post, hvis alle de nøglefelter og obligatoriske felter er bundet i regnearket, eller hvis standardværdier blev udfyldt ved hjælp af filterbetingelsen.
Hvis du vil slette en post, skal du benytte en af følgende fremgangsmåder:

-   Højreklik på rækkenummeret ud for den række i regnearket, der skal slettes, og klik derefter på **Slet**.
-   Højreklik i regnearksrækken, der skal slettes, og klik derefter på **Slet** &gt; **Tabelrækker**.
Hvis datakilder er blevet tilføjet som relaterede, publiceres overskriften før linjerne. Hvis der er afhængigheder mellem andre datakilder, kan det være nødvendigt at ændre standardpubliceringsrækkefølgen. Hvis du vil ændre publiceringsrækkefølgen, skal du i Excel-tilføjelsesprogrammet klikke på knappen **Indstillinger** (tandhjulsymbolet). Klik derefter på **Konfigurer publiceringsrækkefølge** i oversigtspanelet **Data Connector**.

## <a name="add-or-remove-columns"></a>Tilføj eller fjern kolonner
Du kan bruge designeren til at justere de kolonner, der automatisk er føjet til regnearket.

1.  Start datakildedesigneren i Excel-tilføjelsesprogrammet ved at klikke på knappen **Indstillinger** (tandhjulsymbolet) og derefter markere afkrydsningsfeltet **Aktivér design**.
2.  Klik på **Design** i Excel-tilføjelsesprogrammet. Alle datakilderne er angivet.
3.  Ved siden af datakilden, skal du klikke på knappen **Rediger** (blyantssymbolet).
4.  Tilpas listen i listen **Valgte felter** efter behov:
    -   Hvis du vil føje et felt fra listen **Tilgængelige felter** til listen **Valgte felter**, skal du klikke på feltet, og derefter klikke på **Tilføj**. Du kan også dobbeltklikke på feltet.
    -   Hvis du vil fjerne et felt fra listen **Valgte felter**, skal du klikke på feltet og derefter klikke på **Fjern**. Du kan også dobbeltklikke på feltet.
    -   Hvis du vil ændre rækkefølgen af felter, skal du klikke på feltet på listen **Valgte felter**, klikke på et felt og derefter klikke på **Op** eller **Ned**.

5. Du anvender dine ændringer af datakilden ved at klikke på **Opdater**. Klik derefter på **Udført** for at lukke designeren. 
6. Hvis du har tilføjet et felt (kolonne), skal du klikke på **Opdater** for at trække et sæt opdaterede data ind.

## <a name="troubleshooting"></a>Fejlfinding
Der er nogle få problemer, der kan løses gennem nogle nemme trin.

-   **Knappen Indlæs applets vises.** Hvis Excel-tilføjelsesprogrammet har en knap med teksten **Indlæs applets**, når du er logget på, er du sandsynligvis ikke er logget på som den korrekte bruger. Du kan løse dette problem ved at kontrollere, at det rigtige brugernavn vises i øverste højre hjørne af Excel-tilføjelsesprogrammet. Hvis der vises et forkert brugernavn, skal du klikke på det, logge af og derefter logge på igen.
-   **Du få vist meddelelsen "Forbudt".** Hvis du får vist meddelelsen "Forbudt", mens Excel-tilføjelsesprogrammet indlæser metadata, har den konto, der er logget på Microsoft Excel-tilføjelsesprogrammet ikke tilladelse til at bruge den målsatte tjeneste, forekomst eller database. Du kan løse dette problem ved at kontrollere, at det rigtige brugernavn vises i øverste højre hjørne af Excel-tilføjelsesprogrammet. Hvis der vises et forkert brugernavn, skal du klikke på det, logge af og derefter logge på igen.
-   **En tom webside vises i Excel.** Hvis der åbnes en tom webside under logon-processen, kræver kontoen AD FS, men den version af Excel, der kører tilføjelsesprogrammet, er ikke ny nok til at indlæse logon-dialogboksen. Du kan løse dette problem ved at opdatere den version af Excel, du bruger. For at opdatere versionen af Excel, når du er i en virksomhed, der er på den udskudte kanal, kan du bruge [Office Udrulningsværktøj](https://technet.microsoft.com/library/jj219422.aspx) til [at flytte fra den udskudte kanal til den aktuelle kanal](https://technet.microsoft.com/library/mt455210.aspx).




