---
title: Opgørelse over personalegoder
description: Rapporten Frynsegoder indeholder en forklaring på de frynsegoder, som en medarbejder aktuelt er tilmeldt.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 36e7082a890ebec3031021a0871cddad91597447
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336881"
---
# <a name="benefit-statement"></a>Opgørelse over personalegoder

Rapporten **Frynsegodeoversigt** indeholder en oversigt over de frynsegoder, som en medarbejder aktuelt er tilmeldt. En medarbejder kan få adgang til rapporten direkte eller af administratoren af frynsegodet. **Frynsegodsopgørelsen** indeholder en liste over medarbejderens tilmeldte frynsegoder, disponeringsindstillinger, omkostninger og eventuelle tilmeldte afhængige eller modtagere. Opgørelsen kan udskrives for en enkelt arbejder eller flere arbejdere.

> [!NOTE]
I arbejdsområdet **Funktionsstyring** skal du aktivere **Frynsegodestyring**. Hvis du vil gøre dette, skal **Frynsegodestyring** være aktiveret i Funktionsstyring. 


## <a name="importing-the-benefit-statement"></a>Importere Frynsegodeopgørelsen 

Du skal importere **Frynsegodeopgørelsen** ved hjælp af rapportkonfiguration, før **Frynsegodeopgørelsen** er tilgængelig. Dette gøres ved at gennemføre følgende trin:

1.  Gå til arbejdsområdet **Systemadministration**.

2.  Vælg feltet **Elektronisk rapportering**.

3.  Gå til **Konfigurationsudbydere**, og vælg **Lagre**.

  ![Valg af lagre.](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  Vælg **Personaleressourcer** på listen, og vælg derefter **Åbn**.

    ![Konfigurationslagre.](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  Vælg **modellen til frynsegodeopgørelsen** i venstre rude, og udvid den, så formatet for **Frynsegodeopgørelsen** vises.

6.  Vælg **Format for frynsegodeopgørelse** i venstre rude.

7.  I højre side af skærmen vises der et oversigtspanel med **Versioner**. Vælg **Importér**.

    ![Oversigtspanelet Versioner.](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Generere Frynsegodeopgørelsen som en PDF-fil

Som standard udskrives **Frynsegodeopgørelsen** som et Microsoft Word-dokument. Hvis du vil udskrive i et PDF-format, skal du konfigurere PDF-indstillingen i **Elektronisk rapportdestination**. 

1. Det kan du gøre ved at gå til **arbejdsområdet til Systemadministration** > **Elektronisk rapportering** > **Relaterede links** > **Elektronisk rapporteringsdestination**.

1.  Vælg **Ny**.

2.  Vælg formatet **Frynsegodeopgørelse** i feltet **Reference**.

3.  Vælg **Ny** i oversigtspanelet **Fildestination**.

4.  I feltet **Navn** skal du skrive **Frynsegodeoversigt (PDF)**.

5.  Angiv **Frynsegodeoversigt** i feltet **Filkomponentnavn**.

6.  Markér afkrydsningsfeltet **Konverter til PDF** .

7.  Vælg **Indstillinger** fra menupunktet. 

    ![Fildestination.](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  Vælg oversigtspanelet **Filer**, og vælg derefter **Aktiveret**.

9.  Vælg **OK**.
   
> [!NOTE]
> Funktionen frynsegodestyring er i Forhåndsversionstilstand. Der er et kendt problem, når du bruger indstillingen for e-maildestinationen i rapporten **Destination for elektronisk rapportering**. Du modtager muligvis en fejlmeddelelse, og e-mailen kan ikke sendes.

**Frynsegodeopgørelsen** kan genereres fra følgende sider:

-   **Arbejdsområde til frynsegodestyring** > **Links** > **Rapporter** > **Frynsegodeoversigt**

-   **Medarbejdere (ældre form)** > **Fanen Personlige oplysninger** > **Frynsegodeoversigt**

-   **Strømlinet medarbejderindtastning** > **Frynsegoderapporter** > **Frynsegodeoversigt**

-   **Medarbejder, selvbetjening** > **Frynsegoder** > **Vis frynsegodeoversigt**

> [!NOTE]
>  Adgangen til **Frynsegodeoversigt** i **Medarbejder-selvbetjening** styres af **erklæringen Vis frynsegodeoversigt**. Det er under rettigheden **Medarbejder, selvbetjening af frynsegoder**. Medarbejdere tildeles som standard denne rettighed.

## <a name="report-contents"></a>Rapportindhold

**Frynsegodeoversigten** udskriver medarbejderens bekræftede valg af plan, herunder frafaldne planer. Følgende billede viser et eksempel på denne rapport. 

![Frynsegodeoversigtrapport.](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

Rapporten viser **Plan**, **disponeringsindstilling**, **medarbejderomkostninger** og **arbejdsgiveromkostninger**. Rapporten vil også omfatte alle afhængige, der er dækket. Hvis der er knyttet bene der til planen, vises benene og deres fordelingsprioritet og procentdel.

Rapporten **Frynsegodeoversigt** kan udskrives for flere medarbejdere samtidig ved hjælp af oversigtspanelet **Poster, der skal medtages** på siden **Medarbejderopgørelse**.
