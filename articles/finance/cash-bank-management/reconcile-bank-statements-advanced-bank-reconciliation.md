---
title: Afstemme bankkontoudtog ved hjælp af avanceret bankafstemning
description: Med den avancerede bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme dem med banktransaktioner i Microsoft Dynamics 365 Finance. I denne artikel beskrives afstemningsprocessen.
author: moaamer
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationWorksheet
audience: Application User
ms.reviewer: kfend
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e5b229821fc1ca1caa55b733af293aaef65a171
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859858"
---
# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Afstemme bankkontoudtog ved hjælp af avanceret bankafstemning

[!include [banner](../includes/banner.md)]

Med den avancerede bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme dem med banktransaktioner i Dynamics 365 Finance. I denne artikel beskrives afstemningsprocessen.  

## <a name="import-an-electronic-bank-statement"></a>Importere et elektronisk bankkontoudtog

Du kan importere dine kontoudtog fra banken ved hjælp af handlingen **Importér kontoudtog** på siden **Bankkontoudtog** side. Bankkontoen identificeres på bankkontoudtoget via en kombination af værdier, der angives for bankkontooplysningerne. Disse værdier omfatter bankens navn, bankkontonummer, registreringsnummer, SWIFT-kode (Society for Worldwide Interbank Financial Telecommunication) og IBAN-nummer (International Bank Account Number). 

Du kan overføre et bankkontoudtog, der indeholder oplysninger om enten en enkelt konto eller flere konti. Hvis der er flere konti, kan kontiene være i forskellige juridiske enheder.

-   For at importere en enkelt bankkontofil for en enkelt konto skal du vælge **Nej** i indstillingen **Importér kontoudtog for flere bankkonti i alle juridiske enheder** og vælge den bankkonto, der er tilknyttet kontoudtoget. Klik på **Gennemse** for at vælge den tilknyttede bankkontofil, og klik derefter på **Overfør**.
-   For at importere en enkelt bankkontofil for flere konti skal du vælge **Ja** i indstillingen **Importér kontoudtog for flere bankkonti i alle juridiske enheder**. Klik på **Gennemse** for at vælge den tilknyttede bankkontofil, og klik derefter på **Overfør**.

Hvis nogen kontoudtog i den elektroniske fil ikke kan knyttes til en bankkonto, eller hvis det er knyttet til flere bankkonti ved hjælp af id-felterne, kan de ikke importeres. Dog kan andre kontoudtog i filen stadig importeres. Brugeren modtager derefter en meddelelse om, at import af bankkontoudtog lykkedes for bestemte bankkonti. Bemærk, at den bruger, der importerer bankkontoudtogsfilen, skal have adgang til en juridisk enhed for at importere kontoudtog for den juridiske enheds bankkonti. 

Du kan også bruge en zip-fil til at overføre flere kontoudtogsfiler til Finance i en enkelt proces. For at importere flere bankkontofiler for flere konti kan du kombinere alle bankkontofiler i én zip-fil. I dialogboksen **Importér bankkontoudtog** skal du vælge **Ja** i indstillingen **Importér kontoudtog for flere bankkonti i alle juridiske enheder**. Klik på **Gennemse** for at vælge den zip-fil, der indeholder bankkontofilerne, og klik derefter på **Overfør**. Importen vil genkende zip-filen og overføre hvert kontoudtog, som indgår i den, uanset den juridiske enhed for bankkontoen.

Indstillingen **Afstem efter import** er tilgængelig. Når denne indstilling er indstillet til **Ja**, validerer systemet automatisk bankkontoudtoget, opretter en ny bankafstemning og et regneark og kører Standard for sammenholdningsregelsæt, når kontoudtoget er blevet overført. Denne funktion automatiserer processen indtil det punkt, hvor posteringerne skal afstemmes manuelt.

## <a name="validate-the-bank-statement"></a>Validere bankkontoudtoget
Når du vil validere et kontoudtog, skal du klikke på **Valider** på siden **Bankkontoudtog**. Bankkontoudtog skal valideres, før de kan afstemmes. Dette trin udføres automatisk, hvis **Afstem efter import** er indstillet til **Ja** på tidspunktet for importen. 

Valideringen af bankkontoudtog kontrollerer følgende:

-   Bankkontoudtoget svarer til den valgte bankkonto.
-   Valutaen på bankkontoudtoget svarer til valutaen for bankkontoen.
-   Startsaldoen for bankkontoudtoget er lig med ultimosaldoen for det forrige kontoudtog for bankkontoen.
-   Datoen overlapper ikke datoen for et andet bankkontoudtog for den samme bankkonto.
-   Der er ingen huller i datoerne for bankkontoudtog for bankkontoen.
-   Datoer på kontoudtogslinjerne ligger mellem fra-datoen og til-datoen i bankkontoudtoget.
-   Startsaldoen og opsummerede linjebeløb er lig med slutsaldoen.

Når valideringen er fuldført, opdateres status for bankkontoudtoget til **Valideret**. Et bankkontoudtog skal valideres, før det kan afstemmes.

## <a name="reconcile-the-bank-statement"></a>Afstemme bankkontoudtoget
Når du har importeret et elektronisk bankkontoudtog og valideret kontoudtoget på siden **Bankkontoudtog**, kan du afstemme bankkontoudtoget ved hjælp af siderne **Bankafstemning** og **Bankafstemningsarbejdsark**. 

På siden **Bankafstemning** skal du klikke på **Ny** for at oprette en ny afstemning og derefter vælge bankkontoen for det kontoudtog, der blev importeret. En bankkonto kan kun have én åben bankafstemning. Skæringsdatoen bestemmer transaktionerne på bankkontoudtoget og de Operations-bankposteringer, der er medtaget i afstemningsarbejdsarket. Som standard bruges den aktuelle systemdato som skæringsdatoen, men du kan ændre datoen for afstemningen. De resterende oplysninger i hovedet hentes automatisk fra kontoudtoget. Dette trin udføres automatisk, hvis **Afstem efter import** er indstillet til **Ja** på tidspunktet for importen. 

På siden **Bankafstemning** skal du klikke på **Regneark** for at åbne siden **Bankafstemningsarbejdsark**. Hvis indstillingen **Afstem efter import** er **Ja**, køres Standard for sammenholdningsregelsæt automatisk for afstemningen. Hvis du vil køre sammenholdningsregler manuelt, skal du klikke på **Kør sammenholdningsregler** for at vælge de sammenholdningsregelsæt eller sammenholdningsregler, der skal køres mod bankposteringerne. Hvis du har mange transaktioner at behandle, kan du udføre dette trin som en batchproces. 

Siden **Bankafstemningsarbejdsark** har fire gitre, der indeholder posteringer. De to øverste gitre viser transaktioner fra kontoudtoget og Operations, der endnu ikke er afstemt. De to nederste gitre viser afstemte posteringer. Fanen **Transaktionsdetaljer i bankkontoudtog** vises oplysninger om den ikke-sammenholdte kontoudtogspostering, der er valgt i det øverste gitter. 

Der er tre måder at sammenholde eller afstemme transaktioner på bankkontoudtog:

-   Sammenhold transaktionerne med bankposteringer i Operations.
-   Sammenhold transaktioner med en tilbageførselstransaktion for bankkontoudtoget.
-   Markér transaktionerne som **Ny**, så de kan bogføres senere som en banktransaktion i Finance.

Du sammenholder transaktioner manuelt ved at vælge transaktionerne i gitteret **Bankkontoudtogstransaktioner**, markere de tilsvarende transaktioner i gitteret **Operations-bankposteringer** og derefter klikke på **Afstem**. De valgte posteringer flyttes fra de øverste gitre for ikke-sammenholdte transaktioner til de lavere gitre for sammenholdte posteringer. Desuden opdateres de samlede sammenholdte og ikke-sammenholdte beløb. Du kan have én-til-én, mange-til-en og mange-til-mange-transaktionssammenholdelser. Sammenholdelser skal følge reglerne for tilladte datodifferencer og tilknytning af transaktionstype. Disse regler angives på siden **Kontant- og bankstyringsparametre**.

Der kan forekomme øredifferencer i din afstemning. Du kan sammenholde en enkelt bankkontoudtogstransaktion med en enkelt Operations-banktransaktion, som har øredifferencer, hvis øredifferencerne er inden for det tolerancebeløb, der er defineret af feltet **Tilladt øredifference** på bankkontoen. Beløbet vises i feltet **Korrektionsbeløb** på den matchede Operations-banktransaktion. Når bankafstemningen er markeret som afstemt, bliver korrektioner automatisk bogført ved hjælp af den hovedkonto, der er defineret i den tilknyttede banktransaktionstype. Korrektioner understøttes ikke for dokumenttyperne **Bankcheck** og **Depositum**. 

Tilbageførsel af bankkontoudtogtransaktioner sammenholdes ved hjælp af afstemningsarbejdsarket. To kontoudtogslinjer kan sammenholdes, hvis beløbene er modsat, og hvis en af posteringerne er markeret som en tilbageførsel. Du kan også oprette en sammenholdelsesregel for handlingen **Ryd opgørelseslinjer til tilbageførsel**.

Tilbageførte Operations-banktransaktioner skal afstemmes ved hjælp af siden **Operations-banktransaktioner**. Du kan afstemme to Operations-banktransaktioner sammen, hvis dokumenterne har den samme bankkonto, dokumenttype og betalingsreference, og hvis de har modbeløb. Du kan også afstemme en enkelt annulleret check for at forhindre, at disse transaktioner vises på afstemningsarbejdsarket. 

Hvis der er nye banktransaktioner, som er iværksat af banken, f.eks renter, afgifter og gebyrer, som endnu ikke findes i Finance, kan du føje dem til en kladde, der er tilknyttet den valgte afstemning af bankkontoudtoget. Vælg en bankkontoudtogstransaktion i gitteret **Bankkontoudtogstransaktioner** for ikke-sammenholdte transaktioner, og klik derefter på **Markér som ny**. Status for transaktionen indstilles til **Ny**, og transaktionen flyttes til gitteret **Bankkontoudtogstransaktioner** for sammenholdte posteringer. Du skal bogføre posteringer, der er markeret som **Ny** senere fra siden **Bankkontoudtog**. 

Du kan fjerne sammenholdelse af transaktioner, der er sammenholdt ukorrekt. Vælg den sammenholdte bankkontoudtogstransaktion, og klik derefter på **Fjern sammenholdning**. Alle tilknyttede transaktioner flyttes tilbage til de øverste gitre for ikke-sammenholdte transaktioner, og de samlede sammenholdte og ikke-sammenholdte beløb opdateres. 

Når du har afsluttet afstemningsprocessen, skal du markere bankafstemningsarbejdsarket som afstemt.  Denne proces bogfører automatisk rettelsesbeløb ved hjælp af de konti, der er angivet på siden **Bankposttyper**.  Bankafstemningen for en opgørelse kan markeres som afstemt når som helst, selv hvis der er bankkontoudtogslinjer, der endnu ikke er afstemt.  De uafstemte posteringer flyttes automatisk til næste afstemningsregneark som uafstemte banktransaktioner, der skal afstemmes.  Bemærk, at når en afstemning af bankkontoudtog er markeret som afstemt, kan den ikke fortrydes.  Afstemningen kan ikke længere redigeres, og du vil ikke længere have mulighed for at foretage opdateringer af afstemningen.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Bogføre nye transaktioner, der er knyttet til afstemningen
Bankkontoudtogstransaktioner, du har markeret som **Ny** på afstemningsarbejdsarket, bogføres på siden **Bankkontoudtog**. På siden **Bankkontoudtog** skal du vælge kontoudtogs-id'et for at få vist oplysninger på kontoudtoget. I menuen **Regnskab** kan du bruge indstillingerne **Få vist fordelinger** og **Vis regnskab** til at få vist detaljerne bag de nye transaktioner, og de tilknyttede poster. Vælg indstillingen **Bogfør** for at bogføre de bankkontoudtogslinjer, der er markeret som **Ny**, i finansmodulet. Det er vigtigt at bemærke, at der kun kan udføres bogføring én gang pr. bankkontoudtog.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
