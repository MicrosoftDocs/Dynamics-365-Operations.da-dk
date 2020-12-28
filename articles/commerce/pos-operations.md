---
title: POS-handlinger, online og offline
description: Dette emne indeholder oplysninger om POS-handlinger i Dynamics 365 Commerce. Det angiver, hvor i programmet handlingerne kan startes, og om de er tilgængelige i offlinetilstand.
author: jblucher
manager: AnnBe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7dc9f85bf90e6ddf9badf656eb136e28a71b036f
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594107"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>POS-handlinger, online og offline

[!include [banner](includes/banner.md)]

De fleste handlinger, som brugeren udfører på POS, betragtes som handlinger. Handlinger konfigureres og administreres i Dynamics 365 Commerce-administration. Mange handlinger kan føjes til knapper i POS-knapmatrixen. Brugere kan derefter vælge knapperne for at aktivere handlingerne og udføre deres funktion. Andre handlinger indgår i POS-hovedprogrammet og kaldes enten fra på knapper på skærmen eller som en del af andre arbejdsgange eller processer.

Følgende tabel indeholder oplysninger om de handlinger, der er tilgængelige i Modern POS og Cloud POS. Tabellen angiver også, hvor i programmet handlingerne kan startes, og om de er tilgængelige, når POS er i offlinetilstand.

Nogle handlinger er i øjeblikket ikke tilgængelige i Modern POS eller Cloud POS. Nogle af disse handlinger er specifikke for landestandarden og kræver yderligere udvidelser og konfiguration. Andre er funktioner fra Microsoft Dynamics AX 2012, der ikke understøttes i øjeblikket.

Følgende kolonner angiver, hvor handlingerne kan aktiveres:

- **Knapmatrix** – Handlinger kan tildeles til knapper i POS-knapmatrixer, som er en del af et POS-skærmlayout.
- **Transaktionsskærm** – Handlingen kan startes fra POS-knapmatrixer, der er konfigureret på POS-transaktionsskærmen.
- **Velkomstskærm** – Handlingen kan startes fra POS-knapmatrixer, der er konfigureret på POS-velkomstskærmen.

> [!NOTE]
> De handlinger, der er angivet nedenfor, gælder for den nyeste version af Commerce. Nogle handlinger kan være ændret eller er måske ikke tilgængelige i tidligere versioner.

| Id | Handling | Betegnelse | Knapmatrix | Transaktionsskærm | Velkomstskærm | Tilgængelig offline | Specifik for landestandard |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Aktivér enhed | Aktivér den aktuelle enhed ved at lade en godkendt bruger til at angive forbindelsesoplysninger og tildele en enhed og registrere id. | Nej | Nej | Nej | Nej | Nej |
| 134 | Tilføj tilhørsforhold | Føj en forudvalgt tilknytning til en transaktion. Vælg tilknytningen på siden **Egenskaber for knap**. | Ja | Ja | Nej | Ja | Nej |
| 135 | Tilføj tilhørsforhold fra liste | Føj en tilknytning til en transaktion ved at vælge den på en liste. | Ja | Ja | Ja | Ja | Nej |
| 137 | Føje tilknytning til en kunde | Tilføj en tilknytning til en kunde på siden **Kundeoplysninger**. | Nej | Nej | Nej | Ja | Nej |
| 138 | Fjern tilknytning fra kunde | Fjern en tilknytning på siden **Kundeoplysninger**. | Nej | Nej | Nej | Ja | Nej |
| 643 | Tilføj kuponkode | Tilføj en kupon ved at indtaste dens kode på POS. | Ja | Ja | Nr. | Ja | Nr. |
| 141 | Tilføj gebyrer i hoved | Føj et tillæg til ordrehovedet. | Ja | Ja | Nr. | Nr.| Nr. |
| 141 | Tilføj linjegebyrer | Føj et tillæg til en valgt salgslinje. | Ja | Ja | Nr. | Nr.| Nr. |
| 117 | Tilføj fordelskundekort | Bed brugeren om at indtaste et fordelskundekortnummer, der skal føjes til den aktuelle transaktion. | Ja | Ja | Nej | Ja | Nej |
| 136 | Tilføj serienummer | Med denne handling kan brugeren angive et serienummer for det aktuelt valgte produkt. | Ja | Ja | Nej | Ja | Nej |
| 1214 | Tilføj leveringsadresse | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 519 | Føj til gavekort | Tilføj penge til det angivne gavekort. | Ja | Ja | Nej | Nej | Nej |
| 6000 | Tillad, at springe regnskabsregistreringen over | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ja |
| 1212 | Indsættelse i banken | Registrér det pengebeløb, der er sendt til banken, og andre oplysninger, f.eks. bankposenummeret. | Ja | Ja | Ja | Ja | Nej |
| 923 | Bekræftelse af banktotaler | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ja |
| 915 | Tom handling | Denne handling repræsenterer en knap, der kan tilpasses, og som kan ændres via programmering af en softwareudvikler for en hvilken som helst særhandling, virksomheden har brug for. | Ja | Ja | Ja | Ja | Nej |
| 1053 | Luk skifte uden kontrol | Indstil det aktuelle skift til lukket uden kontrol, og log brugeren af. En skift lukket uden kontrol er lukket for yderligere transaktioner, men er stadig åben for handlinger med kasseskuffe, f.eks. fjernelse af betalingsmiddel og kasseoptælling. | Ja | Ja | Ja | Nej | Nej |
| 310 | Beregn total | Når kontantrabatten forsinkes, vil denne handling starte beregningen for den aktuelle transaktion. | Ja | Ja | Nej | Ja | Nej |
| 642 | Udfør alle produkter | Angiv leveringsmåden for alle linjer til **Udfør**. | Ja | Ja | Nej | Ja\* | Nej |
| 641 | Udfør alle valgte produkter | Angiv leveringsmåden for de valgte linjer til **Udfør**. | Ja | Ja | Nr. | Ja\* | Nr. |
| 647 | Ændring af leveringsmetode | Skift leveringsmåde for forudkonfigurerede salgslinjer til forsendelse. | Ja | Ja | Nr. | Nr.| Nr. |
| 1215 | Skift adgangskode | Med denne handling kan POS-brugeren ændre sin adgangskode. | Ja | Ja | Ja | Nej | Nej |
| 123 | Skift måleenhed | Ændre måleenheden for det valgte linjeelement. | Ja | Ja | Nej | Ja | Nej |
| 639 | Ryd standardsælgeren for transaktionen | Fjern provisionssalgsgruppen (sælger) fra transaktionen. | Ja | Ja | Nej | Ja | Nej |
| 106 | Ryd antal | Nulstil antallet på den aktuelt valgte linje for **1**. | Ja | Ja | Nej | Ja | Nej |
| 640 | Ryd sælger på linjen | Fjern provisionssalgsgruppen (sælger) fra den aktuelt valgte linje. | Ja | Ja | Nej | Ja | Nej |
| 121 | Ryd sælger | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 1055 | Luk skift | Luk det aktuelle skifte, udskriv en Z-rapport, og log brugeren af systemet. | Ja | Ja | Ja | Nr. | Nr. |
| 139 | Afslut transaktion | Beder brugeren vælge betalingsmetode | Ja | Ja | Nr. | Ja | Nr. |
| 620 | Opret kundeordre | Konvertér POS-transaktionen til en kundeordre. | Ja | Ja | Nr. | Ja\* | Nr. |
| 925 | Kopiér bankchecken | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ja |
| 620 | Opret kundeordre | Konvertér POS-transaktionen til en kundeordre. | Ja | Ja | Nej | Ja\* | Nej |
| 621 | Opret tilbud | Konvertér POS-transaktionen til et salgstilbud. | Ja | Ja | Nej | Ja\* | Nej |
| 636 | Opret detailtransaktion | Med denne handling kan brugeren oprette en almindelig salgstransaktion, når POS-standardindstillingen er at oprette kundeordrer. | Ja | Ja | Nej | Ja | Nej |
| 600 | Kunde | Tilføj den angivne kunde til transaktionen. | Nej | Nej | Nej | Ja | Nej |
| 1100 | Indbetaling på kundekonto | Foretag en betaling til en kundekonto. | Ja | Ja | Ja | Ja | Ja |
| 612 | Tilføj kunde | Med denne handling kan brugeren oprette en ny kundepost. | Ja | Ja | Ja | Ja† | Nej |
| 603 | Ryd kunde | Fjern kunden fra den aktuelle transaktion. | Ja | Ja | Nej | Ja | Nej |
| 602 | Kundesøgning | Med denne handling kan brugeren søge efter en debitorpost ved at gå til siden med kundesøgning i POS. | Ja | Ja | Ja | Ja | Nej |
| 609 | Debitorposter | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 917 | Forbindelsesstatus for database | Med denne handling kan brugeren få vist de aktuelle forbindelsesindstillinger og skifte mellem online- og offlinetilstand. | Ja | Ja | Ja | Ja | Nej |
| 1200 | Angiv startbeløb | Angiv det beløb, der er i pengeskuffen ved dagens begyndelse, eller når skiftet starter. | Ja | Ja | Ja | Ja | Nej |
| 132 | Tilsidesæt depositum | Tilsidesætte standarddepositum for kundeordrer. | Ja | Ja | Nej | Ja\* | Nej |
| 913 | Deaktiver designtilstand | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 912 | Aktivér designtilstand | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 1217 | Demonter pakker | Opdel en pakke i dens enkelte produktdele. | Ja | Ja | Ja | Ja | Nej |
| 624 | Vis refusionsbeløb | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ja |
| 513 | Vis total | Vis saldoen for transaktionen på kundedisplayet. | Ja | Ja | Ja | Ja | Nej |
| 623 | Rediger kunde | Rediger oplysningerne for den aktuelle kunde. | Ja | Ja | Nej | Nej | Nej |
| 614 | Rediger kundeordre | Tilbagekald den valgte ordre, så den kan redigeres i POS. | Nej | Nej | Nej | Nej | Nej |
| 615 | Rediger tilbud | Tilbagekald det valgte tilbud, så det kan redigeres i POS. | Nej | Nej | Nej | Nej | Nej |
| 518 | Udgiftskonti | Registrer penge, der er fjernet fra pengeskuffen til lejlighedsvise udgifter. | Ja | Ja | Ja | Ja | Nej |
| 919 | Udvidet logon | Tildele eller fjerne tilladelse til at logge på ved at scanne en stregkode eller føre et kort gennem en kortlæser. | Ja | Ja | Ja | Ja | Nr. |
| 1201 | Kassebeholdning | Med denne handling kan brugeren føje flere penge til den aktuelle kasseskuffe eller det aktuelle skift. | Ja | Ja | Ja | Ja | Nej |
| 1218 | Gennemtving oplåsning af ekstern enhed | Denne handling bruges internt af systemet til at låse op for eksterne POS-enheder. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 520 | Gavekortsaldo | Vis saldoen for et gavekort. | Ja | Ja | Nej | Nej | Nej |
| 708 | Deaktiver enhed | Deaktiver den aktuelle enhed, så den ikke kan bruges som et POS kasseapparat. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 804 | indgående handlinger | Få adgang til funktionerne i styring af indgående lagerbeholdning. | Ja | Nr. | Ja | Nr.| Nr. |
| 517 | Indtægtskonti | Registrer penge, der lægges i pengeskuffen af andre årsager end salg. | Ja | Ja | Ja | Ja | Nej |
| 801 | Lagersøgning | Få vist antal for tilgængelige, i bestilling og disponibel til tilsagn (DTT) for det aktuelle lager og andre tilgængelige lokationer. | Ja | Ja | Ja | Nej | Nej |
| 122 | Fakturakommentar | Med denne handling kan brugeren angive en kommentar til den aktuelle transaktion. | Ja | Ja | Nej | Ja | Nej |
| 511 | Udsted kreditnota | Udsted en kreditnota for at give et bilag i stedet for en refusion. | Ja | Ja | Nej | Nej | Nej |
| 512 | Udsted gavekort | Udsted et nyt gavekort for det angivne beløb. | Ja | Ja | Nej | Nej | Nej |
| 625 | Udsted fordelskundekort | Udsted et fordelskundekort til en kunde, så kunden kan deltage i butikkens kundefordelsprogram. | Ja | Ja | Ja | Nej | Nej |
| 300 | Linjerabatbeløb | Angiv et rabatbeløb for en linjevare i transaktionen. Denne operation bruges kun til varer med rabat og kun inden for specifikke rabatgrænser. | Ja | Ja | Nej | Ja | Nej |
| 301 | Linjerabatprocent | Angiv en rabatprocent for en linjevare i transaktionen. Denne operation bruges kun til varer med rabat og kun inden for specifikke rabatgrænser. | Ja | Ja | Nej | Ja | Nej |
| 703 | Lås kasseapparat | Lås det aktuelle kasseapparat, så det ikke kan bruges, men log ikke den aktuelle bruger af. | Nej | Nej | Nej | Ja | Nej |
| 701 | Log af | Log den aktuelle bruger af kasseapparatet. | Ja | Ja | Ja | Ja | Nej |
| 521 | Saldo for fordelskundepoint | Få vist saldoen for point for det angivne fordelskundekort. | Ja | Ja | Nr. | Nr. | Nr. |
| 142 | Administrer gebyrer | Få vist og administrer tillæg, der er anvendt på transaktioner. | Ja | Ja | Nr. | Nr.| Nr. |
| 918 | Administrer skift | Få vist en oversigt over aktive eller afbrudte skift og skift, der er lukket uden kontrol. | Ja | Ja | Ja | Nej | Nej |
| 914 | Minimere POS-vinduet | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 1000 | Åbn kasseskuffe | Udfør en handling af typen "intet salg", og åbn den aktuelt valgte pengeskuffen. | Ja | Ja | Ja | Ja | Nej |
| 928 | Ordreopfyldelse | Denne handling tillader brugerne at plukke, pakke, afsende eller tilbagekalde ordrer for afhentning i butik. | Ja | Ja | Ja | Nr. | Nr. |
| 805 | Udgående handlinger | Få adgang til funktioner til styring af forsendelser af udgående flytteordrer. | Ja | Nr. | Ja | Nr.| Nr. |
| 129 | Tilsidesæt linjeproduktmoms | Tilsidesæt momsen på det valgte linjeelement, og brug en anden angivet moms. | Ja | Ja | Nej | Ja | Nej |
| 130 | Tilsidesæt linjeproduktmoms fra liste | Tilsidesæt momsen på det valgte linjeelement, og brug den moms, som brugeren vælger på en liste. | Ja | Ja | Nej | Ja | Nej |
| 127 | Tilsidesæt transaktionsmoms | Tilsidesæt momsen på transaktionen, og brug en anden angivet moms. | Ja | Ja | Nej | Ja | Nej |
| 128 | Tilsidesæt transaktionsmoms fra liste | Tilsidesæt momsen på transaktionen, og brug den moms, som brugeren vælger på en liste. | Ja | Ja | Nej | Ja | Nej |
| 131 | Følgeseddel | Opret en følgeseddel til den valgte ordre. | Nej | Nej | Nej | Nej | Nej |
| 710 | Udfør parring af hardwarestation | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 201 | Kortbetaling | Accepterer et kort, f.eks. et kreditkort eller debetkort, som betaling. | Ja | Ja | Nej | Ja | Nej |
| 200 | Kontantbetaling | Acceptér kontant som betaling. | Ja | Ja | Nej | Ja | Nej |
| 206 | Hurtig kontantbetaling | Fuldfør transaktionen med et enkelt klik, og acceptér det beløb, der skal betales kontant (nøjagtige penge). | Ja | Ja | Nej | Ja | Nej |
| 204 | Checkbetaling | Acceptér en check som betaling. | Ja | Ja | Nej | Ja | Nej |
| 213 | Kreditnotabetaling | Acceptér en kreditnota (bilag), som butikken udstedte. | Ja | Ja | Nej | Nej | Nej |
| 203 | Valutabetaling | Acceptér betaling i forskellige valutaer. | Ja | Ja | Nej | Ja | Nej |
| 202 | Kundekontobetaling | Debiter transaktionen på kundens konto. Denne betalingsmetode er ikke gyldig for kundeordreindbetalinger. | Ja | Ja | Nej | Nej | Nej |
| 214 | Gavekortbetaling | Accepter et gavekort, der er udstedt af butikken. | Ja | Ja | Nej | Nej | Nej |
| 207 | Betal med fordelskundekort | Accepter et fordelskundekort til betaling, og indløs point for kvalificerede produkter. | Ja | Ja | Nej | Nej | Nej |
| 634 | Betalingshistorik | Få vist kundens betalingshistorik for den aktuelle kundeordre. | Ja | Ja | Nej | Nej | Nej |
| 803 | Pluk og tilgang | Åbn siden **Pluk og tilgang** side, hvor du kan vælge de ordrer, der skal plukkes eller modtages i butikken. | Ja | Ja | Ja | Nej | Nej |
| 632 | Afhent alle produkter | Angiv leveringsmetoden til **Afhentning i butik** for alle linjer. | Ja | Ja | Nej | Ja\* | Nej |
| 631 | Afhent valgte produkter | Angiv leveringsmetoden til **Afhentning i butik** for de valgte linjer. | Ja | Ja | Nej | Ja\* | Nej |
| 400 | Pop op-menu | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 101 | Pristjek | Med denne handling kan brugeren finde prisen for et bestemt produkt. | Ja | Ja | Ja | Ja | Nej |
| 104 | Prisændring | Tilsidesæt prisen på et produkt, hvis produktet er konfigureret, så pristilsidesættelser er tilladt. | Ja | Ja | Nej | Ja | Nej |
| 1058 | Udskriv regnskab X | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ja |
| 1059 | Udskriv regnskab Z | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ja |
| 927 | Udskriv vareetiket | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 926 | Udskriv hyldeetiket | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 1056 | Udskriv X | Udskriv en X-rapport for det aktuelle skift. | Ja | Ja | Ja | Nej | Nej |
| 103 | Produktkommentar | Tilføj en kommentar i det valgte linjeelement i transaktionen. | Ja | Ja | Nej | Ja | Nej |
| 100 | Produktsalg | Føj et angivet produkt til transaktionen. | Ja | Ja | Ja | Ja | Nej |
| 108 | Produktsøgning | Med denne handling kan brugeren søge efter et produkt ved at gå til siden med produktsøgning i POS. | Ja | Ja | Ja | Ja | Nej |
| 633 | Tilbudsudløbsdato | Med denne handling kan brugeren få vist eller ændre udløbsdatoen for et salgstilbud. | Ja | Ja | Nej | Ja\* | Nej |
| 627 | Omberegn | Omberegn alle kundeordrelinjer og moms, der er baseret på den aktuelle konfiguration. | Ja | Ja | Nr. | Ja\* | Nr. |
| 143 | Genberegn gebyrer | Genberegn de automatiske tillæg, der er anvendt på ordren. | Ja | Ja | Nr. | Nr.| Nr. |
| 515 | Tilbagekald ordre | Med denne handling kan brugeren søge efter og tilbagekalde kundeordrer og salgstilbud. | Ja | Ja | Ja | Nej | Nej |
| 504 | Tilbagekald transaktion | Med denne handling kan brugeren tilbagekalde en tidligere udsat transaktion fra det aktuelle lager. | Ja | Ja | Nej | Ja‡ | Nej |
| 305 | Indløs kundefordelspoint | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ja |
| 635 | Refunder forsendelsesgebyrer | Med denne handling kan brugeren-refundere forsendelsesgebyrer på en annulleret ordre. | Nej | Nej | Nej | Nej | Nej |
| 644 | Fjern kuponkode | Bed brugeren om at fjerne kuponer ved at vælge dem på en liste over kuponer, der aktuelt er knyttet til transaktionen. | Ja | Ja | Nej | Ja | Nej |
| 1057 | Udskriv Z igen | Udskrive Z-rapporten for det tidligere skift eller et valgt skift. | Ja | Ja | Ja | Nej | Nej |
| 1216 | Indtast en ny adgangskode | Med denne handling kan en bruger, som har tilladelse til at nulstille adgangskoder, nulstille adgangskoden for en anden medarbejder ved hjælp af en midlertidig adgangskode. | Ja | Ja | Ja | Nej | Nej |
| 1219 | Åbne URL-adresse i POS | Med denne handling kan en bruger åbne en URL-adresse, der er konfigureret af en administratorer, i POS. | Ja | Ja | Ja | Ja | Nej. | 
| 109 | Returprodukt | Returner individuelle produkter. Det næste scannede produkt vises som et returneret produkt, der har en negativ mængde og pris. | Ja | Ja | Nej | Ja | Nej |
| 114 | Returtransaktion | Tilbagekald en tidligere transaktion ved hjælp af den kvitteringsnummer for at returnere nogle af eller alle produkterne. | Ja | Ja | Ja | Ja§ | Nej |
| 1211 | Deponering til pengeskab | Udfør en deponering til et pengeskab for at flytte penge fra kasseapparatet til et pengeskab. | Ja | Ja | Ja | Ja | Nej |
| 516 | Salgsfaktura | Med denne handling kan kunden foretage betalinger for den valgte salgsfaktura. | Ja | Ja | Nej | Nej | Nej |
| 502 | Sælger | Med denne handling kan brugeren angive værdien **Salgsregistrering** på en salgsordre for kundeordrer i POS. | Ja | Ja | Nr. | Ja\* | Nr. |
| 2000 | Administration af tidsplaner | Denne handling understøttes endnu ikke. | Ja | Ja | Ja | Nr. | Nr. |
| 2001 | Planlægning af anmodninger | Denne handling understøttes endnu ikke. | Ja | Ja | Ja | Nr. | Nr. |
| 622 | Søg i ordrer | Med denne handling kan brugere forudkonfigurere POS-knapperne for at udføre søgninger efter vare, kunde eller kategori. | Ja | Ja | Ja | Ja | Nej |
| 1213 | Søg efter leveringsadresse | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 709 | Vælg hardwarestation | Med denne handling kan brugeren vælge en hardwarestation på en liste over tilgængelige hardwarestationer. | Ja | Ja | Ja | Ja | Nej |
| 637 | Indstil standardsælgeren for transaktionen | Med denne handling kan brugeren vælge en af de berettigede provisionssalgsgrupper (sælgere) som standardsælgeren for linjer, der tilføjes senere. | Ja | Ja | Nej | Ja | Nej |
| 105 | Angiv antal | Rediger antallet af en linjevare i transaktionen. | Ja | Ja | Nej | Ja | Nej |
| 638 | Angiv sælger på linjen | Med denne handling kan brugeren vælge en af de berettigede provisionssalgsgrupper (sælgere) til den aktuelt valgte linje. | Ja | Ja | Nej | Ja | Nej |
| 630 | Send alle produkter | Angiv leveringstilstanden til **Forsendelse** for alle linjeelementer. | Ja | Ja | Nej | Ja\* | Nej |
| 629 | Send valgte produkter | Angiv leveringsmåden til **Forsendelse** for de valgte linjer. | Ja | Ja | Nej | Ja\* | Nej |
| 115 | Vis kladde | Vis kladde for butikken. Du kan få vist transaktioner, udskrive kvitteringer og gavekvitteringer og tilbagekald ved returnering. | Ja | Ja | Ja | Ja\*\* | Nej |
| 802 | Status | Med denne handling kan brugeren oprette eller ændre statusoptællingskladder for fysisk lager eller periodisk optælling. | Ja | Ja | Ja | Nej | Nej |
| 401 | Undermenu | Med denne handling føres brugeren til en anden sammenkædede knapmatrix. | Ja | Ja | Ja | Ja | Nej |
| 1054 | Afbryd skifte | Afbryd det aktuelle skift midlertidigt, så et ny eller forskelligt skift kan aktiveres på det aktuelle kasseapparat. | Ja | Ja | Ja | Nej | Nej |
| 503 | Udsæt transaktion | Afbryd den aktuelle salgstransaktion, så den kan tilbagekaldes senere i butikken. | Ja | Ja | Nej | Ja‡ | Nej |
| 1004 | Arbejdsrutineoptager | Åbn Arbejdsrutineoptager for at registrere en trinvis fremgangsmåde på POS. | Nej | Nej | Nej | Ja | Nej |
| 1052 | Kasseoptælling | Med denne handling kan brugeren angive pengebeløbet i kassen for hver optalt betalingsmetode. | Ja | Ja | Ja | Ja | Nej |
| 1210 | Fjernelse af betalingsmiddel | Med denne handling kan brugeren fjerne penge fra den aktuelle kasseskuffe eller det aktuelle skift. | Ja | Ja | Ja | Ja | Nej |
| 920 | Tidsur | Med denne handling kan brugerne stemple ind og ud af arbejdsskift og pauser. | Ja | Ja | Ja | Nej | Nej |
| 302 | Slutrabatbeløb | Indtast et rabatbeløb for transaktionen. Denne operation kan kun bruges til varer med rabat og kun inden for specifikke rabatgrænser. | Ja | Ja | Nej | Ja | Nej |
| 303 | Slutrabatprocent | Indtast en rabatprocent for transaktionen. Denne operation kan kun bruges til varer med rabat og kun inden for specifikke rabatgrænser. | Ja | Ja | Nej | Ja | Nej |
| 501 | Transaktionskommentar | Føj en kommentar til den aktuelle transaktion. | Ja | Ja | Nej | Ja | Nej |
| 922 | Få vist produktdetaljer | Åbn siden med produktoplysninger for det aktuelt valgte linjeelement. | Ja | Ja | Nej | Ja | Nej |
| 1003 | Vis rapporter | Få vist de rapporter, der er konfigureret for den aktuelle bruger. | Ja | Ja | Ja | Nej | Nej |
| 921 | Vis tidsursangivelser | Vis urposter for alle arbejdere i butikken. | Ja | Ja | Ja | Nej | Nej |
| 211 | Afvis betaling | Annuller den aktuelt valgte betalingslinje fra transaktionen. | Ja | Ja | Nej | Ja | Nej |
| 102 | Afvis produkt | Annuller det aktuelt valgte linjeelement fra transaktionen. | Ja | Ja | Nej | Ja | Nej |
| 500 | Afvis transaktion | Annuller den aktuelle transaktion. | Ja | Ja | Nej | Ja | Nej |
| 916 | Windows Workflow Foundation | Denne handling understøttes ikke. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Nej |
| 924 | X-rapport til bankkort | Denne handling understøttes ikke. | Ikke anvendelig | Ikke anvendelig | Ikke anvendelig | Ikke anvendelig | Ja |
| 311 | Fjern systemrabatter fra transaktioner | Fjern alle de rabatter, der anvendes af systemet, inklusive kuponbaserede rabatter, fra transaktionen. Dette fjerner ikke manuelle rabatter. | Ja | Ja | Ja | Ja | Ingen |
| 312 | Genanvend systemrabatter | Genanvend systemrabatter på transaktionen, hvis de blev fjernet ved hjælp af handlingen **Fjern systemrabatter fra transaktionen**. | Ja | Ja | Ja | Ja | Ingen |

\* Handlingen er kun tilgængelig i offlinetilstand, når der oprettes en kundeordre eller et salgstilbud, og kun hvis offlineoprettelse af kundeordrer og salgstilbud er konfigureret i POS-funktionalitetsprofilen. Handlingen kan ikke udføres, når der oprettes ordrer ved hjælp af Real-time Service, eller når ordrer er tilbagekaldt eller redigeres.

† Handlingen kan kun udføres i offlinetilstand, når POS er konfigureret til at tillade offlineoprettelse af kunder i POS-funktionalitetsprofilen.

‡ Når POS er offline, kan udsatte transaktioner kun tilbagekaldes fra det aktuelle kasseapparats offlinedatabase. Brugere kan ikke udsætte og tilbagekalde transaktioner på tværs af kasseapparater.

§ Når POS er offline, kan kun transaktioner i den aktuelle offlinedatabase tilbagekaldes til returnering.

\*\* Når POS er offline, vises kun transaktioner i den aktuelle offlinekanaldatabase på kladden.
