---
title: "Indkøbspolitikker"
description: "Denne artikel indeholder oplysninger om indkøbspolitikker. En indkøbspolitik er en samling af regler, der styrer rekvisitionsprocessen. Indkøbspolitikker er en hjælp for indkøbsadministratorer, der skal implementere indkøbsstrategier, da de udgør en politikstruktur, der tilpasses organisationens strategiske indkøbsbehov."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 11614
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5208dc64d86345de4e53c5e293fbc861351a63ef
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="purchasing-policies"></a>Indkøbspolitikker

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om indkøbspolitikker. En indkøbspolitik er en samling af regler, der styrer rekvisitionsprocessen. Indkøbspolitikker er en hjælp for indkøbsadministratorer, der skal implementere indkøbsstrategier, da de udgør en politikstruktur, der tilpasses organisationens strategiske indkøbsbehov.

En indkøbspolitik består af et sæt af politikregler. Når du definerer en politikregel, skal du først vælge en regeltype. Du skal derefter oprette en regel for regeltypen ved at definere indstillingerne, startdatoen og slutdatoen for reglen.  

En administrator opretter f.eks. en politik, vælger regeltypen **Katalogpolitik** og tilføjer derefter en katalogpolitikregel til politikken. Denne katalogpolitikregel angiver, at kataloget Adventure skal bruges til interne indkøb. Når indkøbspolitikken er blevet knyttet til en bestemt organisation, kan medarbejdere i den pågældende organisation se kataloget Adventure, når de opretter rekvisitioner.

## <a name="assigning-policies-to-organizations"></a>Tildeling af politikker til organisationer
Før en politik kan træde i kraft, skal den være knyttet til en organisation. Indkøbspolitikker er tilknyttet hierarkiformålet **Intern kontrol af indkøb**. Dette betyder derfor, at indkøbspolitikker kun kan gælde for organisationer i hierarkier, der har hierarkiformålet **Intern kontrol af indkøb**. Du kan også vælge organisationer fra den flade liste med juridiske enheder i tabellen CompanyInfo. Disse juridiske enheder udpeges i politikstrukturen som "Firmaer".

## <a name="determining-which-rule-to-apply"></a>Bestemme, hvilken regel der skal anvendes
Afhængigt af, hvordan du konfigurerer indkøbspolitikkerne, kan flere regler påvirke brugerne i en organisation. Følgende eksempler illustrerer forskellige måder at konfigurere indkøbspolitikker på og angiver, hvordan politikker anvendes, når der forekommer posteringer.

### <a name="example-1-simple-purchasing-policy-configuration"></a>Eksempel 1: Simpel konfiguration af indkøbspolitik

Organisationer, der er små og mindre komplicerede, kan konfigurere indkøbspolitikker efter juridisk enhed og kan kun bruge organisationshierarkiet Firmaer.  

Fabrikam, der er en lille virksomhed, har kun en beskeden afvigelse i indkøbsbehovet i hele organisationen. Indkøbsregler varierer kun mellem organisationens juridiske enheder. Medarbejdere hos Fabrikam Canada og medarbejdere hos Fabrikam USA køber f.eks. varer og tjenesteydelser fra forskellige kataloger og hos forskellige kreditorer. Fabrikam konfigurerer derfor sine indkøbspolitikker på niveauet for juridiske enheder.  

Fabrikam opretter to indkøbspolitikker. Politik A gælder for den amerikanske juridiske enhed 1111. Politik B gælder for den canadiske juridiske enhed 2222. Når en medarbejder i den juridiske enhed 1111 opretter en indkøbsrekvisition, afledes politikreglerne af politik A. For eksempel er det produktkatalog, som medarbejderen kan se, angivet i katalogpolitikreglen for politik A.  

Når en medarbejder i juridisk enhed 2222 opretter en indkøbsrekvisition, afledes politikreglerne af politik B.  

**Bemærk:** Hvis en medarbejder hos juridisk enhed 1111 køber en vare på vegne af en medarbejder hos juridisk enhed 2222, anvendes de politikregler, der er angivet for juridisk enhed 2222, dvs. politik B.

### <a name="example-2-complex-purchasing-policy-configuration"></a>Eksempel 2: Avanceret konfiguration af indkøbspolitik

I det foregående eksempel blev alle indkøbsregler defineret i et enkelt organisationshierarki, i dette tilfælde organisationshierarkiet Firmaer. En kompliceret organisation kan dog definere politikker for flere organisationshierarkier.  


Contoso er et stort firma, der kræver komplicerede indkøbsregler til styring af rekvisitionsprocessen. Contoso har defineret regler for to forskellige organisationshierarkier: Afdeling og Global indkøbsstyring.  

Politik 123 er defineret for organisationshierarkiet Afdeling for salgsafdelingen Salg UK. I politik 123 angiver reglen Styring af indkøbsrekvisitioner, at begrænsninger i minimale ordremængder skal overholdes. I denne regel er indstillingen **Gennemtving minimumbegrænsninger for ordreantal** valgt.  

Politik 456 er defineret for organisationshierarkiet Global indkøbsstyring for salgs- og marketingafdelingen. I politik 456 angiver reglen Styring af indkøbsrekvisitioner ikke, at begrænsninger for minimale ordremængder skal overholdes. I denne regel er indstillingen **Gennemtving minimumbegrænsninger for ordreantal** ikke markeret.  

Sam arbejder i salgsafdelingen Salg UK i Contosos kontor i Storbritannien. Politikkerne for organisationshierarkierne Afdeling og Global indkøbsstyring gælder begge for denne afdeling. Når Sam opretter en indkøbsrekvisition, skal systemet bestemme, hvilken politik der skal anvendes. Systemadministratoren konfigurerer parametrene for indkøbspolitikker for at angive at indkøbspolitikker skal anvendes i følgende prioriterede rækkefølge.

1.  Global indkøbsstyring
2.  Afdeling
3.  Firmaer

Derfor anvendes politik 456 til indkøbsrekvisitionen, som Sam opretter, og der kræves ingen minimummængde for indkøbsrekvisitionen.

## <a name="policy-rules"></a>Politikregler
### <a name="catalog-policy-rule"></a>Katalogpolitikregel

Katalogpolitikreglen bestemmer, hvilket indkøbskatalog, som brugerne ser, når de opretter indkøbsrekvisitioner. Hvis en bruger har fået tildelt rettighed til at bestille produkter på vegne af en anden bruger, bruger rekvisitionen den katalogpolitikregel, som er defineret for anmoderens juridiske enhed og driftsenhed, til at afgøre, hvilket katalog der skal vises. Før du kan definere en katalogpolitikregel, skal du oprette og publicere et indkøbskatalog.

### <a name="category-access-policy-rule"></a>Politikregel for adgang til kategori

Kategoriadgangspolitikreglen bestemmer, hvilke kategorier brugere har adgang til, når de opretter indkøbsrekvisitioner. Hvis der ikke angives nogen regler, kan alle indkøbskategorier føjes til indkøbsrekvisitionen.

1.  Markér indstillingen **Medtag overordnet regel** for at anvende kategoriadgangspolitikreglen for den overordnede organisation på kategorien.
2.  I ruden **Tilgængelige kategorier** skal du vælge de kategorier, som reglen gælder for. Når du vælger en kategori, føjes alle de kategorier, der er højere i hierarkiet, også til listen **Valgte kategorier**.
3.  Markér indstillingen **Medtag underkategorier** for at anvende reglen på alle underkategorier af den valgte kategori.

### <a name="category-policy-rule"></a>Politikregel for kategori

Kategoripolitikreglen definerer, hvordan brugerne kan vælge kreditorer for hver kategori. Den definerer også kravene til tilgangs- og faktureringsprocesserne.

### <a name="re-approval-rule-for-purchase-orders"></a>Gengodkendelsesregel for indkøbsordrer

Reglen for gengodkendelse er en valgfri regel, der definerer kriterierne for at kræve gengodkendelse, hvis der foretages ændringer i en indkøbsordre. De valgte felter evalueres i arbejdsgangen for indkøbsordrer, hvis betingelsen "Kræver gengodkendelse af indkøbsordre" konfigureres i arbejdsgangen.

> [!NOTE]
> Regnskabsfordelingen nulstilles altid, når en godkendt købsordre med ændringsstyring aktiveret ændres. Så du skal være opmærksom på, om du vil undgå en fornyet godkendelse af en indkøbsordre, når visse felter ændres, feltet Regnskabsfordeling må IKKE medtages som et valgt felt til fornyet godkendelse. 

### <a name="purchase-requisition-rfq-rule"></a>Regler for tilbudsanmodning ved indkøbsrekvisition

Reglen for tilbudsanmodning ved indkøbsrekvisition definerer kriterierne for at kræve en tilbudsanmodning for en indkøbsrekvisitionslinje. Hvis en linje opfylder betingelserne, vises stemplet "uformel tilbudsanmodning" eller "formel tilbudsanmodning" på rekvisitionslinjen.

### <a name="purchase-requisition-control-rule"></a>Regel for styring af indkøbsrekvisition

Kontrolreglen for indkøbsrekvisition er en valgfri regel. Når du opretter regler af denne type, kan du angive indstillinger under forskellige faner:

-   På fanen **Afsendelse af arbejdsgang** kan du konfigurere de felter, der skal udfyldes på rekvisitionslinjen for, at rekvisitionen kan blive sendt til godkendelse, når rekvisitionsformålet **Forbrug**.
-   På fanen **Ordreantal** kan du konfigurere de felter, der kræves på indkøbsrekvisitionen under visse betingelser. Du kan også gennemtvinge ordreantal.
-   På fanen **Datoer** kan du konfigurere, om regnskabsdatoen er den samme som den ønskede dato
-   På fanen **Adresse** kan du angive, om brugeren har rettighed til at oprette nye adresser i systemet, der skal gælde for indkøbsrekvisitionen.

### <a name="requisition-purpose-rule"></a>Regel for rekvisitionsformål

Reglen for rekvisitionsformål er en valgfri regel, der bestemmer typen af rekvisitionsformål, der er tilladt for en bestemt juridisk enhed. Medmindre et andet formål er angivet i denne regel, har rekvisitioner automatisk et formål med **Forbrug**, når de oprettes.

### <a name="replenishment-category-access-policy-rule"></a>Politikregel for adgang til genopfyldningskategori

Reglen for adgang til genopfyldningskategori er en valgfri regel, der bestemmer, hvilke produkter der er tilgængelige til opfyldelse af rekvisitionsbehov for en bestemt juridisk enhed, når rekvisitionsformålet er **Genopfyldning**.

### <a name="replenishment-control-rule"></a>Kontrolregel for genopfyldning

Kontrolreglen for genopfyldning er en valgfri regel, der definerer felterne på rekvisitionslinjen, der skal udfyldes, for at rekvisitionen kan blive sendt til godkendelse, når rekvisitionsformålet er **Genopfyldning**.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Regel for oprettelse af indkøbsordrer og konsolidering af efterspørgsel

Reglen for oprettelse af indkøbsordre og efterspørgselskonsolidering definerer de politikregler, der skal bruges, når der oprettes en indkøbsordre ud fra en godkendt indkøbsrekvisition. Når du opretter regler af denne type, kan du angive indstillinger under forskellige faner:

-   På fanen **Opdeling af indkøbsordre** kan du definere kriterier for, hvornår indkøbsrekvisitionslinjer skal opdeles i separate indkøbsordrer.
-   På fanen **Pris-/rabatoverførsel** kan du definere, hvornår prisaftalen genberegnes,, når købsordren er oprettet:
    -   **Kun, hvis der ikke er nogen samhandelsaftale** – priser og rabatter overføres kun fra indkøbsrekvisitionen, hvis der ikke er nogen gældende samhandelsaftale eller basispris. Hvis der findes en samhandelsaftale, eller der er en basispris for varen eller kreditoren, skal priserne og rabatterne genberegnes på grundlag af samhandelsaftalen eller basisprisen og anvendes på indkøbsordren. Dette er standardindstillingen, medmindre andet er angivet.
    -   **Altid** – priser og rabatter overføres altid fra indkøbsrekvisitionen.

    Du kan også give anmoderen lov til at ændre metoden for overførsel af pris- og rabatoplysninger for individuelle indkøbsrekvisitionslinjer, uanset den regel der er defineret for pris-/rabatoverførsel. Markér indstillingen **Tillad manuel tilsidesættelse pr. indkøbsrekvisitionslinje**, hvis du vil aktivere denne funktion.
-   På fanen **Overførsel af varebeskrivelse** kan du overføre varebeskrivelsen fra rekvisitionen, når den stammer fra en tilbudsanmodning.
-   På fanen **Pristolerance** kan du definere regler for at dirigere godkendte indkøbsrekvisitioner tilbage gennem evalueringsprocessen, når prisen på en indkøbskatalogvare stiger. Angiv det maksimale beløb som nettobeløbet på et linjeelement i en indkøbsrekvisition kan stige mellem det tidspunkt, hvor indkøbsrekvisitionen godkendes, og det tidspunkt, hvor indkøbsrekvisitionen oprettes. Nettobeløbet beregnes ved hjælp af følgende formel: (\[Mængde × (enhedspris – rabat) ÷ prisenhed\] + indkøbstillæg) × (100 – rabatprocent) ÷ 100 indkøbsrekvisitionslinjer, der overstiger den pristolerance, som du har angivet er tilbageholdt for manuel behandling. De regler, som du konfigurerer under fanen **Fejlbehandling**, bestemmer, hvordan indkøbsrekvisitionslinjerne behandles.
-   På fanen **Fejlbehandling** kan du konfigurere den behandlingsregel, der gælder for en indkøbsrekvisition, hvis den ikke godkendes under oprettelsen af indkøbsordren pga. en kreditorfejl eller en pristolerancefejl. Vælg en af følgende indstillinger:
    -   **Ingen handling** – Indkøbsrekvisitionslinjer forbliver på siden **Frigiv godkendte indkøbsrekvisitioner**. Statussen for indkøbsrekvisitionslinjerne forbliver **Godkendt**. Fejlene skal dog afklares, før der kan genereres en indkøbsordre for indkøbsrekvisitionslinjerne.
    -   **Annuller indkøbsrekvisitionslinjen** – Indkøbsrekvisitionslinjerne annulleres. Anmoderen kan oprette en ny indkøbsrekvisition for de annullerede linjer, hvis vedkommende stadig ønsker at anmode om linjeelementerne.
    -   **Opret en ny indkøbsrekvisitionslinje** – Indkøbsrekvisitionslinjerne annulleres. Der genereres derefter nye indkøbsrekvisitioner, der kun indeholder de indkøbsrekvisitionslinjer, der ikke blev godkendt. De nye indkøbsrekvisitioner, der genereres, har statussen **Kladde**. Disse indkøbsrekvisitioner kan sendes til evaluering igen, når valideringsfejlene er afklaret. Klargøreren af indkøbsrekvisitionslinjerne underrettes om, at linjerne blev annulleret, og at der er genereret nye indkøbsrekvisitioner for de mislykkede indkøbsrekvisitionslinjer.
-   På fanen **Manuel oprettelse af indkøbsordre** kan du definere de parametre, der bestemmer om en indkøbsrekvisition skal behandles manuelt, eller om den automatisk kan konverteres til en indkøbsordre. Parametrene kan gælde for interne katalogvarer, eksterne katalogvarer eller varer uden for katalog. Vælg en af følgende indstillinger:
    -   **Opret indkøbsordrer manuelt** – Opret manuelt indkøbsordrer for alle indkøbsrekvisitioner.
    -   **Opret automatisk indkøbsordrer** – Opret automatisk indkøbsordrer for alle godkendte indkøbsrekvisitioner. Der gemmes ingen indkøbsrekvisitioner ved manuel oprettelse af indkøbsordre.
    -   **Opret indkøbsordrer automatisk, dog ikke på disse betingelser** – Manuelt opret indkøbsordrer for indkøbsrekvisitioner, der svarer til de kriterier, du definerer. Alle andre godkendte indkøbsrekvisitioner konverteres automatisk til indkøbsordrer. Hvis du vælger **Opret indkøbsordrer automatisk, dog ikke på disse betingelser**, kan du tilføje indkøbskategorier og kreditorer for at angive, hvilke godkendte indkøbsrekvisitionslinjer, der gemmes til manuel behandling. Denne indstilling kan gælde for interne katalogvarer, eksterne katalogvarer og varer uden for katalog. Når du vælger en indkøbskategori, vælges også evt. underkategorier, der er defineret til den pågældende indkøbskategori. Vælg indstillingen **Alle** for en bestemt type indkøbsrekvisitionslinje for at gemme alle linjerne til manuel behandling for den pågældende linjetype.

    Hvis indkøbsordrer skal genereres automatisk fra godkendte indkøbsrekvisitioner, når batchjobbet til oprettelse af indkøbsordrer køres, skal du vælge indstillingen **Kør automatisk oprettelse af indkøbsordrer som batchjob**. Denne indstilling gælder kun for indkøbsrekvisitioner, der ikke kræver manuel behandling. Ved at køre den automatiske generering af indkøbsordrer som et batchjob kan du planlægge denne aktivitet til et tidspunkt, hvor ressourcerne ikke er så begrænsede. Hvis indstillingen **Forudbetaling påkrævet** markeres på indkøbsrekvisitionslinjernes, skal du markere indstillingen **Når rekvisitionen er konfigureret til forudbetaling** for at holde godkendte indkøbsrekvisitioner til manuel behandling. Indkøbsrekvisitioner, der gemmes til manuel behandling, kan filtreres, så der kun vises de indkøbsrekvisitionslinjer, der kræver forudbetaling.
-   På fanen **Efterspørgselskonsolidering** kan du definere de parametre, der bestemmer, om indkøbsrekvisitioner, der er behandlet manuelt, kan overvejes til konsolidering af indkøbsrekvisitioner. Parametrene kan gælde for interne katalogvarer, eksterne katalogvarer eller varer uden for katalog. Vælg en af følgende indstillinger:
    -   **Tillad ikke efterspørgselskonsolidering** – Ingen godkendte indkøbsrekvisitionslinjer er berettiget til efterspørgselskonsolidering. Denne indstilling vælges som standard og gælder kun for de indkøbsrekvisitionslinjer, der kræver manuel behandling til oprettelse af indkøbsordrer.
    -   **Tillad altid efterspørgselskonsolidering** – Alle godkendte indkøbsrekvisitionslinjer er berettiget til efterspørgselskonsolidering. **Bemærk:** Hvis du vælger indstillingen **Tillad altid efterspørgselskonsolidering** på fanen **Efterspørgselskonsolidering**, men du vælger indstillingen **Opret automatisk indkøbsordrer** på fanen **Manuel oprettelse af indkøbsordre**, holdes alle indkøbsrekvisitioner til manuel behandling.
    -   **Tillad efterspørgselskonsolidering på disse betingelser** – Definer de kriterier, der bestemmer om godkendte indkøbsrekvisitionslinjer er berettiget til efterspørgselskonsolidering. Du kan angive kriterierne efter indkøbskategori og leverandør for hver type indkøbsrekvisitionslinje. Hvis du vælger **Tillad efterspørgselskonsolidering på disse betingelser**, kan du angive kriterierne efter indkøbskategori og kreditor for hver type indkøbsrekvisitionslinje. Når du vælger en indkøbskategori, vælges også evt. underkategorier, der er defineret til den pågældende indkøbskategori. Hvis du vælger indstillingen **Alle** for en bestemt linjetype, er alle indkøbsrekvisitionslinjer for den pågældende linjetype tilgængelige til efterspørgselskonsolidering.





