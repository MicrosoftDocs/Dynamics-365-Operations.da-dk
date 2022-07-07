---
title: Føje en adresse til en serviceordre
description: Denne artikel beskriver, hvordan du føjer en kundeadresse til en serviceordre.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015719"
---
# <a name="add-an-address-to-a-service-order"></a>Føje en adresse til en serviceordre

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du føjer en kundeadresse til en serviceordre. Når du opretter en serviceordre, overføres adresseoplysningerne fra det projekt, som serviceordren er tilknyttet. Du kan dog vælge en alternativ placering fra adresser, der allerede er angivet i Microsoft Dynamics AX for debitorer, kreditorer, websteder, lagre, serviceordrer og projekter.

Du kan også oprette en ny adresse. Den nye adresse overføres som standard til projektet. Du kan dog angive, at den nye adresse kun er relevant for denne forekomst af tjenesten. Hvis du gør det, overføres den nye adresse ikke til projektet.

## <a name="create-a-customer-address-for-a-service-order"></a>Oprette en debitoradresse for en serviceordre

Hvis du vil føje en adresse til en serviceordre, skal du følge disse trin:

1. Gå til **Servicestyring** \> **Serviceordrer** \> **Serviceordrer**.

1. Åbn den serviceordre, som du vil oprette en adresse for.

1. Åbn fanen **Overskrift**.

1. Udvid oversigtspanelet **Adresse**, og vælg derefter **Tilføj adresse** på værktøjslinjen i oversigtspanelet.

1. I dialogboksen **Ny adresse** skal du indtaste et entydigt navn til adressen og udfylde de resterende felter. 

    > [!WARNING]
    > Hvis du angiver det samme navn som en eksisterende adresse, overskriver de oplysninger, du angiver i resterende felter, oplysninger for den eksisterende adresse.

1. Vælg **OK** for at kopiere den nye adresse til serviceordren.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Angive en alternativ adresse på en serviceordre

Hvis du vil føje en alternativ adresse til en serviceordre, skal du følge disse trin:

1. Gå til **Servicestyring** \> **Serviceordrer** \> **Serviceordrer**.

1. Åbn den serviceordre, som du vil angive en alternativ adresse for.

1. Åbn fanen **Overskrift**.

1. Udvid oversigtspanelet **Adresse**, og vælg derefter **Anden adresse** på værktøjslinjen i oversigtspanelet.

1. I dialogboksen **Valg af adresse** skal du vælge **Serviceordrer** på rullelisten over den gitteret.

1. Vælg en adresse, og vælg derefter **OK** for at kopiere den til serviceordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]