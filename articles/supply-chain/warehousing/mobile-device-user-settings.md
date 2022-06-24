---
title: Indstillinger for mobilenhedsbruger
description: Denne artikel forklarer, hvordan brugerindstillinger for mobilenheder administreres for lagerarbejdere.
author: Mirzaab
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 15f9ce1768e1ed9dc6f7e84d245082b46a7f122c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882338"
---
# <a name="mobile-device-user-settings"></a>Indstillinger for mobilenhedsbruger

[!include [banner](../../includes/banner.md)]

Den nye mobilapp Lokationsstyring indeholder et sæt appspecifikke indstillinger, der er med til at skræddersy brugeroplevelsen. Da appen kan bruges på enheder med forskellige skærmstørrelser og konfigurationer (f.eks. tablet, telefon eller håndholdt), kan det være nyttigt at administrere disse indstillinger centralt fra Microsoft Dynamics 365 Supply Chain Management.

Med funktionen til *brugerindstillinger for mobilenhed* kan du definere globale brugerindstillinger, der skal bruges på alle enheder. Du kan også definere mere detaljerede brugerindstillinger for individuelle enhedsmærker, enhedsmodeller og/eller arbejdere. Når en arbejder logger på mobilappen Lokationsstyring, henter og anvender appen den mest specifikke indstillingsprofil, der er gemt i Supply Chain Management for det tilsvarende brand, enheden og/eller bruger-id'et.

Denne funktion kan hjælpe arbejdere med at komme hurtigere i gang, når de begynder at bruge en ny enhed. Her er nogle eksempler:

- Administratorer kan oprette et sæt standardindstillinger, der fungerer bedst for enheder fra en bestemt producent og/eller for bestemte enhedsmodeller. Arbejderne kan derfor komme i gang med en ny enhed uden at skulle ændre indstillingerne.
- Hvis dit firma har en pulje af identiske enheder, der deles mellem arbejdere, vil arbejderne se deres foretrukne opsætning, hver gang de logger på, selvom de aldrig har brugt den specifikke fysiske enhed, de har valgt på en given dag.
- I Supply Chain Management kan administratorer se og redigere alle gemte indstillinger, også for enkelte arbejdere. Denne egenskab kan hjælpe dem med at foretage fejlfinding af eller finjustere nye funktioner.

> [!IMPORTANT]
> Funktionen til *brugerindstillinger for mobilenheder* gælder kun for den nye mobilapp Lokationsstyring. Den fungerer ikke med den gamle lagerstedsapp.

## <a name="turn-the-mobile-device-user-settings-feature-on-or-off"></a>Aktivere eller deaktivere funktionen til brugerindstillinger for mobilenheder

Hvis du vil bruge den funktionalitet, der er beskrevet i denne artikel, skal funktionen *Brugerindstillinger, ikoner og trintitler til den nye lagerstedsapp* være aktiveret i systemet. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Brugerindstillinger, ikoner og trintitler til den nye lagerstedsapp* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="create-and-manage-user-settings"></a>Oprette og administrere brugerindstillinger

Brug siden **Brugerindstillinger for mobilenhed** til at oprette, se og administrere indstillingsprofiler på alle detaljeniveauer. Første gang en arbejder redigerer sine brugerindstillinger på en ny enhed, tilføjes der automatisk en ny profil på denne side, hvis den ikke allerede findes. Profilen opdateres derefter, hver gang arbejderen foretager en ændring.

Du kan også definere en indstillingsprofil for alle enhedsmærker, enhedsmodeller og/eller arbejdere. Du kan derefter øge granulariteten ved at anvende mere specifikke indstillinger for de enkelte mærker, modeller og/eller arbejdere.

Følg disse trin for at oprette og administrere brugerindstillinger for dine mobilenheder.

1. Gå til **Lokationsstyring \> Konfiguration \> Mobilenhed \> Brugerindstillinger for mobilenhed**.
1. Vælg en eksisterende brugerindstillingsprofil i listeruden for at åbne posten. Du kan også vælge **Ny** i handlingsruden for at oprette en ny profil.

    Hver profil i listeruden har navnet på det mærke, den model og/eller det bruger-id, profilen gælder for. Mere generelle profiler har værdien *Alle* for nogle af eller alle disse egenskaber.

1. Angiv følgende felter i overskriftssektionen for den nye eller valgte post til indstillingsprofil:

    - **Enhedsmærkenavn** – Vælg det enhedsmærkenavn, som profilen skal gælde for. Hvis profilen skal gælde for alle mærker, skal feltet ikke udfyldes. Listen over værdier omfatter alle de mærker, der er defineret i systemet. Du kan finde flere oplysninger om, hvordan listen over mærker defineres, i næste afsnit.
    - **Enhedsmodel-id** – Vælg den enhedsmodel, som profilen skal gælde for. Hvis profilen skal gælde for alle modeller af det valgte mærke, skal feltet ikke udfyldes. Listen over værdier indeholder alle de modeller, der er defineret for det mærke, der er valgt i feltet **Enhedsmærkenavn**. Du kan finde oplysninger om, hvordan listen over modeller for hvert mærke defineres, i næste afsnit.
    - **Bruger-id** – Vælg bruger-id'et for den lagerarbejder, som indstillingsprofilen skal gælde for. Hvis profilen skal gælde for alle arbejdere, skal feltet ikke udfyldes.

1. I oversigtspanelet **Generelt** skal du indstille følgende felter:

    - **Knapposition** – Vælg, hvordan knapperne skal placeres på enheden. Elementer i appen flyttes, så de passer bedre til arbejderens præference eller håndtering. De tilgængelige indstillinger er *Nederst til højre (standard)*, *Nederst til venstre*, *Øverste til højre* og *Øverste til venstre*.
    - **Visningsretning** – Vælg den visningsretning, der skal anvendes som standard i appen.
    - **Scan med kamera** – Angiv denne indstilling til *Ja* for at bruge enheden til at scanne inputfelter, hvor den foretrukne inputtilstand er angivet til *Scanning*. Hvis din enhed har en indbygget scanner, skal du angive denne indstilling til *Nej*, hvis du vil bruge scanneren i stedet.
    - **Vis produktbillede** – Vælg, om produktbilleder skal vises, hvis de er tilgængelige for det frigivne produkt. Du kan finde flere oplysninger om, hvordan du tilføjer produktbilleder, under [Føje et billede til et produkt](../pim/tasks/add-image-product.md).
    - **Vis farvetema** – Vælg et farvetema for enheden.
    - **Lydniveau** – Vælg enhedens lydniveau. Vælg en værdi mellem 0 (nul) og 10. En værdi på *0* repræsenterer ingen lyd, og en værdi på *10* angiver den maksimale lydstyrke. Standardværdien er *4*.
    - **Vibrationsniveau** – Vælg enhedens vibrationsniveau. Vælg en værdi mellem 0 (nul) og 5. En værdi på *0* repræsenterer ingen vibration, og en værdi på *5* angiver den maksimale vibration. Standardværdien er *1*.
    - **Tekstskalaprocent** – Angiv tekststørrelsen som en procentdel af standardstørrelsen. Angiv en værdi mellem 70 og 400. En værdi på *70* repræsenterer den mindste tekstskala, og en værdi på *400* repræsenterer den største tekstskala. Standardværdien er *100*.
    - **Knapskalaprocent** – Angiv kapstørrelsen som en procentdel af standardstørrelsen. Angiv en værdi mellem 50 og 200. En værdi på *50* repræsenterer den mindste knapskala, og en værdi på *200* repræsenterer den største knapskala. Standardværdien er *100*.

## <a name="create-and-manage-mobile-device-brands"></a>Oprette og administrere mobilenhedsmærker

Du kan bruge siden **Mærker til mobilenhed** til at se, oprette og administrere de enhedsmærker og -modeller, der kan bruges sammen med dine indstillingsprofiler. Mobilappen henter og sender automatisk det lokale mærkenavn og model-id, første gang en arbejder redigerer sine indstillinger på en given enhed. Derfor genereres de fleste af disse poster normalt automatisk. Du kan dog også administrere alle posterne på denne side. Du kan f.eks. give mere nyttige beskrivelser af hver enkelt mærke eller model, så du kan skelne mellem lignende eller kryptiske model-id'er.

Følg disse trin for at oprette og administrere dine mobilenhedsmærker og -modeller.

1. Gå til **Lokationsstyring \> Konfiguration \> Mobilenhed \> Mærker til mobilenhed**.
1. Vælg et mobilenhedsmærke i listeruden for at åbne dets post. Du kan også vælge **Ny** i handlingsruden for at oprette et nyt mærke.
1. Angiv følgende felter i overskriftssektionen for den nye eller valgte post til enhedsmærke:

    - **Enhedsmærkenavn** – Enhedsmærkets navn, f.eks. *Microsoft Corporation*.
    - **Beskrivelse** – Du kan angive en beskrivelse, der gør det lettere at skelne mellem mærkenavne.

1. I oversigtspanelet **Modeller til mobilenhed** vises alle modellerne for det valgte enhedsmærke. Brug knapperne på værktøjslinjen til at tilføje rækker i gitteret eller fjerne rækker. For hver række kan du angive følgende felter:

    - **Enhedsmodel-id** – Enhedsmodel-id, f.eks. *Surface Book 2*.
    - **Beskrivelse** – Du kan angive en beskrivelse, der gør det lettere at skelne mellem model-id'er.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Installere og tilslutte mobilapp til lagerstedsadministration](install-configure-warehouse-management-app.md)
- [Tildele trinikoner og titler til mobilappen Warehouse Management](step-icons-titles.md)