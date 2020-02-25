---
title: Konfigurere flekskreditprogrammer
description: Du kan bruge flekskreditprogrammer i Microsoft Dynamics 365 Human Resources til at tilmelde medarbejdere til frynsegoder i overensstemmelse med et foruddefineret antal flekskreditter.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitCreditPrograms
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d27d0f7f3f7e7db62b5d46b3b689d11194a85253
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008503"
---
# <a name="set-up-flex-credit-programs"></a>Konfigurere flekskreditprogrammer

[!include [banner](includes/preview-feature.md)]

Du kan bruge flekskreditprogrammer i Microsoft Dynamics 365 Human Resources til at tilmelde medarbejdere til frynsegoder i overensstemmelse med et foruddefineret antal flekskreditter. Medarbejderne kan vælge, hvordan deres flekskreditter skal fordeles. Hvis en medarbejder f.eks. er dækket af ægtefællens sundhedsforsikring, kan vedkommende evt. bruge de kreditter, der ellers ville være anvendt på sundhedsforsikring, til andre frynsegoder. 

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Flekskreditprogrammer** under **Planer**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | Frynsegodekredit-id | Det entydige id for flekskreditprogrammet. |
   | Beskrivelse | En beskrivelse af flekskreditprogrammet. | 
   | Fra-dato | Den dato og det klokkeslæt, hvor flekskreditprogrammet bliver aktivt. |
   | Til-dato | Slutdatoen for flekskreditprogrammet. Du kan beholde standardværdien (31/12/2154) for at angive, at der ikke er et planlagt udløb for flekskreditprogrammet. |
   | Kreditværdi i alt | Det antal kreditter, hver medarbejder skal bruge til deres frynsegoder. |
   | Regel for forholdsmæssig beregning | Den regel, der skal bruges til forholdsmæssig beregning af flekskreditter, når der ansættes en medarbejder midt i flekskreditperioden. </br></br><ul><li>**Ingen** – medarbejderen får ingen flekskreditter, hvis de er ansat efter starten på perioden for flekskreditprogrammet.</li><li>**Fuld kredit** – medarbejderen modtager det fulde beløb af flekskreditter, uanset hvornår de er ansat.</li><li>**Beregn forholdsmæssigt** – medarbejderen modtager et forholdsmæssigt beløb af flekskreditter baseret på deres startdato.</li></ul> |
   | Formel for forholdsmæssig beregning af flekskredit | Den regel, der skal bruges til forholdsmæssig beregning af flekskreditter for medarbejdere, som ansættes midt i en frynsegodeperiode for flekskreditprogrammet. Forholdsberegningen er baseret på ansættelsens startdato. Dette felt bruges kun, hvis du vælger **Beregn forholdsmæssigt** i feltet **Regel for forholdsmæssig beregning**. </br></br><ul><li>**Dagligt** – laver en forholdsmæssig beregning af det antal flekskreditter, en medarbejder modtager til dagsniveauet. Det samlede antal flekskreditter divideres med antallet af dage i perioden. Hvis din frynsegodeperiode f.eks. er 400 dage, vil systemet dividere det samlede antal flekskreditter med 400 for at beregne antallet af flekskreditter, som medarbejderne får pr. dag.</li><li>**Aktuel måned** – laver en forholdsmæssig beregning af flekskreditter, som en medarbejder modtager til månedsniveauet, afrundet til den aktuelle måned. Det samlede antal flekskreditter divideres med antallet af måneder i perioden. Hvis din frynsegodeperiode f.eks. er 15 måneder, vil systemet dividere det samlede antal flekskreditter med 15 for at beregne antallet af flekskreditter, som medarbejderne får pr. måned.</li><li>**Følgende måned** – laver en forholdsmæssig beregning af flekskreditter, som en medarbejder modtager til månedsniveauet, afrundet til den næste måned. Det samlede antal flekskreditter divideres med antallet af måneder i perioden. Hvis din frynsegodeperiode f.eks. er 15 måneder, dividerer systemet det samlede antal flekskreditter med 15 for at beregne antallet af flekskreditter, som medarbejderne får pr. måned.</li></ul> |
   
