---
title: Administrere fradrag i fradragspanelet
description: Dette emne beskriver, hvordan du bruger fradragspanelet til at behandle kundebetalinger, der omfatter fradrag.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 04d7c1de85978f7915246fd835a0866cefb6de310bba240ebcadc57089e10521
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735105"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Administrere fradrag i fradragspanelet

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Dette emne beskriver, hvordan du bruger fradragspanelet til at behandle kundebetalinger, der omfatter fradrag.

En kunde, der skyldes en rabat, kan beslutte ikke at vente på at få en rabatudbetaling. I stedet kan kunden sende en betaling, der omfatter et fradrag for rabatbeløbet. For at håndtere denne type transaktion kan du bruge fradragspanelet til at matche fradrag med åbne kreditposteringer, opdele fradrag, nægte fradrag og afskrive fradrag.

> [!NOTE]
> Fradragspanelet har længe været en del af salgs- og marketingfunktionen i Microsoft Dynamics 365 Supply Chain Management. Det er nu blevet udvidet, så det også fungerer med det nyere modul **Rabatstyring**. Dette emne beskriver, hvordan du kan bruge både de ældre funktioner og funktioner til rabatstyring i fradragspanelet. Men hvis du ikke har [aktiveret modulet **Rabatstyring** for systemet](rebate-management-enable.md), vil nogle af de funktioner, der er beskrevet her, ikke være tilgængelige for dig.

## <a name="prerequisites"></a>Forudsætninger

### <a name="set-up-the-old-deduction-management-system"></a>Konfigurere det gamle fradragsstyringssystem

Du kan bruge fradragspanelet sammen med de gamle fradragsfunktioner i Supply Chain Management, selvom du ikke bruger modulet **Rabatstyring**. Du skal dog først forberede systemet, som det beskrives i dette afsnit.

Før du kan bruge fradragspanelet, skal du fuldføre de opsætningsopgaver, der er beskrevet i [Konfigurere fradragsstyring](/dynamicsax-2012/appuser-itpro/set-up-deduction-management). Du bør også have en anden type rabataftale, der er konfigureret for kunden: enten en kunderabat, som beskrevet i [Konfigurere og vedligeholde debitorrabatter](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates), eller en handelsrabat.

Hvis du anvender et fradrag på en debitorrabat, skal du udføre disse opgaver:

- [Konfigurer debitorrabatter](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- Godkend og foretag behandling af rabatten, så du kan bruge fradragspanelet.

Hvis du anvender et fradrag på en handelsrabat, skal du udføre disse opgaver:

- Konfigurer tilbagefaktureringsrabatter.
- Anvend tilbagefaktureringsrabatter.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Konfigurere debitorer og fradrag

Systemet registrerer alle fradragshændelser i en kravskladde. Systemet skal derfor inkludere en kladde, der kan bruges til dette formål. Hvis du ikke allerede har en kravskladde, skal den konfigureres nu. Denne kladde skal oprette fradrag direkte på fradragspanelet, debitorudligninger eller debitorsiden.

Når du vil konfigurere en ny kravskladde il fradrag, skal du gøre følgende.

1. Gå til **Finans \> Kladdeopsætning \> Kladdenavne**.
1. Vælg **Ny**, og angiv følgende felter for det nye kladdenavn:

    - **Navn** – Angiv et entydigt navn til kravskladden.
    - **Beskrivelse** – Angiv en kort beskrivelse af den nye kladde.
    - **Kladdetype** – Vælg *Daglig*.
    - **Bilagsserie** – Tildel en eksisterende nummerserie. Du kan også oprette en ny nummerserie af firmaomfang og knytte den til det nye kladdenavn.

1. Gå til **Debitor \> Opsætning \> Debitorparametre**.
1. Under fanen **Fradrag** skal du i oversigtspanelet **Generelt** angive feltet **Kravkladdenavn** til det kladdenavn, du netop har oprettet.
1. I oversigtspanelet **Returordre** skal du angive følgende felter:

    - **Opret returordre** – Angiv denne indstilling for at angive, hvad systemet skal gøre, når et antalsbaseret krav godkendes:

        - *Ja* – Opret en returordre.
        - *Nej* – Opret en negativ salgsordre.

    - **Oprettelse uden tilknyttet faktura** – Vælg en værdi for at angive, hvad systemet skal gøre, når et antalsbaseret krav godkendes, men der ikke tilknyttes en faktura:

        - *Accepter* – Opret en returordre.
        - *Advarsel* – Opret en returordre, men vis følgende advarsel: "Krav er ikke knyttet til en faktura".
        - *Fejl* – Opret ikke en returordre, og vis følgende fejlmeddelelse: "Krav er ikke knyttet til en faktura. Opdateringen er annulleret".

    - **Opret returordre før fradragsgodkendelse** – Angiv denne indstilling til *Ja*, hvis der kan oprettes returordrer, før kravet godkendes. Denne indstilling gælder kun for antalsbaserede krav, hvor indstillingen **Opret returordre** er angivet til *Ja*.

### <a name="configure-general-ledger-parameters"></a>Konfigurere finansparametre

Når systemet opretter en kravkladde til et nyt fradrag, oprettes der også to nye debitorposteringer: en til modregning af kravbeløbet mod den oprindelige faktura og en til registrering af en debitors gæld på kravbeløbet (fordi kravet endnu ikke er godkendt). Du skal derfor konfigurere systemet, så et enkelt bilag kan have flere debitorlinjer.

Hvis du vil aktivere et enkelt bilag, så der er flere debitorlinjer, skal du følge disse trin.

1. Gå til **Finans \> Opsætning Finans \> Finansparametre**.
1. Under fanen **Finans** i oversigtspanelet **Generelt** skal du angive Indstillingen **Tillad flere transaktioner i ét bilag** til *Ja*.
1. Hvis du modtager en advarsel, skal du vælge **Luk** for at acceptere ændringen.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Oprette fradragsårsager

Systemet kræver, at brugere angiver en årsag til hvert fradrag, som de angiver direkte på fradragspanelet, debitorudligningen eller debitorsiden. Årsagen bestemmer, hvordan fradraget håndteres, når det godkendes.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragsårsager**.
1. Vælg **Ny** for at tilføje en række i gitteret, og angiv derefter følgende felter for den:

    - **Kravsårsag** – Angiv et entydigt navn til kravsårsagen.
    - **Beskrivelse** – Angiv en beskrivelse af årsagen for at give flere oplysninger om, hvordan den skal bruges.
    - **Kravgrundlag** – Vælg et kravgrundlag for årsagen til kravet:

        - *Prisbaseret* – Opret en fritekstkredit ved godkendelse.
        - *Antalsbaseret* – Opret en negativ salgsordre eller returordre ved godkendelse.

    - **Årsagskode for returnering** – Vælg en årsagskode for returnering, der skal anvendes som **Returårsagskode**-værdi for returordren.
    - **Type** – Vælg en fradragstype. Værdien af **Modregning af fradrag** for den valgte type bruges til at angive feltet **Modregning af fradrag**, når der oprettes et fradrag eller krav. Fradragstyper defineres på siden **Fradragstyper** (**Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragstyper**).
    - **Kravsbogføringskonto** – Dette felt er kun tilgængeligt, når feltet **Kravgrundlag** er angivet til *Prisbaseret*. Når et prisbaseret krav godkendes, tildeler systemet det den finanskonto, du vælger her, som **Hovedkonto**-værdi for kladden til fritekstkreditnotaen.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>Konfigurere den periodiske opgave til udligning af godkendte fradrag

For fradrag, der oprettes med kommandoen **Nyt fradrag** på fradragspanelet, debitorudligning eller debitorsiden, kan du konfigurere den periodiske opgave *Udlign godkendte fradrag*, så du automatisk kan sammenholde fradrag og kreditter, der har matchende værdier og beløb for **Fradrags-id**.

Du kan planlægge denne opgave ved at gå til **Salg og marketing \> Periodiske opgaver \> Udlign godkendte fradrag** og konfigurere indstillinger, filtre og en plan på samme måde som andre typer periodiske opgaver.

> [!NOTE]
> Hvis indstillingen **Automatisk udligning** er angivet til *Ja* under fanen **Udligning** på siden **Debitorparametre** (**Debitor \> Konfiguration \> Debitorparametre**), gør den periodiske opgave *Udlign godkendte fradrag* ikke noget, da kreditten automatisk udlignes.

## <a name="create-a-deduction"></a>Oprette et fradrag

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Oprette en fradragskladdepost ved hjælp af debitorbetalingskladden

Følg disse trin for at oprette en fradragskladdepost.

1. Gå til **Debitor \> Betalinger \> Debitorbetalingskladde**.
1. Vælg **Ny** for at føje en række til gitteret.
1. Vælg navnet på kladden i feltet **Navn** for den nye række.
1. Vælg **Linjer** i handlingsruden.
1. Angiv datoen, firmakontoen og kundens kontonummer.
1. Vælg den faktura, som fradraget er knyttet til, i feltet **Faktura**.
1. Angiv det beløb, som kunden betalte, i feltet **Kredit**.
1. Vælg **OK** at bekræfte, at beløbet er mindre end det samlede beløb af den markerede transaktion.
1. Vælg typen af modkonto og modkontoen.
1. Vælg **Fradrag** på værktøjslinjen over gitteret.
1. Vælg **Ny** på siden **Fradrag** i handlingsruden for at føje en række til gitteret. Feltet **Fradrags-id** for den nye række angives automatisk.
1. Vælg fradragstypen i feltet **Type**.
1. I feltet **Beløb** skal du angive det beløb, der vises i feltet **Saldo** under fradragslisten. Dette beløb repræsenterer det beløb, kunden har fratrukket betalingen.
1. Luk siden **Fradrag**. Du vender tilbage til siden **Debitorbetalinger**, der nu viser en ny linje for fradraget.
1. Vælg **Valider \> Valider** i handlingsruden. Du modtager følgende meddelelse: "Kladde er OK".
1. Vælg **Bogfør** i handlingsruden.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Oprette et fradrag i fradragspanelet

Følg disse trin for at oprette et nyt fradrag i fradragspanelet.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Vælg **Vedligehold \> Nyt fradrag** i handlingsruden.

    I dialogboksen **Nyt fradrag** er feltet **Fradrags-id** baseret på nummerserien for **Fradrags-id**, der er defineret på siden **Parametre til administration af handelsrabat** (**Salg og market \> Konfiguration \> Handelsrabatter \> Parametre til administration af handelsrabat**).

1. Angiv følgende felter:

    - **Debitorkonto** – Vælg den debitorkonto, som fradraget gælder for.
    - **Eksternt kravnummer** – Angiv kundens kravreference.
    - **Kravsbeløb** – Angiv et kravsbeløb inklusive moms. Værdien skal være positiv.
    - **Valuta** – Vælg valutaen for fradraget. Standardværdien er den valuta, der er angivet for den valgte debitorkonto.
    - **Kravgrundlag** – Vælg kravgrundlaget. Kravgrundlaget er bestemmende for den type kreditpostering, der oprettes, efter at fradraget eller kravet er godkendt.

        - *Prisbaseret* – Der oprettes en kladde til fritekstfaktura.
        - *Antalsbaseret* – Der oprettes en negativ salgsordre eller returordre.

    - **Kravsdato** – Vælg datoen for kravet. Standardværdien er dags dato.
    - **Kravårsag** – Vælg den årsagskode, der gælder for det aktuelle fradrag. Det valgte kravgrundlag påvirker de gældende indstillinger. Du kan finde flere oplysninger om, hvordan du opretter og konfigurerer de kravårsager, der kan vælges her, i afsnittet [Oprette fradragsårsager](#deduction-reasons) tidligere i dette emne.
    - **Noter** – Tilføj eventuelle relevante noter. Når kravet er godkendt, kan godkenderen redigere eller føje det til kravets noter.
    - **Opret kravkladde** – Angiv denne indstilling for at angive, om kravkladden skal oprettes, når kravet eller fradraget oprettes:

        - *Ja* – Systemet opretter og bogfører en finanskladde ved hjælp af den kravkladde, der er oprettet på siden **Debitorparametre**. (Du kan finde flere oplysninger i [Konfigurere debitorer og fradrag](#accounts-receivable-deductions) tidligere i dette emne). Når der er knyttet en faktura til kravet, bruges kravkladden til at reducere saldoen på den gældende faktura. Hvis kravet senere afvises, tilbageføres kravskladden og udligningerne (hvis der er vedhæftet en faktura).
        - *Nej* – Der oprettes ingen kravkladde på dette tidspunkt. Den oprettes, når kravet godkendes. Der kan stadig knyttes en faktura til det nye krav, selvom der ikke er oprettet en kravkladde. Udligning kan dog ikke foretages uden kravkladden.

1. Vælg **OK**.

    Der oprettes et nyt fradrag. Hvis du angiver indstillingen **Opret kravskladde** til *Ja*, bogføres følgende transaktioner:

    - **To nye debitorposteringer** – Én transaktion modregner kravsbeløbet på den oprindelige faktura. Den anden transaktion registrerer en kundes gæld på kravbeløbet, fordi kravet endnu ikke er godkendt. Den oprindelige fakturapostering og modposteringen af kravet markeres automatisk til udligning, når du tilknytter fakturaen ved at vælge **Vedligehold \> Tilknyt faktura** i handlingsruden.
    - **To modposteringer** – Disse posteringer bogføres på finanskontoen **Modregning af fradrag**.
    - **Kravskladde** – Hvis du vil have vist kravskladden for hvert fradrag, der er vist i fradragspanelet, skal du vælge fanen **Referencer**. Kravskladden vises i feltet **Kladdebatchnummer**. Du kan også få vist kravskladden under fanen **Fradragshændelser**. Der vil den have **Opdateringstype**-værdien *Match*.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Oprette et fradrag ud fra en debitorudligning

Processen til oprettelse af et fradrag ud fra en debitorudligning ligner processen til oprettelse af et fradrag via fradragspanelet. Debitor- og fakturavalutaen angives dog automatisk, og fakturaen tilknyttes. Du behøver ikke at vælge **Vedligehold \> Tilknyt faktura** i handlingsruden, når du opretter et krav eller fradrag via debitorens udligningsside.

1. Gå til **Debitorer \> Kunder \> Alle kunder**.
1. Vælg den debitor, der skal oprettes et fradrag for.
1. I handlingsruden på fanen **Indsaml**, i gruppen **Udlign** skal du vælge **Udlign transaktioner**.
1. Vælg den faktura, fradraget skal oprettes mod, under fanen **Oversigt** i dialogboksen **Indstilling af posteringer**.
1. Vælg **Fradrag \> Nyt fradrag** på værktøjslinjen.

    I dialogboksen **Nyt fradrag** er feltet **Fradrags-id** baseret på nummerserien for **Fradrags-id**, der er defineret på siden **Parametre til administration af handelsrabat** (**Salg og market \> Konfiguration \> Handelsrabatter \> Parametre til administration af handelsrabat**). Feltet **Debitorkonto** er angivet til den debitorkonto, som fradraget gælder for.

1. Angiv følgende felter:

    - **Eksternt kravnummer** – Angiv kundens kravreference.
    - **Kravsbeløb** – Angiv et kravsbeløb inklusive moms. Værdien skal være positiv.
    - **Valuta** – Vælg valutaen for fradraget. Standardværdien er den valuta, der er angivet for den valgte debitorkonto.
    - **Kravgrundlag** – Vælg kravgrundlaget. Kravgrundlaget er bestemmende for den type kreditpostering, der oprettes, efter at fradraget eller kravet er godkendt.

        - *Prisbaseret* – Der oprettes en kladde til fritekstfaktura.
        - *Antalsbaseret* – Der oprettes en negativ salgsordre eller returordre.

    - **Kravsdato** – Vælg datoen for kravet. Standardværdien er dags dato.
    - **Kravårsag** – Vælg den årsagskode, der gælder for det aktuelle fradrag. Det valgte kravgrundlag påvirker de gældende indstillinger. Du kan finde flere oplysninger om, hvordan du opretter og konfigurerer de kravårsager, der kan vælges her, i afsnittet [Oprette fradragsårsager](#deduction-reasons) tidligere i dette emne.
    - **Noter** – Tilføj eventuelle relevante noter. Når kravet er godkendt, kan godkenderen redigere eller føje det til kravets noter.
    - **Opret kravkladde** – Angiv denne indstilling for at angive, om kravkladden skal oprettes, når kravet eller fradraget oprettes:

        - *Ja* – Systemet opretter og bogfører en finanskladde ved hjælp af den kravkladde, der er oprettet på siden **Debitorparametre**. (Du kan finde flere oplysninger i [Konfigurere debitorer og fradrag](#accounts-receivable-deductions) tidligere i dette emne). Når der er knyttet en faktura til kravet, bruges kravkladden til at reducere saldoen på den gældende faktura. Hvis kravet senere afvises, tilbageføres kravskladden og udligningerne (hvis der er vedhæftet en faktura).
        - *Nej* – Der oprettes ingen kravkladde på dette tidspunkt. Den oprettes, når kravet godkendes. Der kan stadig knyttes en faktura til det nye krav, selvom der ikke er oprettet en kravkladde. Udligning kan dog ikke foretages uden kravkladden.

1. Vælg **OK**.

    Der oprettes et nyt fradrag. Hvis du angiver indstillingen **Opret kravskladde** til *Ja*, bogføres følgende transaktioner:

    - **To nye debitorposteringer** – Én transaktion modregner kravsbeløbet på den oprindelige faktura. Den anden transaktion registrerer en kundes gæld på kravbeløbet, fordi kravet endnu ikke er godkendt. Den oprindelige fakturapostering og modposteringen af kravet markeres automatisk til udligning, når du tilknytter fakturaen ved at vælge **Vedligehold \> Tilknyt faktura** i handlingsruden.
    - **To modposteringer** – Disse posteringer bogføres på finanskontoen **Modregning af fradrag**.
    - **Kravskladde** – Hvis du vil have vist kravskladden for hvert fradrag, der er vist i fradragspanelet, skal du vælge fanen **Referencer**. Kravskladden vises i feltet **Kladdebatchnummer**. Du kan også få vist kravskladden under fanen **Fradragshændelser**. Der vil den have **Opdateringstype**-værdien *Match*.

    Du vender tilbage til siden **Udlign posteringer**, som nu viser den valgte faktura som markeret. Knappen **Bogfør** er kun tilgængelig, hvis du har angivet indstillingen **Opret kravkladde** til *Ja*. Hvis den er tilgængelig, skal du vælge **Bogfør** for at reducere saldoen på fakturaen med værdien af **Kravbeløb**.

### <a name="create-a-deduction-from-a-customer-page"></a>Oprette et fradrag ud fra en debitorside

Processen til oprettelse af et fradrag ud fra en debitorside ligner processen til oprettelse af et fradrag via fradragspanelet. Debitoren angives dog automatisk.

1. Gå til **Debitorer \> Kunder \> Alle kunder**.
1. Vælg den debitor, der skal oprettes et fradrag for.
1. I handlingsruden under fanen **Indsaml** i gruppen **Fradrag** skal du vælge **Opret fradrag**.

    I dialogboksen **Nyt fradrag** er feltet **Fradrags-id** baseret på nummerserien for **Fradrags-id**, der er defineret på siden **Parametre til administration af handelsrabat** (**Salg og market \> Konfiguration \> Handelsrabatter \> Parametre til administration af handelsrabat**). Feltet **Debitorkonto** er angivet til den debitorkonto, som fradraget gælder for.

1. Angiv følgende felter:

    - **Eksternt kravnummer** – Angiv kundens kravreference.
    - **Kravsbeløb** – Angiv et kravsbeløb inklusive moms. Værdien skal være positiv.
    - **Valuta** – Vælg valutaen for fradraget. Standardværdien er den valuta, der er angivet for den valgte debitorkonto.
    - **Kravgrundlag** – Vælg kravgrundlaget. Kravgrundlaget er bestemmende for den type kreditpostering, der oprettes, efter at fradraget eller kravet er godkendt.

        - *Prisbaseret* – Der oprettes en kladde til fritekstfaktura.
        - *Antalsbaseret* – Der oprettes en negativ salgsordre eller returordre.

    - **Kravsdato** – Vælg datoen for kravet. Standardværdien er dags dato.
    - **Kravårsag** – Vælg den årsagskode, der gælder for det aktuelle fradrag. Det valgte kravgrundlag påvirker de gældende indstillinger. Du kan finde flere oplysninger om, hvordan du opretter og konfigurerer de kravårsager, der kan vælges her, i afsnittet [Oprette fradragsårsager](#deduction-reasons) tidligere i dette emne.
    - **Noter** – Tilføj eventuelle relevante noter. Når kravet er godkendt, kan godkenderen redigere eller føje det til kravets noter.
    - **Opret kravkladde** – Angiv denne indstilling for at angive, om kravkladden skal oprettes, når kravet eller fradraget oprettes:

        - *Ja* – Systemet opretter og bogfører en finanskladde ved hjælp af den kravkladde, der er oprettet på siden **Debitorparametre**. (Du kan finde flere oplysninger i [Konfigurere debitorer og fradrag](#accounts-receivable-deductions) tidligere i dette emne). Når der er knyttet en faktura til kravet, bruges kravkladden til at reducere saldoen på den gældende faktura. Hvis kravet senere afvises, tilbageføres kravskladden og udligningerne (hvis der er vedhæftet en faktura).
        - *Nej* – Der oprettes ingen kravkladde på dette tidspunkt. Den oprettes, når kravet godkendes. Der kan stadig knyttes en faktura til det nye krav, selvom der ikke er oprettet en kravkladde. Udligning kan dog ikke foretages uden kravkladden.

1. Vælg **OK**.

    Der oprettes et nyt fradrag. Hvis du angiver indstillingen **Opret kravskladde** til *Ja*, bogføres følgende transaktioner:

    - **To nye debitorposteringer** – Én transaktion modregner kravsbeløbet på den oprindelige faktura. Den anden transaktion registrerer en kundes gæld på kravbeløbet, fordi kravet endnu ikke er godkendt. Den oprindelige fakturapostering og modposteringen af kravet markeres automatisk til udligning, når du tilknytter fakturaen ved at vælge **Vedligehold \> Tilknyt faktura** i handlingsruden.
    - **To modposteringer** – Disse posteringer bogføres på finanskontoen **Modregning af fradrag**.
    - **Kravskladde** – Hvis du vil have vist kravskladden for hvert fradrag, der er vist i fradragspanelet, skal du vælge fanen **Referencer**. Kravskladden vises i feltet **Kladdebatchnummer**. Du kan også få vist kravskladden under fanen **Fradragshændelser**. Der vil den have **Opdateringstype**-værdien *Match*.

## <a name="create-a-credit-note-for-a-customer"></a>Oprette en kreditnota for en debitor

Når der findes en godkendt rabat for en kunde, kan du oprette en kreditnota til kundens konto, som skal angive rabatten. Kreditten vises derefter i fradragspanelet, hvor den kan afstemmes som et fradrag.

Følg disse trin for at oprette en kreditnota.

1. Gå til **Salg og marketing \> Kunder \> Alle kunder**.
1. Vælg kunden.
1. I handlingsruden på fanen **Indsaml**, i gruppen **Udlign** skal du vælge **Udlign transaktioner**.
1. Vælg den postering, som rabatten blev anvendt på, i dialogboksen **Udlign transaktioner**.
1. Vælg den type rabatprogram, der skal anvendes, i menuen **Funktioner** på værktøjslinjen.
1. På siden **Rabat** under fanen **Oversigt** skal du markere afkrydsningsfeltet **Markér** ud for det relevante rabat-id.
1. Vælg **Funktioner \> Opret kreditnota** i handlingsruden.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Behandle et fradrag i fradragspanelet

I fradragspanelet kan du afstemme fradrag med at åbne kreditposteringer, opdele fradrag, nægte fradrag og afskrive fradrag.

Afhængigt af hvordan du behandler fradraget, skal du udføre en eller flere af fremgangsmåderne i følgende underafsnit: Du kan kombinere procedurerne efter behov. Du kan f.eks. opdele et fradrag i to dele og derefter afstemme den ene del med en kreditnota, men lade den resterende del blive i panelet, så den bliver afstemt i forhold til en anden kreditnota på et senere tidspunkt. Du kan også afstemme et fradrag med en kreditnota, der er mindre en fradragsbeløbet og derefter afvise eller afskrive den resterende fradragssaldo.

### <a name="match-a-deduction-to-a-credit"></a>Afstemme et fradrag med en kreditnota

Benyt følgende fremgangsmåde for at afstemme et fradrag med en kredit.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Markér afkrydsningsfeltet **Markér** ud for det fradrag, der skal behandles.
1. Markér afkrydsningsfeltet **Markér** i sektionen **Åbne posteringer** for den kredit, der skal afstemmes med fradraget. Hvis der vises flere kreditter, kan du vælge mere end én kredit, som skal afstemmes med fradraget. Hvis du ønsker, at systemet automatisk skal vælge kreditter, der afstemmer fradragsbeløbet, skal du vælge en passende indstilling i menuen **Vælg fradragsbeløb** på værktøjslinjen.
1. Vælg **Vedligehold \> Afstem** i handlingsruden. Systemet afstemmer fradraget med kreditten. Hvis der resterer en saldo i fradraget, vises den i feltet **Restbeløb** under fanen **Fradrag**.

    > [!NOTE]
    > For fradrag, der blev oprettet med kommandoen **Nyt fradrag** i fradragspanelet, debitorudligningen eller debitorsiden, er kommandoen **Vedligehold \> Afstem** kun tilgængelig, hvis feltet **Kravstatus** er angivet til *Accepteret*. Denne kommando kan bruges til manuelt at afstemme den prisbaserede eller antalsbaserede transaktion med den tilknyttede kredit i sektionen **Åbne transaktioner**. Denne kredit oprettes enten, når fradraget godkendes (ved hjælp af kommandoen **Vedligehold \> Godkend fradrag**), eller når det er knyttet til en eksisterende kredit som beskrevet i [Kreditter, der oprettes uden for godkendelsesprocessen for fradrag](#credits-outside-approval) senere i dette emne. Den periodiske opgave *Udlign godkendte fradrag* (**Salg og marketing \> Periodiske opgaver \> Udlign godkendte fradrag**) kan også bruges til automatisk at afstemme fradrag og kreditter, der har matchende værdier og beløb for **Fradrags-id**.

### <a name="split-a-deduction"></a>Opdele et fradrag

Følg disse trin, hvis du vil opdele et fradrag.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Markér afkrydsningsfeltet **Markér** ud for det fradrag, der skal behandles.
1. Vælg **Vedligehold \> Opdel** i handlingsruden.
1. Angiv det beløb, der skal opdeles, fra hovedfradraget, i feltet **Opdel beløb** i dialogboksen **Opdel**. Vælg derefter **OK**.
1. Bemærk, at der vises en ny post for det opdelte beløb, under fanen **Fradrag**. Den oprindelige fradragspost indeholder resten af fradragssaldoen. Nu kan du administrere de to dele af den oprindelige rabat hver for sig.
1. Vælg den oprindelige fradragspost, og vælg derefter fanen **Referencer**. Feltet **Opdel beløb** viser det beløb, der blev opdelt fra det oprindelige beløb.

### <a name="attach-an-invoice-to-a-deduction"></a>Knytte en faktura til et fradrag

Du kan knytte en faktura til et fradrag, hvis fradraget er oprettet ved hjælp af kommandoen **Nyt fradrag** i fradragspanelet, debitorudligningen eller debitorsiden, og hvis der ikke er knyttet en faktura til det (det vil sige, at kolonnen **Faktura** er tom).

Benyt følgende fremgangsmåde for at knytte en faktura til et fradrag.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Markér afkrydsningsfeltet **Markér** ud for det fradrag, der skal behandles.
1. Vælg **Vedligehold \> Tilknyt faktura** i handlingsruden.
1. Vælg en faktura i dialogboksen **Tilknyt faktura**, og vælg derefter **OK**.
1. Benyt en af følgende fremgangsmåder i dialogboksen **Udlign posteringer**, afhængigt af om der blev bogført en kravkladde, da fradraget blev oprettet:

    - Hvis der er bogført en kravkladde, er afkrydsningsfeltet markeret i kolonnen **Markér** i den faktura, du har valgt, og kravkladdens debitorkreditransaktion. Vælg **Bogfør**. Restsaldoen på den tilknyttede faktura reduceres med kravbeløbet.
    - Hvis en kravkladde ikke er bogført, er der ikke markeret en postering i kolonnen **Markér**. Da du ikke kan modregne i en kravkladde, før fradraget er godkendt, skal du vælge **Annuller**.

### <a name="detach-an-invoice-from-a-deduction"></a>Fjerne tilknytning af en faktura fra et fradrag

Du kan fjerne tilknytningen af en faktura fra et fradrag, hvis fradraget er oprettet ved hjælp af kommandoen **Nyt fradrag** i fradragspanelet, debitorudligningen eller debitorsiden, og hvis der aktuelt er knyttet en faktura til det (det vil sige, at kolonnen **Faktura** indeholder et fakturanummer), og hvis feltet **Kravstatus** er indstillet til *Åben*. Du kan udføre denne opgave, fordi der er tilknyttet en forkert faktura. Fakturaen fjernes fra fradraget, og den resterende saldo opdateres, hvis den blev reduceret, da fakturaen blev tilknyttet.

Du kan fjerne tilknytningen af en faktura på følgende måde.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Markér afkrydsningsfeltet **Markér** ud for det fradrag, der skal behandles.
1. Vælg **Vedligehold \> Fjern faktura** i handlingsruden.

### <a name="approve-a-deduction"></a>Godkende et fradrag

Du kan godkende fradrag, der er oprettet ved hjælp af kommandoen **Nyt fradrag** på fradragspanelet, debitorudligningen eller debitorsiden. Du kan dog kun godkende fradrag, hvor feltet **Kravstatus** er angivet til *Åben*.

Følg disse trin, hvis du vil godkende et fradrag.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Markér afkrydsningsfeltet **Markér** ud for det fradrag, der skal behandles.
1. Vælg **Vedligehold \> Godkend fradrag** i handlingsruden.
1. Rediger eller tilføj oplysninger til værdien **Note** i dialogboksen **Godkend fradrag** efter behov.
1. Hvis fradraget er prisbaseret, og der ikke er knyttet en faktura til det, skal du vælge en varemomsgruppe. Varemomsgruppen angives som regel på fakturaen. Derfor skal momsvarekoden angives, når den ikke er tilknyttet en faktura.
1. Vælg **OK**.

    På dette tidspunkt kan fradraget ikke ændres yderligere. Hvis indstillingen **Opret kravkladde** blev angivet til *Nej*, da fradraget blev oprettet, oprettes og bogføres kravkladden, når fradraget godkendes. Når fradraget er godkendt, oprettes og åbnes kreditten automatisk. Typen afhænger af fradragets værdi af **Kravgrundlag**:

    - *Prisbaseret* – Hvis fradraget er prisbaseret, oprettes der en fritekstfaktura for debitorkontoen. Du kan tilføje en beskrivelse og bogføre kreditten. Følgende felter udfyldes med fradraget, når kladden oprettes:

        - **Fradrags-id** – Dette felt føjes til overskriften for at gøre det muligt igen at spore fradraget.
        - **Hovedkonto** – Værdien bestemmes af den værdi for **Kravsbogføringskonto**, der er angivet for den fradragsårsagen, der er knyttet til fradraget.
        - **Varemomsgruppe** – Værdien bestemmes af den tilknyttede faktura eller af den værdi, du valgte, da du godkendte fradraget.
        - **Enhedspris** – Værdien er kreditering af kravbeløbet for fradraget.
        - **Fakturatekst** – Dette felt er som standard angivet til værdien for fradragets **Noter**.

    - *Antalsbaseret* – Hvis fradraget er antalsbaseret, oprettes der en åben salgsordre eller returordre. Indstillingen **Opret returordre** på siden **[Debitorparametre](#accounts-receivable-deductions)** bestemmer, om der oprettes en salgsordre eller en returordre, når fradraget godkendes. Siden **Kopiér ordrer** vises og filtreres til at vise rækker, hvor feltet **Fakturakonto** er angivet til fradragets debitorkonto. Følg disse trin:

        1. I oversigtspanelet **Fakturaer** viser sektionen **Sidehoveder** salgsfakturaer, hvor værdien af **Fakturakonto** svarer til fradragets debitorkonto. Vælg en relevant salgsfaktura.
        1. Afsnittet **Linjer** viser linjer fra den valgte salgsfaktura. Markér afkrydsningsfeltet **Vælg** for hver linje, du vil kopiere. Alternativt kan du markere afkrydsningsfeltet **Vælg alle** i sektionen **Sidehoveder** for salgsordren for at vælge alle dens linjer.
        1. Juster **Antal**-værdien for en eller flere linjer efter behov.

            Alle de linjer, du har valgt indtil nu, vises i oversigtspanelet **Valgte linjer eller hoved, der skal kopieres**.

        1. Gentag de foregående to trin efter behov, indtil alle nødvendige linjer er vist i oversigtspanelet **Valgte linjer eller hoved, der skal kopieres**.
        1. Vælg **OK**.

            Den nye returordre åbnes, og følgende felter angives automatisk:

            - **Fradrags-id** – Dette felt føjes til overskriften for at gøre det muligt igen at spore fradraget.
            - **Returårsagskode** – Dette felt er som standard angivet til den værdi af **Returårsagskode**, der er angivet for den fradragsårsag, der er tildelt fradraget.

Når kreditten er faktureret, vises den i sektionen **Åbne transaktioner** i fradragspanelet mod den relevante værdi af **Fradrags-id**, og feltet **Kravtype** angives til *Andre krediteringer*. Kreditten kan benyttes, indtil den afstemmes med fradraget på en af følgende måder:

- Du kan udligne den manuelt ved at vælge **Vedligehold \> Afstem** i handlingsruden.
- Den udlignes automatisk af det periodiske job *Udlignede godkendte krav* (**Salg og marketing \> Periodiske opgaver \> Udlign godkendte krav**).
- Den udlignes automatisk, fordi indstillingen **Automatisk udligning** under fanen **Udligning** på siden **Debitorparametre** er angivet til *Ja*.

Hvis du vil have vist den kredit, der oprettes, når fradraget godkendes, kan du også bruge knappen **Åben kredit** i sektionen **Åbne posteringer** i fradragspanelet.

### <a name="create-a-return-order"></a>Oprette en returordre

Du kan oprette en returordre for fradrag, der er oprettet ved hjælp af kommandoen **Nyt fradrag** på fradragspanelet, debitorudligningen eller debitorsiden. Alle følgende betingelser skal dog være opfyldt:

- Feltet **Kravgrundlag** er angivet til *Antalsbaseret*.
- Feltet **Kravstatus** er indstillet til *Åben*.
- Indstillingen **Opret returordre** under fanen **Fradrag** på siden **[Debitorparametre](#accounts-receivable-deductions)** er angivet til *Ja*.
- Indstillingen **Opret returordre før fradragsgodkendelse** under fanen **Fradrag** på siden **[Debitorparametre](#accounts-receivable-deductions)** er angivet til *Ja*.

Følg disse trin for at oprette en returordre.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Markér afkrydsningsfeltet **Markér** ud for det fradrag, der skal behandles.
1. Vælg **Vedligehold \> Opret returordre** i handlingsruden.
1. Rediger eller tilføj oplysninger til værdien **Note** i dialogboksen **Godkend fradrag** efter behov, og vælg **OK**.
1. I oversigtspanelet **Fakturaer** i dialogboksen **Kopiér ordrer** viser sektionen **Sidehoveder** salgsfakturaer, hvor værdien af **Fakturakonto** svarer til fradragets debitorkonto. Vælg en relevant salgsfaktura.
1. Afsnittet **Linjer** viser linjer fra den valgte salgsfaktura. Markér afkrydsningsfeltet **Vælg** for hver linje, du vil kopiere. Alternativt kan du markere afkrydsningsfeltet **Vælg alle** i sektionen **Sidehoveder** for salgsordren for at vælge alle dens linjer.
1. Juster **Antal**-værdien for en eller flere linjer efter behov.

    Alle de linjer, du har valgt indtil nu, vises i oversigtspanelet **Valgte linjer eller hoved, der skal kopieres**.

1. Gentag de foregående to trin efter behov, indtil alle nødvendige linjer er vist i oversigtspanelet **Valgte linjer eller hoved, der skal kopieres**.
1. Vælg **OK**.

    Den nye returordre åbnes, og følgende felter angives automatisk:

    - **Fradrags-id** – Dette felt føjes til overskriften for at gøre det muligt igen at spore fradraget.
    - **Returårsagskode** – Dette felt er som standard angivet til den værdi af **Returårsagskode**, der er angivet for den fradragsårsag, der er tildelt fradraget.

### <a name="deny-a-deduction"></a>Afvise et fradrag

Følg disse trin, hvis du vil afvise et fradrag.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Markér afkrydsningsfeltet **Markér** ud for det fradrag, der skal behandles.
1. Vælg **Vedligehold \> Afvis** i handlingsruden.
1. Vælg årsagskoden for afvisning i dialogboksen **Afvis**, og vælg derefter **OK**.
1. I feltet **Vis** skal du under handlingsruden vælge *Lukket*.

    Under fanen **Fradrag** vises det afviste fradrag, og feltet **Restbeløb** for fradraget er angivet til *0,00*.

    For fradrag, der er oprettet ved hjælp af kommandoen **Nyt fradrag** på fradragspanelet, debitorudligningen eller debitorsiden, sker følgende:

    - Felterne i afsnittet **Afvisning** opdateres under fanen **Referencer**.
    - Hvis du valgte at oprette kravkladden, da fradraget blev oprettet, og hvis der er knyttet en faktura til det fradrag, der har reduceret fakturaens saldo, frakobles fakturaen, og restsaldoen for den tidligere tilknyttede faktura forøges med beløbet for det afviste krav.
    - Feltet **Status** for fradraget er angivet til *Lukket*.
    - Feltet **Kravstatus** for fradraget er angivet til *Afvist*.

Følg disse trin, hvis du vil fortryde en afvisning.

1. Vælg et afvist fradrag under fanen **Fradrag**.
1. Vælg **Tilbagefør afvisning** i handlingsruden.

    For fradrag, der er oprettet ved hjælp af kommandoen **Nyt fradrag** på fradragspanelet, debitorudligningen eller debitorsiden, sker følgende:

    - Felterne i afsnittet **Afvisning** opdateres under fanen **Referencer**.
    - Feltet **Status** for fradraget angives til *Åben*.
    - Feltet **Kravstatus** for fradraget er angivet til *Åben*.

### <a name="write-off-a-deduction"></a>Afskrive et fradrag

Følg disse trin, hvis du vil afskrive et fradrag.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Markér afkrydsningsfeltet **Markér** ud for det fradrag, der skal behandles.
1. Vælg **Vedligehold \> Afskriv** i handlingsruden.
1. Vælg årsagskoden for afskrivning i dialogboksen **Afskriv**, og vælg derefter **OK**.
1. I feltet **Vis** skal du vælge *Lukket*.

    Under fanen **Fradrag** vises det afskrevne fradrag, og feltet **Restbeløb** for fradraget er angivet til *0,00*.

    For fradrag, der er oprettet ved hjælp af kommandoen **Nyt fradrag** på fradragspanelet, debitorudligningen eller debitorsiden, sker følgende:

    - Felterne i afsnittet **Afskrivning** opdateres under fanen **Referencer**.
    - Hvis du oprettede kravkladden, da fradraget blev oprettet, bogføres en kravkladde i årsagskoden for fradragets afskrivning. Du kan få vist denne post under fanen **Fradragshændelser**, hvor den har **Opdateringstypen** *Afskrivning*.
    - Feltet **Status** for fradraget er angivet til *Lukket*
    - Feltet **Kravstatus** for fradraget er angivet til *Afskrivning*.

Følg disse trin, hvis du vil tilbageføre en afskrivning.

1. Vælg et afvist fradrag under fanen **Fradrag**.
1. Vælg **Tilbagefør afskrivning** i handlingsruden.

    For fradrag, der er oprettet ved hjælp af kommandoen **Nyt fradrag** på fradragspanelet, debitorudligningen eller debitorsiden, sker følgende:

    - Felterne i afsnittet **Afskrivning** opdateres under fanen **Referencer**.
    - Hvis du oprettede kravkladden, da fradraget blev oprettet, bogføres en kravkladde i årsagskoden for fradragets afskrivning. Du kan få vist denne post under fanen **Fradragshændelser**, hvor den har **Opdateringstypen** *Tilbagefør afskrivning*.
    - Feltet **Status** for fradraget angives til *Åben*.
    - Feltet **Kravstatus** for fradraget er angivet til *Åben*.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Kreditter, der oprettes uden for processen Godkend fradrag

Dette afsnit vedrører kun fradrag, der er oprettet ved hjælp af kommandoen **Nyt fradrag** på fradragspanelet, debitorudligningen eller debitorsiden.

Forskellige brugere har måske allerede oprettet en fritekstfaktura, en returordre eller en negativ salgsordre for en kundes krav uden for processen **Godkend fradrag**. Når det eksisterende fradrag godkendes i fradragspanelet, opretter systemet automatisk en ny fritekstfaktura, returordre eller negativ salgsordre. I dette afsnit beskrives, hvordan du knytter eksisterende kredit til et fradrag, før fradraget godkendes, så dubletter af kredit undgås.

### <a name="attach-a-credit-to-deduction"></a>Knytte en kredit til et fradrag

I dette afsnit beskrives, hvordan du kan knytte en kredit til et fradrag fra kreditten.

Når en kredit er tilknyttet fradraget, kan du se den ved at bruge knappen **Åbn kredit** på værktøjslinjen i sektionen **Åbne posteringer** i fradragspanelet.

Når kreditten er faktureret, og fradraget er godkendt, vises kreditten i sektionen **Åbne transaktioner** i fradragspanelet mod den relevante værdi af **Fradrags-id**, og feltet **Kravtype** angives til *Andre krediteringer*.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Knytte en fritekstfaktura til et fradrag

Benyt følgende fremgangsmåde for at knytte en fritekstfaktura til et fradrag.

1. Gå til **Debitor \> Fakturaer \> Alle fritekstfakturaer**.
1. Vælg den ønskede faktura.
1. I handlingsruden skal du under fanen **Faktura** vælge **Knyt kredit til fradrag**. Denne knap er kun tilgængelig, hvis fritekstfakturaens **Fradrags-id**-felt er tomt. Et tomt felt angiver, at fritekstfakturaen ikke allerede er knyttet til et fradrag.
1. Du kan vælge **ét** fradrag på siden *Knyt kredit til fradrag*. Du kan kun vælge åbne *prisbaserede* fradrag.
1. Vælg **OK**. Feltet **Fradrags-id** angives i overskriften for fritekstfakturaen.

#### <a name="attach-a-return-order-to-a-deduction"></a>Knytte en returordre til et fradrag

Benyt følgende fremgangsmåde for at knytte en returordre til et fradrag.

1. Gå til **Debitor \> Ordrer \> Alle returordrer**.
1. Vælg det relevante RMA-nummer (Return Merchandise Authorization).
1. I handlingsruden skal du under fanen **Returordre** vælge **Knyt kredit til fradrag**. Denne knap er kun tilgængelig, hvis returordrens **Fradrags-id**-felt er tomt. Et tomt felt angiver, at returordren ikke allerede er knyttet til et fradrag.
1. Du kan vælge **ét** fradrag på siden *Knyt kredit til fradrag*. Du kan kun vælge åbne *antalsbaserede* fradrag.
1. Vælg **OK**. Feltet **Fradrags-id** angives i overskriften for returordren.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Knytte en salgsordre til et fradrag

Hvis du vil knytte en salgsordre til et fradrag, skal du følge disse trin.

1. Gå til **Debitor \> Ordrer \> Alle salgsordrer**.
1. Vælg den relevante åbne, leverede eller fakturerede salgsordre.
1. I handlingsruden skal du under fanen **Faktura** vælge **Knyt kredit til fradrag**. Denne knap er kun tilgængelig, hvis salgsordrens **Fradrags-id**-felt er tomt. Et tomt felt angiver, at salgsordren ikke allerede er knyttet til et fradrag.
1. Du kan vælge **ét** fradrag på siden *Tilknyt fradrag*. Du kan kun vælge åbne *antalsbaserede* fradrag.
1. Vælg **OK**. Feltet **Fradrags-id** angives i overskriften for salgsordren.

#### <a name="detach-a-deduction-from-a-credit"></a>Fjerne et fradrag fra en kredit

Hvis det forkerte fradrag er blevet tilknyttet, kan du fjerne det fra kreditten. Alle følgende betingelser skal dog være opfyldt:

- Der er knyttet en kredit til fradraget.
- Feltet **Kravstatus** er indstillet til *Åben*.

Hvis du vil fjerne et fradrag fra en kredit, skal du følge et af disse trin, afhængigt af kredittypen:

- **Fritekstfakturaer:** Vælg en faktura på siden **Alle fritekstfakturaer**. I handlingsruden skal du under fanen **Faktura** vælge **Fjern kredit fra fradrag**.
- **Returordrer:** Vælg en ordre på siden **Alle returordrer**. I handlingsruden skal du under fanen **Returordre** vælge **Fjern kredit fra fradrag**.
- **Salgsordrer:** Vælg en ordre på siden **Alle salgsordrer**. I handlingsruden skal du under fanen **Faktura** vælge **Fjern kredit fra fradrag**.

### <a name="attach-a-deduction-to-a-credit"></a>Knytte et fradrag til en kredit

I dette afsnit beskrives, hvordan du kan knytte et fradrag til en kredit fra fradraget.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Knytte et fradrag til en fritekst-, returordre- eller en salgsordrekredit

Følg disse trin for at knytte et fradrag til en fritekst-, returordre- eller en salgsordrekredit.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Vælg det relevante åbne fradrag.
1. Vælg **Vedligehold \> Knyt fradrag til kredit** i handlingsruden. Denne knap er kun tilgængelig, hvis feltet **Kravstatus** er angivet til *Åben*.
1. Du kan vælge **én** kredit på siden *Tilknyt kredit*. Den type kreditter, der vises, afhænger af fradragets værdi af **Kravgrundlag**:

    - *Prisbaseret* – På siden vises fritekstfakturaer for den debitorkonto, hvor feltet **Fradrags-id** er tomt. Debitorrekvisitioner vises også, fordi fritekstfakturaen måske ikke er bogført. Derfor er der muligvis ikke et nummer, der kan refereres til.
    - *Antalsbaseret* – Den type kreditter, der vises, afhænger af indstillingen af **Opret returordre** på siden **[Debitorparametre](#accounts-receivable-deductions)**:

        - *Ja* – På siden vises returordrer for den debitorkonto, hvor feltet **Fradrags-id** er tomt.
        - *Nej* – På siden vises salgsordrer for den debitorkonto, hvor feltet **Fradrags-id** er tomt.

1. Vælg **OK**. Feltet **Fradrags-id** angives i overskriften for kreditten.

Når en kredit er tilknyttet fradraget, kan du se den ved at bruge knappen **Åbn kredit** på værktøjslinjen i sektionen **Åbne posteringer** i fradragspanelet.

Når kreditten er faktureret, og fradraget er godkendt, vises kreditten i sektionen **Åbne transaktioner** i fradragspanelet mod den relevante værdi af **Fradrags-id**, og feltet **Kravtype** angives til *Andre krediteringer*.

#### <a name="detach-a-credit-from-the-deduction"></a>Fjerne en kredit fra fradraget

Hvis den forkerte kredit er blevet tilknyttet, kan du fjerne den fra fradraget. I handlingsruden skal du i gruppen **Vedligehold** vælge **Fjern fradrag fra kredit**. Værdien **Fradrags-id** fjernes fra kreditten.

Knappen **Fjern fradrag fra kredit** er kun tilgængelig, hvis følgende betingelser er opfyldt:

- Der er knyttet en kredit til fradraget.
- Feltet **Kravstatus** er indstillet til *Åben*.

## <a name="create-a-one-time-promotion"></a>Oprette en engangskampagne

Nogle gange har du muligvis ikke en godkendt rabat, som du kan afstemme i forhold til et fradrag. I dette tilfælde kan du bruge funktionen *engangskampagne* til at afstemme fradraget med en handelsrabat, der er knyttet til kunden. Funktionen *engangskampagne* opretter en ny handelsrabataftale og en merchandisinghændelse med et engangsbeløb. Den afstemmer derefter engangsbeløbet med fradraget og opretter de posteringer, der er nødvendige for at lukke fradraget.

Denne funktion er nyttig, hvis du bruger handelsrabatter. Du kan finde flere oplysninger om handelsrabatter i [Administration af handelsrabat](../sales-marketing/trade-allowance.md).

Du skal først konfigurere en skabelon, der kan bruges til at oprette den nye handelsrabataftale. Du kan konfigurere skabelonen på følgende måde.

1. Gå til **Salg og marketing \> Handelsrabatter \> Skabeloner**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Udfyld felterne med de oplysninger, der skal vises i de aftaler, der er oprettet ud fra skabelonen.
1. Vælg et hierarkiniveau i feltet **Hierarki** i oversigtspanelet **Kunder**.
1. Vælg den kunde, der har et ikke-afstemt fradrag, på hierarkilisten, og vælg derefter højre piletast (**\>**). Kunden føjes til listen **Kunder med handelsrabataftale**.
1. Angiv de resterende felter efter behov, og luk siden.
1. Gå til **Salg og marketing \> Konfiguration \> Handelsrabat \> Parametre til administration af handelsrabat**.
1. I feltet **Engangskampagneskabelon** under fanen **Oversigt** skal du vælge navnet på den skabelon, der skal bruges til at oprette engangskampagner.

Derefter kan du oprette en engangskampagne i fradragspanelet. Udfør følgende trin for at oprette en engangskampagne:

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. Markér afkrydsningsfeltet **Markér** ud for det fradrag, der skal behandles.
1. Vælg **Vedligehold \> Udlign fradrag som engangskampagne** i handlingsruden.
1. Benyt følgende fremgangsmåde i dialogboksen **Engangskampagne** for at knytte fradraget til et eller flere midler:

    1. Vælg **Ny**, og vælg derefter et finansierings-id i feltet **Finansierings-id**. Gentag dette trin for at tilføje alle de finansieringsmuligheder, du har brug for.
    1. I feltet **Procent** ud for hvert finansiserings-id skal du angive procentdelen af det fradrag, der skal tildeles finansieringen. De beløb, du angiver i felterne **Procent**, skal give en total på 100 procent.

1. Vælg **OK**. Systemet opretter en handelsrabataftale, der har en merchandisinghændelse med engangsbeløb, og matcher engangsbeløbet med fradraget.

## <a name="do-a-mass-update-of-deductions"></a>Udføre en masseopdatering af fradrag

Hvis du skal foretage den samme ændring for flere fradrag, kan du vælge disse fradrag og udføre en masseopdatering af deres felter.

Følg disse trin for at udføre en masseopdatering.

1. Gå til **Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**.
1. I feltet **Vis** under handlingsruden skal du vælge den type fradrag, der skal vises.
1. Markér afkrydsningsfeltet ud for hvert fradrag, der skal opdateres. Vælg **Vedligehold \> Masseopdater** i handlingsruden.
1. I dialogboksen **Masseopdatering** vises de valgte fradrag. Opdater felterne efter behov, og vælg derefter **OK** for at acceptere ændringerne.
