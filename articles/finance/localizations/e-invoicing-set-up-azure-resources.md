---
title: Konfigurere Azure-ressourcer til elektronisk fakturering
description: Denne artikel indeholder en oversigt over processen til opsætning af Microsoft Azure-ressourcer til elektronisk fakturering.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c5b7b2ca4d7733fb1c75ded8798655699284fe1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907723"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Konfigurere Azure-ressourcer til elektronisk fakturering

[!include [banner](../includes/banner.md)]

Processen til opsætning af Microsoft Azure-ressourcer til elektronisk fakturering har tre trin. De første to trin, "Oprette en Azure Key Vault i Azure-portalen" og "Oprette en Azure-lagerkonto i Azure-portalen", er obligatoriske. Det tredje trin, "Konfigurere en SharePoint-forbindelse", er valgfrit.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Oprette en Azure Key Vault i Azure-portalen

Opret en Key Vault i dit Azure-abonnement. Det anbefales, at du opretter en separat Key Vault til elektronisk fakturering, og at du ikke kombinerer hemmeligheder med andre programmer. Opret lige så mange hemmeligheder og certifikater, du har brug for til dine scenarier i elektroniske dokumenter. Du skal oprette mindst én hemmelighed til at gemme token for delt adgangssignatur (SAS) til den Azure-lagerkontoen, du skal oprette i næste trin.

Du kan finde oplysninger om, hvordan du fuldfører dette trin, i [Oprette en Azure Key Vault i Azure-portalen](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Oprette en Azure-lagerkonto i Azure-portalen

Du ejer alle de elektroniske dokumenter og filer, der genereres af den elektroniske faktureringsservice eller ankommer i tjenesten. Disse dokumenter og filer gemmes i en Azure-lagerkonto, som du opretter i dit Azure-abonnement. Tjenesten giver adgang til din lagerkonto ved hjælp af SAS-token, der er taget fra din Key Vault-hemmelighed.

Du kan finde oplysninger om, hvordan du fuldfører dette trin, i [Oprette en Azure-lagerkonto i Azure-portalen](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>Konfigurere en SharePoint-forbindelse

I nogle tilfælde kan du være nødt til at gemme elektroniske filer i SharePoint og hente dem fra SharePoint. Du kan sikre, at den elektroniske faktureringstjeneste har adgang til dine SharePoint-mapper, ved at konfigurere adgang til SharePoint.

Du kan finde oplysninger om, hvordan du fuldfører dette trin, under [Konfigurere en SharePoint-forbindelse](e-invoicing-create-sharepoint-connection.md).
