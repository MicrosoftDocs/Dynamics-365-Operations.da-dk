---
title: Konfigurere en foretrukket tekniker
description: Du kan vælge enhver arbejder som en foretrukket tekniker til en serviceaftale eller serviceordre.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 850d91372fb1a918840ebc316a4479f4a70bdc24
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424306"
---
# <a name="set-up-a-preferred-technician"></a>Konfigurere en foretrukket tekniker 

[!include [banner](../includes/banner.md)]


Du kan vælge enhver arbejder som en foretrukket tekniker til en serviceaftale eller serviceordre. Det er dog en god idé at føje arbejderen til et relevant planlægningsteam, så arbejderen er medtaget på **Planlægningstavle**.

## <a name="assign-employee-to-a-dispatch-team"></a>Knytte en medarbejder til et planlægningsteam

1.  Klik på **Personale** \> **Generelt** \> **Arbejdere** \> **Arbejdere**. Dobbeltklik på en arbejder for at åbne arbejderens side med detaljer. I **handlingsruden** skal du klikke på **Opsætning** \> **Planlægningsteam** for at åbne formularen **Planlæg medarbejdere**.

2.  Vælg det team, der skal tilknyttes arbejderen, i feltet **Planlægningsteam**.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Knytte en foretrukken tekniker til en serviceaftale

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**. Dobbeltklik på en serviceaftale for at åbne formen med detaljer.

2.  Under fanen **Generelt** skal du vælge feltet **Foretrukken tekniker** for at knytte et medlem af det relevante planlægningsteam til serviceaftalen som den foretrukne tekniker.

## <a name="assign-a-preferred-technician-to-a-service-order"></a>Knytte en foretrukken tekniker til en serviceordre

1.  Klik på **Servicestyring** \> **Periodisk** \> **Planlægningstavle**.
    

    > [!NOTE]
    > <P>I formularen <STRONG>Planlægningstavle</STRONG> skal du angive et datointerval til de planlægningsaktiviteter, du vil have vist. Angiv også, om lukkede aktiviteter skal vises, og om planlægningsaktivitetslisten skal begrænses til teams, som du tilhører, eller som du er bemyndiget til at overvåge. Klik på <STRONG>OK</STRONG> for at åbne formularen <STRONG>Planlægningstavle</STRONG>.</P>



2.  Markér linjen for den serviceaktivitet, du vil redigere.

3.  Vælg fanen **Relateret**, og brug listen **Arbejder** til at tilknytte et medlem af det relevante planlægningsteam som den foretrukne tekniker til servicebesøget.

## <a name="see-also"></a>Se også

[Oversigt over udvikling og udfyldelse af serviceaftaler](service-agreements.md)

[Oprette serviceordrer manuelt](create-service-orders-manually.md)

[Serviceaftaler (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))
  


