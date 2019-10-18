---
title: Samarbejde med kreditorer ved hjælp af kreditorportalen
description: I dette emne forklares, hvordan indkøbere bruger leverandørportalen til at samarbejde med eksterne leverandører under processen til bekræftelse af indkøbsordrer. Oplysningerne i dette emne gælder kun for versioner af Dynamics AX fra februar 2016 og maj 2016.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3bb30ddffb86c7083f40863c0c336fc5f65ce8f5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248974"
---
# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Samarbejde med kreditorer ved hjælp af leverandørportalen

[!include [banner](../includes/banner.md)]

I dette emne forklares, hvordan indkøbere bruger leverandørportalen til at samarbejde med eksterne leverandører under processen til bekræftelse af indkøbsordrer. Oplysningerne i dette emne gælder kun for versioner af Dynamics AX fra februar 2016 og maj 2016.

Oplysningerne i dette emne gælder kun for versioner af Dynamics AX fra februar 2016 og maj 2016. Du kan finde flere oplysninger om den nye kreditorsamarbejdsfunktion under [Brug af leverandørsamarbejde til at arbejde med eksterne leverandører](vendor-collaboration-work-external-vendors.md).  

Kreditorportalen henvender sig til leverandører, der ikke har EDI-integration (electronic data interchange) med Microsoft Dynamics AX til udveksling af indkøbsordreoplysninger (IO). Portalen giver indkøbsagenter mulighed for at sende en IO til kreditoren og modtage et Bekræftet- eller Afvist-svar direkte i Dynamics AX.  

Processen kan konfigureres, så en bekræftelse fra kreditoren automatisk bekræfter ordren. I dette tilfælde kræves der kun lejlighedsvis opfølgning, når en ordre afvises, eller hvis kreditorbekræftelse registreres som et svar, men statussen for Indkøbsordren ikke opdateres til **Bekræftet** på grund af et problem under bekræftelsesprocessen.

## <a name="po-confirmation-and-rejection"></a>Bekræftelse og afvisning af indkøbsordre
IO'er oprettes i Dynamics AX. Når du har en IO, der har status som **Godkendt**, sender du den til leverandøren ved at generere en anmodning om bekræftelse. Hvis du vil henlede kreditorens opmærksomhed på den nye IO, kan du også bruge udskriftsstyringssystemet til at sende IO'en via e-mail. IO'en vises i kreditorportalen med indstilling, som kreditoren kan bruge til at bekræfte eller afvise den. Leverandøren kan også tilføje kommentarer for at kommunikere oplysninger, f.eks. ændringer af IO'en.  

Leverandøren kan se ordrelinjer på kreditorportalen. Disse linjer indeholder oplysninger som det eksterne produktnummer, dimensioner, prisoplysninger, mængde, leveringsdato og leveringsadresse. Leverandøren kan generere en rapport, der viser IO-oplysningerne og også den samlede pris. Gebyrer, der er relevante for kreditoren, vises, hvis leverandøren klikker på knappen **Gebyrer** i hovedet eller på linjerne. Kreditorer kan importere indkøbsordreoplysninger til deres eget system ved hjælp af funktionen **Eksportér til Excel**.  

Nedenstående tabel viser den typiske udveksling af oplysninger, afhængigt af hvordan kreditoren reagerer, når du sender dem en indkøbsordre, der skal bekræftes.

| Svartype                                                                                                  | Resultat                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kreditoren bekræfter ordren. Systemet er konfigureret til automatisk at bekræfte indkøbsordrer, når kreditoren bekræfter.    | Status for ordren opdateres til **Bekræftet**. Hvis noget forhindrer, at ordren opdateres, bliver kreditorens svar stadig registreret som **Bekræftet**, men indkøbsordrens status forbliver **Til eksternt gennemsyn**.                                                                       |
| Kreditoren bekræfter ordren. Systemet er ikke konfigureret til automatisk at bekræfte indkøbsordrer, når kreditoren bekræfter. | Kreditorens svar registreres som **Bekræftet**, men indkøbsordrens status forbliver **Til eksternt gennemsyn**.                                                                                                                                                                                      |
| Kreditoren afviser ordren.                                                                                     | Kreditorens svar registreres som **Afvist**, og indkøbsordrens status forbliver **Til eksternt gennemsyn**. Afslaget modtages sammen med årsagen og et ændringsforslag, f.eks. en alternativ leveringsdato. Du opdaterer indkøbsordren og sender derefter en ny version til bekræftelse. |

## <a name="changes-to-a-po"></a>Ændringer i en indkøbsordre
Når du skal ændre en indkøbsordre, der allerede er blevet bekræftet, kan du sende en ny indkøbsordre til kreditoren via kreditorportalen. Den nye IO har et versionssuffiks, som angiver, at det er en ændret version af en tidligere indkøbsordre. På kreditorportalen kan kreditorer spore historikken for hver ordre. Den tidligere bekræftede version af indkøbsordren forbliver på listen over bekræftede IO'er, indtil den nye indkøbsordre er blevet bekræftet.  

Når du annullerer en indkøbsordre, ændres statussen tilbage til **Godkendt**. Du skal sende IO'en tilbage til kreditoren via kreditorportalen, så kreditoren kan bekræfte eller afvise annulleringen. Når annulleringen bekræftes, vises indkøbsordren på kreditorens liste over bekræftede IO'er som **Annulleret**.

## <a name="versions-status-transitions-and-change-management"></a>Versioner, statusovergange og ændringsstyring
Når en indkøbsordre sendes til kreditoren, registreres den i systemet som en bestemt version af indkøbsordren, og statussen ændres fra **Godkendt** til **Til eksternt gennemsyn**. Hvis indkøbsordren ændres senere, oprettes der en ny version af indkøbsordren, og statussen ændres til **Godkendt** (eller **Kladde**, hvis ændringsstyring er slået til).  

I nedenstående tabel vises et eksempel på ændringerne i status og version, som en indkøbsordre kan gennemgå.

| Handling                                                   | Status og version                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Den første version af indkøbsordren oprettes i Dynamics AX. | Status er **Godkendt**.                                                                           |
| Indløbsordren sendes til kreditorportalen.                     | En version registreres på kreditorportalen, og status ændres til **Til eksternt gennemsyn**.    |
| Du kan foretage nogle ændringer, som kreditoren har anmodet om.  | Statussen ændres tilbage til **Godkendt**.                                                            |
| Du kan sende den nye version af indkøbsordren til kreditorportalen. | En ny version registreres på kreditorportalen, og status ændres til **Til eksternt gennemsyn**. |
| Kreditoren godkender den nye version af IO'en.           | Statussen ændres til **Bekræftet**.                                                                |

Hvis du vil se de versioner af indkøbsordren, der er sendt til kreditoren, og kreditorens svar, skal du klikke på **Kladder** &gt; **Anmodninger om bekræftelse** fra indkøbsordren.  

Ordrer, der er sendt til kreditoren for et svar, og som har statussen **Til eksternt gennemsyn**, vises enten på listen **Indkøbsordrer, der er sendt til kreditorportal, afventer svar** eller listen **Indkøbsordrer, der er sendt til kreditorportal, kræver handling på svar**. Når du ændrer en ordre, der er sendt til kreditoren, så status ændres tilbage til **Godkendt**, vises ordren ikke længere på disse lister. Hvis du vil se, om der tidligere har været et svar til ordren fra leverandøren, skal du klikke på **Kladder** &gt; **Anmodninger om bekræftelse**.  

Kreditorer behøver ikke at bekræfte indkøbsordren på kreditorportalen. De kan også sende en e-mail eller kommunikere deres accept af en IO via andre kanaler. Derefter kan du bekræfte ordren manuelt i Dynamics AX. I dette tilfælde modtager du en advarsel om, at ordren er blevet bekræftet, selv om der intet svar er fra kreditoren. Indkøbsordren vises derefter i oversigten over bekræftelser på kreditorportalen som en åben bekræftet ordre, som ikke har nogen svar. Desuden har kreditoren ikke længere mulighed for at bekræfte eller afvise indkøbsordren.  

**Bemærk!** Den version af indkøbsordren, der er tilgængelig for andre processer i Dynamics AX, er altid den nyeste version, selv om denne version endnu ikke er registreret.

### <a name="change-management"></a>Styring af ændringer

Hvis du har aktiveret ændringsstyring for en indkøbsordre, gennemgår indkøbsordren en godkendelsesarbejdsgang for at nå frem til statussen **Godkendt**. Denne proces er ikke synlig for kreditoren.  

Når ændringsstyring er aktiveret for en indkøbsordre, registreres versionen, når indkøbsordren er godkendt, og ikke når indkøbsordren sendes til kreditoren eller bekræftes.  

I følgende tabel vises et eksempel på ændringerne i status og version, som en indkøbsordre kan gennemgå, når ændringsstyring er slået til.


|                                                    Handling                                                     |                                                                                                                                                                                                                      Status og version                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           Den første version af indkøbsordren oprettes i Dynamics AX.                            |                                                                                                                                                                                                            Status er <strong>Kladde</strong>.                                                                                                                                                                                                             |
| Indkøbsordren sendes til godkendelsesprocessen. (Dette er en intern proces, som kreditoren ikke er involveret i). |                                                                                                                        Status ændres fra <strong>Kladde</strong> til <strong>Til gennemsyn</strong> til <strong>Godkendelse</strong>, hvis indkøbsordren ikke afvises under godkendelsesprocessen. Den godkendte indkøbsordre registreres som en version.                                                                                                                        |
|                                      Indløbsordren sendes til kreditorportalen                                      |                                                                                                                                                                      Versionen registreres på kreditorportalen, og status ændres til <strong>Til eksternt gennemsyn</strong>.                                                                                                                                                                       |
|                            Du kan foretage nogle ændringer, som kreditoren har anmodet om.                            |                                                                                                                                                                                                    Statussen ændres tilbage til <strong>Kladde</strong>.                                                                                                                                                                                                     |
|                              Indkøbsordren sendes igen til godkendelsesprocessen.                               | Status ændres fra <strong>Kladde</strong> til <strong>Til gennemsyn</strong> til <strong>Godkendelse</strong>, hvis indkøbsordren ikke afvises under godkendelsesprocessen. Systemet kan også konfigureres, så specifikke feltændringer ikke kræver fornyet godkendelse. I dette tilfælde ændres status først til <strong>Kladde</strong> og derefter opdateres automatisk til <strong>Godkendt</strong>. Den godkendte indkøbsordre registreres som en ny version. |
|                           Du kan sende den nye version af indkøbsordren til kreditorportalen.                            |                                                                                                                                                                    Den nye version registreres på kreditorportalen, og status ændres til <strong>Til eksternt gennemsyn</strong>.                                                                                                                                                                     |
|                                Kreditoren godkender den nye version af IO'en.                                 |                                                                                                                                                     Statussen ændres til <strong>Bekræftet</strong>. Det sker enten automatisk, eller når du modtager svar fra kreditoren og derefter bekræfter indkøbsordren.                                                                                                                                                     |

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Konfiguration af sikkerhed for brugere af kreditorsamarbejde](configure-security-vendor-portal-users.md)

[Arbejdsområde for kreditorsamarbejdsfakturering](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)



