---
title: Konfigurere hjælp-oplevelsen for programmer til finans og drift
description: Denne artikel giver oplysninger om komponenterne i Hjælp-system til nogle Microsoft Dynamics 365-apps.
author: edupont04
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: edupont
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.form: SystemParameters
ms.openlocfilehash: 75f3cc1b76b2a38d4004c4fa3f86a528a7eebc3f
ms.sourcegitcommit: d3f7a56eaf788d223ece4cedac4a319eaf5f6112
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9538517"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>Konfigurere hjælp-oplevelsen for programmer til finans og drift

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikel har en oversigt over komponenterne i Hjælp-systemet til programmer til finans og drift, f.eks. Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources. Denne artikel forklarer også, hvordan disse komponenter tilknyttes, og indeholder en oversigt over den proces, der bruges til at oprette brugerdefineret hjælp.

## <a name="help-architecture"></a>Hjælp-arkitektur

Programmer til finans og drift indeholder konceptbaserede oversigter og andre emner, der er udgivet på [Microsoft Dynamics 365-dokumentationens](/dynamics365/) websted. Du kan derefter få adgang til dette indhold fra ruden **Hjælp** i produktet. I følgende illustration vises delene i Hjælp-systemet.

[![Hjælp-arkitektur.](./media/help-architecture.png)](./media/help-architecture.png)

Hjælp-systemet i produktet henter artikler fra Microsoft Learn og andre tilknyttede websteder. Det henter også opgavevejledninger, der er gemt i BPM (Business process modeler) i Microsoft Dynamics Lifecycle Services (LCS).

## <a name="adding-task-guides"></a>Tilføje opgaveguider

> [!NOTE]
> Fanen **Opgaveguider** er i øjeblikket ikke tilgængelig i Human Resources eller Commerce. <!--We are currently working to enable this functionality in a future release.--> Opgaveguiderne i oplevelsen Introduktion i Personale forbliver imidlertid tilgængelige og dækker de grundlæggende funktioner. For både Human Resources og Commerce gælder det, at hjælp til procedurer er tilgængelig på [Microsoft Dynamics 365-dokumentation](/dynamics365/)-webstedet.

På siden **Systemparametre** kan systemadministratorer konfigurere adgang til de relevante biblioteker for opgaveguider til implementering af en installation.

> [!NOTE]
> - Hvis du vil konfigurere hjælp, skal du være logget på med en konto i den samme lejer som den lejer, hvor appen er installeret.
> - Det er ikke muligt at oprette forbindelse til et LCS-bibliotek fra en forekomst af den app, der kører på en lokal virtuel harddisk (VHD).

[![Formularen Systemparametre med hjælpeindstillinger.](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Hvis du vil konfigurere opgaveguides til en løsning, skal du følge disse trin på siden **Systemparametre**.

> [!IMPORTANT]
> Første gang du åbner fanen **Hjælp**, skal du oprette forbindelse til Lifecycle Services. Du skal vælge linket i midten af formularen, vente på forbindelsen, lukke dialogboksen og derefter vælge **OK** for at få adgang til siden **Systemparametre**.
>
> [![Opret forbindelse til LCS](./media/connect-to-lcs-crop-1024x365.png "Opret forbindelse til LCS.")](./media/connect-to-lcs-crop.png)

1. Vælg det Lifecycle Services-projekt, der skal oprettes forbindelse til.
2. Vælg BPM-biblioteker (inden for det valgte projekt), hvor der skal hentes opgaveregistreringer fra.
3. Angiv visningsrækkefølgen for BPM-bibliotekerne. Visningsrækkefølgen bestemmer den rækkefølge, som opgaveregistreringer fra bibliotekerne vises i på ruden **Hjælp**.

Når du har fuldført disse trin, kan du åbne ruden **Hjælp** og vælge fanen **Opgaveguider**. Nu kan du se de opgaveguider, der gælder for den aktuelle side i programmer til finans og drift. Hvis der ikke findes opgaveguider, kan du angive nøgleord for at indsnævre søgningen.

### <a name="showing-translated-task-guides"></a>Visning af oversatte opgaveguider

Oversatte opgaveguider blev frigivet i APQC Unified-biblioteket maj 2016 og i introduktionsbiblioteket. For at få vist lokaliseret opgaveguide-hjælp, skal du sikre dig, at din Dynamics 365-løsning er forbundet til maj 2016-biblioteket. Brugere kan ændre det sprog, som en opgaveguide vises i, ved at ændre sprogindstillingerne under **Indstillinger** &gt; **Indstillinger**.

> [!NOTE]
> Selvom mange opgaveguider er blevet oversat, viser klienten i øjeblikket ikke de oversatte opgaveguider. Derudover er oversættelser i maj 2016-bibliotekst kun tilgængelige for de opgaveguider, der blev frigivet i februar 2016. Microsoft udsender et opdateret bibliotek, der omfatter flere oversættelser.
>
> - Hvis en opgaveguide er blevet oversat, vises teksten i opgaveguiden på det valgte sprog, når du åbner denne opgaveguide.
> - Hvis en opgaveguide ikke er blevet oversat, er det kun noget af teksten (tekst i kontrolelementerne), der vises på det valgte sprog, når du åbner guiden.

## <a name="adding-custom-help"></a>Tilføjelse af tilpasset hjælp

Du kan bruge opgaveguider til at oprette brugerdefineret hjælp, eller du kan oprette forbindelse til **Hjælp**-ruden på et websted.

### <a name="create-custom-help-by-using-task-guides"></a>Oprette tilpasset hjælp ved hjælp af opgaveguider

Du kan oprette brugerdefineret hjælp til de understøttedes apps ved at oprette opgaveregistreringer, der afspejler din implementering, og derefter gemme dem i et bibliotek for forretningsprocesser i LCS. Du kan ikke oprette brugerdefinerede opgaveguider til Personale.

Hvis du som partner fremmer et bibliotek til at være virksomhedens bibliotek og medtager det i en løsning, bliver det tilgængeligt for dine kunder. Du kan også oprette en kopi af det APQC Unified-bibliotek og derefter åbne opgaveregistreringen i kopien, redigere dem og gemme dine ændringer. Du kan finde flere oplysninger under [Arbejdsrutineoptagerressourcer](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>Oprette forbindelse til et brugerdefineret Hjælp-websted

Programmer til finans og drift bruges sjældent i den form, de leveres i fra starten. Løsningen bliver i stedet tilpasset og udvidet, så den passer til organisationens behov. Du kan også tilpasse og udvide Hjælp-funktionerne. Du kan f.eks. føje brugerdefineret Hjælp til ruden **Hjælp** i produktet.

Microsoft har stiller en værktøjskasse til rådighed, der hjælper dig med at implementere og forbinde brugerdefineret hjælp til ruden **Hjælp**. Få flere oplysninger om, hvordan du kan konfigurere en brugerdefineret Hjælp-løsning, der er forbundet til ruden **Hjælp**, i [Oversigt over brugerdefineret hjælp](../../dev-itpro/help/custom-help-overview.md).

Hvis du vil samarbejde med Microsoft om værktøjer og processer til tilpasning af hjælp, skal du udfylde formularen på [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).

## <a name="see-also"></a>Se også

[Hjælp-system](help-overview.md)  
[Oversigt over brugerdefineret hjælp](../../dev-itpro/help/custom-help-overview.md)  
[Ressourcer til arbejdsrutineoptager](../../dev-itpro/user-interface/task-recorder.md)  
[Oprette dokumentation eller kursusmateriale ved hjælp af Arbejdsrutineoptager](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Brugerdefineret GitHub-hjælpelager](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
