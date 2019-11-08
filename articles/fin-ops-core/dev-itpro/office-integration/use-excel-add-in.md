---
title: Åbne enhedsdata i Excel og opdatere dem ved hjælp af tilføjelsesprogrammet til Excel
description: Dette emne forklarer, hvordan du åbner enhedsdata i Microsoft Excel, og derefter får vist, opdaterer og redigerer dataene ved hjælp af Microsoft Dynamics Office-tilføjelsesprogrammet til Excel.
author: ChrisGarty
manager: AnnBe
ms.date: 04/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 210231bb442928674b490d83f50bf787d7bfa60c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181007"
---
# <a name="open-entity-data-in-excel-and-update-it-by-using-the-excel-add-in"></a>Åbne enhedsdata i Excel og opdatere dem ved hjælp af tilføjelsesprogrammet til Excel

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du åbner enhedsdata i Microsoft Excel, og derefter får vist, opdaterer og redigerer dataene ved hjælp af Microsoft Dynamics Office-tilføjelsesprogrammet til Excel. Når du vil åbne enhedsdataene, kan du starte fra enten Excel eller Finance and Operations.

Ved at åbne enhedsdata i Excel, kan du hurtigt og let få vist og redigere dataene ved hjælp af tilføjelsesprogrammet til Excel. Dette tilføjelsesprogram kræver Microsoft Excel 2016.

> [!NOTE]
> Hvis din Microsoft Azure Active Directory (Azure AD)-lejer er konfigureret til at bruge Active Directory Federation Services (AD FS), skal du kontrollere, at opdateringen fra maj 2016 til Office er anvendt, så Excel-tilføjelsesprogrammet kan logge dig korrekt på.

Hvis du vil vide mere om brug af tilføjelsesprogrammet til Excel, kan du se den korte video [Opret en Excel-skabelon for hoved- og linjemønstre i Dynamics 365 for Finance and Operations](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-finance-and-operations"></a>Åbn objektdata i Excel, når du starter fra Finance and Operations
1. Klik på **Åbn i Microsoft Office** på en side i Finance and Operations.

    Hvis roddatakilden (tabel) for siden er den samme som roddatakilden for alle enheder, genereres standardindstillingerne **Åbn i Excel** for siden. **Åbn i Excel**-indstillinger kan findes på ofte brugte sider, f.eks. **Alle leverandører** og **Alle kunder**.
 
2. Vælg en **Åbn i Excel**-indstilling, og åbn den projektmappe, der er genereret. Denne projektmappe har binding-oplysningerne for enheden, en pointer til dit miljø og en pointer til Excel-tilføjelsesprogrammet.
3. I Excel skal du vælge **Aktivér redigering** for at aktivere Excel-tilføjelsesprogrammet til at køre. Excel-tilføjelsesprogrammet kører i ruden til højre i Excel-vinduet.
4. Hvis du kører Excel-tilføjelsesprogrammet for første gang, skal du vælge **Har tillid til dette tilføjelsesprogram**.
5. Hvis du bliver bedt om at logge på, skal du vælge **Log på** og derefter logge på ved hjælp af de samme legitimationsoplysninger, du brugte til at logge på Finance and Operations. Excel-tilføjelsesprogrammet bruger en tidligere logon-kontekst fra Internet Explorer og logger dig automatisk på, hvis det er muligt. Derfor skal du kontrollere brugernavnet i øverste højre hjørne af Excel-tilføjelsesprogrammet.

Excel-tilføjelsesprogrammet læser automatisk dataene for den enhed, du har valgt. Bemærk, at der ikke er nogen data i projektmappen, før Excel-tilføjelsesprogrammet læser dem ind.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Åbn enhedsdata i Excel, når du starter fra Excel
1. I Excel skal du under fanen **Indsæt** i gruppen **Tilføjelsesprogrammer** vælge **Store** for at åbne Office Store.
2. I Office Store kan du søge på nøgleordet **Dynamics** og derefter vælge **Tilføj** ud for **Microsoft Dynamics Office-tilføjelsesprogram** (Excel-tilføjelsesprogrammet).
3. Hvis du kører Excel-tilføjelsesprogrammet for første gang, skal du vælge **Har tillid til dette tilføjelsesprogram** for at aktivere Excel-tilføjelsesprogrammet til at køre. Excel-tilføjelsesprogrammet kører i ruden til højre i Excel-vinduet.
4. Vælg **Tilføj serveroplysninger** for at åbne ruden **Indstillinger**.
5. I din browser skal du kopiere URL-adressen fra din destinationsforekomst af Finance and Operations, indsæt den i feltet **Serverens URL-adresse**, og slet derefter alt efter værtsnavnet. Den resulterende URL-adresse skal kun indeholde værtsnavnet.

    Hvis URL-adressen f.eks. er `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`, skal du slette alt undtagen `https://xxx.dynamics.com`.

6. Vælg **OK**, og vælg derefter **Ja** for at bekræfte ændringen. Excel-tilføjelsesprogrammet genstarter og indlæser metadata.

    Knappen **Design** er nu tilgængelig. Hvis Excel-tilføjelsesprogrammet har en knap med teksten **Indlæs applets**, er du sandsynligvis ikke er logget på som den korrekte bruger. Du kan finde yderligere oplysninger i "Knappen Indlæs applets vises" i afsnittet [Fejlfinding](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#troubleshooting) i dette emne.

7. Vælg **Design**. Excel-tilføjelsesprogrammet henter enhedsmetadata.
8. Vælg **Tilføj tabel**. Der vises en liste over enheder. Enhederne er angivet i formatet "Navn – label".
9. Vælg en enhed på listen, f.eks. **Kunde - kunder**, og vælg derefter **Næste**.
10. Hvis du vil føje et felt fra listen **Tilgængelige felter** til listen **Valgte felter**, skal du vælge feltet, og derefter vælge **Tilføj**. Du kan også dobbeltklikke på feltet på listen **Tilgængelige felter**.
11. Når du har tilføjet felterne til listen **Valgte felter**, skal du sørge for, at markøren er placeret på det rigtige sted i regnearket (f.eks. celle A1) og derefter vælge **Udført**. Vælg derefter **Udført** for at lukke designeren.
12. Vælg **Opdater** for at trække i et sæt data ind.

## <a name="view-and-update-entity-data-in-excel"></a>Få vist og opdater enhedsdata i Excel
Når Excel-tilføjelsesprogrammet har indlæst enhedsdata i projektmappen, kan du opdatere dataene når som helst ved at vælge **Opdater** i Excel-tilføjelsesprogrammet.

## <a name="edit-entity-data-in-excel"></a>Rediger enhedsdata i Excel
Du kan ændre enhedsdata efter behov, og derefter udgive dem tilbage igen ved at vælge **Udgiv** i Excel-tilføjelsesprogrammet. Hvis du vil redigere en post, skal du markere en celle i regnearket og derefter ændre celleværdien. Hvis du vil tilføje en ny post, skal du benytte en af følgende fremgangsmåder:

- Klik et vilkårligt sted i datakildetabellen, og vælg derefter **Ny** i Excel-tilføjelsesprogrammet.
- Klik et sted i den sidste række i datakildetabellen, og tryk derefter på tabulatortasten, indtil markøren flyttes ud af den sidste kolonne i rækken, og der oprettes en ny række.
- Klik et sted i rækken umiddelbart under datakildetabellen, og begynd at angive data i en celle. Når du flytter fokus fra cellen, udvides tabellen for at medtage den nye række.
- Ved feltbindinger i overskriftsposter skal du vælge et af felterne, og derefter vælge **Ny** i Excel-tilføjelsesprogrammet.

Bemærk, at der kun kan oprettes en ny post, hvis alle de nøglefelter og obligatoriske felter er bundet i regnearket, eller hvis standardværdier blev udfyldt ved hjælp af filterbetingelsen.

Hvis du vil slette en post, skal du benytte en af følgende fremgangsmåder:

- Højreklik på rækkenummeret ud for den række i regnearket, der skal slettes, og vælg derefter **Slet**.
- Højreklik et sted i den række i regnearket, der skal slettes, og vælg derefter **Slet** &gt; **Tabelrækker**.

Hvis datakilder er blevet tilføjet som relaterede datakilder, publiceres overskriften før linjerne. Hvis der er afhængigheder mellem andre datakilder, kan det være nødvendigt at ændre standardpubliceringsrækkefølgen. For at ændre publiceringsrækkefølgen i Excel-tilføjelsesprogrammet, skal du vælge knapppen **Indstillinger** (tandhjulsymbolet), og derefter skal du på oversigtspanelet **Dataconnector** vælge **Konfigurer publiceringsrækkefølge**.

## <a name="add-or-remove-columns"></a>Tilføj eller fjern kolonner
Du kan bruge designeren til at justere de kolonner, der automatisk er føjet til regnearket.

> [!NOTE]
> Hvis knappen **Design** ikke vises under knappen **Filter** i Excel-tilføjelsesprogrammet, skal du aktivere datakildedesigneren. Vælg knappen **Indstillinger** (tandhjulsymbolet), og vælg derefter afkrydsningsfeltet **Aktivér design** .

1. Vælg **Design** i Excel-tilføjelsesprogrammet. Alle datakilderne er angivet.
2. Ved siden af datakilden, skal du vælge knappen **Rediger** (blyantssymbolet).
3. På listen **Valgte felter** skal du justere listen over felter efter behov:

    - Hvis du vil føje et felt fra listen **Tilgængelige felter** til listen **Valgte felter**, skal du vælge feltet, og derefter vælge **Tilføj**. Du kan også dobbeltklikke på feltet på listen **Tilgængelige felter**.
    - Hvis du vil fjerne et felt fra listen **Valgte felter**, skal du vælge feltet og derefter vælge **Fjern**. Du kan også dobbeltklikke på feltet.
    - Hvis du vil ændre rækkefølgen af felter på listen **Valgte felter**, skal du vælge et felt og derefter vælge **Op** eller **Ned**.

4. Du anvender dine ændringer af datakilden ved at vælge **Opdater**. Vælg derefter **Udført** for at lukke designeren.
5. Hvis du har tilføjet et felt (kolonne), skal du vælge **Opdater** for at trække et sæt opdaterede data ind.

## <a name="copy-environment-data"></a>Kopiér miljødata

De data, der indlæses i projektmappen fra ét miljø kan kopieres til et andet miljø. Du kan ikke dog kun ændre URL-adressen for forbindelsen, fordi datacachen i projektmappen vil fortsætte med at behandle dataene som en eksisterende data. I stedet skal du bruge funktionen Kopiér miljødata for at udgive dataene til et nyt miljø som nye data.

1. Vælg knappen **Indstillinger** (tandhjulssymbolet), og på oversigtspanelet **Dataconnector** skal du derefter vælge **Kopiér miljødata**. 
2. Angiv URL-adressen til serveren til det nye miljø. 
3. Vælg **OK**, og vælg derefter **Ja** for at bekræfte handlingen. Excel-tilføjelsesprogrammet genstartes, og opretter forbindelse til det nye miljø. Alle eksisterende data i projektmappen behandles som nye data.

    Når Excel-tilføjelsesprogrammet er genstartet, viser et meddelelsesfelt, at projektmappen er i miljøkopieringstilstand.

4. Hvis du vil kopiere dataene til det nye miljø som nye data, skal du vælge **Udgiv**. Hvis du vil annullere miljøkopieringshandlingen og gennemse de eksisterende data i det nye miljø, skal du vælge **Opdater**.

## <a name="troubleshooting"></a>Fejlfinding
Der er nogle få problemer, der kan løses gennem nogle nemme trin.

- **Knappen Indlæs applets vises** – Hvis Excel-tilføjelsesprogrammet har en knap med teksten **Indlæs applets**, når du er logget på, er du sandsynligvis ikke er logget på som den korrekte bruger. Du kan løse dette problem ved at kontrollere, at det rigtige brugernavn vises i øverste højre hjørne af Excel-tilføjelsesprogrammet. Hvis der vises et forkert brugernavn, skal du vælge det, logge af og derefter logge på igen.
- **Du får vist meddelelsen "Forbudt"** – Hvis du får vist meddelelsen "Forbudt", mens Excel-tilføjelsesprogrammet indlæser metadata, har den konto, der er logget på Excel-tilføjelsesprogrammet ikke tilladelse til at bruge den målsatte tjeneste, forekomst eller database. Du kan løse dette problem ved at kontrollere, at det rigtige brugernavn vises i øverste højre hjørne af Excel-tilføjelsesprogrammet. Hvis der vises et forkert brugernavn, skal du vælge det, logge af og derefter logge på igen.
- **En tom webside vises i Excel** – Hvis der åbnes en tom webside under logon-processen, kræver kontoen AD FS, men den version af Excel, der kører tilføjelsesprogrammet, er ikke ny nok til at indlæse logon-dialogboksen. Du kan løse dette problem ved at opdatere den version af Excel, du bruger. For at opdatere versionen af Excel, når du er i en virksomhed, der er på den udskudte kanal, kan du bruge [Office Udrulningsværktøj](https://technet.microsoft.com/library/jj219422.aspx) til [at flytte fra den udskudte kanal til den aktuelle kanal](https://technet.microsoft.com/library/mt455210.aspx).