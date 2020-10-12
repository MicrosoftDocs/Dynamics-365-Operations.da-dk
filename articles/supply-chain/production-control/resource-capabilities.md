---
title: Ressourceegenskaber
description: Denne artikel indeholder oplysninger om ressourceegenskaber. En funktion er en operationsressource evne til at udføre en bestemt aktivitet. I denne artikel beskrives det, hvordan egenskaber og relaterede begreber såsom færdighedsniveau og prioritet bruges til at vælge passende ressourcer til en aktivitet.
author: sorenva
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability, WrkCtrTable, WrkCtrCapRes, WrkCtrApplicableResources
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc01e2d28758008d2e147a92c498da7ccb14b173
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826304"
---
# <a name="resource-capabilities"></a>Ressourceegenskaber

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om ressourceegenskaber. En funktion er en operationsressource evne til at udføre en bestemt aktivitet. I denne artikel beskrives det, hvordan egenskaber og relaterede begreber såsom færdighedsniveau og prioritet bruges til at vælge passende ressourcer til en aktivitet.

En funktion er en operationsressource evne til at udføre en bestemt aktivitet. En operationsressource kan have tilknyttet mere end en egenskab, og en egenskab kan have tilknyttet mere end en ressource. Du kan midlertidigt tildele egenskaber til ressourcer ved at definere en startdato og udløbsdato for egenskabstildelingen. Når egenskaben for en ressource udløber, kan ressourcen ikke planlægges for et projekt eller en produktion, der kræver denne egenskab. En egenskab, der er udløbet, kan fornys. Du kan slette egenskaber, så længe de ikke er i en ruterelation eller en del af en produktionsrute for en aktiv produktionsordre. Du skal generelt være forsigtig med at slette egenskaber. Overvej i stedet at justere udløbsdatoen på ressourcer, der har egenskaben. Egenskaber kan tildeles til alle typer ressourcer: værktøj, leverandør, maskine, lokalitet, facilitet eller personale.

## <a name="level"></a>Niveau
Flere ressourcer har ofte samme funktionelle egenskab, men på forskellige niveauer af færdigheder (f.eks styrke, processorhastighed eller nøjagtighed). Når du tildeler en ressource en funktion, kan du derfor angive en værdi for **Niveau**. Niveauet er en simpel numerisk værdi. Hvis du angiver, at en egenskab er en kildeforudsætning for en produktionsrute, kan du også angive en værdi for **Minimumsniveau, der kræves** for denne egenskab. Planlægningsprogrammet vælger derefter kun ressourcer, der har den nødvendige egenskab på et niveau, der er lig med eller overstiger minimumsniveauet, der er angivet i kildeforudsætningen.

## <a name="priority"></a>Prioritet
Operationsressourcer, der har de samme egenskaber, kan tildeles en prioritet. Hvis flere ressourcer har egenskaber, der opfylder planlægningskravene på det ønskede niveau, og har ledig kapacitet, så kan planlægningsprogrammet vælge mellem disse ressourcer. Hvis **Prioritet** er valgt i feltet **Valg af primær ressource** på siden **Planlægningsparametre** side, så vælges den ressource, der har den højeste prioritet (den laveste numeriske værdi i feltet **Prioritet**), som den første under planlægning.

## <a name="resource-requirements"></a>Ressourcebehov
Når du definerer kildeforudsætning for en produktionsrute, kan du angive en eller flere egenskaber som krav. Under produktionsplanlægning bliver de egenskaber, der er defineret i kildeforudsætningerne på ruteoperationen, sammenlignet med de egenskaber, der er defineret for ressourcerne. Ressourcer, der har egenskaber, som opfylder kravene, vælges. Hvis flere ressourcer har samme funktionelle egenskab, men forskellige færdigheder (såsom styrke, processorhastighed eller nøjagtighed), kan du definere flere egenskaber eller bruge egenskabsniveauet til at kvalificere ressourcens egenskab. Her er et eksempel:

-   På en rute er boreprocestiden indstillet til 10 enheder pr.time, mens selve kravet er defineret som Boring.
-   Du har to boremaskiner, M1 og M2.
-   Egenskaben Boring er tildelt begge ressourcer, M1-maskinen og M2-maskinen.
-   M1-maskinen kan bore to enheder i timen, mens M2-maskinen kan bore 11 enheder i timen.

I dette eksempel kan begge maskiner kan vælges af planlægningsprogrammet, fordi de begge opfylder det grundlæggende krav til egenskab, Boring. M1-maskinen kan dog bore to enheder i timen. Da denne sats er meget mindre end 10 enheder pr. time, der er angivet på ruten, medfører M1-maskinen produktionsproblemer, hvis den vælges. Der er to måder at løse dette problem, og sørg for, at M2-maskinen er valgt i stedet:

-   Opret to separate egenskaber: Lav borehastighed og Høj borehastighed. Definer Lav borehastighed som en boreprocestid på en til ni enheder pr. time. Definer Høj borehastighed som en boreprocestid på 10 til 19 enheder pr. time. Tildel derefter M1-maskinen egenskaben "Lav borehastighed", og tildel M2-maskinen egenskaben "Høj borehastighed". Endelig skal kravet til ressourceegenskaben på ruten ændres til Høj borehastighed. Derefter vælger planlægningsprogrammet den korrekte maskine (M2).
-   Brug egenskabsniveauet til at kvalificere egenskaben Boring, der er tildelt boremaskiner. Angiv, at M1-maskinen har boreegenskab på niveau 2.0, og at M2-maskinen har boreegenskab på niveau 11.0. Angiv derefter, at 10.0 er det mindste niveau, der kræves til boreegenskaben på ruten. Planlægningsprogrammet afgør derefter, at kun M2-maskinen opfylder kildeforudsætningerne.

## <a name="competencies-for-human-resources"></a>Kvalifikationer for personale
Når du har operationsressourcer af typen **Personale**, der er knyttet til arbejdere i Personale, kan du også drage fordel af kvalifikationer for arbejdere, når du definerer kildeforudsætninger for en produktionsrute. Med andre ord kan du også angive krav til bestemte færdigheder, kurser, certifikater og titler. Planlægningsprogrammet kan derefter vælge ressourcer, der er kædet sammen med arbejdere, og markeringen vil blive baseret på kvalifikationer for disse arbejdstagere. Kvalifikationer er angivet i Personale, ikke på siden **Ressourceegenskaber**. Når du definerer færdigheder, kurser, certifikater og titler som kildeforudsætninger, skal du bruge funktionen Personale og sammenkæde hver ressource af typen **Personale** til en tilsvarende arbejder. Hvis du ikke bruger funktionen Personale, kan du definere funktioner på siden **Ressourceegenskaber**, der ligner eller efterligner kvalifikationer fra personale. Siden **Ressourceegenskaber** indeholder dog ikke den funktionalitet, der kræves for at kunne vedligeholde færdigheder, kurser, certificeringer eller titler.



