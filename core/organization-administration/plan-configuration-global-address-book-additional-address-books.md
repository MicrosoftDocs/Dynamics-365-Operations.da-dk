---
title: "Konfigurer globale adressebøger"
description: "I denne artikel beskrives de overvejelser og de beslutninger, du skal foretage i planlægningsprocessen, før du opsætter og konfigurerer det globale adressekartotek og eventuelle supplerende adressekartoteker i Microsoft Dynamics 365 for Finance and Operations. Nogle af afgørelser kræver, at du bekræfter de beslutninger, der er foretaget på andre områder for produktet, f.eks. organisationshierarkiet."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 93a9c35b82a8bacd0295416015e783cb6348f550
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="configure-global-address-books"></a>Konfigurer globale adressebøger

[!include[banner](../includes/banner.md)]


I denne artikel beskrives de overvejelser og de beslutninger, du skal foretage i planlægningsprocessen, før du opsætter og konfigurerer det globale adressekartotek og eventuelle supplerende adressekartoteker i Microsoft Dynamics 365 for Finance and Operations. Nogle af afgørelser kræver, at du bekræfter de beslutninger, der er foretaget på andre områder for produktet, f.eks. organisationshierarkiet.

<a name="global-address-book"></a>Globalt adressekartotek
-------------------

Før du begynder at arbejde med det globale adressekartotek, skal du bestemme standardværdierne for det. Disse værdier bruges derefter til eventuelle yderligere adressekartoteker, du opretter. **Beslutninger:**

-   I hvilken rækkefølge skal navne vises i, for partposter af typen **Person**? Én sekvens er f.eks. efternavn, mellemnavn, fornavn.
-   Skal partposter slettes fra adressekartoteket, når rolleposten slettes? Hvis f.eks. en kundepost slettes, skal partposten også slettes?
-   Når der oprettes en ny post, skal brugerne så have besked, hvis der findes en dubletpost i det globale adressekartotek?
-   Skal DUNS-nummeret (Data Universal Numbering System) inkluderes i oplysningerne om en partpost?
-   Hvis DUNS-nummeret er medtaget i en partpost, bør tallets entydighed så kontrolleres?
-   Når en partpost oprettes i det globale adressekartotek, vil du så have en standard for parttype, person eller organisation?
-   Hvilke brugerroller skal have adgang til private adresser og kontaktoplysninger for partposten?

## <a name="additional-address-books"></a>Yderligere adressekartoteker
Når du opretter det globale adressekartotek, kan du oprette yderligere adressekartoteker, du ønsker, som et separat adressekartotek for hvert firma i organisationen eller for hvert forretningsområde. Fabrikam er f.eks. en international organisation, der har flere firmaer og flere forretningsområder. Fabrikam planlægger at oprette et adressekartotek for hvert forretningsområde. Til forretningsområder, der findes på mere end én lokalitet, f.eks. trykluftsværktøj, planlægger Fabrikam at oprette et adressekartotek for hver enkelt lokalitet. Chris, it-leder hos Fabrikam, har oprettet følgende liste over adressekartoteker, der kræves. Denne liste beskriver også de partposter, som hver enkelt adressekartotek skal indeholde.

-   **Offentlig sektor-kontrakter (OffSK)** – partposter for alle parter, der er involveret i de kontrakter med den offentlige sektor, som Fabrikam har.
-   **Privat sektor-kontrakter (PriSK)** – partposter for alle parter, der er involveret i de kontrakter med den private sektor, som Fabrikam har.
-   **Elektroniske værktøjer (EV)** – partposter for alle parter, der er involveret i køb eller salg af elektroniske værktøjer, eller som på anden måde har noget at gøre med de elektroniske værktøjer, der stilles til rådighed af eller købes til Fabrikam i Fabrikams firma i Japan.
-   **Trykluftsværktøj (TVJPN)** – partposter for alle parter, der er involveret i køb eller salg af trykluftsværktøj, eller som på anden måde har noget at gøre med det trykluftsværktøj, der stilles til rådighed af eller købes til Fabrikam i Fabrikams firma i Japan.
-   **Trykluftsværktøj (TVUSA)** – partposter for alle parter, der er involveret i køb eller salg af trykluftsværktøj, eller som på anden måde har noget at gøre med det trykluftsværktøj, der stilles til rådighed af eller købes til Fabrikam i Fabrikams firma i USA.

**Beslutning:**

-   Hvor mange yderligere adressekartoteker vil du oprette?

### <a name="address-book-security"></a>Sikkerhed for adressekartotek

Du kan når som helst oprette adressekartoteker, og du kan også indstille sikkerhedsparametre for adressekartotekerne, hvis du vil. Det er ikke nødvendigt at indstille sikkerhedsrettigheder for et adressekartotek, men hvis du ikke gør det, kan alle arbejdere i organisationen se alle partposter i det pågældende adressekartotek. Du kan indstille sikkerhedsrettigheder til partposter via adressekartoteker: Sikkerhedsrettigheder er baseret på teams. Denne fremgangsmåde garanterer, at det kun er de arbejdere, der er tildelt et team, der har adgang til et adressekartotek, der kan se partposterne i dette adressekartotek. Du skal vælge de teams, der har adgang til hver enkelt adressekartotek. For hvert adressekartotek kan du indstille sikkerhedsrettigheder, som tillader eller afviser adgang til bestemte teams. Hvis du giver teamrettigheder til et adressekartotek, kan alle medlemmer af teamet se posterne i adressekartoteket. Hvis du ikke giver teamadgang til et adressekartotek, kan medlemmerne i teamet ikke se adressekartoteket eller indholdet deraf. **Beslutning:**

-   Hvilke teams skal have adgang til hvert nye adressekartotek, du opretter?





