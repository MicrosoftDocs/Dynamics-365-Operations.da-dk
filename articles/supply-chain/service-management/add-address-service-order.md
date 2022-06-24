---
title: Føje en adresse til en serviceordre
description: Denne artikel beskriver, hvordan du føjer en kundeadresse til en serviceordre.
author: sorenva
ms.date: 05/02/2018
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
ms.openlocfilehash: ce58ff7bbb491fd2d250b8986d02fca04bd5fad1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844729"
---
# <a name="add-an-address-to-a-service-order"></a>Føje en adresse til en serviceordre    

[!include [banner](../includes/banner.md)]


Denne artikel beskriver, hvordan du føjer en kundeadresse til en serviceordre. Når du opretter en serviceordre, overføres adresseoplysningerne fra det projekt, som serviceordren er tilknyttet. Du kan dog vælge en alternativ placering fra adresser, der allerede er angivet i Microsoft Dynamics AX for debitorer, kreditorer, websteder, lagre, serviceordrer og projekter.

Du kan også oprette en ny adresse. Den nye adresse overføres som standard til projektet. Du kan dog angive, at den nye adresse kun er relevant for denne forekomst af tjenesten. Hvis du gør det, overføres den nye adresse ikke til projektet.

## <a name="create-a-customer-address-for-a-service-order"></a>Oprette en debitoradresse for en serviceordre

Hvis du vil føje en adresse til en serviceordre, skal du følge disse trin:

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.

2.  Åbn den serviceordre, som du vil oprette en adresse for.

3.  Klik på **Rediger** i **handlingsruden**, og klik derefter på **Overskriftsvisning**.

4.  Klik på **Tilføj** i oversigtspanelet **Tilføj adresse**.

5.  I formularen **Ny adresse** skal du indtaste et entydigt navn til adressen og udfylde de resterende felter. 
    

    > [!WARNING]
    > <P>Hvis du angiver det samme navn som en eksisterende adresse, overskriver de oplysninger, du angiver i resterende felter, oplysninger for den eksisterende adresse.</P>


6.  Klik på **OK** for at kopiere den nye adresse til serviceordren.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Angive en alternativ adresse på en serviceordre

Hvis du vil føje en alternativ adresse til en serviceordre, skal du følge disse trin:

1.  Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.

2.  Åbn den serviceordre, som du vil angive en alternativ adresse for.

3.  Klik på **Rediger** i **handlingsruden**, og klik derefter på **Overskriftsvisning**.

4.  Klik på **Tilføj** i oversigtspanelet **Anden adresse**.

5.  I formularen **Adressevalg** skal du i feltet **Posttype** vælge **Serviceordrer**.

6.  Vælg en adresse, og klik derefter på **OK** for at kopiere den til serviceordren.


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]