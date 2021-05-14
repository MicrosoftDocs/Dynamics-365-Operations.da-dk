---
title: Oversigt over kundeaktiviteter
description: Dette emne indeholder en oversigt over de nye egenskaber for kundeaktiviteter, der findes i butiksprogrammet.
author: bebeale
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: b680ec227ecd70893999950a8be2ad152c476575
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937006"
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

Ved at bruge Dynamics 365 Customer Insights-programmet kan detailhandlere indsamle data fra de forskellige systemer, som kunderne bruger til at interagere med detailhandlerens varemærke. De kan derefter bruge disse data til at generere en enkelt visning af kunden og udlede indsigt heraf. Integrationen af Customer Insights med Commerce giver detailhandlere mulighed for at vælge en eller flere målpunkter, der skal vises på kundekortet i klientbogen. Detailhandlere kan f.eks. bruge dataene i Customer Insights til at beregne "Churn sandsynligheden" for en kunde og definere, hvad den "næste bedste handling" skal være. Hvis disse værdier defineres som målpunkter, kan de vises på kundekortet, og de kan tilvejebringe vigtige oplysninger til salgsmedarbejderne. Yderligere oplysninger om Customer Insights finder du i dokumentationen [Dynamics 365 Customer Insights](/dynamics365/ai/customer-insights/overview). Du kan finde flere oplysninger målpunkter i [Målpunkter](/dynamics365/ai/customer-insights/pm-measures).

## <a name="set-up-clienteling"></a>Konfigurer kundeaktiviteter

Hvis du vil aktivere funktionen kundeaktiviteter i dit miljø, skal du følge disse trin.

1. I arbejdsområdet **Administration af funktioner** skal du filtrere funktionerne ved hjælp af modulet **Detail og handel**.

    ![Kundeaktiviteter på listen over funktioner i Commerce-modulet](./media/Enable_clienteling.png "Kundeaktiviteter på listen over funktioner i modulet Detail og handel")

2. Aktiver funktionen **Kundeaktiviteter** ved at vælge **Aktivér nu**.
3. På siden **Commerce-parametre** under fanen **Nummerserie** skal du vælge rækken **Identifikator for klientbog**. Dernæst skal du i feltet **Nummerseriekode** vælge en nummerserie. Systemet bruger denne nummerserie til at tildele et ID til klientbøger.
4. Vælg **Gem**.
5. Opret en ny attributgruppe, der indeholder de attributter, du vil registrere for kunder, der administreres i klientbøger. For instruktioner se [Attributter og attributgrupper](./attribute-attributegroups-lifecycle.md).

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

1. Registrer et nyt program på Azure-portalen, og noter programnavnet, program-id'et og hemmelighed. Disse oplysninger bruges til service-til-service-godkendelse mellem Commerce og Customer Insights. Bemærk det sikkert, som det bliver nødvendigt at gemme det i nøgleboksen. I følgende eksempel kan du CI_Access_name nummer CI_Access_AppID CI_Access_AppID, CI_Access_Secret til henholdsvis ansøgningsnavnet, program-id'et og applikations-id'et. Du kan finde flere oplysninger under [Hurtig start: Registrer et program med platformen Microsoft-identitet](/azure/active-directory/develop/quickstart-register-app).

    > [!IMPORTANT]
    > Sikr dig, at du husker at ændre hemmeligheden, før den udløber. Ellers stopper integrationen uventet.

2. Gå til din forekomst af Customer Insights, og søg efter navnet på den applikation, der er oprettet ovenfor (i dette eksempel "CI_Access_name").
3. Opret en vault for en Azure-nøgle, og noter navnet og URL-adressen (i dette eksempel "KeyVaultName", "KeyVaultURL"). Du kan finde instruktioner under [Hurtig start: Angiv og hent en hemmelighed fra Key Vault for Azure ved hjælp af Azure-portalen](/azure/key-vault/quick-create-portal).
4. Gem dit nummer (i dette eksempel "CI_Access_Secret") i boksen. Når denne adresse gemmes i boksen, får denne adresse et navn. Noter navnet på (i dette eksempel, 'Adressenavn").
5. Hvis du vil have adgang til computeren fra Azure Key Vault, skal du oprette et andet program med et program-id og et program-id (i dette eksempel, "KeyVault_Access_AppID" og "KeyVault_Access_Secret"). Bemærk det sikkert, da det ikke vil blive vist igen.
6. Derefter skal du give programmet rettigheder for at få adgang til Key Vault fra Commerce ved hjælp af API'er. Gå til programsiden i Azure-portalen. Vælg **Administrer** under **API-tilladelser**. Tilføj rettigheden til at få adgang til **Azure-nøglehvælving**. Vælg **adgangspolitik** for denne tilladelse. Vælg skabelonen som **Hemmelig administration** og vælg indstillingerne **Hent**, **Liste**, **Dekrypter** og **Krypter**. 
5. Gå til **Systemadministration \> Opsætning \> Parametre for Key Vault** i Commerce Headquarters, og angiv de krævede oplysninger til Key Vault. Derefter skal du i feltet **Key Vault-klient** angive det program-id, du brugte i trin 4, så Commerce kan få adgang til hemmelighederne i Key Vault.
6. Hvis du vil tilføje det program, du oprettede i trin 1, til listen over sikre programmer (kaldes til tider også en sikker liste), skal du gå til Customer Insights og give **Vis** adgang til programmet. Du finder flere instruktioner under [Tilladelser](/dynamics365/ai/customer-insights/pm-permissions).
7. Opdater felterne som beskrevet nedenfor på siden **Systemadministration > Opsætning > Key Vault-parametre** i Commerce HQ: 

- **Nøgle Url-adresse**: "KeyVaultURL" (fra trin 3 ovenfor).
- **Nøgle-Vault-klient**: "KeyVault_Access_AppID" (fra trin 5 ovenfor).
- **Nøgle-Vault hemmelig nøgle**: "KeyVault_Access_Secret" (fra trin 5 ovenfor).
- Afsnittet under **Hemmelighed**:
    - **Navn**: Et hvilket som helst navn, f.eks. "CISecret".
    - **Beskrivelse**: Alle værdier.
    - **Hemmelig**: **vault**://<Name of key vault>/<name of secret>> I dette eksempel vil det være "vault://KeyVaultName/SecretName".

Når du har opdateret felterne, skal du vælge **Valider** for at sikre, at commerce application kan få adgang til den.

8. I Commerce på siden **Commerce-parametre** skal du på fanen **Kundeaktiviteter** på oversigtspanelet **Dynamics 365 Customer Insights** indstille **Program-id** til "CI_Access_AppID" (fra trin 1 ovenfor). Vælg navnet på den hemmelighed, der er angivet i trin 7 ovenfor ("CISecret") i **Hemmeligt navn**. Angiv indstillingen **Aktivér Customer Insights** til **Ja**. Hvis opsætningen af en eller anden grund mislykkes, får du vist en fejlmeddelelse, og denne indstilling vil blive angivet til **Nej**. 

Du kan have flere miljøer i Customer Insights, f.eks. test- og produktionsmiljøer. Angiv i feltet **ID for miljøforekomst** det relevante miljø. I feltet **Alternativt kunde-ID** skal du angive den egenskab i Customer Insights, der er knyttet til kundens kontonummer. (Inden for handel er debitorkontonummeret debitor-id'et). De øvrige tre egenskaber er de mål, der vises på kundekortet i klientkartoteket. Du kan vælge op til tre målpunkter, der skal vises på kundekortet. Det er dog ikke et krav, at du vælger nogen målinger. Som tidligere nævnt viser systemet disse værdier først, og derefter viser det værdierne for attributgruppen for klientkartoteket.


[!INCLUDE[footer-include](../includes/footer-banner.md)]