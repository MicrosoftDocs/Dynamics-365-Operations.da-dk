---
title: Designe ER-udtryk til kald af programklassemetoder
description: Denne artikel indeholder oplysninger om, hvordan du genbruge den eksisterende programlogik i konfigurationer til elektronisk rapportering ved at kalde de krævede metoder for programklasser.
author: NickSelin
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0fb0a9725d882fdc330d7adbb49bd3dcadf7805f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883619"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Designe ER-udtryk til kald af programklassemetoder

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder oplysninger om, hvordan du kan genbruge den eksisterende programlogik i konfigurationer af [elektronisk rapportering (ER)](../general-electronic-reporting.md) ved at kalde de påkrævede metoder for programklasser i ER-udtryk. Værdier af argumenter for kald af klasser kan defineres dynamisk under kørsel. Værdier kan f.eks. baseres på oplysningerne i fortolkningsdokumentet for at sikre, at de er korrekte.

Til eksemplet i denne artikel skal du designe en proces til fortolkning af indgående bankkontoudtog for en opdatering af programdata. Du modtager indgående bankkontoudtog som tekstfiler (.txt) med IBAN-koder (International Bank Account Number). Som en del af importprocessen for kontoudtog skal du validere rigtigheden af disse IBAN-koder ved brug af den logik, der allerede findes.

## <a name="prerequisites"></a>Forudsætninger

Procedurerne i denne artikel er beregnet til brugere, der har fået tildelt rollen som **Systemadministrator** eller **Elektronisk rapporteringsudvikler**.

Procedurerne kan udføres ved hjælp af et hvilket som helst datasæt.

Du skal hente og gemme følgende fil lokalt: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

I denne artikel opretter du de krævede ER-konfigurationer for Litware, Inc., eksempelvirksomheden. Du skal derfor fuldføre følgende trin, før du kan fuldføre procedurerne i denne artikel.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du bekræfte, at konfigurationsudbyderen for eksempelfirmaet **Litware, Inc.** er tilgængeligt og markeret som aktivt. Hvis du ikke kan se denne konfigurationsudbyder, skal du først fuldføre trinnene i [Opret konfigurationsudbydere, og markér den som aktive](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-a-new-er-model-configuration"></a>Importere en ny ER-modelkonfiguration

1. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Microsoft** som konfigurationsudbyder i sektionen **Konfigurationsudbydere**.
2. Vælg **Lagre**.
3. Vælg **Vis filtre** på siden **Lokaliseringslagre**.
4. Hvis du vil vælge global lagerpost, skal du tilføje et filterfelt for **Navn**.
5. I feltet **Navn** skal du angive **Global**. Vælg derefter filteroperatoren **indeholder**.
6. Vælg **Anvend**.
7. Vælg **[Åbn](../er-download-configurations-global-repo.md#open-configurations-repository)** for at gennemgå listen over ER-konfigurationer i det valgte lager.
8. På siden **Konfigurationslager** skal du i konfigurationstræet vælge **Betalingsmodel**.
9. I oversigtspanelet **Versioner** skal du vælge knappen **Importér**, hvis den er tilgængelig, og derefter vælge **Ja**.

    Hvis knappen **Importér** ikke er tilgængelig, har du allerede importeret den valgte version af ER-konfigurationen **Betalingsmodel**.

10. Luk siden **Konfigurationslager**, og luk derefter siden **Lokaliseringslagre**.

## <a name="add-a-new-er-format-configuration"></a>Tilføje en ny ER-formatkonfiguration

Tilføje et nyt ER-format til at fortolke indgående bankkontoudtog i TXT-formatet.

1. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude vælge **Betalingsmodel**.
3. Vælg **Opret konfiguration**. 
4. Følg disse trin i rulledialogboksen:

    1. Skriv **Format baseret på datamodel PaymentModel** i feltet **Ny**.
    2. Angiv **Importformat for bankkontoudtog (eksempel)** i feltet **Navn**.
    3. Vælg **Ja** i feltet **Understøtter dataimport**.
    4. Vælg **Opret konfiguration** for at fuldføre oprettelsen af konfigurationen.

## <a name="design-the-er-format-configuration--format"></a>Designe ER-formatkonfigurationen – format

Design et ER-format, der repræsenterer den forventede struktur i den eksterne fil i TXT-format.

1. Til den formatkonfiguration af **Importformat for bankkontoudtog (eksempel)**, du har tilføjet, skal du vælge **Designer**.
2. Vælg **Tilføj rod** i formatstrukturtræet i venstre rude på siden **Formatdesigner**.
3. Følg disse trin i den viste dialogboks:

    1. Vælg **Tekst\\Sekvens** i træet for at tilføje en **Sekvens** som formatkomponent.
    2. I feltet **Navn** skal du angive **Rod**.
    3. Vælg **Ny linje – Windows (CR LF)** i feltet **Specialtegn**. Baseret på denne indstilling skal hver linje i fortolkningsfilen betragtes som en separat post.
    4. Vælg **OK**.

4. Vælg **Tilføj**.
5. Følg disse trin i den viste dialogboks:

    1. Vælg **Tekst\\Sekvens** i træet.
    2. Angiv **Rækker** i feltet **Navn**.
    3. Vælg **Én mange** i feltet **Multiplicitet**. Baseret på denne indstilling forventes det, at der vises mindst én linje i fortolkningsfilen.
    4. Vælg **OK**.

6. Vælg **Rod\\Rækker** i træet, og vælg derefter **Tilføj sekvens**.
7. Følg disse trin i den viste dialogboks:

    1. I feltet **Navn** skal du angive **Felter**.
    2. Vælg **Nøjagtig én** i feltet **Multiplicitet**.
    3. Vælg **OK**.

8. Vælg **Rod\\Rækker\\Felter** i træet, og vælg derefter **Tilføj**.
9. Følg disse trin i den viste dialogboks:

    1. Vælg **Tekst\\Streng** i træet.
    2. Angiv **IBAN** i feltet **Navn**.
    3.. Vælg **OK**.

10. Vælg **Gem**.

Konfigurationen er nu oprettet, så hver linje i fortolkningsfilen kun indeholder IBAN-koden.

![Formatkonfigurationen Importformat for bankkontoudtog (eksempel) på siden Formatdesigner.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>Designe ER-formatkonfigurationen – tilknytning til en datamodel

Design en ER-formattilknytning, der bruger oplysninger fra fortolkningsfilen til at udfylde en datamodel.

1. Vælg **Knyt format til model** i handlingsruden på siden **Formatdesigner**.
2. Vælg **Ny** i handlingsruden på siden **Tilknytning af model til datakilde**.
3. Vælg **BankToCustomerDebitCreditNotificationInitiation** i feltet **Definition**.
4. Angiv **Tilknytning til datamodel** i feltet **Navn**.
5. Vælg **Gem**.
6. Vælg **Designer**.
7. Vælg **Dynamics 365 for Operations\\Klasse** på siden **Modeltilknytningsdesigner** i træet **Datakildetyper**.
8. I afsnittet **Datakilder** skal du vælge **Tilføj rod** for at tilføje en datakilde, der kalder den eksisterende programlogik til validering af IBAN-koder.
9. Følg disse trin i den viste dialogboks:

    1. I feltet **Navn** skal du angive **Kontrollér\_koder**.
    2. Indtast eller vælg **ISO7064** i feltet **Klasse**.
    3. Vælg **OK**.

10. Følg disse trin i træet **Datakildetyper**:

    1. Udvid datakilden **format**.
    2. Udvid **format\\Rod: Sequence(Root)**.
    3. Udvid **format\\Rod: Sequence(Root)\\Rækker: Sekvens 1..\* (Rækker)**.
    4. Udvid **format\\Rod: Sequence(Root)\\Rækker: Sekvens 1..\* (Rækker)\\Felter: Sekvens 1..1 (Felter)**.

11. Følg disse trin i træet **Datamodel**:

    1. Udvid feltet **Betalinger** i datamodellen.
    2. Udvid **Betalinger\\Kreditorkonto(CreditorAccount)**.
    3. Udvid **Betalinger\\Kreditorkonto(CreditorAccount)\\Identifikation**.
    4. Udvid **Betalinger\\Kreditorkonto(CreditorAccount)\\Identifikation\\IBAN**.

12. Benyt følgende fremgangsmåde for at binde komponenter i det konfigurerede format til datamodelfelter:

    1. Vælg **format\\Rod: Sequence(Root)\\Rækker: Sekvens 1..\* (Rækker)**.
    2. Vælg **Betalinger**.
    3. Vælg **Bind**. Baseret på denne indstilling skal hver linje i fortolkningsfilen betragtes som en enkelt betaling.
    4. Vælg **format\\Rod: Sequence(Root)\\Rækker: Sekvens 1..\* (Rækker)\\Felter: Sekvens 1..1 (Felter)\\IBAN: Streng(IBAN)**.
    5. Vælg **Betalinger\\Kreditorkonto(CreditorAccount)\\Identifikation\\IBAN**.
    6. Vælg **Bind**. På baggrund af denne indstilling udfyldes **IBAN**-feltet for datamodellen med værdien fra fortolkningsfilen.

    ![Binding af formatkomponenter til datamodelfelter på siden Modeltilknytningsdesigner.](../media/design-expressions-app-class-er-02.png)

13. Benyt følgende fremgangsmåde under fanen **Valideringer** for at tilføje en [valideringsregel](../general-electronic-reporting-formula-designer.md#Validation), der viser en fejlmeddelelse for en linje i fortolkningsfilen, som indeholder en ugyldig IBAN-kode:

    1. Vælg **Ny**, og vælg derefter **Rediger betingelse**.
    2. På siden **Formeldesigner** i **Datakilde**-træet kan du udvide datakilden **Kontrollér\_koder**, der repræsenterer **ISO7064**-programklassen, for at få vist de tilgængelige metoder i denne klasse.
    3. Vælg **Kontrollér\_koder\\verifyMOD1271\_36**.
    4. Vælg **Tilføj datakilde**.
    5. I feltet **Formel** skal du angive følgende [udtryk](../general-electronic-reporting-formula-designer.md#Binding): **Kontrollér\_koder.verifyMOD1271\_36(format.Rod.Rækker.Felter.IBAN)**.
    6. Vælg **Gem**, og luk derefter siden.
    7. Vælg **Rediger meddelelse**.
    8. På siden **Formeldesigner** skal du i feltet **Formel** angive **CONCATENATE("Ugyldig IBAN-kode er fundet:&nbsp;", format.Rod.Rækker.Felter.IBAN)**.
    9. Vælg **Gem**, og luk derefter siden.

    Baseret på disse indstillinger vil valideringsbetingelsen returnere *[FALSE](../er-formula-supported-data-types-primitive.md#boolean)* for enhver ugyldig IBAN-kode ved at kalde den eksisterende metode **verifyMOD1271\_36** i programklassen **ISO7064**. Bemærk, at værdien af IBAN-koden defineres dynamisk under kørsel som argument i kaldemetoden baseret på indholdet af tekstfilen til fortolkning.

    ![Valideringsregel på siden Modeltilknytningsdesigner.](../media/design-expressions-app-class-er-03.png)

14. Vælg **Gem**.
15. Luk siden **Modeltilknytningsdesigner**, og luk derefter siden **Tilknytning af model til datakilde**.

## <a name="run-the-format-mapping"></a>Kør formattilknytningen

Til testformål skal du køre formattilknytningen ved hjælp af filen SampleIncomingMessage.txt, som du tidligere har hentet. Det genererede output omfatter data, der importeres fra den valgte tekstfil og overføres til den brugerdefinerede datamodel under den faktiske import.

1. Vælg **Kør** på siden **Tilknytning af model til datakilde**.
2. På siden **Parametre for elektronisk rapport** skal du vælge **Gennemse**, navigere til den **SampleIncomingMessage.txt**-fil, du har hentet, og vælge den.
3. Vælg **OK**.
4. Bemærk, at der på siden **Tilknytning af model til datakilde** vises en fejlmeddelelse om en ugyldig IBAN-kode.

    ![Resultat af kørt formattilknytning på siden Tilknytning af model til datakilde.](../media/design-expressions-app-class-er-04.png)

5. Gennemgå outputtet i XML-format, som viser de data, der er importeret fra den valgte fil og overført til datamodellen. Bemærk, at kun tre linjer i den importerede tekstfil er behandlet uden fejl. IBAN-koden på linje 4 er ikke gyldig og blev sprunget over.

    ![XML-output.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
