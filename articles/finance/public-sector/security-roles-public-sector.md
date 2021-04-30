---
title: Sikkerhedsroller i den offentlige sektor
description: Dette emne indeholder oplysninger om sikkerhedsroller i den offentlige sektor, herunder projektleder- og indkøberroller.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UserRequestListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 19721
ms.assetid: e26a6d93-851e-46be-8543-de2798909350
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff40f915c329187e3fa3f4cba5f1f7f06c2f3e14
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890761"
---
# <a name="security-roles-in-the-public-sector"></a>Sikkerhedsroller i den offentlige sektor

[!include [banner](../includes/banner.md)]

I denne artikel beskrives funktionen for sikkerhedsroller i den offentlige sektor. Disse funktioner omfatter rollerne Projektleder og Indkøber for den offentlige sektor.

Alle brugere skal være tilknyttet mindst én sikkerhedsrolle for at have adgang til Dynamics 365 Finance. Sikkerhedsroller bestemmer, hvilke opgaver brugere kan udføre, og hvilke dele af brugergrænsefladen de kan se.

## <a name="what-are-the-prerequisites-for-assigning-security-roles-in-the-public-sector"></a>Hvad er forudsætningerne for tildeling af sikkerhedsroller i den offentlige sektor?
Brugerne skal findes i Finance, før du kan tildele dem roller. Selvom du bruger automatisk rolletildeling, tilføjes brugerne selv ikke automatisk.

## <a name="which-roles-do-i-have-to-assign"></a>Hvilke roller skal jeg tildele?
Når brugerne er i systemet, er der to roller, som du muligvis skal konfigurere for offentlige organisationer:

-   Projektleder
-   Indkøbsassistent

### <a name="what-is-the-project-manager---public-sector-role"></a>Hvad er Projektleder – Offentlig sektor-rollen?

Sikkerhedsrollen **Projektleder – Offentlig sektor** understøtter de offentlige sektor-udvidelser til projektstyring. Tildel rollen foruden rollen **Projektleder** for at give projektledere adgang til projektstyringsfunktioner. Denne sikkerhedsrolle tildeles som standard følgende opgaver.

| Navn på arbejdsopgave                                                         | Arbejdsopgaves AOT-navn                           | Beskrivelse af programadgangsrettighed                                                                |
|-------------------------------------------------------------------|-----------------------------------------|---------------------------------------------------------------------------------|
| Forespørg om status for indkøbsordre til faktura for offentlig sektor | PurchOrderToInvoiceProgressInquire\_PSN | Besvar forespørgsler om status for processen indkøbsordre til faktura. |

### <a name="what-is-the-purchasing-agent---public-sector-role"></a>Hvad er Indkøbsagent - den offentlige sektor-rollen?

Sikkerhedsrollen **Indkøbsagent - den offentlige sektor** understøtter de offentlige sektor-udvidelser til projektstyring. Tildel denne rolle foruden rollen **Indkøbsassistent** for at give indkøbsassistenter adgang til købsfunktionalitet. Denne sikkerhedsrolle tildeles som standard følgende opgaver.

| Navn på arbejdsopgave                                                       | Arbejdsopgaves AOT-navn                            | Beskrivelse af programadgangsrettighed                                                                                        |
|-----------------------------------------------------------------|------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Vedligehold købsaftalemaster                              | AgreementPurchaseAgreementMasterMaintain | Vedligehold oplysninger om købsaftaler.                                                            |
| Konfigurer AIF-synkronisering                                   | AifSyncConfigure                         | Angiv filtre på porte.                                                                               |
| Forespørg om status for indkøbssager                           | CasePurchasingCaseProgressInquire        | Besvar forespørgsler om status for indkøbssager.                                              |
| Vedligehold kataloger                                               | CatProcurementCatalogMasterMaintain      | Vedligehold alle typer kataloger.                                                                         |
| Vedligehold alle kategorihierarkioplysninger                         | EcoResCategoryMasterMaintain             | Vedligehold kategorier.                                                                                    |
| Forespørg om produktdefinitionsmaster                         | EcoResProductDefinitionMasterInquire     | Besvar forespørgsler om masterdata for produktdefinitioner.                                         |
| Forespørg på Product Builder-konfigurationsdata                 | PBAProductBuilderConfigStatusInquire     | Åbn og gennemse Product Builder-konfigurationer.                                                         |
| Vedligehold Product Builder-konfiguration                          | PBAProductBuilderConfigurationMaintain   | Rediger og opdater Product Builder-konfigurationer.                                                         |
| Vedligehold produktkonfiguration                                  | PCProductConfigConfigurationMaintain     | Vedligehold en begrænsningsbaseret konfiguration for produktkonfigurationsmodeller.                             |
| Forespørg vedrørende produktkonfiguration                              | PCProductConfigConfigurationStatInquir   | Besvar forespørgsler om konfigurationsmasterdata for begrænsningsbaserede produktkonfigurationsmodeller. |
| Vedligehold indstillinger for udskriftsstyring for indkøbsopsætning               | PrintMgmtPurchaseSettingsMaintain        | Vedligehold indstillinger for udskriftsstyring for indkøbsopsætninger.                                                 |
| Vedligehold indstillinger for udskriftsstyring for indkøbsdokumenter            | PrintMgmtPurchDocumentSettingsMaintain   | Vedligehold indstillinger for udskriftsstyring for indkøbsdokumenter.                                              |
| Forespørg om indkøbspolitikker                                | ProcPurchasingProcessInquire             | Besvar forespørgsler om politikker, der styrer indkøbsprocessen.                                 |
| Forespørg om indkøbspolitikker for offentlig sektor              | ProcPurchasingProcessInquire\_PSN        | Besvar forespørgsler om politikker for den offentlige sektor, der styrer indkøbsprocessen.                   |
| Godkend købsaftale                                      | PurchaseAgreementWFMaintain              | Gennemse og godkend købsaftaler i en arbejdsgang.                                                   |
| Vedligehold indkøbsordrer                                        | PurchOrderMaintain                       | Dokumentér og registrer indkøbsordrer.                                                                    |
| Vedligehold konsolidering af indkøbsrekvisition                     | PurchReqConsolidationMaintain            | Vedligehold konsolideringsprocessen for indkøbsrekvisitionen.                                                |
| Vedligehold oprettelse af indkøbsordrer ud fra indkøbsrekvisitioner | PurchReqOrderFromRequisitionMaintain     | Frigiv indkøbsordrer ud fra indkøbsrekvisitioner.                                                     |
| Godkend indkøbsrekvisitioner                                   | PurchReqPurchaseRequisitionApprove       | Bekræft og godkend indkøbsrekvisitioner.                                                            |
| Vedligehold alle indkøbsrekvisitioner                              | PurchReqPurchaseRequisitionMaintainAll   | Rediger og opdater indkøbsrekvisitioner.                                                                  |
| Vis indkøbsrekvisitioner på hold                              | PurchReqTableView                        | Åbn og gennemse indkøbsrekvisitioner, der er på hold.                                                 |
| Vedligehold spørgeskema til tilbudsanmodning                    | PurchRFQQuestionnaireMaintain            | Rediger og opdater spørgeskemaer til tilbudsanmodning.                                             |
| Vedligehold tilbudsanmodning                                  | PurchRFQRequestForQuoteMaintain          | Rediger og opdater tilbudsanmodninger.                                                                                   |
| Vedligehold svar på tilbudsanmodning                          | PurchRFQRequestForQuoteReplyMaintain     | Rediger og opdater svar på tilbudsanmodninger.                                                                            |
| Vedligehold forseglede bud                                            | PurchRFQSealedBids                       | Rediger og opdater forseglet bud.                                                                            |
| Forespørg om betalingsstatus for kreditorfakturaer                | VendInvoice4paymentStatusInquire\_RU     | Besvar forespørgsler om betalingsstatus for kreditorfakturaer.                                      |
| Vedligehold kreditorfakturaer for betaling                            | VendInvoice4PaymMaintain\_RU             | Rediger og opdater kreditorfakturaer for betaling.                                                            |
| Vedligehold master for mulig kreditor                              | VendProspectiveVendorMasterMaintain      | Rediger og opdater master for mulig kreditor.                                                          |
| Vedligehold kreditoranmodning igangsat af medarbejder                     | VendRequestEmployeeVendorRequestMaintain | Dokumentér og registrer kreditoranmodning igangsat af medarbejder.                                                 |
| Forespørg om status for kreditoranmodning                    | VendRequestVendorInitiateRequestInquire  | Besvar forespørgsler om status for anmodninger igangsat af kreditor.                                     |
| Forespørg om ikke-anmodet kreditormaster                          | VendUnsolicitedVendorMasterInquire       | Besvar forespørgsler om masterdata for ikke-anmodet kreditor.                                              |
| Vedligehold kreditorbrugeranmodninger                                   | VendUserRequestMaintain                  | Vedligehold og send kreditorbrugers anmodninger.                                                               |
| Vedligehold kreditormaster                                          | VendVendorMasterMaintain                 | Rediger og opdater master for kreditor.                                                                      |
| Vedligehold kreditorspørgeskemaer                                  | VendVendorQuestionnaireMaintain          | Opret og opdater oplysninger om kreditorspørgeskemaer.                                                     |
| Forespørg om arbejdsgangsperformance                               | WorkflowViewWorkflowPerf                 | Få vist rapporter om arbejdsgangsperformance.                                                        |

## <a name="what-do-i-do-next"></a>Hvad skal jeg gøre nu?
Når brugerne er oprettet, skal du tildele dem roller på siden **Tildel brugere roller**.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Rollebaseret sikkerhed](../../fin-ops-core/dev-itpro/sysadmin/role-based-security.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]