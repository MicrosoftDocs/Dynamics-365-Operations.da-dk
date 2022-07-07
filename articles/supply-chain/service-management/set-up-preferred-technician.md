---
title: Konfigurere en foretrukket tekniker
description: Du kan vælge enhver arbejder som en foretrukket tekniker til en serviceaftale eller serviceordre.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c9495bbc8e5f7cb603c027a125887feba1f0e2d
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017197"
---
# <a name="set-up-a-preferred-technician"></a>Konfigurere en foretrukket tekniker 

[!include [banner](../includes/banner.md)]


Du kan vælge enhver arbejder som en foretrukket tekniker til en serviceaftale eller serviceordre. Det er dog en god idé at føje arbejderen til et relevant planlægningsteam, så arbejderen er medtaget på **Planlægningstavle**.

## <a name="assign-employee-to-a-dispatch-team"></a>Knytte en medarbejder til et planlægningsteam

1.  Klik på **Personale** \> **Arbejdere** \> **Arbejdere**. Dobbeltklik på en arbejder for at åbne arbejderens side med detaljer. I **handlingsruden** skal du klikke på **Opsætning** \> **Planlægningsteam** for at åbne formularen **Planlæg medarbejdere**.

2.  Vælg det team, der skal tilknyttes arbejderen, i feltet **Planlægningsteam**.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Knytte en foretrukken tekniker til en serviceaftale

1.  Klik på **Servicestyring** \> **Serviceaftaler** \> **Serviceaftaler**. Dobbeltklik på en serviceaftale for at åbne formen med detaljer.

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
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]