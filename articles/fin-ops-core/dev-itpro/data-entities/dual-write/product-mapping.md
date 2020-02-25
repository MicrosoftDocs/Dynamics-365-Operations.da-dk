---
title: Samlet produktoplevelse
description: I dette emne beskrives integrationen af produktdata mellem Finance and Operations-apps og Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a52e8f65e7e2a8d90ddf5efa47c07d6995ef645d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019697"
---
# <a name="unified-product-experience"></a>Samlet produktoplevelse

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Når en virksomheds økosystem består af Dynamics 365-applikationer, som f.eks. Finance, Supply Chain Management og Sales, anvender virksomhederne ofte disse programmer til at levere produktdata. Det skyldes, at disse apps udgør en robust produktinfrastruktur suppleret med avancerede prissætningskoncepter og nøjagtige disponible lagerbeholdningsdata. Virksomheder, der bruger et eksternt PLM-system (Product Lifecycle Management) til at levere produktdata, kan kanalisere produkter fra Finance and Operations-apps til andre Dynamics 365-apps. Den samlede produktoplevelse overfører den integrerede produktdatamodel ind til Common Data Service, så alle programbrugere, herunder Power Platform-brugere, kan udnytte de omfattende produktdata, der kommer fra Finance and Operations-apps.

Her er produktdatamodellen fra Sales.

![Datamodel for produkter i CE](media/dual-write-product-4.jpg)

Her er produktdatamodellen fra Finance and Operations-apps.

![Datamodel for produkter i Finance and Operations](media/dual-write-products-5.jpg)

Disse to produktdatamodeller er blevet integreret i Common Data Service som vist nedenfor.

![Datamodel for produkter i Dynamics 365-apps](media/dual-write-products-6.jpg)

Enhedstilknytninger med dobbeltskrivning for produkter er designet til kun at overføre data en vej i næsten realtid fra Finance and Operations-apps til Common Data Service. Men produktinfrastrukturen er gjort åben for at gøre den tovejs, hvis det er nødvendigt. Selvom du kan tilpasse den, er det på egen risiko, da Microsoft ikke anbefaler denne fremgangsmåde.

## <a name="templates"></a>Skabeloner

Produktoplysninger indeholder alle de oplysninger, der er knyttet til produktet og dets definition, f. eks. produktdimensionerne eller sporings-og lagringsdimensionerne. Som følgende tabel viser, oprettes der en samling af enhedstilknytninger for at synkronisere produkter og relaterede oplysninger.

Finance and Operations | Andre Dynamics 365-apps | Beskrivelse
-----------------------|--------------------------------|---
Frigivne produkter V2 | msdyn\_sharedproductdetails | Enheden **msdyn\_sharedproductdetails** indeholder felterne fra Finance and Operations-apps, der definerer produktet, og som indeholder produktets økonomiske og administrative oplysninger. 
Common Data Service frigav specifikke produkter | Produkt | Enheden **Produkt** indeholder de felter, der definerer produktet. Den omfatter individuelle produkter (produkter med undertypeprodukt) og produktvarianterne. Tilknytningerne vises i følgende tabel.
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
Produktmasterfarver | msdyn_sharedproductcolors | Enheden **Delt produktfarve** angiver de farver, en bestemt produktmaster kan have. Dette begreb overflyttes til Common Data Service for at bevare data konsekvente.
Produktmasterstørrelser | msdyn_sharedproductsizes | Enheden **Delt produktstørrelse** angiver de størrelser, som en bestemt produktmaster kan have. Dette begreb overflyttes til Common Data Service for at bevare data konsekvente.
Typografier for produktmaster | msdyn_sharedproductstyles | Enheden **Delt produkttypografi** angiver de typografier, en bestemt produktmaster kan have. Dette begreb overflyttes til Common Data Service for at bevare data konsekvente.
Konfigurationer af produktmaster | msdyn_sharedproductconfigurations | Enheden **Delt produktkonfiguration** angiver de konfigurationer, en bestemt produktmaster kan have. Dette begreb overflyttes til Common Data Service for at bevare data konsekvente.
Alle produkter | msdyn_globalproducts | Enheden Alle produkter indeholder alle produkter, der er tilgængelige i Finance and Operations-apps, både i frigivne og ikke-frigivne produkter.
Enhed | uoms
Enhedsomregninger | msdyn_ unitofmeasureconversions
Konvertering af produktspecifik måleenhed | msdyn_productspecificunitofmeasureconversion
Produktkategorier | msdyn_productcategories | Hver produktkategorier og oplysninger om dens struktur og karakteristika findes i enheden produktkategori. 
Hierarkier for produktkategori | msdyn_productcategoryhierarhies | Du kan bruge produkthierarkier til at kategorisere eller gruppere produkter. Kategorihierarkierne er tilgængelige i Common Data Service ved at bruge enheden Produktkategorihierarki. 
Hierarkiroller for produktkategori | msdyn_productcategoryhierarchies | Produkthierarkier kan bruges til forskellige roller i D365 Finance and Operations. De angiver, hvilken kategori der bruges i hver rolle for enheden produktkategorirolle, som anvendes. 
Tildelinger af produktkategori | msdyn_productcategoryassignments | Du kan anvende enheden produktkategoritildeling til at tildele et produkt til en kategori.

## <a name="integration-of-products"></a>Integration af produkter

I denne model repræsenteres produktet af kombinationen af to enheder i Common Data Service: **Produkt** og **msdyn\_sharedproductdetails**. Den første enhed indeholder definitionen af et produkt (det entydige id for produktet, produktnavnet og beskrivelsen), og den anden enhed indeholder de felter, som er gemt på produktniveauet. Kombinationen af disse to enheder bruges til at definere produktet ud fra begrebet lagerenhed (SKU). Hvert af de frigivne produkter indeholder sine oplysninger i de nævnte enheder (oplysninger om produkt og delt produkt). Hvis du vil holde styr på alle produkter (frigivne og ikke-frigivne), skal du bruge enheden **Globale produkter**. 

Da produktet er repræsenteret som en SKU, kan koncepterne for specifikke produkter, produktmastere og produktvarianter registreres i Common Data Service på følgende måde:

- **Produkter med undertypeprodukt** er produkter, der defineres af dem selv. Der skal ikke defineres dimensioner. Et eksempel er en bestemt bog. For disse produkter oprettes der en post i enheden **Produkt**, og der oprettes en post i enheden **msdyn\_sharedproductdetails**. Der oprettes ingen produktfamiliepost.
- **Produktmastere** bruges som standardprodukter, der indeholder de definitioner og regler, der bestemmer funktionaliteten i forretningsprocesser. Baseret på disse definitioner kan der genereres specifikke produkter, der kaldes produktvarianter. F. eks. er T-shirt produktmasteren, og den kan have farve og størrelse som dimensioner. Der kan frigives varianter med forskellige kombinationer af disse dimensioner, f. eks. en lille blå T-shirt eller en mellem grøn T-shirt. I integrationen oprettes der én post pr. variant i produkttabellen. Denne post indeholder variantspecifikke oplysninger, f. eks. de forskellige dimensioner. De generelle oplysninger for produktet gemmes i enheden **msdyn\_sharedproductdetails**. (Disse standardoplysninger opbevares i produktmasteren). Derudover oprettes der én produktfamiliepost pr. produktmaster. Oplysningerne om produktmasteren synkroniseres med Common Data Service, så snart den frigivne produktmaster er oprettet (men før der frigives varianter).
- **Specifikke produkter** refererer til alle produkternes undertypeprodukt og alle produktvarianterne. 

![Datamodel for produkter](media/dual-write-product.png)

Når dobbeltskrivningsfunktionaliteten er aktiveret, vil apps fra Finance and Operations blive synkroniseret i andre Dynamics 365-apps i tilstanden **Kladde**. De føjes til den første prisliste med samme valuta. De føjes med andre ord til den første prisliste i en Dynamics 365-app, der har samme valuta som din juridiske enhed, hvor produktet frigives i en Finance and Operations-app. 

Som standard synkroniseres produkter fra Finance and Operations-apps til andre Dynamics 365-apps i tilstanden **Kladde**. Hvis du vil synkronisere produktet med tilstanden **Aktiv**, så du f.eks. kan bruge det direkte i salgsordretilbud, skal følgende indstilling vælges: under fanen **System> Administration > Systemadministration > Systemindstillinger > Sales** skal du vælge **Opret produkter i aktiv tilstand = ja**. 

Bemærk, at synkroniseringen af produkter sker fra Finance and Operations-apps til Common Data Service. Det betyder, at værdierne i produktenhedsfelterne kan ændres i Common Data Service, men når synkroniseringen udløses (når et produktfelt ændres i en Finance and Operations-app), overskrives værdierne i Common Data Service. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Produktdimensioner 

Produktdimensioner er egenskaber, der identificerer en produktvariant. De fire produktdimensioner (farve, størrelse, typografi og konfiguration) knyttes også til Common Data Service, så du kan definere produktvarianterne. I følgende illustration vises datamodellen for produktdimensionen Farve. Den samme model anvendes på størrelser, typografier og konfigurationer. 

![Datamodel for produkter](media/dual-write-product-2.PNG)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Når et produkt har forskellige produktdimensioner (en produktmaster har f.eks. størrelse og farve som produktdimensioner), defineres hvert specifikt produkt (dvs. de enkelte produktvarianter) som en kombination af disse produktdimensioner. Produktnummer B0001 er f.eks. en ekstra lille sort T-shirt, og produktnummer B0002 er en lille sort T-shirt. I dette tilfælde defineres de eksisterende kombinationer af produktdimensioner. F.eks. kan T-shirten fra det foregående eksempel være ekstra lille og sort, lille og sort, mellem og sort eller stor og sort, men den kan ikke være ekstrastor og sort. Det vil sige, at de produktdimensioner, en produktmaster kan antage, angives, og varianter kan frigives ud fra disse værdier.

For at holde styr på de produktdimensioner, en produktmaster kan antage, oprettes og tilknyttes følgende enheder i Common Data Service for hver produktdimension. Du kan finde flere oplysninger under [Oversigt over produktoplysninger](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Standardindstillinger for ordrer og produktspecifikke standardindstillinger for ordrer

Standardindstillinger for ordre definerer lokationen og lagerstedet, hvor varerne skal leveres fra eller oplagres, minimum-, maksimum-, flere og standardmængder, der skal bruges til handel eller lagerstyring, leveringstider, stopflaget og metoden for ordretilsagn. Disse oplysninger er tilgængelige i Common Data Service ved hjælp af standardindstillingerne for vareordrer og enheden for produktspecifikke standardindstillinger for vareordrer. Du kan finde flere oplysninger om funktionaliteten under [emnet Standardindstillinger for ordre](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Måleenhed og omregninger af måleenhed

Måleenhederne og de respektive omregninger er tilgængelige i Common Data Service i henhold til datamodellen, der vises i diagrammet.

![Datamodel for produkter](media/dual-write-product-3.PNG)

Måleenhedsbegrebet er integreret mellem Finance and Operations-apps og andre Dynamics 365-apps. For hver enhedsklasse i en Finance and Operations-app oprettes der en enhedsgruppe i en Dynamics 365-app, som indeholder de enheder, der hører til enhedsklassen. Der oprettes også en standardbasisenhed for hver enhedsgruppe. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-common-data-service"></a>Indledende synkronisering af enhedsdata der matches mellem Finance and Operations og Common Data Service

### <a name="initial-synchronization-of-units"></a>Første synkronisering af enheder

Når dobbeltskrivning er aktiveret, synkroniseres enheder fra Finance and Operations-apps til andre Dynamics 365-apps. De enhedsgrupper, der synkroniseres fra Finance and Operations-apps i Common Data Service, har et flag, der angiver, at de er "Eksternt vedligeholdte".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Data for sammenholdte enheder og enhedsklasser/-grupper fra Finance and Operations-apps og andre Dynamics 365-apps

Indledningsvist er det vigtigt at bemærke, at integrationsnøglen for enheden er msdyn_symbol. Derfor skal denne værdi være entydig i Common Data Service eller andre Dynamics 365-apps. Da det i andre Dynamics 365-apps er det parrede "Enhedsgruppe-id" og "Navn", der definerer en enheds entydighed, skal du overveje forskellige scenarier for at kunne sammenligne enhedsdata mellem Finance and Operations-apps og Common Data Service.

For enheder, der matcher/overlapper i Finance and Operations-apps og andre Dynamics 365-Apps:

+ **Enheden tilhører en enhedsgruppe i andre Dynamics 365-apps, der svarer til den tilknyttede enhedsklasse i Finance and Operations-apps**. I dette tilfælde skal feltet msdyn_symbol i andre Dynamics 365-apps udfyldes med enhedssymbolet fra Finance and Operations-apps. Når dataene bliver sammenholdt, vil enhedsgruppen derfor blive angivet som "Eksternt vedligeholdt" i andre Dynamics 365-apps.
+ **Enheden tilhører en enhedsgruppe i andre Dynamics 365-apps, der ikke svarer til den tilknyttede enhedsklasse i Finance and Operations-apps (ingen eksisterende enhedsklasse i Finance and Operations-apps for enhedsklassen i andre Dynamics 365-apps).** I dette tilfælde skal msdyn_symbol udfyldes med en tilfældig streng. Bemærk, at denne værdi skal være entydig i andre Dynamics 365-apps.

For enheder og enhedsklasser i Finance and Operations, der ikke findes i andre Dynamics 365-Apps:

Som en del af dobbeltskrivning er enhedsgrupperne fra Finance and Operations-apps og tilsvarende enheder oprettet og synkroniseret i andre Dynamics 365-apps samt Common Data Service, og enhedsgruppen angives som "Eksternt vedligeholdt". Der kræves ikke nogen ekstra bootstrapping.

For enheder i andre Dynamics 365-apps, som ikke findes i Finance and Operations-apps:

Feltet msdyn_symbol skal udfyldes for alle enheder. Enhederne kan altid oprettes i Finance and Operations-apps i den tilhørende enhedsklasse (hvis den findes). Hvis enhedsklassen ikke findes, skal enhedsklassen først oprettes (bemærk, at du ikke kan oprette en enhedsklasse i Finance and Operations-apps undtagen via udvidelse, hvis du udvider fastteksten), så den stemmer overens med enhedsgruppen for de andre Dynamics 365-apps. Dernæst kan du oprette enheden. Bemærk, at enhedssymbolet i Finance and Operations-apps skal være det tidligere angivne msdyn_symbol i andre Dynamics 365-apps for enheden.

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

Til entydig identifikation af produkter mellem Dynamics 365 for Finance and Operations og produkter i Common Data Service anvendes integrationsnøgler. For produkter er **(produktnummer)** den entydige nøgle, der identificerer et produkt i Common Data Service. Den er sammensat af sammenkædningen af: **(firma, msdyn_produktnummer)**. **Firmaet** angiver den juridiske enhed i Finance and Operations, og **msdyn_productnumber** angiver produktnummeret for det specifikke produkt i Finance and Operations. 

For en anden bruger af Dynamics 365-apps identificeres produktet i brugergrænsefladen med **msdyn_produktnummer** (bemærk, at etiketten for feltet er **Produktnummer**). I produktformularen vises både firmaet og msydn_produktnummeret. Men i feltet (produktnummer) vises den entydige nøgle for et produkt ikke. 

Bemærk, at hvis der bygges apps ovenpå Common Data Service, bør du være særlig opmærksom på, at du anvender det (produktnummmer), der er det entydige produkt-ID, som integrationsnøglen, og ikke msdyn_produktnummer, idet den sidstnævnte ikke er entydig. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-common-data-service-to-finance-and-operations"></a>Første synkronisering af produkter og migrering af data fra Common Data Service til Finance and Operations

### <a name="initial-synchronization-of-products"></a>Første synkronisering af produkter 

Når dobbeltskrivning er aktiveret, synkroniseres produkter fra Dynamics 365 Finance and Operations til Common Data Service og andre Dynamics 365-apps. Bemærk, at produkter oprettet i Common Data Service og andre Dynamics 365-apps forud for dobbeltskrivning, ikke bliver opdateret eller sammenlignet med produktdata fra Finance and Operations.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Sammenligning af produktdata fra Finance and Operations og andre Dynamics 365-apps

Hvis de samme produkter lagres (overlappende/matchende) i Finance and Operations og i Common Data Service samt andre Dynamics 365-apps, når dobbeltskrivning aktiveres, synkroniseres produkter fra Finance and Operations, og dubletposterne vil blive vist i Common Data Service for det samme produkt.
For at undgå den i forrige afsnit refererede situation, i tilfælde af at andre Dynamics 365-apps har produkter, der overlapper hinanden/svarer til dem i Finance and Operations, skal administratoren, der aktiverer dobbeltskrivning, bootstrappe felterne **Firma** (f.eks. "USMF") og **msdyn_productnumber** (f.eks. "1234:Black:S"), før produkterne synkroniseres. Med andre ord skal disse to felter i produktet i Common Data Service udfyldes med det pågældende firma i Finance and Operations, som produktet skal sammenholdes med, og med dets produktnummer. 

Når synkroniseringen er aktiveret og finder sted, vil produkterne fra Finance and Operations blive synkroniseret med de matchende produkter i Common Data Service og andre Dynamics 365-apps. Dette gælder for både specifikke produkter og produktvarianter. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Overførsel af produktdata fra andre Dynamics 365-apps til Finance and Operations

Hvis andre Dynamics 365-apps har produkter, der ikke er til stede i Finance and Operations, kan administratoren indledningsvist anvende **EcoResReleasedProductCreationV2Entity** til at importere disse produkter i Finance and Operations. Dernæst kan produktdataene fra Finance and Operations og andre Dynamics 365-apps sammenholdes som beskrevet ovenfor. 
