---
title: Fuldføre, publicere og udrulle en globaliseringsfunktion
description: Dette emne indeholder oplysninger om livscyklussen for globaliseringsfunktioner.
author: dkalyuzh
ms.date: 12/15/2021
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
ms.openlocfilehash: 21e03660387c7e715bc0f4cb1dbcd3ec9ec6cee2
ms.sourcegitcommit: 1843235766b6f8cf950a13a310e9f4f2f53c59a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/07/2022
ms.locfileid: "8554555"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Fuldføre, publicere og udrulle en globaliseringsfunktion

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Funktionsversioner af elektronisk fakturering

Funktioner til elektronisk fakturering er versionsstyret. Når der oprettes en ny version, øges versionsnummeret automatisk.

Funktionsversioner til elektronisk fakturering følger en livscyklus, der har op til tre statusser:

- **Kladde** - Hvis en funktionsversion har denne status, kan du redigere dens konfigurationsattributter og alle dens genstande (f.eks. filformatkonfigurationer).
- **Fuldført** – Denne status angiver, at du er færdig med at redigere funktionsversionen og ikke vil foretage flere opdateringer af den. Hvis en funktionsversion har denne status, kan du ikke længere redigere den eller nogen af dens komponenter.
- **Publiceret** – Hvis en funktionsversion har denne status, er den publiceret til det globale lager, der er tilknyttet din organisation. Hvis en funktionsversion har denne status, kan du ikke længere redigere den eller nogen af dens komponenter.

Du kan angive en **Gyldig fra**-dato for en ny version af en elektronisk faktureringsfunktion. På denne måde kan du definere en standardversion, der kan bruges, eller som kan overskrives, når funktionen implementeres i servicemiljøet.

Hvis du vil ændre status for en version af funktionen til elektronisk fakturering, skal du følge disse trin.

1. Logge på din RCS-konto (Regulatory Configuration Service).
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Elektronisk fakturering**.
3. På siden **Funktioner til elektronisk fakturering** skal du i venstre side vælge funktionen til elektronisk fakturering.
4. Vælg versionen under fanen **Versioner** til højre på siden.
5. Vælg **Skift status**, og vælg derefter **Fuldført** (hvis den aktuelle status er **Kladde**) eller **Publiceret** (hvis den aktuelle status er **Fuldført**).
6. Vælg **Ja** for at bekræfte anmodningen i meddelelsesboksen.

Det er valgfrit, om du vil ændre manuelt fra **Fuldført** status til **Publiceret** status. Funktionsversioner til elektronisk fakturering opdateres automatisk til **Publiceret** status, når de udrulles til servicemiljøet.

Du kan spore statussen i kolonnen **Funktionsversionsstatus** under fanen **Versioner**.

## <a name="deploy-feature-versions"></a>Udrulle funktionsversioner

I RCS bruger du kommandoen **Udrul** til at publicere en version af funktionen Elektronisk fakturering til målservicemiljøet eller det tilknyttede program.

1. På siden **Funktioner til elektronisk fakturering** skal du i venstre side vælge funktionen til elektronisk fakturering.
2. Under fanen **Versioner** i højre side skal du vælge den elektroniske faktureringsfunktionsversion, du vil udrulle i servicemiljøet eller det tilknyttede program. Den valgte version skal have status som **Fuldført** eller **Publiceret**.
3. Vælg **Udrul**, og vælg derefter en af eller begge følgende indstillinger for at definere destinationen for installationen:

    - **Tilknyttet program** – Den konfiguration, der leveres af programopsætningen, skrives i den forekomst af Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management, som tidligere er knyttet til det.
    - **Servicemiljø** – Versionen af funktionen til elektronisk fakturering udrulles til servicemiljøet. Elektronisk fakturering er derefter klar til at modtage og behandle elektroniske dokumenter, som Finans eller Supply Chain Management sender.

> [!NOTE]
> Normalt skal du ændre parametrene for den ER-funktion (elektronisk rapportering), der skal implementeres i servicemiljøet. Der vil sjældent være ændringer af det tilknyttede program. Du skal kun udrulle nye versioner til det tilknyttede program, når du ændrer de tilsvarende parametre i programmet.

Hvis du vil se, om en bestemt version af en funktion til elektronisk fakturering er udrullet til et bestemt miljø, kan du gennemse oplysningerne under fanen **Miljøer**.

## <a name="remove-feature-versions"></a>Fjerne funktionsversioner

I RCS kan du vælge **Annuller** for at fjerne en bestemt elektronisk faktureringsfunktionsversion fra et servicemiljø, hvis den er udrullet i miljøet.

> [!IMPORTANT]
> Knappen **Annuller** fungerer kun i tjenestemiljøer. Den fjerner ikke noget fra det tilknyttede program for den aktuelle elektroniske faktureringsfunktion.

## <a name="rebase-electronic-invoicing-features"></a>Rebasere funktioner til elektronisk fakturering

Når en funktion til elektronisk fakturering afledes af en anden, kan du vælge **Rebaser** for at opdatere den afledte funktion med de ændringer, der er indført i den oprindelige (overordnede) funktion.

Hvis du vil rebasere en afledt version af en funktion, som du har oprettet, skal du følge disse trin.

1. Hent den seneste version af funktionen ved at importere den fra det globale lager. Du kan finde flere oplysninger under [Importere en funktion fra det globale lager](e-invoicing-import-feature-global-repository.md).
2. Vælg den funktion, der skal rebaseres, på listen over funktioner.
3. Under fanen **Versioner** skal du vælge **Ny** for at oprette en kladdeversion.
4. Vælg **Rebaśer**.
5. I dialogboksen **Rebasér** skal du vælge den version af funktionen, der skal rebaseres til.
6. Vælg **OK**.
7. Gennemgå funktionskomponenterne, og foretag eventuelle nødvendige ændringer.
8. Vælg **Skift status** for at fuldføre den rebaserede funktion. Når rebaseringen er fuldført, kan du udføre yderligere handlinger.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Få en specifik version af funktioner til elektronisk fakturering

Når du opretter en ny version af en funktion til elektronisk fakturering, opretter systemet en kopi af den seneste funktionsversion. Hvis du vil bruge en tidligere version af funktionen som basis for en ny version, skal du vælge versionen og derefter vælge **Hent denne version**. Der oprettes en ny kladdeversion af funktionen, som er en kopi af den valgte version.
