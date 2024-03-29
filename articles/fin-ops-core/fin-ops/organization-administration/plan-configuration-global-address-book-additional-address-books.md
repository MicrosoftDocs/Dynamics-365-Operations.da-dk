---
title: Planen for det globale adressekartotek og andre adressekartoteker
description: Denne artikel beskriver de overvejelser og de beslutninger, du skal foretage i planlægningsprocessen.
author: msftbrking
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288c96d8c877f5e3b3101080294b2f6cdeb39882
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863153"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Planen for det globale adressekartotek og andre adressekartoteker

[!include [banner](../includes/banner.md)]

Denne artikel beskriver de overvejelser og de beslutninger, du skal foretage i planlægningsprocessen, før du opsætter og konfigurerer det globale adressekartotek og eventuelle supplerende adressekartoteker. Nogle af afgørelser kræver, at du bekræfter de beslutninger, der er foretaget på andre områder for produktet, f.eks. organisationshierarkiet.

## <a name="global-address-book"></a>Globalt adressekartotek

Før du begynder at arbejde med det globale adressekartotek, skal du bestemme standardværdierne for det. Disse værdier bruges derefter til eventuelle yderligere adressekartoteker, du opretter.

**Beslutninger**

- I hvilken rækkefølge skal navne vises i, for partposter af typen **Person**? Én sekvens er f.eks. efternavn, mellemnavn, fornavn.
- Skal partposter slettes fra adressekartoteket, når rolleposten slettes? Hvis f.eks. en kundepost slettes, skal partposten også slettes?
- Når der oprettes en ny post, skal brugerne så have besked, hvis der findes en dubletpost i det globale adressekartotek?
- Skal DUNS-nummeret (Data Universal Numbering System) inkluderes i oplysningerne om en partpost?
- Hvis DUNS-nummeret er medtaget i en partpost, bør tallets entydighed så kontrolleres?
- Når en partpost oprettes i det globale adressekartotek, vil du så have en standard for parttype, person eller organisation?
- Hvilke brugerroller skal have adgang til private adresser og kontaktoplysninger for partposten?

## <a name="additional-address-books"></a>Yderligere adressekartoteker

Når du opretter det globale adressekartotek, kan du oprette yderligere adressekartoteker, du ønsker, som et separat adressekartotek for hvert firma i organisationen eller for hvert forretningsområde. Fabrikam er f.eks. en international organisation, der har flere firmaer og flere forretningsområder. Fabrikam planlægger at oprette et adressekartotek for hvert forretningsområde. Til forretningsområder, der findes på mere end én lokalitet, f.eks. trykluftsværktøj, planlægger Fabrikam at oprette et adressekartotek for hver enkelt lokalitet. Chris, it-leder hos Fabrikam, har oprettet følgende liste over adressekartoteker, der kræves. Denne liste beskriver også de partposter, som hver enkelt adressekartotek skal indeholde.

- **Offentlig sektor-kontrakter (OffSK)** – partposter for alle parter, der er involveret i de kontrakter med den offentlige sektor, som Fabrikam har.
- **Privat sektor-kontrakter (PriSK)** – partposter for alle parter, der er involveret i de kontrakter med den private sektor, som Fabrikam har.
- **Elektroniske værktøjer (EV)** – partposter for alle parter, der er involveret i køb eller salg af elektroniske værktøjer, eller som på anden måde har noget at gøre med de elektroniske værktøjer, der stilles til rådighed af eller købes til Fabrikam i Fabrikams firma i Japan.
- **Trykluftsværktøj (TVJPN)** – partposter for alle parter, der er involveret i køb eller salg af trykluftsværktøj, eller som på anden måde har noget at gøre med det trykluftsværktøj, der stilles til rådighed af eller købes til Fabrikam i Fabrikams firma i Japan.
- **Trykluftsværktøj (TVUSA)** – partposter for alle parter, der er involveret i køb eller salg af trykluftsværktøj, eller som på anden måde har noget at gøre med det trykluftsværktøj, der stilles til rådighed af eller købes til Fabrikam i Fabrikams firma i USA.

**Beslutning:**

- Hvor mange yderligere adressekartoteker vil du oprette?


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]