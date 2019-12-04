---
title: Formalisere forretningsprocesser
description: I dette emne forklares det, hvordan du kan bruge funktionen til forretningsprocesser til at oprette en skabelon til forretningsproces til processer, der skal fuldføres inden for organisationen.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.openlocfilehash: 2a245891e2e3e8c0eae4f28d0932776c3ee976dc
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832809"
---
# <a name="formalize-business-processes"></a>Formalisere forretningsprocesser

[!include [banner](includes/banner.md)]

Funktionen til forretningsprocesser giver dig mulighed for at oprette en skabelon til forretningsproces til processer, der skal fuldføres i organisationen. Virksomheden udfører f.eks. en revision af personale (HR) hvert år. I så fald kan du oprette en skabelon, der sporer alle de opgaver, revisionsprocessen består af. Denne skabelon kan hjælpe med til at sikre, at alle opgaver er udført, hver gang revisionen udføres. Hvis opgaverne skal fuldføres i en bestemt rækkefølge, kan skabelonen desuden hjælpe med til at sikre, at de udføres i den rigtige rækkefølge.

Skabeloner kan genbruges til gentagne processer. De kan også kopieres og bruges som udgangspunkt til at oprette nye skabeloner.

Når der oprettes en forretningsprocesskabelon, kan en forretningsproces startes og spores i arbejdsområdet **Forretningsproces**. Når der startes en forretningsproces, tildeles der opgaver til de relevante personer, og opgaverne indeholder en forfaldsdato.

## <a name="business-process-templates"></a>Forretningsprocesskabeloner
En forretningsprocesskabelon indeholder en gruppe opgaver, der udgør en forretningsproces. Personalechefer og -assistenter kan som standard oprette forretningsprocesser. Du kan dog ændre de roller, der kan oprette forretningsprocesser ved at ændre pligten **Vedligehold generiske forretningsprocesser** i sikkerhedskonfigurationen.

For hver forretningsproces kan du definere en procesejer. Procesejeren har overblik over alle opgaver for processen og kan tildele opgaver igen eller ændre forfaldsdatoer. Personaledirektøren opretter f.eks. forretningsprocesskabelon til gennemgang af frynsegoder og angiver chefen for kompensation og frynsegoder som procesejeren. Chefen for kompensation og frynsegoder har derefter indsigt i de opgaver, der skal udføres som en del af gennemgangen.

En procesejer kan ikke oprette nye forretningsprocesser eller forretningsprocesskabeloner eller slette aktive forretningsprocesser eller forretningsprocesskabeloner.

## <a name="tasks"></a>Opgaver
En forretningsproces består ofte af flere opgaver. Nogle opgaver, f.eks. gennemgang af interne kursustilbud, kan udføres i Microsoft Dynamics 365 Talent. I så fald vælges en indstilling i feltet **Opgavelink**. Andre opgaver kan omfatte gennemgang eller udfyldelse af sider på et websted. I dette tilfælde er **URL-adressen** valgt i feltet **Opgavelink**, og webadressen kan derefter angives. Du kan angive URL-adresser for både eksterne og interne websteder. Du kan også oprette opgaver for aktiviteter, der udføres manuelt, f.eks. et gennemsyn af adgangen til alle strukturer. I dette tilfælde er et opgavelink ikke påkrævet. Denne fleksibilitet gør det muligt at spore flere typer opgaver i en omfattende proces.

Opgaver kan enten tildeles til en bestemt arbejder eller til en stilling. For eksempel vil chefen for kompensation og frynsegoder altid være den person, der udfører en gennemgang af forsikringspræmier. Når du opretter denne opgave, skal du derfor vælge **Stilling** i feltet **Tildelingstype** og derefter vælge **Chef for kompensation og frynsegoder** på listen **Stilling**. Når forretningsprocessen startes, tildeles opgaven til den medarbejder, der har stillingen **Chef for kompensation og frynsegoder**. Hvis du vil tildele en opgave til en bestemt arbejder, skal du vælge **Arbejder** i feltet **Tildelingstype** og derefter vælge den relevante person.

Forfaldsdatoer for opgaver afhænger af den måldato, der er angivet ved starten af forretningsprocessen. Nogle opgaver skal fuldføres før måldatoen, og andre opgaver kan muligvis fuldføres efter måldatoen. Når du definerer en opgave, skal du angive en relativ forfaldsdato i forhold til måldatoen i feltet **Forskydning af forfaldsdato fra måldato**. F.eks. skal chefen for kompensation og frynsegoder foretage en gennemgang af forsikringspræmier, 10 dage før HR-revisionen er fuldført. I dette tilfælde har den opgave, der oprettes til en gennemgang, en værdi i feltet **Forskydning af forfaldsdato fra måldato** på **-10**. Hvis forretningsprocessen derfor er startet den 13. maj, er opgaven forfalden den 3. maj.

> [!NOTE]
> Forfaldsdatoer kan også justeres, når forretningsprocessen er startet.

Komplekse opgaver kan kræve flere trin, eller de personer, der udfører opgaverne, skal måske angive yderligere oplysninger. Du kan tilføje instruktioner til en opgave for disse scenarier. Instruktionerne kan give den person, der er tildelt til at fuldføre opgaven, yderligere oplysninger om, hvordan opgaven skal fuldføres. Du kan også medtage RTF-formatering i instruktionerne.

## <a name="starting-a-business-process"></a>Starte en forretningsproces
En forretningsprocesskabelon kan du starte en forretningsproces ved at vælge **Start proces**. Når en proces er startet, oprettes opgaver for de valgte arbejdere og/eller stillinger, der er defineret i de opgaver, der er inkluderet i skabelonen. En forfaldsdato tildeles også til hver opgave ved at tilføje eller fratrække antallet af forskydningsdage fra måldatoen, som forklaret i afsnittet "Opgave". Du kan få vist aktive forretningsprocesser i arbejdsområdet **Forretningsprocesser**.

## <a name="employee-self-service"></a>Medarbejderselvbetjening
Når en opgave er tildelt til en medarbejder, kan medarbejderen få vist den og alle hans eller hendes andre tildelte opgaver på siden **Medarbejderselvbetjening**. For hver forretningsprocesopgave, der er tildelt ham eller hende, kan medarbejderen se navn og beskrivelse af opgaven, instruktioner til at fuldførelse af opgaven og navnet på en kontaktperson. Fra siden **Medarbejderselvbetjening** kan medarbejderen også åbne den tilknyttede side i Microsoft Dynamics 365 eller den tilknyttede webside og kan markere opgaver som igangværende, annullerede eller fuldførte.

## <a name="business-process-workspace"></a>Arbejdsområdet Forretningsproces
Personalemedarbejdere kan se de aktive forretningsprocesser i arbejdsområdet **Forretningsproces**. Dette arbejdsområde viser alle aktive processer og de opgaver, der er tilknyttet hver enkelt. Den omfattende opgaveliste kan filtreres efter forfaldsdato. Arbejdsområdet viser også forfaldne opgaver og opgaver, der specifikt er tildelt til personalemedarbejderen. Personalemedarbejderen kan også opdatere status for alle opgaver og kan om nødvendigt tildele opgaver til andre for at sørge for, at den overordnede forretningsproces bevæger sig fremad.

## <a name="my-business-processes-workspace"></a>Arbejdsområdet Mine forretningsprocesser
Procesejere kan få vist de aktive forretningsprocesser, der er tildelt dem, i arbejdsområdet **Mine forretningsprocesser**. Dette arbejdsområde viser alle aktive processer og de tilknyttede opgaver, som den pågældende bruger ejer. Den omfattende opgaveliste kan filtreres efter forfaldsdato. Arbejdsområdet viser også forfaldne opgaver og opgaver, der specifikt er tildelt til procesejeren. Procesejeren kan også opdatere status for alle opgaver og omfordele alle opgaver.

## <a name="navigating-business-processes"></a>Navigere i forretningsprocesser
Hvis du vil oprette eller kopiere en forretningsprocesskabelon eller starte en forretningsproces, skal du gå til Forretningsprocesser - Links – Administration af forretningsprocesser. Du kan derefter udføre følgende opgaver:

- Vælg **Ny** for at oprette en ny forretningsprocesskabelon.
- Vælg **Kopier fra skabelon** for at kopiere den valgte skabelon til en ny skabelon.
- Vælg **Start proces** for at starte den valgte forretningsproces, tildele opgaver og beregne forfaldsdatoer.

For at få vist aktive processer og tilknyttede opgaver skal du åbne arbejdsområdet **Forretningsprocesser**.

