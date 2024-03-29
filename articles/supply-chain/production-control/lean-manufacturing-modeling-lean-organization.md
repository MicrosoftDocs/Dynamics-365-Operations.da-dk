---
title: Modellering af en lean organisation
description: Artiklen indeholder oplysninger om de vigtigste begreber inden for modellering af lean organisation.
author: johanhoffmann
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, KanbanFlowSelection, KanbanFlow
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f3958d21188163fe95e36ba4b8117ae8314b0fd1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570195"
---
# <a name="modeling-a-lean-organization"></a>Modellering af en lean organisation

[!include [banner](../includes/banner.md)]

Artiklen indeholder oplysninger om de vigtigste begreber inden for modellering af lean organisation. 

Et lean manufacturing-scenarie er typisk mere end en samling af ikke-relaterede kanban-regler eller materialeforsyningspolitikker. Strømmen af materialer og produkter i arbejdsceller og lokationer for et bestemt produktions- eller forsyningsscenarie kan beskrives som en sekvens eller et mindre netværk af proces- eller overførselsaktiviteter. Denne sekvens eller dette netværk kaldes også et produktionsflow.

## <a name="production-flows-in-lean-manufacturing"></a>Produktionsflows i lean manufacturing
I produktionsscenarier baseret på produktionsordrer udstedes materiale til en bestemt produktionsordre. Under en sekvens af handlinger, der er baseret på en stykliste og ruter, oprettes produkter og modtages slutteligt på den angivne lokalitet. Procestiden for produktionsordrer varierer i intervaller fra få minutter til uger. Alle relaterede omkostninger, materialer og arbejde akkumuleres på produktionsordren. 

For at reducere leveringstider og overskydende lager mellem ressourcer, der er forårsaget af batchproduktion, introducerer lean manufacturing kanban-opfyldning og supermarkeder i produktion og genopfyldning af lagersted. Dette bringer normalt uorden i produktionen af delvist uafhængige kanban-cyklusser. Genopfyldning af en kanban for et halvfærdigt produkt udløses ikke længere af en ordre til et færdigt produkt. 

Hvis du vil genoprette en produktions- og omkostningskontekst for de forskellige kanban-scenarier, der foreslås, introduceres de aktivitetsbaserede produktionsflows som grundstenen i lean manufacturing. Alle kanban-regler refererer til denne prædefinerede struktur. Den aktivitetsbaserede model understøtter opsætningen af en lang række scenarier. Men denne model tilføjer ikke kompleksitet for medarbejdere i produktionen, fordi alle scenarier bruger den samme aktivitetsbaserede brugergrænseflade.

## <a name="semi-finished-products-non-bom-levels"></a>Halvfabrikata (ikke-styklisteniveauer)
Lean Manufacturing integrerer kanban for produkter på lager og halvfabrikata i en enkelt ramme, hvilket derfor sikrer en ensartet brugeroplevelse for alle sager. På grund af denne arkitektur skal flere styklisteniveauer ikke længere indføres for at aktivere kanbans til anvendelse på halvfabrikata. Denne arkitektur er også med til at reducere lagertransaktioner til et minimum.

## <a name="products-and-material-in-work-in-progress"></a>Produkter og materialer i igangværende arbejde
Reduktion af batchstørrelser til den ideelle tilstand af et enkelt stykke flow i lean manufacturing kan medføre en dramatisk stigning i lagertransaktioner, hvis hver plukningsproces eller kanban-registrering medfører transaktioner for de forbrugte varer. Produktionsflow-arkitektur giver mulighed for overførsel af materiale til produktionsflowet sammen med udbetalingskanbans på lager eller transport af materialehåndteringsenheder. Værdien af det udstedte materiale er føjet til den igangværende forarbejdningskonto, der er relateret til produktionsflowet. Denne funktionsmåde ligner funktionsmåden for materiale, der er udstedt til en produktionsordre. Det samme princip kan anvendes på produkter og halvfabrikata. Medmindre disse er oprettet, overflyttet eller forbrugt i et produktionsflow, er lagertransaktioner valgfri. Når produkterne bogføres til lageret, reduceres IGVF-kontoen for produktionsflowet ved at fratrække den relaterede standardomkostning.

## <a name="value-streams-and-value-stream-mapping"></a>Værdistrømme og værdistrømtilknytning
Arkitekturen i Lean Manufacturing er inspireret af de fem Lean-principper, der er udarbejdet af Womack og Jones: Customer value, Value stream, Flow, Pull og Perfection. En godkendt metode til implementering af lean manufacturing-løsninger i den fysiske verden af produktion er tilknytning af værdistrøm (VSM). Denne metode blev introduceret af Rother og Shook i deres publikation "Learning to See" på Lean Manufacturing Institute. 

Den fremtidige værdistrøm modelleres som en version af produktionsflowet. Alle processer af værdistrømmen er udformet som procesaktiviteter. Bevægelser eller overførsler kan modelleres som overførselsaktiviteter, hvis overførselsstatussen skal registreres, eller hvis en integration med lagerplukning eller konsolideret forsendelse er påkrævet. 

Selve værdistrømmen er udformet som en driftsenhed. Værdistrømmen kan derfor bruges som en økonomisk dimension.

Du kan finde flere oplysninger om driftsenheder under [Oprette en driftsenhed](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md).

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Efterkalkulation af lean manufacturing baseret på produktionsflowet
Periodisk konsolidering af omkostningerne for et produktionsflow retter den relaterede IGVF-konto og giver mulighed for bestemmelse af afvigelser for produkterne, der leveres af produktionsflowet.

## <a name="continuous-improvement"></a>Løbende forbedring
For bedre at understøtte løbende forbedring, implementeres produktionsflow i tidseffektive versioner. Derfor kan en eksisterende version af produktionsflowet samt alle relaterede kanban-regler kopieres til en fremtidig version af produktionsflowet. Desuden kan produktionsflowets fremtidige tilstand modelleres, før det er godkendt og aktiveret for produktionen. Eksisterende kanbans fra gamle produktionsflowversioner er automatisk relateret til den nye version for at sikre et problemfrit materialeforbrug på overførselsdatoen og senere.

## <a name="simplicity"></a>Enkelhed
For implementeringen af Lean Manufacturing skal du vælge et produktionsflow og den aktivitetstilgang, der muliggør modellering af enkle og komplekse scenarier i en enkelt skalerbar arkitektur. Et nærmere kig på aktivitetskonceptet afslører en ny enkelhed for de brugere, der har brug for det: produktions- og logistikarbejdere. Ved at rapportere mod aktivitetsbaseret job i stedet for lagerposteringer, overfører en ensartet brugergrænseflade for alle lean manufacturing-varianter forretningskompleksiteten fra brugergrænsefladen til, hvor den hører til: produktionsflowet som grundstenen i lean manufacturing.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]