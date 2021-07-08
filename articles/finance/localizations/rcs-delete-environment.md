---
title: Regulatory Configuration Service (RCS) – Slette et RCS-miljø
description: I dette emne forklares, hvordan en RCS-systemadministrator (Regulatory Configuration Service) kan slette et RCS-miljø og relaterede data.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295812"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) – Slette et RCS-miljø

[!include [banner](../includes/banner.md)]

I dette emne forklares, hvordan en RCS-systemadministrator (Regulatory Configuration Service) kan slette et RCS-miljø og relaterede data.

Før du kan fuldføre trinnene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:

- Du skal have tildelt rollen **Systemadministrator** for RCS-miljøet.
- Rollen **Systemadministrator** skal være tildelt rollen **RCSDeleteEnvironmentDuty**.

## <a name="delete-an-rcs-environment"></a>Slette et RCS-miljø

1. Åbn RCS, og vælg arbejdsområdefeltet **Elektronisk rapportering**.
2. Vælg **Slet RCS-miljø** i afsnittet **Relaterede links**.

    ![Linket Slet RCS-miljø i afsnittet Relaterede links](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. Gennemse meddelelserne om området for sletning af miljøet i den dialogboks, der vises.

    ![Meddelelser i dialogboksen Slet RCS-miljø](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > Du kan ikke fortryde sletning af et RCS-miljø.
    >
    > Handlingen sletter det valgte RCS-miljø og eventuelle relaterede data, herunder funktioner og konfigurationer, der er lagret i det globale lager. Funktioner og konfigurationer, der deles med andre organisationer, deles ikke længere og slettes, hvis de ikke har nogen afhængigheder. Funktioner og konfigurationer, der har afhængigheder, markeres som afbrudt.

4. I det felt, der er angivet, skal du angive RCS-miljøets GUID (Global Unique Identifier) for at bekræfte, at du vil slette det. Miljøets GUID medtages i meddelelsen om sletning.
5. Vælg **Slet miljø**.
    
RCS-miljøet og eventuelle relaterede data er nu slettet.

> [!IMPORTANT]
> Når du har slettet et RCS-miljø, kan dataene ikke gendannes. Der kan oprettes et nyt RCS-miljø i alle tilgængelige RCS-områder.
