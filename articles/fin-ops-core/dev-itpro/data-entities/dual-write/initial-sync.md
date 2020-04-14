---
title: Enhedsafhængighedskæde (synkroniseringsrækkefølge)
description: Dette emne angiver den synkroniseringsrækkefølge, du skal følge for at oprette de første data.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 4adb2c8d57ad8f67346b8d34212b7a4b0bd052ab
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173125"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Enhedsafhængighedskæde (synkroniseringsrækkefølge)

[!include [banner](../../includes/banner.md)]



I følgende tabeller vises enhederne i den rækkefølge, du skal aktivere dem. Når du aktiverer en tilknytning til første synkronisering, registrerer Dobbeltskrivning automatisk andre tilknytninger, der skal aktiveres. Du kan bruge siden **Dobbeltskrivning** i Finance and Operations-apps til at vælge eller annullere valgte enheder under den første synkronisering.

I den seneste version af Dobbeltskrivning kan du kun aktivere nogle enheder, og afhængighederne håndteres for dig.

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management-enheder

Følgende enheder til Supply Chain Management vises i den rækkefølge, du skal aktivere dem.

| Navn på tilknytning på siden Dobbeltskrivning | Navn på enhedsmetadata i Supply Chain Management | Navn på enhedsmetadata i Common Data Service | Notater |
|---|---|---|---|
| Enheder ... uoms                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| Enhedsomregninger ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Alle produkter ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Produktdimensionsgrupper ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Lagringsdimensionsgrupper ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Sporingsdimensionsgrupper ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Farver ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Størrelser ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Typografier ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Konfigurationer ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Frigivne produkter V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service-frigivne specifikke produkter ... products                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | produkt                                      | |
| Stregkode identificeret ud fra produktnummer ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Standardindstillinger for ordre ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Standardindstillinger for produktordrer V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Produktspecifikke enhedsomregninger ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Websteder ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Lagersteder ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Se [note 1](#scm-notes). |
| Produktmasterfarver ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Produktmasterstørrelser ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Typografier for produktmaster ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Konfigurationer af produktmaster ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Produktkategorier ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | Se [note 2](#scm-notes). |
| Tildelinger af produktkategori ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Hierarkier for produktkategori ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Hierarkiroller for produktkategori ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Lagergang ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Lagerstedszoner ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Lagerstedszonegrupper ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Lagerstedslokationer ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Se [note 3](#scm-notes). |
| Arbejdshoveder for lagersted ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Arbejdslinjer for lagersted ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Se [note 4](#scm-notes). |
| Leveringsmåder ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Leveringsbetingelser ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Koder for salgsordreoprindelse ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Service-salgsordrehoveder ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| Common Data Service-salgsordrelinjer ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| Common Data Service-salgstilbudshoved ... quotes                               | SalesQuotationHeaderCommon Data ServiceEntity          | quote                                        | |
| Common Data Service-salgstilbudslinjer ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Salgsfakturahoveder V2 ... invoices                                               | SalesInvoiceHeaderV2Entity                             | invoice                                      | |
| Salgsfakturalinjer V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Tilknytningsspecifikke noter

1. På grund af selv-afhængighed kan det være nødvendigt at køre den første synkronisering to gange.
2. Den første synkronisering er som standard slået fra på grund af den overordnede/underordnede relation ("intelligent" sortering ikke håndteres af platformen). De eksisterende produktkategorier skal derfor synkroniseres manuelt (f.eks. ved at opdatere beskrivelsen af kategorien) i den korrekte rækkefølge (rodkategorien først, derefter underordnede og derefter underordnede til underordnede). Gå til **Administration af produktoplysninger \> Opsætning \> Kategorier og attributter \> Kategorihierarkier**. På siden **Kategorihierarkier** kan du vælge hvert enkelt hierarki og se produktkategorierne i det.
3. Tilknytningen af tomme **ItemNumberInLocation**-opslagsfelter og de første, anden og tredje ekstra lagerstedszoner medfører, at den første synkronisering mislykkes. Derfor er disse tilknytninger fjernet indtil videre.
4. Tilknytningen af det tomme **CaptureWeight**-felt medfører, at første synkronisering mislykkes. Derfor er denne tilknytning fjernet indtil videre.

### <a name="setup-related-information"></a>Opsætningsrelaterede oplysninger

+ Når der oprettes poster første gang i enheden **Produkter** i modelbaserede apps i Dynamics 365, har de status **Kladde**. Hvis du vil ændre status til **Aktiv**, skal du gå til **Indstillinger \> Administration \> Systemindstillinger \> Salg** i den modelbaserede app og vælge **Ja** i indstillingen **Opret produkter i aktiv tilstand**.
+ Hvis du opretter poster i enheden **Produkter** i modelbaserede apps i Dynamics 365 eller i Common Data Service, inden du aktiverer Dobbeltskrivning, vil disse poster kun blive opdateret, hvis hele nøglen, herunder **Firma**, svarer til data i Finance and Operations-appen.
+ Synkroniseringen af enheden **Produkter** er envejs og går fra Finance and Operations-apps til Common Data Service. Hvis et tilknyttet felt i enheden **Produkter** i modelbaserede apps i Dynamics 365 opdateres, overskrives opdateringen ved næste synkronisering fra Finance and Operations-appen.

### <a name="known-issues"></a>Kendte problemer

- Der opstår en fejl, når en enhed slettes i en Finance and Operations-app. Når måleenheder synkroniseres fra Finance and Operations-appen til Common Data Service, oprettes den første enhed i en bestemt klasse som den primære enhed, og den vil forhindre sletning.

    **Afhjælpning:** Du skal først slette enheden i Common Data Service. Den kan derefter slettes i Finance and Operations-appen.

- Der opstår en fejl, når et operationelt sted slettes i en Common Data Service-app. Fejlmeddelelsen angiver, at "Infolog: Advarsel: Den primære adresse ikke kan slettes.; Advarsel! enhedsposten kunne ikke slettes, da valideringen mislykkedes for følgende datakilde: InventSiteLogisticsLocation (InventSiteLogisticsLocation)". Denne fejl skyldes et problem i dataenheden i Finance and Operations-appen.

    **Afhjælpning:** Du kan slette stedet i Finance and Operations-appen. Stedet slettes derefter i Common Data Service, hvis den tilsvarende dobbeltskrivningstilknytning kører.

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance-enheder

Følgende enheder for Dynamics 365 Finance vises i den rækkefølge, du skal aktivere dem.

| Navn på tilknytning på siden Dobbeltskrivning | Navn på enhedsmetadata i Finance | Navn på enhedsmetadata i Common Data Service | Noter |
|---|---|---|---|
| Valutaer ... transactioncurrencies                                            | CurrencyEntity                              | Valuta                                   | |
| Valutakurstype ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Valutapar for valutakurser ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Common Data Service-valutakurser ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | Se [note 1](#fin-notes). |
| Integrationsenhed for regnskabskalender ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Integrationsenhed for regnskabsår ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Regnskabskalenderperiode ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Organisationshierarkitype ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Se [note 1](#fin-notes). |
| Formål med organisationshierarkier ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Se [note 1](#fin-notes). |
| Juridiske enheder ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | Se [note 1](#fin-notes). |
| Juridiske enheder ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Driftsenhed ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Se [note 1](#fin-notes). |
| Organisationshierarki – publiceret ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Se [note 1](#fin-notes). |
| Foranstillede navne ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Betalingsdage Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Betalingsdagslinjer Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Betalingsplan ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Betalingsplanlinjer ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Betalingsbetingelser ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Debitorbetalingsmetode ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Kreditorbetalingsmetode ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Debitorgrupper ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Kreditorgrupper ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| Momsgrupper ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Varemomsgrupper ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| Momsfinanskonteringsgrupper V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Enhed for momsfritagelseskode Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| Momsmyndigheder ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| Momskode ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Se [note 1](#fin-notes). |
| Økonomisk dimensionsformat ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Økonomiske dimensioner ... msdyn_dimensionattributes                              | DimensionAttributEnhed                    | msdyn_dimensionattribute                   | |
| Grupper for indeholdt skat ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Koder for indeholdt skat ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Kontoplan ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Finans ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Se [note 1](#fin-notes). |
| Hovedkontokategorier ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Hovedkonto ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Debitorer V3 ... konti                                                       | CustCustomerV3Entity                        | account                                    | Se [note 2](#fin-notes). |
| Debitorer V3 ... kontakter                                                       | CustCustomerV3Entity                        | contact                                    | Se [note 3](#fin-notes). |
| Kreditorer V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Se [note 2](#fin-notes). |
| Common Data Service-kontakter V2 ... contacts                                    | smmContactPersonCommon Data ServiceV2Entity | contact                                    | Se [note 4](#fin-notes). |
| Common Data Service-kontakter V2 ... contacts                                    | smmContactPersonCommon Data ServiceV2Entity | contact                                    | Se [note 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Tilknytningsspecifikke noter

1. Envejs synkronisering sker fra Finance and Operations-apps til Common Data Service.
2. På grund af selv-afhængighed kan det være nødvendigt at køre den første synkronisering mere end én gang. Sørg for at vælge **Debitor** som relationstype, når du opretter en konto ved hjælp af siden **Konti** i Common Data Service. Hvis du får problemer med feltet **Primær kontaktperson** under den første synkronisering, skal du fjerne dette felt fra tilknytningen og derefter køre den første synkronisering igen. Når den første synkronisering er gennemført, skal du stoppe tilknytningen og føje feltet **Primær kontaktperson** til den igen. Start derefter tilknytningen, men spring den første synkronisering over. Værdien i feltet **Primær kontaktperson** medtages ikke i den første synkronisering, og du skal overføre værdierne manuelt.
3. Vælg **Ja** i indstillingen **Salgbar** på siden **Kontaktpersoner** i Common Data Service, når du forsøger at oprette en kunde af typen **Person**.
4. Denne tilknytning har et filter i begge sider til sammenkædning af debitorkontaktpersoner. Åbn tilknytningsdetaljerne, og vælg filterknappen (tragtformet) ud for enhedsnavnet **Sales.Contact**, og kontroller, at de angivne filterkriterier indeholder **msdyn_contactforvendor eq true and msdyn_sellable eq false**.
5. Denne tilknytning har et filter i begge sider til sammenkædning af kreditorkontaktpersoner. Åbn tilknytningsdetaljerne, og vælg filterknappen (tragtformet) ud for enhedsnavnet **Sales.Contact**, og kontroller, at de angivne filterkriterier indeholder **msdyn_contactforvendor eq true and msdyn_sellable eq false**. 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources-enheder

Følgende enheder for Dynamics 365 Human Resources vises i den rækkefølge, du skal aktivere dem.

| Navn på tilknytning på siden Dobbeltskrivning | Navn på enhedsmetadata i Human Resources | Navn på enhedsmetadata i Common Data Service | Noter |
|---|---|---|---|
| cdm_jobfunction - Jobfunktion                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - Jobtyper                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - Job                                               |                                   | cdm_jobs                         | |
| cdm_jobs - Jobdetaljer                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - Stillingstype                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - Basisstilling                              | HcmPositionBaseEntity             | cdm_jobposition                  | Se [note 1](#hr-notes). |
| cdm_jobposition - Detaljer for stilling                            | HcmPositionDetailEntity           | cdm_jobposition                  | Se [note 1](#hr-notes). |
| cdm_jobposition - Stillings varighed                           | HcmPositionDurationEntity         | cdm_jobposition                  | Se [note 1](#hr-notes). |
| cdm_jobposition - Stillingshierarkier                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Se [note 1](#hr-notes). |
| cdm_veteranstatus - Veteranstatus                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - Etnisk oprindelse                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - Sprogkode                              |                                   | cdm_languagecode                 | |
| cdm_worker - Arbejder                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - Ansættelser                                 |                                   | cdm_employments                  | |
| cdm_employments - Detaljer om ansættelse                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - Arbejdertildeling til stilling | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Se [note 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Tilknytningsspecifikke noter

1. En Common Data Service-enhed er knyttet til flere Finance and Operations-appenheder.
2. Denne tilknytning har en reference til sig selv.

## <a name="asset-management-entities"></a>Enheder til Aktivadministration

Følgende enheder til Aktivadministration i Dynamics 365 Supply Chain Management vises i den rækkefølge, du skal aktivere dem.

| Navn på tilknytning på siden Dobbeltskrivning | Navn på enhedsmetadata i Aktivadministration | Navn på enhedsmetadata i Common Data Service | Noter |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Aktivlivscyklustilstande i Aktivadministration               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Aktivlivscyklusmodeller i Aktivadministration               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Livcyklusmodeller til funktionel placering i Aktivadministration | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Livcyklustilstande til funktionel placering i Aktivadministration | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Aktivtyper i Aktivadministration                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Funktionelle placeringstyper i Aktivadministration            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Funktionelle placeringer i Aktivadministration                 | msdyn_functionallocations                | Se [noten](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Aktiver i Aktivadministration                               | msdyn_customerassets                     | Se [noten](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Producenter i Aktivadministration                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Modeller i Aktivadministration                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Garanti af Aktivadministration                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Tilknytningsspecifikke noter

- På grund af selv-afhængighed kan det være nødvendigt at køre den første synkronisering mere end én gang.
