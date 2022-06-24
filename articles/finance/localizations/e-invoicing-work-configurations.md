---
title: Arbejde med konfigurationer
description: Denne artikel indeholder en oversigt over hovedscenariet for arbejde med ER-konfigurationer (elektronisk rapportering) fra arbejdsområdet til globaliseringsfunktioner.
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
ms.openlocfilehash: 359f00336811efd5f21463a325627df0e01a5f3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875936"
---
# <a name="work-with-configurations"></a>Arbejde med konfigurationer

[!include [banner](../includes/banner.md)]

Konfigurationer af elektronisk rapportering (ER) er et af hovedsættene for komponenterne i funktioner til elektronisk fakturering. En ER-konfiguration indeholder opsætningen af filstrukturen og et sæt transformationsregler for transformering af data på to måder:

- **Eksportér ER-formatkonfiguration** – Denne konfiguration transformerer data fra den samlede interne struktur (ER-model) til det elektroniske filformat.
- **Importér ER-formatkonfiguration** – Denne konfiguration transformerer data fra det elektroniske filformat til den samlede interne struktur (ER-model).

Udover at generere udgående elektroniske filer i det foruddefinerede format bruges ER-konfigurationer i vidt omfang til at parre indgående meddelelser fra eksterne webtjenester som svar. Denne funktionalitet hjælper med at opbygge konfigurerbar logik for at hente resultaterne af kommunikation med eksterne kanaler, konvertere disse resultater (koder, meddelelser og logfiler) til den brugerlæsbare struktur og derefter overføre disse oplysninger til klientprogrammet.

Hvis du vil begynde at bruge ER-konfigurationer i din funktion til elektronisk fakturering, skal du knytte dem til funktionen og gøre dem tilgængelige under fanen **Konfigurationer** for den aktuelle funktionsversion. Du kan arbejde med en tilknyttet ER-konfiguration ved at vælge **Tilføj**, **Slet**, **Rediger** eller **Vis**.

Før du kan føje et link til en ER-konfiguration, skal konfigurationen findes i RCS-lageret (Regulatory Configuration Service). Hvis du vil gennemse de ER-konfigurationer, der er tilgængelige i RCS-lageret, skal du følge disse trin.

1. Log på din RCS-konto.
2. Gå til arbejdsområdet **Elektronisk rapporteringreporting**, og vælg feltet **Reporting configurations** i sektionen **Konfigurationer**.

Du kan finde oplysninger om, hvordan du opretter en ny ER-konfiguration eller importerer en eksisterende ER-konfiguration fra det globale lager, under [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Hvis du vil justere en tilknyttet ER-konfiguration, skal du vælge **Rediger** under fanen **Konfigurationer** for den aktuelle funktion til elektronisk fakturering. Systemet opretter automatisk en version af ER-konfigurationen. Hvis den aktuelle version ikke er oprettet af den aktive konfigurationsudbyder, opretter systemet en afledt version, der bruger din konfigurationsudbyder. Hvis den aktuelle version er oprettet af den aktive konfigurationsudbyder, opretter systemet en ny version. I begge tilfælde kan du redigere den version, der oprettes, og derefter udføre alle nødvendige opdateringer automatisk.
