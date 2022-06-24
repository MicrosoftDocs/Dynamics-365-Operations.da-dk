---
title: Lastopbygningspanel
description: Denne artikel beskriver, hvordan du kan arbejde med lastopbygningspanelet.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 12d8c351f84e9045ffa94f3fcf0dbdefc633d2a0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878723"
---
# <a name="load-building-workbench"></a>Lastopbygningspanel

[!include [banner](../../includes/banner.md)]

Med lastopbygningspanelet kan du anvende lastopbygningsstrategier, når du opretter laster.

## <a name="create-a-load-building-strategy"></a>Oprette en lastopbygningsstrategi

Du kan bruge lastopbygningsstrategier til automatisk at opbygge laster. Denne funktion kan være nyttige i følgende situationer:

- Hvis du jævnligt leverer et bestemt sæt produkter, kan du spare tid ved at bruge laststrategier, da du ikke behøver at bygge samme last hver gang.
- Hvis du vil undgå halvfulde laster for at maksimere effektiviteten, kan laststrategier være med til at fylde hver last så meget som muligt.

En klasse med lastopbygningsstrategi med navnet `TMSLoadBuildingVolumeStrategy` leverer en laststrategi, der kaldes *Volumenbaseret lastopbygningsstrategi*. Denne strategi gør det muligt for dig at bruge de maksimumværdier, der er angivet for højde og vægt i lastskabelonen, eller du kan tilsidesætte indstillingerne ved at angive nye værdier. Denne strategi er den eneste strategi, der er inkluderet i produktet. (Du kan dog have nogle brugerdefinerede strategier).

Hvis du vil bruge standardstrategien *Volumenbaseret lastopbygningsstrategi*, skal du markere den i feltet **Lastopbygningsstrategi** på siden **Lastopbygningspanel** (**Transportstyring &gt; Planlægning &gt; Lastopbygningspanel**).

Følg disse trin for at oprette en lastopbygningsstrategi.

1. Gå til **Transportstyring &gt; Konfiguration &gt; Lastopbygning &gt; Lastopbygningsstrategier**.
1. Vælg **Generér klasseliste** i handlingsruden for at sikre dig, at du har de seneste versioner af alle tilgængelige klasser.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv et entydigt navn til strategien, vælg dens klasse for lastopbygningsstrategi, og indtast en beskrivelse.
1. Vælg **Gem** i handlingsruden.
1. Gå til handlingsruden, og vælg **Parametre**.
1. Vælg **Volumenkapacitet** på listen på siden **Parametre for lastopbygningsstrategi**, og brug derefter feltet **Værdi** til at angive den procentdel af lastens samlede volumenkapacitet, der skal anvendes for den nye lastopbygningsstrategi.
1. Vælg **Vægtkapacitet** på listen, og brug derefter feltet **Værdi** til at angive den procentdel af lastens samlede vægtkapacitet, der skal anvendes for den nye lastopbygningsstrategi.
1. Luk siden **Parametre for lastopbygningsstrategi**.
1. Luk siden **Lastopbygningsstrategier**.

Du kan nu tildele lastopbygningsstrategien til en lastopbygningsskabelon. Du kan også bruge den direkte i lastplanlægningspanelet.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Bruge en lastopbygningsstrategi i lastopbygningspanelet

1. Gå til **Transportstyring &gt; Planlægning &gt; Lastopbygningspanel**.
1. Udfør ét af følgende trin:

    - Vælg en strategi i feltet **Lastopbygningsstrategi**.
    - Hvis du har defineret en lastopbygningsskabelon og tildelt den lastopbygningsstrategien, skal du vælge **Anvend skabelon** under fanen **Administrer skabeloner** i handlingsruden. Vælg derefter en skabelon i feltet **Navn på lastopbygningsskabelon** i rullemenuen i dialogboksen **Anvend lastopbygningsskabelon**.

1. Vælg en eller flere [lastskabeloner](load-template.md) i oversigtspanelet **Indlæs skabelonrækkefølge**. Panelet vil forsøge at indpasse lasten i disse typer objektbeholdere i den rækkefølge, der er angivet her. Du skal typisk anbringe de mindste objektbeholdere øverst på listen for at sikre, at den mindst mulige objektbeholder vælges først.
1. Vælg **Foreslå laster** i handlingsruden.
1. Gennemse de foreslåede laster og de foreslåede lastlinjer.
1. I handlingsruden skal du vælge **Opret laster** for at oprette laster, der er baseret på kildedokumentlinjerne i oversigtspanelet **Foreslåede lastlinjer**.
1. Luk siden **Lastopbygningspanel**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]