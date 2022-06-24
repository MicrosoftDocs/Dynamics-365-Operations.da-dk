---
title: Stillinger
description: Denne artikel beskriver de grundlæggende elementer, som en stilling kan indeholde. Det indeholder også eksempler, der viser, hvordan du kan bruge disse elementer i organisationen.
author: twheeloc
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9c97a96e27188d12b9c5e626613e18d54d6632c0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888724"
---
# <a name="positions"></a>Stillinger


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver de grundlæggende elementer, som en stilling kan indeholde. Det indeholder også eksempler, der viser, hvordan du kan bruge disse elementer i organisationen.

Før du kan oprette en stilling, skal der konfigureres et job. Nogle stillingsoplysninger, for eksempel kompensationsområde, arbejdertildeling, stillingsvarighed og rapporteringsrelation, er datorelaterede.

## <a name="general-information"></a>Generelle oplysninger

Når du opretter en stilling, skal du vælge et job. Følgende oplysninger indsættes automatisk fra det job, du vælger:

- Betegnelse
- Stilling
- Fuldtidsækvivalent
- Jobserie

Stillingsbetegnelsen bruges til at referere til en medarbejders titel. (Den titel, der er angivet for medarbejderen, bruges ikke). Stillingsbetegnelserne skal derfor standardiseres så meget som muligt.

> [!NOTE]
> En arbejder kan ikke tildeles til en stilling på en dato, der ligger før den dato for, hvornår tildelingen er tilgængelig.
>
> En parameter under fanen **Stillinger** på siden **Delte parametre for Human Resources** styrer funktionsmåden for arbejdertildelingen. Vælg en af følgende værdier:
>
> - **Altid** – Du kan tildele arbejdere til nye stillinger, når stillingerne oprettes. Når der oprettes stillinger, angives dato og klokkeslæt for **Tilgængelig for tildeling** under fanen **Generelt** på siden **Stilling** automatisk til oprettelsesdatoen og -klokkeslættet.
> - **Aldrig** – Du kan ikke tildele arbejdere til nye stillinger, når stillingerne oprettes. Hvis du vælger denne indstilling, skal du åbne siden **Stilling** for hver ny stilling, efterhånden som den bliver tilgængelig. Derefter skal du gå til fanen **Generelt** og angive datoen **Tilgængelig for tildeling** for at aktivere arbejdertildeling. Hvis du vælger denne indstilling, angives datoen for arbejdertildeling som standard til **Aldrig**, når du prøver at tildele arbejderen.

## <a name="position-duration"></a>Stillings varighed

Hver enkelt stilling gælder i et bestemt tidsrum, som kaldes varigheden. Sommerjob har muligvis en varighed fra d. 1 maj 2021 indtil d. 31. august 2021. Aktiveringsdatoen er den dato, hvor stillingen bliver aktiv i systemet. Ophørsdatoen er den dato, hvor stillingen ikke længere er aktiv i systemet.

Bemærk, at hverken datoen for tilgængelig til tildeling eller arbejdertildelingsdatoen kan være før aktiveringsdatoen. En stilling anses ikke for at være aktiv, før aktiveringsdatoen er nået. Derudover kan en arbejdertildeling ikke udvides til efter stillingens ophørsdato.

## <a name="reports-to-position"></a>Rapporterer til-stilling

Stillinger er vigtige elementer i et organisationshierarkis lavere niveau. På siden **Stilling** kan du angive den stilling, en stilling rapporterer til. Når du tildeler en medarbejder til en stilling, der refererer til en anden stilling, opretter du en rapporteringsrelation mellem de arbejdere, der er tildelt til disse to stillinger. Stilling 000220 rapporterer for eksempel til stilling 000300. Kim Akers er tildelt stillingen 000220, og Sanjay Patel er tildelt stillingen 000300. Kim Akers rapporterer derfor til Sanjay Patel.

> [!TIP]
> Rapporterer til-stillingen bruges i hele systemet til at afgøre, hvem en medarbejders chef er. Hvis rollen som chef i det foregående eksempel er tildelt til Sanjay Patel i systemet, kan han se Kim Akers som en direkte underordnet i selvbetjening for ledere. Rapporteringsrelationen kan også bruges, når du opretter ruteregler for arbejdsgange og checklisteopgaver.

## <a name="relationships"></a>Relationer

Hvis organisationen bruger et matrixhierarki eller et andet brugerdefineret hierarki, kan du konfigurere stillingshierarkityper. Du kan derefter føje rapporteringsrelationer til stillinger for hver hierarkitype, du konfigurerer. Lori Penor er for eksempel administrerende direktør hos Adventure Works og tildelt stillingen **Adm. direktør**. Lori styrer udviklingen af et produkt, der bruges til at rense dimser. Hun har brug for, at en bogholder hjælper hende med økonomien. Derfor har hun ansat Kim Akers som sin bogholder. Kim rapporterer direkte til Sanjay Patel, men hun samarbejder også med Lori Penor med regnskabsopgaver til udvikling af renseanordningen.

Du skal udføre følgende opgaver for at konfigurere samarbejdsforhold mellem Kim Akers og Lori Penor i det foregående eksempel:

1. Opret en brugerdefineret stillingshierarkitype, som kaldes **Widget**, for at oprette et hierarki, der omfatter stillinger, der er ansvarlige for at arbejde på rensningsproduktet.
2. Angiv stillingen **Adm. direktør** til at være den stilling, som Kims stilling rapporterer til i **Widget**-hierarkiet.
3. Brug stillingshierarkiet til at se rapporteringsstrukturen for stillinger. Hvis du har flere stillingshierarkier, kan du se hierarkiet for hver enkelt hierarkitype i stillingshierarkiet. Du kan også søge efter en stilling efter stillings-id eller efter navnet på den arbejder, der er tildelt stillingen. Stillingshierarkiet er et organisationshierarki.

## <a name="labor-union"></a>Fagforening

Du kan registrere, om der kræves en fagforeningsaftale for stillingen, og hvilken fagforening der anvendes. Du kan også knytte aftalen til en juridisk enhed.

## <a name="financial-dimensions"></a>Økonomiske dimensioner

Når du opretter den økonomiske dimension for en stilling, skal du angive en juridisk enhed. Du kan vælge standarddimensionerne for hver enkelt dimension. Du kan også vælge en fordelingsskabelon, der automatisk udfylder standarddimensioner. En fordelingsskabelon giver dig også mulighed for at fordele beløb på tværs af flere dimensionsværdier.
