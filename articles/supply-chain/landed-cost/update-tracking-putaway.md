---
title: Opdateringssporing for læg på lager
description: Denne artikel indeholder en beskrivelse af, hvordan du kan konfigurere og køre den periodiske opgave Opdateringssporing for læg på lager.
author: Weijiesa
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b36fe5a9828ea018881f08b8af27d77cdf0babc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882599"
---
# <a name="update-tracking-for-put-away"></a>Opdateringssporing for læg på lager

[!include [banner](../includes/banner.md)]

Den periodiske opgave *Opdateringssporing for læg på lager* er beregnet til at blive kørt som et tilbagevendende batchjob om natten. Den identificerer, hvilke fragter der har modtaget alle lagertransaktioner, og hvilke fragter der ikke har en værdi for den faktiske slutdato. Derefter angives den faktiske slutdato til dags dato efter behov.

Der oprettes *containeraktiviteter* for hver *etape* af en rejse for hver *forsendelsescontainer*. Disse værdier defineres af den rejseskabelon, der vælges, når der oprettes en fragt. For hver containeraktivitetspost kan der angives værdier for felterne **Startdato**, **Forventet slutdato** og **Faktisk slutdato**. Disse felter kan opdateres, når der modtages bekræftelse af, at en etape er startet eller er fuldført.

Oplysninger, der er relateret til bekræftede datoer, leveres typisk af tredjepart, f.eks. en speditør, da disse handlinger vedligeholdes uden for Microsoft Dynamics 365 Supply Chain Management. Oplysninger fra tredjepart kræves dog ikke for at spore varernes modtagelse fra en etape til lagerstedet (som markeret af læg varer på lager). Sporing kan derfor bestemmes på basis af oplysningerne i Dynamics 365 Supply Chain Management.

Hvis du vil konfigurere og køre den periodiske opgave *Opdateringssporing for læg på lager*, skal du følge disse trin.

1. Gå til **Landingsomkostninger \> Periodiske opgaver \> Opdateringssporing for læg på lager**.
1. Angiv følgende felter i afsnittet **Parametre** i dialogboksen **Opdateringssporing for læg på lager**:

    - **Etape** – Vælg det entydige id-navn/nummer for den del af en rejse, som du vil opdatere sporing for. Den valgte værdi skal repræsentere modtagelsen af fragten på lagerstedet.
    - **Aktivitet** – Vælg den aktivitet, der blev udført under den valgte etape. Disse værdier tildeles pr. rejseskabelonlinje i sporingskontrolcenteret.

1. Hvis du vil begrænse, hvilke poster der skal medtages i opdateringen, skal du vælge knappen **Filter** i oversigtspanelet **Poster, der skal indgå**. Der vises en standarddialogboks til forespørgsler, hvor du kan definere udvælgelseskriterier, sorteringskriterier og joinforbindelser. Felterne fungerer på samme måde som for andre typer af forespørgsler i Supply Chain Management. Felterne her er skrivebeskyttede og viser værdier, der er relateret til forespørgslen.
1. I oversigtspanelet **Kør i baggrunden** skal du konfigurere batch- og planlægningsindstillinger efter behov på samme måde som ved andre typer af batchjob i Supply Chain Management.
1. Vælg **OK**, hvis du vil anvende indstillingerne og køre eller planlægge opdateringen.
