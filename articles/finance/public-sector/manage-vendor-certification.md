---
title: Bevare kreditorcertificering
description: Denne artikel beskriver den fremgangsmåde, som leverandører kan bruge til at bevare deres certificeringer ved hjælp af arbejdsområdet Kreditorsamarbejde.
author: v-kiarnd
ms.date: 04/27/2021
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 37990292748c363f44d306bda0263dd117808eb1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891431"
---
# <a name="maintain-vendor-certification"></a>Bevare kreditorcertificering

[!include [banner](../includes/banner.md)]

Denne artikel beskriver den fremgangsmåde, som dine kreditorer kan bruge til at bevare deres certificeringer ved hjælp af **arbejdsområdet Kreditorsamarbejde**. Eksempler på certificeringer kan omfatte en virksomhed af typen Woman Business Enterprise (WBE) eller Leadership in Energy and Environment Design (LEED). Kreditorer skal angive certificeringsoplysninger i arbejdsområdet **Kreditoroplysninger**. Derfra vælger kreditorerne vælge **Flere detaljer** og derefter **Certificeringer**.

## <a name="turn-on-the-vendor-certification-feature"></a>Aktivere funktionen til kreditorcertificering

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge siden [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul** - *Kreditor*
- **Funktionsnavn** - *Aktiver styring af certificeringer til kreditorsamarbejde*

## <a name="add-a-new-certification"></a>Tilføje en ny certificering

Hvis du vil tilføje en ny certificering, skal du vælge knappen **Tilføj**, der er placeret over gitteret for **Certificering** i arbejdsområdet **Kreditoroplysninger**. Angiv følgende oplysninger:

- Certificeringsnummer
- Certificeringstype
- Certificeringsorganisation
- Certificeringsdato
- Forpligtelsesbeløb, hvis det er relevant
- Ikrafttrædelsesdato
- Udløbsdato
- Kommentarer, valgfrit

Hvis der er dokumenter relateret til den specifikke certificering, kan du tilknytte dem ved at vælge knappen **Dokument**.

Certificeringer, der er angivet af dine kreditorer på denne side, tildeles kilden "Kreditor". Du kan angive certifikatoplysninger på kreditorens vegne under kreditorbankkonti. Oplysningerne vises her, og kilden vises som **Debitor**.

Kreditorer kan redigere eller slette deres certificeringer efter behov.

## <a name="vendor-collaboration-generated-certification-records"></a>Certificeringsposter oprettet under kreditorsamarbejde

Når en leverandør har tilføjet certificeringsoplysninger, kan oplysningerne ses på siden **Certificeringer oprettet under kreditorsamarbejde**. Du kan åbne siden ved at gå til **Kreditor > Forespørgsler > Kreditorrapporter > Certificeringer oprettet under kreditorsamarbejde**. Som standard vises alle nye eller ændrede certificeringsposter. Kreditormedarbejderen kan få vist ændringerne og kontrollere oplysningerne via sin bekræftelsesproces for at validere dem. Når oplysningerne er bekræftet, kan den certificeringspost, der vises på siden, vælges og markeres som gennemset. Hvis du markerer posten som gennemset, fjernes den fra standardlisten.

Alle certificeringsændringer er synlige på siden **Certificeringer oprettet under kreditorsamarbejde**. Hvis en ændring ikke vises på siden, kan du få den vist ved at justere filtrene for kreditorkontoen, ikrafttrædelsesdatointervallet eller vælge, om der skal medtages oplysninger om de certificeringsændringer, der er blevet gennemset.

