---
title: POS-offlinetilstand
description: "Denne artikel indeholder oplysninger om offline-tilstand for Retail Modern POS, hvor POS-enheder automatisk skifter fra kanaldatabasen til offlinedatabasen, hvis detailserveren ikke er tilgængelig. Denne artikel indeholder også generelle oplysninger for offline-tilstand og forklarer den datasynkronisering, der opstår mellem offlinedatabasen og kanaldatabasen."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>POS-offlinetilstand

Denne artikel indeholder oplysninger om offline-tilstand for Retail Modern POS, hvor POS-enheder automatisk skifter fra kanaldatabasen til offlinedatabasen, hvis detailserveren ikke er tilgængelig. Denne artikel indeholder også generelle oplysninger for offline-tilstand og forklarer den datasynkronisering, der opstår mellem offlinedatabasen og kanaldatabasen.

<a name="overview"></a>Overblik
--------

I moderne Retail POS går et punkt for salg (POS) enhed i offlinetilstand, når retail-serveren ikke er tilgængelig. Derfor, hvis forbindelsen til serveren retail går tabt, moderne detail-POS skifter automatisk til offlinedatabasen. Hvis en dataanmodning ikke lykkes under en salgstransaktion inden for det timeoutinterval, der er konfigureret i offlineprofilen, skifter Retail Modern POS automatisk til offlinedatabasen og fortsætter salgstransaktionen. Mens POS-enheden er i offlinetilstand, forsøger Retail Modern POS at genoprette forbindelsen til detailserveren efter det interval for forsøg på at genoprette forbindelse, der er konfigureret i offlineprofilen. Dette forsøg på genoprettelse af forbindelse opstår kun i begyndelsen af en transaktion.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>Bestemmelse af forbindelsestilstanden for Retail Modern POS

Statushovedet i Retail Modern POS angiver den aktuelle forbindelsesstatus, og vinduet **Forbindelsesstatus** viser status for det seneste forsøg på synkronisering med offlinedatabasen. [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Oprette en knap til at skifte manuelt mellem online- og offlinetilstande

Du kan føje en knap til Retail Modern POS for at skifte manuelt mellem online- og offlinetilstande. Opret en knap til POS-operation **917 – Forbindelsesstatus for database**. Navnet på denne knap er **Afbryd**, når Retail Modern POS er tilsluttet detailserveren, og **Opret forbindelse**, når den er frakoblet. Du kan bruge denne knap til at få vist forbindelsen, og til at afbryde forbindelsen til detailserveren eller oprette forbindelse til den. [![Afbryde forbindelsen til knappen i moderne detail-POS](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Konfiguration
For at aktivere offline-understøttelse til POS-enhed (register), angive den **understøtter offline** at **Ja** på den **registrere** side. En ny kanal database-objekt oprettes og føjes til gruppen af butikkens kanal data. Kør derefter alle påkrævede distributionsplaner for at generere datapakker til offlinedatabasen. Derefter installere den offline version af moderne detail-POS. Installationen opretter offlinedatabasen. Desuden skal du installere Microsoft SQL Server 2014 Express Hvis det er nødvendigt. Synkronisering af offlinedata starter efter den første logon til Retail Modern POS.

## <a name="data-synchronization"></a>Datasynkronisering
Retail planlægger bruges til at sende masterdata til offlinedatabasen. Når du kører en distributionsplan, sendes dataændringer som standard til både kanaldatabasen og offlinedatabasen. Retail Modern POS indeholder det asynkrone synkroniseringsbibliotek, som henter alle tilgængelige datapakker og indsætter dem i offlinedatabasen. Hvis der oprettes transaktioner offline, overfører Retail Modern POS dem til detailserveren, så de kan indsættes i kanaldatabasen. Synkronisering af offlinedata kan kun ske, hvis Retail Modern POS kører. [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)


