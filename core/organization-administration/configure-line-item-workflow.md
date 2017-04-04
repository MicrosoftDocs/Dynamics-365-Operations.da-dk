---
title: Konfigurere en arbejdsgang for linjeelement
description: Dette emne forklarer, hvordan du konfigurerer et element i en arbejdsgang for linjeelement.
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 6c2b2c863d0783bd436db57d9fd3c7c5aa8dba5c
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-line-item-workflow"></a>Konfigurere en arbejdsgang for linjeelement

Dette emne forklarer, hvordan du konfigurerer et element i en arbejdsgang for linjeelement.

Hvis du vil konfigurere et element i en arbejdsgang for linjeelementer i arbejdsgangseditoren, skal du højreklikke på elementet og derefter klikke på **Egenskaber** for at åbne siden **Egenskaber**. Brug derefter nedenstående procedure til at konfigurere egenskaberne for et element i en arbejdsgang for linjeelementer.

## <a name="name-the-lineitem-workflow-element"></a>Navnet arbejdsgangselement lineitem
Udfør følgende trin for at angive et navn på et element i en arbejdsgang for linjeelementer.

1.  Klik på **Grundlæggende indstillinger** i venstre rude.
2.  Angiv et entydigt navn på elementet i en arbejdsgang for linjeelementer i feltet **Navn**.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Angive, om samme arbejdsgang bruges til at behandle alle linjeelementer
Udfør følgende trin for at angive, om samme arbejdsgang bruges til at behandle alle linjeelementer i et dokument.

1.  Klik på **Grundlæggende indstillinger** i venstre rude.
2.  Hvis samme arbejdsgang skal behandle alle linjeelementerne i et dokument, skal du klikke på **Aktivér én arbejdsgang for alle linjeelementer**. Vælg derefter den arbejdsgang, der skal bruges til behandling af linjeelementerne.
3.  Hvis en bestemt arbejdsgang skal behandle de linjeelementer, der opfylder et bestemt sæt betingelser, skal du klikke på **Aktivér en arbejdsgang for hvert linjeelement**. Udfør derefter følgende trin for at definere et sæt betingelser:
    1.  Klik på **Tilføj**.
    2.  Vælg betingelsen i tabellen.
    3.  Angiv et navn på det sæt betingelser, du definerer, under fanen **Betingelsesnavn**.
    4.  Klik på **Tilføj betingelse** for at angive betingelsen.
    5.  Angiv eventuelle supplerende betingelser, hvis det er påkrævede.
    6.  Hvis du vil kontrollere, om det sæt betingelser, du har angivet, er konfigureret korrekt, skal du klikke på **Test**. På siden **Test betingelse for arbejdsgang** i området **Valider betingelse** skal du vælge en post og derefter klikke på **Test**. Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret. Klik på **OK** eller **Annuller** for at vende tilbage til siden **Egenskaber**.

    Under fanen **Arbejdsgang** skal du vælge den arbejdsgang, der skal bruges til at behandle de linjeelementer, der opfylder et sæt betingelser, du har defineret.



