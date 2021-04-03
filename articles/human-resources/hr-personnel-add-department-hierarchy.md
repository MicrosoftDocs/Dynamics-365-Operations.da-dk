---
title: Oprette afdelinger og knytte dem til afdelingshierarkiet
description: En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation. En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale. Du kan bruge afdelinger til at rapportere om funktionsområder. Afdelinger kan have ansvar for driftsregnskabet.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 723e46f98545e80551da9f79b6aeffc3eca48830
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466008"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Oprette afdelinger og knytte dem til afdelingshierarkiet

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation. En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale. Du kan bruge afdelinger til at rapportere om funktionsområder. Afdelinger kan have ansvar for driftsregnskabet.

En afdeling kan også omfatte en gruppe af bærere. Stillinger kan tildeles til afdelinger. For at oprette en afdeling skal du klikke på **Human Resources** &gt; **Afdelinger** &gt; **Afdeling**. I følgende tabel forklares de felter, der er tilgængelige.

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

1.  Klik på **Human Resources** &gt; **Afdelinger** &gt; **Afdelingshierarki**.
2.  Klik på **Rediger**, og vælg derefter den organisation, som afdelingen skal være under.
3.  Klik på **Indsæt**, og vælg **Afdeling** på listen.
4.  På listen over afdelinger, der vises, skal du vælge afdelingen til at føje den til hierarkiet.
5.  Gem ændringerne. Du modtager en meddelelse om, at der er oprettet en kladdeversion af hierarkiet.
6.  Når du er klar, skal du klikke på **Udgiv** i hierarkidesigner. Du kan angive en ikrafttrædelsesdato, der angiver, hvornår hierarkiet skal offentliggøres. Hvis du f.eks. vil tilføje en ny afdeling i starten af næste kalenderår, skal du sætte ikrafttrædelsesdatoen til 1. januar i det nye kalenderår. Ændringer af hierarkiet træder i kraft på denne dato.

## <a name="steps-for-creating-a-department"></a>Trin til oprettelse af en afdeling
Se artiklen [Definerere nye afdelinger](../fin-and-ops/hr/tasks/define-new-departments.md) for den trinvise procedure til at oprette en ny afdeling. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]