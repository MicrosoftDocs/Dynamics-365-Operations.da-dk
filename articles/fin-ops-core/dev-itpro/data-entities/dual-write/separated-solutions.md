---
title: Separat orkestreringspakke med program til dobbeltskrivning
description: Dobbeltskrivningsprogrammets orkestreringspakke er ikke længere en enkelt pakke, men er adskilt i mindre pakker. Denne artikel indeholder en forklaring på de løsninger og tilknytninger, som hver enkelt pakke indeholder, og dens afhængighed af andre pakker.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 504939f1f98c18005c092cabc1d040b420402c93
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874806"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Separat orkestreringspakke med program til dobbeltskrivning

[!include [banner](../../includes/banner.md)]



Tidligere var dobbeltskrivningsprogrammets orkestreringspakke en enkelt pakke, der indeholdt følgende løsninger:

- Dynamics 365 Notes
- Dynamics 365 Finans og drift Common Anchor
- Dynamics 365 Finans og drift Dual Write Entity Maps
- Dynamics 365 Aktivadministration-app
- Dynamics 365 Aktivadministration
- HCM, fælles
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 Finans og drift Common
- Dynamics 365 Company
- Valutakurser
- Field Service Common

Da den var en enkelt pakke, oprettede denne pakke en "alt eller intet"-situation for kunderne. Men Microsoft har nu adskilt den i mindre pakker. Kunderne kan derfor kun vælge pakkerne til de løsninger, de skal bruge. Hvis du f.eks. er kunde med Microsoft Dynamics 365 Supply Chain Management og ikke har brug for integration med Dynamics 365 Human Resources, noter og aktivstyring, kan du udelukke disse løsninger fra de løsninger, der er installeret. Da de underliggende løsningsnavne, udgivere og tilknyttede versioner forbliver de samme, er denne en ikkeforstyrrende ændring. Eksisterende installationer opgraderes.

![Adskilt pakke.](media/separated-package-1.png)

Denne artikel indeholder en forklaring på de løsninger og tilknytninger, som hver enkelt pakke indeholder, og dens afhængighed af andre pakker.

## <a name="dual-write-application-core"></a>Programkerne til dobbeltskrivning

Med pakken Programkerne til dobbeltskrivning kan brugerne installere og konfigurere dobbeltskrivning uden nogen kundeengagementsapp. Den indeholder følgende fem løsninger.

| Entydigt navn                           | Vist navn                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 Company                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finans og drift Common |
| CurrencyExchangeRates                 | Valutakurser                    |
| msdyn_DualWriteAppCoreMaps            | Enhedstilknytninger for programkerne til dobbeltskrivning   |
| msdyn_DualWriteAppCoreAnchor          | Programkerneanker til dobbeltskrivning        |

Følgende tilknytninger er tilgængelige i denne pakke:

| Finans og drift-apps     | Kundeengagementapps                    |
|---------------------------------|---------------------------------------------|
| Driftsenhed                  | msdyn_internalorganizations                 |
| Organisationshierarki          | msdyn_internalorganizationhierarchies       |
| Juridiske enheder                  | msdyn_internalorganizations                 |
| Juridiske enheder                  | cdm_companies                               |
| Formål med organisationshierarkier | msdyn_internalorganizationhierarchypurposes |
| Valutapar for valutakurser     | msdyn_currencyexchangeratepairs             |
| Foranstillede navne                    | msdyn_nameaffixes                           |
| Valutakurstype              | msdyn_exchangeratetypes                     |
| CDS-valutakurser              | msdyn_currencyexchangerates                 |
| Type af organisationshierarki     | msdyn_internalorganizationhierarchytypes    |
| Valutaer                      | handelsvaluta                       |
| Enhed for mixed reality-guider     | msmrw_guides                                |

**Oplysninger om afhængighed**

Pakken Programkerne til dobbeltskrivning har ingen afhængighed af andre pakker.

## <a name="dual-write-human-resources"></a>Dobbeltskrivning til Human Resources

Pakken Dobbeltskrivning til Human Resources indeholder de løsninger og tilknytninger, der er nødvendige for at synkronisere Human Resources-data. Den indeholder følgende tre løsninger.

| Entydigt navn                | Vist navn                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM, fælles                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources-enhedstilknytninger |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources-anker      |

Følgende tilknytninger er tilgængelige i denne pakke:

| Finans og drift-apps | Kundeengagementapps         |
|-----------------------------|----------------------------------|
| Etnisk oprindelse              | cdm_ethnicorigins                |
| Kompensation - jobfunktion   | cdm_jobfunctions                 |
| Stillinger V2                | cdm_jobpositions                 |
| Job                        | cdm_jobs                         |
| Kompensation - jobtype       | cdm_jobtypes                     |
| Sprogkoder              | cdm_languages                    |
| Stillingstype               | cdm_positiontypes                |
| Arbejderopgaver for stilling | cdm_positionworkerassignmentmaps |
| Veteranstatus              | cdm_veteranstatuses              |
| Arbejdstråd                      | cdm_workers                      |
| Ansættelse pr. firma      | cdm_employments                  |

**Oplysninger om afhængighed**

Pakken Dobbeltskrivning til Human Resources afhænger af pakken Programkerne til dobbeltskrivning. Du skal derfor installere pakken Programkerne til dobbeltskrivning, før du installerer pakken Dobbeltskrivning til Human Resources.

## <a name="dual-write-supply-chain"></a>Dobbeltskrivning til forsyningskæde

Pakken Dobbeltskrivning til forsyningskæde indeholder de løsninger og tilknytninger, der er nødvendige for at synkronisere Supply Chain Management-data. Den indeholder følgende tre løsninger.

| Entydigt navn                                | Vist navn                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management-udvidede enhedstilknytninger |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management-udvidet anker      |

Følgende tilknytninger er tilgængelige i denne pakke:

| Finans og drift-apps                 | Kundeengagementapps                      |
|---------------------------------------------|-----------------------------------------------|
| Objekter                                       | uoms                                          |
| CDS-salgsordrehoveder                     | salesorders                                   |
| CDS-salgsordrelinjer                       | salesorderdetails                             |
| CDS-salgstilbudshoved                  | pristilbud                                        |
| CDS-salgstilbudslinjer                   | quotedetails                                  |
| Frigivne specifikke produkter i CDS              | produkter                                      |
| Lagerstedszoner                             | msdyn_warehousezones                          |
| Lagerstedszonegrupper                       | msdyn_warehousezonegroups                     |
| Linjer for lagerstedsarbejde                        | msdyn_warehouseworklines                      |
| Overskrifter for lagerstedsarbejde                      | msdyn_warehouseworkheaders                    |
| Lagersteder                                  | msdyn_warehouses                              |
| Lagergang                             | msdyn_warehouseaisles                         |
| Enhedsomregninger                            | msdyn_unitofmeasureconversions                |
| Leveringsbetingelse                           | msdyn_termsofdeliveries                       |
| Leveringsmåder                           | msdyn_shipvias                                |
| Typografier for produktmaster                       | msdyn_sharedproductstyles                     |
| Salgsfakturalinjer V2                      | invoicedetails                                |
| Salgsfakturahoveder V2                    | fakturaer                                      |
| Produktmasterstørrelser                        | msdyn_sharedproductsizes                      |
| Frigivne produkter V2                        | msdyn_sharedproductdetails                    |
| Konfigurationer af produktmaster               | msdyn_sharedproductconfigurations             |
| Produktmasterfarver                       | msdyn_sharedproductcolors                     |
| Koder for salgsordreoprindelse                    | msdyn_salesorderorigins                       |
| Hoved til produktkvittering                      | msdyn_purchaseorderreceipts                   |
| Produktkvitteringslinje                        | msdyn_purchaseorderreceiptproducts            |
| Indkøbsordrehoveder V2                   | msdyn_purchaseorders                          |
| Foreløbig slettet enhed for CDS-indkøbsordrelinje | msdyn_purchaseorderproducts                   |
| Enhed for CDS-indkøbsordrelinje              | msdyn_purchaseorderproducts                   |
| Sporingsdimensionsgrupper                   | msdyn_producttrackingdimensiongroups          |
| Typer                                      | msdyn_productstyles                           |
| Lagringsdimensionsgrupper                    | msdyn_productstoragedimensiongroups           |
| Produktspecifikke enhedsomregninger           | msdyn_productspecificunitofmeasureconversions |
| Standardindstillinger for produktordrer V2           | msdyn_productspecificdefaultordersettings     |
| Størrelser                                       | msdyn_productsizes                            |
| Produktdimensionsgrupper                    | msdyn_productdimensiongroups                  |
| Standardindstillinger for ordre                      | msdyn_productdefaultordersettings             |
| Konfigurationer                              | msdyn_productconfigurations                   |
| Alle produkter                                | msdyn_globalproducts                          |
| Farver                                      | msdyn_productcolors                           |
| Hierarkiroller for produktkategori            | msdyn_productcategoryhierarchyroles           |
| Hierarkier for produktkategori                | msdyn_productcategoryhierarchies              |
| Tildelinger af produktkategori                | msdyn_productcategoryassignments              |
| Produktkategorier                          | msdyn_productcategories                       |
| Lagerstedslokationer                         | msdyn_inventorylocations                      |
| CDS-lager på                            | msdyn_inventoryonhandentries                  |
| Produktkategorier                          | msdyn_productcategories                       |
| CDS-lager på                            | msdyn_inventoryonhandrequests                 |
| Stregkode identificeret ud fra produktnummer           | msdyn_productbarcodes                         |
| Fordelskundekort                                | msdyn_loyaltycards                            |
| Fordelskundebelønningspoint                       | msdyn_loyaltyrewardpoints                     |
| Kundeprisgrupper                       | msdyn_pricecustomergroups                     |
| Steder                                       | msdyn_operationalsites                        |
| CDS-salgstilbudslinjer                   | quotedetails                                  |
| CDS-salgsordrelinjer                       | salesorderdetails                             |

**Oplysninger om afhængighed**

Pakken Dobbeltskrivning til forsyningskæde afhænger af følgende tre pakker. Du skal derfor installere disse pakker, før du installerer pakken Dobbeltskrivning til forsyningskæde.

- Pakken Programkerne til dobbeltskrivning
- Pakken Dobbeltskrivning til Finance
- Pakken Dobbeltskrivning til Human Resources

## <a name="dual-write-finance"></a>Dobbeltskrivning til Finance

Pakken Dobbeltskrivning til Finance indeholder de løsninger og tilknytninger, der er nødvendige for at synkronisere Dynamics 365 Finance-data. Den indeholder følgende fire løsninger.

| Entydigt navn                            | Vist navn                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance Extended-enhedskort |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance Extended-anker      |

Følgende tilknytninger er tilgængelige i denne pakke:

| Finans og drift-apps             | Kundeengagementapps        |
|-----------------------------------------|---------------------------------|
| Grupper for indeholdt skat                  | msdyn_withholdingtaxgroups      |
| CDS kontakter V2 (kunde)              | kontakter                        |
| CDS kontakter V2 (leverandør)                | kontakter                        |
| Debitorer V3                            | kontakter                        |
| Koder for indeholdt skat                   | msdyn_withholdingtaxcodes       |
| Kreditorer V2                              | msdyn_vendors                   |
| Kreditorbetalingsmetode                   | msdyn_vendorpaymentmethods      |
| Kreditorgrupper                           | msdyn_vendorgroups              |
| Kontoplan                       | msdyn_chartofaccountses         |
| Momsfinanskonteringsgrupper V2      | msdyn_taxpostinggroups          |
| Varemomsgruppe                    | msdyn_taxitemgroups             |
| Momsgrupper                        | msdyn_taxgroups                 |
| Enhed for momsfritagelseskode i CDS        | msdyn_taxexemptcodes            |
| Debitorgrupper                         | msdyn_customergroups            |
| Debitorbetalingsmetode                 | msdyn_customerpaymentmethods    |
| Økonomiske dimensioner                    | msdyn_dimensionattributes       |
| Momsmyndigheder                   | msdyn_taxauthorities            |
| Format af økonomisk dimension              | msdyn_financialdimensionformats |
| Regnskabskalenderperiode                  | msdyn_fiscalcalendarperiods     |
| Enhed for regnskabskalenderintegration      | msdyn_fiscalcalendars           |
| Enhed for regnskabskalenderårsintegration | msdyn_fiscalcalendaryears       |
| Betalingsbetingelse                        | msdyn_paymentterms              |
| Betalingsplan                        | msdyn_paymentschedules          |
| Betalingsplanlinjer                  | msdyn_paymentschedulelines      |
| Betalingsdage CDS                        | msdyn_paymentdays               |
| Betalingsdagslinjer CDS V2                | msdyn_paymentdaylines           |
| Hovedkonto                            | msdyn_mainaccounts              |
| Hovedkontokategorier                 | msdyn_mainaccountcategories     |
| Ledger                                  | msdyn_ledgers                   |
| Debitorer V3                            | konti                        |

**Oplysninger om afhængighed**

Pakken Dobbeltskrivning til Finance afhænger af pakken Programkerne til dobbeltskrivning. Du skal derfor installere pakken Programkerne til dobbeltskrivning, før du installerer pakken Dobbeltskrivning til Finance.

## <a name="dual-write-notes"></a>Dobbeltskrivning til Notes

Pakken Dobbeltskrivning til Notes indeholder de løsninger og tilknytninger, der er nødvendige for at synkronisere note- og anmærkningsdata. Den indeholder følgende fire løsninger.

| Entydigt navn                  | Vist navn                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Dynamics 365-noter udvidet    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365-noters enhedstilknytninger |
| msdyn_Dynamics365NotesAnchor | Dynamics 365-noteanker      |

Følgende tilknytninger er tilgængelige i denne pakke:

| Finans og drift                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Vedhæftede dokumenter til salgsordrehoved    | anmærkninger         |
| Vedhæftede filer for debitorer                       | anmærkninger         |
| Vedhæftede kreditordokumenter                | anmærkninger         |
| Vedhæftede dokumenter til indkøbsordrehoved | anmærkninger         |

**Oplysninger om afhængighed**

Pakken Dobbeltskrivning til Notes afhænger af følgende to pakker. Du skal derfor installere disse pakker, før du installerer pakken Dobbeltskrivning til Notes.

- Pakken Programkerne til dobbeltskrivning
- Pakken Dobbeltskrivning til Finance

## <a name="dual-write-asset-management"></a>Dobbeltskrivning til Aktivadministration

Pakken Dobbeltskrivning til Aktivadministration indeholder de løsninger og tilknytninger, der er nødvendige for at synkronisere data fra Supply Chain Management eller Dynamics 365 Field Service. Den indeholder følgende fire løsninger.

| Entydigt navn                          | Vist navn                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 Aktivadministration             |
| Dynamics365AssetManagementApp        | Dynamics 365 Aktivadministration-app          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 Aktivadministration-enhedstilknytninger |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 Aktivadministration-anker      |

Følgende tilknytninger er tilgængelige i denne pakke:

| Finans og drift-apps                           | Kundeengagementapps                |
|-------------------------------------------------------|-----------------------------------------|
| Garanti af Aktivadministration                             | msdyn_warranties                        |
| Modeller i Aktivadministration                               | msdyn_models                            |
| Producenter i Aktivadministration                        | msdyn_manufacturers                     |
| Funktionelle placeringstyper i Aktivadministration            | msdyn_functionallocationtypes           |
| Funktionelle placeringer i Aktivadministration                 | msdyn_functionallocations               |
| Livcyklustilstande til funktionel placering i Aktivadministration | msdyn_functionallocationlifecyclestates |
| Livcyklusmodeller til funktionel placering i Aktivadministration | msdyn_functionallocationlifecyclemodels |
| Aktiver i Aktivadministration                               | msdyn_customerassets                    |
| Aktivtyper i Aktivadministration                          | msdyn_customerassetcategories           |
| Aktivlivscyklustilstande i Aktivadministration               | msdyn_assetlifecyclestates              |
| Aktivlivscyklusmodeller i Aktivadministration               | msdyn_assetlifecyclemodels              |

**Oplysninger om afhængighed**

Pakken Dobbeltskrivning til Aktivadministration afhænger af pakken Programkerne til dobbeltskrivning. Du skal derfor installere pakken Programkerne til dobbeltskrivning, før du installerer pakken Dobbeltskrivning til Aktivadministration.

## <a name="packages-required-for-project-operations"></a>Pakker, der kræves til Project Operations
Project Operations afhænger af følgende pakker. Du skal derfor installere disse pakker, før du installerer Project Operations.

- Pakken Programkerne til dobbeltskrivning
- Pakken Dobbeltskrivning til Finance
- Pakken Dobbeltskrivning til forsyningskæde
- Pakken Dobbeltskrivning til Aktivadministration
- Pakken Dobbeltskrivning til Human Resources

## <a name="dual-write-party-and-global-address-book-solutions"></a>Løsninger til dobbeltskrivningspart og globalt adressekartotek

Pakken til dobbeltskrivningspart og globalt adressekartotek indeholder følgende løsninger og kort, som er nødvendige for at synkronisere data til parten og det globale adressekartotek. 

| Entydigt navn                       | Vist navn                            |
|-----------------------------------|-----------------------------------------|
| Part                             | Part                                   |
| Dynamics365GABExtended            | Dynamics 365 GAB Extended               |
| Dynamics365GABDualWriteEntityMaps | Dynamics 365 GAB Dual Write Entity Maps |
| Dynamics365GABParty_Anchor        | Dynamics 365 GAB and Party              |

Følgende tilknytninger er tilgængelige i denne pakke:

| Finans og drift-apps | Kundeengagementapps | 
|-----------------------------|--------------------------|
| CDS-parter | msdyn_parties | 
| Lokaliteter for CDS-postadresse | msdyn_postaladdresscollections | 
| Oversigt over CDS-postadresse V2 | msdyn_postaladdresses | 
| Lokaliteter for CDS-parts postadresse | msdyn_partypostaladdresses | 
| Partkontakter V3 | msdyn_partyelectronicaddresses | 
| Debitorer V3 | konti | 
| Debitorer V3 | kontakter | 
| Kreditorer V2 | msdyn_vendors | 
| Titler på kontaktpersoner | msdyn_salescontactpersontitles | 
| Afsluttende hilsner | msdyn_complimentaryclosings | 
| Tiltaleformer | msdyn_salutations | 
| Beslutningstagerrolle | msdyn_decisionmakingroles | 
| Ansættelsesjobfunktioner | msdyn_employmentjobfunctions | 
| Loyalitetsniveauer | msdyn_loyaltylevels | 
| Personlige tegntyper | msdyn_personalcharactertypes | 
| Kontakter V2 | msdyn_contactforparties | 
| CDS-salgstilbudshoved | pristilbud | 
| CDS-salgsordrehoveder | salesorders | 
| Salgsfakturahoveder V2 | fakturaer | 
| CDS-adresseroller | msdyn_addressroles |

**Oplysninger om afhængighed**

Løsningerne til dobbeltskrivningspart og den globale adressebog afhænger af følgende tre pakker. Du skal derfor installere disse pakker, før du installerer pakken med løsninger til dobbeltskrivningspart og globalt adressekartotek.

- Pakken Programkerne til dobbeltskrivning
- Pakken Dobbeltskrivning til Finance
- Pakken Dobbeltskrivning til forsyningskæde
