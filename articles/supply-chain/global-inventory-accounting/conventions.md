---
title: Konventioner
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere principper, der fastlægger, hvordan omkostninger skal registreres i Global Inventory Accounting.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 97c27006ce95d0cd4551fec209f40328779b435b
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678585"
---
# <a name="conventions"></a>Konventioner

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!--KFM: Until 4/30/2022 -->

Et princip er en objektbeholder for et sæt politikker, der påvirker systemets funktionsmåde. Ud fra dine forretningsbehov skal du definere principper ved at bruge en kombination af de forskellige politikker, der fastlægger, hvordan omkostninger skal gøres registreres i Global Inventory Accounting. Du kan knytte de enkelte principper til ét eller flere finanskonti for at sikre ensartethed i regnskabspolitikker, der anvendes på tværs af finansmoduler.

Du kan konfigurere dine principper ved at gå til **Globalt lagerregnskab \> Konfiguration \> Principper**. For hvert princip skal du angive følgende felter:

- **Navn** – Angiv navnet på princippet.
- **Beskrivelse** – Indtast en beskrivelse af princippet.
- **Politik for omkostningsobjekt** – Vælg en politik for omkostningsobjekt. Disse politikker bestemmer det granularitetsniveau, som systemet bruger til at beregne og vedligeholde lagerværdien. Der findes følgende foruddefinerede indstillinger:

    - Produkt
    - Produkt – Lokation
    - Produkt – Lokation – Lagersted

    Hvis du for eksempel vælger *Produkt – Lokation*, beregner og vedligeholder systemet lageromkostningerne for hvert produkt på lokationsniveau for hver lagerbevægelse (indgående eller udgående vare). Lagerbevægelser på lavere niveauer, for eksempel lagerstedsniveau, påvirker derfor ikke lagerværdien. (Et eksempel på en overførsel på lagerstedsniveau er en vareoverførsel mellem to lagersteder i én lokation). På samme måde kan du ikke få vist lageromkostningerne på et lavere niveau, for eksempel lagerstedsniveau.

- **Politik for basis for inputmåling** – Vælg en politik for basis for inputmåling. Disse politikker bestemmer, hvilke omkostninger der skal gå ind på lagerkontoen, og de omkostninger, der skal opkræves. Følgende indstillinger er relevante for samhandelsfirmaer:

    - **Normal historisk** – Alle omkostningskomponenter går ind på lagerkontoen.
    - **Standard** – Standardomkostninger går ind på lagerkonti, og forskellen mellem de anvendte omkostninger og de faktiske omkostninger debiteres på konti for afvigelse. Hvis du vil oprette en *standard* politik for basis for inputmålinger, skal du først oprette en prisliste, hvor politikken kan slå varens standardomkostninger op.
    - **Prislister** – Global Inventory Accounting understøtter hentning af varepriser fra flere juridiske enheder. Du kan definere en prisliste, som politikken for basis for inputmåling vil bruge. På denne måde ved systemet, hvor varens pris skal slås op. Benyt følgende fremgangsmåde for at konfigurere prislister:

        1. Indtast et navn i feltet **Navn**.
        1. Indtast en beskrivelse i feltet **Beskrivelse**.
        1. Vælg en omkostningstype (*Standardkostpris* eller *Planlagte omkostninger*) i feltet **Efterkalkulationstype**.
        1. Vælg en pristype i feltet **Pristype** (*Omkostning*, *Indkøb* eller *Salgspris*).
        1. Tilføj en efterkalkulationsversion.
        1. Vælg **Pris** i handlingsruden for at validere varepriserne på prislisten.

- **Politik for forudsætning for omkostningsforløb** – Vælg en politik for forudsætning for omkostningsforløb. Disse politikker bestemmer, hvordan omkostninger fjernes fra lageret og rapporteres som vareforbrug. Der findes følgende foruddefinerede indstillinger:

    - Gennemsnit
    - Specifik – Batch

    > [!NOTE]
    > Global Inventory Accounting er et tidsubegrænset lagersystem. Systemet sporer derfor lagerværdien efter hver enkelt transaktion.

- **Politik for omkostningselement** – Du kan definere politikker for omkostningselementer og knytte dem til dette felt. Et *omkostningselement* er omkostningen for en ressource, der forbruges ved en hændelse. Du kan bruge omkostningselementer til at spore og kategorisere omkostninger. Hvis du vil oprette politikker for omkostningselementer, skal du angive oplysninger følgende steder:

    - Feltet **Navn**
    - Feltet **Beskrivelse**
    - Listen **Omkostningselement**
    - Gitteret **Regler**

    Hvis du ikke vil opdele lagerværdien yderligere, skal du stadig oprette en liste over omkostningselementer, der har et enkelt omkostningselement. Du skal derefter oprette en politik for omkostningselementer for at knytte alle relevante måletyper (omkostningskomponenter) til det pågældende omkostningselement.
