---
title: Automatisering af opkrævningsproces
description: Denne artikel beskriver processen for opsætning af strategier for rykkerprocessen, der automatisk identificerer debitorfakturaer, der kræver en mailpåmindelse, en rykkeraktivitet eller et rykkerbrev, der sendes til kunden.
author: JodiChristiansen
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9ec749db197b4d04ee2e99ac7a16f4f2120c6707
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946141"
---
# <a name="collections-process-automation"></a>Automatisering af opkrævningsproces

[!include [banner](../includes/banner.md)]

Denne artikel beskriver processen for opsætning af strategier for rykkerprocessen, der automatisk identificerer debitorfakturaer, der kræver en mailpåmindelse, en rykkeraktivitet (f.eks. et telefonopkald) eller et rykkerbrev, der sendes til kunden. 

Organisationer bruger ofte en betydelig del af tiden på at søge efter aldersfordelte saldorapporter, debitorkonti og åbne fakturaer for at lære, hvilke kunder der bør kontaktes om en åben faktura eller kontosaldo. Denne eftersøgning stjæler tid fra en inkassators tidsforbrug på kommunikation med kunderne for at opkræve forfaldne saldi eller løse fakturatvister. Med en automatiseret rykkerproces kan du oprette en strategibaseret tilgang til din rykkerproces. Dette hjælper dig med at anvende rykkeraktiviteter på en ensartet måde ved at bruge tilpassede mailpåmindelser eller en programproces til at udsende rykkere. 

## <a name="collections-process-setup"></a>Opsætning af rykkerproces
Du kan bruge siden **Opsætning af rykkerproces** (**Kredit og rykkere > Opsætning > Opsætning af rykkerproces**) til at oprette en automatiseret rykkerproces, der planlægger aktiviteter, sender mailmeddelelser og opretter og bogfører debitorrykkerbreve. Procestrinnene er baseret på den indledende eller ældste åbne faktura. Hvert trin bruger denne faktura til at bestemme, hvilken kommunikation eller aktivitet der skal ske med en bestemt kunde.  

Rykkerteam sender typisk en tidlig besked vedrørende hver udestående faktura, sådan at en kunde får besked, når fakturaen er forfalden. Valget **Varsel om rykker** kan angives, så der kan reageres på ét trin i hvert proceshierarki for hver faktura, efterhånden som tidspunktet for fakturaen når dette trin.

### <a name="process-hierarchy"></a>Proceshierarki
Hver kundepulje kan kun tildeles ét proceshierarki. Hierarkirangen af dette trin identificerer, hvilken proces der har forrang, hvis en kunde er inkluderet i mere end én pulje, hvor der er tildelt et proceshierarki. Pulje-id'et bestemmer, hvilke kunder der vil blive tildelt processen. Hvert konfigurerede hierarki kan kun tildeles til én procesautomatisering.

Stilledage bruges til at sikre, at en kunde ikke bliver kontaktet for ofte af den automatiserede proces. Hvis stilledage f.eks. er angivet til to, vil en kunde ikke blive kontaktet af den automatiserede proces i mindst to dage, selvom den oprindelige indledende faktura er betalt fuldt ud. 

Du kan udelukke kunder fra procesautomatisering, hvis kundens aldersfordelte saldo eller fakturabeløb er mindre end en defineret værdi, ved at vælge **Kundens aldersfordelte saldo er mindre end** eller **Fakturabeløb er mindre end** i feltet **Udeluk fra proces** og angive beløbsværdien.

Markér **Brug forudsigelse** for at oprette rykkeraktiviteter ved hjælp af kundebetalingsforudsigelser. De aktiviteter, der oprettes, vil bruge aktivitetsskabelonen fra **Betalingsforudsigelser** på siden **Debitorparametre**, fanen **Automatisering af rykkerproces**. 

### <a name="process-details"></a>Procesdetaljer
Klik på **Ny** for at føje en ny procesdetalje til hierarkiet. **Beskrivelse** bruges til at identificere formålet med eller navnet på trinnet i hierarkiet. Vælg **Handlingstypen** for at definere trinnet, der skal oprette en aktivitet, sende en mail eller oprette en rykker. 

- **Forretningsdokument** definerer den skabelon, der bruges til at oprette handlingstypen. Dette dokument kan være en aktivitetsskabelon, en mailskabelon eller en rykker til hver kunde. I rykkerprocessens automatisering oprettes kun rykkere pr. kunde, uanset hvordan andre rykkerparametre er angivet.
- **Når** definerer det procestrin, der skal finde sted før eller efter forfaldsdatoen for den indledende (ældste) faktura, og det bruges sammen med det antal, der vises i kolonnen **Dage i forhold til fakturaens forfaldsdato**. 
- Markér indstillingen **Varsel om rykker** for at oprette en handling for hver faktura i ét trin i et proceshierarki. Varsel om rykker er typisk en tidlig besked vedrørende udestående fakturaer, så en kunde får besked, når fakturaen snart bliver forfalden. Varsel om rykker kan kun markeres for én aktivitet pr. hierarki. Når du vælger en mailhandlingstype, bruges modtageren til at definere, om mailmeddelelsen skal sendes til en kunde, salgsgruppe eller inkassatorkontakt. 
- Værdien i feltet **Kontakt til forretningsformål** bestemmer derefter, hvilken kontakt fra kundens konto der skal modtage kommunikationen.

### <a name="business-document-details"></a>Detaljer om forretningsdokument
Oplysningerne om forretningsdokumenter varierer, afhængigt af den handlingstype, der er valgt i procesoplysningerne. Når handlingstypen er en aktivitet, vises oplysningerne om aktivitetsskabelonen. Disse oplysninger omfatter navnet på aktivitetsskabelonen, den aktivitetstype, der oprettes, formålet med aktiviteten, det antal dage, der er planlagt til at fuldføre aktiviteten, og detaljer om aktiviteten. Denne aktivitet vil derefter oprette en kæde til den indledende faktura, der fortæller modtageren, hvilken handling der skal bruges til at fuldføre aktiviteten.

Hvis handlingstypen er en mail i procesoplysningerne, vil dette afsnit indeholde to oversigtspaneler. Det første bruges til at definere skabelon-id, mailbeskrivelse, standardsprog, det brugernavn, der vil blive tildelt de mails, som automatisk udsendes, og mailadressen på den tilknyttede afsenders mailadresse. Det andet vil tillade, at brødteksten i mailen oprettes, efter at værdierne i felterne **Sprog** og **Emne** gemmes ved at vælge **Rediger**. Derved åbnes et vindue, hvor det er muligt at overføre HTML-indhold. 

> [!Note]
> Du kan gemme en Outlook-mail, der indeholder brødteksten til kommunikationen i HTML-format. Du kan derefter uploade meddelelsesindholdet for at implementere skabelonen. <br> <br> Hvis handlingstypen rykker er valgt, vil der ikke være et detaljeafsnit til forretningsdokument på opsætningssiden.

Brug knappen **Rykkerproceshistorik** til at få vist den seneste historik for det valgte proceshierarki. 

Klik på handlingen **Tildeling af rykkerproces** for at få vist kunder, der er tilknyttet en rykkerproces. Du kan bruge **Prøveversion af kundetildeling** til at få vist det hierarki, som en bestemt kunde er tildelt. Du kan bruge **Prøveversion af procestildeling** til at få vist de kunder, der tildeles til et hierarki, når det køres. Klik på **Manuel tildeling** for at se kunder, der er blevet tildelt en proces manuelt, eller vælg kunder, der skal tildeles en proces.

Klik på handlingen **Processimulering** for at se de handlinger, der vil blive oprettet, hvis den valgte proces-automatisering køres på dette tidspunkt. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
