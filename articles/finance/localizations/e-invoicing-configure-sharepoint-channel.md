---
title: Konfigurere en SharePoint-kanal
description: Denne artikel forklarer, hvordan du konfigurerer en Microsoft SharePoint-kanal til behandling af indgående elektroniske fakturaer.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 92eaa357c6d72cc637d4ce353702e5d41ecf4338
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272298"
---
# <a name="configure-a-sharepoint-channel"></a>Konfigurere en SharePoint-kanal

[!include [banner](../includes/banner.md)]

Før du kan konfigurere en Microsoft SharePoint-kanal for at behandle indgående dokumenter, skal du udføre de trin, der er beskrevet i [Konfigurere en SharePoint-forbindelse](e-invoicing-create-sharepoint-connection.md).

Du kan derefter bruge SharePoint-kanalen til at importere elektroniske kreditorfakturaer fra filer, der er gemt i dine SharePoint-mapper.

1. Opret følgende mapper på dit SharePoint-websted:

    - **Hovedmappe** – Den mappe, som tjenesten behandler filer fra.
    - **Arkivmappe** – Den mappe, hvor de behandlede filer gemmes.
    - **Fejlmappe** – Den mappe, som systemet flytter filer til, hvis behandlingen mislykkes.

2. Vælg den funktion til elektronisk fakturering, du har oprettet, i RCS (Regulatory Configuration Service). Sørg for at vælge den version, der har status af **Kladde**.
3. Vælg **Tilføj** under fanen **Konfigurationer**.
4. Vælg indstillingen **Brugerdefineret opsætning**, i feltgruppen **Ny** i dialogboksen **Opret funktionsopsætning**.
5. I feltgruppen **Opsætningstype** skal du vælge indstillingen **Datakanal**.
6. Vælg **SharePoint**-mappe i feltet **Vælg datakanal**.
7. Vælg **Opret**.
8. Vælg den linje, du oprettede, og vælg derefter **Rediger**.
9. Angiv følgende obligatoriske felter i afsnittet **Parametre** under fanen **Datakanal**.

    | Felt                 | Beskrivelse |
    |-----------------------|-------------|
    | Datakanal          | Angiv et entydigt navn til identifikation af datakanalen. Navnet må højst være på 10 tegn. Der vil blive refereret til den i anvendelighedsreglerne og i tilknyttede programmer under kommunikationsprocessen. |
    | SharePoint-adresse    | Angiv SharePoint-URL-adressen. Angiv for eksempel `<domain>.sharepoint.com`. |
    | Program-id        | Vælg navnet på Azure Key Vault-hemmeligheden, der indeholder id'et for SharePoint-brugerkontoen. Denne hemmelighed skal oprettes i Key Vault og konfigureres i dit servicemiljø. Værdien er **Program-id (klient)** fra [Konfigurere SharePoint-forbindelse](e-invoicing-create-sharepoint-connection.md). |
    | Programhemmelighed    | Vælg navnet på Key Vault-hemmeligheden, der indeholder adgangskoden til SharePoint-brugerkontoen. Værdien er **Appregistreringshemmelighed** fra [Konfigurere SharePoint-forbindelse](e-invoicing-create-sharepoint-connection.md). |
    | Navn på sted             | Angiv navnet på SharePoint-webstedet. |
    | Navn på dokumentbibliotek | Angiv navnet på SharePoint-dokumentbiblioteket. |
    | Timeout               | Angiv den maksimale tid i millisekunder (ms), som systemet skal vente på et svar. Standardværdien er 10.000 ms (10 sekunder). |
    | Hovedmappe           | Angiv filens importkilde eller den mappe, som tjenesten skal behandle filer fra. |
    | Arkivmappe        | Angiv den mappe, hvor de behandlede filer skal gemmes. |
    | Fejlmappe          | Angiv den mappe, som systemet skal flytte filer til, hvis behandlingen mislykkes. |
    | Den maksimale filstørrelse         | Angiv den maksimale størrelse i byte på en enkelt fil, der behandles. Standardværdien er 20.000.000 byte. |
    | Maksimalt antal filer      | Angiv det maksimale antal filer, der skal behandles i en enkelt handling. Hvis du ikke vil begrænse antallet af filer, skal du angive værdien til **0** (nul). |
    | Filfilter           | Angiv en streng, der skal filtreres efter filnavn. Dette felt er valgfrit. En simpel maske som f.eks. **\*smth\*.ext** understøttes, hvor hver stjerne (\*) repræsenterer nul eller flere forekomster af et tegn. Angiv f.eks. **\*.pdf** for at konfigurere kanalen til at læse PDF-filer. |
    | Brugerdefineret filnavn      | Angiv det brugerdefinerede filnavn fra klienten. |

10. Gennemse og opdater kriterierne under fanen **Anvendelighedsregler**, hvis det er nødvendigt. Værdien i feltet **Kanal** skal være lig med den værdi, du angav i feltet **Datakanal** i det foregående trin.
11. Vælg **Gem**, og luk siden.
