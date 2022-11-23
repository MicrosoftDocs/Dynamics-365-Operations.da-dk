---
title: Begræns adgang til arbejdere efter juridisk enhed
description: I denne artikel forklares det, hvordan du kan konfigurere arbejderadgang efter juridisk enhed.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780387"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Begræns adgang til arbejdere efter juridisk enhed

I denne artikel forklares det, hvordan du kan konfigurere arbejderadgang efter juridisk enhed.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Medarbejdere er ansat i juridiske enheder. Her er nogle eksempler:

- Aaron Con er ansat i den juridiske enhed USSI.
- Ahmed Barnett er ansat i den juridiske enhed USMF.
- Alicia Thornber er ansat i de juridiske enheder GLSI og USMF.

Afhængigt af en brugers rolle i firmaet, kan det være nødvendigt at have adgang til at få vist alle medarbejdere på tværs af juridiske enheder. Alternativt kan det være, at en bruger skal begrænses, så den kun kan få vist medarbejdere i den juridiske enhed, som brugeren har adgang til. Hvis du vil styre, hvilke medarbejdere en bruger kan få vist, skal du vælge parameteren **Begræns adgang til arbejderoplysninger** på siden **Delte parametre for Personale**.

En bruger har f.eks. adgang til **arbejder**-siden og har kun adgang til den juridiske enhed USMF. I dette tilfælde kan brugeren få vist følgende oplysninger for medarbejderne på den foregående liste:

- Hvis funktionen til at begrænse adgangen til arbejderoplysninger ikke er aktiveret, kan brugeren få vist oplysningerne for Aaron, Ahmed og Alicia.
- Hvis funktionen er aktiveret, kan brugeren kun få vist oplysninger for Alicia og Ahmed, fordi de også er ansat i den juridiske enhed USMF.

De oplysninger, der vises, varierer, afhængigt af det program du bruger.

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources enkeltstående

Hvis funktionen til at begrænse adgangen til arbejderoplysninger er aktiveret, vil den begrænsede bruger få vist en tom værdi på nogle lister, der indeholder arbejderens navn.

En bruger har f.eks. adgang til den juridiske enhed USMF og kan opleve følgende opførsel:

- På listen **Aktive stillinger** er kolonnen **Arbejder** tom for Aarons stilling, fordi brugeren ikke har adgang til medarbejdere i den juridiske enhed USSI.
- Hvis brugeren rulles ned i arbejderens navn, vises en tom **arbejderside**.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources på finansinfrastruktur

Hvis funktionen til at begrænse adgangen til arbejderoplysninger er aktiveret, vil den begrænsede bruger få vist nogle lister, der indeholder arbejderens navn.

En bruger har f.eks. adgang til den juridiske enhed USMF og kan opleve følgende opførsel:

- På listen **Aktive stillinger** vises navnet Aaron på kolonnen **Arbejder**. Hvis brugeren peger på arbejderens navn, vises kun navnet og titlen.
- Hvis brugeren rulles ned i arbejderens navn, vises en tom **arbejderside**.

> [!TIP]
> Hvis du bruger Dynamics 365 Human Resources i finansinfrastruktur og ønsker, at begrænsede brugere skal se tomme værdier for arbejdernavne, kan du føje **Begræns adgang til arbejderes** sikkerhedsrettigheden til brugerrollerne på **sikkerhedskonfigurationssiden**.

Når du aktiverer denne funktion, skal du udfylde nogle ekstra trin for at angive tilladelser for hver af de brugere, hvis visning skal begrænses.

1. Vælg en bruger på siden **Brugere**.
2. Vælg en rolle for brugeren. Indstillingen **Tildel organisationer** bliver tilgængelig.
3. Vælg **Tildel organisationer**.
4. Vælg **Giv adgang til bestemte organisationer enkeltvis** på den nye side, og vælg derefter de organisationer, som brugeren skal have adgang til.
5. Gentag trin 2-4 for alle andre roller, brugeren har, herunder systembrugerrollen.

> [!NOTE]
> De juriske enheder, som en bruger har adgang til, skal matche på tværs af alle brugerens roller.
