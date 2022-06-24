---
title: Servicemiljøer
description: Denne artikel indeholder oplysninger om tjenestemiljøer til elektronisk fakturering, og hvordan du konfigurerer dem.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8c743c5b2fbc7dcc3ae04fa4d7ca0e65de6c2507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901241"
---
# <a name="service-environments"></a>Tjenestemiljøer

[!include [banner](../includes/banner.md)]

Tjenestemiljøer er logiske partitioner, der er oprettet for at understøtte Globaliseringsfunktioner og de tilhørende dokumenter, der behandles i den elektroniske faktureringsservice. Sikkerhedsfunktionerne og de digitale certifikater, og de nye adgangsrettigheder (styring), skal konfigureres på tjenestemiljøniveau.

Du kan oprette lige så mange tjenestemiljøer, du har brug for. Alle de tjenestemiljøer, som du opretter, er uafhængige af hinanden. Som bedste praksis anbefales det, at du opretter mindst to servicemiljøer:

- Et miljø, der kan anvendes til hovedudviklings- og valideringsformål. Dette miljø er typisk til test af brugeraccept (UAT).
- Et miljø, der anvendes til produktionsformål. Dette miljø er normalt et produktionsmiljø.

Denne type partitionering hjælper med at sikre, at e-faktureringsprocesserne valideres og tilpasses i sandboksen, før de går til produktion.

Tjenestemiljøer skal oprettes og vedligeholdes i Regulatory Configuration Service (RCS). Når de er klar, skal de publiceres til den elektroniske faktureringsservice. Publiceringsprocessen sender parametrene for servicemiljøet fra RCS-forekomsten til den elektroniske faktureringsservice.

Hvis du ikke fuldfører publiceringsprocessen, efter du har oprettet et nyt servicemiljø eller har justeret et eksisterende servicemiljø (f.eks. ved at tilføje eller fjerne brugere eller Microsoft Azure Key Vault-hemmeligheder), gælder ændringerne ikke. Det er kun publicerede miljøer, som Dynamics 365 Finance eller Dynamics 365 Supply Chain Management kan få adgang til.

## <a name="service-environment-statuses"></a>Statusser for servicemiljøer

Servicemiljøer kan administreres via deres status. Du kan få vist status for et miljø på siden **Servicemiljøer**. Følgende statusser er tilgængelige:

- **Ikke udgivet** – Miljøet er oprettet, men det er endnu ikke udgivet.
- **Publiceret** – Miljøet er publiceret til den elektroniske faktureringsservice.
- **Ændret** – Attributterne i et udgivet miljø er ændret, men ændringerne er endnu ikke publiceret.

## <a name="users"></a>Brugere

De enkelte servicemiljøer skal indeholde en oversigt over de brugere, der kan oprette forbindelse til Elektronisk fakturering fra Finans eller Supply Chain Management.

## <a name="applications"></a>Anvendelser

I nogle scenarier kan andre programmer end Finans eller Supply Chain Management oprette forbindelse til den elektroniske faktureringsservice for at sende elektroniske dokumenter til videre behandling eller for at hente oplysninger, f.eks. afsendelsesstatus for et dokument. I disse scenarier skal programmet defineres på listen over programmer. På denne måde vil det have adgang til tjenesten Elektronisk fakturering. Programmet skal også registreres som et program i Azure Active Directory (Azure AD), og objekt-id'et skal bruges til at identificere det. 

Da Microsoft kræver højt sikkerhedsniveau og kontrol over programmer, der kan oprette forbindelse til den elektroniske faktureringsservice, skal du kontakte Microsoft på <DGXRegulatoryservicesengineering@service.microsoft.com> og angive følgende oplysninger om dit program:

- Azure AD-lejer-id
- Microsoft Dynamics Lifecycle Services-miljø-id (LCS)
- Program-id (klient-id)
- Objekt-id
- Berettigelse og en beskrivelse på højt niveau af programmet

Microsoft vil evaluere anmodningen og registrere programmet i sikkerhedsregisteret for at sikre, at programmet fungerer sammen med elektronisk fakturering.

## <a name="number-sequences"></a>Nummerserier

Hvis dine scenarier kræver nummerserier (f.eks. i filnavne), kan du bruge nummerserier, der er defineret for et bestemt miljø, men som kan bruges enten på tværs af globaliseringsfunktioner eller til en bestemt globaliseringsfunktion. Når der er defineret en nummerserie, kan du bruge den i variabler og behandlingspipelines. Hvis du vil spore brugen skal du søge efter værdien **Aktuel** for parameteren **I brug** på siden **Nummerserier**.

### <a name="working-with-number-sequences"></a>Arbejde med nummerserier
På siden **Nummerserier**: 

- Vælg **Ny** for at oprette en nummerserie. Angiv derefter et navn og en beskrivelse. 
- Vælg **Slet** for at slette en nummerserie, hvis den ikke længere bruges.
- Du behøver ikke vælge **Publicer** i handlingsruden for at publicere ændringerne af en nummerserie. Opdateringen foretages automatisk.

## <a name="create-a-key-vault-reference"></a>Oprette en Key Vault-reference

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktionen** i sektionen **Miljø** skal du vælge feltet **Elektronisk fakturering**.
3. På siden **Miljøkonfiguration** skal du vælge **Servicemiljøer** i handlingsruden.
4. På siden **Tjenestemiljøer** skal du i handlingsruden vælge **Key Vault-parametre**.
5. Vælg **Ny** på siden **Parametre for Key Vault** for at oprette en Key Vault-reference.
6. Angiv navnet på Key Vault-referencen i feltet **Navn**.
7. Indtast en beskrivelse i feltet **Beskrivelse**.
8. Indsæt Key Vault-URI fra Key Vault (`https://<your key vault>.vault.azure.net/`) i feltet **Key Vault-URI**. Du kan finde flere oplysninger i [Oprette en Azure Key Vault i Azure-portalen](e-invoicing-create-azure-key-vault-azure-portal.md).
9. Vælg **Gem**.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Oprette en hemmelighed for lagerkontoens hemmelighedstoken

1. Vælg den Key Vault-reference, du oprettede ovenfor, på siden **Key Vault-parametre**, og vælg derefter **Tilføj** i sektionen **Certifikater**.
2. Angiv navnet på lagerkontohemmeligheden i feltet **Navn**. Dette navn skal svare til navnet på den Key Vault-hemmelighed, der indeholder lagertoken for den delte adgangssignatur (SAS). Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto i Azure-portalen](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. Indtast en beskrivelse i feltet **Beskrivelse**.
4. I feltet **Type** skal du vælge **Hemmelighed**.
5. Vælg **Gem**.
    
## <a name="create-a-service-environment"></a>Opret et servicemiljø

1. På siden **Servicemiljøer** skal du vælge **Nyt** for at oprette et servicemiljø.
2. Angiv navnet på det elektroniske faktureringsmiljø i feltet **Navn**.
3. Indtast en beskrivelse i feltet **Beskrivelse**.
4. Vælg navnet på den hemmelige lagerkonto, der skal bruges til godkendelse af adgang til lagringskontoen, i feltet **Opbevaring af SAS-token**.
5. I afsnittet **Brugere** skal du vælge **Tilføj** for at tilføje en bruger, som har tilladelse til at sende elektroniske fakturaer gennem miljøet og oprette forbindelse til lagerkontoen.
6. Angiv **Bruger-id** i feltet for brugerens alias. 
7. I feltet **E-mail** skal du angive brugerens e-mailadresse.
8. Vælg **Gem**.
9. Vælg **Publicer** i handlingsruden for at publicere miljøet til den elektroniske faktureringsservice. Kontrollér, at værdien i feltet **Status** er ændret til **Publiceret**.
