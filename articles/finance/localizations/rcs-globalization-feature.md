---
title: Regulatory Configuration Service (RCS) – globaliseringsfunktioner
description: Denne artikel forklarer, hvordan du bruger Microsoft Regulatory Configuration Services (RCS) og det globale lager for at oprette og bruge globaliseringsfunktioner.
author: JaneA07
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 4981d72d76d6f865b919e90994a0ce1b0bcba494
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066101"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Service (RCS) – globaliseringsfunktioner

[!include [banner](../includes/banner.md)]

Du kan bruge RCS (Microsoft Regulatory Configuration Services) til at oprette en globaliseringsfunktion, der kan bruges i globaliseringstjenester, f.eks. en e-faktureringstjeneste. RCS giver dig mulighed for at udføre disse opgaver:

- Definere relaterede komponenter i en funktion.
- Administrere funktionens livscyklus via en funktionsstatus.
- Gøre en funktion tilgængelig for definerede miljøer.
- Dele en funktion med andre organisationer.

I de følgende procedurer forklares det, hvordan en bruger i RCS kan tilføje en globaliseringsfunktion og relaterede komponenter, opdatere funktionens status og gøre funktionen tilgængelig, så den kan bruges i globaliseringstjenester.

Før du fuldfører procedurerne, skal du udføre de trin, der er knyttet til følgende opgaver:

- Adgang til en RCS-forekomst.
- Oprettelse og aktivering af en konfigurationsudbyder. Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Følg disse trin i din forekomst af programmer til finans og drift.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Hvis der ikke er klargjort noget RCS-miljø til dit firma, skal du vælge **Regulatory services – Konfiguration** og derefter følge vejledningen for at klargøre et miljø.

> [!NOTE]
> Hvis der allerede er klargjort et RCS-miljø til dit firma, kan du bruge siden med URL-adresser til at få adgang til miljøet ved at vælge indstillingen til logon.

## <a name="turn-on-the-globalization-features"></a>Slå globaliseringsfunktionerne til

1. I RCS-forekomsten skal du vælge feltet **Funktionsstyring**.
2. I området **Funktionsstyring** skal du vælge **Globaliseringsfunktioner** på listen og derefter **Aktivér nu**.

    ![Globaliseringsfunktioner i funktionsstyring.](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Globaliseringsfunktioner

Hvis du vil bruge en globaliseringsfunktion, skal du importere den fra det globale lager og oprette din egen version af den. Du kan tilføje globaliseringsfunktioner på to måder:

- Tilføj en afledt funktion, som er baseret på en eksisterende funktion, der er publiceret eller delt.
- Tilføj en ny funktion, som du har oprettet fra bunden.

## <a name="access-globalization-features"></a>Tilgå globaliseringsfunktioner

1. Sørg for, at funktionen **Globaliseringsfunktioner** er aktiveret i funktionsstyring, som beskrevet tidligere i denne artikel.
2. Åbn det nye arbejdsområde **Globaliseringsfunktioner**, og under **Funktioner** skal du vælge feltet **e-fakturering**.

    ![Arbejdsområde til globale funktioner.](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    Siden **e-faktureringsfunktioner** åbnes.

    ![Side med e-faktureringsfunktioner.](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Tilføje en afledt globaliseringsfunktion

Du kan tilføje en ny globaliseringsfunktion ved at aflede den fra en eksisterende funktion, der er publiceret eller delt.

1. Vælg **Importér** for at åbne siden **Importér funktion fra globalt lager**.

    ![Siden Importér funktion fra globalt lager.](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Vælg **Synkroniser** for at hente de nyeste funktioner.

    Den synkroniserede liste indeholder funktioner, som enten er tilgængelige, fordi de blev publiceret af Microsoft, eller fordi de blev delt med dig af en anden konfigurationsudbyder.

    ![Synkroniseret liste over funktioner.](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. Vælg de funktioner, der skal importeres, på listen, og vælg derefter **Importér**. Du modtager en meddelelse, når de valgte funktioner er blevet importeret.

    ![Meddelelse om vellykket import.](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Vælg **Tilføj**, og derefter skal du i rulledialogboksen vælge indstillingen **Baseret på eksisterende version**.
5. Angiv et navn til og en beskrivelse af funktionen.
6. Vælg funktionens basisversion på listen over tilgængelige funktioner og derefter **Opret funktion**.

    ![Tilføje en afledt funktion.](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Den funktion, du har tilføjet, er oprettet og har statussen **Kladde**.

    ![Afledt funktion med kladdestatus.](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Gennemse funktionskomponenterne for at finde ud af, om der kræves opdateringer:

    - Gennemse konfigurationerne, hvis du skal tilpasse ER-formaterne (Electronic Reporting) og deres binding med formattilknytninger til funktionsversionen.
    - Gennemse opsætningen, hvis du har brug for at tilpasse fanen **Handlinger**, fanen **Anvendelighedsregler** eller fanen **Variabler** for funktionsversionen.

8. På fanen **Versioner** skal du vælge en **Ikrafttrædelsesdato** og angive en beskrivelse, hvis feltet **Beskrivelse** er tomt.
9. Vælg **Skift status** for at fuldføre funktionen. Fuldførte funktioner kan gøres tilgængelige for et bestemt miljø, så de kan bruges i globaliseringstjenester, eller de kan publiceres til det globale lager.

> [!NOTE]
> Funktioner, der har en **Funktionsversionsstatus**-værdi for **Publiceret**, kan deles med eksterne organisationer.

## <a name="add-a-new-globalization-feature"></a>Tilføje en ny globaliseringsfunktion

Du kan tilføje en ny globaliserings funktion ved at oprette den fra bunden.

1. På siden **Importér funktion fra globalt lager** skal du vælge **Tilføj** og derefter i rulledialogboksen vælge indstillingen **Ny funktion**.
2. Angiv et navn til og en beskrivelse af funktionen.
3. Vælg **Opret funktion**.

    ![Tilføje en ny funktion.](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. På fanen **Versioner** skal du vælge en **Ikrafttrædelsesdato** og derefter **Skift status** for at fuldføre funktionen. Fuldførte funktioner kan gøres tilgængelige for et bestemt miljø, så de kan bruges i globaliseringstjenester, eller de kan publiceres til det globale lager.

> [!NOTE]
> Funktioner, der har en **Funktionsversionsstatus**-værdi for **Publiceret**, kan deles med eksterne organisationer.

## <a name="feature-component-overview"></a>Oversigt over funktionskomponenter

Globaliseringsfunktioner har flere forskellige komponenter:

- **Version** – Denne komponent understøtter styring af funktionens livscyklus og giver brugerne mulighed for at styre status for forskellige versioner af funktionen.
- **Konfigurationer** – Denne komponent giver brugerne mulighed for at administrere, få vist og redigere relaterede ER-formater og formattilknytninger.
- **Opsætninger** – Denne komponent giver brugerne af globaliseringstjenester, f.eks. en e-faktureringstjeneste, mulighed for at administrere opsætningen af den relaterede funktionsversion. Den understøtter derfor den fleksible konstruktion af kommunikations- og svarregler.
- **Miljø** – Denne komponent giver brugerne af globaliseringstjenester, f.eks. en e-faktureringstjeneste, mulighed for at administrere det miljø, hvor opsætningen af funktionsversionen bruges, og give tilladelse til de brugere, der skal have adgang til miljøet.
- **Organisationer** – Denne komponent giver brugerne mulighed for at dele funktionen med eksterne organisationer.

## <a name="configuring-feature-components"></a>Konfigurere funktionskomponenter

### <a name="version-and-status"></a>Version og status

Versionen bruges til at administrere globaliseringsfunktionens livscyklus.

Status kan ændres i feltet **Status** på fanen **Version**. Følgende statusser er tilgængelige:

- **Kladde** – Funktionen kan kun redigeres, når den er i denne status.
- **Fuldført** – Funktionen og alle relaterede komponenter er blevet færdiggjort (fuldført) og kan ikke redigeres.
- **Publiceret** – Funktionen og alle relaterede komponenter er blevet publiceret til det globale lager.
- **Delt** – Funktionen og alle relaterede komponenter er blevet delt med eksterne organisationer.
- **Aktiveret** – Funktionen og alle relaterede komponenter er aktiveret til brug i en globaliseringstjeneste, f.eks. en e-faktureringstjeneste.

> [!NOTE]
> Funktioner skal flyttes sekventielt gennem nogle af disse statusser. Derfor er det ikke alle statusser, der kan være tilgængelige i alle livscyklusser.

### <a name="configurations"></a>Varianter

De følgende handligner er tilgængelige for konfigurationer:

- **Vis** – Få vist de underliggende funktionskonfigurationer, der ikke kræver opdatering.
- **Rediger** – Opretfe en kladdeversion af en valgt konfiguration, så du kan redigere formatet eller formattilknytningen i formatdesigneren.
- **Slet** – Slette en valgt konfiguration fra funktionen.
- **Rebasér** – Rebasere funktionen. Du kan finde flere oplysninger i afsnittet [Rebasér delte globaliseringsfunktioner](#rebase) nedenfor i denne artikel.

### <a name="setups"></a>Konfigurationer

Følgende handlinger er tilgængelige for funkionsopsætninger:

- **Tilføj** – Oprette en ny funktionsopsætning. Denne funktionsopsætning kan afledes fra en eksisterende funktionsopsætning eller oprettes fra bunden.
- **Slet** – Slette en valgt funktionsopsætning.
- **Vis** – Få vist en underliggende funktionsopsætning, der ikke kræver nogen ændringer.
- **Rediger** – Oprette, slette eller redigere attributterne for de tre hovedkomponenter i en funktionsopsætning:

    - Handlinger og deres parametre
    - Anvendelighedsregler
    - Variabler

![Siden Opsætning af funktionsversion.](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Miljøer

De følgende handlinger er tilgængelige for miljøer:

- **Aktivér** – For en valgt funktionsversion skal du vælge et publiceret miljø og vælge en **Ikrafttrædelsesdato**, når den skal være tilgængelig. Du kan finde flere oplysninger i afsnittet [Konfigurer miljøer til aktivering](#configureenvironment) nedenfor i denne artikel.
- **Annuller** – Fjerne et miljø for en funktionsopsætning.

### <a name="organizations"></a>Organisationer

Udfør følgende trin for at dele en globaliseringsfunktion med en ekstern organisation.

1. På siden **e-faktureringsfunktioner** skal du vælge den funktion og den funktionsversion, du vil dele.
2. På fanen **Organisationer** skal du vælge **Del med** og derefter i rulledialogboksen angive organisationens domænenavn.
3. Vælg **Del**.

    ![Deling af en funktion med en organisation.](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Funktionen deles med den valgte organisation og er tilgængelig for denne organisation i det globale lager. Derfra kan funktionen importeres til organisationens forekomst af RCS eller Dynamics 365 Finance, så den kan bruges.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Rebasér afledte globaliseringsfunktioner

Du kan rebasere en afledt globaliseringsfunktion til den nye eller opdaterede basisfunktionsversion. På denne måde kan ændringer, der er foretaget i basisversionen, opdateres automatisk. Den opdaterede basisfunktionsversion oprettes af den oprindelige konfigurationsudbyder, og den publiceres eller deles derefter.

![Opdateret version af basisfunktion.](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Hvis du f eks. vil rebasere den afledte version af en funktion, du har oprettet, skal du først hente den seneste version af funktionen ved at importere den fra det globale lager.

1. På siden **e-faktureringsfunktioner** skal du vælge **Importér**.
2. Vælg **Synkroniser** for at hente de nyeste funktioner.
3. På listen over funktioner skal du vælge de funktioner, der skal importeres, og derefter **Importér**.

    ![Import af den seneste version af en funktion.](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. Vælg den funktion, der skal rebaseres, på listen over funktioner.
5. På fanen **Version** skal du vælge **Ny** for at oprette en kladdeversion.

    ![Ny kladdeversion oprettet.](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Vælg **Rebaśer**.
7. I dialogboksen **Rebasér** skal du vælge den seneste version af funktionen, der skal rebaseres til.

    ![Dialogboksen Rebasér.](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Vælg **OK**.
9. Gennemgå funktionskomponenterne, og foretag eventuelle nødvendige ændringer.
10. Vælg **Skift status** for at fuldføre den rebaserede funktion. Når rebaseringen er fuldført, kan du udføre yderligere handlinger. Du kan f.eks. publicere funktionen og gøre den tilgængelig for brug i globaliseringstjenester.

    ![Funktionsstatus er opdateret til Fuldført.](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Konfigurere miljøer til globaliseringsfunktioner

Brugere af globaliseringstjenester kan administrere miljøet for at konfigurere en globaliseringsfunktion og give godkendelse til andre brugere, der skal have adgang til den.

1. I arbejdsområdet **Globaliseringsfunktioner** under **Miljøer** skal du vælge feltet **e-fakturering**.

    ![Arbejdsområdet for globale funktioner.](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Vælg **Parametre for Key Vault** og derefter **Ny** for at oprette en Azure Key Vault-hemmelighed.
3. Angiv et navn til og en beskrivelse af Key Vault, og angiv derefter i feltet **Key Vault URI** den URL-adresse, der identificerer Key Vault-ressourcen i Azure.
4. I oversigtspanelet **Certifikater** skal du vælge **Tilføj** for at tilføje certifikatet og angive et navn til og en beskrivelse af hvert certifikat.

    ![Certifikat tilføjet.](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Vælg **Ny** for at oprette et nyt miljø.
6. Angiv et navn, en beskrivelse og det hemmelige token for signaturer til delt adgang, der er nødvendigt til lagring.
7. I oversigtspanelet **Brugere** skal du vælge **Ny** for at tilføje en bruger, der ønsker tilladelse til at få adgang til dette miljø.
8. Angiv brugerens bruger-id og e-mailadresse.
9. Gentag trin 7 og 8 for at tilføje flere brugere.
10. Vælg **Publicer** for at publicere miljøet.

    ![Publiceret miljø.](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
