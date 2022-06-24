---
title: Afbryde konfigurationer i RCS Global-lageret
description: Denne artikel beskriver, hvordan konfigurationer i RCS Global-lageret skal afbrydes.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4121f45a95e1712f21390c317af532662846a0fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894805"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Afbryde konfigurationer i RCS Global-lageret

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan konfigurationer i RCS Global-lageret skal afbrydes. Tidligere var det kun muligt at slette konfigurationer, der ikke længere var nødvendige. Men nu kan du markere en frigivet konfiguration som **Annulleret** i RCS Global-lageret. Med denne funktionalitet kan du også gøre følgende: 
 
 - Angiv beskeder på forhånd, når en konfiguration er planlagt til ikke længere at være tilladt.
 - Medtag relevante oplysninger om erstatningskonfigurationen.
 - Angiv en **Understøttet indtil**-dato for den specifikke konfiguration for at informere brugeren om, hvornår den ikke længere vil blive afbrudt.

Når du ikke længere vil bruge en konfigurationsversion, kan du angive følgende valgfrie oplysninger:

  - **Erstatningskonfiguration**
  - **Erstatningskonfigurationsversion**
  - **Fritekstnote**: Brug dette felt til at angive dokumentationslinks eller referencer
  - **Understøttes indtil**: Dette felt indeholder den foreslåede dato, indtil hvilken den aktuelle konfiguration/version vil blive understøttet. Denne dato skal opdateres manuelt.
  
Hvis konfigurationen ikke længere skal afbrydes, skal du udføre følgende trin. 

1. Vælg, om du ikke længere vil afbryde en enkelt version eller alle versioner med samme indstillinger i én handling ved at indstille **Alle versioner** til **Ja**. 
2. Angiv parameteren til **Annuller** til **Ja**.
3. Vælg **OK**, hvis konfigurationerne ikke længere skal afbrydes. Feltet **Understøttet indtil** udfyldes, når du gemmer ændringerne.

![Annullere konfigurationsoplysninger.](media/Discontinue-details-2.png)
  
Du kan altid gendanne konfiguration til **Delt** eller regulere oplysninger, der ikke længere er tilgængelige. Hvis du deler en konfiguration, skal du angive datoen for **Understøttet indtil** og alle andre oplysninger, der vedrører den afbrydelse, der angiver dine planer for fremtidig afbrydelse.

Hvis du vil dele oplysninger om en planlagt afbrydelse, inden konfigurationen faktisk afbrydes, kan brugeren udfylde alle felter, der er relateret til erstatning, men lade parameteren **Annuller** være angivet til **Nej**.

> [!NOTE]
> Afbrydelse begrænser ikke handlinger med konfigurationer. Du kan fortsætte med at importere, køre eller afsende konfigurationerne. Disse felter er oplysninger.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finans understøtter visning af disse oplysninger med start i version 10.0.14

Med start i version 10.0.14 understøtter Dynamics 365 Finance visning af oplysninger om afbrydelse. På siden **Globalt lager** kan du få vist opdaterede oplysninger, der vedrører afbrydelse. De konfigurationer, der ikke længere afbrydes, filtreres som standard ud.
  
På siden **Importerede konfigurationer** (ERSolutionTable) vises de konfigurationer, som allerede var afbrudt, da de blev importeret. For de konfigurationer, der blev afbrudt efter importen, kan de oplysninger, der ikke længere er tilgængelige, synkroniseres ved at køre jobbet **Importer konfigurationsopdateringer**.


