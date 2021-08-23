---
title: Konfigurere handlingsafhængige ER-destinationer
description: Dette emne forklarer, hvordan du kan konfigurere handlingsafhængige destinationer for et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter.
author: NickSelin
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 93adc5b91667fdcd5969439994170fe7d28258fc9f5762d1262d8e72862c4f5f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762242"
---
# <a name="configure-action-dependent-er-destinations"></a>Konfigurere handlingsafhængige ER-destinationer

[!include [banner](../includes/banner.md)]

Du kan konfigurere [destinationer](electronic-reporting-destinations.md) for hver outputkomponent (mappe eller fil) til en [elektronisk rapportering (ER)](general-electronic-reporting.md)-[format](general-electronic-reporting.md#FormatComponentOutbound)-[konfiguration](general-electronic-reporting.md#Configuration), der bruges til at generere et udgående dokument. Brugere, som kører et ER-format af denne type, og som har de relevante adgangsrettigheder, kan også ændre de konfigurerede destinationsindstillinger under kørslen.

I Microsoft Dynamics 365 Finance **version 10.0.17 og senere** kan der køres et ER-format ved at [klargøre](er-apis-app10-0-17.md) en handlingskode, som brugeren udfører ved at køre dette ER-format. I modulet **Debitor** kan du f.eks. vælge et ER-format i indstillingerne for udskriftsstyring, der genererer et bestemt forretningsdokument, f.eks. en fritekstfaktura. Du kan derefter vælge **Vis** for at få vist fakturaen eller **Udskriv** for at sende den til en printer. Hvis der sendes en brugerhandling for det kørende ER-format under kørsel, kan du konfigurere forskellige ER-destinationer til forskellige brugerhandlinger. Dette emne forklarer, hvordan du konfigurerer ER-destinationer for denne type ER-format.

## <a name="make-action-dependent-er-destinations-available"></a>Gøre handlingsafhængige ER-destinationer tilgængelige

Hvis du vil konfigurere handlingsafhængige ER-destinationer i den aktuelle Finans-forekomst og aktivere den [nye](er-apis-app10-0-17.md) ER API, skal du åbne arbejdsområdet til [funktionsstyring](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) og aktivere funktionen **Konfigurer bestemte ER-destinationer til forskellige PM-handlinger**. Hvis du vil bruge konfigurerede ER-destinationer til [bestemte](#reports-list-wave1) rapporter under kørslen, skal du aktivere funktionen **Ruteoutput af PM-rapporter baseret på ER-destinationer, der er brugerhandlingsspecifikke (bølge 1)**.

## <a name="configure-action-dependent-er-destinations"></a>Konfigurere handlingsafhængige ER-destinationer

Når du aktiverer funktionen **Konfigurer bestemte ER-destinationer, der skal bruges til forskellige PM-handlinger**, kan du konfigurere handlingsafhængige ER-destinationer i oversigtspanelet **Fildestination** på destinationssiden **Elektronisk rapportering**. For hver komponent kan du tilføje en post og aktivere bestemte ER-destinationer. For hver post skal du angive den type dokument, som de konfigurerede ER-destinationer skal anvendes på. Vælg en af følgende værdier i feltet **Dokumenttype**.

- Vælg **Elektronisk** for at anvende de konfigurerede destinationer, hvis der ikke er angivet en brugerhandlingskode under kørslen.
- Vælg **Udskriftsstyring** for at anvende de konfigurerede destinationer, hvis der er angivet en brugerhandlingskode under kørslen.
- Vælg **Enhver** for altid at anvende de konfigurerede destinationer, uanset om der er angivet en brugerhandlingskode under kørslen.

Hvis du vælger dokumenttypen **Udskriftsstyring**, skal du angive de brugerhandlinger, som de konfigurerede ER-destinationer skal anvendes til. Vælg en af følgende værdier i feltet **Udskriftsstyringshandling**:

- Vælg **Vis** for at anvende de konfigurerede destinationer, hvis brugerhandlingen **Vis** er angivet under kørslen.
- Vælg **Udskriv** for at anvende de konfigurerede destinationer, hvis brugerhandlingen **Udskriv** er angivet under kørslen.
- Vælg **Send** for at anvende de konfigurerede destinationer, hvis brugerhandlingen **Send** er angivet under kørslen.

> [!NOTE]
> Der kan vælges flere handlinger for en enkelt destinationspost.

Hvis du vælger dokumenttypen **Enhver**, vælges **Automatisk søgning** automatisk i handlingsfeltet **Udskriftsstyringshandling** som en brugerhandling, og følgende funktionsmåde forekommer:

- His der ikke er angivet en brugerhandlingskode under kørslen, anvendes alle konfigurerede ER-destinationer.
- Hvis der angives en brugerhandlingskode under kørslen, anvendes en ER-destination, der er foruddefineret for en bestemt aktion, **uanset om den er aktiveret**:

    - Når handlingen **Vis** er angivet under kørslen, anvendes **Skærm** som ER-destination.
    - Når handlingen **Send** er angivet under kørslen, anvendes **Mail** som ER-destination.
    - Når handlingen **Udskriv** er angivet under kørslen, anvendes **Printer** som ER-destination.

Du kan f.eks. bruge ER-formatet **Fritekstfaktura (Excel)** til at udskrive en [fritekstfaktura](../../../finance/accounts-receivable/create-free-text-invoice-new.md), når du bogfører den. Hvis du vil distribuere et genereret dokument, skal du konfigurere ER-destinationer for dette ER-format. Du skal f.eks. konfigurere disse ER-destinationer for at udføre følgende på et genereret dokument:

- Arkivér dokumentet, hvis ER-formatet køres, men der ikke er angivet en handlingskode (f.eks. når dokumentet sendes elektronisk).
- Se dokumentet i en webbrowser, når en bruger udfører handlingen **Vis**.
- Arkivér og udskriv dokumentet, når en bruger udfører handlingen **Udskriv**.
- Arkivér dokumentet, og send det med mail som en vedhæftet fil i en udgående mailmeddelelse, når en bruger udfører handlingen **Send**.

I følgende illustration vises, hvordan du kan opnå dette ved at konfigurere ER-destinationer som et sæt individuelle destinationsposter, når hver post er konfigureret til en individuel brugerhandling:

![Destinationsside for elektronisk rapportering, der har handlingsafhængige destinationsindstillinger for et ER-format, når alle destinationspost er konfigureret til en enkelt brugerhandling.](./media/er-destination-action-dependent-01.png)

I følgende illustration vises, hvordan du også kan opnå dette ved at konfigurere ER-destinationer som et sæt individuelle destinationsposter, når hver post er konfigureret til en individuel destination:

![Destinationsside for elektronisk rapportering, der har handlingsafhængige destinationsindstillinger for et ER-format, når alle destinationspost er konfigureret til en enkelt destination.](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Hvis der er angivet en handlingskode for det kørende ER-format, men der ikke er konfigureret nogen destinationer for denne handlingskode, anvendes [standarden](electronic-reporting-destinations.md#default-behavior) for funktionsmåden til destinationen.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Ændre handlingsafhængige ER-destinationer ved kørslen

Når der køres et ER-format, og der er leveret brugerhandlinger for de brugere, som har de nødvendige [rettigheder](electronic-reporting-destinations.md#security-considerations) til at ændre konfigurerede destinationsindstillinger under kørslen, vises en dialogboks, der giver mulighed for at ændre de konfigurerede destinationsindstillinger. Denne dialogboks er valgfri, og dens udseende afhænger af, hvordan det kald, ER-strukturen foretager for at køre et ER-format, er blevet implementeret. Hvis denne dialogboks vises, aktiveres ER-destinationer i den i henhold til den brugerhandling, der er angivet.

I følgende illustration vises et eksempel på dialogboksen **Destinationer for elektronisk rapporteringsformat**, der vises, når en fritekstfaktura [bogføres](../../../finance/accounts-receivable/create-free-text-invoice-new.md), og ER-formatet **Fritekstfaktura (Excel)** køres for at generere dette dokument, hvis handlingen **Printer** er klargjort, og der er konfigureret ER-destinationer for dette format, som vist tidligere i dette emne.

![Dialogboks, der giver mulighed for at ændre de oprindeligt konfigurerede ER-destinationer for det kørende ER-format.](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Hvis du har konfigureret ER-destinationer for flere komponenter i det kørende ER-format, tilbydes der en indstilling separat for hver konfigureret komponent i ER-formatet.

## <a name="verify-the-provided-user-action"></a>Kontrollere den leverede brugerhandling

Du kan kontrollere, hvilken brugerhandling der eventuelt er angivet for det kørende ER-format, når du udfører en bestemt brugerhandling. Denne kontrol er vigtig, når du skal konfigurere handlingsafhængige ER-destinationer, men du ikke er sikker på, hvilken brugerhandlingskode der eventuelt er angivet. Når du f.eks. begynder at bogføre en fritekstfaktura og angiver indstillingen **Udskriv faktura** til **Ja** i dialogboksen **Bogfør fritekstfaktura**, kan du angive indstillingen **Brug destination for udskriftsstyring** til **Ja** eller **Nej**.

Følg disse trin for at kontrollere den brugerhandlingskode, der er leveret.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. I dialogboksen **Brugerparametre** skal du [angive](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) indstillingen **Kør i fejlfindingstilstand** til **Ja**.
4. Udfør en brugerhandling ved at køre et ER-format. Vær opmærksom på, at ER-brugerparametre er brugerspecifikke og firmaspecifikke.
5. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Fejlfindingslogs for konfigurationer**.
6. På siden **Fejlfindingslogs for konfigurationer** skal du filtrere ER-kørselslogfiler for at finde logfilen til din ER-formatkørsel.
7. Gennemse de logposter, der skal indeholde den post, der viser den angivne brugerhandlingskode, hvis der er angivet en handling for kørsel af ER-format.

    ![Siden Kørselslog for elektronisk rapportering har oplysninger om den brugerhandlingskode, der er angivet for den filtrerede kørsel af et ER-format.](./media/er-destination-action-dependent-03.png)

## <a name=""></a><a name="reports-list-wave1">Liste over forretningsdokumenter (bølge 1)</a>

Følgende liste over forretningsdokumenter styres af funktionen **Ruteoutput af PM-rapporter baseret på ER-destinationer, der er brugerhandlingsspecifikke (bølge 1)**:

- Debitorfaktura (fritekstfaktura)
- Debitorfaktura (salgsfaktura)
- Indkøbsordre
- Købsforespørgsel om indkøbsordre
- Salgsordrebekræftelse
- Rykkernota
- Kundekontoudtog
- Rentenota
- Kreditorbetalingsvejledning
- Tilbudsanmodning

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)

[Ændringer af API-struktur til elektronisk rapportering for Application update 10.0.17](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]