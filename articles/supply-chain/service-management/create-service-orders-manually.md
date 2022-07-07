---
title: Oprette serviceordrer manuelt
description: Du kan oprette serviceordrer manuelt ved hjælp af en serviceaftale eller formularen **Serviceordrer**.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1764d97d4492e7b982a5d2c9f7e7f1c15380be1d
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014845"
---
# <a name="create-service-orders-manually"></a>Oprette serviceordrer manuelt    

[!include [banner](../includes/banner.md)]


Du kan oprette serviceordrer manuelt ved hjælp af en serviceaftale eller formularen **Serviceordrer**. Du kan også oprette en serviceordre fra et projekt.

> [!TIP]
> <P>Du kan bruge automatiske processer til at oprette serviceordrer. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Oprette en serviceordre manuelt fra en serviceaftale

1.  Vælg **Servicestyring** \> **Serviceaftaler** \> **Serviceaftaler**.

2.  Vælg en serviceaftale, eller opret en ny serviceaftale.

3.  Vælg fanen **Levér** og vælg i gruppen **Opret** **Planlagte serviceordrer** for at åbne formularen **Opret serviceordrer**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Oprette en serviceordre manuelt i formen Serviceordrer

1.  Vælg **Servicestyring** \> **Serviceordrer** \> **Serviceordrer**.

2.  Vælg **Ny** for at oprette en ny serviceordre.

3.  Opret serviceordrelinjer til serviceordren.

> [!NOTE]
> <P>Hvis afkrydsningsfeltet <STRONG>Tillad uden serviceaftale</STRONG> i formularen <STRONG>Parametre for servicestyring</STRONG> er markeret, kan du bogføre posteringer fra serviceordrelinjerne uden at knytte serviceordren til en serviceaftale. Hvis markeringen i afkrydsningsfeltet fjernes, skal du knytte den manuelt oprettede serviceordre til et projekt, inden du bogfører serviceordrelinjerne.</P>

## <a name="create-a-service-order-from-a-project"></a>Oprette en serviceordre ud fra et projekt

1.  Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.

2.  I formularen **Projekter** skal du i **handlingsruden** vælge fanen **Administrer** \> og vælge **Service** \> **Serviceordrer**.

3.  Følg den foregående fremgangsmåde for at oprette en serviceordre manuelt i formularen **Serviceordrer**. I feltet **Projekt-id** vises projektreferencen.

> [!NOTE]
> <P>Hvis afkrydsningsfeltet <STRONG>Tillad uden serviceaftale</STRONG> i formularen <STRONG>Parametre for servicestyring</STRONG> er markeret, kan du bogføre posteringer fra serviceordrelinjerne uden at knytte serviceordren til en serviceaftale. Hvis markeringen i afkrydsningsfeltet fjernes, skal du knytte den manuelt oprettede serviceordre til et projekt, inden du bogfører serviceordrelinjerne.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Oprette en serviceordre fra formen Salgsordre

Du kan oprette en serviceordre fra formularen **Salgsordrer** ved hjælp af guiden **Opret en ny serviceordre ud fra salgsordren**.

1.  Gå til **Salg og marketing** \> **Salgsordrer** \> **Alle salgsordrer**.

2.  Åbn den relevante salgsordre.

3.  Under fanen **Salgsordre** skal du vælge **Serviceordre** for at starte guiden **Opret en ny serviceordre ud fra salgsordren**.

4.  Vælg **Næste \>**, og udfør derefter følgende trin på siden **Vælg aftale for serviceordre**:
    
      - Brug feltet **Serviceaftale** til at vælge den serviceaftale, den nye serviceordre skal knyttes til.
    
      - Valgfrit: Brug feltet **Projekt-id** til at knytte denne serviceordre til et bestemt projekt.

5.  Vælg **Næste \>**, og udfør derefter følgende trin på siden **Opret serviceordre**:
    
      - Angiv en dato og et klokkeslæt for, hvornår servicebesøget skal starte, i feltet **Foretrukket servicetidspunkt**.
    
      - Valgfrit: Rediger teksten i feltet **Beskrivelse**. Dette felt indeholder som standard en beskrivelse af den serviceaftale, du har valgt på forrige side.
    
      - Vælg id'et for den medarbejder, der er ansvarlig for aftalen, i feltet **Ansvarlig**, og hvis du kender id'et for kundens foretrukne tekniker ved servicebesøget, skal du også angive det.
    
      - Vælg den person hos kunden, der skal kontaktes angående denne serviceordre, i feltet **Kontakt-id**.

6.  Vælg **Næste \>**, og vælg derefter **Udfør**.


## <a name="see-also"></a>Se også

[Serviceordrer](service-orders.md)

[Oprette serviceordrer automatisk](create-service-orders-automatically.md)

[Opret serviceordrer (klasseform)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]