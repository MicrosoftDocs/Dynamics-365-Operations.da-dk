---
title: Variantgrupper til løsningen Invoice Capture
description: Denne artikel indeholder generelle oplysninger om variantgrupper i løsningen Invoice Capture.
author: sunfzam
ms.date: 09/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691166"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Variantgrupper til løsningen Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Brugere kan administrere listen over fakturafelter og indstillingen for manuel evaluering for juridiske enheder ved hjælp af variantgrupper. Brugere kan konfigurere fakturakonfigurationer for forskellige juridiske enheder i grupper. Alle de juridiske enheder i samme variantgruppe bruger samme fakturafelter og indstillinger for manuelt gennemsyn.

## <a name="manage-configuration-groups"></a>Administrer variantgrupper

Hvis du vil administrere variantgrupper ved hjælp af appen, skal du gå til **Opsætning** og derefter vælge **Systemopsætning \> Definer komponent for variantgrupper**.

På siden **Definer variantgrupper** viser hovedfanen listen over variantgrupper, der er defineret. Den viser også en standardvariantgruppe. De følgende handligner er tilgængelige for hver variantgruppe:

- **Kopiér en variantgruppe** – Du kan oprette en ny variantgruppe ved at duplikere en eksisterende gruppe. Den nye gruppe har samme værdier som den oprindelige gruppe for alle felterne med undtagelse af **Gruppenavn** og **Gruppebeskrivelse**. Når variantgruppen er duplikeret, skal du vælge **OK**.
- **Slet variantgrupper** – Hvis du vil slette en variantgruppe, skal du markere den og derefter vælge **Slet**.

    > [!NOTE]
    > Standardvariantgruppen kan ikke slettes.

- **Rediger en variantgruppes id** – Hvis du vil redigere id'et for en variantgruppe, skal du vælge feltet **Gruppe-id** og opdatere værdien. Gruppe-id'et må ikke indeholde mellemrum eller specialtegn, og det må ikke overstige 20 tegn.

    > [!NOTE]
    > Værdien i feltet **Gruppe-id** kan kun opdateres én gang.

- **Rediger en variantgruppes beskrivelse** – Hvis du vil redigere beskrivelsen af en variantgruppe, skal du vælge feltet **Beskrivelse** og opdatere værdien.
- **Ændre indstillingen for manuelt gennemsyn** – Brugerne kan beslutte, om en faktura skal gennemses manuelt. Hvis du vil ændre indstillingen for manuelt gennemsyn, skal du vælge indstillingen **Behøver manuelt gennemsyn**. Der findes følgende indstillinger:

    - **Altid manuelt gennemsyn** – Vælg denne indstilling, hvis fakturaer i variantgruppen altid kræver manuelt gennemsyn.
    - **For fejl og advarsler** – Vælg denne indstilling, hvis fakturaer, der indeholder fejlmeddelelser eller advarselsmeddelelser, kræver manuelt gennemsyn.
    - **For fejl** – Vælg denne indstilling, hvis fakturaer, der indeholder fejlmeddelelser, kræver manuelt gennemsyn.

- **Rediger indstillingen for konfidensscore** – Konfidensscoren er metadata, som løsningen Invoice Capture indeholder, så nøjagtigheden af registrerede fakturadata rapporteres. Jo højere scoren er, jo mere præcis kan de genkendte data være. Konfigurationen giver brugerne mulighed for at definere, hvornår manuelt gennemsyn er påkrævet, baseret på konfidensscoren. Brugere kan ændre konfidensscoregrænsen for fakturaer. Hvis du vil opdatere indstillingen af konfidensscore, skal du vælge feltet **Konfidensscore** og opdatere værdien.

    Der er to påmindelsestyper for konfidensscore:

    - **Advarsel** – Fakturafelter, der har konfidensscorer over advarselsgrænsen, betragtes som korrekte. Advarselsgrænsen skal være større end fejlgrænsen og mindre end 100.
    - **Fejl** – Fakturafelter, der har konfidensscorer under fejlgrænsen, betragtes som ugyldige. Fejlmeddelelser vises for brugeren. Fejlgrænsen skal være større end 0 (nul) og mindre end advarselsgrænsen. Der vises advarselsmeddelelser for fakturafelter, der har en konfidensscore mellem advarselsgrænsen og fejltærsklen.

- **Administrer fakturafelter** – Brugerne kan administrere listen over fakturafelter, der vises i fremviseren side om side. Vælg tandhjulsymbolet under fanen **Fakturafeltstyring**, vælg de fakturafelter, du vil tilføje, og vælg derefter **Gem**. De valgte felter tilføjes på listen. Hvis du vil fjerne et fakturafelt fra listen, skal du vælge **Fjern** i feltet.

### <a name="manage-file-filters-optional"></a>Administrere filfiltre (valgfrit)

Administrer filfiltre, så brugere kan definere flere filtre for indgående fakturafiler. Filer, der ikke opfylder filterkriterierne, modtages og vises på listen **Modtagne filer**, men de viser fejl i filvalidering. Denne funktionalitet er forskellig fra funktionaliteten for filtre, der er defineret i kanalen. Ved disse filtre modtages filer, der ikke opfylder kriterierne, slet ikke. Brugere kan gennemse indgående filer og bestemme, om hver enkelt fil er en ikke-gyldig faktura, og de kan gøre filen forældet eller manuelt medtage den for at blive registreret og medtaget i hentede fakturaer.

Når løsningen Invoice Capture er installeret, defineres der et standardfilfilter. Dette filfilter er globalt. Hvis du vil bruge andre filterindstillinger, kan du opdatere standardfilteret. Hvis et felt er obligatorisk, skal du vælge **Obligatorisk**. 

### <a name="accepted-file-size"></a>Accepteret filstørrelse

Du kan vælge den accepterede filstørrelse.

> [!NOTE]
> Filer, der er større end 20.480 kilobyte (KB), understøttes ikke.

### <a name="supported-file-types"></a>Understøttede filtyper

Følgende filtyper understøttes i øjeblikket:

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF
