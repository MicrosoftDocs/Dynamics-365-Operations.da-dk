---
title: Administrere forretningspartnerbrugere på B2B-e-handelswebsteder
description: Dette emne beskriver, hvordan administratorer kan tilføje, redigere og slette forretningspartnerbrugere på business-to-business (B2B)-e-handelswebsteder.
author: josaw1
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f6cc1d5dfeb48fd00216fc1908e9e8be24f07131b3e5f1eaeefb10396efbebc3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734937"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Administrere forretningspartnerbrugere på B2B-e-handelswebsteder

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan administratorer kan tilføje, redigere og slette forretningspartnerbrugere på business-to-business (B2B)-e-handelswebsteder.

B2B-e-handelswebsteder kræver, at organisationer registrerer sig som forretningspartnere. Når en organisation har indsendt registreringsoplysninger til et B2B-e-handelswebsted, gennemgår den en kvalifikationsproces. Hvis organisationen er kvalificeret, er den startet som forretningspartner.

Når en organisation er startet som forretningspartner, identificeres den organisationsbruger, der startede anmodningen om at blive forretningspartner, som administratorbruger og tildeles rettigheder til at modtage yderligere autoriserede brugere af webstedet for B2B-e-handel. Disse autoriserede brugere kan derefter placere ordrer på vegne af forretningspartneren.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>Aktivere funktionen til B2B-e-handel i Commerce Headquarters

Funktionen til B2B-e-handel i Commerce Headquarters giver organisationer mulighed for at få forretningspartnere med og definere administratorbrugere. Denne funktion sætter også administratorer i stand til at oprette og administrere brugere og teams i forretningspartnere og til at tildele specifikke roller til dem. Endelig giver de forretningspartnerbrugere mulighed for at oprette ordreskabeloner og bruge eksisterende ordrer til at bestille produkter.

Følg disse trin for at aktivere funktionen til B2B-e-handel i Commerce Headquarters.

1. Gå til **Arbejdsområder \> Funktionsstyring**.
1. Filtrer i feltet **Modul** på fanen **Alle** ved hjælp af termen **Detail og handel**.
1. Find og vælg den funktion, der hedder **Aktiver brugen af B2B-eCommerce-egenskaber**, og vælg derefter **Aktivér nu**.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Oprette en nummerserie og føje den til delte parametre for handel

Talserier bruges til generering af læselige, entydige identifikatorer for masterdataposter og transaktionsposter, der kræver identifikatorer. Du kan finde flere oplysninger om nummerserier i [Oversigt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Hvis du vil oprette en nummerserie og føje den til delte parametre for handel i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Headquarters-opsætning \> Nummerserier \> Nummerserier**, og opret en nummerserie.
1. Gå til **Retail og Commerce \> Headquarters-opsætning \> Parametre \> Commerce-delte parametre**, og tilføj ny nummerserie til referencen for **Kundehierarki-id**.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Konfigurere administratorbrugeren til en ny forretningspartner

Potentielle forretningspartnere kan igangsætte processen til start på et B2B-e-handelswebsted ved at sende en anmodning om, at de kan modtage dem, via et link på webstedet. Når en potentiel forretningspartnerbruger har valgt linket, kan de angive de detaljer, der kræves til start og tilmelding. Når anmodningen er sendt, vises siden med bekræftelse af afsendelse. Hvis afsendelsen godkendes, bliver anmoderen (dvs. den bruger, der startede anmodningen om onboarding) brugeren som administrator af forretningspartneren.

Hvis du vil godkende og oprette en administratorbruger i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Detail og handel-it \> Distributionsplan**.
1. Kør **P-0001**-jobbet for at trække alle forretningspartneranmodninger til Commerce Headquarters.
1. Når **P-0001**-jobbet er kørt korrekt, skal du gå til **Retail og Commerce IT \> Kunde**, og køre jobbet **Synkroniseringen af kunder og forretningspartnere fra async-tilstand**. Når jobbet er kørt korrekt, oprettes anmodningerne om onboarding som kundeemner i Commerce Headquarters. Feltet **Type-id** for disse poster er angivet til **B2B-kundeemne**.
1. Gå til **Kunder \> Alle kundeemner**, og åbn siden kundeemner.
1. Vælg kundeemneposten for den nye forretningspartner for at åbne siden med kundeemnet.
1. Under fanen **Generelt** skal du vælge **Konverter \> Godkend/Afvis** for at godkende eller afvise anmodningen om onboarding. Når der vises en bekræftelsesmeddelelse, skal du bekræfte, at du vil fortsætte med processen og godkende anmodningen. Der sendes derefter en e-mail til anmoderens e-mail-adresse for at bekræfte, at deres organisation er blevet godkendt som forretningspartner.

    Når du har godkendt anmodningen, angives feltet **Status** for kundeemneposten til **Godkendt**. Desuden oprettes der to nye kundeposter i systemet: en kundepost af typen **Organisation** for partnerorganisationen for forretningspartneren og en kundepost af typen **Person** for anmoderen. Der oprettes også en post for debitorhierarkiet for forretningspartneren. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. Gå til **Retail og Commerce IT \> Distributionsplan**, og kør jobbet **1010** (**Kunder**) for at flytte de nyoprettede debitor- og debitorhierarkiposter til kanaldatabasen.

Når anmodningen er godkendt, og debitor- og debitorhierarkiposterne synkroniseres til kanaldatabasen, kan anmoderen logge på webstedet for B2B-e-commerce ved hjælp af den e-mail-adresse, de har angivet, da de sendte anmodningen. Brugere kan bruge tilmeldingsflowet til at definere adgangskoden til deres konto. Hvis du vil muliggøre, at id-udbyderen (Azure AD B2C-post) kan knyttes til B2B-kundeposten, der blev oprettet ved tilmelding eller logon, skal du følge instruktionerne i [Aktivere automatisk sammenkædning af identitetsposter til kundekonti](../identity-record-linking.md).

## <a name="onboard-additional-business-partner-users"></a>Få flere forretningspartnerbrugere med i gang

Forretningspartneradministratoren kan efter behov få yderligere forretningspartnerbrugere med til webstedet for B2B-e-handel.

Hvis du vil have flere forretningspartnerbrugere med på et B2B-e-handelswebsted, skal du følge disse trin.

1. Log på B2B-e-handelswebstedet som administrator.
1. Gå til **Min konto \> Organisationsbrugere \> Vis oplysninger**, og vælg **Tilføj bruger**.
1. Angiv de nødvendige oplysninger, og klik derefter på **Gem**. Status for den nye bruger er **Afventer**.

    Når **P-0001** og **Synkroniser kunder og forretningspartnere fra job i async-tilstand** er kørt, oprettes der en kundepost af **Persontype** for den nye bruger i Commerce Headquarters. Denne kundepost er også knyttet til den relevante forretningspartners kundehierarkipost. Desuden sendes der en e-mail til den nye brugers e-mail-adresse for at give dem besked om, at de er blevet tilføjet som bruger af forretningspartnerorganisationen og nu kan logge på B2B-e-commerce-webstedet.

1. Kør jobbet **1010** (**Kunder**) for at synkronisere den nye forretningspartnerbruger med kanaldatabasen.

Når kundeposten er synkroniseret, angives status for brugeren på B2B-e-handelswebstedet til **Aktiv**, og den nye bruger kan logge på webstedet for B2B-e-handel ved hjælp af deres e-mailadresse. Brugere kan bruge tilmeldingsflowet til at definere adgangskoden til deres konto. Hvis du vil muliggøre, at id-udbyderen (Azure AD B2C-post) kan knyttes til B2B-kundeposten, der blev oprettet ved tilmelding eller logon, skal du følge instruktionerne i [Aktivere automatisk sammenkædning af identitetsposter til kundekonti](../identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Redigere brugeroplysninger for forretningspartner

Hvis du vil redigere detaljerne for forretningspartnerbrugere, skal du følge disse trin.

1. Log på B2B-e-handelswebstedet som administrator.
1. Gå til **Min konto \> Organisationsbrugere \> Vis detaljer**, vælg knappen **Rediger** (blyantssymbol), foretag de nødvendige ændringer, og vælg derefter **Gem**. Ændringerne træder først i kraft, når **P-0001**, **Synkroniser kunder og forretningspartnere fra async-tilstand**, og der er kørt **1010** (**Kunder**)-jobs.

## <a name="remove-a-business-partner-user"></a>Fjerne en forretningspartnerbruger

Efter behov kan en administrator fjerne eksisterende brugere af en forretningspartnerorganisation fra listen over brugere, der kan få adgang til B2B-e-handelswebstedet.

Hvis du vil fjerne en forretningspartnerbruger, skal du følge disse trin.

1. Log på B2B-e-handelswebstedet som administrator.
1. Gå til **Min konto \> Organisationsbrugere \> Vis oplysninger**, og vælg knappen **Fjern** ("X"-symbol). Når der vises en bekræftelsesmeddelelse, skal du bekræfte, at du vil fjerne brugeren. Ændringerne træder først i kraft, når **P-0001**, **Synkroniser kunder og forretningspartnere fra async-tilstand** og **1010** (**Kunder**)-jobs er kørt.

> [!NOTE]
> Når du fjerner en bruger fra listen over brugere, der har adgang til B2B-e-handelswebstedet, fjernes den tilsvarende debitorpost fra forretningspartnerens debitorhierarkipost. Selve kundeposten er dog ikke slettet fra Commerce Headquarters.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Få forretningspartner og -brugere med i Commerce Headquarters

Administratorer kan få forretningspartnere og brugere direkte i Commerce Headquarters.

Følg disse trin for at administratorer kan få forretningspartnere og brugere direkte i Commerce Headquarters.

1. Opret en kundepost af typen **Organisation** for forretningspartnerorganisationen.
1. Opret kundeposter af typen **Person** for forretningspartnerbrugere. Kontroller, at der er angivet en primær e-mail-adresse for hver kunde.
1. For hver kundepost af typen **Person**, der skal udpeges som administratorbruger af organisationen for forretningspartneren, skal du angive indstillingen **B2B-administrator** til **Ja** i oversigtspanelet **Retail**.
1. Opret et debitorhierarki-id. Indtast et navn i feltet **Navn**.
1. Angiv en kunde i forretningspartnerorganisationen i feltet **Organisation**.
1. Vælg **Tilføj**, og vælg derefter en kunde i feltet **Navn**.
1. Gentag denne proces for at føje flere kunder til hierarkiet.

## <a name="additional-information"></a>Flere oplysninger

- Alle de job, der nævnes i dette emne, kan konfigureres til at køre efter en plan i et batchformat. Det ønskes, at forretningspartnere vil konfigurere batchjob efter behov.
- I øjeblikket kan der kun udpeges én bruger-/kundepost som administratorbruger, og denne rolle kan kun ændres i Commerce Headquarters. Der er ingen understøttelse af selvbetjeningsfunktioner, der giver forretningspartnere mulighed for at udpege flere administratorer eller ændre administratorer fra B2B-e-handelswebsteder.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Selvom forbrugsgrænser kan defineres for brugerne, er håndhævelsen af forbrugsgrænser i løbet af ordreindtastningsprocessen endnu ikke implementeret.
- Al forretningslogik og -validering for en brugers erfaring med et B2B-e-handelswebsted er baseret på konfigurationen af den kundepost, der er knyttet til brugeren i Commerce Headquarters.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere et B2B-e-handelswebsted](set-up-b2b-site.md)

[Oprette organisationsmodelhierarkier for B2B-organisationer](org-model.md)

[Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder](payment-method.md)

[Angive produktantalsgrænser for B2B-e-handelswebsteder](quantity-limits.md)

[Oversigt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
