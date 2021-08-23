---
title: Opret og kør behandling for at kalde et simpelt ER-eksportformat for at oprette en Excel-rapport
description: Dette emne indeholder et eksempel på, hvordan du kan konfigurere og bruge elektroniske meddelelser.
author: liza-golub
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a5fd466c98e0855f7a33929eeee42b9147d26ba19780b4ae7c8eb895ac27ea5e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737671"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Opret og kør behandling for at kalde et simpelt ER-eksportformat for at oprette en Excel-rapport

[!include [banner](../includes/banner.md)]

Når du har oprettet ER-formatet, knyttet det til datakilder og fuldført det, kan du køre det ved hjælp af arbejdsområdet **Elektronisk rapportering**. Når rapporten er genereret, får du mulighed for at gemme den lokalt.

Du kan styre følgende aspekter af rapporteringsprocessen ved at konfigurere behandlingen af elektroniske meddelelser:

- Log oplysninger om, hvem der oprettede rapporten.
- Logoplysninger om, hvornår rapporten blev genereret.
- Gem de rapporter, der blev oprettet for tidligere perioder.

Følgende eksempel viser, hvordan du kan oprette elektroniske meddelelser for at generere en rapport, der er baseret på et ER-eksportformat til Microsoft Excel. Hvis du ønsker at følge dette eksempel, skal ER-eksportformatet til Excel allerede være oprettet, knyttet til datakilderne og fuldført. Derudover skal der allerede være konfigureret en nummerserie for elektroniske meddelelser.

Når du konfigurerer behandling, er det nyttigt, hvis du først definerer de behandlingshandlinger og statusser, der skal oprettes. I følgende illustration vises, hvordan behandlingen ser ud i dette eksempel.

![Behandlingsskema](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Opret meddelelsesstatusser

1. Gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Meddelelsesstatusser**.
2. Oprette følgende meddelelsesstatusser:

    - Nyt
    - Forberedt
    - Genereret

    ![Meddelelsesstatusser](media/message-statuses.png)

3. På linjen for den **Ny** status, skal du markere afkrydsningsfeltet **Tillad sletning** for at tillade, at brugere sletter meddelelser med denne status.

## <a name="create-additional-fields"></a>Oprette flere felter

1. Gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Ekstra felter**.
2. Tilføj et ekstra felt og de tilhørende værdier.
3. Vælg **Ja** i indstillingen **Brugerredigering**, så brugerne kan redigere feltet.

![Ekstra felter](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Oprette handlinger til meddelelsesbehandling

I dette eksempel skal du oprette følgende meddelelsesbehandlingshandlinger:

- **Opret meddelelse**
- **Opdater til Forberedt**
- **Generér rapport**
- **Opdater til første status** (valgfrit)

Følg disse trin for at oprette handlinger.

1. Gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Meddelelsesbehandlingshandlinger**.
2. Opret en handling, der hedder **Opret meddelelse**. I oversigtspanelet **Generelt** skal du i feltet **Handlingstype** vælge **Opret meddelelse**.
3. Opret en handling, der hedder **Opdater til Forberedt**, og indstil følgende felter:

    - I oversigtspanelet **Generelt** skal du i feltet **Handlingstype** vælge **Behandling af bruger på meddelelsesniveau**.
    - I oversigtspanelet **Første statusser** skal du i feltet **Meddelelsesstatus** vælge **Ny**.
    - I oversigtspanelet **Resultatstatusser** skal du i feltet **Meddelelsesstatus** vælge **Forberedt**. I feltet **Svartype** skal du angive **Udført korrekt**.

4. Opret en handling, der hedder **Generér rapport**, og indstil følgende felter:

    - I oversigtspanelet **Generelt** skal du i feltet **Handlingstype** vælge **Eksport af elektronisk rapportering**. I feltet **Formattilknytning** skal du vælge ER-formatet til eksport. De tilgængelige indstillinger er **Excel**, **XML**, **JSON**, **Tekst** og **Andet**.
    - I oversigtspanelet **Første statusser** skal du i feltet **Meddelelsesstatus** vælge **Forberedt**.
    - I oversigtspanelet **Resultatstatusser** skal du i feltet **Meddelelsesstatus** vælge **Genereret**. I feltet **Svartype** skal du angive **Udført korrekt**.

    ![Handlingen Generér rapport](media/generate-report-action.png)

5. Valgfrit: Du kan lade brugerne generere en rapport flere gange ved at oprette en **Opdater til første status**-handling og angive følgende felter:

    - I oversigtspanelet **Generelt** skal du i feltet **Handlingstype** vælge **Behandling af bruger på meddelelsesniveau**.
    - I oversigtspanelet **Første statusser** skal du i feltet **Meddelelsesstatus** vælge **Genereret**.
    - I oversigtspanelet **Resultatstatusser** skal du tilføje en separat linje for hver af de to meddelelsesstatusser (**Forberedt** og **Ny**). Angiv feltet **Svartype** til **Udført korrekt** for begge linjer.

## <a name="electronic-message-processing"></a>Behandling af elektronisk meddelelse

I dette eksempel skal alle handlingerne være konfigureret, så de kører separat. Det antages, at brugeren påbegynder hver handling.

1. Gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Elektroniske meddelelsesbehandling**.
2. Føj en post til din behandling, og tilføj alle tidligere definerede handlinger og et ekstra felt.
3. Valgfrit: i oversigtspanelet **Sikkerhedsroller** skal du definere sikkerhedsrollerne for din behandling for derved at begrænse adgangen til specifikke rapporter.
4. Gå til **Moms** \> **Forespørgsler og rapporter** \> **Elektroniske meddelelser** \> **Elektroniske meddelelser**.
5. Vælg **Ny** for at oprette en meddelelse. På dette tidspunkt kan du tilføje datoer og en beskrivelse. Du kan også opdatere værdien af det ekstra felt efter behov.

    ![Oprette en elektronisk meddelelse](media/create-electronic-message.png)

    Gitteret i oversigtspanelet **Handlingslog** udfyldes automatisk med en log over alle handlinger, der udføres på meddelelsen.

    Du kan nu slette eller opdatere meddelelsesstatus. 

6. Vælg **Opdater status** for at opdatere meddelelsens status. I feltet **Ny status** skal du vælge **Forberedt** og dernæst vælge **OK**.

    ![Opdatere meddelelsens status](media/update-status.png)

    Meddelelsens status opdateres til **Forberedt**.

7. Generere rapporten ved at vælge **Generer rapport**.

    Rapporten oprettes, og meddelelsesstatus og handlingsloggen opdateres.

8. For at gennemse den genererede rapport skal du trykke på knappen **Vedhæft fil** (symbolet med papirklip) i øverste højre hjørne af siden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
