---
title: Redigere og overvåge onlineordre- og asynkrone kundeordretransaktioner
description: Denne artikel beskriver, hvordan du redigerer og overvåger onlineordre- og asynkrone kundeordretransaktioner i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 10/21/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: dbeeff47446c1617da44f34ae56f333717f577a1
ms.sourcegitcommit: 18b7a02c497709e8d9c7b943d82f1fcc3dafa4cd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/21/2022
ms.locfileid: "9712102"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Redigere og overvåge onlineordre- og asynkrone kundeordretransaktioner

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du redigerer og overvåger onlineordre- og asynkrone kundeordretransaktioner i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Fra Commerce-version 10.0.5 til 10.0.6 er der tilføjet understøttelse for redigering af cash and carry-transaktioner (f.eks. salg og returneringer) og kassestyringstransaktioner (f.eks. kassebeholdning og fjernelse af betalingsmiddel). I Commerce version 10.0.7 blev der tilføjet understøttelse for redigering af onlineordretransaktioner og asynkrone kundeordretransaktioner.

## <a name="edit-and-audit-order-transactions"></a>Redigere og overvåge ordretransaktioner

Hvis du vil redigere og overvåge ordretransaktioner i Commerce headquarters, skal du følge disse trin.

1. Installér [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. På siden **Commerce-parametre** på fanen **Kundeordrer** i oversigtspanelet **Ordre** skal du angive en holdkode for **Holdkode for ordresynkroniseringsfejl**.
2. Afbryd andre ordresynkroniseringsjob, der er i konflikt med tidspunktet for redigering og overvågning.
3. Åbn arbejdsområdet **Butiksregnskab**. Felterne **Onlineordresynkroniseringsfejl** og **Kundeordresynkronisering** indeholder en forudfiltreret visning af detailtransaktionssiden. Hver enkelt viser de transaktionsposter, hvor synkroniseringen mislykkedes for den tilsvarende ordretype.
4. Åbn enten siden **Onlineordresynkroniseringsfejl** eller siden **Kundeordresynkroniseringsfejl**. Vælg en post for at få vist oplysninger om synkroniseringsfejlen. Oversigtspanelet **Synkroniseringsstatus** viser følgende fejloplysninger:

    - Ventende ordrestatus
    - Oplysninger om ordrefejl
    - Dato og klokkeslæt for ændring
    - Antal forsøg

1. Hvis fejloplysningerne indikerer, at posten skal rettes, skal du vælge **Office-tilføjelsesprogram** og derefter vælge **Rediger den valgte transaktion**. En Excel-fil, der viser oplysningerne om den valgte transaktion, åbnes.

    - Hvis den transaktion, der redigeres, er en onlineordretransaktion, indeholder Excel-filen følgende regneark:

        - **Transaktioner** – dette regneark indeholder oplysningerne for transaktionen på hovedniveau.
        - **Salgstransaktioner** – dette regneark indeholder oplysningerne for transaktionen på linjeniveau.
        - **Betalingstransaktioner** – dette regneark indeholder oplysningerne om transaktionens betalingslinjer.
        - **Rabattransaktioner** – dette regneark indeholder de rabatrelaterede oplysninger for transaktionen.
        - **Momstransaktioner** – dette regneark indeholder de momsrelaterede oplysninger for transaktionen.
        - **Gebyrtransaktioner** – dette regneark indeholder de gebyrrelaterede data for transaktionen.

    - Hvis den transaktion, der redigeres, er en asynkron kundeordretransaktion, indeholder Excel-filen følgende regneark:

        - **Linjer** – dette regneark indeholder oplysningerne for transaktionen på hoved- og linjeniveau.
        - **Betalinger** – dette regneark indeholder oplysningerne om transaktionens betalingslinjer.
        - **Rabatter** – dette regneark indeholder de rabatrelaterede detaljer for transaktionen.
        - **Moms** – dette regneark indeholder de momsrelaterede detaljer for transaktionen.
        - **Gebyrer** – dette regneark indeholder de gebyrrelaterede data for transaktionen.

1. I Excel-filen i feltet **Ventende ordrestatus** skal du angive **Redigering** og derefter publicere ændringen. På denne måde forhindrer du, at jobbet **Synkroniser ordre**, der kører i batchtilstand, springer denne post over under behandlingen.
1. I Excel-filen redigerer du de relevante felter og overfører derefter dataene tilbage til Commerce headquarters ved hjælp af publiceringsfunktionen i Dynamics Excel-tilføjelsesprogrammet. Når dataene er publiceret, afspejles ændringerne i systemet. Under publiceringen sker der ingen validering for de ændringer, brugerne foretager.
    > [!NOTE]
    > Hvis du ikke kan finde det felt, du skal redigere, skal du følge trinnene nedenfor for at tilføje det manglende felt i regnearket.
    >   1. Vælg **Design** i Data Connector.
    >   1. Vælg blyantsikonet ud for den tabel, du vil føje et felt til.
    >   1. Markér feltet i sektionen **Tilgængelige felter**, og vælg derefter **Tilføj**.
    >   1. Tilføj så mange felter, du har brug for, og vælg derefter **Opdater**.
    >   1. Når opdateringen er fuldført, skal du muligvis vælge **Opdater** for at opdatere værdierne.

3. Du kan få vist et komplet revisionsspor for ændringerne ved at vælge **Vis revisionsspor** i hovedet på **detailtransaktionen** for ændringerne på hovedniveau og i den relevante sektion og post på den relevante transaktionsside. Alle ændringer, der f.eks. er relateret til salgslinjer, vises på siden **Salgstransaktioner**, og alle ændringer, der er relateret til betalinger, vises på siden **Betalingstransaktioner**. Følgende revisionsoplysninger bevares for ændringerne:

    - Dato og klokkeslæt for ændring
    - Felt
    - Gammel værdi
    - Ny værdi
    - Ændret af

1. Når du har foretaget og publiceret ændringerne, skal du vælge **Synkroniser ordre** for at starte synkroniseringsprocessen med det samme. Du kan også vente på, at synkroniseringsprocessen, der kører i batchtilstand, behandler transaktionen.

Når ordrerne er synkroniseret, sættes de som standard i en holdstatus baseret på den holdkode, der er defineret i Commerce-parametrene. Holdstatussen på ordrerne skal fjernes, før de kan behandles yderligere til opfyldelse eller andre aktiviteter.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere og overvåge cash and carry-transaktioner og kassestyringstransaktioner](edit-cash-trans.md)

[Redigere økonomiske dimensioner for detailtransaktioner](edit-financial-dim.md)

[Oprette en Excel-projektmappe for at redigere detailtransaktioner](create-excel-edit.md)

[Føje felter til en Excel-projektmappe for at redigere detailtransaktioner](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
