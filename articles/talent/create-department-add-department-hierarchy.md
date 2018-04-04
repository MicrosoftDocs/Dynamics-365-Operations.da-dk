---
title: Oprette en afdeling og knytte den til afdelingshierarkiet
description: "En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation. En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale. Du kan bruge afdelinger til at rapportere om funktionsområder. Afdelinger kan have ansvar for driftsregnskabet."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: 3fc30669bf7a16616484bf7115cb121ce463840f
ms.contentlocale: da-dk
ms.lasthandoff: 03/23/2018

---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a>Oprette en afdeling og knytte den til afdelingshierarkiet

[!include[banner](includes/banner.md)]


En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation. En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale. Du kan bruge afdelinger til at rapportere om funktionsområder. Afdelinger kan have ansvar for driftsregnskabet.

En afdeling kan også omfatte en gruppe af bærere. Stillinger kan tildeles til afdelinger. For at oprette en afdeling skal du klikke på **Personale** &gt; **Afdelinger** &gt; **Afdeling**. I følgende tabel forklares de felter, der er tilgængelige.

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

1.  Klik på **Personale** &gt; **Afdelinger** &gt; **Afdelingshierarki**.
2.  Klik på **Rediger**, og vælg derefter den organisation, som afdelingen skal være under.
3.  Klik på **Indsæt**, og vælg **Afdeling** på listen.
4.  På listen over afdelinger, der vises, skal du vælge afdelingen til at føje den til hierarkiet.
5.  Gem ændringerne. Du modtager en meddelelse om, at der er oprettet en kladdeversion af hierarkiet.
6.  Når du er klar, skal du klikke på **Udgiv** i hierarkidesigner. Du kan angive en ikrafttrædelsesdato, der angiver, hvornår hierarkiet skal offentliggøres. Hvis du f.eks. vil tilføje en ny afdeling i starten af næste kalenderår, skal du sætte ikrafttrædelsesdatoen til 1. januar i det nye kalenderår. Ændringer af hierarkiet træder i kraft på denne dato.

## <a name="steps-for-creating-a-department"></a>Trin til oprettelse af en afdeling
Referere til emnet [Definerer nye afdelinger](../fin-and-ops/hr/tasks/define-new-departments.md) for den trinvise procedure til at oprette en ny afdeling. 

