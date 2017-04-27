---
title: "Justere arbejdsstyrkens færdigheder med virksomhedens behov"
description: "Du kan spore færdigheder, som arbejdere, ansøgere eller kontakter har eller bør have for at udfylde deres roller effektivt. Du kan også angive de færdigheder, der kræves til et bestemt job."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 720a1f272948eb310dc3cd02588aeec40b556d20
ms.openlocfilehash: 31dda85ff2e4a4e5380401b031b2dd74acff394b
ms.lasthandoff: 03/31/2017


---

# <a name="align-workforce-skills-with-business-needs"></a>Justere arbejdsstyrkens færdigheder med virksomhedens behov

Du kan spore færdigheder, som arbejdere, ansøgere eller kontakter har eller bør have for at udfylde deres roller effektivt. Du kan også angive de færdigheder, der kræves til et bestemt job.

Eksempler på færdigheder, du kan spore, omfatter følgende:
-   Supervision – evnen til at føre tilsyn med andres arbejde.
-   Ledelse – evnen til at lede medarbejdere og forretningsområder.
-   Planlægning – evnen til at se fremad, formulere visioner og få dem gennemført.
-   HTML – evnen til at skrive HTML-kode.

Før du kan tildele en færdighed til en person eller et job, oprette en kompetencesøgning eller oprette en kompetenceprofil, skal du angive oplysninger om færdigheder på siden **Færdigheder**. Du kan vælge en færdighedstype og en rangeringsmodel for hver færdighed.

## <a name="rating-models"></a>Klassifikationsmodeller
Rangeringsmodeller er en hjælp til at evaluere en persons faktiske færdighedsniveau, det niveau de skal tilsigte, eller det færdighedsniveau, der kræves til et job. Du kan angive op til ti niveauer til en rangeringsmodel.  Hvert niveau i en klassifikationsmodel er tildelt en faktor.  Faktorværdien bruges til at normalisere resultaterne af færdigheder, der bruger forskellige klassifikationsmodeller.  Faktoren skal være et tal mellem 0-9, og hvert niveau skal have en entydig faktor.  Niveauer med højere faktorværdier vægter mere i rangeringsmodellen.

## <a name="specify-job-skills"></a>Angive jobfærdigheder
Når du indtaster oplysninger om et job, kan du angive de færdigheder, en person skal have for at kunne udføre det arbejde, der kræves til jobbet.  Desuden kan du angive det ønskede niveau for hver færdighed samt vigtighedsniveauet for færdigheden. Forskellige job kan have forskellige krav til vigtighedsniveau for den samme færdighed.

## <a name="enter-skills-for-workers-applicants-or-contacts"></a>Angiv færdigheder for arbejdere, ansøgere eller kontakter
Du kan angive målfærdigheder eller reelle færdigheder for arbejdere, ansøgere eller kontakter. En målfærdighed er en færdighed, som en person har til hensigt at opnå. En reel færdighed er en færdighed, som en person har i øjeblikket.

## <a name="skill-mapping-and-skill-mapping-profiles"></a> Konfigurere kompetencesøgning og profiler for kompetencesøgning
Du kan oprette en kompetencesøgning for at finde en medarbejder, ansøger eller kontaktperson, der er kvalificeret til at udføre en bestemt type opgave. Kompetencesøgninger søger på tværs af kvalifikationer, uddannelse, certifikater, tillidsposter og projekterfaring og returnerer et resultat, der svarer til de kriterier, der er angivet.  Det kan f.eks. være nyttigt at vide, hvilke arbejdere i organisationen, der har oparbejdet deres CPA.

Ved hjælp af kompetencesøgningsprofiler kan du finde aktuelle medarbejdere eller ansøgere med kvalifikationer, der svarer direkte til virksomhedens behov.  Du kan f.eks. oprette en kompetencesøgningsprofil til en ledig stilling i organisationen. Ved at oprette en profil for et bestemt job og kopiere færdigheder, uddannelse og certifikater fra dette job til profilen kan du hurtigt søge efter arbejdere, ansøgere og kontakter, der opfylder et eller flere af de kriterier, der er angivet i profilen, og se en liste over de ansøgere, hvis kvalifikationer bedst svarer de færdigheder, der kræves for jobbet.

<table>
<thead>
<tr class="header">
<th><strong>Bemærk! </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Det er kun arbejdere, ansøgere og kontaktpersoner, som du har valgt til at indgå i kompetencesøgninger, der kan vises på en resultatliste for kompetencesøgning eller indgå i en kompetenceprofil. Hvis du vil medtage en medarbejder, ansøger eller kontakt i kompetencesøgninger, skal du angive <strong>Medtag i kompetencetilknytning</strong> til Ja på de følgende sider:
<ul>
<li>Arbejdstråd</li>
<li>Medarbejder</li>
<li>Ansøger</li>
<li>Kontaktpersoner</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a>Analyse af kompetencekløft og kompetenceprofilanalyse
Du kan oprette en kompetenceprofilanalyse for at få vist en liste over en arbejders, ansøgers eller kontakts færdigheder pr. en bestemt dato. Oprette en analyse af kompetencekløft for at sammenligne en persons færdigheder med de færdigheder, der kræves til et bestemt job.  



<a name="see-also"></a>Se også
--------

[Personale](index.md)


