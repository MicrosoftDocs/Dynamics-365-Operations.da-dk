---
title: Kundecertifikater og -hemmeligheder
description: Denne artikel beskriver, hvordan du konfigurerer kundecertifikater og -hemmeligheder i Elektronisk fakturering.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 3943e7cb43cc6bf93995f0b3957766227cc3ec99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279834"
---
# <a name="customer-certificates-and-secrets"></a>Kundecertifikater og -hemmeligheder

[!include [banner](../includes/banner.md)]

Hvis du allerede har en Microsoft Azure Key Vault-reference i Regulatory Configuration Service (RCS), kan du oprette referencer til Key Vault-certifikater og -hemmeligheder. Hvis du endnu ikke har en reference til Key Vault, kan du finde flere oplysninger om, hvordan den oprettes, i [Servicemiljøer](e-invoicing-service-environments.md).

## <a name="create-certificates-and-secrets"></a>Oprette certifikater og hemmeligheder

Følg disse trin for at oprette og konfigurere certifikater og hemmeligheder.

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktionen** i sektionen **Miljø** skal du vælge feltet **Elektronisk fakturering**.
3. På siden **Miljøkonfiguration** skal du vælge **Servicemiljøer** i handlingsruden.
4. På siden **Tjenestemiljøer** skal du i handlingsruden vælge **Key Vault-parametre**.
5. Vælg en Key Vault-reference på siden **Key Vault-parametre**, og vælg derefter **Tilføj** i sektionen **Certifikater**.
6. Angiv navnet på Key Vault-certifikatet eller -hemmeligheden i feltet **Navn**. Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto i Azure-portalen](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Indtast en beskrivelse i feltet **Beskrivelse**.
8. Vælg **Certifikat** i feltet **Type**, hvis du refererer til det certifikat, der er gemt i Key Vault. Vælg **Hemmelighed**, hvis du refererer til den hemmelighed, der gemmes i Key Vault.
9. Vælg **Gem**.

> [!NOTE]
> I nogle tilfælde skal du bruge offentlige certifikater, der har filtypenavnet .cer. Key Vault understøtter dog ikke import og lagring af certifikater af denne type som Key Vault-certifikater. I disse tilfælde skal du gemme .cer-filen som en Base-64-kodet X.509-streng (.CER). Gem derefter i Key Vault den streng, der vises mellem linjen **BEGYND CERTIFIKAT** og linjen **AFSLUT CERTIFIKAT** i filen. I servicemiljøet skal du stadig oprette en reference til Key Vault-posten og indstille feltet **Type** til **Certifikat**.

## <a name="create-a-chain-of-certificates"></a>Oprette en certifikatkæde

Hvis dine land/område-specifikke fakturaer kræver en kæde af certifikater for at anvende digitale signaturer eller oprette en sikker (Secure Sockets Layer \[SSL\])-forbindelse til eksterne webtjenester, skal du oprette en kæde af certifikater, hvor certifikaterne er i følgende rækkefølge:

1. Rodcertifikater
2. Mellemcertifikater
3. Slutbrugercertifikater

Rodnøglecentre (CA'er) er en betroet kilde til certifikater. CA-mellemcertifikater er broer, der sammenkæder slutbrugercertifikaterne med CA-rodcertifikaterne.

Følg disse trin for at oprette og konfigurere en kæde af certifikater.

1. På siden **Key Vault-parametre** skal du i handlingsruden vælge **Kæde af certifikater**.
2. Vælg **Ny** for at oprette en kæde af certifikater.
3. Angiv navnet på kæden af certifikater i feltet **Navn**.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. I afsnittet **Certifikater** skal du vælge **Tilføj** for at føje et certifikat til kæden.
6. Brug knappen **Op** eller **Ned** til at ændre certifikatets placering i kæden. Behold CA-rodcertifikatet øverst på listen og slutbrugercertifikatet nederst.
7. Vælg **Gem**.

Du kan oprette lige så mange Key Vault-referencer i RCS, som du vil. Husk, at token for hemmeligheden til den delte adgangssignatur (SAS) bruges til at knytte et givent servicemiljø til Key Vault-referencen. Du kan referere til Key Vault-certifikater og -hemmeligheder, der er lagret i en Key Vault, som også indeholder hemmeligheden til det lager SAS-token, som du bruger, når du konfigurerer servicemiljøet.
