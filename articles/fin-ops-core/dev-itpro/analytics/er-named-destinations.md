---
title: Konfigurere postspecifikke ER-destinationer for udskriftsstyring
description: Denne artikel forklarer, hvordan du kan konfigurere postspecifikke destinationer i udskriftsstyringen til et elektronisk rapporteringsformat (ER), som er konfigureret til at generere udgående dokumenter.
author: NickSelin
ms.date: 08/03/2021
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
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2972dc6a0b373cbc63b811c01ef7a5538810edbb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872707"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Konfigurere postspecifikke ER-destinationer for udskriftsstyring

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan en bruger med rollen Systemadministrator eller Debitorassistent kan udføre følgende opgaver:

- Konfigurer navngivne destinationer for [Elektronisk rapportering (ER)](general-electronic-reporting.md) til en ER-løsning, der genererer fritekstfakturaer.
- Tildel en ER-destination til en enkelt post til [udskriftsstyring](document-reporting-services.md).

Procedurerne kan udføres i USMF-virksomheden. Der kræves ingen kodning.

## <a name="introduction"></a>Start her

Du kan konfigurere [destinationer](electronic-reporting-destinations.md) for hver mappe i filoutputkomponenten til en ER-[format](general-electronic-reporting.md)[konfiguration](general-electronic-reporting.md#Configuration), der bruges til at generere et udgående dokument. Når du kører et ER-format af denne type og har de relevante adgangsrettigheder, kan du også ændre de konfigurerede destinationsindstillinger under kørslen.

I Microsoft Dynamics 365 Finance **version 10.0.17 og senere** kan du [konfigurere](er-apis-app10-0-17.md) en handlingskode til et ER-format for at angive den handling, som brugere udfører ved at køre dette ER-format. I modulet **Debitor** kan du f.eks. vælge et ER-format i indstillingerne for udskriftsstyring, der genererer et bestemt forretningsdokument, f.eks. en fritekstfaktura. Du kan derefter vælge **Vis** for at få vist fakturaen eller **Udskriv** for at sende den til en printer. Hvis en handling sendes for det aktuelle ER-format under kørslen, kan du [konfigurere forskellige ER-destinationer for forskellige brugerhandlinger](er-action-dependent-destinations.md).

I Finance **version 10.0.21 og senere** kan du [konfigurere](er-apis-app10-0-21.md) en navngivet destination for et ER-format og tildele den til den post for udskriftsstyring, som behandles, når det pågældende ER-format køres. I modulet **Debitor** i indstillingerne for udskriftsstyring kan du f.eks. konfigurere posten **Oprindelig** til at udføre følgende handlinger:

- Køre et ER-format.
- Sende den genererede faktura pr. email til en kunde.
- Konfigurere posten **Kopi** til at køre samme format.
- Udskrive en kopi af fakturaen til en netværksprinter.

I dette tilfælde skal du konfigurere forskellige ER-destinationer for det ER-format, der kører, og du skal vælge destinationer til forskellige poster for udskriftsstyring.

## <a name="prerequisites"></a>Forudsætninger

Før du går i gang, skal funktionen **Tillad opsætning af ER-destinationer pr. funktion til udskriftsstyring** være aktiveret i arbejdsområdet til [Funktionsstyring](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace). Kildekoden skal også ændres, hvis du vil tillade konfiguration af navngivne ER-destinationer i den aktuelle Finance-forekomst og aktivering af den [nye](er-apis-app10-0-21.md) ER-API.

ER-konfigurationen for **Fritekstfakturaer (Excel)** skal desuden [importeres](er-download-configurations-global-repo.md) til din Finance-forekomst.

## <a name="configure-a-new-er-destination"></a>Konfigurere en ny ER-destination

1. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Vælg en faktura for debitorkontoen **US-001**.
3. På siden **Fritekstfaktura** under fanen **Faktura** i gruppen **Udskriftsstyring** skal du vælge **Udskriftsstyring**.
4. På siden **Opsætning af udskriftsstyring** skal du udvide **Modul – debitor** \> **Dokumenter** \> **Fritekstfaktura**, vælge posten **Oprindeligt** og derefter følge disse trin:

    1.  Tag højde for de aktuelle indstillinger for den valgte post:
        -   SSRS-standardrapporten **FreeTextInvoice.Report** er valgt i feltet **Rapportformat**.
        -   Navnet **\<Default\>** vises i feltet **Destination** og oplyser om, at der ikke er valgt en brugerdefineret destination til den tildelte SSRS-rapport. 
    2.  Vælg ER-formatkonfigurationen **Fritekstfaktura (Excel)** i feltet **Rapportformat**.
        -   Navnet i feltet **Destination** ændres til **Destinationsnavn**.
        -   Navnet **\<No named destination\>** vises i feltet **Destinationsnavn** og oplyser om, at der ikke er valgt en navngivet destination til det tildelte ER-format.
    3.  Vælg pileknappen til højre for feltet **Destinationsnavn**.    
    4. Angiv **Hoveddestination** i feltet **Navn** på siden **Navngiven destination for elektronisk rapportering**.
    5. Vælg **Gem**.
    6. På oversigtspanelet **Fildestination** skal du [konfigurere](er-destination-type-email.md) destinationen **Email** for komponenten **Rapport**.
    7. Luk siden **Navngivet destination for elektronisk rapportering**.
    8. Vælg den navngivne destination for **Hoveddestination** i feltet **Destinationsnavn** på siden **Opsætning af udskriftsstyring**.

    ![Konfigurere en navngivet ER-destination for det valgte ER-format og tildele den til en konfigureret post for udskriftsstyring på siden Opsætning af udskriftsstyring](./media/er-named-destinations-01.gif)

    Du har nu konfigureret den navngivne ER-destinations **Hoveddestination** til formatet **Fritekstfaktura (Excel)** og tildelt den til udskiftsstyringsposten **Original** under **Modul - Debitor** \> **Dokumenter** \> **Fritekstfaktura**.

5. Udvid **Modul - Debitor** \> **Konto - US-001** \> **Fritekstfaktura**, vælg posten **Oprindelig**, og følg derefter disse trin:

    1. Vælg og hold (eller højreklik på) posten, og vælg derefter **Tilsidesæt**.
    2. Vælg pileknappen til højre for feltet **Destinationsnavn**.
    3. Vælg **Ny** i handlingsruden på siden **Navngivet destination for elektronisk rapportering**.
    4. I feltet **Navn** skal du skrive **US-001-destination**.
    5. På oversigtspanelet **Fildestination** skal du [konfigurere](er-destination-type-print.md) destinationen **Printer** for komponenten **Rapport**.
    6. Luk siden **Navngivet destination for elektronisk rapportering**.
    7. Vælg den navngivne destination for **US-001-destination** i feltet **Destinationsnavn** på siden **Opsætning af udskriftsstyring**.

    ![Konfigurere en navngivet ER-destination for det valgte ER-format og tildele den til den konfigurerede post for udskriftsstyring på siden Opsætning af udskriftsstyring](./media/er-named-destinations-02.gif)

    Du har nu konfigureret den navngivne ER-destination **US-001-destination** til formatet **Fritekstfaktura (Excel)** og tildelt den til udskiftsstyringsposten **Original** under **Modul - Debitor** \> **Konto - US-001** \> **Fritekstfaktura**.

Når en fritekstfaktura er behandlet, køres ER-formatet **Fritekstfaktura (Excel)** og en af følgende hændelser finder sted:

- Hvis fritekstfakturaen er til en anden debitor end US-001, sendes det oprettede dokument via email.
- Hvis fritekstfakturaen er til debitoren US-001, udskrives det oprettede dokument.

> [!NOTE]
> Når der ikke er defineret en navngivet destination for en post til udskriftsstyring, som er behandlet under kørslen, bruges ER-standarddestinationerne, hvis de er tilgængelige for det ER-format, der kører.

> [!IMPORTANT]
> Hvis du vælger et ER-format, som mindst en navngivet destination er konfigureret til, på siden **Elektronisk rapporteringsdestination** (**Organisationsadministration** \> **Elektronisk rapportering** \> **Elektronisk rapporteringsdestination**), får du besked om, at der findes navngivne destinationer.
>
> ![Besked om forekomsten af konfigurerede navngivne destinationer for det valgte ER-format på destinationssiden Elektronisk rapportering](./media/er-named-destinations-03.png)
>
> Hvis du sletter standarddestinationen, slettes alle navngivne destinationer også. Hvis de navngivne destinationer er valgt for poster til udskriftsstyring, annulleres valget af disse navngivne destinationer.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Kopiere en eksisterende ER-destination som en ny navngivet destination

Når den navngivne ER-standarddestination er tilgængelig for et ER-format, kan den bruges som skabelon for nye ER-destinationer. Hvis du vil oprette en ny ER-destination, der er baseret på standarddestinationen, skal du vælge **Kopiér fra standard** på siden **Navngivet destination for elektronisk rapportering**. Den nye destination kaldes **Standard**. Du kan gentage dette trin lige så mange gange, du har brug for.

Du kan vælge en hvilken som helst eksisterende navngivet destination som skabelon for en ny navngivet destination. Hvis du vil oprette en ny navngivet ER-destination, der er baseret på en valgt navngivet destination, skal du vælge **Kopiér** på siden **Navngivet destination for elektronisk rapportering**. Den nye destination har samme navn som den valgte navngivne destination, men med tilføjelsen af suffikset "Kopi". Du kan gentage dette trin lige så mange gange, du har brug for.

## <a name="security-considerations"></a>Sikkerhedsovervejelser

Du kan kun oprette navngivne ER-destinationer på siden **Opsætning af udskriftsstyring**, hvis du har [tilladelse](../sysadmin/role-based-security.md#permissions) til at udføre denne opgave. Du kan tildeles rettigheder, hvis [opgaven](../sysadmin/role-based-security.md#duties) **Konfigurer destination for elektronisk rapporteringsformat** er tildelt en af dine [sikkerhedsroller](../sysadmin/role-based-security.md#security-roles). Du kan finde flere oplysninger under [Sikkerhedsovervejelser](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)

[Ændringer af API-struktur til elektronisk rapportering for applikationsopdatering 10.0.17](er-apis-app10-0-17.md)

[Ændringer af API-struktur til elektronisk rapportering for applikationsopdatering 10.0.21](er-apis-app10-0-21.md)

[Ændringskode, så brugere kan konfigurere og bruge navngivne ER-destinationer](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
