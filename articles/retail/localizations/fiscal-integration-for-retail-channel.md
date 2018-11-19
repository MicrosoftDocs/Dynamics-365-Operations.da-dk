---
title: Regnskabsintegration for detailkanal
description: Dette emne indeholder en oversigt over regnskabsintegrationen for Retail POS.
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: da-dk
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Regnskabsintegration for detailkanal

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over funktionen til regnskabsintegration, der er tilgængelig i Microsoft Dynamics 365 for Retail. Regnskabsintegrationsfunktionen er en struktur, der er udviklet til at understøtte lokal regnskabslovgivning, som har til formål at hindre svindel i detailbranchen. Typiske scenarier, som regnskabsintegrationen kan omfatte:

- Udskrivning af en regnskabskvittering, som gives til kunden.
- Sikring af indsendelse af de oplysninger, der vedrører salg og returneringer i POS til en ekstern tjeneste, der leveres af myndigheden.
- Brug af databeskyttelse med en digital signatur, der er godkendt af myndigheden.

Dette emne indeholder retningslinjer for konfiguration af regnskabsintegration, så brugerne kan udføre følgende opgaver. 

- Konfigurere regnskabsforbindelser, som er regnskabsenheder eller -tjenester, der bruges til regnskabsmæssig registrering som lagring, digitale signaturer og beskyttet indsendelse af regnskabsdata.
- Konfigurere den dokumentudbyder, der definerer en outputmetode og en algoritme til generering af regnskabsdokumenter.
- Konfigurere den regnskabsmæssige registreringsproces, som definerer en række trin og en gruppe af forbindelser, der bruges på hvert trin.
- Tildele regnskabsregistreringsprocesser til POS-funktionalitetsprofiler.
- Tildele tekniske connectorprofiler, enten til hardwareprofiler (til de lokale regnskabsforbindelser) eller til POS-funktionalitetsprofiler (til andre regnskabsconnectortyper).

## <a name="fiscal-integration-execution-flow"></a>Kørselsproces for regnskabsintegration
Følgende eksempel viser den almindelige kørselsproces for regnskabsintegration.

1. Initialisering af regnskabsregistreringprocessen.
  
   Når du har udført nogle handlinger, hvor regnskabsregistrering er nødvendig, f.eks. når en detailtransaktion er fuldført, knyttes regnskabsregistreringsprocessen til den aktuelle POS-funktionalitetsprofil.

1. Søg efter en regnskabsconnector.
   
   For hvert trin i regnskabsregistreringen, der indgår i regnskabsregistreringsprocessen, sammenligner systemet listen over regnskabsconnectorer. Disse connectorer har en funktionel profil, der indgår i angivne connectorgruppe, med en liste over connectorer, der har en teknisk profil knyttet til den aktuelle hardwareprofil (kun for en connectortype, der er lig med **Lokal**) eller til den aktuelle POS-funktionalitetsprofil (for andre typer af connectorer).
   
1. Udfør regnskabsintegrationen.

   Systemet udfører alle nødvendige handlinger, der er defineret af en assembly, der er knyttet til den fundne connector. Dette gøres i overensstemmelse med indstillingerne for den funktionelle profil og den tekniske profil, der blev fundet i det forrige trin for denne connector.

## <a name="setup-needed-before-using-fiscal-integration"></a>Nødvendig konfiguration før brug af regnskabsintegration
Før du bruger funktionen til regnskabsintegration, skal du definere følgende indstillinger:

- Definer nummerserien på siden **Detailparametre** for regnskabsfunktionens profilnummer.
  
- Definer nummerserierne på siden **Delte parametre for detail** for følgende referencer:
  
  - Regnskabsteknisk profilnummer
  - Regnskabsconnectorgruppenummer
  - Registreringsprocesnummer

- Opret en **Regnskabsconnector** i **Retail > Konfiguration af kanal > Regnskabsintegration > Regnskabsconnectorer** for hver enhed eller tjeneste, du planlægger at bruge med henblik på regnskabsintegration.

-  Opret en **Udbyder af regnskabsdokumenter** i **Retail > Konfiguration af kanal > Regnskabsintegration > Udbydere af regnskabsdokumenter** for alle regnskabsconnectorer. Datatilknytning betragtes som en del af regnskabsdokumentudbyderen. Hvis du vil oprette andre datatilknytninger for samme connector (som f.eks. specifik lovgivning), skal du oprette forskellige regnskabsdokumentudbydere.

- Opret en **Funktionel profil for connector** i **Retail > Konfiguration af kanal > Regnskabsintegration > Funktionelle profiler for connector** for hver regnskabsdokumentudbyder.
  - Vælg et connectornavn.
  - Vælg en dokumentudbyder.
  - Angiv indstillinger for momssatser under fanen **Konfiguration af tjeneste**.
  - Angiv tilknytning af momskoder og betalingsmiddeltype under fanen **Tilknytning af data**.

  #### <a name="examples"></a>Eksempler 

  |  | Format | Eksempel | 
  |--------|--------|--------|
  | Indstillinger for momssats | værdi : VATrate | 1 : 2000, 2 : 1800 |
  | Tilknytning af momskoder | VATcode : værdi | vat20 : 1, vat18 : 2 |
  | Tilknytning af betalingsmiddeltyper | TenderTyp : værdi | Kontant : 1, Kort : 2 |

- Opret **Regnskabsconnectorgrupper** i **Retail > Konfiguration af kanal > Regnskabsintegration > Regnskabsconnectorgruppe**. En connectorgruppe er et undersæt af funktionelle profiler, der er knyttet til regnskabsconncetorer, der udfører samme funktioner og bruges på samme stadie i en regnskabsregistreringsproces.

   - Tilføj funktionelle profiler til connectorgruppen. Klik på **Tilføj** på siden **Funktionelle profiler**, og vælg et profilnummer.
   - Hvis du vil afbryde brugen af den funktionelle profil, kan du indstille **Deaktiver** til **Ja**. 
   
     Denne ændring påvirker kun den aktuelle connectorgruppe. Du kan fortsætte med at bruge den samme funktionelle profil i andre connectorgrupper.

     >[!NOTE]
     > I en connectorgruppe kan hver regnskabsconnector kun have én funktionel profil.

- Opret en **Teknisk profil for connector** i **Retail > Konfiguration af kanal > Regnskabsintegration > Tekniske profiler for connector** for hver regnskabsconnector.
  - Vælg et connectornavn.
  - Vælg en connectortype: 
      - **Lokal** - Indstil denne type til fysiske enheder eller programmer, der er installeret på en lokal computer.
      - **Intern** - Indstil denne type til regnskabsenheder og -tjenester, der er tilknyttet Retail Server.
      - **Ekstern** - Til eksterne regnskabstjenester som f.eks. en webportal, der er leveret af en skattemyndighed.
    
  - Angiv indstillinger under fanen **Forbindelse**.

      
 >[!NOTE]
 > En opdateret version af en konfiguration, der blev indlæst tidligere, indlæses for både funktionelle og tekniske profiler. Hvis en passende connector eller dokumentudbyder allerede er i brug, får du besked. Som standard gemmes alle ændringer, der er oprettet manuelt i funktionelle og tekniske profiler. For at tilsidesætte disse profiler med standardsættet af parametre fra en konfiguration, skal du klikke på **Opdater** på siden **Funktionelle profiler for connector** og siden **Tekniske profiler for connector**.
 
- Opret en **Proces for regnskabsregistrering** i **Retail > Konfiguration af kanal > Regnskabsintegration > Processer for regnskabsregistrering** for hver entydige proces til en regnskabsintegration. En registreringsproces defineres af rækkefølgen af trinnene i registreringen og den connectorgruppe, der er brugt i hvert trin. 
  
  - Føj registreringstrin til processen:
      - Klik på **Tilføj**.
      - Vælg en connectortype.
      
      >[!NOTE]
      > Dette felt definerer, hvor systemet søger i en teknisk profil for connectoren, enten i hardwareprofiler for connectortypen at skrive **Lokal** eller i POS-funktionalitetsprofiler for andre regnskabsconnectortyper.
      
   - Vælg en connectorgruppe.
   
     >[!NOTE]
     > Klik på **Valider** for at kontrollere integriteten af registreringsprocesstrukturen. Det anbefales, at der foretages valideringer i følgende tilfælde:
       >- Ved en ny registreringsproces, når alle indstillinger er fuldført, herunder binding til POS-funktionalitetsprofiler og hardwareprofiler.
       >- Når du har foretaget opdateringer af en eksisterende registreringsproces.

-  Bind regnskabsregistreringsprocesser til POS-funktionalitetsprofiler i **Retail > Konfiguration af kanal > POS-opsætning > POS-profiler > Funktionalitetsprofiler**.
   - Klik på **Rediger**, og vælg et **Procesnummer** under fanen **Regnskabsregistreringsproces**.
- Bind tekniske connectorprofiler til hardwareprofiler i **Retail > Konfiguration af kanal > POS-opsætning > POS-profiler > Hardwareprofiler**.
   - Klik på **Rediger**, og klik derefter på **Ny** under fanen **Regnskabsteknisk profil**.
   - Vælg en teknisk connectorprofil i feltet **Profilnummer**.
   
     >[!NOTE]
     > Du kan tilføje flere tekniske profiler til en hardwareprofil. Men dette understøttes ikke, hvis en hardwareprofil har mere end ét skæringspunkt med en connectorgruppe. Hvis du vil undgå forkerte indstillinger, anbefales det, at du validerer registreringsprocessen, når du har opdateret alle hardwareprofiler.

