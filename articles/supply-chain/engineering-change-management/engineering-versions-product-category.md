---
title: Tekniske versioner og tekniske produktkategorier
description: Dette emne giver oplysninger om begrebet tekniske versioner. Tekniske versioner sikrer, at forskellige tilstande af et produkt og dets data holdes opdaterede og tydelige, og at de kan visualiseres i systemet.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42faa9e5f073d718c18422e37212c2ae8a28b28d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572883"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Tekniske versioner og tekniske produktkategorier

[!include [banner](../includes/banner.md)]

Tekniske produkter udvikler sig i løbet af deres livscyklus, af mange grunde. Der kan f.eks. blive introduceret ændringer for at forbedre produktets servicevenlighed, udskifte en komponent, fordi leverandøren ikke længere tilbyder den, reagere på nye indsigter eller rette fejl i det indledende design. Der er også mange årsager til, at disse ændringer skal gemmes som en del af et igangværende produkt, på en sådan måde, at tidligere data ikke overskrives. Her er nogle af disse årsager:

- Du vil holde styr på produktet, som det blev fremstillet og leveret til dine kunder i tidligere livscyklustilstande.
- Du skal bruge en gennemløbstid, før du kan godkende og anvende ændringerne.
- Du skal have et tidsstempel på hver ændring, og du vil kunne levere tidligere fremstillede produkter separat fra hinanden.

*Tekniske versioner* sikrer, at forskellige tilstande af et produkt og dets data holdes opdaterede og tydelige, og at de kan visualiseres i systemet. Dette begreb hjælper dig med at bevare konsistensen, nedlukke styklisterne for produktion, eliminere variabilitet og nemt identificere ændringer.

Generelt set anvendes reglerne for *form, tilpasning og funktion* for at bestemme, om en ændring kræver et nyt produkt, en ny version eller en opdatering til en eksisterende version. Hvert af de tre udtryk i navnet på denne regel refererer til et specifikt aspekt af en del, som hjælper teknikerne med at matche dele med behov. Reglen for form, tilpasning og funktion øger fleksibiliteten i designændringer, da det er nødvendigt med minimal dokumentation og designomkostning for at ændre en del, hvis form, tilpasning og funktion af produktet bevares.

- **Tilpas** refererer til delens eller funktionens mulighed for at blive tilsluttet, matchet eller sammensat med en anden funktion eller del i en assembly. Funktionen Tilpas giver delen mulighed for at overholde de påkrævede assembly-tolerancer, så den kan være nyttig.
- **Form** henviser til karakteristika for en del eller en assembly, f.eks. eksterne dimensioner, vægt, størrelse og det visuelle udtryk. Formen er det aspekt, der påvirkes mest af en teknikers æstetiske valg. Den omfatter kabinettet, chassiset og kontrolpanelet, der bliver den udadvendte "flade" af produktet.
- **Funktion** er et kriterium, der overholdes, når delen effektivt og pålideligt udfører dens tilsigtede formål. I et elektronikprodukt kan funktionen f.eks. være afhængig af de faste komponenter, der bruges, og software eller firmware. Ofte kan den også afhænge af funktionerne i det valgte kabinet. To af de mest almindelige årsager til, at et kabinet ikke opfylder funktionskriteriet, er porte med dårlig placering eller størrelse, samt vildledende eller manglende etikettering. 

## <a name="engineering-versions"></a>Tekniske versioner

Når du bruger tekniske produkter, har hvert produkt mindst én teknisk version. Den første tekniske version oprettes automatisk, når du opretter et teknisk produkt. Hver enkelt tekniske version gemmer de teknisk relevante data, der er specifikke for den pågældende version. Her er nogle eksempler på disse data:

- Versionsnummeret og det tidligere versionsnummer (hvis relevant)
- Ikrafttrædelsesdato og sidste holdbarhedsdato
- Produktversionens aktivstatus, der angiver, om versionen kan frigives og bruges i transaktioner (yderligere oplysninger finder du i [Produktets parathed](product-readiness.md)).
- Det tekniske firma, der har oprettet og ejer produktet (yderligere oplysninger finder du i [Tekniske virksomheder og regler for ejerskab af data](engineering-org-data-ownership-rules.md)).
- Relaterede tekniske dokumenter, f.eks. en monteringsmanual, brugervejledninger, billeder og links
- De tekniske attributter (Yderligere oplysninger finder du i [Tekniske attributter og søgning efter tekniske attributter](engineering-attributes-and-search.md)).
- Stykliste for tekniske produkter
- Formler for produkter i procesproduktion
- De tekniske ruter

Du kan opdatere disse data i en eksisterende version eller oprette en ny version ved at bruge en *teknisk ændringsordre*. (Yderligere oplysninger finder du i [Administrere ændringer af tekniske produkter](engineering-change-management.md)). Hvis du opretter en ny version af et produkt, kopierer systemet alle teknisk relevante data til den nye version. Du kan derefter redigere dataene for den nye version. På denne måde kan du spore bestemte data for hver fortløbende version. Hvis du vil sammenligne forskellene mellem på hinanden følgende tekniske versioner, skal du undersøge den tekniske ændringsordre, som indeholder ændringstyper, der angiver alle ændringer.

Som nævnt, oprettes den første tekniske version automatisk, når du opretter et teknisk produkt. Versionsnummeret for denne version følger den versionsnummerregel, der er defineret i produktets tekniske kategori. Hvis du vil overgå til en efterfølgende version, skal du føje produktet til en teknisk ændringsordre som en linje, og du skal indstille feltet **Virkning** til *Ny version*. Den tekniske ændringsordre indeholder oplysninger om ændringen fra den aktuelle version til næste version.

Bemærk, at et teknisk produkt kun kan være i én teknisk ændringsordre ad gangen. Denne begrænsning sikrer datanøjagtighed og hjælper med at undgå overlappende eller modstridende ændringer i produktet. Bemærk også, at feltet **Tekniker** i **Overskrift**-visningen af den tekniske ændringsordre vises den tekniker, der er ansvarlig for ændringsordren. Hvis teknikeren tilhører team, der er defineret i systemet, viser feltet **Ansvarlig** lederen af det pågældende team.

## <a name="track-versions-in-transactions"></a>Spore versioner i transaktioner

Når du bruger teknisk ændringsstyring, indeholder produktmasterdataene altid en eller flere tekniske versioner. I opsætningen af tekniske produkter kan du vælge, om den tekniske version også er en del af *logistiske transaktioner*. (Yderligere oplysninger finder du i afsnittet [Konfigurer tekniske produktkategorier](#product-category) senere i dette emne). Hvis logistikeffekten er relevant, varierer den pr. produkt og pr. firma. Nogle gange bruges kun den nyeste version af et produkt. Derfor kan den tidligere version ikke længere bruges, når du introducerer en ny version. I andre tilfælde kræves den tidligere version i logistiske transaktioner for at overvinde følgende udfordringer:

- Logistikafdelingen skal levere to stykker af et produkt til en kunde. I dette tilfælde skal du beslutte, om du ønsker eller vil tillade, at to forskellige versioner afsendes.
- Det opdages senere, at der opstår et problem, og at det er knyttet til en bestemt ændring. I dette tilfælde kan det være en fordel at bestemme, nøjagtigt hvilken version der er afsendt i hver ordre.
- Virksomheder vil typisk levere gamle versioner først, så de udgår fra lageret. Denne tilgang, der er specielt beregnet til produkter med lav volumen, kan ofte administreres ved at fastlægge gyldighedsdatoer for den nye version i forhold til forudsigelser om, hvornår lageret af den gamle version vil blive udtømt. I nogle tilfælde kan du måske ikke foretage denne sammenligning, eller du kan vurdere, at usikkerheden ved forudsigelser af lagerbeholdning er for høj.

Beslutningen om, hvorvidt versioner skal være synlige på lageret, afhænger af faktorer som f.eks. dem, der tidligere er nævnt, plus firmapraksis og andre overvejelser, der er specifikke for de enkelte firmaer. Du kan angive funktionaliteten for den *tekniske produktkategori*. Den gælder derefter for alle produkter, der er oprettet ud fra den pågældende kategori, for alle firmaer, som produktet frigives til.

For produkter, der er konfigureret, så de har en logistisk indflydelse, skal den tekniske version angives på de enkelte transaktioner. Selvom systemet vil foreslå den *seneste aktive version*, kan du vælge mellem alle de aktive versioner, der er tilgængelige for firmaet. For produkter, der er konfigureret, så de ikke har en logistisk indflydelse, skal den tekniske version ikke angives på transaktioner. Systemet bruger imidlertid den seneste aktive version. Når du f.eks. føjer et produkt til en produktionsstykliste, bruges den seneste version, og når du kører varedisponering, vil den seneste version blive antaget.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Konfigurere tekniske produktkategorier

En teknisk produktkategori er basis for oprettelse af et bestemt teknisk produkt. Hver kategori fastlægger et sæt standardværdier og -politikker. Når du opretter et teknisk produkt, skal du derfor først vælge den kategori, det skal oprettes ud fra.

Bemærk, at der automatisk oprettes en ny kategorihierarkitype (*teknisk produkthierarki*) for dig. Du kan oprette kategorierne manuelt ved at gå til **Teknisk ændringsstyring \> Konfiguration \> Detaljer om teknisk produktkategori**.

De enkelte tekniske produktkategorier fastsætter standardfunktionaliteten for de tekniske produkter, der oprettes ud fra den pågældende kategori. Når du har oprettet et teknisk produkt, kan du ikke ændre dets tekniske produktkategori. Men hvis du vælger den forkerte kategori, kan du slette produktet og derefter oprette det igen.

Når der oprettes en teknisk produktkategori, kan du ikke ændre følgende indstillinger:

- Teknisk virksomhed
- Produkttype
- Produktundertype
- Produktdimensionsgruppe
- Konfigurationsteknologi
- Regel for versionsnummer

Andre indstillinger arver muligvis standardværdier, der er konfigureret for den tekniske produktkategori. I henhold til systemreglerne kan disse værdier dog ændres.

Du kan arbejde med tekniske produktkategorier ved at gå til **Teknisk ændringsstyring \> Konfiguration \> Detaljer om teknisk produktkategori**. Udfør derefter ét af følgende trin.

- Hvis du vil oprette en ny kategori, skal du vælge **Nyt** i handlingsruden og derefter angive felterne som beskrevet i følgende underafsnit.
- Hvis du vil redigere en eksisterende kategori, skal du vælge den i listeruden, vælge **Rediger** i handlingsruden og derefter angive felterne som beskrevet i følgende underafsnit.
- Hvis du vil slette en eksisterende kategori, skal du vælge den i listeruden og derefter vælge **Slet** i handlingsruden.

### <a name="header"></a>Overordnet

Angiv følgende felter i overskriften på en teknisk produktkategori.

| Felt | Beskrivelse |
|---|---|
| Navn | Angiv et navn til den tekniske produktkategori. |
| Teknisk virksomhed | Vælg den tekniske virksomhed, hvor produkter i denne tekniske produktkategori kan oprettes, og hvor de skal vedligeholdes. |

### <a name="details-fasttab"></a>Oversigtspanelet Detaljer

Angiv følgende felter i oversigtspanelet **Detaljer** på en teknisk produktkategori.

| Felt | Beskrivelse |
|---|---|
| Produkttype | Vælg, om kategorien gælder for produkter eller tjenester. |
| Produktionstype | Dette felt vises kun, når du har aktiveret [administration af formelændringer](manage-formula-changes.md) i systemet. Vælg den produktionstype, som denne kategori for tekniske produkter gælder for:<ul><li>**Planlægningsvare** – Brug denne tekniske kategori til at administrere formelændringer for planlægningsvarer. Planlægningsvarer bruger formler. De ligner formelvarer, men de bruges kun til at producere samprodukter og biprodukter, ikke færdige produkter. Formler bruges under procesproduktion.</li><li>**Stykliste** – Brug denne tekniske kategori til at administrere tekniske produkter, som ikke bruger formler og typisk (men ikke nødvendigvis) indeholder styklister.</li><li>**Formel** – Brug denne tekniske kategori til at administrere formelændringer for færdige varer. Disse varer har en formel, men ikke en stykliste. Formler bruges under procesproduktion.</li></ul> |
| Fastvægt | Denne indstilling vises kun, når du har aktiveret [administration af formelændringer](manage-formula-changes.md) i systemet. Den er kun tilgængelig, når feltet **Produktionstype** er angivet til *Planlægningsvare* eller *Formel*. Angiv denne indstilling til *Ja*, hvis du vil bruge denne tekniske kategori til at administrere varer, der kræver understøttelse af fastvægt. |
| Spore versioner i transaktioner | Vælg, om produktversionen skal stemples på alle transaktioner (logistisk effekt). Hvis du f.eks. sporer versionen i transaktioner, viser hver salgsordre, hvilken bestemt version af produktet der blev solgt i den pågældende salgsordre. Hvis du ikke sporer versionen i transaktioner, viser salgsordrer ikke, hvilken bestemt version der blev solgt. De viser i stedet altid den seneste version.<ul><li>Hvis denne indstilling er angivet til *Ja*, oprettes en produktmaster for produktet, og hver version af produktet er en variant, der bruger produktdimensionen *version*. Feltet **Produktundertype** angives automatisk til *Produktmaster*, og i feltet **Produktdimensionsgruppe** du skal vælge en produktdimensionsgruppe, hvor dimensionen *version* er aktiv. Kun produktdimensionsgrupper, hvor *version* er en aktiv dimension, vises. Du kan oprette nye produktdimensionsgrupper ved at vælge knappen **Rediger** (blyantssymbolet).</li><li>Hvis denne indstilling er angivet til *Nej*, bruges *version* ikke som produktdimension. Du kan derefter vælge, om du vil oprette et produkt eller en produktmaster, der bruger de andre dimensioner.</li></ul><p>Denne indstilling bruges ofte til produkter, der har en omkostningsdifference mellem versioner, eller produkter, hvor der gælder forskellige betingelser i relation til kunden. Derfor er det vigtigt at angive, hvilken version der er brugt i de enkelte transaktioner.</p> |
| Produktundertype | Vælg, om kategorien skal indeholde produkter eller produktmastere. I forbindelse med produktmastere bruges der produktdimensioner.
| Produktdimensionsgruppe | Med indstillingen **Spor versioner i transaktioner** kan du lettere vælge produktdimensionsgruppen. Hvis du har angivet, at du vil spore versionen i transaktioner, vil de produktdimensionsgrupper, hvor dimensionen *version* bruges, blive vist. Ellers vises kun produktdimensionsgrupper, hvor *version*-dimensionen ikke bruges. |
| Produktets livscyklustilstand ved oprettelse | Konfigurer den standard for produktlivscyklustilstand, som et teknisk produkt skal have, når det først oprettes. Du kan finde flere oplysninger i [Produktlivscyklustilstand og transaktioner](product-lifecycle-state-transactions.md). |
| Regel for versionsnummer | Vælg den versionsnummerregel, som gælder for kategorien.<ul><li>**Manuel** – Du vælger versionsnummeret for hver ny version.</li><li>**Automatisk** – Systemet angiver det versionsnummer, der er baseret på et format, som du definerer. Når du konfigurerer formatet, skal du bruge et nummertegn (\#) til at angive et ciffer og eventuelle andre tegn, der skal repræsentere en konstant værdi. Hvis du f.eks. definerer formatet som *V-\#\#*, vil den første version være "V-01", den anden version vil være "V-02" osv.</li><li>**Liste** – Systemet tager det næste nummer fra en foruddefineret liste over værdier, som du definerer.</li></ul> |
| Gennemtving gyldighedsdato | Vælg, om gyldighedsdatoerne for tekniske versioner skal være sammenhængende, eller om der kan være huller og overlap. Denne indstilling påvirker den måde, som du kan bruge felterne **Gyldig fra** og **Gyldig til** for hver af de tekniske versioner, hvor kategorien gælder.<ul><li>Hvis denne indstilling er angivet til *Ja*, skal der angives en **Gyldig fra**-værdi for hver version, og hverken overlap eller huller er tilladt mellem versioner. Datointervallet for hver enkelt tekniske version er direkte forbundet til de tidligere og næste tekniske versioner, hvis de findes. I dette scenario bruges den nyeste version altid, og ældre versioner bruges ikke længere.</li><li>Hvis denne indstilling er angivet til **Nej**, er der ingen begrænsninger for gyldighedsdatofelterne til tekniske versioner, og både overlap og huller er tilladt. I dette scenario kan flere versioner være aktive på samme tid, og du kan arbejde med en hvilken som helst aktiv version.</li></ul><p>Denne indstilling påvirker også de styklister og ruter, der er tilknyttet en produktversion. Du kan finde flere oplysninger i afsnittet [Oprette forbindelse mellem styklister og ruter til tekniske versioner](#boms-routes) senere i dette emne.</p> |
| Brug nomenklatur for talregel | Angiv denne indstilling til *Ja* for at aktivere regler for definition af et produktnummer ved hjælp af nummerserier, tekniske attributnavne og -værdier samt tekstkonstanter som segmenter. Hvis du vil oprette eller redigere regler, skal du vælge knappen **Rediger**. |
| Brug nomenklatur for navneregel | Angiv denne indstilling til *Ja* for at aktivere regler for definition af et navn ved hjælp af de tekniske attributnavne og -værdier samt tekstkonstanter som segmenter. Hvis du vil oprette eller redigere regler, skal du vælge knappen **Rediger**. |
| Brug nomenklatur for beskrivelsesregel | Angiv denne indstilling til *Ja* for at aktivere regler for definition af beskrivelsen ved hjælp af de tekniske attributnavne og -værdier samt tekstkonstanter som segmenter. Hvis du vil oprette eller redigere regler, skal du vælge knappen **Rediger**. |

### <a name="attributes-fasttab"></a>Oversigtspanelet Attributter

Brug gitteret i oversigtspanelet **Attributter** til at definere de tekniske attributter, der gælder for produkter, der tilhører denne kategori. Yderligere oplysninger om oprettelse af tekniske attributter finder du i [Tekniske attributter og søgning efter tekniske attributter](engineering-attributes-and-search.md).

Brug knapperne i oversigtspanelet **Attributter** til at tilføje, fjerne og arrangere attributter i gitteret.

Hvis du ændrer valget af attributter for en teknisk kategori, og der allerede findes produkter, der er baseret på den pågældende kategori, skal du beslutte, om du vil anvende ændringerne på disse produkter. Hvis du vil have, at eksisterende produkter skal afspejle ændringerne, skal du vælge **Opdater eksisterende produkter** i oversigtspanelet **Attributter**.

For hver række, du føjer til gitteret, skal du angive følgende felter.

| Felt | Beskrivelse |
|---|---|
| Navn | Vælg den attribut, der skal tilføjes. |
| Værdi | Vælg standardværdien for attributten. |
| Obligatorisk | I forbindelse med attributter af typen *Boolesk* skal brugere, hvis denne indstilling er angivet til *Ja*, angive attributten til *Ja*. Hvis denne indstilling er angivet til *Nej*, kan brugere angive attributten til enten *Ja* eller *Nej*. Denne indstilling er kun til orientering for andre datatyper. |
| Batchattribut | Vælg, om attributten skal udbredes via batchfunktionen. |

### <a name="readiness-policy-fasttab"></a>Oversigtspanelet Parathedspolitik

Brug feltet **Politik for produktparathed** til at vælge den parathedspolitik, der skal gælde for produkter, som oprettes på baggrund af denne tekniske kategori. Du kan finde flere oplysninger under [Produktparathed](product-readiness.md).

> [!NOTE]
> Feltet **Politik for produktparathed** fungerer lidt anderledes, hvis du har aktiveret funktionen *Parathedskontroller af produkt* i systemet. (Denne funktion giver dig mulighed for at anvende parathedspolitikker på standard \[ikke-tekniske\] produkter). Du kan finde flere oplysninger under [Tildele parathedspolitikker til standardprodukter og tekniske produkter](product-readiness.md#assign-policy).

### <a name="release-policy-fasttab"></a>Oversigtspanelet Frigivelsespolitik

Brug feltet **Politik for produktfrigivelse** til at vælge den frigivelsespolitik, der gælder for produkter, der tilhører denne kategori. Yderligere oplysninger finder du under [Frigive produktstrukturer](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Oprette forbindelse mellem styklister og ruter til tekniske versioner

Indstillingen af **Gennemtving gyldighed** er vigtig for forbindelsen mellem styklister og ruter til hver enkelt tekniske version. Du kan kun aktivere flere styklister eller ruter pr. produkt, hvis der er forskel på en af følgende indstillinger:

- Produktdimension
- Kvantitet
- Lokation
- Gyldighedsdatoer

Der oprettes tekniske styklister og ruter ud fra den tekniske version, hvor de gælder. De kan genkendes af markeringen i afkrydsningsfeltet **Teknisk kontrolleret**. Når du arbejder med tekniske styklister og ruter, kan du normalt ikke designe dem ved hjælp af forskellige mængder. Du kan typisk heller ikke designe forskellige styklister pr. sted. Derudover er gyldighedsdatoer for tekniske styklister og ruter altid hentet fra den tekniske version. En teknisk version, dens stykliste og rute har derfor alle de samme gyldighedsdatoer.

For produkter, hvor du bruger produktdimensionen *version* (sammen med logistisk indflydelse på transaktionerne), føjes versionen også til styklisterne og ruterne. Denne funktionsmåde hjælper med at skelne mellem styklisterne og ruterne for fortløbende versioner uanset indstillingen af **Gennemtving gyldighed**.

For produkter, hvor du ikke bruger produktdimensionen *version* (uden logistisk indflydelse på transaktionerne), føjes versionen ikke til styklisterne eller ruterne. Derfor vil der ikke være nogen forskel mellem styklisterne og ruterne i fortløbende versioner. I dette tilfælde anbefales det, at du angiver indstillingen **Gennemtving gyldighed** til *Ja*. På denne måde er du med til at forhindre, at tekniske versioner overlapper, og du kan også aktivere styklisten og ruten for en nyere version uden først at skulle deaktivere styklisten og ruten for den tidligere version. Hvis du angiver indstillingen **Gennemtving gyldighed** til *Ja* i dette tilfælde, skal du deaktivere styklisterne og ruterne i tidligere versioner manuelt, før du kan aktivere den seneste version.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
