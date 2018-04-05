---
title: Modtage kreditorer
description: "I dette emne beskrives processen til modtagelse af nye kreditorer. I emnet beskrives de handlinger, der kræves af forskellige roller under denne proces."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests,SysUserRequestListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 7265e119a8b59399db1fa35373a7b6aba52ba8e0
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="onboard-vendors"></a>Modtage kreditorer
[!include[banner](../includes/banner.md)]
---

Nye kreditorer kan modtages og registreres som kreditorer i Microsoft Dynamics 365 for Finance and Operations baseret på oplysninger, der er indsamlet fra en person, der repræsenterer kreditoren.

Processen består af følgende trin, hvor forskellige roller udfører handlinger i systemet.

1. **OData til datastyring** – Import af enhed – Den oprindelige anmodning er anmodningen om registrering af den mulige kreditor. Denne anmodning stammer normalt fra en kilde som f.eks. et websted til hos kunden, der tillader anonym adgang. Kreditorer kan tilmelde sig ved at angive grundlæggende oplysninger, f.eks. kreditornavnet, berettigelse, organisationsnummer og navn på og mailadresse til kontaktpersonen. Anmodningerne importeres via brugergrænsefladen i Datastyring.
2. **Listeside med registreringsanmodning for mulige kreditorer** - Baseret på de oplysninger, der er angivet i registreringsanmodningen for mulige kreditorer, beslutter en anmoder, om kreditoren skal modtages. Anmoderen kan se den indgående anmodning på listesiden **Anmodninger om registrering af mulig kreditor** i Finance and Operations.
3. **Arbejdsgang for brugerklargøring** – Når en anmoder har kontrolleret oplysningerne i den indgående anmodning og har besluttet at fortsætte modtagelsesprocessen, klargør brugeranmodningsarbejdsgangen den nye bruger og sender en mail med invitation til at acceptere kontaktpersonen som godkendt bruger af Microsoft Dynamics 365.
4. **Guide til registrering af kreditorer** - Kreditorens kontaktperson logger på Finance and Operations ved hjælp af den nye brugerkonto. Han eller hun kører en kreditorregistreringsguide for at angive oplysninger som f.eks. adresser, forretningsoplysninger, indkøbskategorier og spørgeskemasvar.
5. **Godkendelsesarbejdsgang** - Der oprettes en kreditoranmodning, der indeholder oplysningerne om registreringen. Denne kreditoranmodning sendes til en arbejdsgang og videresendes til gennemsyn og godkendelse.
6. **Oprettelse af en kreditormaster og ændring af brugerrolle** – Når kreditoranmodningen er godkendt, oprettes en kreditorpost. Brugerkontoen for kreditorens kontaktperson har enten tilladelse til samarbejde med leverandøren eller er deaktiveret.

I følgende tabel vises de trin og roller, der er involveret i processen.

| Rolle og "proces"       | OData til datastyring – import af enhed | Listeside med registreringsanmodning for mulige kreditorer | Arbejdsgang for brugerklargøring | Guiden til registrering af kreditorer | Godkendelsesarbejdsgang | Oprettelse af en kreditormaster og ændring af brugerrolle |
|--------------------------|---|---|---|---|---|---|
| System                   | Anmodningen om en ny kreditor importeres. | | | | | Når kreditoranmodningen er accepteret, oprettes kreditorposten. |
| Anmoder | | Start modtagelsesprocessen. | | | Gennemse og accepter eller afvis kreditoranmodningen. | |
| Administrator            | | | Opret en bruger i Finance and Operations og Microsoft Azure. | | | |
| Kreditors kontaktperson    | | | Send e-mail til kontaktpersonen. | Registrer oplysninger om kreditoren. | | |

Du kan se en hurtig demonstration af processen til onboarding af kreditor i denne korte YouTube-video: 
> [!Video https://www.youtube.com/embed/0KUc3AGaTKk]

## <a name="importing-the-prospective-vendor-registration-request"></a>Import af anmodning om registrering af mulig kreditor

Registreringsanmodningen for den mulige kreditor er en enhed i Finance and Operations. Du kan konfigurere systemet til at importere data via denne enhed. 

I følgende tabel vises de oplysninger, som denne enhed indeholder, og som kan importeres.

| Felt                        | Betegnelse |
|------------------------------|-------------|
| Navn på kreditor                  | Kreditorens navn. |
| Forretningsberettigelse       | Årsagen eller årsagerne til kreditoranmodningen. |
| Organisationsnummer          | Et officielt kendt registreringsnummer. |
| Forretningsområder             | Det forretningsområde, som kreditoren driver forretning i. |
| Kontaktpersonens fornavn  | Fornavnet på den person, der inviteres til at registrere kreditoroplysninger. |
| Kontaktpersonens mellemnavn | Mellemnavnet på den person, der inviteres til at registrere kreditoroplysninger. |
| Kontaktpersonens efternavn   | Efternavnet på den person, der inviteres til at registrere kreditoroplysninger. |
| Kontaktpersonens e-mail       | Den e-mailadresse, der skal bruges til at oprette en ny bruger i Finance and Operations, og som vil blive registreret i lejerens Azure Active Directory (Azure AD)-konto. |
| Afsendelsesdato               | Den dato, hvor anmodningen blev oprettet i et eksternt system. |
| Juridisk enhed                 | Den juridiske enhed, hvor kreditoren anmoder om at blive kreditor. Denne værdi skal være en kode for en juridisk enhed, der er registreret i Finance and Operations. Hvis ingen værdi modtages under importprocessen, anvendes en værdi fra indkøbs- og forsyningsparametrene. |
| Kreditortype                  | Kreditoren kan enten være en organisation eller en person. Kreditortypen bestemmer, hvordan kreditoren oprettes til slut. |

Efter at anmodningen om registrering af den mulige kreditor er importeret, vises den på listesiden **Anmodning om registrering af mulig kreditor**. En anmoder kan invitere brugeren fra denne listeside. En brugeranmodning om klargøring af brugeren sendes til en arbejdsgang.

## <a name="submitting-a-prospective-vendor-user-request"></a>Afsendelse af en anmodning om mulig kreditorbruger

Formålet med en mulig kreditorbrugeranmodning er, at klargøre den person, som sendte den oprindelige anmodning, så vedkommende kan logge på Finance and Operations ved hjælp af den e-mailkonto, som findes i anmodningen om registrering af mulig kreditor.

Anmodningen om mulig kreditorbruger behandles af brugeranmodningsarbejdsgangen. Denne arbejdsgang kommunikerer via Azure AD B2B-samarbejde. Den opretter en bruger i Finance and Operations, der har de nødvendige sikkerhedsindstillinger.

Nye brugere, der oprettes, har følgende sikkerhedsroller:

- Ekstern systembruger
- Kreditormulighed (ekstern)

Den nye bruger modtager en e-mail, der genereres af brugeranmodningsarbejdsgangen. Denne e-mail inviterer brugeren til at logge på systemet.

Oplysninger om konfigurationen af e-mailen og arbejdsgangen generelt finder du i beskrivelsen af en brugeranmodningsarbejdsgangen i [Konfigurere og vedligeholde kreditorsamarbejde](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Registrering af kreditor

En mulig kreditorbruger, der logger på Finance and Operations, ser den første side i en kreditorregistreringsguide, hvor han eller hun kan angive kreditoroplysninger.

Guiden afspejler konfigurationen af kreditoranmodningen. Det land eller område, hvor kreditoren handler, bestemmer, hvilke oplysninger der anmodes om i guiden, og hvilke oplysninger er obligatoriske.

Du kan finde flere oplysninger om opsætning af kreditoranmodningen under [Konfigurere og vedligeholde kreditorsamarbejde](set-up-maintain-vendor-collaboration.md). Følgende tabel indeholder en oversigt over siderne i guiden og formålet med hver side.

| Side                       | Betegnelse |
|----------------------------|-------------|
| Land/område             | Landet eller området bestemmer den konfiguration af kreditoranmodninger, der anvendes på de resterende guidesider. Det bestemmer også værdierne i opslaget **Momstilstand**. |
| Vilkår og betingelser       | Denne side kan være tilgængelige, afhængigt af konfigurationen af kreditoranmodningen. Hvis den er tilgængelig, skal brugeren acceptere vilkårene og betingelserne for at fortsætte. |
| Kreditoroplysninger         | Denne side indeholder kreditornavnet, som automatisk indsættes fra den oprindelige registreringsanmodning for den mulige kreditor. Siden indeholder også organisationsnummeret, kreditorens telefonnummer, faxnummer og e-mailadresse og kreditorens adresser til forskellige formål. |
| Oplysninger om kontaktperson | Denne side indeholder kontaktpersonens navn, som automatisk indsættes fra den oprindelige registreringsanmodning for den mulige kreditor. Den indeholder også kontaktpersonens telefonnummer og e-mailadresse og kontaktpersonens adresser til forskellige formål. |
| Firmaoplysninger       | Denne side indeholder momsregistreringsnumre (for forskellige lande eller områder) og antallet af medarbejdere. Siden angiver også, om virksomheden er minoritetsejet. |
| Indkøbskategorier     | Denne side indeholder de indkøbskategorier, som kreditoren anmoder om godkendelse for. Brugeren kan vælge kategorier i indkøbskategorihierarkiet. Du kan konfigurere antallet af niveauer, der vises i hierarkiet, i **Indkøbs- og forsyningsparametre** &gt; **Kreditorsamarbejde** under **Indkøb og forsyning** &gt; **Opsætning**. |
| Spørgeskemaer             | Guiden kan indeholde et sæt spørgeskemaer for kreditoren. Spørgeskemaer, der vises i guiden, konfigureres i kreditoranmodningen eller pr. indkøbskategori. Hvis spørgeskemaer konfigureres pr. indkøbskategori, bestemmer de indkøbskategorier, som kreditoren anmoder om godkendelse af, hvilke spørgeskemaer der vises i guiden. På siden **Indkøbskategorier** kan du tilføje et spørgeskema under den relevante kategori og indstille aktivitetstypen til **Modtagelse af kreditorer**. |

Når den mulige kreditorbruger fuldfører kreditorregistreringsguiden, oprettes der en kreditoranmodning.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Sende en kreditoranmodning manuelt eller automatisk

En kreditoranmodning kan oprettes som en kladde og sendes manuelt til en arbejdsgang. Kreditoranmodningen kan også automatisk sendes til en arbejdsgang, når kreditorregistreringsguiden er fuldført. En anmodning kan sendes manuelt, hvis, f.eks. en anmoder ønsker at vurdere, om anmodningen skal dirigeres gennem en godkendelsesproces, før den sendes til arbejdsgangen.

- Vælg **Indkøbs- og forsyningsparametre** &gt; **Kreditorsamarbejde**, og vælg derefter **Send automatisk registrering af mulig kreditor til arbejdsgang** for at konfigurere kreditoranmodningen, så den sendes automatisk til en arbejdsgang, når kreditorregistreringsguiden er fuldført.

## <a name="vendor-requests"></a>Kreditoranmodninger

Kreditoranmodninger er tilgængelige på siden **Brugeranmodninger om kreditorsamarbejde**.

En kreditoranmodning indeholder de oplysninger, som den mulige kreditorbruger har angivet i kreditorregistreringsguiden.

I anmodningen kan du gennemse kreditoroplysningerne og afgøre, om kreditoren skal gøres til registreret kreditor i Finance and Operations.

Kreditoranmodningen skal sendes til en arbejdsgang, og den skal sendes til de relevante korrekturlæsere og godkendere. Du kan finde grundlæggende oplysninger om, hvordan du kan konfigurere arbejdsgange i [Indkøbs- og forsyningsarbejdsgange](procurement-sourcing-workflows.md).

Følgende tabel viser de statusser, som kreditoranmodninger kan have.

| Status                     | Betegnelse |
|----------------------------|-------------|
| Udkast                      | Kreditoranmodningen er ikke endnu blevet afsendt. |
| Anmodningen er sendt          | Kreditoranmodningen er sendt, og det første trin i arbejdsgangen behandles. |
| Afventer gennemsyn             | Hvis der er flere korrekturlæsere i en arbejdsgangsopgave, kan en korrekturlæser acceptere opgaven med at gennemse kreditoranmodningen og derefter fuldføre gennemgangen. Hvis der kun er en enkelt korrekturlæser, kan denne deltager fuldføre gennemgangen af ved at vælge **Fuldført** i arbejdsproceshandlingen. Han eller hun behøver ikke at acceptere workflowopgaven først. |
| Anmodning afventer godkendelse   | Kreditoranmodningen er blevet sendt til deltagerne til godkendelse, og det er muligt at anmode om yderligere oplysninger. En anmodning om supplerende oplysninger medfører, at workflowopgaven bliver dirigeret tilbage til afsenderen. Kreditoranmodningen kan også godkendes eller afvises, mens den har denne status. |
| Anmodning om ændring af ansøgning | Der er anmodet om yderligere oplysninger af godkenderen, og kreditoranmodningen er blevet sendt til den person, der sendte kreditoranmodningen. Denne person kan tilføje de oplysninger, der anmodes om, og derefter sende kreditoranmodningen igen. Hvis en kreditoranmodning sendes igen, ændres status tilbage til status **Anmodning afventer godkendelse**. |
| Anmodningen er godkendt           | Denne status er en sluttilstand. |
| Anmodning afvist           | Denne status er en sluttilstand. |

## <a name="approving-a-vendor-request"></a>Godkendelse af en kreditoranmodning

Når en kreditoranmodning er godkendt, oprettes der en kreditorkonto, og status **Godkendt** vises på den oprindelige registreringsanmodning om mulig kreditor og kreditoranmodningen.

Før du godkender en kreditoranmodning skal du på siden **Ny kreditor** i oversigtspanelet **Generelt** vælge **Kreditorgruppe** for at vælge en kreditorgruppe.

Hvis den mulige kreditorbruger skal have adgang til Finance and Operations som en kreditorsamarbejdsbruger, der repræsenterer kreditoren, skal du indstille adgangsrettigheder for kreditorsamarbejde til **Ja**. Hvis du vil deaktivere den brugerkonto, som den mulige kreditor brugte til at blive registreret, skal du indstille denne rettighed til **Nej**.

Hvis adgangstilladelsen for kreditorsamarbejdet er indstillet til **Ja**, sendes der en anmodning om at redigere brugerens roller, så brugeren har de roller, der er defineret for typen **Kreditor** i **Eksterne roller**, når kreditoranmodningen er godkendt. Hvis denne rettighed er indstillet til **Nej**, når kreditoranmodningen er godkendt, sendes der en anmodning til den inaktive bruger. I så fald skal arbejdsgangen om at deaktivere en brugeranmodning konfigureres.

Hvis en kreditorkonto skal oprettes, når kreditoranmodningen er godkendt, skal nummerserien for oprettelse af kreditorer fra kreditoranmodninger indstilles til **Automatisk**.

En oversigt over adgangsrettighederne for en kreditorsamarbejdsbruger finder du i [Konfigurere og vedligeholde kreditorsamarbejde](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Afvisning af en leverandøranmodning

Hvis en kreditoranmodning afvises, skal der vælges en årsag til afvisningen i kreditoranmodningen.

Når en kreditoranmodning afvises, sendes der en anmodning om at inaktivere brugeren. I så fald skal arbejdsgangen om at deaktivere en brugeranmodning konfigureres. Du kan finde flere oplysninger under [Konfigurere og vedligeholde kreditorsamarbejde](set-up-maintain-vendor-collaboration.md).

Når en kreditoranmodning er afvist, vises status **Afvist** vises på den oprindelige registreringsanmodning om mulig kreditor og kreditoranmodningen.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Sletning af en anmodning om registrering af mulig kreditor i forskellige statusser

De forskellige statusser for en anmodning om registrering af mulig kreditor giver et overblik over anmodningens status.

Ved hjælp af handlingen **Slet** i anmodningen om registrering af mulig kreditor, du kan slette i og fjerne kæden af poster, der er oprettet, og du kan deaktivere brugerkontoen. Resultatet af handlingen **Slet** varierer, afhængigt af status for registreringsanmodningen for mulig kreditor som vist i følgende tabel.

| Status                   | Statusbeskrivelse | Resultat af handlingen Slet |
|--------------------------|--------------------|-----------------------------------|
| Nyt                      | Der er ikke udført nogen handlinger på anmodningen. | Anmodningen om registrering af mulig kreditor er slettet. |
| Anmodet bruger           | Når du vælger **Inviter bruger**, ændres status til **Anmodet bruger**, og en anmodning om en mulig bruger oprettes og sendes til en brugeranmodningsarbejdsgang. | Du kan ikke slette en anmodning om registrering af mulig kreditor, der har denne status, fordi brugeranmodningsarbejdsgangen ikke endnu er afsluttet. |
| Inviteret bruger             | Brugeranmodningsarbejdsgangen er godkendt, og brugeren er oprettet. | Der oprettes en anmodning om at deaktivere brugeren, og anmodningen om registrering af mulig kreditor slettes. |
| Registrering er i gang | Den nye bruger har logget på og har startet kreditorregistreringsguiden. | Der oprettes en anmodning om at deaktivere brugeren, og anmodningen om registrering af mulig kreditor og de data, der blev angivet i kreditorregistreringsguiden, slettes. |
| Oprettet kreditoranmodning   | Kreditorregistreringsguiden er fuldført. | Der oprettes en anmodning om at deaktivere brugeren, og anmodningen om registrering af mulig kreditor, de data, der blev angivet i kreditorregistreringsguiden, og kreditoranmodningen slettes.<blockquote>[!NOTE]<br>Du kan ikke bruge handlingen **Slet**, når kreditoranmodningen er i en evalueringsproces i arbejdsgangen.</blockquote> |
| Godkendt                 | Kreditoranmodningen er godkendt. | Anmodningen om registrering af mulig kreditor, de data, der blev angivet i kreditorregistreringsguiden, og kreditoranmodningen slettes. |
| Afvist                 | Kreditoranmodningen slettes. | Anmodningen om registrering af mulig kreditor, de data, der blev angivet i kreditorregistreringsguiden, og kreditoranmodningen slettes. |

