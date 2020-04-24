---
title: Oprette indkøbspolitikker
description: Dette emne viser, hvordan du opretter indkøbspolitikker, der skal justeres med dine forretningsprocesser til indkøb.
author: mkirknel
manager: tfehr
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e13a9a594e8c4041a586734df53321d57b43586
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204786"
---
# <a name="create-purchasing-policies"></a>Oprette indkøbspolitikker

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du opretter indkøbspolitikker, der skal justeres med dine forretningsprocesser til indkøb. Før du kan oprette indkøbspolitikker, skal du konfigurere parametrene for indkøbspolitikker. Det er muligt at oprette, redigere og trække en indkøbspolitik tilbage, men du kan ikke slette en indkøbspolitik. Denne procedure vil typisk blive udført af en indkøbschef. Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.


## <a name="set-up-policy-parameters"></a>Konfigurere politikparametre
1. I navigationsruden skal du gå til **Moduler > Indkøb og forsyning > Opsætning > Politikker > Indkøbspolitikker**.
2. Gå til handlingsruden, og vælg **Parametre**.
- Prioriteringsregler for politikker gælder for forskellige niveauer i organisationen. De organisatoriske enheder, der vises, afhænger af organisationshierarkiet, og på hvilke niveauer i hierarkiet der er tildelt formål med intern kontrol af indkøb. Organisationen kan f.eks. have juridiske enheder, bærere, områder og afdelinger, men det kan være, at kun nogle af dem har et hierarkiformål for intern kontrol af indkøb. Som standard er organisationen af typen Firma tilgængelig.  
3. Vælg fanen **Parametre for regeltypen**.
4. Gå til **Indkøbspolitik > Regel for styring af indkøbsrekvisition** i træet.
- Du kan angive prioriterede rækkefølge for løsning af politikker på politikniveau. For nogle politiktyper kan du dog tilsidesætte den prioriterede rækkefølge for enkelte politikregeltyper. Du kan f.eks. definere den prioriterede rækkefølge for indkøbspolitikker til at være: bærer, afdeling, firma. For katalogpolitikreglen skal den prioriterede rækkefølge måske være følgende: afdeling, bærer, firma. Du kan ændre den prioriterede rækkefølge for katalogpolitikreglen. Når en arbejder opretter en rekvisition, bestemmes det viste katalog af de politikker, der er tilknyttet arbejderens afdeling, derefter bæreren og derefter firmaet.  
- Hvis der vises mere end ét organisationsniveau, kan du bruge op/ned-pilene til at angive den prioriterede rækkefølge for reglen for styring af indkøbsrekvisition.  
5. Luk siden.

## <a name="create-a-new-policy"></a>Opret en ny politik
1. Vælg **Ny**.
2. Skriv en værdi i feltet **Navn**.
3. Indtast en værdi i feltet **Beskrivelse**.
- En enkelt indkøbspolitik kan kun anvendes til ét organisationshierarki. Du kan f.eks. have ét hierarki, der kaldes "Geografisk", og et, der kaldes "Afdeling", og have en forskellige indkøbspolitik for hver af dem.  
- Vælg en organisation, som politikken skal gælde for.  
4. Vælg pilen for at tilføje den valgte organisation.
- Du kan gentage denne proces for at føje flere organisationer.  

## <a name="add-a-policy-rule"></a>Tilføj en politikregel
1. Vælg **Regel for rekvisitionsformål** på listen **Regeltype**.
- Du opretter en regel, der angiver formålet med standardrekvisitionen til typen Forbrug, men tillader, at typen Opfyldning vælges i stedet.  
2. Vælg **Opret politikregel**.
3. Vælg **Ja** i feltet **Tillad manuel tilsidesættelse**.
4. Vælg **Luk**.
- Du kan nu konfigurere andre politikregler for indkøbspolitikken. Bemærk, at en politikregeltype ikke kan have overlappende regler, der er aktive på samme tid i en enkelt indkøbspolitik.  

