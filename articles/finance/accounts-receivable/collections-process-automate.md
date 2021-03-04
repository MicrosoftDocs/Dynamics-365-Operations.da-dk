---
title: Automatiseret rykkerproces
description: I dette emne beskrives processen for opsætning af strategier for rykkerprocessen, der automatisk identificerer debitorfakturaer, der kræver en mailpåmindelse, en rykkeraktivitet (f.eks. et telefonopkald) eller et rykkerbrev, der sendes til kunden.
author: panolte
manager: AnnBe
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: db59bad2ed3caf38f22bd4d6059e57747d1d983f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441430"
---
# <a name="collections-process-automation"></a>Automatiseret rykkerproces

[!include [banner](../includes/banner.md)]

I dette emne beskrives processen for opsætning af strategier for rykkerprocessen, der automatisk identificerer debitorfakturaer, der kræver en mailpåmindelse, en rykkeraktivitet (f.eks. et telefonopkald) eller et rykkerbrev, der sendes til kunden. 

Organisationer bruger en betydelig del af tiden på at søge efter aldersfordelte saldorapporter, debitorkonti og åbne fakturaer for at afgøre, hvilke kunder der skal kontaktes om en åben faktura eller kontosaldo. Denne eftersøgning stjæler tid fra en inkassators tidsforbrug på kommunikation med kunderne for at opkræve forfaldne saldi eller løse fakturatvister. Med en automatiseret rykkerproces kan du oprette en strategibaseret tilgang til din rykkerproces. Dette hjælper dig med at anvende rykkeraktiviteter på en ensartet måde ved at bruge tilpassede mailpåmindelser eller en programproces til at udsende rykkere. 

## <a name="collections-process-setup"></a>Opsætning af rykkerproces
Du kan bruge siden **Opsætning af rykkerproces** (**Kredit og rykkere > Opsætning > Opsætning af rykkerproces**) til at oprette en automatiseret rykkerproces, der planlægger aktiviteter, sender mailmeddelelser og opretter og bogfører debitorrykkerbreve. Procestrinnene er baseret på den indledende eller ældste åbne faktura. Hvert trin bruger denne faktura til at bestemme, hvilken kommunikation eller aktivitet der skal ske med en bestemt kunde.  

### <a name="process-hierarchy"></a>Proceshierarki
Hver kundepulje kan kun tildeles ét proceshierarki. Hierarkirangen af dette trin identificerer, hvilken proces der har forrang, hvis en kunde er inkluderet i mere end én pulje, hvor der er tildelt et proceshierarki. Pulje-id'et bestemmer, hvilke kunder der vil blive tildelt processen. 

Stilledage bruges til at sikre, at en kunde ikke bliver kontaktet for ofte af den automatiserede proces.  Hvis stilledage f.eks. er angivet til to, vil en kunde ikke blive kontaktet af den automatiserede proces i mindst to dage, selvom den oprindelige indledende faktura er betalt fuldt ud. 

Hvis du vil udelukke kunder fra procesautomatiseringen, hvis kontosaldoen eller fakturasaldoen er mindre end en defineret værdi, skal du angive feltet **Udeluk fra proces** til **Ja** og angive beløbsværdien.

## <a name="process-details"></a>Procesdetaljer
**Beskrivelse** bruges til at identificere formålet med eller navnet på trinnet i hierarkiet.

**Handlingstypen** definerer, om trinnet vil oprette en aktivitet, sende en mail eller oprette en rykker.

**Forretningsdokument** definerer den skabelon, der bruges til at oprette handlingstypen.  Det kan være en aktivitetsskabelon, en mailskabelon eller en rykker pr. kunde. 

Handlingstyperne kan oprettes enten før eller efter datoen for fakturaens forfaldsdato, baseret på den indstilling, der vises i kolonnen **Dage i relation til fakturaens forfaldsdato**.

Når du vælger en mailhandlingstype, bruges modtageren til at definere, om det er en kunde-, salgsgruppe- eller inkassatorkontakt. Værdien i feltet **Kontakt til forretningsformål** bestemmer derefter, hvilken kontakt fra kundens konto der skal modtage kommunikationen.

## <a name="business-document-details"></a>Detaljer om forretningsdokument
Oplysningerne om forretningsdokumenter varierer, afhængigt af den handlingstype, der er valgt i procesoplysningerne.  Når handlingstypen er en aktivitet, vises oplysningerne om aktivitetsskabelonen.  Disse oplysninger omfatter navnet på aktivitetsskabelonen, den aktivitetstype, der oprettes, formålet med aktiviteten, det antal dage, der er planlagt til at fuldføre aktiviteten, og detaljer om aktiviteten.  Denne aktivitet vil derefter oprette en kæde til den indledende faktura, der fortæller modtageren, hvilken handling der skal bruges til at fuldføre aktiviteten.

Hvis handlingstypen er en mail i procesoplysningerne, vil dette afsnit indeholde to oversigtspaneler.  Det første bruges til at definere skabelon-id, mailbeskrivelse, standardsprog, det brugernavn, der vil blive tildelt de mails, som automatisk udsendes, og mailadressen på den tilknyttede afsenders mailadresse. Det andet vil tillade, at brødteksten i mailen oprettes, efter at værdierne i felterne **Sprog** og **Emne** gemmes ved at vælge **Rediger**.  Derved åbnes et vindue, hvor det er muligt at overføre HTML-indhold. Du kan også skrive den meddelelse, der skal oprettes, manuelt i nederste venstre felt i vinduet.  

> [!Note]
> En Outlook-mail kan gemmes med den ønskede meddelelsestekst i HTML-format. Denne kan derefter overføres til implementering af skabelonen. <br> <br> Hvis handlingstypen rykker er valgt, vil der ikke være et detaljeafsnit til forretningsdokument i opsætningsformularen.


## <a name="fasttab-reference"></a>Oversigtspanelet Reference
Følgende tabeller viser de sider og felter, som de angivne oversigtspaneler kan åbnes fra, sammen med en beskrivelse af oplysningerne under den pågældende fane. 

### <a name="process-hierarchy"></a>Proceshierarki

|     Side                                                  |     Felt                         |     Beskrivelse                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Opsætning af rykkerproces <br> Procesautomatisering       |                                   |     Opret og administrer rykkerprocesser baseret på tildelinger af kundepulje.                                                                                                                             |
|     Opsætning af rykkerproces <br> Procesautomatisering       |     Hierarki                     |     Definerer prioriteten af procesautomatisering, der skal tildeles en kunde, hvis kunden tilhører flere puljer.                                                                                                   |
|     Opsætning af rykkerproces <br> Procesautomatisering       |     Pulje-id                       |     Forespørgsler, der definerer en gruppe af kundeposter.                                                                                                                                                        |
|     Opsætning af rykkerproces <br> Procesautomatisering       |     Stilledage                    |     Begræns, hvor ofte et procestrin kan fuldføres. Hvis der f.eks. er angivet to stilledage, vil næste procestrin ikke forekomme i mindst to dage, hvis den indledende faktura ændres.     |
|     Opsætning af rykkerproces <br> Procesautomatisering       |     Udeluk fra proces        |     Hvis du enten vælger **Kundens aldersfordelte saldo er mindre end** eller **Fakturabeløb er mindre end**, udelukkes en kunde fra procesautomatiseringen, hvis værdikriterierne ikke opfyldes.                                   |

### <a name="process-details"></a>Procesdetaljer
|     Side                                                  |     Felt                                         |      Beskrivelse                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Opsætning af rykkerproces <br> Procesautomatisering       |                                                   |     Definer de trin, der udføres, på baggrund af den indledende faktura.                                                                                                |
|                                                           |     Beskrivelse                                   |     Et fritekstfelt, der bruges til at angive et navn og/eller en beskrivelse af trinnet.                                                                           |
|                                                           |     Handlingstype                                   |     Aktivitet, mail eller rykker, der oprettes af procestrinnet.                                                                     |
|                                                           |     Forretningsdokument                           |     Definerer den aktivitet eller mailskabelon, der bruges under procestrinnet.                                                                        |
|                                                           |     Når                                          |     Angiver, om procestrinnet skal foregå før eller efter den indledende fakturas forfaldsdato, sammen med feltet **Dage i relation til fakturaens forfaldsdato**.        |
|                                                           |     Dage i relation til fakturaens forfaldsdato        |     Sammen med feltet **Hvornår** identificerer det timingen af procestrinnet.                                                                          |
|                                                           |     Modtager                                     |     Angiver, om der skal sendes en mail til en kontakt hos en kunde, salgsgruppe eller inkassator.                                                   |
|                                                           |     Kontakt til forretningsformål                    |     Bestemmer, hvilken modtagers mailadresse der bruges i mailkommunikation.                                                                                 |

### <a name="business-process-activity-template-details"></a>Oplysninger om forretningsprocessens aktivitetsskabelon 
|     Side                                                  |     Felt                     |      Beskrivelse                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Opsætning af rykkerproces <br> Procesautomatisering       |                               |     Den del af opsætningsprocessen, der identificerer detaljerne i aktivitetsskabelonen.                                                                      |
|     Opsætning af rykkerproces <br> Procesautomatisering       |     Aktivitetsskabelon       |     Identificerer typen, formålet, antallet af dage til fuldførelse og indeholder oplysninger om den aktivitet, der oprettes i løbet af et aktivitetsprocestrin.       |

### <a name="business-document-email-template-details"></a>Oplysninger om e-mailskabelon til forretningsdokument 
|     Side                                                  |     Felt     |      Beskrivelse                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Opsætning af rykkerproces <br> Procesautomatisering       |               |     Identificerer mailbeskrivelsen, standardsproget, afsendernavnet og mailadressen, der oprettes under et mailprocestrin.        |


### <a name="collections-history"></a>Rykkerhistorik 
|     Side                              |     Felt     |      Beskrivelse                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Opsætning af rykkerproces       |               |     Se den seneste historik for det valgte proceshierarki.     |

### <a name="collection-process-assignment"></a>Tildeling af rykkerproces
|     Side                              |     Felt     |      Beskrivelse                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Opsætning af rykkerproces       |               |     Få vist kunder, der er tildelt en rykkerproces.  
|     Manuel tildeling               |               |     Få vist kunder, der er blevet tildelt en proces manuelt, eller vælg kunder, der skal tildeles en proces. |
|     Prøveversion af procestildeling      |               |     Få vist de kunder, der skal tildeles en strategi, når den køres.   |
|     Prøveversion af kundetildeling     |               |     Få vist den strategi, som en bestemt kunde er tildelt.    |
 
### <a name="parameters"></a>Parametre
|     Side                                                                  |     Felt                                             |      Beskrivelse                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Debitorparametre > Automatiseret rykkerproces     |     Procentdel af kunder pr. batchopgave          |     Indstilling til at bestemme antallet af batchopgaver pr. automatiseringsproces.                                          |
|     Debitorparametre > Automatiseret rykkerproces     |     Bogfør rykkerbreve automatisk           |     Rykkerhandlingstyperne vil bogføre brevet under automatiseringen.                                      |
|     Debitorparametre > Automatiseret rykkerproces     |     Oprette aktiviteter automatisk                |     Opret og luk aktiviteter for handlingstyper uden aktivitet for at få vist alle de automatiserede trin, der udføres på en konto.        |
|     Debitorparametre > Automatiseret rykkerproces     |     Opbevaringsdage for automatiseret rykkerproces     |     Definerer, hvor mange dage rykkerhistorikken gemmes.                                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]