---
title: Kom i gang med aktivleasing
description: Dette emne beskriver aktivleasingkapaciteten og gennemgår trinnene til oprettelse af aktivleasing og visning af oplysninger for disse leasinger.
author: moaamer
manager: Ann Beebe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9e206569aad3f53a2f6f66e6d6253226e5980078
ms.sourcegitcommit: 30c541426cf2037b768e3556e1b170a64991f64a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/17/2020
ms.locfileid: "4441734"
---
# <a name="asset-leasing-get-started"></a>Kom i gang med aktivleasing

[!include [banner](../includes/banner.md)]

Dette emne beskriver aktivleasingkapaciteten og gennemgår trinnene til oprettelse af aktivleasing og visning af oplysninger for disse leasinger. Emnet definerer også den terminologi, der bruges i brugergrænsefladen og dokumentationen. Aktivleasing er et avanceret funktion til styring, sporing og automatisering af finanstransaktioner for leasede aktiver i Microsoft Dynamics 365 Finance. Aktivleasing overholder internationale regnskabsstandarder (IFRS 16) og US GAAP-standarder (ASC 842). Aktivleasing registrerer og behandler leasingoplysninger og opretter kladdeposteringer for leasingens levetid fra den første registrering over månedlige kladdeposteringer til værdiforringelsen og afslutningen af leasingen. Aktivleasing integreres problemfrit med andre komponenter i Dynamics 365 Finance, herunder anlægsaktiver, kreditor og finans.

Du kan få flere oplysninger om regnskabsstandarder i standarddokumentationen til IFRS 16 og US GAAP ASC 842.

## <a name="asset-leasing-elements"></a>Aktivleasingelementer
I følgende diagram vises de vigtigste elementer i forretningsprocessen for leasinger.

[![Aktivleasingelementer](./media/overview-01.png)](./media/overview-01.png)

Et leaset aktiv indeholder følgende hovedkomponenter:

- **Leasingaftale** – Leasinggiveren ejer aktivet og aftaler med leasingtageren, at et aktiv leases i en bestemt periode mod regelmæssige leasingbetalinger. Ud over den juridiske kontrakt mellem leasinggiveren og leasingtageren indeholder leasingaftalen administrative beslutninger som f.eks. sandsynligheden for at gennemføre en fornyelsesmulighed og overdragelse af ejerskab.

- **Leasingberegning og klassificering pr. regnskabsstandard** - Leasingberegningen og klassificeringen identificerer den regnskabsstandard, der anvendes i den første og den efterfølgende måling, samt klassifikationstesten, der bestemmer, hvad leasingtypen vil være. En leasing kan være en finansiel leasing, en operationel leasing, en kortfristet leasing eller en lavværdileasing. Systemet beregner også den nuværende værdi af fremtidige minimumsleasingbetalinger med henblik på værdiansættelse og klassifikation.

- **Leasingtransaktioner** – Aktivleasing understøtter den første anerkendelse af brugsretsaktivet for leasinger på balancen samt efterfølgende måling af enten balanceførte leasinger eller ikke-balanceførte leasinger. Ved den første genkendelsestransaktion måles den aktuelle værdi af fremtidige mindsteleasingbetalinger. Disse data bruges til at bestemme værdien af det første brugsretsaktiv og den første leasingforpligtelse, som påvirker organisationens balance. Den efterfølgende måling af de månedlige leasingtransaktioner omfatter akkumulering af rente for leasingforpligtelsen, hvilket øger leasingforpligtelsen. Det måler også de periodiserede leasingbetalinger, der reducerer leasingforpligtelsen, og som efterfølgende vil blive udbetalt til leasinggiveren. Målingen indeholder også amortisering af brugsretsaktivet.

  I forbindelse med ikke-balanceførte leasinger beregner systemet den lineære leasingudgift i forhold til det mindste beløb: aktivets økonomiske levetid eller leasingperioden. Ved leasingreguleringerne måles kontraktændringer, f.eks. en leasings forlængelse eller udvidelse, og den værdiforringelsestransaktion, der bruger brugsretsaktivet til ikke-refunderbare omkostninger.

  Aktivleasing integreres med Finans for at sikre, at alle bogførte leasingtransaktioner opdaterer kontoplanen. Aktivleasing integreres med kreditorer for at spore leasinggiverfakturaer i kreditor og foretage fremtidige betalinger derfra. Integrationen med anlægsaktiver giver dig mulighed for at spore leasinger i anlægsaktivregistret og bogføre brugsretsaktivstransaktioner, herunder den første anerkendelse, afskrivning og værdiforringelse af aktivet, inde fra Anlægsaktiver.   

## <a name="asset-leasing-components"></a>Komponenter for aktivleasing 
Aktivleasing tilknytter leasingoplysninger, betalingsplaner, start- og slutdatoer og betalingsfrekvensen. Den automatiserer også beregninger for nutidsværdien, månedlige leasingbetalinger, renter og amortisering af leasing. Systemet udfører test af leasingklassifikation afhængigt af konfigurationen. I systemet oprettes og bogføres også de tilsvarende leasingtransaktioner, som er baseret på den struktur, der er defineret af den regnskabsstandard, du følger.

I følgende diagram vises leasingbogen, leasingen, beregnet betalingsplan, klassifikationstest for leasinger og leasingbøger samt de tilsvarende regnskabstransaktioner.

[![Leasing, leasingbog og betalingsplan](./media/overview-02.png)](./media/overview-02.png)

- **Leasingbog** - Leasingbogen omfatter alle oplysninger om leasingkontrakten, f.eks. leasingperiode, handelsværdi og leasingbetalinger. Den omfatter også den regnskabsstandard, som du følger, den leasingtype og de tærskler, der tages i betragtning ved test af leasingklassifikation. Leasingbogen indeholder også de leasingtransaktioner, der er bogført i finans. 
  
- **Leasing** - Leasingen indeholder oplysninger om aktivleasing, der repræsenterer grundlaget for aktivleasing, kilden til leasingoplysninger er leasingkontrakt og administrative beslutninger, som begge sker uden for Dynamics 365 Finance. Anlægsaktivets handelsværdi er den pris, der ville blive betalt for et aktiv i en transaktion på målingsdatoen. Denne værdi kan afhænge af aktivtypen, markedsbetingelserne og andre kriterier, der kan tages i betragtning under vurderingen. Aktivets handelsværdi vil blive taget i betragtning i klassifikationens testligning.

- **Aktivets brugstid** - Repræsenterer de resterende perioder for et aktivs brugstid fra leasingens startdato. Aktivets brugstid vil blive taget i betragtning i klassifikationens testligning. Den adskiller sig fra den brugstid, der er defineret i anlægsaktiver.

- **Trinvis lånesats** - Dette er den rentesats, der vil blive brugt til beregning af nutidsværdien. Systemet bruger den implicitte sats, hvis den er defineret i leasingdataene, til beregning af den aktuelle værdi af leasingbetalingerne. Hvis den implicitte sats ikke er defineret, vil systemet bruge den trinvise lånesats.

- **Annuitetstype** - Dette er leasingbetalingen, som enten forfalder i starten af betalingsperioden eller i slutningen af perioden. Dette kan være forskudsbetaling eller forfalden annuitet (ved begyndelsen af leasingbetalingsperioden) eller almindelige annuiteter (ved afslutningen af leasingbetalingsperioden).

  Den første måned betragtes som periode nummer nul for forskudsbetaling. Den første måned vil blive vurderet som en periode for efterbetalinger.

- **Sammenlægningsinterval** - Det repræsenterer det antal perioder, som renten sammenlægges pr. år. Dette kan f.eks. være månedligt (12 perioder pr. år), kvartalsvist (4 perioder pr. år), halvårligt (2 perioder pr. år) eller hvert år (1 periode pr. år). Antallet af perioder tages i betragtning i beregningen af nutidsværdien.

- **Ikrafttrædelsesdato** - Dette er den dato, hvor leasinggiveren gør aktivet tilgængeligt for leasingtagerens brug. Alle leasingberegninger og transaktioner baseres på ikrafttrædelsesdatoen. Ikrafttrædelsesdatoen skal være i begyndelsen af en periode (først i måneden) for at sikre nøjagtigheden af efterfølgende beregninger. Du kan bruge feltet **Kontraktsignaturdato** til at angive den faktiske dato, hvor kontrakten blev underskrevet.

- **Leasingperiode** – Dette er længden af leasingperioden i antal måneder.

> [!NOTE] 
> Definitionen af leasingperioden er baseret på antallet af perioder, eller intervaller, i betalingsplanens linjer. Det definerede antal intervaller vil blive konverteret til måneder.

- **Betalingsplanslinje** - Den registrerer leasingbetalingerne pr. periode. Den angiver også, om en fornyelsesperiode skal udøves og medtages i den første måling af brugsretsaktivet og leasingforpligtelsen. Du kan definere startdatoen for de forfaldne leasingbetalinger og de periodeintervaller, der angiver længden af leasingen, som kan være dage, måneder eller år.

- **Betalingsfrekvens** – Dette angiver, om betalingen er månedlig, kvartalsvis, halvårlig eller årlig. Slutdatoen beregnes automatisk på baggrund af startdatoen og antallet af angivne perioder.

- **Betalingsplan** - Dette er den beregnede nutidsværdi baseret på den tid, der er omfattet af leasingbetalingerne, betalingernes beløb, sammenlægningsperioderne og annuitetstypen.

- **Perioder** - Det er de leasingperioder, der afspejler den interne sammenlægning og annuitetstype. Sammenlægningsintervallet bestemmer, hvordan perioderne opdeles. Du kan angive følgende sammenlægningsintervaller:

  - Månedligt, 12 perioder pr. år
  - Kvartalsvist, 4 perioder pr. år
  - Halvårligt, 2 perioder pr. år
  - Årligt, 1 perioder pr. år

Den første periode starter med periode nul, hvis annuitetstypen er forfalden annuitet. Ellers starter den første periode med periode ét, hvis annuitetstypen er efterbetalinger.

- **Måneder** - Dette angiver antallet af kalendermåneder i leasingforløbet. Betalingsbeløbet er det forfaldne beløb, som det er defineret i betalingsfrekvensen. Den beregnede nutidsværdi er den aktuelle værdibaserede leasingbetaling pr. periode, sammenlægningsintervallerne og den trinvise lånesats.

> [!NOTE] 
> Nutidsværdien beregnes på baggrund af den nedsatte likviditetsligning.

- **Bøger** - Dette er den forudkonfigurerede opsætning, der vil blive knyttet til hver leasing. I bogen defineres de anvendte regnskabsstandarder, leasingtyper og den tærskel, der skal bruges som grundlag for klassifikationstestene. Klassifikationstest bruges til at angive leasingtypen automatisk.

- **Regnskabsstruktur** – Den viser den valgte regnskabsstandard, enten IFRS 16 og ASC 842, som du understøtter. Regnskabsstandarden angives i den bog, der er knyttet til leasingen. Regnskabsstandarden bestemmer, hvilke finanskonti der er angivet i posteringsprofilen.

- **Leasingtyper** Den angiver, hvilken af de to typer leasinger der vil blive brugt, enten en finansiel leasing eller en operationel leasing. Under en finansiel leasing overføres risici og belønninger, der er relateret til det leasede aktiv, til leasingtageren. Under en operationel leasing vil risici og belønninger, der vedrører et leaset aktiv, forblive hos leasinggiveren. En tredje mulighed er en automatisk identifikation af leasingtypen, enten finansiel eller operationel, baseret på de definerede tærskler i bogen. Denne automatiske identifikation udføres under genklassificeringstesten af leasingen.

- **Tærskler** - Dette bruges i test af leasingklassifikation til at bestemme, om aktivet klassificeres som et af følgende:

  - **Leasingperiode** - Det er den procentdel af brugstiden, der skal bruges i klassifikationstesten. Systemet klassificerer leasingen som finansiel, hvis leasingtypen er angivet til automatisk, og hvis leasingperioden for aktivets brugstid er større end eller lig med den procent, der er defineret her.

  - **Nutidsværdi** - Det er den procentdel af aktivets handelsværdi, der skal bruges i klassifikationstesten. Systemet klassificerer leasingen som finansiel, hvis leasingtypen er angivet til automatisk, og hvis nutidsværdien af fremtidige leasingbetalinger for aktivets handelsværdi er større end eller lig med den procent, der er defineret her.

  - **Kortfristet leasing** – Hvis leasingperioden er mindre end eller lig med den angivne værdi, klassificeres leasingen som en kortfristet leasing.

  - **Lavværdi** – Hvis handelsværdien af aktivet er mindre end eller lig med den definerede værdi, klassificeres leasingen som en lavværdileasing.

  - **Leasingklassifikation og -transaktioner** Leasingklassifikationen er en automatisk proces, der bruges til at klassificere leasinger baseret på de fastsatte tærskler i bøger ud over andre klassifikationstestkriterier, for at identificere, om leasingen er en finansiel leasing, operationel leasing, kortfristet leasing eller lavværdileasing. Dette bruges også til at identificere, om den udskudte lejeproces følges.

Klassifikationstest omfatter overdragelse af ejendomsretten, købsoption, leasingperiode, nutidsværdi og entydigt aktiv. Følgende diagram viser klassifikationstest af leasinger.

[![Test af leasingklassifikation](./media/overview-03.png)](./media/overview-03.png)

Hver leasingtype håndterer regnskabet forskelligt for forskellige leasingtransaktioner. Transaktionerne omfatter indledende anerkendelse, renteudgift, forfalden leasingbetaling og leasingafskrivning, og de er baseret på de regnskabsstandarder, du følger (IFRS 16 eller ASC 842). Finanskonti defineres under leasingposteringsprofilen for hver transaktionstype og regnskabsstruktur.

## <a name="asset-leasing-transactions"></a>Leasingtransaktioner for aktiv

#### <a name="initial-recognition"></a>Første indregning 
Den første anerkendelse af et leaset aktiv bruger den beregnede nutidsværdi, så den kan rapporteres på balancen. Regnskabsposten for denne genereres automatisk. Denne transaktion debiterer kontoen for brugsretsaktivet og krediterer den operationelle leasingforpligtelseskonto på følgende måde. Hvis der er knyttet et anlægsaktiv til leasingen, vil den oprindelige anerkendelsespost blive vist som en anskaffelse af et anlægsaktiv. I dette scenario skal du definere en posteringsprofil for anlægsaktiver, der skal bogføres på brugsretsaktivets konto. 

> [!NOTE]
> Operationelle leasinger understøttes kun af US GAAP ASC 842.

|     Type                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operationel leasing under US GAAP              |     Brugsretsaktiv      |     Operationel leasingforpligtelse       |
|     Finansiel leasing under IFRS og US GAAP        |     Brugsretsaktiv      |     Operationel leasingforpligtelse       |

#### <a name="lease-liability-amortization-interest-expense"></a>Amortisering af leasingforpligtelse (renteudgift) 
Renten for en leasing anerkendes ved at beregne rente for leasingens startsaldo, leasingbetaling for perioder, rentelånesats og sammenlægningsintervalperioder pr. år. Rentebeløbet øger den operationelle leasingforpligtelseskonto ved at kreditere den, hvilket vil blive afspejlet i organisationens balance. Transaktionen omfatter også en debetpost på renteudgiftskontoen, som afspejles på driftsregnskabet for finansielle leasinger og på leasingudgiftskontoen for operationelle leasinger.

|     Type                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Post for operationel leasingforpligtelse under US GAAP ASC 842    |     Renteudgift          |     Operationel leasingforpligtelse         |
|     Post for finansiel leasingforpligtelse under IFRS og US GAAP      |     Renteudgift          |     Finansiel leasingforpligtelse           |

#### <a name="accrued-lease-payment"></a>Periodiseret leasingbetaling
En periodiseret leasingbetaling anerkendes som en fremtidig leasingbetaling, der er forfalden til at blive behandlet som en betalingstransaktion fra bank- eller kontantkonti. Den forfaldne leasingbetaling reducerer leasingforpligtelsen ved at debitere leasingforpligtelseskontoen mod, om en kreditorreskontro i tilfældet af en leasinggiver er defineret som en kreditor, eller kreditsiden bogføres på en finanskonto for vekselgæld, så betalingen vil blive udført mod enten kreditor eller vekselgæld.

|     Type                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operationel leasing under US GAAP              |  Operationel leasingforpligtelse    |   Kreditors passiv (reskontro)/Vekselgæld  |
|     Finansiel leasing under IFRS og US GAAP        |  Finansiel leasingforpligtelse      |   Kreditors passiv (reskontro)/Vekselgæld  |

#### <a name="asset-depreciation"></a>Afskrivning af aktiv
Brugsretsaktivet afskrives i forhold til den mindste værdi, som enten er aktivets brugstid eller leasingperioden. Metoden til beregning af afskrivning for US GAAP (ASC 842) er baseret på forskellen mellem den lineære leasingudgift og rentebeløbet. Renter på finansiel leasing beregnes ved hjælp af en lineær standardmetode. Leasingafskrivningen har indflydelse på driftsregnskabet ved debitering af renteudgifter. Balancen påvirkes ved kreditering af akkumuleret brugsretsaktivkonto for finansielle leasinger. For operationel leasing krediterer afskrivningen leasingens udgiftskonto. Hvis leasingen er knyttet til et anlægsaktiv, udføres afskrivningstransaktionerne kun fra anlægsaktivmodulet. 

|     Type                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operationel leasing under US GAAP              |  Leasingudgift                |   Akkumuleret afskrivning af brugsretsaktiv     |
|     Finansiel leasing under IFRS og US GAAP        |   Afskrivning af brugsretsaktivets udgift   |   Akkumuleret afskrivning af brugsretsaktiv    |

#### <a name="short-term-lease"></a>Kortfristet leasing
En kortfristet leasing anerkendes som en udgift, der vil påvirke en organisations resultatopgørelse. Den genererede forfaldne leasingbetaling vil debitere leasingudgiftskontoen og kreditere vekselgælds- eller kreditorens reskontrokonto.

|     Type                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Post for kortfristet leasing under IFRS og US GAAP     |  Leasingudgift                |   Kreditors passiv (reskontro)/Vekselgæld  |

#### <a name="low-value-lease"></a>Lavværdileasing
En lavværdileasing anerkendes som en udgift, der påvirker din organisations resultatopgørelse. Den genererede forfaldne leasingbetaling vil debitere leasingudgiftskontoen og kreditere vekselgælds- eller kreditorens reskontrokonto.

|     Type                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Post for lavværdileasing under IFRS og US GAAP      |  Leasingudgift                |   Kreditors passiv (reskontro)/Vekselgæld  |


#### <a name="index-revaluation"></a>Værdiregulering af indeks
Dette er aktivleasingkontoen for variable leasingbetalinger, der måles med en indekssats. Ændringer i leasingbetalinger, der skyldes indekssatsudsving, udgør en leasingregulering under IFRS 16. Leasingforpligtelsen og brugsretsaktiverne reguleres for at afstemme de nye betalinger. 

|     Type                                          |     Debet                             |     Kredit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Indeksrevaluering under IFRS i tilfælde af forøgelse  |  Brugsretsaktiv       |   Operationel leasingforpligtelse |
|   Indeksrevaluering under IFRS i tilfælde af fald  |  Operationel leasingforpligtelse  |   Brugsretsaktiv      |

Når betalinger ændres på grund af en ændring af indekssatsen, vil kun de variable betalinger blive ændret, medmindre der er flere ændringer i pengestrømme, f.eks. en ændring i leasingperioder for rentesatser i henhold til US GAAP ASC 842.

#### <a name="lease-adjustment"></a>Leasingregulering
Ved leasing af aktiver kan leasinger reguleres, hvis leasingperioderne ændres, leasingen forlænges, eller hvis der er flere omstændigheder, inden for hvilke en leasing kræver en regulering. Der bogføres leasingreguleringer for at øge eller reducere brugsretsaktivet og leasingforpligtelsen. Reguleringsprocessen tager overførte slutsaldi for amortisering af passiver og aktivsaldo på reguleringsdatoen. Når en leasing er knyttet til anlægsaktivet, bogføres reguleringen af brugsretten ved hjælp af det id, der er tildelt i Anlægsaktiver. 

|     Type                                          |     Debet                             |     Kredit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Reguleringspost til leasing for IFRS og US GAAP i tilfælde af forøgelse     |  Brugsretsaktiv       |   Operationel leasingforpligtelse |
|   Reguleringspost til leasing for IFRS og US GAAP i tilfælde af fald     |  Operationel leasingforpligtelse  |   Brugsretsaktiv      |


#### <a name="lease-impairment"></a>Værdiforringelse af leasing
Dette repræsenterer den overførte saldoreduktion af brugsretsaktivet. Identificer værdiforringelsesbeløbet, transaktionsdatoen og de resterende perioder. Det resterende brugsretsaktiv amortiseres på et lineært grundlag. Logikken for leasingens værdiforringelse vurderer aktivets overførte værdi, som findes i afskrivningsplanen for aktiver.  

|     Type                                          |     Debet                             |     Kredit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Post til værdiforringelse for IFRS og US GAAP           |  Udgift til værdiforringelse                   |    Brugsretsaktiv     |

>[!NOTE]
> Hvis leasingen er knyttet til et anlægsaktiv, skal værdiforringelseen af leasingen bogføres fra anlægsaktiver, da afskrivning af aktiver køres fra modulet Anlægsaktiver.

**Dobbelt valuta** Leasingtransaktioner kan bogføres i en anden valuta end regnskabs- og rapporteringsvalutaen. Valutakursen er angivet i finansmodulet på ikrafttrædelsesdatoen. Du kan ændre valutakurserne ved at indstille feltet **Fastkurs** til **Ja**, når du opretter leasingen. Når du angiver leasingtransaktioner, vil de første anerkendelsestransaktioner og efterfølgende afskrivningstransaktioner bruge valutakursen pr. ikrafttrædelsesdatoen. De efterfølgende betalings- og rentetransaktioner vil bruge den aktuelt aktive valutakurs. 

## <a name="create-an-asset-lease"></a>Oprette en aktivleasing
Udfør følgende trin for at oprette en ny leasing. 

1. Hvis du vil bruge **Aktivleasing**, skal du aktivere den i arbejdsområdet **Funktionsstyring**. Fra arbejdsområdet **Funktionsstyring** skal du vælge **Alle**, så alle funktioner vises på siden. Vælg **Aktivleasing**, og vælg derefter **Aktivér nu**.
2. Gå til **Aktivleasing > Generelt > Leasingoversigt**. I oversigtspanelet **Generelt** skal du udfylde de obligatoriske felter. 
   - **Leasingdetaljer**
   - **Brugstid for aktiv (måneder)**
   - **Leasinggruppe**
   - **Trinvis lånesats (%)**
   - **Sammensætningsinterval**
   - **Annuitetstype**
   - **Valuta**
   - **Dato for påbegyndelse**

3. Gå til oversigtspanelet **Betalingsplanslinjer**, angiv en betalingslinje, og vælg **Opret planer**.

4. Vælg **Bøger**. 

5. Skift til oversigtspanelet **Generelt**. Det **Første leasingforpligtelse** og **leasingforpligtelse** beregnes. 

6. Gå til oversigtspanelet **Test af leasingklassifikation** for at kontrollere værdien i feltet **Leasingtype**. 

   Den automatiske **Leasingtype** klassificeres ud fra de kriterier, der er defineret på siden **Bøger**.

7.  Gå til **Betalingsplan** i sektionen **Funktion**.  

   Siden **Betalingsplan** viser fremtidige betalingsplaner for et leasing-id. Vælg **Bekræft tidsplan** for at kunne bogføre **Første anerkendelse**-transaktioner. 

[![Funktionen til første anerkendelse](./media/overview-13.png)](./media/overview-13.png)

8. Vælg **Første anerkendelse** for at oprette en indledende anerkendelseskladde. 

9. Vælg **Aktivleasingkladder** for at bogføre den første anerkendelsestransaktion. 

   Fra betalingsplanen kan du åbne en detaljeret side, der viser transaktioner for brugsretsaktiv. 
 
   **Amortiseringsplanen for leasingforpligtelse** viser det rentebeløb, der er beregnet for hver periode.
   
10. Opret kladden, og gå derefter til **Aktivleasingkladder**. **Amortiseringsplanen for leasingforpligtelse** vises også i rentetransaktionerne.

   På siden **afskrivningsplan for aktiver** vises afskrivningstransaktionerne for det valgte leasing-id. 

   [![Side for ROU-aktivtransaktioner](./media/overview-20.png)](./media/overview-20.png)

   På siden **ROU-aktivtransaktioner** vises den første anerkendelse, akkumuleret afskrivning og aktivets saldo. 

   Siden **Transaktioner for leasingforpligtelse** viser den første anerkendelse, betaling af leasingrente, leasingbetaling og saldoen for leasingforpligtelse. 

