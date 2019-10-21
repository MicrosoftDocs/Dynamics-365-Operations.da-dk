---
title: Administrere ordrer på hold
description: Denne procedure viser, hvordan du sætter kundesalgsordrer på hold, hvordan du arbejder med udtjekning af ordrehold, og hvordan du fjerner ordrehold.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7168d13ef0b24d06aa28fbbc22bbb4e6093df24
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/11/2019
ms.locfileid: "1994904"
---
# <a name="manage-order-holds"></a>Administrere ordrer på hold

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du sætter kundesalgsordrer på hold, hvordan du arbejder med udtjekning af ordrehold, og hvordan du fjerner ordrehold. En ordre kan sættes på hold af en række årsager. Du kan for eksempel holde en ordre tilbage, indtil en kundeadresse eller betalingsmetode er kontrolleret, eller indtil en chef kan gennemse kundens kreditmaksimum. Mens ordren er på hold, kan den ikke behandles af lagerstedet til forsendelse. 

Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.


## <a name="set-up-order-holds"></a>Konfigurere salgsordrer på hold
1. Gå til **Navigationsrude > Moduler > Salg og marketing > Opsætning > Salgsordrer > Koder for ordrehold**.
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Holdkode**. Skriv f.eks. 'Tilbagekald'.  
4. Indtast en værdi i feltet **Beskrivelse**.
    - For eksempel: Ordre tilbageholdes, venter på kundes tilbagekald.  
    - Du kan eventuelt markere afkrydsningsfeltet **Fjern reservationer** for at fjerne eventuelle fysiske reservationer fra ordren, når holdkoden tilføjes.  
5. Klik på **Gem**.

## <a name="place-order-on-hold"></a>Placere ordre på hold
1. Gå til **Navigationsrude > Moduler > Salg og marketing > Salgsordrer > Alle salgsordrer**.
2. Klik på **Ny**.
3. Indtast eller vælg en værdi i feltet **Debitorkonto**.
4. Klik på **OK**.
5. Indtast eller vælg en værdi i feltet **Varenummer**.
6. Angiv et tal i feltet **Antal**.
7. Klik på **Salgsordre** i **handlingsruden**.
8. Klik på **Ordrer på hold**.
9. Klik på **Ny**.
10. Vælg den kode, du har oprettet i den tidligere underopgave, i feltet **Holdkode**.
11. Klik på **Gem**.
12. Luk siden.
13. Gå til **Salg og marketing > Salgsordrer > Alle salgsordrer**.
14. Markér den valgte række på listen. Ordrer, der er på hold, har felterne "Udfør ikke behandling" og "Hold" markeret.
15. Klik på **Pluk og pak** i handlingsruden.

## <a name="manage-order-holds"></a>Administrere ordrer på hold
1. Gå til **Salg og marketing > Salgsordrer > Åbne ordrer > Ordrer på hold**. Siden **Ordrer på hold** fungerer som et panel, hvor du kan få en oversigt over alle aktuelle og behandlede hold og håndtere dem og tilknyttede salgsordrer.     
2. Markér den valgte række på listen.
3. Klik på **Hold på udtjekning** i **handlingsruden**.
4. Klik på **Check ud**.
5. Fjern markeringen af den valgte række på listen. Feltet **Udtjekningen til** viser nu dit bruger-id.   
6. Klik på **Ryd udtjekning**.
7. Klik på **Ryd På hold** i **handlingsruden**.
    - Når du er klar til at fjerne holdet og lade ordren fortsætte til næste trin i opfyldelsen, skal du rydde holdet. Hvis ordren ikke kræver nogen ændringer, kan du køre handlingen Ryd På hold. Du kan dog bruge handlingen Ryd og rediger, hvis ordren skal opdateres, når du fjerner et hold.      
    - Handlingen **Ryd og send** er kun gældende, når du bruger callcenter-funktionalitet.  
8. Klik på **Ryd På hold**. Holdet er nu ryddet fra ordren og fjernet fra listen over aktive hold. Hvis du vil se alle hold eller deres delsæt i henhold til en bestemt status, skal du ændre værdien i feltet Vis.     

