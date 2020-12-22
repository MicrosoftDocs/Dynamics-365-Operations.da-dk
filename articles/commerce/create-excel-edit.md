---
title: Oprette en Excel-projektmappe for at redigere detailtransaktioner
description: Dette emne beskriver, hvordan du opretter en Excel-projektmappe, så du kan redigere detailtransaktioner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2b6e98db54e7747912aad26f4b8ae24b9ad5a6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458728"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>Oprette en Excel-projektmappe for at redigere detailtransaktioner

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opretter en Excel-projektmappe, så du kan redigere detailtransaktioner i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Der er en foruddefineret Excel-skabelon, som kunder kan få adgang til fra forskellige dele af systemet og bruge til at redigere og overvåge detailtransaktioner. Kunder kan også oprette en brugerdefineret Excel-projektmappe til dette formål.

## <a name="create-and-configure-an-excel-workbook"></a>Oprette og konfigurere en Excel-projektmappe

Hvis du vil oprette og konfigurere en Excel-projektmappe, så du kan redigere detailtransaktioner, skal du følge disse trin.

1. Åbn Excel, og opret en tom projektmappe.
1. Vælg **Mine tilføjelsesprogrammer** på fanen **Indsæt**.
1. Vælg linket **Tilføj serveroplysninger** i højre rude.
1. Angiv URL-adressen til serveren, og vælg derefter **OK**.
1. Hvis du modtager fejlmeddelelsen "Der blev ikke fundet nogen applet-registreringer", skal du følge disse trin for at løse problemet:

    1. I Commerce skal du gå til **Systemadministration \> Opsætning \> Parametre for Office-apps**.
    1. Vælg **Initialiser app-parametre** på oversigtspanelet **App-parametre**.
    1. Vælg **OK** i boksen med bekræftelsesmeddelelsen.
    1. Vælg **Initialiser applet-registrering** på oversigtspanelet **Registrerede applets**.
    1. Gentag de forrige tre trin efter behov.

1. Vælg **Design**, og vælg derefter **Tilføj tabel**.
1. På baggrund af de data, der skal ændres, skal du vælge de enheder, der skal føjes til Excel-projektmappen til redigering. Brug følgende tabel som reference.

    | Transaktionstype | Dataenheder, der skal bruges |
    |------------------|----------------------|
    | Cash and carry-transaktioner, onlineordrer, asynkrone kundeordrer, asynkrone kundetilbud | Transaktion (reviderbar), salgstransaktion (reviderbar), betalingstransaktioner (reviderbare), momstransaktioner (reviderbare), rabattransaktioner (reviderbare), gebyrtransaktioner (reviderbare) |
    | Indsættelse i banken | Transaktion (reviderbar), betalingsmiddeltransaktioner i banken (reviderbare) |
    | Deponering til pengeskab | Transaktion (reviderbar), betalingsmiddeltransaktioner lagt i pengeskab (reviderbare) |
    | Kasseoptælling | Transaktion (reviderbar), betalingsmiddeltransaktioner med kasseoptælling (reviderbare) |
    | Indtægt, udgift | Transaktioner (reviderbare), indkomst-/udgiftstransaktioner (reviderbare), betalingstransaktioner (reviderbare) |
    | Angive startbeløb, fjernelse af betalingsmiddel, kassebeholdning, betalingsmiddel for byttepenge, fakturabetaling, kundeindbetalinger | Transaktion (reviderbar), betalingstransaktioner (reviderbare) |

    > [!NOTE]
    > Det er vigtigt, at du kun føjer én dataenhed til hver enkelt Excel-projektmappe. Desuden skal alle felter, der er markeret med et nøglesymbol, føjes til den relevante projektmappe.

1. Når projektmappen er konfigureret, skal du anvende de påkrævede filtre. Sørg for at anvende de samme filtre på alle regneark i filen. Undgå at indlæse meget store datamængder i Excel-filen. Ellers kan ydeevnen påvirkes, og Excel og dit system kan blive langsommere. Det anbefales, at du altid bruger "Firma" og enten "Opgørelsesnummer" eller "Transaktionsnummer" som filtre til filen.
1. Når filtrene er konfigureret, skal du vælge **Opdater** for at indlæse dataene.
1. Rediger de nødvendige data, og publicer dem derefter. Hvis knappen **Publicer** ikke er tilgængelig, er nogle nøglefelter sandsynligvis ikke føjet til Excel-projektmappen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere og overvåge cash and carry-transaktioner og kassestyringstransaktioner](edit-cash-trans.md)

[Redigere og overvåge onlineordre- og asynkrone kundeordretransaktioner](edit-order-trans.md)

[Redigere økonomiske dimensioner for detailtransaktioner](edit-financial-dim.md)

[Føje felter til en Excel-projektmappe for at redigere detailtransaktioner](add-fields-excel.md)
