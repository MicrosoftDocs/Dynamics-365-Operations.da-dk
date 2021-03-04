---
title: Forberede programspecifikke metadata til RCS og ER
description: Dette emne forklarer, hvordan du forbereder programspecifikke metadata til Regulatory Configuration Service (RCS) og elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f15b78d3ed5b4df47540f9f89cc69c0b535a7241
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680188"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a>Forberede programspecifikke metadata til RCS og ER

[!include[banner](../includes/banner.md)]

I dette emne gennemgås eksempler på følgende opgaver:

- [Klargøre programmetadata, der kan bruges i RCS](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Få adgang til programmetadata ved hjælp af ER-konfiguration](#access-application-metadata-by-using-an-er-configuration)
- [Få adgang til programmetadata ved hjælp af tilsluttede programmer](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>Klargøre programmetadata, der kan bruges i RCS

Følgende procedure viser, hvordan en bruger, der har rollen **Systemadministrator** eller rollen **Udvikler af elektronisk rapportering**, kan oprette en elektronisk rapporteringskonfiguration (ER), der indeholder metadata til programmet, og som bruges til at designe konfigurationer af ER-modeltilknytning i Regulatory Configuration Service (RCS). Eksempelkonfigurationen af ER-modeltilknytning, der oprettes i dette eksempel, bruges til at få adgang til udenlandske handelstransaktioner.

I dette eksempel skal du bruge RCS til at designe en ER-løsning for programmet, der skal bruges til at generere elektroniske dokumenter, der indeholder oplysninger fra forretningsdomænet til udenrigshandel. Hvis du vil angive tilknytningen mellem ER-datamodellen og kilderne til de påkrævede data, skal du have adgang til programmetadata i RCS. Som en del af processen med at designe ER-løsningen skal du oprette en ny ER-metadatakonfiguration, der indeholder alle de metadata, der i øjeblikket er påkrævet for at generere ER-rapporter for det valgte forretningsdomæne.

> [!NOTE]
> I dette eksempel skal du oprette en konfiguration til eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i enhver virksomhed.

1. Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.
2. Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret konfigurationsudbydere, og markér dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Vælg **Konfiguration af metadata**.
4. Vælg **Opret konfiguration**.
5. Angiv et navn i feltet **Navn** i rulledialogboksen. I dette eksempel skal du angive **Udenrigshandelmetadata**.
6. Vælg **Opret konfiguration**.
7. Vælg **Designer**.
8. Vælg **Tilføj**.

    > [!NOTE]
    > Du kan enten vælge alle metadata for hele programmet eller for udvalgte modeller eller moduler. Bemærk i begge tilfælde, at følgende metadata vil blive tilføjet automatisk: tabeller over poster, fasttekster og udvidede datatyper (EDT'er). Når der kræves flere typer metadata, skal de tilføjes manuelt.

    Du skal tilføje nogle metadata, der er relateret til udenlandske handelstransaktioner, og vælge metadataelementer manuelt.

9. Vælg **Tilføj datakilde \> Tabelposter**.
10. Filtrer efter værdien **Intrastat** i feltet **Navn**.
11. Vælg **Intrastat** -tabelposten.
12. Vælg **OK**.

    Du skal tilføje metadataoplysninger om Intrastat-tabellen med poster.

13. I træet skal du vælge **Tabelposter Intrastat \> \>Relationer \> IntrastatCommodity (tabelposter EcoResCategory)**.
14. Vælg **Tilføj metadata**.

    > [!NOTE]
    > Metadata om nødvendige relationer for den valgte tabel med poster skal tilføjes manuelt.

15. Vælg **Tilføj datakilde**.
16. Vælg **Fasttekst**.
17. Filtrer efter værdien **IntrastatDirection** i feltet **Navn**.
18. Vælg **IntrastatDirection**-fasttekstposten.
19. Vælg **OK**.
20. Vælg **Gem**.
21. Luk siden.
22. Fuldfør kladdeversionen af metadatakonfigurationen:

    1. Vælg **Skift status \> Fuldfør**.
    2. Vælg **OK**.
    3. Vælg den fuldførte version 1.

23. Eksportér den fuldførte version af metadatakonfigurationen fra programmet som en XML-fil:

    1. Vælg **Udveksling \> Eksportér som XML-fil**.
    2. Vælg **OK**.

Den ER-metadatakonfiguration, som du har oprettet, gemmes som filen **Udenrigshandelmetadata.xml**. Du kan nu importere den i RCS, så den kan bruges som kilden til metadata i forretningsdomænet for udenrigshandel. Baseret på disse oplysninger kan du angive tilknytningen mellem programmetadata og ER-datamodellen.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Få adgang til programmetadata ved hjælp af ER-konfiguration

Følgende procedure viser, hvordan en RCS-bruger, der har rollen **Systemadministrator** eller **Udvikler til elektronisk rapportering** kan designe en ny ER-modeltilknytning ved hjælp af metadata fra programmet. Der opnås adgang til programmetadata ved hjælp af en ER-metadatakonfiguration, der indeholder et eksempel sæt af metadata for adgang til udenrigshandelstransaktioner.

Før du kan fuldføre denne procedure, skal du fuldføre følgende procedurer:

- [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [Klargøre programmetadata, der kan bruges i RCS](#prepare-application-metadata-that-can-be-used-in-rcs)

1. Gå til **Alle arbejdsområder \> Elektronisk rapportering**.
2. Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret konfigurationsudbydere, og markér dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Importer den ER-metadatakonfiguration, der indeholder metadata for programmet, og som er konfigureret til at generere elektroniske dokumenter for udenrigshandelens forretningsdomæne. Du har oprettet denne ER-metadatakonfiguration og eksporteret den som en XML-fil i proceduren [Klargøre programmetadata, der kan bruges i RCS](#prepare-application-metadata-that-can-be-used-in-rcs) tidligere i dette emne.

    1. Vælg **Konfiguration af metadata**.
    2. Vælg **Udveksling**.
    3. Vælg **Indlæs fra XML-fil**.
    4. Naviger for at vælge filen **Udenrigshandelmetadata.xml**.
    5. Vælg **OK**.
    6. Luk siden.

4. Opret en datamodelkonfiguration:

    1. Vælg **Rapporteringskonfigurationer**.
    2. Vælg **Opret konfiguration**.
    3. Angiv **Udenrigshandelmodel** i feltet **Navn** i rulledialogboksen.
    4. Vælg **Opret konfiguration**.
    5. Vælg **Designer**.
    6. Vælg **Ny** for at åbne dialogboksen Slip.

        1. Skriv **Rod** i feltet **Navn**.
        2. Vælg **Tilføj**.
    
    7. Vælg **Ny** for at åbne dialogboksen Slip.

        1. Skriv **Transaktion** i feltet **Navn**.
        2. Vælg **Liste over poster** i feltet **Varetype**.
        3. Vælg **Tilføj**.
 
    8. Vælg **Ny** for at åbne dialogboksen Slip.

        1. Skriv **Varekode** i feltet **Navn**.
        2. Vælg **Streng** i feltet **Varetype**.
        3. Vælg **Tilføj**.

    9. Vælg **Ny** for at åbne dialogboksen Slip.

        1. Skriv **Faktureret beløb** i feltet Navn.
        2. Vælg **Kommatal** i feltet **Varetype**.
        3. Vælg **Tilføj**.

    10. Vælg **Ny** for at åbne dialogboksen Slip.

        1. Skriv **Dato** i feltet **Navn**.
        2. Vælg **Dato** i feltet **Varetype**.
        3. Vælg **Tilføj**.
 
    11. Vælg **Tilføj \> Rodreference**.
    12. Vælg **OK**.
    13. Vælg **Gem**.
    14. Luk siden.
    15. Vælg **Skift status \> Fuldfør**.
    16. Vælg **OK**.

5. Opret en konfiguration af modeltilknytning:

    1. Vælg **Opret konfiguration**.
    2. Angiv **Modeltilknytning baseret på datamodellen Udenrigshandelmodel** i feltet **Ny** i rulledialogboksen.
    3. Skriv **Tilknytning af udenrigshandel** i feltet **Navn**.
    4. Vælg **Opret konfiguration**.
    5. Vælg **Rediger** i oversigtspanelet **Forudsætninger**.
    6. Vælg **Ny**.
    7. Vælg **Konfiguration** i feltet **Type af forudsætningskomponent**.
    8. Vælg konfigurationen **Udenrigshandelmetadata**.
    9. Vælg **Gem**. Bemærk, at referencen er føjet til version 1 af konfigurationen **Udenrigshandelmetadata**. Der tilbydes programmetadata fra denne konfiguration, mens modeltilknytningen bliver udformet.
    10. Luk siden.
    11. Vælg **Designer**.
    12. Vælg **Designer**.
    13. Vælg **Dynamics 365 for Operations \> Tabelposter** i træet.
    14. Vælg **Tilføj rod**.
    15. I feltet **Navn** skal du skrive **Intrastat**.
    16. Vælg **Intrastat** -tabelposter.
    17. Vælg **OK**.

        > [!NOTE]
        > Der tilbydes kun to tabeller, da der kun blev føjet to tabeller til det sæt metadata, der bruges i øjeblikket.

    18. Vælg **Bind**.
    19. Vælg **Intrastat \> AmountMST** i træet.
    20. Vælg **Transaktion = Intrastat \> Faktureret beløb** i træet.
    21. Vælg **Bind**.
    22. Vælg **Intrastat \> TransDate** i træet.
    23. Vælg **Transaktion = Intrastat \> Dato** i træet.
    24. Vælg **Bind**.
    25. Vælg **Intrastat \> \>Relationer \> IntrastatCommodity \> Kode** i træet.
    26. Vælg **Transaktion = Intrastat \> Varekode** i træet.
    27. Vælg **Bind**.
    28. Vælg **Valider**.

        > [!NOTE]
        > Når validering er fuldført, har du bundet elementer i datamodellen til elementer i de datakilder, der er beskrevet, ved hjælp af oplysninger om programmetadata fra den ER-metadatakonfiguration, der refereres til.

    29. Vælg **Gem**.

Du kan efter behov udvide det eksisterende sæt metadata i programmet. Du kan derefter eksportere den nye fuldførte version af ER-metadatakonfigurationen, importere den til RCS og opdatere forudsætningerne for den konfigurerede konfiguration af modeltilknytning, der refererer til en ny version af den importerede metadatakonfiguration.

> [!NOTE]
> Denne indlæsningsmetode af oplysninger om programmetadata er den eneste, der er tilgængelig for lokalt installerede programmer (når der bruges lokale virksomhedsdata \[LBD\] eller en lokal installationsmodel for programmet).

## <a name="access-application-metadata-by-using-connected-applications"></a>Få adgang til programmetadata ved hjælp af tilsluttede programmer

Følgende procedure viser, hvordan en RCS-bruger, der har rollen **Systemadministrator** eller **Udvikler til elektronisk rapportering** kan designe en ny ER-modeltilknytning ved hjælp af metadata fra programmet. Du kan få adgang til programmetadata online ved hjælp af det RCS-tilsluttede program. Et eksempel på ER-modeltilknytning konfigureres til at give adgang til udenrigshandelstransaktioner.

For at fuldføre denne procedure skal du først fuldføre proceduren [Opret konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md) i RCS. Hvis du ikke har fuldført [Få adgang til programmetadata ved hjælp af ER-konfiguration](#access-application-metadata-by-using-an-er-configuration) tidligere i dette emne, skal du gå til siden [Opgaveguider til elektronisk rapportering for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) for at downloade følgende ER-konfigurationsfiler på forhånd og gemme dem lokalt: **Udenrigshandelmetadata.xml**, **Udenrigshandelmodel.xml** og **Tilknytning af udenrigshandel.xml**.


### <a name="get-required-er-configurations"></a>Få de nødvendige ER-konfigurationer

Hvis du allerede har udført trinnene i proceduren [Få adgang til programmetadata ved hjælp af ER-konfiguration](#access-application-metadata-by-using-an-er-configuration) tidligere i dette emne, har du allerede alle de nødvendige ER-konfigurationer (konfigurationer af metadata til udenrigshandel, model og tilknytning) i den aktuelle RCS-forekomst. I dette tilfælde kan du springe denne procedure over.

1. Gå til **Alle arbejdsområder \> Elektronisk rapportering**.
2. Vælg **Rapporteringskonfigurationer**.
3. Indlæs konfigurationsfilerne **Udenrigshandelmetadata.xml**, **Udenrigshandelmodel.xml** og **Tilknytning af udenrigshandel.xml** ved at gentage følgende trinserie for hver af dem:

    1. Vælg **Udveksling**.
    2. Vælg **Indlæs fra XML-fil**.
    3. Vælg **Gennemse**, og vælg en fil.
    4. Vælg **OK**.

### <a name="register-the-connection-with-the-application"></a>Registrer forbindelsen til programmet

1. Gå til **Alle arbejdsområder \> Elektronisk rapportering**.
2. Vælg **Tilsluttede programmer**.
3. Sørg for, at det konfigurerede program er baseret på Microsoft Azure, og at det er generelt tilgængeligt for RCS-brugere. Det kræves også, at den aktuelle RCS-bruger har adgang til det konfigurerede program, der registreres, som bruger af dette program med en rolle, som giver adgangsrettigheder til programmets metadata.
4. Vælg **Ny**.
5. I feltet **Navn** skal du angive **MyConnectedApp** som navnet på det tilknyttede program.
6. Angiv programmets URL-adresse i feltet **Applikation**.
7. Angiv programmets udbyder i feltet **Lejer**.
8. Vælg **Gem**. 
9. Når du kontrollerer forbindelsen til det konfigurerede program, skal du på siden **Opret forbindelse til eksternt program** vælge linket **Klik her for at oprette forbindelse til det valgte eksterne program**. 
10. Vælg **Kontrollér forbindelsen** for at validere adgangen til det konfigurerede program.
11. Vælg **Luk**.

Når du har udført denne procedure, og forbindelsen er valideret korrekt, opdateres versions- og lejeroplysningerne for det konfigurerede program i det aktuelle gitter.

### <a name="review-the-existing-model-mapping-configuration"></a>Gennemgå den eksisterende modeltilknytningskonfiguration

1. Gå til **Alle arbejdsområder \> Elektronisk rapportering**.
2. Vælg **Rapporteringskonfigurationer**.
3. Vælg **Udenrigshandelmodel \> Tilknytning af udenrigshandel** i træet.
4. Vælg oversigtspanelet **Forudsætninger**.

    > [!NOTE]
    > I øjeblikket refererer denne tilknytning til metadatakonfigurationen. Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet.

4. Vælg **Designer**.
5. Vælg **Designer**.
6. Vælg **Dynamics 365 for Operations \> Tabelposter** i træet.
7. Vælg **Tilføj rod**.
8. Indtast eller vælg en værdi i feltet **Tabel**.

    > [!NOTE]
    > I øjeblikket refererer denne tilknytning til metadatakonfigurationen. Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet.

9. Vælg **Annuller**.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>Tildele det tilsluttede program en modeltilknytning

1. Vælg **Rediger**.
2. Vælg programmet **MyConnectedApp** i feltet **Tilsluttet program**.

    > [!NOTE]
    > Denne tilknytning refererer til metadataene for det valgte tilsluttede program. Hvis en tilknytning refererer til metadatakonfigurationen og det tilsluttede program samtidig, bruges metadataene for det tilsluttede program.

3. Vælg **Designer**.
4. Vælg **Designer**.
5. Vælg **Dynamics 365 for Operations \> Tabelposter** i træet.
6. Vælg **Tilføj rod**.
7. Indtast eller vælg en værdi i feltet **Tabel**.

    > [!NOTE]
    > Nu tilbydes der mere end to programtabeller, da denne tilknytning bruger alle de metadata, der er tildelt det tilsluttede program.

8. Vælg **Annuller**.
9. Vælg **Valider**.

Du har nu bundet elementer i datamodellen til elementer i de datakilder, der er beskrevet, ved hjælp af oplysninger om metadata for det tilsluttede program, der er tildelt denne tilknytning.

Når du skal evaluere denne modeltilknytning ved hjælp af metadata for en anden version af programmet, skal du registrere et andet tilsluttet program, tildele det denne modeltilknytning og validere det mod de nye metadata.

## <a name="additional-resources"></a>Yderligere ressourcer

Du kan også afspille opgaveguiden **Klargøre programmetadata, der kan bruges i RCS** i programmet samt opgaveguiderne **Få adgang til programmetadata ved hjælp af ER-konfiguration** og **Få adgang til programmetadata ved hjælp af tilsluttede programmer** i RCS. Disse opgaveguider kan downloades fra siden [Opgaveguider til elektronisk rapportering for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]