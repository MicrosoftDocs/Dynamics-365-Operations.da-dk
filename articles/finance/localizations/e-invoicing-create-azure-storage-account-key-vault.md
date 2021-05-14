---
title: Oprette en Azure Storage-konto og Key Vault
description: Dette emne forklarer, hvordan du kan oprette en Azure Storage-konto og Key Vault.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5c2ddad10f9cbedd77a04fe0f42bdc217fd43344
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963233"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Oprette en Azure Storage-konto og Key Vault

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Forudsætninger

Før du kan fuldføre trinene i dette emne, skal du sørge for, at følgende opgaver er fuldført:

- Opret en ny Key Vault-ressource i Azure. Du kan finde flere oplysninger i [Om Azure Key Vault](/azure/key-vault/general/overview).
- Opret en Azure Storage-konto (Blob-lager). Du kan finde flere oplysninger i [Vedligeholde en Azure Storage-konbo](/azure/storage/blobs/).

## <a name="overview"></a>Overblik

I dette emne skal du fuldføre to hovedtrin:

- Konfigurer Azure Storage-kontoen for at hente URI'en til lagerkontoen.
- Konfigurer Key Vault'en til opbevaring af URI'en for lagerkontoen.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Konfigurere Azure Storage-kontoen for at hente URI'en til lagerkontoen

1. Åbn den lagerkonto, du planlægger at bruge sammen med elektronisk fakturering.
2. Gå til **Blob service** \> **Containere**, og opret en ny container.
3. Angiv et navn til containeren, og angiv feltet **Offentlig adgangsniveau** til **Privat (ingen anonym adgang)**.
4. Åbn containeren, og gå til **Indstillinger \> Adgangspolitik**.
5. Vælg **Tilføj politik** for at tilføje en lagret adgangspolitik.
6. Angiv felterne **Identifikator** og **Rettigheder** efter behov. Vælg alle rettigheder i feltet **Rettigheder**.

    ![Tildele tilladelse til Blob-lager](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Angiv start- og udløbsdatoerne. Udløbsdatoen skal være i fremtiden.
8. Vælg **OK** for at gemme politikken, og gem derefter ændringerne i containeren.
9. Vend tilbage til lagerkontoen, og åbn **Lagercenter (prøveversion)**.
10. Højreklik på containeren, og vælg derefter **Hent delt adgangssignatur**.
11. I dialogboksen **Delt adgangssignatur** skal du kopiere og gemme værdien i feltet **URI**. Denne værdi vil blive brugt i den næste procedure og vil blive henvist til som *URI for delt adgangssignatur*.

    ![Vælge og kopiere URI-værdien](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Konfigurere Key Vault'en til opbevaring af URI'en for lagerkontoen

1. Åbn den Key Vault, du vil bruge sammen med elektronisk fakturering.
2. Gå til **Indstillinger** \> **Hemmeligheder**, og vælg derefter **Generer/importer** for at oprette en ny hemmelighed.
3. På siden **Opret en hemmelighed** skal du vælge **Manuel** i feltet **Uploadindstillinger**.
4. Angiv navnet på hemmeligheden. Dette navn bruges under konfigurationen af tjenesten i RCS (Regulatory Configuration Service) og vil blive henvist til som *det hemmelige Key Vault-navn*.
5. Vælg **URI for delt adgangssignatur** i feltet **Værdi**, og vælg derefter **Opret**.
6. Konfigurer adgangspolitikken for at tildele elektronisk fakturering det korrekte niveau for sikker adgang til den hemmelighed, du har oprettet. Gå til **Indstillinger \> Adgangspolitik**, og vælg **Tilføj adgangspolitik**.
7. Angiv de hemmelige tilladelser til handlingerne **Get** og **List**.

    ![Tildele tjenesteadgang](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Angiv certifikattilladelserne til handlingerne **Get** og **List**.

    ![Tildele certifikattilladelse](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Vælg **Ingen valgt** i feltet **Vælg sikkerhedskonto**.
10. I dialogboksen **Sikkerhedskonto** skal du vælge sikkerhedskontoen ved at tilføje **e-faktureringstjeneste**.
11. Vælg **Tilføj**, og vælg derefter **Gem Key Vault-ændringer**.
12. På siden **Oversigt** skal du kopiere værdien **DNS-navn** for Key Vault. Denne værdi vil blive brugt under konfigurationen af tjenesten i RCS og vil blive henvist til som *URI for Key Vault*.

> [!NOTE]
> Hvis du vil øge sikkerheden for lagringskontoen, kan du konfigurere Azure Defender for Storage.
> 
> Du kan finde flere oplysninger i [Introduktion til Azure Defender for Storage](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
