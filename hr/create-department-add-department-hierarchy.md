---
title: Oprette en afdeling og knytte den til afdelingshierarkiet
description: "En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation. En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale. Du kan bruge afdelinger til at rapportere om funktionsområder. Afdelinger kan have ansvar for driftsregnskabet."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ee51abe108b3bc0aabc764b991222db6d185e532
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a>Oprette en afdeling og knytte den til afdelingshierarkiet

En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation. En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale. Du kan bruge afdelinger til at rapportere om funktionsområder. Afdelinger kan have ansvar for driftsregnskabet.

En afdeling kan også omfatte en gruppe af bærere. Stillinger kan tildeles til afdelinger. Klik for at oprette en afdeling, **personale**&gt;**afdelinger**&gt;**afdeling**. I følgende tabel beskrives de felter, der er tilgængelige.

| Felt               | Beskrivelse                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Navn                | Angiv et navn for afdelingen.                                                                                                                                                                                  |
| Afdelingsnummer   | Der kan automatisk genereres en standardværdi, hvis der er knyttet en nummerseriekode til referencen for **Organisationsnummer** på siden **Nummerserier**.                                                 |
| Søgenavn         | Angiv et navn eller et akronym, der kan bruges til en hurtig søgning efter afdelingen.                                                                                                                                            |
| Notat                | Angiv yderligere oplysninger her.                                                                                                                                                                            |
| I hierarki        | Et markeret afkrydsningsfelt angiver, at en afdeling er medtaget i afdelingshierarkiet. Du kan finde oplysninger om, hvordan du føjer en afdeling til afdelingshierarkiet senere i denne artikel. |
| DUNS-nummer         | DUNS står for Data Universal Number System. Dette er et 9-cifret tal, der er udstedt af Dun & Bradstreet.                                                                                                     |
| Leder             | Angiv den karakter, der administrerer afdelingen.                                                                                                                                                                    |
| Adresser           | Tilføj afdelingens adresseoplysninger. Tilføj f.eks. postadressen for den bygning, som afdelingen findes i.                                                                          |
| Kontaktoplysninger | Tilføj kontaktoplysninger afdelingen. Du kan f.eks. føje et telefonnummer til afdelingens helpdesk.                                                                                           |

Følg disse trin for at føje en afdeling til afdelingshierarkiet.

1.  Klik på **personale**&gt;**afdelinger**&gt;**afdelingshierarkiet**.
2.  Klik på **Rediger**, og vælg derefter den organisation, som afdelingen skal være under.
3.  Klik på **Indsæt**, og vælg **Afdeling** på listen.
4.  På listen over afdelinger, der vises, skal du vælge afdelingen til at føje den til hierarkiet.
5.  Gem ændringerne. Du modtager en meddelelse, der er oprettet en kladdeversion af hierarkiet.
6.  Når du er klar, skal du klikke på **Udgiv** i hierarkidesigner. Du kan angive en ikrafttrædelsesdato, der angiver, hvornår hierarkiet bør offentliggøres. Hvis du f.eks. vil tilføje en ny afdeling i starten af næste kalenderår, skal du sætte ikrafttrædelsesdatoen til 1. januar i det nye kalenderår. Ændringer af hierarkiet træder i kraft på denne dato.



