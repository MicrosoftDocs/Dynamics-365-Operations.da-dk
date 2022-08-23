---
title: Regulatory Configuration Service (RCS) – Slette et RCS-miljø
description: Denne artikel forklarer, hvordan en RCS-systemadministrator (Regulatory Configuration Service) kan slette et RCS-miljø og relaterede data.
author: kfend
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, System Admin
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
ms.openlocfilehash: bdcb6820ead72fce0f89bf80cc5e474cb3942724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277202"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) – Slette et RCS-miljø

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan en RCS-systemadministrator (Regulatory Configuration Service) kan slette et RCS-miljø og relaterede data.

Før du kan fuldføre trinnene i denne artikel, skal du kontrollere, at følgende forudsætninger er opfyldt:

- Du skal have tildelt rollen **Systemadministrator** for RCS-miljøet.
- Rollen **Systemadministrator** skal være tildelt rollen **RCSDeleteEnvironmentDuty**.

## <a name="delete-an-rcs-environment"></a>Slette et RCS-miljø

1. Åbn RCS, og vælg arbejdsområdefeltet **Elektronisk rapportering**.
2. Vælg **Slet RCS-miljø** i afsnittet **Relaterede links**.

    ![Linket Slet RCS-miljø i afsnittet Relaterede links.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. Gennemse meddelelserne om området for sletning af miljøet i den dialogboks, der vises.

    ![Meddelelser i dialogboksen Slet RCS-miljø.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > Du kan ikke fortryde sletning af et RCS-miljø.
    >
    > Handlingen sletter det valgte RCS-miljø og eventuelle relaterede data, herunder funktioner og konfigurationer, der er lagret i det globale lager. Funktioner og konfigurationer, der deles med andre organisationer, deles ikke længere og slettes, hvis de ikke har nogen afhængigheder. Funktioner og konfigurationer, der har afhængigheder, markeres som afbrudt.

4. I det felt, der er angivet, skal du angive RCS-miljøets GUID (Global Unique Identifier) for at bekræfte, at du vil slette det. Miljøets GUID medtages i meddelelsen om sletning.
5. Vælg **Slet miljø**.
    
RCS-miljøet og eventuelle relaterede data er nu slettet.

> [!IMPORTANT]
> Når du har slettet et RCS-miljø, kan dataene ikke gendannes. Der kan oprettes et nyt RCS-miljø i alle tilgængelige RCS-områder.
