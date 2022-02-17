---
title: Ofte stillede spørgsmål til integration with Finance
description: Dette emne beskriver, hvilke data der synkroniseres i en integration af Human Resources og Finance.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 308e2a538666522edf4a76be13b93c82c3f3a774
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071104"
---
# <a name="integration-with-finance-faq"></a>Ofte stillede spørgsmål til integration with Finance


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dette emne indeholder svar på almindelige spørgsmål om, hvilke data der synkroniseres, når Dynamics 365 Human Resources integreres med Dynamics 365 Finance.

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>Kan jeg redigere Dynamics 365 Talent-programbrugeren i Power Apps?

Nej. Hvis du redigerer Human Resources-applikationsbrugeren, vil integrationen mellem Human Resources og Dataverse muligvis ikke fungere. Følgende tabel viser standardindstillingerne for Talent-programbrugeren.

| Fulde navn | Program-id | Azure AD-objekt-id | Program-id-URI |
| --- | --- | --- | --- |
| Dynamics 365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![Standardindstillinger for Talent-programbruger.](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Synkroniseres alle data eller bare nogle dataenheder?

Eet undersæt af dataene synkroniseres. Du kan finde en liste over alle enheder i [Integration med Dynamics 365 Finance](hr-admin-integration-finance.md).

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>Hvorfor kan jeg ikke se data, der er synkroniseret til Dataverse?

Som standard er Dataverse-integrationen slået fra i nye miljøer, der ikke indeholder de leverede demonstrationsdata. Som standard er den aktiveret i nye miljøer, der indeholder demonstrationsdata, og datasynkroniseringen starter, når miljøet klargøres. Når miljøet er klar til at synkronisere data, kan du aktivere integrationen. Du kan finde flere oplysninger under [Konfigurere Dataverse-dataintegration](hr-admin-integration-common-data-service.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Kan jeg oprette en ny tilknytning uden at bruge skabelonerne?

Skabeloner bruges som udgangspunkt. Du kan oprette din egen skabelon, men der skal altid bruges en skabelon ved oprettelse af et integrationsprojekt. Du kan finde flere oplysninger om dataintegrator (DI), skabeloner og projekter under [Integrer data i Microsoft Dataverse](/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>Kan jeg tilknytte økonomiske dimensioner for at overføre mellem Human Resources og Finance?

Økonomiske dimensioner findes ikke på nuværende tidspunkt i Dataverse og er derfor ikke del af standardskabelonen. Denne enhed er planlagt, men i øjeblikket er der ingen versionstidslinje.

For data i Finans og drift, som ikke findes i Human Resources, kan du sammenkæde de to systemer ved hjælp af **Konfigurer links** i Human Resources.

![Tilknyt økonomiske dimensioner.](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Når jeg importerer medarbejdere, bliver de sommetider placeret blandt inaktive arbejdere i Finance. Hvorfor?

Denne fejl kan opstå, hvis medarbejderne ikke har en aktiv post med ansættelsesoplysninger i Human Resources. Du kan løse dette ved at gå til **Personalestyring \> Medarbejdere \> Ansættelseshistorik \> Datoadministrator** og kontrollere, at der findes en aktiv post med ansættelsesoplysninger.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Hvis jeg vælger kun at tilknytte et undersæt af felter, udløser ændringer af ikke-tilknyttede felter så en synkronisering?

Synkronisering af data følger tidsplanen for udførelse. Integrationen henter en post, hvis et felt i posten ændres, uanset om feltet er en del af integrationstilknytningen.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Hvordan kan jeg nøjes med at sende ændringer, der kun gælder en aktiv arbejder og ikke de afsluttede poster?

Ved hjælp af "Avanceret forespørgsel" kan du filtrere og omforme kildedata, før du overfører dem til destinationen.

![Avanceret forespørgsel for aktive arbejdere.](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Kan jeg angive, hvilke felter der skal sendes til Finance for en bestemt enhed?

Felter kan tilføjes eller fjernes fra integrationsopgaven. Ikke alle datafelter, der findes i Dataverse-tabellen, udfyldes fra Human Resources.
Yderligere data kan udfyldes via Power Apps.

![Tilføje eller fjerne felter i en integrationsopgave.](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Jeg konfigurerede integration som et batchjob, men så mistede Human Resources forbindelsen til destinationssystemet. Hvordan kan jeg sende det samme sæt ændringer til destinationssystemet?

Der kræves ingen speciel opsætning for undtagelseshåndtering. Dataintegrator registrerer og rapporterer automatisk fejl, der finder sted på kilde og destination og giver mulighed for nye manuelle forsøg. Men det tillader ikke manuel rettelse af data. Hvis det er nødvendigt at opdatere data, skal det foregå ved kilden eller destinationen.

## <a name="can-i-set-up-bi-directional-integration"></a>Kan jeg konfigurere tovejsintegration?

Nej, integration går i øjeblikket kun én vej (Human Resources til Finans og drift). Der er dog en tilgængelig standardskabelon, som kan bruges til at sende data fra Human Resources til Finance.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Kan jeg tillade sletning af poster som en del af integrationen?

Nej, Dataintegrator henter ikke slettede poster til dataoverførsel. Kun oprettelse og opdateringer af data (UPSERT) er inkluderet i øjeblikket.

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Kan jeg foretage den kørsel, der mislykkedes, igen? Vil den i så fald sende en komplet fil eller kun ændringerne?

Den første kørsel af Dataintegrator er altid en fuld kørsel. Efterfølgende kørsler er baseret på registrering af ændringer. Når der er foretaget en fejlkørsel, udpakkes de poster, der er medtaget i kørslen, og de seneste ændringer fra Dataverse udsendes.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Når jeg gemmer projektet, får jeg fejlmeddelelsen: "Projektet har tilknytningsfejl". Hvad skal jeg gøre?

Kontroller konfiguration af integrationsnøglerne, foretag eventuelle nødvendige ændringer i opsætningen, og opdater derefter objekterne i projektet.

Når standardskabelonen bruges, importeres integrationsnøglerne automatisk. Dette problem kan opstå, når der føjes nye opgaver til den eksisterende skabelon.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Hvis jeg har N antal juridiske enheder, hvor arbejdere har ansættelse, skal jeg så oprette en tilknytning for hver af dem?

Ja, du skal bruge et separat integrationsprojekt i dataintegrationen for hver juridiske enhed i Finance.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Jeg har brug at overføre data, ikke der er en del af den standardskabelon, der leveres af Microsoft. Kan jeg gøre det?

Ja, du kan tilføje felter i eller fjerne dem fra den eksisterende skabelon. Skabelonen kan ændres, så der medtages yderligere data fra andre Dataverse-tabeller. Enheden skal være i Dataverse, hvis den skal medtages i skabelonen. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Jeg har netop oprettet nye Finance- og Human Resources-miljøer, og jeg får fejlmeddelelsen "Dataværdien overtræder integritetsbegrænsningerne". Hvorfor?

Årsager til denne fejl kan omfatte:

- Dataoverførslen resulterede i, at der blev udtrukket dubletposter ved kilden (Dataverse).

- Dataoverførslen har null-værdier for felter, der kræves i Finans og drift. Kontroller de data, der er i Dataverse, og at de opfylder kravene i Finans og drift.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Hvis der er kørselsfejl, og medarbejder-id'et ikke synkroniseres, hvordan finder jeg så historikjobbet med den mislykkede medarbejderpost?

Dataintegrator opretter flere projekter i Finance. Forholdet mellem Dataintegrator-opgaven og Finance-projektet er 1 til 1.

Spor tiden fra historikken for Dataintegrator-udførelse, og se efter indeks -1-projektet i Finance. Hvis opgavenummeret er 9 i Dataintegrator, er indekset i Finance 8.

1. Hent opgaveindekset fra Dataintegrator (i dette eksempel er det "9").

    ![Hent opgaveindeks fra Dataintegrator.](media/CaptureTaskIndex.png)

2. Spor projektets kørselstidspunkt.

    ![Spor projektets kørselstidspunkt.](media/CaptureTimeOfExecution.png)

3. I Finance skal du identificere indeks - 1. I dette eksempel matcher projektet med suffikset "8" og kørselstidspunkt for indeks "0" udførelsestidspunktet i trin 2.

    ![Identifikation af indeks.](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>Når jeg integrerer Human Resources og Finance, kan jeg ikke se mine Human Resources-data i Finance. Hvad skal jeg gøre?

Integrationen i Finance er en totrinsproces. Kontroller først, at Human Resources-dataene er opdaterede og tilgængelige i Dataverse. Dette er en synkronisering i nær-realtid, som du kan kontrollere i Power Apps ved at se på dataene i datatabellerne.

![Data i Dataverse.](media/DataInCDS.png)

Hvis dataene ikke vises som forventet i Dataverse, skal du kontrollere, om enheden understøttes i integrationen. For at medtage flere data i Dataverse kræver det en ændring fra Microsofts side.

Hvis enheden understøttes, og dataene er tilgængelige i Dataverse, skal du kontrollere, at tilknytningen i dataintegrator er korrekt. Hvis integratortilknytningen ser ud til at være i orden, skal du kontrollere, at datastyringsjobbet er kørt korrekt. Fejl kan opstå under kørsel af batchjob. Du kan finde flere oplysninger om datastyring i [Datastyring](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Adresserne for mine medarbejdere er forkerte, når jeg har importeret dem i Finance. Hvad skal jeg gøre?

Nummerserien for **Lokations-id** bruger det samme mønster i både Human Resources og Finance. Nummerserien skal være unik på begge sider, så der ikke opstår adressekollisioner under integrationen af data fra Dataverse til Finans og drift.

Ved implementering af Human Resources skal du kontrollere, at nummerserierne ikke de samme i Human Resources og Finance. Kontroller, at alle nummerserier ikke er ens, hvor data kan vedligeholdes i begge systemer.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Når jeg opretter mit forbindelsessæt, kan jeg ikke se forbindelsen i rullelisten Forbindelse. Hvad skal jeg gøre?

Sørg for, når du opretter forbindelser, at vælge Dynamics 365 Finance og Dataverse.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Når jeg synkroniserer ansættelser, vises fejlmeddelelserne "CompanyInfo_FK findes ikke", eller "Værdien '31/12/2154 23:59:59' i feltet 'Slutdato for ansættelse' bliver ikke fundet i den relaterede tabel 'Ansættelse'". Hvad skal jeg gøre?

Kontroller, at det er de korrekte juridiske enheder, du opretter tilknytning til. Synkroniseringen af en juridisk enhed er ikke en del af standardskabelonen, så det forventes, at de enkelte juridiske enheder, der findes i Human Resources og Dataverse, også findes i Finance. Kontroller også, at det er de korrekte juridiske enheder for det tilknyttede forbindelsessæt, du vælger.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Når jeg har oprettet projektet, ser felttilknytningen for Finance ud til at være tom. Hvad skal jeg gøre?

Opdater dataenhederne i Finance ved at gå til **Datastyring \> Rammeparametre \> Indstillinger for enhed \> Opdater liste over enheder.** Dette tager et par minutter, og derefter bør du kunne se disse tilknytninger. Dette problem opstår, når der oprettes nye projekter.

![Manglende felttilknytning.](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Yderligere ressourcer

- Dataintegrator (DI): 

  - [Integrer data i Microsoft Dataverse](/powerapps/administrator/data-integrator)

  - [Dataintegrator-fejlstyring og fejlfinding](/powerapps/administrator/data-integrator-error-management)

  - [Svar på DSR-anmodninger om systemgenererede logfiler i Power Apps, Microsoft Power Automate og Dataverse](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Datastyring:

  - [Datastyring](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
