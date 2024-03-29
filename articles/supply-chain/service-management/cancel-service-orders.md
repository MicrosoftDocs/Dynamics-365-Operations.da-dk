---
title: Annuller serviceordrer
description: Du kan annullere en serviceordre eller serviceordrelinje fra selve serviceordren, eller du kan annullere flere serviceordrer ved at køre et periodisk job.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 228b76d6f6f0bb048662c8e82df76f51b7cb3652
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017370"
---
# <a name="cancel-service-orders"></a>Annuller serviceordrer   

[!include [banner](../includes/banner.md)]


Du kan annullere en serviceordre eller serviceordrelinje fra selve serviceordren, eller du kan annullere flere serviceordrer ved at køre et periodisk job.


> [!NOTE]
> <P>Serviceordrer kan ikke annulleres, hvis stadiet i serviceordren ikke tillader annullering, hvis der er varebehov i serviceordren, eller hvis serviceordren allerede er bogført.</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>Annullere en serviceordre i formen Serviceordrer

1.  Klik på **Servicestyring** \> **Serviceordrer** \> **Serviceordrer**. Vælg serviceordren, og klik på **Annuller ordre** i handlingsruden.

## <a name="cancel-a-service-order-line"></a>Annullere en serviceordrelinje

1.  Klik på **Servicestyring** \> **Serviceordrer** \> **Serviceordrer**. Dobbeltklik på den serviceordre, der indeholder den linje, du vil annullere.

2.  Vælg den serviceordrelinje, du vil annullere, og klik derefter på **Annuller ordrelinje** for at ændre linjens status til **Annulleret**.


> [!TIP]
> <P>Du kan tilbageføre annulleringen af en serviceordrelinje og ændre dens status tilbage til <STRONG>Oprettet</STRONG> ved at klikke på <STRONG>Fortryd annullering</STRONG>.</P>


## <a name="cancel-multiple-service-orders"></a>Annullere flere serviceordrer

1.  Klik på **Servicestyring** \> **Periodisk** \> **Serviceordrer** \> **Annuller serviceordrer**.

2.  Klik på knappen **Vælg**.

3.  Vælg de serviceordrer, du vil annullere, i kolonnen **Kriterier** i formularen **Forespørgsel**.

4.  Klik på **OK** for at lukke formularen **Forespørgsel**.

5.  Markér afkrydsningsfeltet **Vis infolog** for at generere en infolog, der viser de annullerede serviceordrer.

6.  Markér afkrydsningsfeltet **Fortryd annullering**, hvis du vil fortryde statusangivelsen **Annulleret** for en serviceordre.

7.  Klik på **OK**.

De valgte serviceordrer annulleres, eller deres status **Annulleret** ændres til **Igangværende**.


> [!NOTE]
> <P>Hvis du markerer afkrydsningsfeltet <STRONG>Fortryd annullering</STRONG>, fortrydes statusangivelsen <STRONG>Annulleret</STRONG> for serviceordrerne, mens serviceordrer med statusangivelsen <STRONG>Igangværende</STRONG> ikke annulleres.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]