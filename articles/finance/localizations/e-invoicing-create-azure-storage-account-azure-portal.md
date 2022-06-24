---
title: Oprette en Azure-lagerkonto i Azure-portalen
description: Denne artikel forklarer, hvordan du kan oprette en Azure-lagerkonto til elektronisk fakturering.
author: dkalyuzh
ms.date: 02/14/2022
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
ms.openlocfilehash: 4380261140086bcb278162f8dc70b39eaa7078fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898012"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Oprette en Azure-lagerkonto i Azure-portalen

[!include [banner](../includes/banner.md)]

Alle elektroniske filer, der genereres af tjenesten Elektronisk fakturering eller går til tjenesten under behandling, gemmes i Microsoft Azure-lagerkontobeholderne. For at sikre, at elektronisk fakturering kan få adgang til disse containere, skal du angive den delte adgangssignaturs (SAS) token for lagerkontoen til tjenesten Elektronisk fakturering. Du skal desuden sikre dig, at tokenet er sikkert gemt, hvis du ikke angiver SAS-token direkte. Du kan i stedet gemme det i en Azure Key Vault og angive en Azure Key Vault-hemmelighed.

1. Åbn den lagerkonto, du planlægger at bruge sammen med tjenesten til elektronisk fakturering.
2. Gå til **Indstillinger** \> **Konfiguration**, og kontrollér, at parameteren **Tillad blob-offentlig adgang** er angivet til **Aktiveret**.
3. Gå til **Datalager** \> **Containere**, og opret en ny container.
4. Angiv et navn til containeren, og angiv feltet **Offentlig adgangsniveau** til **Privat (ingen anonym adgang)**.
5. Åbn den nye container, og gå til **Indstillinger** \> **Adgangspolitik**.
6. Vælg **Tilføj politik** for at tilføje en lagret adgangspolitik.
7. Angiv feltet **Identifikator** efter behov.
8. Vælg alle rettigheder i feltet **Rettigheder**.

    ![Alle de rettigheder, der er valgt i feltet Rettigheder i dialogboksen Tilføj politik.](media/e-invoicing-azure-1.png)

9. Angiv start- og slutdatoer. Slutdatoen skal være i fremtiden.
10. Vælg **OK** for at gemme politikken, og gem derefter ændringerne i containeren.
11. Gå til **Indstillinger** \> **Delte adgangstokener**, og angiv feltværdierne.
12. Angiv start- og slutdatoer. Slutdatoen skal være i fremtiden.
13. Vælg følgende rettigheder i feltet **Rettigheder**:

    - Læs
    - Tilføj
    - Opret
    - Skriv
    - Slet
    - Liste

14. Vælg **Generate SAS-token og URL**.
15. Kopier og gem værdien i feltet **Blob SAS URL**. Denne værdi vil blive brugt senere i denne procedure og vil blive henvist til som *URI for delt adgangssignatur*.
16. Åbn den Key Vault, du vil bruge sammen med elektronisk fakturering.
17. Gå til **Indstillinger** \> **Hemmeligheder**, og vælg derefter **Generér/importér** for at oprette en hemmelighed.
18. På siden **Opret en hemmelighed** skal du vælge **Manuel** i feltet **Uploadindstillinger**.
19. Angiv navnet på hemmeligheden. Dette navn bruges under konfigurationen af tjenesten i RCS (Regulatory Configuration Service) og vil blive henvist til som *det hemmelige Key Vault-navn*. Du kan finde flere oplysninger om RCS i [Konfigurere Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).
20. I feltet **Værdi** skal du indsætte den URI for delt adgangssignatur, du har kopieret tidligere.
21. Vælg **Opret**.
