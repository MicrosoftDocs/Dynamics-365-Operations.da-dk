---
title: Oversigt over plantype
description: En plantype i Microsoft Dynamics 365 Human Resources er en overordnet gruppering af bestemte typer frynsegoder. Hver plantype har en plantypekode, der bestemmer reglerne for plantypen.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8966b0aa01795ff00832e480a186c05fa129e7c728112f81cf4f78b6b0915463
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732723"
---
# <a name="plan-type-overview"></a>Oversigt over plantype

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

En plantype er en overordnet gruppering af bestemte typer frynsegoder. Hver plantype har en plantypekode, der bestemmer reglerne for plantypen. Plantypen **Basisliv** har f.eks. plantypekoden **Liv**, fordi den er en slags livsforsikringsplan og skal overholde de regler, der er fastsat for plantypekoden **Liv**. En anden plantype kan være **Supplerende liv**. Denne plantype vil også have plantypekoden **Liv**.

Hver enkelt plantype angiver, om en medarbejder kan tilmelde sig en eller flere af planerne af denne typen. En medarbejder kan f.eks. sandsynligvis tilmelde sig politikkerne for både Basisliv og Øvrige liv for plantypen Liv. En medarbejder må højst sandsynligt kun tilmeldes sig én politik af typen Medicinsk.

Hvis en plantype omfatter kontakter, angiver plantypen, om kontaktpersoner er modtagere eller afhængige. Plantypen Basisliv kan f.eks. have modtagere, mens plantypen Basis medicinsk ville have afhængige. I nogle tilfælde kan en plan ikke have personlige kontaktpersoner. Det kan f.eks. være en Fleksibel forbrugskonto eller Parkeringsgodtgørelse.

En plantype kan definere disponeringsindstillinger. Disponeringsindstillingerne defineres i formularen Disponeringsindstilling. En disponeringsindstilling kan angive beløbet for frynsegodet eller de kontakter, der er berettigede til plantypen. Hvis kontakttypen f.eks. er modtager, skal disponeringsindstillingen definere de betingelser, som modtageren er berettiget til at modtage, når frynsegodet bruges. Hvis kontakttypen er Afhængig, skal disponeringsindstillingen definere forholdet mellem den afhængige og medarbejderen. 

> [!IMPORTANT]
> Formularen indeholder nøgledata, der påvirker de tilgængelige muligheder ved oprettelse af en ny frynsegodeplan:
>
> - **Plantypekode** – Dette felt påvirker, hvad der vises under fanen **Konfiguration**, når den faktiske frynsegode konfigureres.  
> - **Samtidig tilmelding** – Dette felt bestemmer, om der tillades flere tilmeldinger. (For en sundhedsplan angives dette felt typisk til **Én tilmelding**).
> - **Kontakttype** – Dette felt gør det muligt at føje afhængige eller modtagere til en plan. Hvis den er angivet til **Ingen**, har medarbejdere, der tilmeldes fryndegoder, ikke mulighed for at vælge en modtager eller en afhængig.
> - **Dækningsindstillinger** – Brug dette felt til at sammenkæde dækningsmulighederne med plantyperne. Den definerer enten de personer, der vil blive dækket af denne plantype, eller de dækningsbeløb, der er tilgængelige for denne plantype. Du kan f.eks. angive, at dækningen for en sundhedsforsikringstype kun vil være tilgængelig for medarbejderen, medarbejderen og en anden person eller medarbejderen og dennes familie.

## <a name="create-plan-types"></a>Oprette plantyper

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
