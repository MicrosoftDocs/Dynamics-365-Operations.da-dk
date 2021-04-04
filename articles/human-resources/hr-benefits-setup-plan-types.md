---
title: Oprette plantyper
description: En plantype i Microsoft Dynamics 365 Human Resources er en overordnet gruppering af bestemte typer frynsegoder. Hver plantype har en plantypekode, der bestemmer reglerne for plantypen.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1d8db6900e6b697e988e2a7e9e31828b70e4ad0d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463906"
---
# <a name="create-plan-types"></a>Oprette plantyper

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

En plantype i Microsoft Dynamics 365 Human Resources er en overordnet gruppering af bestemte typer frynsegoder. Hver plantype har en plantypekode, der bestemmer reglerne for plantypen. Plantypen Basisliv har f.eks. plantypekoden Liv, fordi den er en slags livsforsikring, og den skal overholde de regler, der er fastsat for plantypekoden Liv. En anden plantype kan være Øvrigt liv, som også har plantypekoden Liv.

Hver enkelt plantype angiver, om en medarbejder kan tilmelde sig en eller flere af planerne af denne typen. En medarbejder kan f.eks. sandsynligvis tilmelde sig politikkerne for både Basisliv og Øvrige liv for plantypen Liv. En medarbejder må højst sandsynligt kun tilmeldes sig én politik af typen Medicinsk.

Hvis en plantype omfatter kontakter, angiver plantypen, om kontaktpersoner er modtagere eller afhængige. Plantypen Basisliv kan f.eks. have modtagere, mens plantypen Basis medicinsk ville have afhængige. I nogle tilfælde kan en plan ikke have personlige kontaktpersoner. Det kan f.eks. være en Fleksibel forbrugskonto eller Parkeringsgodtgørelse.

En plantype kan definere disponeringsindstillinger. Disponeringsindstillingerne defineres i formularen Disponeringsindstilling. En disponeringsindstilling kan angive beløbet for frynsegodet eller de kontakter, der er berettigede til plantypen. Hvis kontakttypen f.eks. er modtager, skal disponeringsindstillingen definere de betingelser, som modtageren er berettiget til at modtage, når frynsegodet bruges. Hvis kontakttypen er Afhængig, skal disponeringsindstillingen definere forholdet mellem den afhængige og medarbejderen. 

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Plantyper** under **Konfiguration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Plantype** | Et entydigt navn, der identificerer plantypen. |
   | **Beskrivelse** | En beskrivelse af plantypen. |
   | **Kode for plantype** | Vælg en plantypekode på rullelisten over værdier. Listen over plantypekoder viser alle de plantyper, der understøttes i den aktuelle version. |
   | **Samtidig tilmelding** | Angiver, om en medarbejder kan tilmelde sig flere frynsegodeplaner af samme plantype eller kun én frynsegodeplan pr. plantype. |
   | **Kontakttype** | Angiver rollen for den personlige kontakt. Værdierne er tom, Afhængig og Modtager. Du kan lade feltet **Kontakttype** være tomt, hvis deres plantype ikke kræver en afhængig eller modtager baseret på disponeringsindstillingen. |

4. Hvis du vil konfigurere indstillinger for livshændelser, skal du vælge **Handlinger** og derefter vælge **Indstillinger for livshændelser**. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Plantype** | Den plantype, der skal konfigureres indstillinger for livshændelser for. |
   | **Livshændelsestype-id** | Id'et for livshændelsestypen. |
   | **Tillad annullering** | Angiver, om en medarbejder kan annullere en frynsegodeplan under livshændelsen. |
   | **Skift dækningsindstilling** | Angiver, om en medarbejder kan ændre disponeringsindstillinger under livshændelsen. |
   | **Skift til en ny plan** | Angiver, om en medarbejder kan ændre planer under livshændelsen. |
   | **Annuller plan automatisk** | Angiver, om planen automatisk skal annulleres under livshændelsen. |
   | **Åbn automatisk kontrol af berettigelse** | Angiver, om kontrollen for berettigelse til frynsegoder ved tilmelding skal genåbnes automatisk under livshændelsen. |
   | **Rapporteringsvindue** | Angiver rapporteringsvinduet, i dage, for livshændelsen. **Bemærk!** Hvis du ikke indtaster et beløb, antager systemet, at rapporteringsvinduet skal være nul, og livshændelsen behandles ikke. |

5. Vælg **Gem**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]