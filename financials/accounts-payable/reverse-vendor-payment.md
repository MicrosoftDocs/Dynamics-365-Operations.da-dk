---
title: "Tilbageføre en kreditorbetaling"
description: "I denne artikel beskrives forskellene mellem tilbageførsel, sletning, annullering og afvisning af en betaling. Derudover forklarer den de to metoder til at tilbageføre en check til kreditor."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4f8b77efabe0c002654dac0b80d721a79dc42003
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="reverse-a-vendor-payment"></a>Tilbageføre en kreditorbetaling

[!include[banner](../includes/banner.md)]


I denne artikel beskrives forskellene mellem tilbageførsel, sletning, annullering og afvisning af en betaling. Derudover forklarer den de to metoder til at tilbageføre en check til kreditor. 

Når en kreditorbetaling er bogført, kan det ske, at betalingen skal tilbageføres. Tilbageførsel er ikke det samme som at slette, annullere eller afvise en betaling. Du kan kun slette en betaling, hvis status er **Oprettet**. Denne status angiver, at betalingen er blevet oprettet, men endnu ikke er blevet genereret. Denne begrænsning gælder altid, uanset betalingsmåden. Du kan annullere ikke-bogførte checks, når de er blevet genereret, men før de er blevet bogført. Hvis den genererede betaling foretages som en elektronisk pengeoverførsel (EFT), kan du afvise betalingen, før den bogføres. Hvis du vil afvise en betaling, kan du ændre værdien **Betalingsstatus**. En betaling, der er blevet nedlagt eller afvist, kan gendannes, når værdien **Betalingsstatus** er ændret tilbage **Ingen**. 

Når en betaling er blevet bogført, bruges tilbageførsler. Betalinger, der foretages elektronisk, kan ikke tilbageføres, når de er blevet bogført. I stedet skal der oprettes en ny transaktion for betalingsbeløbet for at få passivet tilbage på kreditorens konto. Der er to metoder til tilbageførsel af bogførte checks. I den ene metode bogføres tilbageførsler straks, når du klikker på **Annullering af checks** på siden **Check**. Den anden metode indebærer, at når du klikker på **Annullering af checks** på siden **Check**, sendes tilbageførslen først til kladden til annullering af check i Kontant- og bankstyring, hvor en evaluator derefter kan bogføre eller afvise tilbageførslen. 

Hvis du vil have mere at vide om, hvilken metode der bruges i din organisation, skal du åbne siden **Kontant- og bankstyringsparametre**. Hvis indstillingen **Brug evalueringsprocessen til annullering af checks** er angivet til **Ja**, sendes tilbageførsler til tilbageførselskladden til gennemsyn. I følgende tabel beskrives, hvordan metoderne til tilbageførsel af checks er forskellige.

| Hvis din organisation ikke gennemgår tilbageførsler før bogføring                                                                                                                                  | Hvis din organisation gennemgår tilbageførsler før bogføring                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Checken tilbageføres straks, når du klikker på **OK** på siden **Check**.                                                                                                                      | Checken tilbageføres ikke øjeblikkeligt. Der oprettes en kladde til tilbageførsel af check til gennemsyn. Hvis kladden til tilbageførsel af check slettes, kan checken tilbageføres igen.                                                                                                                                                                                                                                                                |
| Regnskabsposterne for den oprindelige check er tilbageført.                                                                                                                                         | Finanskontoen fra kontoposten for den oprindelige check er muligvis ikke bogført. De økonomiske dimensioner fra kladden til den oprindelige check bruges som de økonomiske standarddimensioner i kladden for tilbageførsel af check. Du kan ændre disse standardværdier. Når tilbageførselskladden for checken er bogført, indtastes der automatisk værdier i hovedkontiene til Kreditor fra de posteringsprofiler, der muligvis er ændret. |
| De regnskabsmæssige strukturer, der blev brugt ved bogføringen af den oprindelige check, bruges til at tilbageføre checken, også selvom kontostrukturen er blevet ændret. Kontokombinationen er ikke valideret. | Hvis en kontostruktur blev ændret, efter at den oprindelige check blev bogført, kræves der muligvis en ny økonomisk dimension for tilbageførsel af checken. Denne økonomiske dimension kan måske ikke indsættes automatisk fra den oprindelige betalingskladde. Kontokombination valideres, når tilbageførslen af checken er bogført.                                                                                                        |
| Faste dimensioner anvendes ikke ved tilbageførsel for at sikre, at de samme finanskonti tilbageføres.                                                                                      | Faste dimensioner anvendes på kladden til tilbageførsel af check under bogføringen. Den økonomiske dimensionsværdi findes muligvis ikke i regnskabsposten til den oprindelige check, afhængigt af hvornår den faste dimension blev defineret.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Tilbageføre bogførte check uden at gennemse dem
Hvis din virksomhed ønsker at bogføre tilbageførsler af checks med det samme, når du klikker på **Annullering af checks** på siden **Checks**, skal du følge disse trin: På siden **Kontant- og bankstyringsparametre** skal du angive indstillingen **Brug evalueringsprocessen til annullering af checks** til **Nej**. På siden **Checks** kan du vælge den check, der skal tilbageføres, og vælge **Annullering af checks**. Du kan derefter angive datoen og vælge en årsag til tilbageførslen.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Tilbageføre bogførte checks, efter at de er blevet gennemgået i kladden til tilbageførsel af check
Hvis din virksomhed ønsker at gennemgå tilbageførsel af checks, før de bogføres, kan du oprette en checktilbageførselskladde til gennemsyn og på siden **Kontant- og bankstyringsparametre** skal du angive indstillingen den **Brug evalueringsprocessen til annullering af checks** til **Ja**. På siden **Checks** kan du vælge den check, der skal tilbageføres, og vælge **Annullering af checks**. Du kan derefter angive datoen og vælge en årsag til tilbageførslen. Du skal også vælge et kladdenavn for at oprette en kladde i checktilbageførselskladden.

### <a name="review-a-reversal"></a>Evaluere en tilbageførsel

Hvis du er en bruger, der skal evaluere tilbageførsler, kan du enten godkende og bogføre kladden eller afvise tilbageførslen ved at slette kladden. På siden **Tilbageførsel af checks** kan du vælge den tilbageførselskladde, der skal gennemses, og derefter klikke på **Linjer**. Du kan evaluere den tilbageførte check og derefter vælge en af følgende godkendelsesindstillinger:

-   Hvis du vil godkende og bogføre tilbageførselskladden, skal du klikke på **Bogfør** eller **Bogfør og overfør**.
-   Hvis du vil afvise tilbageførslen, skal du slette checktilbageførselskladden.

> [!NOTE]
> Hvis du sletter kladden, fjernes tilbageførslen fra systemet, men den oprindelige check bevares på siden **Check**. Checkens status er ikke længere **Afventer annullering**.

## <a name="results-of-posting-a-reversal"></a>Resultater af at bogføre en tilbageførsel
Når du bogfører en checktilbageførsel, sker følgende:

-   Checkens status opdateres til statussen **Annullering**.
-   Hvis indstillingen **Afstem** er valgt på tilbageførselssiden under tilbageførslen, afstemmes checken (indstillingen **Afstemt** vælges), og den vises ikke på siden **Kontoafstemning**.
-   Tilbageførselsbilaget bogføres mod den bankkonto, som checken blev udstedt fra, hvilket opskriver saldoen på bankkontoen.
-   Bilaget bogføres i finansmodulet.
-   Oplysningerne om ændringerne opdateres i feltgruppen **Oversigt** på siden **Check**.

> [!NOTE] 
> Når du tilbagefører en check, der blev udstedt for en intern handelstransaktion, kommer modposteringerne fra opsætningen af den interne handelstransaktion og ikke fra den oprindelige postering. Hvis den tilbageførte check blev udstedt til en kreditorbetaling, vil følgende også ske:

-   Tilknytningen til den oprindelige betaling fra den faktura, som betalingen blev udlignet mod, ophæves (udligningen tilbageføres).
-   Der bogføres en postering mod kreditorkontoen for betalingstilbageførslen, og den tilbageførte betaling udlignes mod den oprindelige betaling. Feltet **Sidste udligningsbilag** på siden **Kreditorposteringer** for den oprindelige kreditorbetaling opdateres, så det afspejler bilagsnummeret for den tilbageførte postering.

Hvis den tilbageførte check blev udstedt til en debitorrefusion, vil følgende også ske:

-   Der bogføres en postering for betalingstilbageførslen mod debitorkontoen, og udligningen mellem den oprindelige betaling og det dokument, som betalingen oprindeligt blev udlignet mod, tilbageføres (der oprettes en negativ betaling).
-   Der knyttes en betalingstilbageførsel til den oprindelige betaling. Feltet **Sidste udligningsbilag** på siden **Kundetransaktioner** for den oprindelige debitorbetaling opdateres, så det afspejler bilagsnummeret for den tilbageførte postering.





