---
title: Samlet produktoplevelse
description: Denne artikel beskriver integrationen af produktdata mellem programmer til finans og drift og Dataverse.
author: t-benebo
ms.date: 06/23/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 89ef56510ec971ef97fc9eb5c80768527abf5f88
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288916"
---
# <a name="unified-product-experience"></a>Samlet produktoplevelse

[!include [banner](../../includes/banner.md)]



Når en virksomheds økosystem består af Dynamics 365-applikationer, som f.eks. Finance, Supply Chain Management og Sales, anvender virksomhederne ofte disse programmer til at levere produktdata. Det skyldes, at disse apps udgør en robust produktinfrastruktur suppleret med avancerede prissætningskoncepter og nøjagtige disponible lagerbeholdningsdata. Virksomheder, der bruger et eksternt PLM-system (Product Lifecycle Management) til at levere produktdata, kan kanalisere produkter fra programmer til finans og drift til andre Dynamics 365-apps. Den samlede produktoplevelse overfører den integrerede produktdatamodel ind i Dataverse, så alle programbrugere, herunder Power Platform-brugere, kan udnytte de omfattende produktdata, der kommer fra programmer til finans og drift.

Her er produktdatamodellen fra Sales.

![Datamodel for produkter i CE.](media/dual-write-product-4.jpg)

Her er produktdatamodellen fra programmer til finans og drift.

![Datamodel for produkter i programmer til finans og drift.](media/dual-write-products-5.jpg)

Disse to produktdatamodeller er blevet integreret i Dataverse som vist nedenfor.

![Datamodel for produkter i Dynamics 365-apps.](media/dual-write-products-6.jpg)

Tabeltilknytninger med dobbeltskrivning for produkter er designet til kun at overføre data en vej i en næsten realtidsoplevelse fra programmer til finans og drift til Dataverse. Men produktinfrastrukturen er gjort åben for at gøre den tovejs, hvis det er nødvendigt. Selvom du kan tilpasse den, er det på egen risiko, da Microsoft ikke anbefaler denne fremgangsmåde.

## <a name="templates"></a>Skabeloner

Produktoplysninger indeholder alle de oplysninger, der er knyttet til produktet og dets definition, f. eks. produktdimensionerne eller sporings-og lagringsdimensionerne. Som følgende tabel viser, oprettes der en samling af tabeltilknytninger for at synkronisere produkter og relaterede oplysninger.

Programmer til finans og drift | Andre Dynamics 365-apps | Beskrivende tekst
-----------------------|--------------------------------|---
[Alle produkter](mapping-reference.md#138) | msdyn_globalproducts | Tabellen Alle produkter indeholder alle produkter, der er tilgængelige i programmer til finans og drift, både i frigivne og ikke-frigivne produkter.
[Frigivne specifikke produkter i CDS](mapping-reference.md#213) | Produkt | Tabellen **Produkt** indeholder de kolonner, der definerer produktet. Den omfatter individuelle produkter (produkter med undertypeprodukt) og produktvarianterne. Tilknytningerne vises i følgende tabel.
[Farver](mapping-reference.md#170) | msdyn\_productcolors
[Varianter](mapping-reference.md#171) | msdyn\_productconfigurations
[Standardindstillinger for ordre](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Produktkategorier](mapping-reference.md#166) | msdyn_productcategories | Hver produktkategorier og oplysninger om dens struktur og karakteristika findes i tabellen produktkategori.
[Tildelinger af produktkategori](mapping-reference.md#167) | msdyn_productcategoryassignments | Du kan anvende tabellen produktkategoritildeling til at tildele et produkt til en kategori.
[Hierarkier for produktkategori](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Du kan bruge produkthierarkier til at kategorisere eller gruppere produkter. Kategorihierarkierne er tilgængelige i Dataverse ved hjælp af tabellen Produktkategorihierarki.
[Hierarkiroller for produktkategori](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | Produkthierarkier kan bruges til forskellige roller i D365 finans og drift. De angiver, hvilken kategori der bruges i hver rolle for tabellen produktkategorirolle, som anvendes.
[Standardindstillinger for produktordrer V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Produktdimensionsgrupper](mapping-reference.md#173) | msdyn\_productdimensiongroups | Produktdimensionsgruppen definerede, hvilke produktdimensioner der definerer produktet.
[Produktmasterfarver](mapping-reference.md#187) | msdyn_sharedproductcolors | Tabellen **Delt produktfarve** angiver de farver, en bestemt produktmaster kan have. Dette begreb overflyttes til Dataverse for at bevare data konsekvente.
[Konfigurationer af produktmaster](mapping-reference.md#188) | msdyn_sharedproductconfigurations | Tabellen **Delt produktkonfiguration** angiver de konfigurationer, en bestemt produktmaster kan have. Dette begreb overflyttes til Dataverse for at bevare data konsekvente.
[Produktmasterstørrelser](mapping-reference.md#190) | msdyn_sharedproductsizes | Tabellen **Delt produktstørrelse** angiver de størrelser, som en bestemt produktmaster kan have. Dette begreb overflyttes til Dataverse for at bevare data konsekvente.
[Typografier for produktmaster](mapping-reference.md#191) | msdyn_sharedproductstyles | Tabellen **Delt produkttypografi** angiver de typografier, en bestemt produktmaster kan have. Dette begreb overflyttes til Dataverse for at bevare data konsekvente.
[Stregkode identificeret ud fra produktnummer](mapping-reference.md#164) | msdyn\_productbarcodes | Produktstregkoder bruges til entydig identifikation af produkter.
[Produktspecifikke enhedsomregninger](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Frigivne produkter V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | Tabellen **msdyn\_sharedproductdetails** indeholder kolonnerne fra programmer til finans og drift, der definerer produktet, og som indeholder produktets økonomiske og administrative oplysninger.
[Størrelser](mapping-reference.md#174) | msdyn\_productsizes
[Lagringsdimensionsgrupper](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | Dimensionsgruppen for produktlagring repræsenterer den metode, der bruges til at definere placeringen af produktet på lagerstedet.
[Typer](mapping-reference.md#178) | msdyn\_productstyles
[Sporingsdimensionsgrupper](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | Gruppen for produktsporingsdimension repræsenterer den metode, der bruges til at spore produktet på lageret.
[Objekter](mapping-reference.md#219) | uoms
[Enhedsomregninger](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>Integration af produkter

I denne model repræsenteres produktet af kombinationen af to tabeller i Dataverse: **Produkt** og **msdyn\_sharedproductdetails**. Den første tabel indeholder definitionen af et produkt (det entydige id for produktet, produktnavnet og beskrivelsen), og den anden tabel indeholder de kolonner, som er gemt på produktniveauet. Kombinationen af disse to tabeller bruges til at definere produktet ud fra begrebet lagerenhed (SKU). Hvert af de frigivne produkter indeholder sine oplysninger i de nævnte tabeller (oplysninger om produkt og delt produkt). Hvis du vil holde styr på alle produkter (frigivne og ikke-frigivne), skal du bruge tabellen **Globale produkter**.

Da produktet er repræsenteret som en SKU, kan koncepterne for specifikke produkter, produktmastere og produktvarianter registreres i Dataverse på følgende måde:

- **Produkter med undertypeprodukt** er produkter, der defineres af dem selv. Der skal ikke defineres dimensioner. Et eksempel er en bestemt bog. For disse produkter oprettes der en række i tabellen **Produkt**, og der oprettes en række i tabellen **msdyn\_sharedproductdetails**. Der oprettes ingen produktfamilierække.
- **Produktmastere** bruges som standardprodukter, der indeholder de definitioner og regler, der bestemmer funktionaliteten i forretningsprocesser. Baseret på disse definitioner kan der genereres specifikke produkter, der kaldes produktvarianter. F. eks. er T-shirt produktmasteren, og den kan have farve og størrelse som dimensioner. Der kan frigives varianter med forskellige kombinationer af disse dimensioner, f. eks. en lille blå T-shirt eller en mellem grøn T-shirt. I integrationen oprettes der én række pr. variant i produkttabellen. Denne række indeholder variantspecifikke oplysninger, f.eks. de forskellige dimensioner. De generelle oplysninger for produktet gemmes i tabellen **msdyn\_sharedproductdetails**. (Disse standardoplysninger opbevares i produktmasteren). Oplysningerne om produktmasteren synkroniseres med Dataverse, så snart den frigivne produktmaster er oprettet (men før der frigives varianter).
- **Specifikke produkter** refererer til alle produkternes undertypeprodukt og alle produktvarianterne.

![Datamodel for produkter.](media/dual-write-product.png)

Når dobbeltskrivningsfunktionaliteten er aktiveret, vil produkter fra finans og drift blive synkroniseret i andre Dynamics 365-produkter i tilstanden **Kladde**. De føjes til den første prisliste med den samme valuta, som bruges i Customer Engagement-appen og ved hjælp af alfabetisk sortering på prislistenavnet. De føjes med andre ord til den første prisliste i en Dynamics 365-app, der har samme valuta som din juridiske tabel, hvor produktet frigives i et program til finans og drift. Hvis der ikke findes en prisliste for den angivne valuta, oprettes der automatisk en prisliste, og produktet vil blive tildelt til den.

Den aktuelle implementering af de script-plugins, der knytter standardprislisten til enheden, viser den valuta, der er tilknyttet programmet til finans og drift, og finder den første prisliste i kundekonteringsappen ved hjælp af alfabetisk sortering på prislistenavnet. Hvis du vil angive en standardprisliste for en bestemt valuta, når du har flere prislister for den pågældende valuta, skal du opdatere prislistenavnet til et navn, der er tidligere i alfabetisk rækkefølge end andre prislister for den samme valuta. Hvis der ikke findes en prisliste for den angivne valuta, oprettes der en ny.

Som standard synkroniseres produkter fra programmer til finans og drift til andre Dynamics 365-apps i tilstanden **Kladde**. Hvis du vil synkronisere produktet med tilstanden **Aktiv**, så du f.eks. kan bruge det direkte i salgsordretilbud, skal følgende indstilling vælges: under fanen **System> Administration > Systemadministration > Systemindstillinger > Sales** skal du vælge **Opret produkter i aktiv tilstand = ja**.

Når produkter synkroniseres, skal du angive en værdi til feltet **Salgsenhed** i programmer til finans og drift, fordi det er et obligatorisk felt i Salg.

Oprettelsen af produktfamilier fra Dynamics 365 Sales understøttes ikke med synkronisering af produkter.

Synkroniseringen af produkter sker fra programmer til finans og drift til Dataverse. Det betyder, at værdierne i produkttabelkolonnerne kan ændres i Dataverse, men når synkroniseringen udløses (når et produktfelt ændres i programmer til finans og drift), overskrives værdierne i Dataverse.

Programmer til finans og drift | Kundeengagementapps |
---|---
[Frigivne specifikke produkter i CDS](mapping-reference.md#213) | Produkt |
[Frigivne produkter V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[Alle produkter](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Produktdimensioner

Produktdimensioner er egenskaber, der identificerer en produktvariant. De fire produktdimensioner (farve, størrelse, typografi og konfiguration) knyttes også til Dataverse, så du kan definere produktvarianterne. I følgende illustration vises datamodellen for produktdimensionen Farve. Den samme model anvendes på størrelser, typografier og konfigurationer.

![Datamodel til produktdimensioner.](media/dual-write-product-two.png)

Programmer til finans og drift | Kundeengagementapps |
---|---
[Farver](mapping-reference.md#170) | msdyn\_productcolors
[Størrelser](mapping-reference.md#174) | msdyn\_productsizes
[Typer](mapping-reference.md#178) | msdyn\_productstyles
[Varianter](mapping-reference.md#171) | msdyn\_productconfigurations

Når et produkt har forskellige produktdimensioner (en produktmaster har f.eks. størrelse og farve som produktdimensioner), defineres hvert specifikt produkt (dvs. de enkelte produktvarianter) som en kombination af disse produktdimensioner. Produktnummer B0001 er f.eks. en ekstra lille sort T-shirt, og produktnummer B0002 er en lille sort T-shirt. I dette tilfælde defineres de eksisterende kombinationer af produktdimensioner. F.eks. kan T-shirten fra det foregående eksempel være ekstra lille og sort, lille og sort, mellem og sort eller stor og sort, men den kan ikke være ekstrastor og sort. Det vil sige, at de produktdimensioner, en produktmaster kan antage, angives, og varianter kan frigives ud fra disse værdier.

For at holde styr på de produktdimensioner, en produktmaster kan antage, oprettes og tilknyttes følgende tabeller i Dataverse for hver produktdimension. Du kan finde flere oplysninger under [Oversigt over produktoplysninger](../../../../supply-chain/pim/product-information.md).

Programmer til finans og drift | Kundeengagementapps |
---|---
[Produktmasterfarver](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Konfigurationer af produktmaster](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Produktmasterstørrelser](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Typografier for produktmaster](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Stregkode identificeret ud fra produktnummer](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Standardindstillinger for ordrer og produktspecifikke standardindstillinger for ordrer

Standardindstillinger for ordre definerer lokationen og lagerstedet, hvor varerne skal leveres fra eller oplagres, minimum-, maksimum-, flere og standardmængder, der skal bruges til handel eller lagerstyring, leveringstider, stopflaget og metoden for ordretilsagn. Disse oplysninger er tilgængelige i Dataverse ved hjælp af standardindstillingerne for vareordrer og enheden for produktspecifikke standardindstillinger for vareordrer. Du kan finde flere oplysninger om funktionaliteten i [artiklen Standardindstillinger for ordre](../../../../supply-chain/production-control/default-order-settings.md).

Programmer til finans og drift | Kundeengagementapps |
---|---
[Standardindstillinger for ordre](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Standardindstillinger for produktordrer V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Måleenhed og omregninger af måleenhed

Måleenhederne og de respektive omregninger er tilgængelige i Dataverse i henhold til datamodellen, der vises i diagrammet.

![Datamodel for måleenhed.](media/dual-write-product-three.png)

Måleenhedsbegrebet er integreret mellem programmer til finans og drift og andre Dynamics 365-apps. For hver enhedsklasse i programmer til finans og drift oprettes der en enhedsgruppe i en Dynamics 365-app, som indeholder de enheder, der hører til enhedsklassen. Der oprettes også en standardbasisenhed for hver enhedsgruppe.

Programmer til finans og drift | Kundeengagementapps |
---|---
[Produktspecifikke enhedsomregninger](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Objekter](mapping-reference.md#219) | uoms
[Enhedsomregninger](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Indledende synkronisering af enhedsdata der matches mellem finans og drift og Dataverse

### <a name="initial-synchronization-of-units"></a>Første synkronisering af enheder

Når dobbeltskrivning er aktiveret, synkroniseres enheder fra programmer til finans og drift til andre Dynamics 365-apps. De enhedsgrupper, der synkroniseres fra programmer til finans og drift i Dataverse, har et flag, der angiver, at de er "Eksternt vedligeholdte".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Data for sammenholdte enheder og enhedsklasser/-grupper fra programmer til finans og drift og andre Dynamics 365-apps

Indledningsvist er det vigtigt at bemærke, at integrationsnøglen for enheden er msdyn_symbol. Derfor skal denne værdi være entydig i Dataverse eller andre Dynamics 365-apps. Da det i andre Dynamics 365-apps er det parrede "Enhedsgruppe-id" og "Navn", der definerer en enheds entydighed, skal du overveje forskellige scenarier for at kunne sammenligne enhedsdata mellem programmer til finans og drift og Dataverse.

For enheder, der svarer til/overlapper i programmer til finans og drift og andre Dynamics 365-Apps:

+ **Enheden tilhører en enhedsgruppe i andre Dynamics 365-apps, der svarer til den tilknyttede enhedsklasse i programmer til finans og drift**. I dette tilfælde skal kolonnen msdyn_symbol i andre Dynamics 365-apps udfyldes med enhedssymbolet fra programmer til finans og drift. Når dataene bliver sammenholdt, vil enhedsgruppen derfor blive angivet som "Eksternt vedligeholdt" i andre Dynamics 365-apps.
+ **Enheden tilhører en enhedsgruppe i andre Dynamics 365-apps, der ikke svarer til den tilknyttede enhedsklasse i programmer til finans og drift (ingen eksisterende enhedsklasse i programmer til finans og drift for enhedsklassen i andre Dynamics 365-apps).** I dette tilfælde skal msdyn_symbol udfyldes med en tilfældig streng. Bemærk, at denne værdi skal være entydig i andre Dynamics 365-apps.

For enheder og enhedsklasser i finans og drift, der ikke findes i andre Dynamics 365-Apps:

Som en del af dobbeltskrivning er enhedsgrupperne fra programmer til finans og drift og dens tilsvarende enheder oprettet og synkroniseret i andre Dynamics 365-apps samt Dataverse, og enhedsgruppen angives som "Eksternt vedligeholdt". Der kræves ikke nogen ekstra bootstrapping.

For enheder i andre Dynamics 365-apps, som ikke findes i programmer til finans og drift:

Kolonnen msdyn_symbol skal udfyldes for alle enheder. Enhederne kan altid oprettes i programmer til finans og drift i den tilhørende enhedsklasse (hvis den findes). Hvis enhedsklassen ikke findes, skal enhedsklassen først oprettes (bemærk, at du ikke kan oprette en enhedsklasse i programmer til finans og drift undtagen via udvidelse, hvis du udvider fastteksten), så den stemmer overens med enhedsgruppen for de andre Dynamics 365-apps. Dernæst kan du oprette enheden. Bemærk, at enhedssymbolet i programmer til finans og drift skal være det tidligere angivne msdyn_symbol i andre Dynamics 365-apps for enheden.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Produktpolitikker, dimension, sporing og lagringsgrupper

Produktpolitikkerne er sæt af politikker, der bruges til at definere produkter og deres egenskaber på lageret. Produktdimensionsgruppen, gruppen for produktsporingsdimension og lagringsdimensionsgruppen kan findes som produkt politikker.

Programmer til finans og drift | Kundeengagementapps |
---|---
[Produktdimensionsgrupper](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[Lagringsdimensionsgrupper](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[Sporingsdimensionsgrupper](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>Produkthierarkier

Programmer til finans og drift | Kundeengagementapps |
---|---
[Tildelinger af produktkategori](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Hierarkier for produktkategori](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Hierarkiroller for produktkategori](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles |

## <a name="integration-key-for-products"></a>Integrationsnøgle for produkter

Til entydig identifikation af produkter mellem Dynamics 365 Finance og produkter i Dataverse anvendes integrationsnøgler.
For produkter er **(produktnummer)** den entydige nøgle, der identificerer et produkt i Dataverse. Den er sammensat af sammenkædningen af: **(firma, msdyn_produktnummer)**. **Firmaet** angiver den juridiske enhed i finans og drift, og **msdyn_produktnummer** produktnummeret for det specifikke produkt i finans og drift.

For brugere af andre Dynamics 365-apps identificeres produktet i brugergrænsefladen med **msdyn_produktnummer** (bemærk, at etiketten for kolonnen er **Produktnummer**). I produktformularen vises både firmaet og msydn_produktnummeret. Men i kolonne (produktnummer) vises den entydige nøgle for et produkt ikke.

Hvis du bygger apps på Dataverse, skal du være opmærksom på at bruge **produktnummer** (det entydige produkt-id) som integrationsnøgle. Brug **ikke msdyn_productnumber**, da det ikke er entydigt.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Første synkronisering af produkter og migrering af data fra Dataverse til finans og drift

### <a name="initial-synchronization-of-products"></a>Første synkronisering af produkter

Når dobbeltskrivning er aktiveret, synkroniseres produkter fra programmer til finans og drift til Dataverse og kundeengagementsapps. Produkter oprettet i Dataverse og andre Dynamics 365-apps før dobbeltskrivning blev frigivet, ikke bliver opdateret eller sammenlignet med produktdata fra programmer til finans og drift.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Sammenligning af produktdata fra finans og drift og andre Dynamics 365-apps

Hvis de samme produkter lagres (overlappende/sammenholdte) i finans og drift og i Dataverse samt andre Dynamics 365-apps, når dobbeltskrivning aktiveres, synkroniseres produkter fra finans og drift og dubletrækkerne vil blive vist i Dataverse for det samme produkt.
For at undgå den i forrige afsnit refererede situation, i tilfælde af at andre Dynamics 365-apps har produkter, der overlapper hinanden/svarer til dem i finans og drift, skal administratoren, der aktiverer dobbeltskrivning, bootstrappe kolonnerne **Firma** (f.eks. "USMF") og **msdyn_produktnummer** (f.eks. "1234:Black:S") før produkterne synkroniseres. Med andre ord skal disse to felter i produktet i Dataverse udfyldes med det pågældende firma i finans og drift, som produktet skal sammenholdes med, og med dets produktnummer.

Når synkroniseringen er aktiveret og finder sted, vil produkterne fra finans og drift blive synkroniseret med de matchende produkter i Dataverse og andre Dynamics 365-apps. Dette gælder for både specifikke produkter og produktvarianter.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Migration af produktdata fra andre Dynamics 365-apps til finans og drift

Hvis andre Dynamics 365-apps har produkter, der ikke er til stede i finans og drift, kan administratoren indledningsvist anvende **EcoResReleasedProductCreationV2Entity** til at importere disse produkter i finans og drift. Dernæst kan produktdataene fra finans og drift og andre Dynamics 365-apps sammenholdes som beskrevet ovenfor.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

