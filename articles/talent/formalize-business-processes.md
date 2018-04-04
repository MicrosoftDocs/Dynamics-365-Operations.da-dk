---
title: Formalisere forretningsprocesser
description: "Funktionen til forretningsprocesser giver dig mulighed for at oprette en skabelon til forretningsproces til processer, der skal fuldføres inden for organisationen."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: 48f80eac5009e1a241d501b0c4a3a70b78f5d709
ms.contentlocale: da-dk
ms.lasthandoff: 03/23/2018

---
# <a name="formalize-business-processes"></a>Formalisere forretningsprocesser
Funktionen til forretningsprocesser giver dig mulighed for at oprette en skabelon til forretningsproces til processer, der skal fuldføres inden for organisationen. Dit firma udfører f.eks. en HR revision hvert år. Der kan oprettes en skabelon til at spore alle de opgaver, som revisionen består af, for at sikre at alle opgaver er udført, hver gang processen er fuldført, og om nødvendigt for at sikre, at opgaver udføres i den rigtige rækkefølge. Skabeloner kan bruges igen til gentagne processer eller kopieres for at blive brugt som udgangspunkt ved oprettelsen af nye.

Når der oprettes en skabelon, kan en proces startes og spores i arbejdsområdet Forretningsproces.  Når der startes en forretningsproces, tildeles der opgaver til de relevante personer opgaverne, og der angives en forfaldsdato. Vi dækker disse komponenter detaljeret nedenfor.

## <a name="business-process-template"></a>Forretningsprocesskabelon
En forretningsprocesskabelon indeholder en gruppe opgaver, der udgør en forretningsproces. Personalechefer og -assistenter kan som standard oprette forretningsprocesser.  Dette kan dog ændres i sikkerhedskonfigurationen ved at redigere pligten Vedligehold generiske forretningsprocesser.

Der kan defineres en procesejer for hver proces.  Procesejeren har overblik over alle opgaver for processen og kan tildele opgaver igen eller ændre forfaldsdatoer.  Personaledirektøren kan f.eks. oprette en forretningsprocesskabelon for en gennemgang af frynsegoder.  Chef for kompensation og frynsegoder kan angives som ejeren af processen, så vedkommende kan få indsigt i de opgaver, der skal fuldføres som en del af gennemgangen.  En procesejer kan ikke oprette eller slette aktive forretningsprocesser eller forretningsprocesskabeloner.

## <a name="task"></a>Opgave
En forretningsproces består ofte af flere opgaver. Nogle opgaver kan udføres inden for Dynamics 365 for Talent[?], f.eks. gennemgang af interne kursustilbud. I dette tilfælde kan der vælges et menupunkt i feltet Opgavelink. Andre opgaver kan omfatte gennemgang eller udfyldelse af formularer på et websted. Hvis du vælger URL-adresse i feltet Opgavelink kan webadressen angives. Du kan angive URL-adresser for både eksterne og interne websteder i dette felt. Du kan også oprette opgaver for aktiviteter, der udføres manuelt, f.eks. gennemsyn af adgangen til alle strukturer. I dette tilfælde er en opgavekæde ikke påkrævet. Denne fleksibilitet gør det muligt at spore flere typer opgaver i en omfattende proces.

Opgaver kan tildeles til en bestemt arbejder eller til en stilling. For eksempel vil chefen for kompensation og frynsegoder altid være den person, der udfører en gennemgang af forsikringspræmier.   Når du opretter denne opgave, skal du vælge Stilling som Tildelingstypen og derefter vælge chefen for kompensation og frynsegoder på listen Stilling. Når processen begynder, tildeles opgaven til den medarbejder, der har stillingen chef for kompensation og frynsegoder. Du kan også tildele en opgave til en bestemt arbejder ved at vælge arbejderen i feltet Tildelingstype og derefter vælge den relevante person.

Forfaldsdatoer for opgaven er afhængig af den måldato, der er angivet i starten af processen. Nogle opgaver skal fuldføres før måldatoen, og nogle kan muligvis udføres efter måldatoen.  Når du definerer en opgave, angiver du en relativ forfaldsdato i forhold til måldatoen i feltet Forskydning af forfaldsdato fra måldato. Antag for eksempel, at chefen for kompensation og frynsegoder skal foretage en gennemgang af forsikringspræmier, 10 dage før HR-revisionen er fuldført. Den oprettede opgave har en forfaldsdato i forhold til måldatoen på -10. Hvis processen derfor er startet den 13. maj, er opgaven forfalden den 3. maj. Bemærk: Forfaldsdatoer kan også justeres, når processen er startet.

Komplekse opgaver kan kræve flere trin, eller der er behov for, at den person, der udfører opgaver, skal angive yderligere oplysninger. Du kan føje instruktioner til opgaven og desuden foretage RTF-formatering af instruktionerne. Instruktionerne kan give yderligere oplysninger om, hvordan opgaven skal fuldføres, til den person, der er tildelt til at gennemføre den.

Starte en proces. En proces kan startes fra en forretningsprocesskabelon ved at vælge Start proces.  Når en proces er startet, oprettes opgaver for de valgte arbejdere og/eller stillinger, der er defineret i de opgaver, der er inkluderet i forretningsprocesskabelonen. En forfaldsdato tildeles også til hver opgave ved at tilføje eller fratrække forskydningsdagene fra måldatoen (se oplysningerne om forskydningsdage i afsnittet Opgave). De aktive forretningsprocesser kan ses i arbejdsområdet Forretningsprocesser. 

## <a name="employee-self-service"></a>Medarbejderselvbetjening
Når en opgave er tildelt til en medarbejder, kan vedkommendes tildelte opgaver ses på siden Medarbejderselvbetjening. Medarbejdere, der har en forretningsprocesopgave knyttet til sig, kan se opgaven, dens beskrivelse, instruktioner til at fuldførelse og navnet på en kontaktperson, og de kan åbne den tilknyttede Dynamics365-side eller -webside fra deres side Medarbejderselvbetjening. Opgaver kan markeres som igangværende, annullerede eller fuldførte.

## <a name="business-process-workspace"></a>Arbejdsområdet Forretningsproces
Personalemedarbejdere kan se de aktive forretningsprocesser i arbejdsområdet Forretningsproces. Arbejdsområdet viser alle aktive processer og de opgaver, der er tilknyttet hver enkelt. Den omfattende opgaveliste kan filtreres efter forfaldsdato. Siden viser også forfaldne opgaver og opgaver, der specifikt er tildelt til personalemedarbejderen. De kan også opdatere status for alle opgaver og kan om nødvendigt tildele opgaver til andre for at sørge for at den overordnede forretningsproces bevæger sig fremad.

## <a name="my-business-processes-workspace"></a>Arbejdsområdet Mine forretningsprocesser
Procesejere kan få vist de aktive forretningsprocesser, der er tildelt dem, fra arbejdsområdet Mine forretningsprocesser. Arbejdsområdet viser alle aktive processer og de tilknyttede opgaver, som den pågældende bruger ejer.  Den omfattende opgaveliste kan filtreres efter forfaldsdato. Siden viser også de opgaver, der specifikt er tildelt procesejer. Procesejeren kan også opdatere status for alle opgaver, samt omfordele alle opgaver.

## <a name="navigating-business-processes"></a>Navigere i forretningsprocesser
1.   Hvis du vil tilføje en forretningsprocesskabelon, skal du gå til Forretningsprocesser – Links – Administration af forretningsprocesser.
 - a.   Ny opretter en ny skabelon.
 - b.   Kopier fra skabelon kopierer den valgte skabelon til en ny.
 - c.   Start proces starter den valgte forretningsproces, tildelet opgaver og beregner forfaldsdatoer.  
2.  For at få vist aktive processer og tilknyttede opgaver skal du gå til arbejdsområdet Forretningsprocesser.

