---
title: "Frarådede funktioner"
description: "Dette emne beskriver funktioner, der er blevet fjernet eller er planlagt til at blive fjernet fra Dynamics 365 for Operations. Det indeholder også funktioner, som blev frarådet i Dynamics AX 7.0 udgivelser."
author: sericks007
manager: AnnBe
ms.date: 04/18/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Platform
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8fbfc8c91c836eb9922f2bf1165ec887d8a0bc8e
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="deprecated-features"></a>Frarådede funktioner

[!include[banner](../includes/banner.md)]


Dette emne beskriver funktioner, der er blevet fjernet eller er planlagt til at blive fjernet fra Dynamics 365 for Operations. Det indeholder også funktioner, som blev frarådet i Dynamics AX 7.0 udgivelser.

<a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Funktioner, der er blevet frarådet i Dynamics 365 for Operations 1611 med platformsopdatering 3
---------------------------------------------------------------------------------------------

### <a name="aeb-payment-formats-for-spain"></a>AEB-betalingsformater for Spanien

Betalingsformater Consejo Superior Bancario bruges til at sende remitteringsfiler til banken for debitor- og kreditorbetalinger. Indholdet af disse formater bestemmes af Asociación Española de Banca. Det dækker Cuaderno 19, 32, 58, 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformaterne bruges ikke længere.                                  |
| Erstattet af en anden funktion? | Ja, ISO20022-overførsel og Direct Debit-betalingsformater for Spanien |
| Påvirkede moduler             | Debitor/kreditor                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Bankoverførsel af betalinger for Litauen

Bankbetalingsoverførsler genereres og udskrives ved hjælp af eksportformatet for betalingsoverførsler (LT) for Litauen. Det litauiske marked begyndte at bruge LITAS, det fælles elektroniske banksystem, i 2005.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformaterne bruges ikke længere.                    |
| Erstattet af en anden funktion? | Ja, ISO20022-kreditoverførsel som betalingsformat for Litauen |
| Påvirkede moduler             | Kreditor                                           |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS Direkte Remittering-betalingsformater for Norge

BBS Direkte Remittering-betalingsformater omfatter eksport af kundebetalingsopkrævning (Direct Debit) og import af returmeddelelse.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformaterne bruges ikke længere.                                                                                                                        |
| Erstattet af en anden funktion? | AvtaleGiro-kundebetalingsformater for Norge kan bruges til at oprette direct debit-meddelelser. Import af returmeddelelse vil blive implementeret i fremtidige versioner. |
| Påvirkede moduler             | Debitor/kreditor                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>Kontoplanværktøj for Spanien

Dette værktøj bruges, når en kontoplan i Spanien kræver omfattende ændringer. Brugere kan importere en ny kontoplan i Microsoft Excel- eller tekstformat og kan også importere regnskaber.

|                              |                |
|------------------------------|----------------|
| Årsagen til fjernelsen       | Begrænset brug  |
| Erstattet af en anden funktion? | Nr.             |
| Påvirkede moduler             | Finans |

### <a name="dom80-payment-format-for-belgium"></a>Dom80-betalingsformater for Belgien

Det gamle belgiske betalingsformat for betalingsopkrævning (Direct Debit).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformatet bruges ikke længere.                  |
| Erstattet af en anden funktion? | Ja, ISO 20022 Direct Debit-betalings format for Belgien |
| Påvirkede moduler             | Debitor                                    |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG-betalingsformater for Schweiz

DTA/EZAG-formater integreres i ESR-systemet, fordi de kan overføre et referencenummer. Da referencenumre ikke er obligatorisk, kan disse formater bruges til at behandle alle kreditorbetalinger. Disse formater anvendes af virksomheder, der har en bankkonto et andet sted end "Postfinance".

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformaterne bruges ikke længere.                      |
| Erstattet af en anden funktion? | Ja, ISO20022-kreditoverførsel som betalingsformat for Schweiz |
| Påvirkede moduler             | Kreditor                                             |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB-betalingsformat for Østrig

EDIFACT-DIRDEB-betalingsformat for betalingsopkrævning (Direct Debit).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformatet bruges ikke længere.                  |
| Erstattet af en anden funktion? | Ja, ISO 20022 Direct Debit-betalings format for Østrig |
| Påvirkede moduler             | Debitor                                    |

### <a name="edivat-for-belgium"></a>EDIVAT for Belgien

EDIVAT er en forældet belgisk standard for elektronisk indberetning via sikker mail. Microsoft Dynamics AX 2012 bevarer den skrivebeskyttede løsning for at give adgang til de historiske data.

|                              |                                      |
|------------------------------|--------------------------------------|
| Årsagen til fjernelsen       | Funktionaliteten bruges ikke længere. |
| Erstattet af en anden funktion? | Nr.                                   |
| Påvirkede moduler             | Finans                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro EDIFACT CREMUL-betalingsimportformat for Norge

eGiro er baseret på den internationale FN standard EDIFACT CREMUL, (Multiple Credit Advice Message), der bruges til automatisk bogføring af betalinger fra kunder. eGiro er implementeret som et format til import af kundebetaling i Microsoft Dynamics AX.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformatet bruges ikke længere.                                                     |
| Erstattet af en anden funktion? | Nr. Formatet erstattes med ISO 20022-importformater i fremtidige versioner. |
| Påvirkede moduler             | Debitor                                                                       |

### <a name="external-inventory-for-poland"></a>Eksternt lager til Polen

Bevis for varer, der er taget fra en kreditor til salg uden køb. Varer, der kan håndteres i eksternt lager, som ikke påvirker standardlageret, og kan sælges og derefter købes automatisk. Denne proces opretter reelle lagerbevægelser.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| Årsagen til fjernelsen       | Erstattet af en anden funktion                     |
| Erstattet af en anden funktion? | Ja, kernefunktionalitet for indgående konsignation |
| Påvirkede moduler             | Kreditor, Lagerstyring          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Finansiel rapportgenerator for Østeuropa

Et værktøj bruges til at konfigurere indsamling af data til regnskabs- og momsrapporter og eksportere data til XLS og DOC rapportskabeloner.

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Begrænset brug                                                                            |
| Erstattet af en anden funktion? | Nr. Værktøjet erstattes af elektroniske indberetningskonfigurationer i fremtidige udgivelser. |
| Påvirkede moduler             | Finans                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Import af debitorbetalingsposteringer til Finland

Du kan vælge et importformat til finske betalinger, der importerer debitorbetalingsposteringer fra en ekstern fil, der leveres af banken.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformatet bruges ikke længere.                                                     |
| Erstattet af en anden funktion? | Nr. Formatet erstattes med ISO 20022-importformater i fremtidige versioner. |
| Påvirkede moduler             | Debitor                                                                       |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Import af betalingstransaktioner i en finanskladde til Finland

Et format, der er specifikt for Finland, bruges til import af regnskabstransaktioner i Finans.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformatet bruges ikke længere.                                                     |
| Erstattet af en anden funktion? | Nr. Formatet erstattes med ISO 20022-importformater i fremtidige versioner. |
| Påvirkede moduler             | Debitor                                                                       |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integration med Isabel synkroniseret (CIS) i Belgien

Isabel er rammen for elektroniske betalinger i Europa og er en de facto standard i Belgien.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Integration med Isabel-klient er blevet afbrudt.                                                                |
| Erstattet af en anden funktion? | Nr. Betalingsformater, der ikke længere bruges, erstattes af ISO20022-kreditoverførselsbetalingsformat for Belgien. |
| Påvirkede moduler             | Kreditor                                                                                                     |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Ændringer i kontoplan og regnskabsregler for Spanien

Denne funktion bruges til ændringer i kontoplanen og regnskabsregler i Spanien. Den knytter konti for at hjælpe med at omdanne den gamle kontoplan til den nye kontoplan og sammenligner det foregående år med det nye regnskabsår, selvom de blev bogført på forskellige kontonumre.

|                              |                |
|------------------------------|----------------|
| Årsagen til fjernelsen       | Begrænset brug  |
| Erstattet af en anden funktion? | Nr.             |
| Påvirkede moduler             | Finans |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori-kreditorbetalingsformat

Gammelt italiensk betalingsformat for kreditoverførsler.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformatet bruges ikke længere.                  |
| Erstattet af en anden funktion? | Ja, ISO20022-kreditoverførsel som betalingsformat for Italien |
| Påvirkede moduler             | Kreditor                                       |

### <a name="payment-export-formats-for-estonia"></a>Formater til eksport af betalinger for Estland.

Telehansa- og Teleservice-formater bruges til eksport af bankens betaling.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformaterne bruges ikke længere.                  |
| Erstattet af en anden funktion? | Ja, ISO20022-kreditoverførsel som betalingsformat for Estland |
| Påvirkede moduler             | Kreditor                                         |

### <a name="payment-file-archive-for-norway"></a>Betalingsfilarkiv til Norge

Når betalingsfilerne genereres, arkiverer filarkivet automatisk alle filer, der oprettes, selv filer, der tidligere er skrevet eller læst.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| Årsagen til fjernelsen       | Erstattet af en anden funktion                                        |
| Erstattet af en anden funktion? | Ja, elektronisk rapportering af arkiverede job                            |
| Påvirkede moduler             | Debitor, Kreditor og Virksomhedsadministration |

### <a name="payment-import-formats-for-estonia"></a>Formater til import af betalinger for Estland.

Telehansa- og TeleTeenus-formater bruges til import af bankens betaling.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformaterne bruges ikke længere.                                                    |
| Erstattet af en anden funktion? | Nr. Formaterne erstattes med ISO 20022-importformater i fremtidige versioner. |
| Påvirkede moduler             | Debitor                                                                        |

### <a name="performance-management-goal-workflow"></a>Målarbejdsgang for performancestyring

Performancestyring omfatter målstyring og integration med performanceevalueringer.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Performancestyring er blevet ændret, og antallet af målsider blev reduceret for at forenkle processen.                 |
| Erstattet af en anden funktion? | Nr. Mål kan ses af ledere gennem Chefselvbetjening-portalen, og kan ændres og ses af chefen. |
| Påvirkede moduler             | Styring af menneskelig kapital                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Postgirot- og Postgirot Utland-betalingsformater for Sverige

Postgirot- og Postgirot Utland-betalingsformater for Sverige.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformaterne bruges ikke længere.                 |
| Erstattet af en anden funktion? | Ja, ISO20022-kreditoverførsel som betalingsformat for Sverige |
| Påvirkede moduler             | Kreditor                                        |

### <a name="radio-frequency-identifier"></a>Radio Frequency Identification (RFID)

RFID (Radio Frequency Identification) er en teknologi til indsamling af data, hvor der bruges elektroniske mærkater til lagring af identifikationsdata og en læser uden krav om sigtelinje til registrering af disse data.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| Årsagen til fjernelsen       | Lavt forbrug og begrænset funktionssæt. |
| Erstattet af en anden funktion? | Nr.                                            |
| Påvirkede moduler             | Lagerstyring                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Rapport om fakturanummerering for Letland

Lettisk lovgivning indeholder særlige regler om, hvordan salgsfakturaer skal nummereres. Med funktionaliteten kan du tildele specifikke numre til salgsfakturaer, baseret på bruger eller brugergruppe. Derefter kan du generere en rapport eller en XML-fil. Du kan også udskrive en rapport om fakturanumre, der bruges.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Statsfakturanummerering skal ikke længere opretholdes. Rapporten om anvendte fakturanumre er ikke længere påkrævet. |
| Erstattet af en anden funktion? | Nr.                                                                                                                       |
| Påvirkede moduler             | Debitor                                                                                                      |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Angiv navnene på chefen og den generelle revisor i en virksomhed til Litauen

Navnene på chefen og den generelle revisor i en virksomhed kan angives i firmaoplysningerne og bruges i forskellige lokale rapportudskrifter.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Årsagen til fjernelsen       | Erstattet af en anden funktion                                     |
| Erstattet af en anden funktion? | Ja, opsætning af embedsmænd kan bruges til samme formål.   |
| Påvirkede moduler             | Kreditor, Debitor, Kontant- og bankstyring |

### <a name="telepay-payment-formats-for-norway"></a>Telepay-betalingsformater for Norge

Telepay-betalingsformater omfatter kreditorbetalingseksport (pengeoverførsel) og kundebetalingsopkrævning (Direct Debit).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformaterne bruges ikke længere.                                                        |
| Erstattet af en anden funktion? | Ja, ISO20022-kreditoverførsel som betalingsformat og AvtaleGiro-debitorbetalingsformat til Norge |
| Påvirkede moduler             | Debitor/kreditor                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Eksportformater til kreditorbetalinger for Finland

Der findes to formater til eksport af betalinger for Finland. LM02 (FI) bruges til indenlandske betalinger, og LUM2 (FI) bruges til betaling til udlandet.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Årsagen til fjernelsen       | Betalingsformaterne bruges ikke længere.                  |
| Erstattet af en anden funktion? | Ja, ISO20022-kreditoverførsel som betalingsformat for Finland |
| Påvirkede moduler             | Kreditor                                         |

### <a name="workflow-for-creating-goals"></a>Arbejdsgang for oprettelse af mål

En arbejdsgang til styring af oprettelse af medarbejdermål er et af flere arbejdsgange, der kan hjælpe med at koordinere performancestyringsprocessen.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Performancestyring er blevet ændret fuldstændigt i Microsoft Dynamics 365 for Operations.                                                                                                                                                                                                                                        |
| Erstattet af en anden funktion? | Den nyudviklede funktion til performancestyring giver bedre kontrol over indholdet af mål, de mål, der bruges til at spore forløbet, og den vedhæftede fil med yderligere dokumentation. Mål kan gemmes som skabeloner og genbruges derefter. Denne funktion kan hjælpe dig med at konfigurere yderligere mål for medarbejderne hurtigere. |
| Påvirkede moduler             | Styring af menneskelig kapital                                                                                                                                                                                                                                                                                                               |

## <a name="features-deprecated-in-dynamics-ax-70-releases"></a>Funktioner, der frarådes i Dynamics AX 7.0-udgivelser
### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Mulighed for at annullere ændringer af en kreditorfaktura

|                              |                         |
|------------------------------|-------------------------|
| Årsagen til fjernelsen       | Performanceforbedring |
| Erstattet af en anden funktion? | Nej                      |
| Påvirkede moduler             | Kreditor        |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD og AxBC integrationer

I Application Integration Framework (AIF) kan data udveksles med eksterne systemer via forretningslogik, der vises som tjenester. Dynamics AX indeholder tjenester, der er baseret på dokumenter og .NET Business Connector (AxBC). Der oprettes et dokument ved hjælp af XML. XML-filen indeholder hovedoplysninger, der er tilføjet for at oprette en *meddelelse*, der kan overføres til eller fra Dynamics AX. Eksempler på dokumenter omfatter salgsordrer og indkøbsordrer. Næsten enhver enhed, f.eks. en kunde, kan dog være repræsenteret af et dokument. Tjenester, der er baseret på dokumenter, bruger **Axd &lt;*Dokument*&gt;** klasser.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Arkitekturen i AIF og AxDs kan ikke skaleres til en skytjeneste. Der var problemer med ydeevnen omkring masseimport.                                                                               |
| Erstattet af en anden funktion? | I den aktuelle version af Dynamics AX er denne funktion erstattet af Struktur til dataimport/-eksport, som understøtter tilbagevendende masseimport/eksport. AxBC anbefaler vi, at du bruger tabellerne. |
| Påvirkede moduler             | AxDs, AxBCs og AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>Styklister uden styklisteversioner

Når **Styklisteversioner**-konfigurationsnøglen var deaktiveret, blev styklisteversioner skjult i alle formularer, og systemet ville gennemtvinge en 1:1 relation mellem frigivne produkter og styklister. **Styklisteversioner**-konfigurationsnøglen kan ikke være deaktiveret i den aktuelle version af Dynamics AX.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Når du bruger en konfigurationsnøgle til styring, skaleres styklisteversioner ikke i et skymiljø. |
| Erstattet af en anden funktion? | Nej                                                                                      |
| Påvirkede moduler             | Administration af produktoplysninger, Lagerstyring                                    |

### <a name="brazilian-bordero"></a>Brasiliansk Bordero

Specifik betalingsmåde for brasilianske virksomheder

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Understøttelse af brasiliansk Bordero-betalingsmåde er blevet afbrudt fra brasiliansk lokalisering |
| Erstattet af en anden funktion? | Nr.                                                                                                    |
| Påvirkede moduler             | Kreditor                                                                                      |

### <a name="brazilian-sintegra-statement"></a>Brasiliansk Sintegra-opgørelse

Momsangivelse for ICMS-moms

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Denne opgørelse er ikke længere gældende i visse brasilianske stater.                                                     |
| Erstattet af en anden funktion? | Nr. Brugere kan bruge generisk elektronisk rapporteringsværktøj for at konfigurere opgørelsen, hvis det er påkrævet under bestemte situationer. |
| Påvirkede moduler             | Regnskabsbøger                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasiliansk SCAN-beredskabstilstand for NF-e

(SCAN) beredskabsmiljø bruges til at oprette, eksportere og importere status for en Nota Fiscal eletrônica (NF-e), når miljøet i Secretaria da Fazenda (SEFAZ) ikke er tilgængeligt.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Denne beredskabsmetode er ikke længere gældende i alle brasilianske stater |
| Erstattet af en anden funktion? | Nr.                                                                          |
| Påvirkede moduler             | Debitor                                                         |

### <a name="business-analyzer"></a>Forretningsanalyse

Med dette mobilprogram kan brugerne gennemse vigtige virksomhedsmål.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Denne funktion er blevet erstattet af en anden funktion.                                                                                                      |
| Erstattet af en anden funktion? | Indholdspakken Overvågning af økonomisk performance til Microsoft PowerBI omfatter vigtige økonomiske nøgletal, der tidligere var tilgængelige i Business Analyzer. |
| Påvirkede moduler             | Finans                                                                                                                                                |

### <a name="business-statistics"></a>Handelsstatistik

Konfiguration af forespørgsler vedrørende handelsstatistik, som kan bidrage til analysen af organisationens performance

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Ældre tilgang til business intelligence (BI), lavt forbrug og et begrænset funktionssæt |
| Erstattet af en anden funktion? | Nye BI-løsninger til den aktuelle version af Dynamics AX                                      |
| Påvirkede moduler             | Indkøb og forsyning, Kreditor, Salg og marketing, Debitor.         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Ændre dokumentdatofunktion i fakturagodkendelseskladde

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Lav belastning                                                               |
| Erstattet af en anden funktion? | Ja. Bilagsdato på den bogførte kreditorpostering kan ændres. |
| Påvirkede moduler             | Kreditor                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03-betalingsformat for Nederlandene

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Formatet er ikke længere gældende i Nederlandene, fordi det er blevet erstattet af SEPA-funktioner. |
| Erstattet af en anden funktion? | Eksport af SEPA-betalinger                                                                                       |
| Påvirkede moduler             | Alle                                                                                                        |

### <a name="compliance-center"></a>Overholdelsescenter

Overholdelsescenter var et Enterprise Portal-websted til administration af dokumentationskrav for overholdelsesinitiativer vedrørende Sarbanes-Oxley-loven.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Mangel på forbrug. Microsoft SharePoint indeholder samme egenskab, der var tilgængelig i Overholdelsescenter. |
| Erstattet af en anden funktion? | Nej                                                                                                                     |
| Påvirkede moduler             | Overholdelse og interne kontroller                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>Connector til Microsoft Dynamics

Dette værktøj blev brugt til at integrere vigtige data fra Microsoft Dynamics CRM i Microsoft Dynamics ERP-applikationer.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Årsagen til fjernelsen       | Denne funktion er blevet erstattet af en anden funktion. |
| Erstattet af en anden funktion? | Dynamics Integrator                                      |
| Påvirkede moduler             | Connector til Microsoft Dynamics                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Containerenhed og flerdimensionale beholdninger

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Identiske funktioner                                                                                                                                         |
| Erstattet af en anden funktion? | Ja. Denne funktionalitet er blevet erstattet af konsolideret batchordre-funktionssæt siden AX 2012. Denne funktion omfatter den konsoliderede disponible visning. |
| Påvirkede moduler             | Administration af produktoplysninger, Produktionsstyring, Lagerstyring, Salg og marketing                                                                   |

### <a name="cue-group-metadata"></a>Køgruppemetadata

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Køgrupper blev brugt til at vise en eller flere køer i faktaboksområdet. Der var begrænset optagelse, og der var også problemer med ydeevnen, fordi en ændring af en post i en overordnet formular forårsagede en forespørgsel pr. kø i gruppen Kø. |
| Erstattet af en anden funktion? | Nej                                                                                                                                                                                                                            |
| Påvirkede moduler             | Alle                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>Kømetadata

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Kømetadata var begrænset til antals- eller beløbsoplysninger.                                                                                                                                                                                   |
| Erstattet af en anden funktion? | Feltmetadata blev indført for at give større fleksibilitet for modellering. Du kan f.eks. modellere aktuelle tæller-, navigations- og nøgletal (KPI'er). Metadata for antalsfelter er den direkte erstatning af Kømetadata. |
| Påvirkede moduler             | Alle                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Dansk checkformat

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Det danske checklayout format understøttes ikke længere, og rapporten er blevet fjernet fra lokaliseringen til dansk. |
| Erstattet af en anden funktion? | Nej                                                                                                                      |
| Påvirkede moduler             | Alle                                                                                                                     |

### <a name="data-partitions"></a>Datapartitioner

Datapartitioner giver en logisk adskillelse af dataene i Microsoft Dynamics AX-databasen.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Datapartitioner blev introduceret i Microsoft Dynamics AX 2012 R2 for at give mulighed for dataisolering. I et almindeligt scenarie har en virksomhed datterselskaber, og data fra ét datterselskab bør ikke være synlige for et andet datterselskab, selvom begge datterselskaber, der administreres af samme it-afdeling. Dog var ekstra scripts og indirekte administrationsomkostninger i hele programmet påkrævet for at oprette nye partitioner og udfylde dem med data og til sikkerhedskopiering af data på partitionen. I skyen, hvor vi har adgang til PaaS-databasetjenester (platform som en tjeneste) (Microsoft Azure, SQL Database), er det langt mere effektivt at bruge en database som isolationscontainer end at udføre isolation i programmet. Uanset om datapartitionering er påkrævet for datterselskaber, for flere lejere eller blot af skaleringsårsager, mener vi, at scenarierne kan håndteres bedre gennem flere databaser eller flere Dynamics AX-forekomster. |
| Erstattet af en anden funktion? | Datapartitioner erstattes gennem støtte til flere databaser eller Dynamics AX-forekomster i en fremtidig version.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Påvirkede moduler             | Alle                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

### <a name="delimitation"></a>Afgrænsning

|                              |                                        |
|------------------------------|----------------------------------------|
| Årsagen til fjernelsen       | Ingen brug af funktionen blev ikke fundet. |
| Erstattet af en anden funktion? | Nej                                     |
| Påvirkede moduler             | Tid og fremmøde                    |

### <a name="desktop-client"></a>Desktopklient

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Dynamics AX-klientoplevelsen er blevet ændret for at forbedre brugervenligheden på tværs af flere platforme og enheder.                      |
| Erstattet af en anden funktion? | Den nye webklient er baseret på skrivebordsformularens metadata- og programmeringsmodel, der er blevet ændret for at give plads til en omfattende webplatform. |
| Påvirkede moduler             | Alt                                                                                                                                    |

### <a name="direct-database-connection"></a>Direkte databaseforbindelse

I Dynamics AX 2012 R3 kunne Retail Modern POS forbindes direkte med kanaldatabasen på lignende måde som Enterprise POS. Dette var ud over den almindelige kommunikationsmetode for Retail Modern POS-kommunikation via Retail Server.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Direkte databaseforbindelse krævede lavere sikkerhedsprotokoller og blev primært brugt til at opnå den bedst mulige ydeevne. På grund af bedre ydeevne og sikkerhedsmæssige forbedringer i Dynamics 365 for Operations medfører denne funktion nu flere problemer, end den løser. |
| Erstattet af en anden funktion? | Nr. Kun standard Retail Server-kommunikation understøttes nu.    |
| Påvirkede moduler             | Kanaldatabase/Retail Modern POS                                    |

### <a name="dutch-swift-mt940"></a>Nederlandsk SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Generiske funktioner bruges nu i stedet for oversat funktionalitet.                                                                                                                                                                 |
| Erstattet af en anden funktion? | Ja, denne funktion er erstattet af funktionen Avanceret bankafstemning. Implementering af import af camt.053 ISO20022-kontoopgørelse er desuden planlagt for finanskladden i den næste opdatering af Dynamics AX. |
| Påvirkede moduler             | Alle                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL-adresse for Tyskland)

Denne funktionalitet leverede XBRL-output (eXtensible Business Reporting Language), der er beregnet specifikt til den tyske eBilanz-taksonomi.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Mangel på forbrug                                                                                                                                                 |
| Erstattet af en anden funktion? | Denne funktion er ikke erstattet af en anden funktion, men flere specialiserede XBRL-pakker, der giver omfattende XBRL-funktionalitet, er tilgængelige for det tyske marked. |
| Påvirkede moduler             | Management Reporter                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Enterprise Portal-klient

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Har fået tildelt en enkelt klientplatform.                                                                                            |
| Erstattet af en anden funktion? | Den nye webklient er baseret på skrivebordsformularens metadata- og programmeringsmodel, der er blevet ændret for at give plads til en omfattende webplatform. |
| Påvirkede moduler             | Alle                                                                                                                                    |

### <a name="environmental-sustainability"></a>Miljømæssig bæredygtighed

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| Årsagen til fjernelsen       | Lavt forbrug og begrænset funktionssæt       |
| Erstattet af en anden funktion? | Nej                                                 |
| Påvirkede moduler             | Overholdelse og interne kontroller, Kreditor |

### <a name="form-activex-and-managed-host-controls"></a>Kontrolelementer til ActiveX-formular og administrerede vært

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Kontrolelementerne til ActiveX og administreret vært er baseret på den forældede klient til stationære computere.                                                                                                             |
| Erstattet af en anden funktion? | Kontrolstruktur, som kan udvides, understøtter opbygning af nye kontrolelementer, der er baseret på HTML, CSS og JavaScript, og er en førsteklasses kontrol i Microsoft Visual Studio-værktøjsmiljøet. |
| Påvirkede moduler             | Alle                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Opret adviseringer ved hjælp af en batch

Oprettelsen af adviseringer kan ikke udføres ved hjælp af et batch, men kan stadig udføres af en bruger.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Der findes ingen formular til at fastholde og vise den resulterende adviseringsfil, når den er oprettet ved hjælp af et batch. |
| Erstattet af en anden funktion? | Der kan stadig oprettes adviseringer, og brugeren har kontrol over, hvor filen gemmes.   |
| Påvirkede moduler             | Kreditor, Debitor, Kontant- og bankstyring                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Tysk DTAUS betalingseksporter og kontoopgørelsesimport (totaler og transaktioner)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Formatet er ikke længere gældende i Tyskland, fordi det er blevet erstattet af SEPA-funktioner (Single Euro Payments Area).                                                                                                                                                                 |
| Erstattet af en anden funktion? | Ja, denne funktionalitet er blevet erstattet af eksport af SEPA-betaling og avancerede bankafstemningsfunktioner til import af kontoudtog. Implementering af import af camt.053 ISO20022-kontoopgørelse er desuden planlagt for finanskladden i den næste opdatering af Dynamics AX. |
| Påvirkede moduler             | Alle                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Tysk DTAZV-betalingsformat

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Formatet er ikke længere gældende i Tyskland, fordi det er blevet erstattet af SEPA-funktioner. |
| Erstattet af en anden funktion? | Eksport af SEPA-betalinger                                                                               |
| Påvirkede moduler             | Alle                                                                                                |

### <a name="german-mt940-import"></a>Tysk MT940-import

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Generiske funktioner bruges nu i stedet for oversat funktionalitet.                                                                                                                                                                 |
| Erstattet af en anden funktion? | Ja, denne funktion er erstattet af funktionen Avanceret bankafstemning. Implementering af import af camt.053 ISO20022-kontoopgørelse er desuden planlagt for finanskladden i den næste opdatering af Dynamics AX. |
| Påvirkede moduler             | Alle                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>Tysk EU-listesystem i XML-format

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | XML-format til rapportering af tysk EU-listesystem understøttes ikke længere. Kun ELMA5-tekstfilformatet kan bruges til at sende rapporten for EU-listesystemet til de tyske skattemyndigheder. |
| Erstattet af en anden funktion? | Nej                                                                                                                                                                                 |
| Påvirkede moduler             | Skat                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>GL SSRS-rapporter

Rapporter, der indeholder følgende menupunkter, er blevet fjernet: **Råbalanceoversigt**, **Detaljeret råbalance**, **Kontoplan**, **Revisionsspor**, **Saldi** og **Saldoliste**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Økonomirapporter til Microsoft SQL Server Reporting Services (SSRS) er blevet erstattet af Management Reporter-funktioner og standardrapporter. |
| Erstattet af en anden funktion? | Management Reporter (med navnet **Økonomirapportering** i den aktuelle version af Dynamics AX)                                                  |
| Påvirkede moduler             | Finans                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>InfoPart og FormPart-metadata

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | InfoPart og FormPart-metadata aktiverede oprettelsen af faktabokse for to forskellige klienter.                                                                                                                                    |
| Erstattet af en anden funktion? | InfoPart-metadata, som var en definition i forenklet form, er konverteret til en formular ved hjælp af opgraderingsværktøj. FormPart-metadata, som refererede til en formular, er erstattet af en mere direkte reference, der oprettes af opgraderingsværktøj. |
| Påvirkede moduler             | Alle                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Hovedkonto-listeside

En liste over konti for den juridiske enhed og relaterede saldooplysninger

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Saldooplysninger er tilgængelige på listesiden **Råbalance** pr. konto og dimension.                                                                                      |
| Erstattet af en anden funktion? | **Hovedkonti** indeholder den samme liste over konti, som listesiden **Hovedkonto** indeholdt. Gittervisningen i **Hovedkonti** viser også en endnu mindre, gitterlignende visning. |
| Påvirkede moduler             | Finans                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaysia og Singapore bankpengestrømsrapport

Med denne funktion kan brugeren udskrive en pengestrømsanalyse, der viser transaktioner og detaljer i indgående og udgående pengestrømme for et bestemt datointerval for udvalgte bankkonti.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Årsagen til fjernelsen       | De samme oplysninger kan fås fra bankposteringen Forespørgsel. |
| Erstattet af en anden funktion? | Bankposteringen Forespørgsel                                            |
| Påvirkede moduler             | Kontant- og bankstyring                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Mexicansk elektronisk CFD-faktura.

Denne funktion muliggjorde oprettelse af mexicanske elektroniske fakturaer ved hjælp af CFD-metoden (Comprobante finansiel Digital), hvor virksomheden underskriver fakturaen ved at anmode om relateret tilladelse fra regeringen. Denne funktion leverer også en månedlig rapport, der omfatter alle de elektroniske fakturaer, der er udstedt i perioden.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Denne metode anvendes ikke længere. Generering af elektroniske fakturaer ved at bruge CFD-metoden er blevet udfaset af skattemyndighederne og erstattet af CFDI-metoden (Comprobante Fiscal Digital a través de Internet ), hvor undertegnelse er uddelegeret til tredjepartsudbyderen (PAC). Den månedlige rapport er blevet fjernet, og brugerne kan bruge en forespørgselsindstilling til at forhøre sig om historiske transaktioner. |
| Erstattet af en anden funktion? | Nej                                                                                                                                                                                                                                                                                                                                                                                                        |
| Påvirkede moduler             | Debitor, Projekt                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Mexico, realiseret og ikke-realiseret købsmoms

Microsoft Dynamics AX 2012 administrerede ikke-realiseret købsmoms ved hjælp af Mexico-specifik funktionalitet til "ikke-realiseret moms".

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Identiske funktioner                                                                                             |
| Erstattet af en anden funktion? | Ja, denne funktion er erstattet af almindelig betinget momsfunktionalitet, der leveres af Kerne. |
| Påvirkede moduler             | Skat                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>Integration med Microsoft Outlook

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Denne funktionalitet er blevet erstattet af Microsoft Exchange Server-integration. |
| Erstattet af en anden funktion? | Ja                                                                            |
| Påvirkede moduler             | Salg og marketing                                                            |

### <a name="payroll-information-in-human-resources"></a>Lønoplysninger i personale

Lønoplysninger personale

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Denne funktionalitet er blevet erstattet af grundlæggende løn- og personalesider.                                                                                                                                                                                                                                              |
| Erstattet af en anden funktion? | **Frynsegoder**, **Indtjeninger** og andre relaterede sider, der tidligere var i amerikanske lønopgaver, er blevet ændret og er nu en del af den centrale personalekonfigurationen og støtter ekstern lønbehandling. Der opnås adgang til denne funktion ved hjælp af **Personale 1** &gt; **Løn**-konfigurationsnøglen. |
| Påvirkede moduler             | Personale, Løn                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Privat blokering af lager- og lokationsstyringskladder

Lager- og lokalitetsstyringskladderne understøtte ikke længere muligheden for at markere en kladde som privat for den valgte bruger. Kun processen med at blokere kladder som private for brugergrupper og blokering under redigering understøttes.

|                              |                                        |
|------------------------------|----------------------------------------|
| Årsagen til fjernelsen       | Ingen brug af funktionen blev ikke fundet. |
| Erstattet af en anden funktion? | Nej                                     |
| Påvirkede moduler             | Lagerstyring                   |

### <a name="product-builder"></a>Product Builder

Product Builder blev brugt til at konfigurere varer dynamisk fra en salgsordre, en indkøbsordre, en produktionsordre, et salgstilbud, et projekttilbud eller et varebehov. Baseret på en produktmodel, der havde modelvariabler, kunne brugeren vælge værdier, der opfyldte kundekrav og få en entydig produktvariant, der havde en stykliste og rute.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Product Builder viste X ++-kode for slutbrugere. Det understøttes ikke i den aktuelle version af Dynamics AX. Det er blevet fjernet for at undgå dobbelt vedligeholdelsesarbejde på overlappende kodebaser, hvor størrelsen kan tilpasses. |
| Erstattet af en anden funktion? | Produktkonfiguration                                                                                                                                                                                   |
| Påvirkede moduler             | Administration af produktoplysninger, Salg og marketing                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Omdøb produktdimension

Med denne funktion kan du ændre navnet på en af de tre standardproduktdimensioner (størrelse, farve eller typografi) til et navn, der passer bedre til virksomhedens behov. Omdøbning inkluderer alle de etiketter, hvor produktdimensionsnavnet blev brugt.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Den aktuelle version af Dynamics AX understøtter ikke ændringer af etiketter på kørselstidspunktet. |
| Erstattet af en anden funktion? | Nr.                                                                            |
| Påvirkede moduler             | Administration af produktoplysninger                                                |

### <a name="retail-server-connectivity-using-http"></a>Retail Server-forbindelse ved hjælp af HTTP

I Dynamics AX 2012 R3 kunne Retail Server fungere ved hjælp af HTTP-kommunikation (ikke-sikret). Dette var ud over standardkommunikationen via HTTPS.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | På grund af nye sikkerhedskrav understøttes nu kun sikret kommunikation ved hjælp af TLS 1.2 (eller nyere, afhængigt af tilgængelighed). Det selvbetjente installationsprogram konfigurerer automatisk computeren til denne kommunikation. |
| Erstattet af en anden funktion? | Nr. Kun standard HTTPS-kommunikation understøttes nu.                                                                           |
| Påvirkede moduler             | Detailserver                                                |

### <a name="role-center-pages"></a>Sider for rollebaserede områder

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Sider med det rollebaserede område var baseret på den forældede Enterprise Portal-platform, som er blevet erstattet af den nye webklientplatform i den aktuelle version af Dynamics AX. |
| Erstattet af en anden funktion? | Den nye arbejdsområdeformularmønster giver brugere et procescentreret design, der giver nem adgang til ofte anvendte opgaver inden for denne proces.                       |
| Påvirkede moduler             | Alle                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>Momsjurisdiktionsområder

|                              |                                              |
|------------------------------|----------------------------------------------|
| Årsagen til fjernelsen       | Lavt forbrug og begrænset funktionssæt |
| Erstattet af en anden funktion? | Nej                                           |
| Påvirkede moduler             | Amerikansk moms                                 |

### <a name="shipping-carrier-interface"></a>Fragtmandsgrænseflade

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Identiske funktioner                                                                                                                         |
| Erstattet af en anden funktion? | Ja, denne funktion er delvist erstattet af Transportstyring, men er endnu ikke erstattet af grundlæggende Lagerstedsstyring (WMS I). |
| Påvirkede moduler             | Salg og marketing, Lagerstyring                                                                                                       |

### <a name="sites-services"></a>Webstedstjenester

Med webstedstjenester kan du opbygge websteder, der udvider dine forretningsprocesser til internettet uden it-support.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Microsoft Azure-infrastrukturen, der bruges af Dynamics AX, indeholder nye funktioner, der kan bruges i stedet (f.eks Azure websteder). |
| Erstattet af en anden funktion? | Nej                                                                                                                                       |
| Påvirkede moduler             | Rekruttering, sagsstyring, anmodning om tilbud, registrering af kreditor                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>Strategi for SSAS-behovsprognose

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Udformningen af funktionen understøttes ikke i den nye cloud-arkitektur. |
| Erstattet af en anden funktion? | Strategi for Azure Machine Learning-behovsprognose                           |
| Påvirkede moduler             | Planlægning                                                                     |

### <a name="travel-requisitions"></a>Rejserekvisitioner

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Årsagen til fjernelsen       | Lav belastning og de fleste funktioner fandtes i Enterprise Portal. |
| Erstattet af en anden funktion? | Nej                                                              |
| Påvirkede moduler             | Udgiftsstyring                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Kreditorfakturapulje ekskl. bogføringsdetaljer

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Lav belastning. Denne funktionalitet er blevet erstattet af fakturajournalen med arbejdsgangens funktionalitet. |
| Erstattet af en anden funktion? | Funktioner i arbejdsgang for fakturajournal.                                                           |
| Påvirkede moduler             | Kreditor                                                                                        |

### <a name="virtual-company-accounts"></a>Virtuelle regnskaber

Funktionen til virtuelle regnskaber understøttes ikke længere i Dynamics AX. Funktionen til virtuelle regnskaber gør det muligt for brugere at oprette tabeller, der skulle deles med en række regnskaber. Du kan finde en beskrivelse af funktionen her: [Regnskaber og virtuelle regnskaber](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Funktionen fungerer ved at gruppere tabeller i samlinger, der er tildelt til virtuelle regnskaber, som er grupper af eksisterende "reelle" regnskaber. Forespørgsler oprettes, så alle regnskaber i det virtuelle regnskab kan få adgang til dataene i tabellerne i de tilknyttede tabelsamlinger.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Årsagen til fjernelsen</td>
<td><ul>
<li>Virtuelle regnskaber skal konfigureres, før data gemmes i tabellerne. Baglæns tilpasning af virtuelle regnskaber til en eksisterende installation er meget vanskeligt.</li>
<li>Da der har været meget datanormalisering i den aktuelle version af Microsoft Dynamics AX, er det blevet meget vanskeligt at vide, hvad der skal tilføjes i tabelsamlingen. For eksempel er det svært at vide, hvilke tabeller der skal deles. Alle de tabeller, der refereres til fra tabeller, der er i et virtuelt regnskab, skal også tilføjes. Grundet tabelnormalisering skal selv simple stamdata, der er spredt over flere tabeller, være en del af det virtuelle regnskab. Eventuelle fejl, der er foretaget her, vil medføre funktionelle problemer.</li>
<li>Når en tabel er en del af et virtuelt regnskab, mister den oplysninger om oprindelsen af dataene, og kun det virtuelle regnskab registreres.</li>
</ul></td>
</tr>
<tr class="even">
<td>Erstattet af en anden funktion?</td>
<td>Globale tabeller kan bruges til at gøre tabeller tilgængelige fra alle regnskaber. Der er i øjeblikket ingen erstatning.</td>
</tr>
<tr class="odd">
<td>Påvirkede moduler</td>
<td>Ikke tilgængelig</td>
</tr>
</tbody>
</table>

### <a name="warehouse-management-ii"></a>Lokationsstyring II

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Lagerstedsstyring II-løsningen (WMS II), der er tilgængelig i modulet **Lagerstyring**, dublerer funktioner i det **Lagerstyring**-modul, der blev udgivet i Microsoft Dynamics AX 2012 R3.                                                                         |
| Erstattet af en anden funktion? | **Lagerstyring**-modulet, der blev udgivet i AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 og Microsoft Dynamics AX 2012 R3 CU9, erstatter funktionerne i Lagerstyring II. Det nye modul har mere avancerede funktioner og mere fleksible processer til styring af lagersted end dem, der blev tilbudt til Lagerstedsstyring II. |
| Påvirkede moduler             | Lagerstyring, salg og marketing, indkøb og forsyning                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>Påmindelser for arbejdere i Personale

Lønoplysninger personale

|                              |                 |
|------------------------------|-----------------|
| Årsagen til fjernelsen       | Lav belastning       |
| Erstattet af en anden funktion? | Nej              |
| Påvirkede moduler             | Personale |

### <a name="workplanner"></a>Arbejdsplanlægning

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Lav belastning                                                                                                                                                            |
| Erstattet af en anden funktion? | Nej, men siden **Profilrelation**, som åbnes fra siden **Profilgrupper**, understøtter det samme forretningsscenario som den forældede **Arbejdsplanlægning**-side. |
| Påvirkede moduler             | Tid og fremmøde                                                                                                                                                  |

### <a name="x-financial-statements"></a>X++-regnskaber

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| Årsagen til fjernelsen       | Denne funktion er blevet erstattet af en anden funktion.                                    |
| Erstattet af en anden funktion? | Management Reporter (med navnet **Økonomirapportering** i den aktuelle version af Dynamics AX) |
| Påvirkede moduler             | Finans                                                                              |






