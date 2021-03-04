---
title: Konfigurere tilføjelsesprogrammet til elektronisk fakturering
description: Dette emne beskriver, hvordan du konfigurerer tilføjelsesprogrammet til elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7e631f1bf64b47b5f3e85d4f98c6edafe67d627a
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/19/2020
ms.locfileid: "4441739"
---
# <a name="set-up-the-electronic-invoicing-add-on"></a>Konfigurere tilføjelsesprogrammet til elektronisk fakturering

[!include [banner](../includes/banner.md)]


Funktionsopsætningen for tilføjelsesprogrammet til elektronisk fakturering er processen til oprettelse af den krævede konfiguration via RCS-miljøet (Regulatory Configuration Services) og udgivelse af denne konfiguration på serveren for tilføjelsesprogrammet til elektronisk fakturering. Konfigurationen gør det muligt at oprette de konfigurerbare regler, tilføjelsesprogrammet til elektronisk fakturering kan bruge en sikker protokol over internettet til at kommunikere og udveksle data med en tredjepartsenhed ved hjælp af webtjenester.

Mulighederne for konfiguration er afhængig af det elektroniske rapporteringsformat (ER) for at oprette indhold, der sendes og modtages via digitale filer. Det er også afhængigt af organiseringen af kommunikationshandlinger for at sende anmodninger til og modtage svar fra tredjepartswebtjenester uden behov for at skrive kode.

## <a name="overview"></a>Overblik

"Funktionen for tilføjelsesprogrammet til elektronisk fakturering" er det generiske navn på den ressource, der er konfigureret og publiceret til at bruge serveren for tilføjelsesprogrammet til elektronisk fakturering. Funktionsopsætningen kombinerer bl.a. brugen af ER-konfigurationsformater for til at oprette konfigurerbare eksport- og importfiler samt brugen af handlinger og handlingsflow for at muliggøre oprettelsen af regler til at sende anmodninger, importere svar og analysere indhold i svar.

I følgende illustration vises hovedkomponenterne af en funktion for tilføjelsesprogrammet til elektronisk fakturering.

![Oversigt over funktionen for tilføjelsesprogrammet til elektronisk fakturering](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

På grund af variationer i fakturaformater og handlingsflow kan funktionsopsætningen variere afhængigt af land eller område eller efter forretningsbehov.

## <a name="set-up-the-electronic-invoicing-add-on-feature"></a>Konfigurere funktionen for tilføjelsesprogrammet til elektronisk fakturering

Konfigurationsprocessen skal fuldføres i dit RCS-miljø. Følg nedenstående trin for at oprette en ny funktioon for tilføjelsesprogrammet til elektronisk fakturering.

1. Log på dit RCS-miljø.
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.
3. På siden med **funktioner for tilføjelsesprogrammet til elektronisk fakturering** skal du vælge **Importér** for at importere ER-datamodelkonfigurationen fra det globale lager.
4. Vælg **Tilføj** for at oprette en funktion for tilføjelsesprogrammet til elektronisk fakturering. Du kan enten oprette funktionen fra bunden eller have den afledt fra en eksisterende funktion for tilføjelsesprogrammet til elektronisk fakturering.

    ![Tilføje en funktion for tilføjelsesprogrammet til elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Når du opretter en ny funktion for tilføjelsesprogrammet til elektronisk fakturering, har den et versionsnummer, og standardstatussen er angivet til **Kladde**.

### <a name="configurations"></a>Varianter

Konfigurationer indeholder de ER-formatkonfigurationer, der kræves til transformationer og til at oprette de filer, der udveksles under kommunikationen med tredjepartswebtjenester. En funktion for tilføjelsesprogrammet til elektronisk fakturering kan have det antal ER-filformatkonfigurationer, som er nødvendige, på baggrund af den tekniske specifikation for integration, som webtjenesteudbyderen har stillet til rådighed.

Følg nedenstående trin for at føje ER-formater til funktionen for tilføjelsesprogrammet til elektronisk fakturering.

1. På siden med **funktioner for tilføjelsesprogrammet til elektronisk fakturering** skal du på fanen **Konfigurationer** vælge **Tilføj** for at føje ER-filformatkonfigurationer til funktionen for tilføjelsesprogrammet til elektronisk fakturering.

    ![Tilføje konfigurationer af funktionen for tilføjelsesprogrammet til elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Når du opretter en funktion for tilføjelsesprogrammet til elektronisk fakturering fra bunden, skal du manuelt tilføje alle ER-filformatkonfigurationerne. Når du har afledt en funktion for tilføjelsesprogrammet til elektronisk fakturering fra en eksisterende funktion, oprettes ER-filformatkonfigurationerne automatisk, fordi de nedarves fra den oprindelige funktion for tilføjelsesprogrammet til elektronisk fakturering.

2. Vælg **Rediger** for at åbne siden **Formatdesigner**, hvor du kan redigere ER-filformatkonfigurationer.

    ![Redigere konfigurationer af funktionen for tilføjelsesprogrammet til elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Når du redigerer formatet, angives statussen for konfigurationsversionen til **Kladde**.

3. Du kan bruge siden **Formatdesigner** til at ændre filformatkonfigurationen. Du kan finde flere oplysninger i [Oprette konfigurationer for elektroniske dokumenter](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Siden Formatdesigner](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Funktionsopsætninger

Funktionsopsætninger indkapsler reglerne for kommunikation og sikkerhed med en tredjepartswebtjeneste. En funktion for tilføjelsesprogrammet til elektronisk fakturering kan det antal funktionsopsætninger, som er nødvendige, ud fra den forretningsregel, du vil opnå.

Følg nedenstående trin for at føje funktionsopsætninger til funktionen for tilføjelsesprogrammet til elektronisk fakturering.

1. På siden med **funktioner for tilføjelsesprogrammet til elektronisk fakturering** skal du på fanen **Konfigurationer** vælge **Tilføj** for at føje funktionsopsætninger til funktionen for tilføjelsesprogrammet til elektronisk fakturering.

    ![Tilføje funktionsopsætninger for tilføjelsesprogrammet til elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Når du opretter en funktion for tilføjelsesprogrammet til elektronisk fakturering fra bunden, skal du manuelt tilføje alle de nødvendige funktionsopsætninger. Når du har afledt en funktion for tilføjelsesprogrammet til elektronisk fakturering fra en eksisterende funktion, oprettes alle funktionsopsætninger automatisk, fordi de nedarves fra den oprindelige funktion for tilføjelsesprogrammet til elektronisk fakturering.

2. Vælg **Rediger** for at redigere opsætningen af funktionsversionen.

    ![Redigere funktionsopsætninger for tilføjelsesprogrammet til elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. Du kan bruge siden **Opsætning af funktionsversion** til at konfigurere handlinger, anvendelighedsregler og variabler.

    ![Handlinger, anvendelighedsregler og variabler](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Handlinger

Handlinger er en foruddefineret liste over operationer, der køres i sekventiel rækkefølge. Denne liste repræsenterer opdelingen af de trin, der kræves til fuld udførelse af funktionen for tilføjelsesprogrammet til elektronisk fakturering. Handlingerne kan – i den samme funktion for tilføjelsesprogrammet til elektronisk fakturering – indkapsle kommunikationen i begge retninger: sende en anmodning om en destination og modtage svar og fortolke indholdet.

Hver handling indeholder en foruddefineret liste med parametre, der kræves, for at handlingen kan opnå målet. Der kan eventuelt angives yderligere parametre.

#### <a name="actions-fasttab"></a>Oversigtspanelet Handlinger

På siden **Opsætning af funktionsversion** skal du på fanen **Handlinger** i oversigtspanelet **Handlinger** følge et af eller begge disse trin for at administrere handlinger:

- Vælg **Ny** eller **Slet** for at tilføje nye handlinger eller slette eksisterende handlinger.
- Vælg **Op** eller **Ned** for at flytte markerede handlinger op eller ned i gitteret og derfor ændre den rækkefølge, de køres i. Handlinger køres i den rækkefølge, hvormed de vises i gitteret, fra top til bund.

![Administrere handlinger](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Handlinger**.

| Felt        | Betegnelse |
|--------------|-------------|
| Handling       | Der findes otte foruddefinerede handlinger.<ul><li><strong>Underskriv dokument</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Transformér dokument</strong></li><li><strong>Behandl svar</strong></li><li><strong>Kald REST-webtjeneste</strong></li><li><strong>Kald mexicansk PAC-tjeneste</strong></li><li><strong>Kald brasiliansk SEFAZ-tjeneste</strong></li><li><strong>Kald italiensk SDI-tjeneste</strong></li></ul> |
| Handlingsnavn  | Navnet på handlingen og rækkefølgen for udførelse. |
| Betegnelse  | En beskrivelse af handlingen. |
| Aktiver forsøg igen | Et markeret afkrydsningsfelt angiver, at handlingen kan forsøges igen, hvis det forrige forsøg mislykkedes. |
| Handling for gentagelse | I tilfælde af et nyt forsøg den handling, det nye forsøg starter fra. Forsøget afsluttes derefter med den aktuelle handling (herunder nye forsøg). I forbindelse med handlinger, der har dem, angiver parametrene **Min. back-off** og **Maks. back-off** det mindste antal og det maksimale antal forsøg. |

#### <a name="parameters-fasttab"></a>Oversigtspanelet Parametre

I oversigtspanelet **Parametre** vises parametrene for den handling, der er valgt i oversigtspanelet **Handlinger**.

![Oversigtspanelet Parametre](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Parametre**.

| Felt       | Betegnelse |
|-------------|-------------|
| Navn        | En foruddefineret liste over parametre. Du kan finde flere oplysninger i sektionen [Liste over parametre efter handling](#list-of-parameters-by-action). |
| Betegnelse | En beskrivelse af parameteren. |
| Værdi       | Værdien for parameteren. |

#### <a name="list-of-parameters-by-action"></a>Liste over parametre efter handling

De tilgængelige parametre varierer, afhængigt af den handling, der er valgt i oversigtspanelet **Handlinger**.

###### <a name="action-sign-document"></a>Handling: Underskriv dokument

| Parameter                             | Betegnelse |
|---------------------------------------|-------------|
| Inputfil                            | Den input-XML-dokumentfil, der skal underskrives ved hjælp af en elektronisk signatur. |
| Certifikatnavn                      | Navnet på certifikatet i lageret. |
| Signaturtype                        | Den signaturtype, der skal bruges. |
| Navn på signaturmetode                 | Navnet på den signaturmetode, der bruges til at oprette en elektronisk signatur. |
| Navn på digest-metode                    | Den digest-metode, der bruges til at generere en digest-streng i den digitale signatur. |
| Navn på godkendt metode          | Den godkendte metode, der bruges til at beregne signaturens hash. |
| Navn på referenceattribut              | Det attributnavn, der angiver, hvor reference-id'et skal indsættes i signaturelementet. |
| Navn på det element, der skal underskrives               | Navnet på det XML-element i dokumentet, der skal underskrives ved hjælp af en elektronisk signatur. Hvis der ikke er angivet et element, underskrives roden af dokumentet. |
| Navn på det element, hvor signaturen skal indsættes   | Navnet på det XML-element, hvor den oprettede digitale signatur skal indsættes. Hvis der ikke er angivet et element, indsættes signaturen i roden af dokumentet. |
| XLST-fil med digest-transformation       | XSLT-filen (Extensible Stylesheet Language Transformations), der indeholder regler for digest-transformation til oprettelse af digest-strengen for en elektronisk signatur. |
| Sti til indsættelse af digest-streng          | Stien, i formatet **\<elementName\>.\<Attribute.Path\>**, for den placering, hvor den oprettede digest-streng skal indsættes. |
| Placering af certifikatnummer           | Navnet på det element og den attribut, hvor certifikatnummeret skal placeres. |
| Placering af certifikatdata          | Navnet på det element og den attribut, hvor certifikatdataene (Base64) skal indsættes. |
| Certifikatnummeret er i ASCII-format | En værdi, der angiver, om nummeret på certifikatet er kodet i ASCII-format. |

###### <a name="action-filestoreactionname"></a>Handling: FileStoreActionName

| Parameter  | Betegnelse |
|------------|-------------|
| Inputfil | Den inputfil, der skal gemmes. |

###### <a name="action-transform-document"></a>Handling: Transformér dokument

| Parameter                       | Betegnelse |
|---------------------------------|-------------|
| Inputfil                      | Den kildefil, der indeholder de data, som skal køres for handlingen. |
| Vej                       | En værdi, der angiver, om importformatet eller eksportformatet skal bruges. |
| Konfigurations-id                | Det format, der skal køres. |
| Konfigurationsversion           | Hvis der ikke er angivet en konfigurationsversion, vil den seneste version blive brugt. |
| Integrationspunkt for konfiguration | Den kildefil, der indeholder data til kørsel af rapporteringen. |

###### <a name="action-process-response"></a>Handling: Behandl svar

| Parameter                    | Betegnelse |
|------------------------------|-------------|
| Inputfil                   | Det svar, der skal analyseres. |
| Liste over rapporteringskonfiguration | En liste over konfigurationer, der bruges til at fortolke svar. |

###### <a name="action-call-rest-web-service"></a>Handling: Kald REST-webtjeneste

| Parameter                   | Betegnelse |
|-----------------------------|-------------|
| URL-adresse til webtjeneste             | Den URL-adresse, der skal sendes anmodninger til. |
| Timeout for webanmodning         | Det maksimale tidsrum (i millisekunder), der skal ventes på et svar fra webtjenesten. |
| Operationstype på anmodning      | Operationstypen på HTTP-anmodningen (f.eks. **GET**, **POST** eller **DELETE**). |
| Certifikatnavne           | Certifikatnavnene. |
| Kodning på svarets brødtekst      | Den forventede kodning på svarets HTTP-brødtekst, så det kan afkodes korrekt. |
| Indholdstype for HTTP-anmodning   | Headerinput for indholdstypen på HTTP-anmodningen. |
| Indholdsbrødteksten for HTTP-anmodningen   | Brødteksten i HTTP-anmodningen. (Brødteksten kan stå tom). |
| HTTP-parameterforespørgselsværdier | Parameterforespørgselsværdier, der bruges til at udfylde URL-adressen med variable parametre. |
| Anmodningsrute               | Rutestien for HTTP-anmodningen. De variable parametre kan skrives i anmærkningen **\{paramName\}**. Her er et eksempel: **"api/{id}/submit"**. |
| Liste over ruteparametre        | Ruteparametrene, i nøgleværdianmærkning, der bruges til at indsætte variabler i ruten. |
| Brugerdefinerede HTTP-headere         | De brugerdefinerede HTTP-headere, der skal placeres i anmodningen. |
| Cookies for HTTP-anmodning        | En liste over cookies, i nøgleværdianmærkning, som skal placeres i cookieheaderen for HTTP-anmodningen. |
| Sikkerhedsprotokol           | Den sikkerhedsprotokol, der skal bruges til HTTP-anmodninger for at kommunikere med serveren. (Transport Layer Security \[TLS\] 1.2 bruges som standard). |

###### <a name="action-call-mexican-pac-service"></a>Handling: Kald mexicansk PAC-tjeneste

| Parameter                | Betegnelse |
|--------------------------|-------------|
| Inputfil               | Den fil, der indeholder XML-data, som vil blive sendt til webtjenesten som en metodeinputparameter. |
| URL-adresse              | Webtjenesteadresse (slutpunkt). |
| Navn på webmetode (handling) | Navnet på den webmetode (handling), der skal køres. |
| Certifikater             | Den certifikatkæde, der kræves til klientgodkendelse af webtjenesten. Klientcertifikatet skal være det sidste certifikat i kæden. Rodcertifikater og midlertidige certifikater skal være først. |
| Timeout for webanmodning      | Det maksimale tidsrum (i millisekunder), der skal ventes på et svar fra webtjenesten. |
| Interval mellem forsøg           | Intervallet mellem forsøg på at kalde og modtage svar fra webtjenesten. Hvis der ikke er angivet et interval, foretages der ingen yderligere forsøg, når det første kald mislykkes. |
| Antal forsøg              | Det maksimale antal forsøg på at kalde og modtage et svar fra webtjenesten. |
| Tidsfrist for forsøg               | Den maksimale tid (i millisekunder), som forsøg på at kalde kan fortsætte. |
| Min. back-off         | Min. back-off-frekvens for eksponentiel beregning af intervaller mellem forsøg. |
| Maks. back-off         | Maks. back-off-frekvens for eksponentiel beregning af intervaller mellem forsøg. |
| Sikkerhedsprotokol        | Den sikkerhedsprotokol, der skal bruges til HTTP-anmodninger for at kommunikere med serveren. (TLS 1.2 bruges som standard). |

###### <a name="action-call-brazilian-sefaz-service"></a>Handling: Kald brasiliansk SEFAZ-tjeneste

| Parameter                | Betegnelse |
|--------------------------|-------------|
| Inputfil               | Den fil, der indeholder XML-data, som vil blive sendt til webtjenesten som en metodeinputparameter. |
| URL-adresse              | Webtjenesteadresse (slutpunkt). |
| Navn på webmetode (handling) | Navnet på den webmetode (handling), der skal køres. |
| Certifikater             | Den certifikatkæde, der kræves til klientgodkendelse af webtjenesten. Klientcertifikatet skal være det sidste certifikat i kæden. Rodcertifikater og midlertidige certifikater skal være først. |
| Timeout for webanmodning      | Det maksimale tidsrum (i millisekunder), der skal ventes på et svar fra webtjenesten. |
| Interval mellem forsøg           | Intervallet mellem forsøg på at kalde og modtage svar fra webtjenesten. Hvis der ikke er angivet et interval, foretages der ingen yderligere forsøg, når det første kald mislykkes. |
| Antal forsøg              | Det maksimale antal forsøg på at kalde og modtage et svar fra webtjenesten. |
| Tidsfrist for forsøg               | Den maksimale tid (i millisekunder), som forsøg på at kalde kan fortsætte. |
| Min. back-off         | Min. back-off-frekvens for eksponentiel beregning af intervaller mellem forsøg. |
| Maks. back-off         | Maks. back-off-frekvens for eksponentiel beregning af intervaller mellem forsøg. |
| Sikkerhedsprotokol        | Den sikkerhedsprotokol, der skal bruges til HTTP-anmodninger for at kommunikere med serveren. (TLS 1.2 bruges som standard). |

###### <a name="action-call-italian-sdi-service"></a>Handling: Kald italiensk SDI-tjeneste

| Parameter                | Betegnelse |
|--------------------------|-------------|
| Inputfil               | Den fil, der indeholder XML-data, som vil blive sendt til webtjenesten som en metodeinputparameter. |
| URL-adresse              | Webtjenesteadresse (slutpunkt). |
| Navn på webmetode (handling) | Navnet på den webmetode (handling), der skal køres. |
| Certifikater             | Den certifikatkæde, der kræves til klientgodkendelse af webtjenesten. Klientcertifikatet skal være det sidste certifikat i kæden. Rodcertifikater og midlertidige certifikater skal være først. |
| Timeout for webanmodning      | Det maksimale tidsrum (i millisekunder), der skal ventes på et svar fra webtjenesten. |
| Interval mellem forsøg           | Intervallet mellem forsøg på at kalde og modtage svar fra webtjenesten. Hvis der ikke er angivet et interval, foretages der ingen yderligere forsøg, når det første kald mislykkes. |
| Antal forsøg              | Det maksimale antal forsøg på at kalde og modtage et svar fra webtjenesten. |
| Tidsfrist for forsøg               | Den maksimale tid (i millisekunder), som forsøg på at kalde kan fortsætte. |
| Min. back-off         | Min. back-off-frekvens for eksponentiel beregning af intervaller mellem forsøg. |
| Maks. back-off         | Maks. back-off-frekvens for eksponentiel beregning af intervaller mellem forsøg. |
| Sikkerhedsprotokol        | Den sikkerhedsprotokol, der skal bruges til HTTP-anmodninger for at kommunikere med serveren. (TLS 1.2 bruges som standard). |

### <a name="applicability-rules"></a>Anvendelighedsregler

Anvendelighedsregler giver dig mulighed for at oprette logiske regler, der bestemmer anvendelseskonteksten for funktionsopsætningen. Sammenholdelsen mellem den kontekst, der er angivet for det forretningsdokument, der sendes til behandling, sammen med kriterierne for anvendelighedsreglen, bestemmer, hvilken funktion for tilføjelsesprogrammet til elektronisk fakturering der bruges til at behandle den pågældende indsendelse.

#### <a name="set-up-applicability-rules"></a>Konfigurere anvendelighedsregler

1. På siden **Opsætning af funktionsversion** skal du på fanen **Anvendelighedsregler** vælge **Ny** for at tilføje en anvendelighedsregel.

    ![Administrere anvendelighedsregler](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. Vælg de delsætninger, der skal grupperes, i gitteret.
3. Vælg **Gruppér delsætning**.

    ![Gruppere delsætninger](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Når delsætningerne er grupperet, føjes der en ny kolonne til gitteret. Denne kolonne angiver den logiske operator for de grupperede delsætninger.

    ![Logisk operator for grupperede delsætninger](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Hvis du vil opdele grupperede delsætninger, skal du vælge de grupperede delsætninger, der skal opdeles, og derefter vælge **Opdel grupperet delsætning**.

![Opdele grupperede delsætninger](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Når du opdeler en grupperet delsætning, skal du altid starte fra det inderste grupperingsniveau.

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Anvendelighedsregler**.

| Felt         | Betegnelse |
|---------------|-------------|
| Og/eller        | Den logiske operator. |
| Felt         | Det felt, der skal bruges til at konstruere reglen. |
| Operatortype | Operatortypen:<ul><li>Lig</li><li>Ikke lig med</li><li>Større end/mindre end</li><li>Større end eller lig med/mindre end eller lig med</li><li>Indeholder</li><li>Begynd med</li></ul> |
| Værdi         | Kriteriet for reglen. |

### <a name="variables"></a>Variabler

Du kan oprette variabler og derefter bruge dem som inputværdi for en parameter for en bestemt handling. Du kan også bruge dem til at udveksle – mellem tjenesterne for tilføjelsesprogrammet til elektronisk fakturering og klienten – oplysninger, der er resultatet af udførelsen af en bestemt handling som del af indsendelsesflowet.

#### <a name="set-up-variables"></a>Konfigurer variabler

- På siden **Opsætning af funktionsversion** skal du på fanen **Variabler** vælge **Ny** eller **Slet** for at administrere variabler.

    ![Administrere variabler](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

I følgende tabel forklares de felter, der er tilgængelige i oversigtspanelet **Variabler**.

| Felt       | Betegnelse |
|-------------|-------------|
| Navn        | Navnet på variablen. |
| Betegnelse | En kort beskrivelse af variablen. |
| Type        | Variabeltypen:<ul><li><strong>Konstant</strong> – indholdet af variablen er fast.</li><li><strong>Fra klient</strong> – indholdet af variablen hentes fra Microsoft Dynamics 365-klienten under udførelsen af indsendelsesprocessen.</li><li><strong>Til klient</strong> – indholdet af variablen er gjort tilgængelig til import af Microsoft Dynamics 365-klienten under udførelsen af indsendelsesprocessen.</li></ul> |
| Datatype   | Datatypen for variablen:<ul><li>Boolesk</li><li>Dato</li><li>Tal</li><li>UUID</li><li>Streng</li><li>Filer</li></ul> |
| Værdi       | Variablens værdi eller navnet på den handling, der angiver variablens værdi. |

### <a name="validate-the-feature-setup"></a>Validere funktionsopsætning

- På siden **Opsætning af funktionsversion** skal du i handlingsruden vælge **Valider** for at validere opsætningen af funktionsversionen.

   ![Vælge knappen Valider](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Valideringen kontrollerer konsistensen af hele konfigurationen. Hvis en bestemt parameter til en handling f.eks. er obligatorisk, men værdien stadig er tom, registrerer valideringen denne inkonsistens, og du modtager en advarsel.

## <a name="environments"></a>Miljøer

Et miljø for tilføjelsesprogrammet til elektronisk fakturering skal knyttes til og være aktiveret for funktionen for tilføjelsesprogrammet til elektronisk fakturering. Miljøer for tilføjelsesprogrammet til elektronisk fakturering skal oprettes og publiceres på forhånd via konfigurationen af globaliseringsfunktionerne i din organisations RCS-konto.

Følg nedenstående trin for at aktivere et miljø for tilføjelsesprogrammet til elektronisk fakturering for funktionen for tilføjelsesprogrammet til elektronisk fakturering.

1. På siden med **funktioner for tilføjelsesprogrammet til elektronisk fakturering** skal du på fanen **Miljøer** vælge **Aktivér** for at tilføje et miljø for tilføjelsesprogrammet til elektronisk fakturering.
2. I feltet **Gyldig fra** skal du angive den dato, hvor det nye miljø skal være gyldigt.

![Aktivere et miljø for tilføjelsesprogrammet til elektronisk fakturering](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Organisationer

Funktionen for tilføjelsesprogrammet til elektronisk fakturering kan deles på tværs af flere organisationer.

- På siden med **funktioner for tilføjelsesprogrammet til elektronisk fakturering** skal du på fanen **Organisationer** vælge **Del med** for at tilføje den organisation, du vil dele funktionen for tilføjelsesprogrammet til elektronisk fakturering med.

Hvis du ikke længere vil dele funktionen for tilføjelsesprogrammet til elektronisk fakturering med organisationen, skal du vælge **Fjern deling**.

## <a name="versions"></a>Versioner

Versioner hjælper dig med at styre livscyklussen for funktionen for tilføjelsesprogrammet til elektronisk fakturering ved at administrere statussen. Du kan oprette en ny version af en eksisterende funktion for tilføjelsesprogrammet til elektronisk fakturering, eller du kan ændre funktionens status til **Fuldført** og derefter til **Publicer**, når alle konfigurationer for funktionen for tilføjelsesprogrammet til elektronisk fakturering er fuldført.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-add-on-feature"></a>Oprette en ny version af en eksisterende funktion for tilføjelsesprogrammet til elektronisk fakturering

1. På siden med **funktioner for tilføjelsesprogrammet til elektronisk fakturering** skal du på gitteret til venstre vælge funktionen for tilføjelsesprogrammet til elektronisk fakturering.
2. Vælg **Ny** på fanen **Versioner** for at tilføje en ny version af funktionen for tilføjelsesprogrammet til elektronisk fakturering.

### <a name="change-the-status-of-the-electronic-invoicing-add-on-feature"></a>Ændre statussen på funktionen for tilføjelsesprogrammet til elektronisk fakturering

Følg nedenstående trin for at administrere livscyklussen for funktionen for tilføjelsesprogrammet til elektronisk fakturering.

1. På siden med **funktioner for tilføjelsesprogrammet til elektronisk fakturering** skal du på gitteret til venstre vælge funktionen for tilføjelsesprogrammet til elektronisk fakturering.
2. Vælg **Skift status** på fanen **Versioner**, og skift derefter statussen fra **Kladde** til **Fuldført**.
3. Du bliver bedt om at bekræfte, at du vil fuldføre funktionen for tilføjelsesprogrammet til elektronisk fakturering og alle tilhørende komponenter. Vælg **Ja** for at bekræfte handlingen eller **Nej** for at annullere den.

    > [!NOTE]
    > Når du vælger **Ja**, ændres statussen for konfigurationsversioner, der er komponenter i funktionen for tilføjelsesprogrammet til elektronisk fakturering, automatisk fra **Kladde** til **Fuldført**.

4. Vælg **Skift status**, og skift derefter statussen fra **Fuldført** til **Publicer**.
5. Du bliver bedt om at bekræfte, at du vil publicere funktionen for tilføjelsesprogrammet til elektronisk fakturering og alle tilhørende komponenter til det globale lager. Vælg **Ja** for at bekræfte handlingen eller **Nej** for at annullere den.

    > [!NOTE]
    > Når du vælger **Ja**, ændres statussen for konfigurationsversioner automatisk fra **Fuldført** til **Delt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]