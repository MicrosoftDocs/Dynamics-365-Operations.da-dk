---
title: Fejlfinding i forbindelse med problemer med direkte synkronisering
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med direkte synkronisering.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: df184decdfa900ccb5c2070575e55052b9dfc547
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062357"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Fejlfinding i forbindelse med problemer med direkte synkronisering

[!include [banner](../../includes/banner.md)]



Dette emne indeholder fejlfindingsoplysninger for dobbeltskrivning mellem Finans- og driftsapps og Microsoft Dataverse. Specifikt indeholder emnet oplysninger, der kan hjælpe dig med at løse problemer med direkte synkronisering.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller Azure Active Directory (Azure AD) -legitimationsoplysninger fra lejeradministratoren. Hvert afsnit forklarer, om der kræves en bestemt rolle eller specifikke legitimationsoplysninger.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Live synkronisering viser en fejl, når du opretter en række

Du kan få vist følgende fejlmeddelelse, når du opretter en række i en Finans- og driftsapp:

*\[{\\"fejl\\":{\\"kode\\":\\"0x 80072560\\",\\"meddelelse\\":\\"Brugeren er ikke medlem af organisationen.\\"}}\], Fjernserveren returnerede en fejl: (403) forbudt."}}".*

Du kan løse problemet ved at følge trinnene i [Systemkrav og forudsætninger](requirements-and-prerequisites.md). Hvis du vil udføre disse trin, skal de brugere af dobbeltskrivningsprogrammet, der er oprettet i Dataverse, have rollen som systemadministrator. Standard-ejerteamet skal også have rollen som systemadministrator.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Live-synkronisering viser en fejl, når du forsøger at gemme tabeldata

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist følgende fejlmeddelelse, når du forsøger at gemme tabeldata i en Finans- og driftsapp:

*Ændringerne kan ikke gemmes i databasen. Arbejdsenheden kan ikke allokere transaktionen. Der kunne ikke skrives data til enhedsmåleenheder (uoms). Skrivning til UnitOfMeasureEntity mislykkedes, og fejlmeddelelsen "Kan ikke synkronisere med enhedsmåleenheder" vises.*

Hvis du vil løse dette problem, skal du sørge for, at de nødvendige referencedata findes i både Finans- og driftsappen og Dataverse. Hvis en kunde post f.eks. tilhører en bestemt kundegruppe, skal du kontrollere, at kundegruppeposten findes i Dataverse.

Hvis der findes data på begge sider, og du har bekræftet, at problemet ikke er datarelateret, skal du følge disse trin.

1. Åbn enheden **DualWriteProjectConfigurationEntity** ved hjælp af tilføjelsesprogrammet til Excel. Hvis du vil bruge tilføjelsesprogrammet, skal du aktivere designtilstand i Excel-tilføjelsesprogrammet Finans og drift og føje **DualWriteProjectConfigurationEntity** til regnearket. Du kan finde flere oplysninger i [Få vist og opdatere enhedsdata med Excel](../../office-integration/use-excel-add-in.md).
2. Vælg og slet de poster, der indeholder problemer i tilknytningen til skriv og projekt. Der vil være to poster for hver tilknytning, der skrives i.
3. Udgiv ændringerne ved hjælp af tilføjelsesprogrammet Excel. Dette trin er vigtigt, fordi det sletter posterne fra enheden og underliggende tabeller.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Håndtere fejl i forbindelse med læse- eller skriverettigheder, når du opretter data i en Finans- og driftsapp

Du kan få vist en fejlmeddelelsen "Forkert anmodning", når du opretter data i en Finans- og driftsapp.

![Eksempel på fejlmeddelelsen Ugyldig anmodning.](media/error_record_id_source.png)

For at løse problemet skal du tildele den manglende rettighed ved at tildele den korrekte sikkerhedsrolle til teamet for den tilknyttede Dynamics 365 Sales- eller Dynamics 365 Customer Service-virksomhedsenheder.

1. Find den virksomhedsenhed i Finans- og driftsappen, der er tilknyttet i Dataintegration-forbindelsessættet.

    ![Organisationstilknytning.](media/mapped_business_unit.png)

2. Log på miljøet i Customer Engagement-appen i miljøet, naviger til **Indstilling \> Sikkerhed**, og find teamet for den tilknyttede virksomhedsenhed.

    ![Team for den tilknyttede virksomhedsenhed.](media/setting_security_page.png)

3. Åbn siden for teamet til redigering, og vælg derefter **Administrer roller**.

    ![Knappen Administrer roller.](media/manage_team_roles.png)

4. I dialogboksen **Administrer teamroller** skal du tildele den rolle, der har læse-/skriverettigheden til de relevante tabeller, og derefter vælge **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Rette synkroniseringsproblemer i et miljø, der har et Dataverse-miljø, som er blevet ændret for nylig

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist følgende fejlmeddelelse, når du opretter data i en Finans- og driftsapp:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Der kunne ikke oprettes nyttedata for enheden CustCustomerV3Entity**", "logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Der opstod en fejl under oprettelse af nyttedata med følgende fejlmeddelelse om ugyldig URI: URI'en er tom".}\],"isErrorCountUpdated":true}*

Her kan du se, hvordan fejlen ser ud i Customer Engagement-appen:

> Der opstod en uventet fejl fra ISV-koden. (ErrorType = ClientError) Uventet undtagelse fra plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: enhedskontoen kunne ikke behandles - (et forbindelsesforsøg mislykkedes, fordi den tilsluttede part ikke svarede korrekt efter en tidsperiode, eller den oprettede forbindelse mislykkedes, fordi den vært, der er oprettet forbindelse til, ikke svarede.

Denne fejl opstår, når Dataverse-miljøet nulstilles forkert, samtidig med at du forsøger at oprette data i Finans- og driftsappen.

> [!IMPORTANT]
> Hvis du har sammenkædet miljøet igen, skal du stoppe alle enhedsstilknytninger, før du fortsætter med de trin, der er under begrænsning.

Du kan løse problemet ved at udføre trin både i Dataverse og i Finans- og driftsappen.

1. Følg disse trin i Finans- og driftsappen.

    1. Åbn enheden **DualWriteProjectConfigurationEntity** ved hjælp af tilføjelsesprogrammet til Excel. Hvis du vil bruge tilføjelsesprogrammet, skal du aktivere designtilstand i Excel-tilføjelsesprogrammet Finans og drift og føje **DualWriteProjectConfigurationEntity** til regnearket. Du kan finde flere oplysninger i [Få vist og opdatere enhedsdata med Excel](../../office-integration/use-excel-add-in.md).
    2. Vælg og slet de poster, der indeholder problemer i tilknytningen til skriv og projekt. Der vil være to poster for hver tilknytning, der skrives i.
    3. Udgiv ændringerne ved hjælp af tilføjelsesprogrammet Excel. Dette trin er vigtigt, fordi det sletter posterne fra enheden og underliggende tabeller.
    4. Hvis du vil forhindre fejl, når du sammenkæder Finans- og drifts- eller Dataverse-miljøerne igen, skal du sikre dig, at der ikke længere er nogen konfigurationer af skærmskrivning.

2. Følg disse trin i Dataverse:

    1. Log på dit Dataverse-miljø (f.eks. `https://*****.crm.dynamics.com/`).
    2. Gå til **Avanceret søgning** \> **Avancerede indstillinger**.
    3. Vælg **konfiguration af runtime for den aktuelle opsætning**.
    4. Markér den kolonne, der skal vises.
    5. Vælg **resultater** for at få vist varianterne.
    6. Slet alle forekomster.

3. Følg disse trin i Finans- og driftsappen.

    1. Åbn enheden **DualWriteProjectConfigurationEntity** ved hjælp af tilføjelsesprogrammet til Excel. Hvis du vil bruge tilføjelsesprogrammet, skal du aktivere designtilstand i Excel-tilføjelsesprogrammet Finans og drift og føje **DualWriteProjectConfigurationEntity** til regnearket. Du kan finde flere oplysninger i [Få vist og opdatere enhedsdata med Excel](../../office-integration/use-excel-add-in.md).
    2. Vælg og slet de poster, der indeholder problemer i tilknytningen til skriv og projekt. Der vil være to poster for hver tilknytning, der skrives i.
    3. Udgiv ændringerne ved hjælp af tilføjelsesprogrammet Excel. Dette trin er vigtigt, fordi det sletter posterne fra enheden og underliggende tabeller.
    4. Hvis du vil forhindre fejl, når du sammenkæder Finans- og drifts- eller Dataverse-miljøerne igen, skal du sikre dig, at der ikke længere er nogen konfigurationer af skærmskrivning.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Live-synkroniseringsfejl, efter du har kopieret hele databasen

Du kan få vist følgende fejlmeddelelse, når du kører en fuld databasekopi fra et system til et andet og derefter prøver at køre en databasehandling:

*SecureConfig Organization (???) svarer ikke til den faktiske CRM-organisation (???).*

Fejlmeddelelsen vises fra runtime-in-systemet for at sikre, at den konfiguration, der er konfigureret i ét system, ikke kan bruges i et andet system.

Du kan løse problemet ved at slette alle posterne i **msdyn_dualwriteruntimeconfig**, når du har gendannet databasen. Du kan finde flere oplysninger i [Fjerne sammenkædningen og sammenkædningen af nye omskrivningsmiljøer](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Problemer med live synkronisering, som forårsages af forkerte filtersyntaks for forespørgsler på maps'et

Selvom forespørgselsudtrykket for et visningsoversigtsfilter er syntakt korrekt, vil det muligvis ikke fungere som forventet. Filterudtrykket er på en enhed, ikke på en individuel datakilde for et forespørgselsobjekt. Den SQL-forespørgsel, der genereres, returnerer derfor ikke de forventede resultater.

Her er et eksempel.

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Du forventer måske, at projekter, der ikke har nogen overordnet, filtreres ud. Filteret virker dog ikke, fordi det er oversat til en forespørgsel, der ligner følgende eksempel.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Det faktiske resultat er, at `parentProject`-feltet evalueres til `null`. Men `null` er ikke det samme som den tomme streng. På grund af denne uoverensstemmelse giver forespørgselsfilteret ikke gyldige resultater.

Følg disse trin for at løse dette problem.

1. Tilføj en beregnet kolonne, der kan tilføjes i en udvidelsesmodel, og som er udgangspunktet for logik, der konverterer `null` til den tomme streng.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Brug filteret på den nye beregnede kolonne i stedet for standardkolonnen.

Hvis du vil evaluere filteret i et udviklingsmiljø, kan du bruge følgende X++-kode til at validere resultaterne. Kør denne kode som et enkeltstående program. Du kan bruge den til at evaluere forskellige typer filtre, der gælder for en enhed, før du bruger disse filtre på kort, der skrives på. Forespørgslen kan køres mod databasen for at evaluere uoverensstemmelser.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Data fra Finans- og driftsapps, hvor de ikke er synkroniseret til Dataverse

Under live synkronisering kan der opstå et problem, hvor kun en del af dataene synkroniseres fra Finans- og driftsapps til Dataverse, eller hvor datasæt ikke er synkroniseret overhovedet.

> [!NOTE]
> Du skal løse dette problem under udviklingen.

Før du begynder at rette problemet, skal du gennemgå følgende forudsætninger:

+ Kontroller, at dine brugerdefinerede ændringer er skrevet med et enkelt posteringsområde.
+ Forretningshændelser og computerskrivestruktur kan ikke håndtere `doinsert()`, `doUpdate()` og `recordset()`-operationer eller poster, hvor `skipBusinessEvents(true)` er markeret. Hvis koden findes i disse funktioner, udløses skrivekoden ikke.
+ Forretningshændelser skal være registreret for den tilknyttede datakilde. Nogle datakilder kan bruge en ydre joinforbindelse og kan være markeret som skrivebeskyttet i Finans- og driftsapps. Disse datakilder spores ikke.
+ Ændringer udløses kun, hvis ændringerne findes i de tilknyttede felter. Feltændringer, der ikke er tilknyttet, udløser ikke skrivning.
+ Sørg for, at filterevalueringer giver et gyldigt resultat.

### <a name="troubleshooting-steps"></a>Fejlfindingstrin

1. Gennemse felttilknytninger på startsiden til admin-skrivning. Hvis et felt ikke er tilknyttet fra Finans- og driftsapps til Dataverse, spores det ikke. I følgende illustration spores feltet **Beskrivelse** f.eks. fra Dataverse, men ikke fra Finans- og driftsapps. Ingen ændringer af dette felt i Finans- og driftsapps spores.

    ![Sporet felt.](media/live-sync-troubleshooting-1.png)

2. Bestem, om datakilden spores i definitionen af forretningshændelser. I følgende illustration spores der f.eks. ikke et felt fra tabellen **DefaultDimensionDAVs** og underliggende tabeller, så der ikke spores ændringer. Datakilder, der bruger en ydre joinforbindelse, og som er markeret som skrivebeskyttede, spores ikke.

    ![Felt, som ikke er sporet.](media/live-sync-troubleshooting-2.png)

3. Bestem, om de tilknyttede tabelfelter skal vises i tabellen **BUSINESSEVENTSDEFINITION**, som vist i følgende illustration. Hvis du ikke kan finde det felt, du leder efter, i forespørgselsresultatet, udløses det ikke af omskrivning.

    ![Feltet Spores i tabellen.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Eksempelscenario

I Finans- og driftsapps opdateres adressen til en kontaktpersonpost, men adresseændringen synkroniseres ikke til Dataverse. Dette scenario opstår, fordi ingen post i tabellen **BusinessEventsDefinition** indeholder kombinationen af den berørte tabel og enheden. Tabellen **LogisticsPostalAddress** er specifikt den direkte datakilde for enheden **smmContactpersonCDSV2Entity**. **SmmContactpersonCDSV2Entity**-enheden har **smmContactPersonV2Entity** som datakilde, og **smmContactPersonV2Entity** har til gengæld **LogisticsPostalAddressBaseEntity** som datakilde. Tabellen **LogisticsPostalAddress** er datakilden for **LogisticsPostalAddressBaseEntity**.

En lignende situation kan forekomme i nogle mønstre, der ikke er standard, f.eks. tilfælde, hvor den tabel, der ændres i Finans- og driftsapps, muligvis ikke er knyttet til den enhed, der indeholder den. De primære adressedata beregnes f.eks. på enheden **smmContactPersonCDSV2Entity**. Dobbeltskrivestruktur forsøger at finde ud af, hvordan en ændring i en underliggende tabel knyttes tilbage til enheder. Normalt er denne indfaldsvinkel tilstrækkelig. I nogle tilfælde er linket dog så komplekst, at du skal være specifik. Du skal sikre dig, at **RecId** for den relaterede tabel er direkte tilgængelig for enheden. Tilføj derefter en statisk metode for at overvåge tabellen, så tabellen ikke ændres.

Gennemse f.eks. **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()**-metoden. **CustCustomerV3entity** og **VendVendorV2Entity** er blevet ændret for at håndtere denne situation.

Følg disse trin for at løse dette problem.

1. Føj feltet **PrimærPostalAddressRecId** til **smmContactPersonV2Entity**-enheden. Gør det internt.

    ![Felt, der er føjet til smmContactPersonV2Entity-enheden.](media/Troubleshoot_live_sync_issue_1.png)

2. Tilføj samme felt til **smmContactPersonCDSV2Entity**-enheden.

    ![Felt, der er føjet til smmContactPersonCDSV2Entity-enheden.](media/Troubleshoot_live_sync_issue_2.png)

3. Føj følgende metode til **smmContactPersonCDSV2Entity-klassen**.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Synkroniser databasen, og opbyg programmet.
5. Stop alle de knyttekort, der er oprettet i **smmContactPersonCDSV2Entity**-enheden.
6. Start kortet. Den nye tabel (**LogisticsPostalAddress** i dette eksempel), som du er begyndt at spore, ved hjælp af kolonnen **RefTableName** for den række, hvor værdien for **refentityname** er lig med **smmContactPersonCDSV2Entity** i tabellen **BusinessEventsDefinition**.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Fejl, når du opretter en post, hvor der sendes flere poster fra en Finans- og driftsapp til Dataverse i samme batch

Ved enhver transaktion opretter en Finans- og driftsapp data i et batch og sender dem som en batch til Dataverse. Hvis der oprettes to poster som en del af den samme transaktion, og de refererer til hinanden, får du måske vist en fejlmeddelelse, der ligner følgende eksempel i Finans- og driftsappen:

*Det var ikke muligt at skrive data til enheder aaa_fundingsources. Det var ikke muligt at ebecsfs_contracts med {PC00...}-værdier. Det var ikke muligt at aaa_fundingsources med {PC00...}-værdier. Skriver for at aaa_fundingsources der mislykkedes med fejlmeddelelsen Undtagelse: Fjernserveren returnerede en fejl: (400) Ugyldig anmodning.*

Du kan løse problemet ved at oprette enhedsforhold i Finans- og driftsappen for at angive, at de to enheder er relateret til hinanden, og at de relaterede poster håndteres i samme transaktion.

## <a name="enable-verbose-logging-of-error-messages"></a>Aktiver verboselog af fejlmeddelelser

I en Finans- og driftsapp kan der opstå fejl, der er relateret til Dataverse-miljøet. Fejlmeddelelsen indeholder muligvis ikke den fulde tekst til meddelelsen eller andre relevante data. Hvis du vil have flere oplysninger, kan du aktivere verbose-logføring ved at angive mærket **IsDebugMode**, der findes på enheden **DualWriteProjectConfigurationEntity** i alle projektkonfigurationer i Finans- og driftsapps.

1. Åbn enheden **DualWriteProjectConfigurationEntity** ved hjælp af tilføjelsesprogrammet til Excel. Hvis du vil bruge tilføjelsesprogrammet, skal du aktivere designtilstand i Excel-tilføjelsesprogrammet Finans og drift og føje **DualWriteProjectConfigurationEntity** til regnearket. Du kan finde flere oplysninger i [Få vist og opdatere enhedsdata med Excel](../../office-integration/use-excel-add-in.md).
2. Indstil mærket **IsDebugMode** til **Ja** for projektet.
3. Køre scenariet.
4. De detaljerede logfiler er tilgængelige i tabellen **DualWriteErrorLog**. Hvis du vil slå data op ved hjælp af tabelbrowseren, skal du bruge følgende URL-adresse: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`
5. Hvis du vil hente flere logfiler i fejlfindingstilstand, skal du installere opdateringen i [KB 4595434 (Ret blanke værdier, der udbredes i dobbeltskrivning-live synkronisering)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Fejl, når du tilføjer en adresse til en kunde eller kontakt

Du kan få vist følgende fejlmeddelelse, når du forsøger at tilføje en adresse til en kunde eller kontaktperson i Finans- og driftsapps eller Dataverse:

*Det var ikke muligt at skrive data til enheder msdyn_partypostaladdresses. Skriver til DirPartyPostalAddressLocationCDSEntity mislykkedes med fejlmeddelelsen Anmodningen mislykkedes med statuskoden BadRequest og CDS-fejlkoden: 0x80040265-svarmeddelelse: Der opstod en fejl i plugin. Der findes allerede en post med attributværdierne Lokalitets-id. Nøglen til lokations-id'et for enhedsnøglen kræver, at dette sæt attributter indeholder entydige værdier. Vælg entydige værdier, og prøv igen.*

Du kan løse problemet ved at installere dubbeltskrivning-orkestreringspakkeversionen (2.2.2.60), så nøglerne i **adressetabellen** er defineret som vist i følgende tabel.

| Egenskab | Værdi |
|---|---|
| Vist navn | **Placeringsnøgle** |
| Navn | **msdyn_locationkey** |
| Felter | **msdyn_locationid**, **parentid** |
| Status | **Aktive** |
| Systemjob | Tom |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Fejl, når du tilføjer en kunde i Dataverse

Du kan få vist følgende fejlmeddelelse, når du forsøger at tilføje en kunde i Dataverse:

*"RecordError0":"Write failed for entity Customers V3 with unknown exception – Partposten blev ikke fundet for parttypen 'Organisation'"}.*

Når en debitor oprettes i Dataverse, genereres der et nyt partnummer. Fejlmeddelelsen vises, når kundeposten sammen med parten synkroniseres med Finans- og driftsapps, men der allerede er en kundepost, der har et andet partnummer.

Du kan løse problemet ved at finde kunden via opslag efter part. Oprette en kundepost for kunden, hvis der ikke allerede findes en post. Hvis kunden ikke findes, skal du bruge den eksisterende part til at oprette den nye debitorpost.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Fejl, når du opretter en ny debitor, kreditor eller kontaktperson i Dataverse

Du kan få vist følgende fejlmeddelelse, når du forsøger at oprette en ny kunde, kreditor eller kontakt i Dataverse:

*Kan ikke opdatere en partstype fra 'DirOrganization' til 'DirPerson', og der skal udføres en sletning af den eksisterende part efterfulgt af en indsættelse med den nye type i stedet.*

I Dataverse er der en nummerserie i **msdyn_party**-tabellen. Når en konto oprettes i Dataverse, oprettes i der en ny part (f.eks. **Party-001** af typen **Organisation**). Disse data sendes til Finans- og driftsappen. Hvis Dataverse-miljøet nulstilles, eller Finans- og driftsmiljøet er kædet sammen med et andet Dataverse-miljø, og der derefter oprettes en ny kontaktpersonpost i Dataverse, oprettes der en ny partværdi, der starter med **Party-001**. Denne gang vil den oprettede partpost være **Party-001** af typen **Person**. Når disse data synkroniseres, vises den foregående fejlmeddelelse i Finans- og driftsapps, fordi partposten **Party-001** af typen **Organisation** allerede findes.

Du kan løse problemet ved at ændre den automatiske nummerserie for **msdyn_partynumber** i **msdyn_party**-tabellen i Dataverse til en anden automatisk nummerserie.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Performanceproblem ved kunde- eller kontakttilknytninger

Du kan muligvis forbedre ydeevnen for live synkronisering for kunder og kontaktpersoner marginalt ved at tilpasse metoden **getEntityDataSourceToFieldMapping** (i enheden **CustCustomerV3Entity**) og metoden **getEntityDataSourceToFieldMapping** (i enheden **smmContactPersonCDSV2Entity**). Disse tilpasninger reducerer antallet af poster i tabellen **BusinessEventsDefinition**. Denne reduktion i antallet af poster reducerer også antallet af hændelser, der opstår.

Metoden **getEntityDataSourceToFieldMapping** i enheden **CustCustomerV3Entity** sikrer, at en opdatering af kundens elektroniske adresse eller postadresse udløser forretningshændelser, så de opdaterede data sendes til Dataverse. Hvis du ikke bruger alle felterne og ikke har brug for oplysningerne i skrive skrivefeltet, kan du kommentere de relevante linjer i metoden. Alle sporede felter og tabeller, der tilføjes med denne metode, tilføjer en post i tabellen **BusinessEventsDefinition** for kombinationen af den sporede tabel og den sporede enhed.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

På lignende måde sikrer metoden **getEntityDataSourceToFieldMapping** i enheden **smmContactPersonCDSV2Entity**, at en opdatering af kundens elektroniske adresse eller postadresse udløser forretningshændelser, så de opdaterede data sendes til Dataverse. I metoden kan du kommentere linjerne for alle felter, du ikke bruger.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Når du har opdateret metoderne, skal du følge disse trin.

1. Synkroniser databasen, og opbyg programmet.
2. Stop alle de dobbeltskrivningskort i enhederne **smmContactPersonCDSV2Entity** og **CustCustomerV3Entity**.
3. Start kortene. Der skal vises færre poster i **smmContactPersonCDSV2Entity** og **CustCustomerV3Entitytities** og tabellen **BusinessEventsDefinition**, og ydeevnen kan blive marginalt forbedret.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
