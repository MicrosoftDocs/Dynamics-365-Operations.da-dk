---
title: Installer en IoT-eksempelløsning på Azure
description: Data intelligence bruger data fra det, som man ellers har forbindelse til Microsoft Azure. I denne artikel forklares det, hvordan du installerer en IoT-løsning (Internet of Things) på dit Azure-abonnement.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 284aba91aa436ed1dfc02b5a93b4358ffc518017
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428330"
---
# <a name="deploy-an-iot-solution-on-azure"></a>Installer en IoT-eksempelløsning på Azure

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Data intelligence bruger data fra det, som man ellers har forbindelse til Microsoft Azure. Hvis du vil gøre det muligt for Azure at hente data fra din aftale og dele dem med Dynamics 365 Supply Chain Management, skal du implementere en IoT-løsning (Internet of Things) på dit Azure-abonnement. Følgende arkitekturdiagram indeholder en oversigt over løsningen og dens komponenter.

![Diagram over arkitekturen for dataoplysninger.](media/sdi-architecture.png "Diagram over arkitekturen for dataoplysninger")

Følg disse trin for at anvende de nødvendige ressourcer i Azure.

1. Log på dit Supply Chain Management som administrator.
1. Gå til **Systemadministration \> Opsætning, \> Sensor Data Intelligence \> Installér, og forbind Azure-ressourcer** for at åbne installationsguiden.
1. Læs oplysningerne på siden **Velkommen**, og vælg Derefter **Næste**.
1. På siden **Installer IoT-eksempelløsningen på Azure** skal du læse oplysningerne og derefter vælge **Installér** i afsnittet **Instruktioner**.
1. Der åbnes en ny browserfan, og du tages med til Azure-portalen, så du kan implementere Azure-ressourcerne. Hvis du bliver bedt om det, skal du logge på med dine legitimationsoplysninger til dit Azure-abonnement.
1. Vælg dit abonnement i feltet **Abonnement** på siden **Brugerdefineret implementering**.
1. Under feltet **Ressourcegruppe** skal du vælge **Opret ny** for at oprette en ressourcegruppe til de Azure-komponenter, du vil implementere.
1. Angiv et navn til den nye ressourcegruppe i feltet **Navn** i den dialogboks, der vises (f.eks. *IoT-demo*). Vælg derefter **OK**.
1. Angiv følgende felter:

    - **Ressourcegruppe** – Vælg den ressourcegruppe, du lige har oprettet.
    - **Region** – Vælg en region– ideelt set den region, hvor Dit Supply Chain Management-miljø implementeres. Husk, at Azure-områder har en anden prissætning. Du kan få vist estimerede omkostninger for dit område ved hjælp af [prisregnemaskinen til dataoplysninger](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68).
    - **URL-adresse til Supply Chain Management-miljøet** – Angiv URL-adressen til dit Supply Chain Management-miljø.
    - **Genbrug eksisterende Azure IoT Hub** – Lad dette afkrydsningsfelt ikke være markeret.

1. Vælg **Næste gennemsyn + opret**.
1. Klik på **Opret** på siden til **bekræftelse af installationen**, når du har kontrolleret, at oplysningerne er korrekte.
1. Siden **Installation er i gang**, viser status for installationen. Installationsprocessen kan tage op til 30 minutter. Når siden **Installation er i gang**, angiver det, at installationen er fuldført, skal du vælge linket til navnet på ressourcegruppen for at åbne en side med en liste over de ressourcer, der er implementeret i gruppen.
1. Find den post, hvor feltet **Type** er angivet til *Administreret identitet*, på ressourcelisten. Vælg navnet i kolonnen **Navn** for at åbne siden Detaljer om ressourcen.
1. Kopier værdien i feltet **Klient-id** (f.eks. ved at vælge knappen **Kopiér til Udklipsholder**).
1. Gå tilbage til fanen browser, hvor Supply Chain Management kører, *men luk ikke fanen for Azure-portalen*. Siden **Implementer eksempel-IoT-løsningen på Azure-guiden** bør stadig være åben. 
1. Vælg **Næste**.
1. Indsæt den **klient-id-værdi**, du kopierede i feltet **Azure AD Programklient-id** på siden **Opret forbindelse til Azure-ressourcer**.
1. Gå tilbage til fanen browser, hvor Azure-portalen er åben, *men luk ikke fanen for Supply Chain Management*. Detaljesiden for ressourcen skal være åben.
1. Vælg browserens **tilbage-knap** for at vende tilbage til listen over ressourcer i den nye ressourcegruppe.
1. Find den post, hvor feltet **Type** er angivet til *Azure Cache for Redis*, på ressourcelisten. Vælg navnet i kolonnen **Navn** for at åbne siden Detaljer om ressourcen.
1. Vælg **Adgangsnøgler** i den venstre navigationsrude.
1. Kopier den værdi, der er vist for **primær forbindelsesstreng (StackExchange.Redis)** (f.eks. ved at vælge knappen **Kopiér til Udklipsholder**) på siden **Adgangsnøgler**.
1. Gå tilbage til fanen browser, hvor Supply Chain Management kører. Siden **Connect Azure-ressourcer** skal stadig være åben.
1. Indsæt den værdi, du har kopieret **Primær forbindelsesstreng (StackExchange.Redis)** i feltet **Forbindelsesstreng for Redis Metric-lager**.
1. Vælg **Udfør**.

Azure resources for Azure Data Intelligence implementeres nu på dit Azure-abonnement.

> [!NOTE]
> Du kan når som helst få vist eller redigere de forbindelsesoplysninger, der er gemt i Supply Chain Management, ved at åbne siden **Sensor Data Intelligence-parametre**. Du kan finde flere oplysninger på [Sensor Data Intelligence-parametre](sdi-parameters.md).
