---
title: Oprette serviceordrer manuelt
description: Du kan oprette serviceordrer manuelt ved hjælp af en serviceaftale eller formularen **Serviceordrer**.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d80461694a28a0842155cbd8ca224c37bd85dde7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202692"
---
# <a name="create-service-orders-manually"></a>Oprette serviceordrer manuelt    

[!include [banner](../includes/banner.md)]


Du kan oprette serviceordrer manuelt ved hjælp af en serviceaftale eller formularen **Serviceordrer**. Du kan også oprette en serviceordre fra et projekt.

> [!TIP]
> <P>Du kan bruge automatiske processer til at oprette serviceordrer. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Oprette en serviceordre manuelt fra en serviceaftale

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.

2.  Vælg en serviceaftale, eller opret en ny serviceaftale.

3.  Klik på fanen **Levér** og klik i gruppen **Opret** på **Planlagte serviceordrer** for at åbne formularen **Opret serviceordrer**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Oprette en serviceordre manuelt i formen Serviceordrer

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.

2.  Tryk på Ctrl+N for at oprette en ny serviceordre.

3.  Opret serviceordrelinjer til serviceordren.

> [!NOTE]
> <P>Hvis afkrydsningsfeltet <STRONG>Tillad uden serviceaftale</STRONG> i formularen <STRONG>Parametre for servicestyring</STRONG> er markeret, kan du bogføre posteringer fra serviceordrelinjerne uden at knytte serviceordren til en serviceaftale. Hvis markeringen i afkrydsningsfeltet fjernes, skal du knytte den manuelt oprettede serviceordre til et projekt, inden du bogfører serviceordrelinjerne.</P>

## <a name="create-a-service-order-from-a-project"></a>Oprette en serviceordre ud fra et projekt

1.  Klik på **Projektstyring og regnskab** \> **Generelt** \> **Projekter** \> **Alle projekter**.

2.  I formularen **Projekter** skal du i **handlingsruden** klikke på fanen **Administrer** \> og klikke på **Service** \> **Serviceordrer**.

3.  Følg den foregående fremgangsmåde for at oprette en serviceordre manuelt i formularen **Serviceordrer**. I feltet **Projekt-id** vises projektreferencen.

> [!NOTE]
> <P>Hvis afkrydsningsfeltet <STRONG>Tillad uden serviceaftale</STRONG> i formularen <STRONG>Parametre for servicestyring</STRONG> er markeret, kan du bogføre posteringer fra serviceordrelinjerne uden at knytte serviceordren til en serviceaftale. Hvis markeringen i afkrydsningsfeltet fjernes, skal du knytte den manuelt oprettede serviceordre til et projekt, inden du bogfører serviceordrelinjerne.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Oprette en serviceordre fra formen Salgsordre

Du kan oprette en serviceordre fra formularen **Salgsordrer** ved hjælp af guiden **Opret en ny serviceordre ud fra salgsordren**.

1.  Klik på **Salg og marketing** \> **Generelt** \> **Salgsordrer** \> **Alle salgsordrer**.

2.  Åbn den relevante salgsordre.

3.  Under fanen **Salgsordre** skal du klikke på **Serviceordre** for at starte guiden **Opret en ny serviceordre ud fra salgsordren**.

4.  Klik på **Næste \>**, og udfør derefter følgende trin på siden **Vælg aftale for serviceordre**:
    
      - Brug feltet **Serviceaftale** til at vælge den serviceaftale, den nye serviceordre skal knyttes til.
    
      - Valgfrit: Brug feltet **Projekt-id** til at knytte denne serviceordre til et bestemt projekt.

5.  Klik på **Næste \>**, og udfør derefter følgende trin på siden **Opret serviceordre**:
    
      - Angiv en dato og et klokkeslæt for, hvornår servicebesøget skal starte, i feltet **Foretrukket servicetidspunkt**.
    
      - Valgfrit: Rediger teksten i feltet **Beskrivelse**. Dette felt indeholder som standard en beskrivelse af den serviceaftale, du har valgt på forrige side.
    
      - Vælg id'et for den medarbejder, der er ansvarlig for aftalen, i feltet **Ansvarlig**, og hvis du kender id'et for kundens foretrukne tekniker ved servicebesøget, skal du også angive det.
    
      - Vælg den person hos kunden, der skal kontaktes angående denne serviceordre, i feltet **Kontakt-id**.

6.  Klik på **Næste \>**, og klik derefter på **Udfør**.


## <a name="see-also"></a>Se også

[Serviceordrer](service-orders.md)

[Oprette serviceordrer automatisk](create-service-orders-automatically.md)

[Opret serviceordrer (klasseform)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 

