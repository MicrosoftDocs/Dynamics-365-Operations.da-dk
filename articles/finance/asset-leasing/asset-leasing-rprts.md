---
title: Aktivleasingrapporter
description: I dette emne beskrives kort de rapporter, der er tilgængelige for Aktivleasing.
author: moaamer
manager: Ann Beebe
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4bc4bac1a422a7505ef4c66b9c3b79a3d754cc4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971472"
---
# <a name="asset-leasing-reports"></a>Aktivleasingrapporter

[!include [banner](../includes/banner.md)]

I dette emne beskrives kort de rapporter, der er tilgængelige for Aktivleasing. De fleste rapporter viser ved at udføre disse trin eller trin, der er næsten ens, som angivet). 

- Hvis du vil have vist aktivleasingrapporter vedrørende aktivleasing, skal du gå til **Aktivleasing > Forespørgsler og rapporter > Leasingrapporter** og derefter vælge en rapport, der skal vises. I forbindelse med de rapporter, der kræver en anden udvælgelsessti, medtages de trin, der skal bruges til at åbne rapporten, i beskrivelsen af rapporten. 
- Når du vælger en rapport, der skal udskrives, åbnes en parameterside, som du kan bruge til at filtrere de oplysninger, der medtages i rapporten. Angiv filterkriterier, og vælg derefter **OK** for at generere rapporten. Den genererede rapport indeholder oplysninger, der falder inden for de angivne filtre.

## <a name="asset-movement"></a>Aktivbevægelse
Aktivbevægelserapporten fungerer som en rollforward-rapport for de brugsrettighedsbalancer for hver leasingaftale. Denne rapport giver dig mulighed for at få vist aktivposter for en leasingaftale i en bestemt periode. Rapporten indeholder følgende felter. 

|     Rapportfelter                  |     Betegnelse                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Dato for påbegyndelse              |     Påbegyndelsesdatoen for leasingaftalens tidligste version.                     |   
|     Leasingperiode                     |     Leasingperioden for leasingaftalens tidligste version.                            |
|     Kortfristet leasingaftale               |     Hvis leasingaftalen klassificeres som en kortsigtet leasingaftale, vises som **Ja**.         |
|     Leasingaftale med lav værdi                |     Hvis leasingaftalen klassificeres som en leasingaftale med lav værdi, vises der **Ja**.          |
|     Oprindeligt brugsretsaktiv     |     Den oprindelige værdi af brugsretsaktivet fra den oprindelige genkendelseskladde.      |
|     Startsaldo              |     Den bogførte nettoværdi af brugsretsaktivets pr **Fra dato**.                         |
|     Periodeafskrivningsudgift    |     Beløbet for de afskrivningsudgifter, der stammer fra det datointerval, der er defineret for rapporten.        |
|     Akkumuleret afskrivning       |     Beløbet for akkumuleret afskrivning pr **Fra dato**.                               |
|     Værdiforringelse                     |     Beløbet for de aktiver, der er forringet inden for det datointerval, der er defineret for rapporten.               |
|     Ændringer                  |     Antallet af reguleringer for brugsretsaktiver mellem datoparametre.                            |
|     Bogført nettoværdi                 |     Den slutbogførte nettoværdi af brugsretsaktivet, som er nettobeløbet for den akkumulerede afskrivning pr **Til dato**.    |

## <a name="differences-report"></a>Differencerapport
Forskelsrapporten viser forskellene mellem oplysninger, der er indlæst i leasingimportstrukturen, og de oplysninger, der aktuelt findes i systemet. På denne måde kan du sammenligne, hvad der er justeret, opdateret eller tilføjet via leasingimportstrukturen.  

Værdierne i rapporten varierer, afhængigt af den valgte leasingaftale. Rapporten viser kun de felter, der er forskellige fra det, der aktuelt findes i systemet, og hvad der er i de midlertidige tabeller. Den gamle værdi er det, der enten er i systemet i øjeblikket, eller hvad der tidligere har været i systemet, afhængigt af om importprocessen er kørt. Den nye værdi viser den værdi, der er i den midlertidige tabel, der erstatter den gamle værdi.

## <a name="five-years-undiscounted-payment-forecast"></a>Prognose for fem års ikke-diskonteret betaling
Rapporten for de fem års ikke-diskonterede betalingsprognose viser de forventede ikke-diskonterede leasingbetalinger, der skal betales i løbet af de næste fem år fra den dato, der er angivet i rapportparametrene. Rapporten indeholder følgende felter. 

|     Rapportfelter         |     Betegnelse                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Leasingbeskrivelse     |     Leasingbeskrivelsen fra leasingoverskriften.                                                      |
|     Leasing-id              |     Entydigt ID for leasingaftale.                                                                              |
|     Kartotek                  |     Det leasingkartotek, der er tilknyttet det bogførte ID.                                                         |
|     Klassifikation        |     Klassifikationen af leasingaftalen.                                                                  |
|     Posteringslag         |     Det lag, hvor denne leasingaftale skal bogføres.                                                         |
|     Valuta              |     Leasingaftalens valuta.                                                                        |
|     Løbende               |     Summen af alle de leasingbetalinger, der skal betales inden for de næste 12 måneder fra rapporteringsdatoen.          |
|     13 - 24 måneder          |     Summen af alle de leasingbetalinger, der skal betales mellem 13 og 24 måneder fra rapporteringsdatoen.           |
|     25 - 36 måneder          |     Summen af alle de leasingbetalinger, der skal betales mellem 25 og 36 måneder fra rapporteringsdatoen.           |
|     37 - 48 måneder          |     Summen af alle de leasingbetalinger, der skal betales mellem 37 og 48 måneder fra rapporteringsdatoen.           |
|     49 - 60 måneder          |     Summen af alle de leasingbetalinger, der skal betales mellem 49 og 60 måneder fra rapporteringsdatoen.           |
|     Herefter            |     Summen af alle de leasingbetalinger, der skal betales på eller efter 61 måneder fra rapporteringsdatoen.              |

## <a name="gaap-cash-flows-report"></a>GAAP-pengestrømsrapport
GAAP-afslutningsrapporten opfylder kravene i US GAAP til offentliggørelse, der er angivet i 842-20-50-4 (g) (1). Hvis du vil se denne rapport, skal du gå til **Aktivleasing > Forespørgsler og rapporter > Afslutningerne > GAAP – pengestrømme**. 

|     Rapportfelter                                 |     Betegnelse                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     Fra-dato <br> Til-dato                        |     Definerer et datointerval, der bruges til at begrænse de oplysninger, der medtages i rapporten.      |
|     Juridisk enhed                                  |     Den juridiske enhed, der er knyttet til leasingaftalerne.                                      |
|     Leasingaftaletype                                    |     Klassificeringen af leasingaftalen som enten finansiering eller drift.           |
|     Leasing-id                                      |     Entydigt ID for leasingaftale.                                                      |
|     Leasingbeskrivelse                             |     Leasingbeskrivelsen fra leasingoverskriften.                              |
|     Leasingkartotek                                    |     Det leasingkartotek, som linjen refererer til.                        |
|     Posteringslag                                 |     Hver bog, der tilknyttes et anlægsaktiv, oprettes til et bestemt posteringslag med et overordnet afskrivningsformål.                          |
|     Leasingaftalegruppe                                   |     Den gruppe, som leasingaftalen er tilknyttet.                                     |
|     Valuta                                      |     Den forkortelse, der er anvendt til transaktionsvaluta. Alle rapporter konverterer transaktionsvalutaen til rapporteringsvalutaen.                      |
|     Finansiel leasingaftale - Operationelle pengestrømme         |     Summen af de samlede bogførte variable betalinger og de samlede rentebetalinger, der er bogført fra amortiseringsplanen mellem datoparametrene.        |
|     Finansiel leasingaftale - Finansielle pengestrømme           |     Summen af de samlede hovedbetalinger fra amortiseringsplanen mellem datoparametrene.       |
|     Operationelle leasingaftaler - Operationelle pengestrømme       |     Summen af alle bogførte leasingbetalinger og bogførte variable betalinger mellem datoparametrene.            |

## <a name="lease-balances-forecast"></a>Prognose for leasingsaldi
Leasingaftalen i budgetsaldi viser oplysninger direkte fra planlægningen for passiv afskrivning og afskrivningsplanen for aktiver. Rapporten viser de budgetterede beløb for det forventede leasingforbrug, og de rettigheder, der gælder for et bestemt tidsrum, herunder alle forventede udgifter for disse leasingaftaler. Rapporten indeholder følgende felter.

|     Rapportfelter                 |     Betegnelse                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Startsaldo             |     Primosaldoen i planlægningen af leasingaftalens afskrivning for den periode, der indeholder rapportens startdato.            |
|     Første indregning           |     Hvis leasingaftalens startdato ligger inden for det datointerval, der er defineret for rapporten, viser denne kolonneværdien af passivkontoen i den oprindelige genkendelseskladdepost.      |
|     Betalinger                      |     Summen af leasingbetalingens betalinger, der falder inden for det datointerval, der er defineret for rapporten.                               |
|     Interesser                      |     Summen af leasingaftalens renteudgifter, der falder inden for det datointerval, der er defineret for rapporten.                    |
|     Slutsaldo                |     Leasingforpligtelsens saldoen pr **Til dato**.                                                             |
|     Kortfristet forpligtelse          |     Det kortfristede leasingbeløb i leasingaftalens amortiseringsplan pr **Til dato**.                           |
|     Langfristede forpligtelse           |     Det langsigtede leasingbeløb i leasingaftalens amortiseringsplan pr **Til dato**.                            |
|     Primo bogført nettoværdi      |     Primo bogført nettoværdi i planlægningen af leasingaftalens aktivafskrivning for den periode, der indeholder rapportens startdato.      |
|     Første indregning           |     Hvis leasingaftalens startdato ligger inden for det datointerval, der er defineret for rapporten, viser denne kolonne aktivkontoværdien for den oprindelige genkendelseskladdepost.            |
|     Afskrivningsomkostning          |     Summen af leasingaftalens afskrivning, der falder inden for det datointerval, der er defineret for rapporten.                  |
|     Slutsaldo                |     Leasingforpligtelsens aktivsaldo pr **Til dato**.                                                              |
|     Egenkapitalregulering             |     Startsaldoen minus primo bogført nettoværdi.                                                             |

## <a name="lease-commencements-report"></a>Rapport over leasingaftalens påbegyndelse
Leasingaftalens startdato viser alle rettigheder, der er påbegyndt inden for et angivet datointerval, herunder det første forpligtelse og brugsrettighedsbalancer. Rapporten indeholder følgende felter. 

|     Rapportfelter                 |     Betegnelse                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Dato for påbegyndelse             |     Dato for den postering med den oprindelige genkendelseskladde, der blev bogført for den pågældende leasingaftaleversion.         |
|     Oprindelig forpligtelsesbeløb      |     Ansvarsbeløbet fra den oprindelige genkendelseskladdepost.                                  |
|     Startbeløb for aktiv          |     Aktivbeløbet fra den oprindelige genkendelseskladdepost.                                      |

## <a name="lease-modification-report"></a>Leasingaftalens ændringsrapport
I rapporten med leasingaftalens ændringer vises alle rettigheder, der er ændret inden for et bestemt datointerval. Rapporten viser også den bruger, der justerede leasingaftalen, og det samlede ansvarsbeløb, der er reguleret. Rapporten indeholder følgende felter. 

|     Rapportfelter                 |     Betegnelse           |
|---------------------------------  |-------------------------  |
|     Reguleret af                   |     Brugernavnet for den person, der redigerede leasingaftalen.                                |
|     Justeringsform               |     Den dato, reguleringskladdeposten blev bogført.                        |
|     Reguleringer                   |     Beløbet for alle de reguleringskladdeposter, der er bogført på leasingaftalens forpligtelseskonti mellem datoparametrene. Kreditter vil fremstå positive, mens debiteringer vil være negative.       |
|     Gevinstbeløb (tab)            |     Beløbet for alle de reguleringskladdeposter, der er bogført på leasingaftalens gevinst/tab mellem datoparametrene. Kreditter vil fremstå positive, mens debiteringer vil være negative.       |
|     Overført resultat             |     Beløbet for alle de reguleringskladdeposter, der er bogført på leasingaftalens overførte resultater mellem datoparametrene.      |
|     Afsluttende passivsaldo      |     Leasingforpligtelsens resultat pr reguleringsdato for leasingaftalen.           |

## <a name="lease-movement-report"></a>Rapport over leasingaftalens bevægelser
Rapporten over leasingaftalens bevægelser fungerer som en rollforward-rapport for de leasingforpligtelserne for hver leasingaftale. Denne rapport giver brugeren mulighed for at se forpligtelsestransaktioner for en leasingaftale i en bestemt periode.

|     Rapportfelter             |     Betegnelse                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Dato for påbegyndelse         |     Påbegyndelsesdatoen for leasingaftalens tidligste version.    |
|     Leasingperiode                |     Leasingperioden for leasingaftalens tidligste version.           |
|     Resterende betalinger        |     Det antal betalinger, der endnu ikke er bogført for leasingaftalen.                       |
|     Startsaldo         |     Summen af alle posteringer, der påvirker den leasingaftalens forpligtelse, der er opstået før rapportens startdato.             |
|     Første indregning       |     Beløbet for eventuelle første genkendelsestransaktion for den leasingaftale, der blev bogført inden for det datointerval, der er defineret for rapporten.     |
|     Betalinger                  |     Summen af leasingaftalens betalingstransaktioner, der falder inden for det datointerval, der er defineret for rapporten. Værdierne i denne kolonne vises som negative beløb, efterhånden som betalingerne reducerer leasingaftalens forpligtelsessaldo.  |
|     Interesser                  |     Summen af renteperiodiseringer, der vedrører leasingaftalen, og som falder inden for det datointerval, der er defineret for rapporten.            |
|     Reguleringer               |     Summen af leasingaftalens bogførte reguleringstransaktioner, der falder inden for det datointerval, der er defineret for rapporten.                               |
|     Slutsaldo            |     Saldoen for alle transaktioner i leasingaftalens forpligtelse, der er bogført pr **Til dato** i rapporten.                  |

## <a name="lease-transactions-report"></a>Rapport over leasingaftalens transaktioner
Forespørgslen vedrørende leasingaftalens transaktioner viser alle de kladdeposter, der er genereret af aktivleasing. Hver kladdepost er knyttet til det bogførte ID, som den stammer fra. Det giver dig mulighed for nemt at knytte kladdeposten til den tilsvarende leasingaftale. Forespørgslens leasingtransaktioner fungerer på en måde, der ligner siden **Bilagstransaktioner** i Finans.

## <a name="weighted-average-discount-rate-report"></a>Rapporten med vægtet gennemsnitsrabatsats
Rapporten med gennemsnitsrabatsats opfylder de krav til US GAAP, der er angivet i ASC-842-20-50-4(g)(4) for en vægtet gennemsnitsrabatsats. Hvis du vil se denne rapport, skal du gå til **Aktivleasing > Forespørgsler og rapporter > Afslutninger > Vægtet gennemsnitsrabatsats**. Rapporten indeholder følgende felter. 

|     Rapportfelter                     |     Betegnelse                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Fra og med dato                        |     Denne rapport indeholder alle de leasingaftaler, der er påbegyndt på eller før **Pr dato**-parameteren. Denne rapport skal køres pr. sidste dag i den periode, der skal forsættes.      |
|     Juridisk enhed                      |     Den juridiske enhed, der er knyttet til leasingaftalen.                           |
|     Leasing-id                          |     Entydigt ID for leasingaftale.                                                  |
|     Leasingbeskrivelse                 |     Leasingbeskrivelsen fra leasingoverskriften.                          |
|     Kartotek                              |     Den angivne kartotektype for den viste leasingaftale.                                                                                                                                            |
|     Posteringslag                     |     Hver bog, der tilknyttes et anlægsaktiv, oprettes til et bestemt posteringslag med et overordnet afskrivningsformål.      |
|     Leasinggruppe                       |     Den gruppe, som leasingaftalen tilhører.                                 |
|     Rabatsats                     |     Den sats, der bruges til at diskontere leasingbetalinger.                             |
|     Valuta                          |     Den forkortelse, der er anvendt til transaktionsvaluta. Alle rapporter konverterer transaktionsvalutaen til rapporteringsvalutaen.  |
|     Resterende leasingbetalinger          |     Det samlede beløb for ubetalte leasingbetalinger fra den resterende betalingsplan fra **Pr** dato.            |
|     Resterende vægtede betalinger       |     Leasingaftalens betalinger skal multipliceres med den anvendte diskonteringssats.   |
