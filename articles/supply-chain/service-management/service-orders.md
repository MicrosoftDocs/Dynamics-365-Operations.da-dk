---
title: Serviceordrer
description: En serviceordre repræsenterer en serviceteknikers besøg hos en kunde på en bestemt dato.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64863b8c19c756cffab94adeaa9c38a0a3388d70
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215027"
---
# <a name="service-orders"></a>Serviceordrer   

[!include [banner](../includes/banner.md)]


En serviceordre repræsenterer en serviceteknikers besøg hos en kunde på en bestemt dato. Hver serviceordre består af en eller flere serviceordrelinjer. Serviceordrelinjer repræsenterer de arbejdstimer, der skal udføres af serviceteknikeren, og de relaterede varer, omkostninger og gebyrer.

Du kan knytte opgaver og objekter til en serviceordrelinje. Du kan derefter gruppere serviceordrelinjer efter opgave eller objekt. Du kan også knytte varer, der findes på lagerlisten, til serviceordrelinjer.

## <a name="create-service-orders"></a>Oprette serviceordrer

Du kan oprette serviceordrer på basis af en serviceaftale og linjerne i den pågældende aftale. Du kan dog kun oprette serviceordrer, der er tilknyttet en serviceaftale, i den periode, der er angivet i aftalen. Hvis en serviceaftale f.eks. er gyldig for kalenderåret 2011, kan du oprette serviceordrer for aftalen fra 1. januar 2011 og 31. december 2011.

Du kan også oprette serviceordrer individuelt, uden at knytte dem til en aftale. Disse serviceordrer kan bruges til at håndtere ikke-planlagt eller enkeltstående servicebesøg. I marts måned beslutter din kunde sig f.eks. for at få udført service på to maskiner ud over dem, der er angivet i serviceaftalen. Til denne opgave skal du oprette serviceordrer, men de skal ikke knyttes til en aftale.


> [!NOTE]
> <P>Hvis du vil oprette serviceordrer, der ikke der er tilknyttet en serviceaftale, skal du markere afkrydsningsfeltet <STRONG>Tillad uden serviceaftale</STRONG> i formularen <STRONG>Parametre for servicestyring</STRONG>.</P>

**Scenario**

I følgende scenario beskrives en anden situation, hvor det er praktisk at oprette en serviceordre, der ikke er knyttet til en serviceaftale.

Firmadispatcheren modtager et opkald om hasteservice for en elevator. Der er ikke tid til at oprette en serviceaftale og et projekt for servicen. Derfor opretter afsenderen en serviceordre direkte i formularen **Serviceordrer**, vedhæfter serviceordren til et eksisterende projekt og opretter serviceordrelinjerne. Afsenderen opretter også en opgave- eller objektrelation for en eksisterende serviceordre for at registrere arbejde, der ikke er relateret til serviceaftalen. Du kan finde flere oplysninger under [Oprette serviceordrer manuelt](create-service-orders-manually.md) og [Oprette serviceopgaverelationer](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>Overvåge status for serviceordrer

Hvis du vil overvåge status for en salgsordre via gennem de forskellige teams og arbejdsprocesser, kan du opretteet system over trin og årsagskoder for serviceordrer. Du kan angive de handlinger, der er tilladt for hvert trin. Du kan finde flere oplysninger under [Oprette årsagskoder](create-reason-codes.md).

**Eksempel**

En serviceordre godkendes af afsenderen. Afsenderen opdaterer serviceordretrinnet og angiver en årsagskode, som angiver, at serviceordren er blevet frigivet til serviceteknikeren. Serviceteknikeren besøger kunden og udfører servicen.

## <a name="specify-item-requirements-for-service-orders"></a>Angive varebehov til serviceordrer

Du kan angive de lagervarer, der er nødvendige til serviceordrer. Serviceordren skal dog være tilknyttet et projekt. Varebehov til serviceordrer behandles løbende igennem et projekt. 

**Eksempel**

De serviceordrer, der oprettes ud fra serviceaftalen, behandles derefter af afsenderen. På den første serviceordre kan afsenderen se, at serviceteknikeren skal bruge en vigtig reservedel, der ikke findes på lageret. Afsenderen opretter derfor et varebehov for reservedelen direkte ud fra serviceordren.

## <a name="move-and-post-lines"></a>Flytte og bogføre linjer

En servicetekniker returnerer fra et servicebesøg og ændrer og opdaterer derefter serviceordrelinjerne. Under servicebesøget udførte teknikeren et servicejob, der var planlagt til næste servicebesøg. Derfor flytter teknikeren linjerne fra det næste servicebesøg til det aktuelle servicebesøg. Teknikeren bogfører derefter serviceordren. Du kan finde flere oplysninger under [Flytte serviceordrelinjer](move-service-order-lines.md).

## <a name="cancel-service-orders"></a>Annuller serviceordrer

En af de andre serviceordrer, der blev oprettet for januar måned, bliver forældet, fordi jobbet er annulleret. Serviceafsenderen annullerer derfor serviceordren. Du kan finde flere oplysninger under [Annullere serviceordrer](cancel-service-orders.md).

## <a name="post-from-projects"></a>Bogføre fra projekter

I slutningen af ugen ønsker afsenderen at bogføre alle serviceordrer, der er knyttet til et bestemt projekt. Afsenderen finder derfor det relevante projekt i formularen **Projekter** og bogfører de fuldførte serviceordrer. Du kan finde flere oplysninger under [Bogføre serviceordrer (klasseformular)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Slet serviceordrer

I løbet af anden halvdel af året beslutter kunden sig for, at servicebesøgene ikke sker ofte nok. Du skal oprette en ny række af mere hyppige servicebesøg for den resterende tid i serviceaftalen. Du skal derfor slette de eksisterende oprettede serviceordrer og oprette nye serviceordrer. Du kan finde flere oplysninger under [Slette serviceordrer](delete-service-orders.md).

## <a name="see-also"></a>Se også

[Serviceordrer (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))

  


