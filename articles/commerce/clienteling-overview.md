---
title: Oversigt over kundeaktiviteter
description: Dette emne indeholder en oversigt over de nye egenskaber for kundeaktiviteter, der findes i butiksprogrammet.
author: bebeale
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: d76668fa16a7634e7fbd953afaa6c89eed5457a2
ms.sourcegitcommit: 21943fa91c35f063a5bd064290bf2c005394df52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456501"
---
# <a name="clienteling-overview"></a>Kundeaktiviteter, oversigt

[!include [banner](includes/banner.md)]


Mange detailhandlere, især højkvalitets specialdetailhandlere, vil have deres salgsmedarbejdere til at danne langsigtede relationer med deres centrale kunder. Medarbejderne forventes at have kendskab til, hvad disse kunder kan og ikke kan lide, deres indkøbshistorik, produktpræferencer og vigtige datoer, f.eks. jubilæer og fødselsdage. Medarbejderne skal bruge et sted, hvor de kan hente disse oplysninger, og hvor det er let finde dem, når det er påkrævet. Hvis disse oplysninger er tilgængelige i en enkelt visning, kan medarbejderne nemt gå målrettet efter kunder, der opfylder bestemte kriterier. De kan f.eks. finde alle kunder, der foretrækker at købe håndtasker, eller kunder, hvor en vigtig hændelse nærmer sig, som f.eks. en fødselsdag eller mærkedag.

## <a name="client-book"></a>Klientkartotek

I Microsoft Dynamics 365 Commerce kan detailhandlere bruge funktionen Klientbog til at hjælpe med at bibehold medarbejdernes langsigtede relationer med centrale kunder.

Klientbogen indeholder kundekort, der viser kontaktoplysninger for hver kunde sammen med tre yderligere egenskaber, der defineres af detailhandleren, og som er konfigureret i Headquarters. Detailhandlerne kan beslutte de tre vigtigste ting, som salgsmedarbejderne skal vide om kunderne. En smykkeforhandler ønsker f.eks. at inkludere vigtige datoer såsom jubilæer eller fødselsdage, fordi disse datoer er lejligheder, hvor folk potentielt køber flere smykker. På samme måde vil en detailhandler måske gerne medtage kundens foretrukne indkøbsinteresser og mærker.

I klientbogen kan du også gøre det muligt for salgsmedarbejderen at filtrere listen, så den kun viser kunder, der opfylder bestemte kriterier. En ny kollektion af sko er f.eks. landet i butikken, og en medarbejder ønsker at informere de kunder, der gerne vil købe sko. I dette tilfælde kan medarbejderen filtrere klientbogen for at finde de relevante kunder og derefter foretage yderligere handlinger.

Hvis en kunde ikke længere betragtes som en nøglekunde af en eller anden grund, og denne derfor ikke skal følges tæt, kan salgsmedarbejderen fjerne dem fra deres klientbog.

Nogle detailhandlere ønsker ikke at administrere kunder på salgsmedarbejderniveau. De foretrækker i stedet for at administrere en række nøglekunder på butiksniveau. Disse detailhandlere kan få vist kunder fra butikkens klientbøger. Ved hjælp af denne indstilling kan detailhandlere få vist kunderne fra klientbøgerne fra alle de salgsmedarbejdere, hvis adressekartotek svarer til adressekartoteket i den aktuelle butik. Hvis en salgsmedarbejder arbejder i flere af den juridiske enheds butikker, viser klientbogen alle kunder fra alle de pågældende butikker. Denne funktion understøtter yderligere egenskaber. Kunder kan f.eks. omfordeles fra én salgsmedarbejder til en anden salgsmedarbejder. Denne egenskab er nyttig, når salgsmedarbejdere overflyttes eller forlader virksomheden.

Hver salgsmedarbejder kan have én klientbog pr. juridisk enhed, og salgsmedarbejdere kan føje en eller flere kunder til deres klientbog. I øjeblkket kan hver kunde i Commerce kun føjes til én klientbog. Microsoft har dog planer om at tilføje funktioner, der gør det muligt for en enkelt kunde at blive tilføjet til flere klientbøger.

> [!NOTE]
> I modsætning til kundesøgning filtrerer klientbogen ikke kundeposter baseret på butikkens adressekartoteker.

## <a name="activities-and-notes"></a>Aktiviteter og bemærkninger

Online-kanaler giver detailhandlere mulighed for at få mere at vide om kundepræferencer uden at det kræves, at kunderne udtrykkeligt angiver disse oplysninger. Når kunderne interagerer med salgsmedarbejdere i butikken, vil de derimod dele eksplicitte oplysninger om deres præferencer. Disse oplysninger kan desværre gå tabt, når salget er gennemført. Men hvis disse oplysninger registreres, kan det hjælpe forhandlerne med bedre at forstå kunderne, og derved give bedre anbefalinger og en bedre overordnet indkøbsoplevelse.

Hvis du vil registrere vigtige oplysninger, som kunder deler, kan salgsmedarbejdere gøre brug af ikke blot attributterne for klientbogen, men også bruge funktionerne aktiviteter og noter. Detailhandlerne kan konfigurere aktivitetstyper, f.eks. oplysninger om besøget i butikken, e-mailadresse, telefonnummer og aftaler. Aktiviteter, som medarbejderne opretter, kan vises i tidslinjeformat på POS. De vises også under fanen **Aktiviteter** på siden **Alle kunder \> Generelt** i Headquarters.

Salgsmedarbejdere kan også bruge noter til at registrere generelle kundeoplysninger, der kan refereres til før hver enkelt interaktion. Disse noter gemmes i Headquarters og kan ses i kundeprofilen eller på siden over kundedetaljer i callcentret.

> [!NOTE]
> I øjeblikket kan alle notater og aktiviteter ses af alle salgsmedarbejdere, der arbejder for den juridiske enhed og kan se sider med kundedetaljer. Noter og aktiviteter er ikke begrænset til den medarbejder, der har føjet en kunde til klientbogen.

## <a name="integration-with-dynamics-365-customer-insights"></a>Integration med Dynamics 365 Customer Insights

Ved at bruge Dynamics 365 Customer Insights-programmet kan detailhandlere indsamle data fra de forskellige systemer, som kunderne bruger til at interagere med detailhandlerens varemærke. De kan derefter bruge disse data til at generere en enkelt visning af kunden og udlede indsigt heraf. Integrationen af Customer Insights med Commerce giver detailhandlere mulighed for at vælge en eller flere målpunkter, der skal vises på kundekortet i klientbogen. Detailhandlere kan f.eks. bruge dataene i Customer Insights til at beregne "Churn sandsynligheden" for en kunde og definere, hvad den "næste bedste handling" skal være. Hvis disse værdier defineres som målpunkter, kan de vises på kundekortet, og de kan tilvejebringe vigtige oplysninger til salgsmedarbejderne. Yderligere oplysninger om Customer Insights finder du i dokumentationen [Dynamics 365 Customer Insights](https://docs.microsoft.com/dynamics365/ai/customer-insights/overview). Du kan finde flere oplysninger målpunkter i [Målpunkter](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="set-up-clienteling"></a>Konfigurer kundeaktiviteter

Hvis du vil aktivere funktionen kundeaktiviteter i dit miljø, skal du følge disse trin.

1. I arbejdsområdet **Administration af funktioner** skal du filtrere funktionerne ved hjælp af modulet **Detail og handel**.

    ![Kundeaktiviteter på listen over funktioner i Commerce-modulet](./media/Enable_clienteling.png "Kundeaktiviteter på listen over funktioner i modulet Detail og handel")

2. Aktiver funktionen **Kundeaktiviteter** ved at vælge **Aktivér nu**.
3. På siden **Commerce-parametre** under fanen **Nummerserie** skal du vælge rækken **Identifikator for klientbog**. Dernæst skal du i feltet **Nummerseriekode** vælge en nummerserie. Systemet bruger denne nummerserie til at tildele et ID til klientbøger.
4. Vælg **Gem**.
5. Opret en ny attributgruppe, der indeholder de attributter, du vil registrere for kunder, der administreres i klientbøger. For instruktioner se [Attributter og attributgrupper](https://docs.microsoft.com/dynamics365/retail/attribute-attributegroups-lifecycle).

    - Definer de nødvendige attributter som **Kan redigeres**. Salgsmedarbejdere kan derefter bruge disse attributter til at filtrere deres klientbog.
    - Angiv visningsrækkefølgen for disse attributter. Denne visningsrækkefølge bestemmer, hvilke attributter der skal vises på kundekortet i klientbogen. En visningsrækkefølge på 1 anses for at være højere end en visningsrækkefølge på 2. Derfor vises den attribut, der har en visningsrækkefølge på 1, før til den attribut, der har en visningsrækkefølge på 2.

    > [!NOTE]
    > Du kan gøre Customer Insights tilgængelige fra samme side. Der skal dog oprettes et Azure-program-ID og en hemmelighed til godkendelsesformål. Du kan finde flere oplysninger om kravene under afsnittet [Aktiver integration af Customer Insights med Commerce](#turn-on-the-integration-of-customer-insights-with-commerce) senere i dette emne. Hvis Customer Insights er aktiveret, og du vælger en eller flere målpunkter, der skal vises på kundekortet, vises disse målpunkter først. Derefter vises attributgrupperne for klientbogen på baggrund af visningsrækkefølgen. Hvis du f.eks. vælger to målpunkter fra Customer Insights, vises disse to målpunkter og én attribut for klientbogen på kundekortet. (Den viste attribut for klientbogen vil være den attribut, der har den højeste visningsrækkefølge.)

6. På siden **Commerce-parametre** under fanen **Kundeaktiviteter** skal du i feltet **Attributgruppe for klientbog** vælge den attributgruppe, som du netop har oprettet.

    ![Valgt attributgruppe for klientbog](./media/Client%20book%20attributes.png "Valgt attributgruppe for klientbog")

7. Hvis du vil registrere aktiviteter, der finder sted på POS, skal du definere aktivitetstyperne på siden **Aktivitetstyper** (**Retail og Commerce \> Kunder \> Aktivitetstyper**).

    > [!NOTE]
    > Aktivitetstyper udtrækkes fra Commerce Scale Unit, når der er foretages et opkald i real tid for første gang. Når aktiviteterne er blevet udtrukket, gemmes de i et par timer. Hvis du ændrer aktivitetstyperne, skal du vente, indtil cachen ikke længere er gyldig. Alternativt kan du genstarte tjenesten Commerce Scale Unit, hvis du ikke bruger et produktionsmiljø.

8. Føj to knapper til det relevante POS-skærmlayout, så salgsmedarbejderne kan få vist deres egen klientbog og butikkens klientbog. (Butikkens klientbøger omfatter klienter fra alle klientbøger for alle salgsmedarbejdere, der deler et adressekartotek med butikken.) De tilsvarende operationer benævnes henholdsvis **Få vist kunder i klientbogen** og **Få vist kunder fra butikkens klientbog**. Der findes tre yderligere handlinger, der er relateret til klientbøger. Disse handlinger bestemmer, hvilke salgsmedarbejdere der kan tilføje, fjerne og omfordele kunder fra klientbogen. De benævnes henholdsvis **Tilføj kunder til klientbog**, **Fjern kunder fra klientbog** og **Omfordel kunder til en klientbog**.
9. Kør følgende job for tidsplanen for distributionen: 1040, 1150, 1110 og 1090.

Når du har fuldført denne procedure, kan salgsmedarbejderne åbne siden med kundedetaljer på POS og tilføje kunder til deres klientbog, få vist og registrere aktiviteter og noter for kunder og målrette kunder ved at bruge attributterne kunder og klientbog til at filtrere klientbogen. Følgende illustration viser et eksempel på en klientbog.

![Eksempel på en klientbog](./media/client_book.png "Eksempel på en klientbog")

## <a name="turn-on-the-integration-of-customer-insights-with-commerce"></a>Aktiver integration af Customer Insights med Commerce

Hvis du vil aktivere integrationen af Customer Insights med Commerce, skal du sikre dig, at du har en aktiv forekomst af Customer Insights på den lejer, hvor Commerce er klargjort. Du skal også have en Azure Active Directory (Azure AD)-brugerkonto med et Azure-abonnement.

Følg disse trin for at konfigurere integrationen.

1. Registrer et program i Azure-portalen. Dette program bruges til godkendelse i relation til Customer Insights. Du kan finde instruktioner under [Hurtig start: Registrer et program med platformen Microsoft-identitet](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).
2. Generér en ny hemmelighed for programmet Noter dig hemmeligheden, og opbevar den på et sikkert sted, for du får brug for den senere. Vælg også, hvornår hemmeligheden skal udløbe.

    > [!IMPORTANT]
    > Sikr dig, at du husker at ændre hemmeligheden, før den udløber. Ellers stopper integrationen uventet.

3. Opret en Key Vault for Azure, og gem programhemmeligheden. Du kan finde instruktioner under [Hurtig start: Angiv og hent en hemmelighed fra Key Vault for Azure ved hjælp af Azure-portalen](https://docs.microsoft.com/azure/key-vault/quick-create-portal).
4. Aktivér adgangen til Key Vault for Azure fra Commerce. For at fuldføre dette trin skal du have et program-ID og en hemmelighed. Programmet kan være det samme program, som du oprettede i trin 1, eller det kan være et nyt program. (Med andre ord kan du bruge det program, du oprettede i trin 1, til at få adgang til både Key Vault og tjenesten Customer Insights, eller du kan oprette et unikt program til hver enkelt adgangstype.) Yderligere oplysninger finder du i [Gem primære legitimationsoplysninger til tjenester Stack Key Vault for Azure](https://docs.microsoft.com/azure-stack/user/azure-stack-key-vault-store-credentials?view=azs-1908#create-a-service-principal).
5. Gå til **Systemadministration \> Opsætning \> Parametre for Key Vault** i Headquarters, og angiv de krævede oplysninger til Key Vault. Derefter skal du i feltet **Key Vault-klient** angive det program-id, du brugte i trin 4, så Commerce kan få adgang til hemmelighederne i Key Vault.
6. Hvis du vil tilføje det program, du oprettede i trin 1, til listen over sikre programmer (kaldes til tider også en sikker liste), skal du gå til Customer Insights og give **Vise**-adgang til programmet. Du finder flere instruktioner under [Tilladelser](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-permissions).
7. I Commerce skal du på siden **Parametre for Commerce** på fanen **Kundeaktiviteter** i oversigtspanelet **Dynamics 365 Customer Insights** gøre følgende:

    1. I feltet **Program-ID** skal du angive det program-ID, du brugte i trin 1.
    2. I feltet **Hemmeligt navn** skal du angive navnet på den hemmelighed i Kay Vault, du oprettede i trin 5.
    3. Angiv indstillingen **Aktivér Customer Insights** til **Ja**. Hvis opsætningen af en eller anden grund mislykkes, får du vist en fejlmeddelelse, og denne indstilling vil blive angivet til **Nej**.
    4. Du kan have flere miljøer i Customer Insights, f.eks. test- og produktionsmiljøer. Angiv i feltet **ID for miljøforekomst** det relevante miljø.
    5. I feltet **Alternativt kunde-ID** skal du angive den egenskab i Customer Insights, der er knyttet til kundens kontonummer. (i Commerce er kundens kontonummer det samme som kundens id.)
    6. De resterende tre egenskaber er de målpunkter, der vil blive vist på kundekortet i klientbogen. Du kan vælge op til tre målpunkter, der skal vises på kundekortet. (Du behøver dog ikke at vælge nogen målpunkter.) Som tidligere nævnt, viser systemet disse værdier først, og derefter vises værdierne for attributgruppen for klientbogen.
