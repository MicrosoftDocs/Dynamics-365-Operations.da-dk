---
title: Samlet produktoplevelse
description: I dette emne beskrives integrationen af produktdata mellem Finance and Operations-apps og Dataverse.
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6941a38e96520befd3bdba65956d45a6bbaee4be
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306383"
---
# <a name="unified-product-experience"></a>Samlet produktoplevelse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Når en virksomheds økosystem består af Dynamics 365-applikationer, som f.eks. Finance, Supply Chain Management og Sales, anvender virksomhederne ofte disse programmer til at levere produktdata. Det skyldes, at disse apps udgør en robust produktinfrastruktur suppleret med avancerede prissætningskoncepter og nøjagtige disponible lagerbeholdningsdata. Virksomheder, der bruger et eksternt PLM-system (Product Lifecycle Management) til at levere produktdata, kan kanalisere produkter fra Finance and Operations-apps til andre Dynamics 365-apps. Den samlede produktoplevelse overfører den integrerede produktdatamodel ind til Dataverse, så alle programbrugere, herunder Power Platform-brugere, kan udnytte de omfattende produktdata, der kommer fra Finance and Operations-apps.

Her er produktdatamodellen fra Sales.

![Datamodel for produkter i CE](media/dual-write-product-4.jpg)

Her er produktdatamodellen fra Finance and Operations-apps.

![Datamodel for produkter i Finance and Operations](media/dual-write-products-5.jpg)

Disse to produktdatamodeller er blevet integreret i Dataverse som vist nedenfor.

![Datamodel for produkter i Dynamics 365-apps](media/dual-write-products-6.jpg)

Tabeltilknytninger med dobbeltskrivning for produkter er designet til kun at udføre envejsoverførsel af data i næsten realtid fra Finance and Operations-apps til Dataverse. Men produktinfrastrukturen er gjort åben for at gøre den tovejs, hvis det er nødvendigt. Selvom du kan tilpasse den, er det på egen risiko, da Microsoft ikke anbefaler denne fremgangsmåde.

## <a name="templates"></a>Skabeloner

Produktoplysninger indeholder alle de oplysninger, der er knyttet til produktet og dets definition, f. eks. produktdimensionerne eller sporings-og lagringsdimensionerne. Som følgende tabel viser, oprettes der en samling af tabeltilknytninger for at synkronisere produkter og relaterede oplysninger.

Finance and Operations-apps | Andre Dynamics 365-apps | Beskrivende tekst
-----------------------|--------------------------------|---
Frigivne produkter V2 | msdyn\_sharedproductdetails | Tabellen **msdyn\_sharedproductdetails** indeholder kolonnerne fra Finance and Operations-apps, der definerer produktet, og som indeholder produktets økonomiske og administrative oplysninger. 
Dataverse frigav specifikke produkter | Produkt | Tabellen **Produkt** indeholder de kolonner, der definerer produktet. Den omfatter individuelle produkter (produkter med undertypeprodukt) og produktvarianterne. Tilknytningerne vises i følgende tabel.
Stregkode identificeret ud fra produktnummer | msdyn\_productbarcodes | Produktstregkoder bruges til entydig identifikation af produkter.
Standardindstillinger for ordre | msdyn\_productdefaultordersettings
Produktspecifikke standardordreindstillinger | msdyn_productdefaultordersettings
Produktdimensionsgrupper | msdyn\_productdimensiongroups | Produktdimensionsgruppen definerede, hvilke produktdimensioner der definerer produktet. 
Lagringsdimensionsgrupper | msdyn\_productstoragedimensiongroups | Dimensionsgruppen for produktlagring repræsenterer den metode, der bruges til at definere placeringen af produktet på lagerstedet.
Sporingsdimensionsgrupper | msdyn\_producttrackingdimensiongroups | Gruppen for produktsporingsdimension repræsenterer den metode, der bruges til at spore produktet på lageret.
Farver | msdyn\_productcolors
Størrelser | msdyn\_productsizes
Typografier | msdyn\_productsytles
Konfigurationer | msdyn\_productconfigurations
Produktmasterfarver | msdyn_sharedproductcolors | Tabellen **Delt produktfarve** angiver de farver, en bestemt produktmaster kan have. Dette begreb overflyttes til Dataverse for at bevare data konsekvente.
Produktmasterstørrelser | msdyn_sharedproductsizes | Tabellen **Delt produktstørrelse** angiver de størrelser, som en bestemt produktmaster kan have. Dette begreb overflyttes til Dataverse for at bevare data konsekvente.
Typografier for produktmaster | msdyn_sharedproductstyles | Tabellen **Delt produkttypografi** angiver de typografier, en bestemt produktmaster kan have. Dette begreb overflyttes til Dataverse for at bevare data konsekvente.
Konfigurationer af produktmaster | msdyn_sharedproductconfigurations | Tabellen **Delt produktkonfiguration** angiver de konfigurationer, en bestemt produktmaster kan have. Dette begreb overflyttes til Dataverse for at bevare data konsekvente.
Alle produkter | msdyn_globalproducts | Tabellen Alle produkter indeholder alle produkter, der er tilgængelige i Finance and Operations-apps, både i frigivne og ikke-frigivne produkter.
Enhed | uoms
Enhedsomregninger | msdyn_ unitofmeasureconversions
Konvertering af produktspecifik måleenhed | msdyn_productspecificunitofmeasureconversion
Produktkategorier | msdyn_productcategories | Hver produktkategorier og oplysninger om dens struktur og karakteristika findes i tabellen produktkategori. 
Hierarkier for produktkategori | msdyn_productcategoryhierarhies | Du kan bruge produkthierarkier til at kategorisere eller gruppere produkter. Kategorihierarkierne er tilgængelige i Dataverse ved hjælp af tabellen Produktkategorihierarki. 
Hierarkiroller for produktkategori | msdyn_productcategoryhierarchies | Produkthierarkier kan bruges til forskellige roller i D365 Finance and Operations. De angiver, hvilken kategori der bruges i hver rolle for tabellen produktkategorirolle, som anvendes. 
Tildelinger af produktkategori | msdyn_productcategoryassignments | Du kan anvende tabellen produktkategoritildeling til at tildele et produkt til en kategori.

## <a name="integration-of-products"></a>Integration af produkter

I denne model repræsenteres produktet af kombinationen af to tabeller i Dataverse: **Produkt** og **msdyn\_sharedproductdetails**. Den første tabel indeholder definitionen af et produkt (det entydige id for produktet, produktnavnet og beskrivelsen), og den anden tabel indeholder de kolonner, som er gemt på produktniveauet. Kombinationen af disse to tabeller bruges til at definere produktet ud fra begrebet lagerenhed (SKU). Hvert af de frigivne produkter indeholder sine oplysninger i de nævnte tabeller (oplysninger om produkt og delt produkt). Hvis du vil holde styr på alle produkter (frigivne og ikke-frigivne), skal du bruge tabellen **Globale produkter**. 

Da produktet er repræsenteret som en SKU, kan koncepterne for specifikke produkter, produktmastere og produktvarianter registreres i Dataverse på følgende måde:

- **Produkter med undertypeprodukt** er produkter, der defineres af dem selv. Der skal ikke defineres dimensioner. Et eksempel er en bestemt bog. For disse produkter oprettes der en række i tabellen **Produkt**, og der oprettes en række i tabellen **msdyn\_sharedproductdetails**. Der oprettes ingen produktfamilierække.
- **Produktmastere** bruges som standardprodukter, der indeholder de definitioner og regler, der bestemmer funktionaliteten i forretningsprocesser. Baseret på disse definitioner kan der genereres specifikke produkter, der kaldes produktvarianter. F. eks. er T-shirt produktmasteren, og den kan have farve og størrelse som dimensioner. Der kan frigives varianter med forskellige kombinationer af disse dimensioner, f. eks. en lille blå T-shirt eller en mellem grøn T-shirt. I integrationen oprettes der én række pr. variant i produkttabellen. Denne række indeholder variantspecifikke oplysninger, f.eks. de forskellige dimensioner. De generelle oplysninger for produktet gemmes i tabellen **msdyn\_sharedproductdetails**. (Disse standardoplysninger opbevares i produktmasteren). Oplysningerne om produktmasteren synkroniseres med Dataverse, så snart den frigivne produktmaster er oprettet (men før der frigives varianter).
- **Specifikke produkter** refererer til alle produkternes undertypeprodukt og alle produktvarianterne. 

![Datamodel for produkter](media/dual-write-product.png)

Når dobbeltskrivningsfunktionaliteten er aktiveret, vil produkterne fra Finance and Operations vil blive synkroniseret i andre Dynamics 365-produkter i tilstanden **Kladde**. De føjes til den første prisliste med samme valuta. De føjes med andre ord til den første prisliste i en Dynamics 365-app, der har samme valuta som din juridiske tabel, hvor produktet frigives i en Finance and Operations-app. Hvis der ikke findes en prisliste for den angivne valuta, oprettes der automatisk en prisliste, og produktet vil blive tildelt til den. 

Den aktuelle implementering af de script-plugins, der knytter standardprislisten til enheden, viser den valuta, der er tilknyttet Finance and Operations-appen, og finder den første prisliste i kundekonteringsappen ved hjælp af alfabetisk sortering på prislistenavnet. Hvis du vil angive en standardprisliste for en bestemt valuta, når du har flere prislister for den pågældende valuta, skal du opdatere prislistenavnet til et navn, der er tidligere i alfabetisk rækkefølge end andre prislister for den samme valuta.

Som standard synkroniseres produkter fra Finance and Operations-apps til andre Dynamics 365-apps i tilstanden **Kladde**. Hvis du vil synkronisere produktet med tilstanden **Aktiv**, så du f.eks. kan bruge det direkte i salgsordretilbud, skal følgende indstilling vælges: under fanen **System> Administration > Systemadministration > Systemindstillinger > Sales** skal du vælge **Opret produkter i aktiv tilstand = ja**. 

Når produkter synkroniseres, skal du angive en værdi til feltet **Salgsenhed** i Finance and Operations-appen, fordi det er et obligatorisk felt i Salg.

Oprettelsen af produktfamilier fra Dynamics 365 Sales understøttes ikke med synkronisering af produkter.

Bemærk, at synkroniseringen af produkter sker fra Finance and Operations-appen til Dataverse. Det betyder, at værdierne i produkttabelkolonnerne kan ændres i Dataverse, men når synkroniseringen udløses (når en produktkolonne ændres i en Finance and Operations-app), overskrives værdierne i Dataverse. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Produktdimensioner 

Produktdimensioner er egenskaber, der identificerer en produktvariant. De fire produktdimensioner (farve, størrelse, typografi og konfiguration) knyttes også til Dataverse, så du kan definere produktvarianterne. I følgende illustration vises datamodellen for produktdimensionen Farve. Den samme model anvendes på størrelser, typografier og konfigurationer. 

![Datamodel til produktdimensioner](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Når et produkt har forskellige produktdimensioner (en produktmaster har f.eks. størrelse og farve som produktdimensioner), defineres hvert specifikt produkt (dvs. de enkelte produktvarianter) som en kombination af disse produktdimensioner. Produktnummer B0001 er f.eks. en ekstra lille sort T-shirt, og produktnummer B0002 er en lille sort T-shirt. I dette tilfælde defineres de eksisterende kombinationer af produktdimensioner. F.eks. kan T-shirten fra det foregående eksempel være ekstra lille og sort, lille og sort, mellem og sort eller stor og sort, men den kan ikke være ekstrastor og sort. Det vil sige, at de produktdimensioner, en produktmaster kan antage, angives, og varianter kan frigives ud fra disse værdier.

For at holde styr på de produktdimensioner, en produktmaster kan antage, oprettes og tilknyttes følgende tabeller i Dataverse for hver produktdimension. Du kan finde flere oplysninger under [Oversigt over produktoplysninger](../../../../supply-chain/pim/product-information.md). 

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Standardindstillinger for ordrer og produktspecifikke standardindstillinger for ordrer

Standardindstillinger for ordre definerer lokationen og lagerstedet, hvor varerne skal leveres fra eller oplagres, minimum-, maksimum-, flere og standardmængder, der skal bruges til handel eller lagerstyring, leveringstider, stopflaget og metoden for ordretilsagn. Disse oplysninger er tilgængelige i Dataverse ved hjælp af standardindstillingerne for vareordrer og enheden for produktspecifikke standardindstillinger for vareordrer. Du kan finde flere oplysninger om funktionaliteten under [emnet Standardindstillinger for ordre](../../../../supply-chain/production-control/default-order-settings.md).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Måleenhed og omregninger af måleenhed

Måleenhederne og de respektive omregninger er tilgængelige i Dataverse i henhold til datamodellen, der vises i diagrammet.

![Datamodel for måleenhed](media/dual-write-product-three.png)

Måleenhedsbegrebet er integreret mellem Finance and Operations-apps og andre Dynamics 365-apps. For hver enhedsklasse i en Finance and Operations-app oprettes der en enhedsgruppe i en Dynamics 365-app, som indeholder de enheder, der hører til enhedsklassen. Der oprettes også en standardbasisenhed for hver enhedsgruppe. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Indledende synkronisering af enhedsdata der matches mellem Finance and Operations og Dataverse

### <a name="initial-synchronization-of-units"></a>Første synkronisering af enheder

Når dobbeltskrivning er aktiveret, synkroniseres enheder fra Finance and Operations-apps til andre Dynamics 365-apps. De enhedsgrupper, der synkroniseres fra Finance and Operations-apps i Dataverse, har et flag, der angiver, at de er "Eksternt vedligeholdte".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Data for sammenholdte enheder og enhedsklasser/-grupper fra Finance and Operations-apps og andre Dynamics 365-apps

Indledningsvist er det vigtigt at bemærke, at integrationsnøglen for enheden er msdyn_symbol. Derfor skal denne værdi være entydig i Dataverse eller andre Dynamics 365-apps. Da det i andre Dynamics 365-apps er det parrede "Enhedsgruppe-id" og "Navn", der definerer en enheds entydighed, skal du overveje forskellige scenarier for at kunne sammenligne enhedsdata mellem Finance and Operations-apps og Dataverse.

For enheder, der matcher/overlapper i Finance and Operations-apps og andre Dynamics 365-Apps:

+ **Enheden tilhører en enhedsgruppe i andre Dynamics 365-apps, der svarer til den tilknyttede enhedsklasse i Finance and Operations-apps**. I dette tilfælde skal kolonnen msdyn_symbol i andre Dynamics 365-apps udfyldes med enhedssymbolet fra Finance and Operations-apps. Når dataene bliver sammenholdt, vil enhedsgruppen derfor blive angivet som "Eksternt vedligeholdt" i andre Dynamics 365-apps.
+ **Enheden tilhører en enhedsgruppe i andre Dynamics 365-apps, der ikke svarer til den tilknyttede enhedsklasse i Finance and Operations-apps (ingen eksisterende enhedsklasse i Finance and Operations-apps for enhedsklassen i andre Dynamics 365-apps).** I dette tilfælde skal msdyn_symbol udfyldes med en tilfældig streng. Bemærk, at denne værdi skal være entydig i andre Dynamics 365-apps.

For enheder og enhedsklasser i Finance and Operations, der ikke findes i andre Dynamics 365-Apps:

Som en del af dobbeltskrivning er enhedsgrupperne fra Finance and Operations-apps og tilsvarende enheder oprettet og synkroniseret i andre Dynamics 365-apps samt Dataverse, og enhedsgruppen angives som "Eksternt vedligeholdt". Der kræves ikke nogen ekstra bootstrapping.

For enheder i andre Dynamics 365-apps, som ikke findes i Finance and Operations-apps:

Kolonnen msdyn_symbol skal udfyldes for alle enheder. Enhederne kan altid oprettes i Finance and Operations-apps i den tilhørende enhedsklasse (hvis den findes). Hvis enhedsklassen ikke findes, skal enhedsklassen først oprettes (bemærk, at du ikke kan oprette en enhedsklasse i Finance and Operations-apps undtagen via udvidelse, hvis du udvider fastteksten), så den stemmer overens med enhedsgruppen for de andre Dynamics 365-apps. Dernæst kan du oprette enheden. Bemærk, at enhedssymbolet i Finance and Operations-apps skal være det tidligere angivne msdyn_symbol i andre Dynamics 365-apps for enheden.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Produktpolitikker, dimension, sporing og lagringsgrupper

Produktpolitikkerne er sæt af politikker, der bruges til at definere produkter og deres egenskaber på lageret. Produktdimensionsgruppen, gruppen for produktsporingsdimension og lagringsdimensionsgruppen kan findes som produkt politikker. 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Produkthierarkier

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Integrationsnøgle for produkter 

Til entydig identifikation af produkter mellem Dynamics 365 for Finance and Operations og produkter i Dataverse anvendes integrationsnøgler. For produkter er **(produktnummer)** den entydige nøgle, der identificerer et produkt i Dataverse. Den er sammensat af sammenkædningen af: **(firma, msdyn_produktnummer)**. **Firmaet** angiver den juridiske enhed i Finance and Operations, og **msdyn_productnumber** angiver produktnummeret for det specifikke produkt i Finance and Operations. 

For brugere af andre Dynamics 365-apps identificeres produktet i brugergrænsefladen med **msdyn_produktnummer** (bemærk, at etiketten for kolonnen er **Produktnummer**). I produktformularen vises både firmaet og msydn_produktnummeret. Men i kolonne (produktnummer) vises den entydige nøgle for et produkt ikke. 

Hvis du bygger apps på Dataverse, skal du være opmærksom på at bruge **produktnummer** (det entydige produkt-id) som integrationsnøgle. Brug **ikke msdyn_productnumber**, da det ikke er entydigt. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Første synkronisering af produkter og migrering af data fra Dataverse til Finance and Operations

### <a name="initial-synchronization-of-products"></a>Første synkronisering af produkter 

Når dobbeltskrivning er aktiveret, synkroniseres produkter fra Finance and Operations-apps til Dataverse og kundeengagementapps. Produkter, der er oprettet i Dataverse- og andre Dynamics 365-apps, før dobbeltskrivning blev frigivet, bliver ikke opdateret eller sammenlignet med produktdata fra Finance and Operations-apps.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Sammenligning af produktdata fra Finance and Operations og andre Dynamics 365-apps

Hvis de samme produkter lagres (overlappende/matchende) i Finance and Operations og i Dataverse samt andre Dynamics 365-apps, når dobbeltskrivning aktiveres, synkroniseres produkter fra Finance and Operations, og dubletrækkerne vil blive vist i Dataverse for det samme produkt.
For at undgå den i forrige afsnit refererede situation, i tilfælde af at andre Dynamics 365-apps har produkter, der overlapper hinanden/svarer til dem i Finance and Operations, skal administratoren, der aktiverer dobbeltskrivning, bootstrappe kolonnerne **Firma** (f.eks. "USMF") og **msdyn_productnumber** (f.eks. "1234:Black:S"), før produkterne synkroniseres. Med andre ord skal disse to kolonner i produktet i Dataverse udfyldes med det pågældende firma i Finance and Operations, som produktet skal sammenholdes med, og med dets produktnummer. 

Når synkroniseringen er aktiveret og finder sted, vil produkterne fra Finance and Operations blive synkroniseret med de matchende produkter i Dataverse og andre Dynamics 365-apps. Dette gælder for både specifikke produkter og produktvarianter. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Overførsel af produktdata fra andre Dynamics 365-apps til Finance and Operations

Hvis andre Dynamics 365-apps har produkter, der ikke er til stede i Finance and Operations, kan administratoren indledningsvist anvende **EcoResReleasedProductCreationV2Entity** til at importere disse produkter i Finance and Operations. Dernæst kan produktdataene fra Finance and Operations og andre Dynamics 365-apps sammenholdes som beskrevet ovenfor. 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
