---
title: "Organisere dine medarbejdere, ved hjælp af afdelinger, job og stillinger"
description: "Afdelinger, job og stillinger er organisatoriske elementer, der vedligeholdes i Personale. Dette emne beskriver begrebsmæssige oplysninger om disse elementer."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: f1bbc66ecefb12d14d7d707ada2b99ca42b3fdd8
ms.lasthandoff: 03/31/2017


---

# <a name="organize-your-workforce-using-departments-jobs-and-positions"></a>Organisere dine medarbejdere, ved hjælp af afdelinger, job og stillinger

Afdelinger, job og stillinger er organisatoriske elementer, der vedligeholdes i Personale. Dette emne beskriver begrebsmæssige oplysninger om disse elementer. 

Følgende eksempel bruges til at illustrere de begreber, der er beskrevet i dette emne.

|**Afdeling**|**Position**|**Job**|
|---|---|---|
|**Salg**|Salgschef (øst)|Salgsdirektør|
|**Salg**|Salgschef (vest)|Salgsdirektør|
|**Salg**|Salgschef (centralt)|Salgsdirektør|
|**Accounting**|Regnskabsansvarlig|Regnskabschef|
|**Accounting**|Regnskab-A|Bogholder|
|**Human resources**|Personalechef (øst)|Personalechef|
|**Human resources**|Personalechef (vest)|Personalechef|
|**Human resources**|Personalechef (centralt)|Personalechef|

 
 <a name="departments"></a>Afdelinger
------------

En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation, der er ansvarlig for et bestemt område af organisationen, f.eks. salg eller regnskab. En afdeling bruges til at rapportere om funktionsområder og kan have driftsansvar. En afdeling kan også omfatte en gruppe af bærere. Salgs-, regnskabs- og personaleressourcer er nogle eksempler på afdelinger i en organisation.

## <a name="jobs-and-positions"></a>Job og stillinger
Et job er en samling opgaver og ansvarsområder, der kræves af en person, der udfører et job. En stilling er en individuel forekomst af et job. Ansvarsområder, jobopgaver, jobfunktioner, færdigheder, oplysninger om uddannelse og certifikater, der kræves for et job er også påkrævet for stillinger, der er tilknyttet et job.
### <a name="job-tasks"></a>Arbejdsopgaver

Du kan oprette jobopgaver, der beskriver de grundlæggende opgaver, der skal udføres af en arbejder i en position for det pågældende job. Samme arbejdsopgave kan føjes til flere job, og stillinger for disse job arver disse opgaver. Der vises eksempler på jobopgaver i følgende tabel.

<table>
<thead>
<tr class="header">
<th>Stilling</th>
<th>Arbejdsopgave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Salgsdirektør</td>
<td><ul>
<li><span class="input">Performance-gennemgang</span> – Gennemgang af en sælgers jobperformance.</li>
<li><span class="input">Fraværsgennemgang</span> – Godkend eller afvis en sælgers fraværsanmodninger eller registreringer.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bogholder</td>
<td><span class="input">Regnskabsrapport</span> – Forelæg ugentlige regnskaber til regnskabsdirektøren.</td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a>Jobfunktioner

Jobfunktioner er som arbejdsopgaver. En jobfunktion beskriver en eller flere opgaver, pligter eller ansvarsområder, der er tildelt til et job. Jobfunktioner kan tildeles job og bruges til at konfigurere og implementere berettigelsesregler for lønstrukturer. I følgende tabel vises eksempler på jobfunktioner.

| Stilling           | Jobfunktion                                                |
|---------------|-------------------------------------------------------------|
| Salgsdirektør | MNG personer – Administrer personer, der rapporterer til dig.               |
| Bogholder    | Regnskabsgennemgang – Vedligehold økonomiske data for et sæt regnskaber. |

### <a name="job-types"></a>Jobtyper

Du kan bruge jobtyper til at klassificere lignende job i kategorier. Jobtyper kan ligesom jobfunktioner tildeles job og bruges til at konfigurere og implementere berettigelsesregler for lønstrukturer. Nedenstående liste indeholder eksempler på jobtyper:
-   Fuld tid
-   Deltid
-   Månedsløn
-   Timeløn

### <a name="areas-of-responsibility"></a>Ansvarsområder

Brug ansvarsområder til at angive arbejdsroller, processer, og produkter, som en arbejder i en stilling for det pågældende job ville være ansvarlig for. Et eksempel på et ansvarsområde for et job med titlen "Bogholder" kunne være "Finansiel rapportering for vare A".

<a name="positions"></a>Stillinger
----------

Stillinger er et vigtigt element i et organisationshierarkis lavere niveau. En stilling er en individuel forekomst af et job. For eksempel er stillingen, "Salgschef (øst)," blot én af de stillinger, der er tilknyttet jobbet, "Salgschef". Stillinger, der findes i en afdeling og tildeles til arbejdere.
### <a name="position-creation-and-maintenance"></a>Oprette og vedligeholde stillinger

-   Du kan få vist en oversigt over stillingsrelaterede systemændringer på en listeside.
-   Du kan oprette årsagskoder, som brugerne kan vælge, når de opretter eller ændrer stillinger.
-   Du kan oprette personaleaktionstyper og tildele en nummerserie til personalehandlinger.
-   Du kan oprette arbejdsprocessen, så tilføjelser og ændringer i stillinger kan kræve godkendelse.

### <a name="position-duration"></a>Stillings varighed

Alle stillinger har en tidsperiode, hvor stillingen er gældende. Dette tidsrum kaldes varighed. Sommerjob har muligvis en varighed fra d. 1 maj 2015 indtil d. 31. august 2015.

### <a name="worker-assignments"></a>Medarbejdertildelinger

Når du tildeler en medarbejder til en stilling, udfylder du stillingen. Du kan tildele arbejdere til flere stillinger, men kun én arbejder kan tildeles en stilling ad gangen.

### <a name="reporting-relationships"></a>Rapporteringsrelationer

Stillinger er vigtige elementer i et organisationshierarkis lavere niveau. I formen Stilling kan du angive den stilling, en stilling rapporterer til. Når du tildeler en medarbejder til en stilling, der refererer til en anden stilling, opretter du en rapporteringsrelation mellem de arbejdere, der er tildelt til to stillinger. For eksempel rapporterer stillingen "Bogholder-A" til stillingen "Regnskabsansvarlig". Kim Akers er tildelt stillingen "Regnskabsansvarlig", og Sanjay Patel er tildelt stillingen "Bogholder-A". Det betyder, at Sanjay Patel rapporter til Kim Akers. 

Hvis organisationen bruger et matrixhierarki eller et andet brugerdefineret hierarki, kan du konfigurere stillingshierarkityper og derefter tilføje rapporteringsforhold for hver enkelt hierarki, du har angivet. Lori Penor er f.eks. administrerende direktør hos Eventyrcykler og er tildelt stillingen "Adm. direktør". Lori styrer udviklingen af et produkt, der bruges til at rense dimser. Lori har brug for, at en bogholde hjælper hende med økonomi til udvikling af produktet. Derfor har hun ansat Sanjay Patel sin bogholder. Sanjay rapporterer direkte til Kim Akers, men samarbejder også med Lori Penor med regnskabsopgaver til udvikling af renseanordningen. 

Du ville skulle udføre følgende opgaver for at konfigurere samarbejdsforhold mellem Sanjay Patel og Lori Penor i det forrige eksempel:
1.  Opret en brugerdefineret stillingshierarkitype kaldes "Dims" for at oprette et hierarki, der omfatter stillinger, der er ansvarlig for at arbejde på rensningsproduktet.
2.  Tildele stillingen adm. direktør til at være den stilling, som Bogholder-A-stillingen rapporterer til i Dims-hierarkiet.

Brug stillingshierarkiet til at se rapporteringsstrukturen for stillinger. Hvis du har flere stillingshierarkier, kan du se hierarkiet for hver enkelt hierarkitype i stillingshierarkiet. Desuden kan du søge efter en stilling efter stillings-id eller efter navnet på den arbejder, der er tildelt stillingen. Stillingshierarkiet er et organisationshierarki.

## <a name="date-effective-records"></a>Poster for gældende dato
For nogle poster kan du angive fremtidige ændringer i posten. Følgende oplysninger er for ikrafttrædelsesdatoen.

<table>
<thead>
<tr class="header">
<th>Poster</th>
<th>Oplysninger om ikrafttrædelsesdato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Job</td>
<td><ul>
<li>Detaljerede joboplysninger</li>
<li>Oplysninger om jobklassificering</li>
<li>Lønoplysninger</li>
</ul></td>
</tr>
<tr class="even">
<td>Stillinger</td>
<td><ul>
<li>Detaljerede stillingsoplysninger</li>
<li>Arbejdertildelinger</li>
<li>Stillingers varighed</li>
<li>Stillingshierarkier</li>
</ul></td>
</tr>
</tbody>
</table>

Du kan ændre de oplysninger, der er nævnt i den foregående tabel for en stilling eller et job og angive en dato, hvor ændringer til stillingen eller jobbet skal træde i kraft. For eksempel kan en stilling kun tildeles én arbejder, men Sanjay Patel, der er tildelt stillingen Bogholder-A, forlader jobbet om to uger. Joe Healy erstatter Sanjay Patel, når han rejser. Selvom Sanjay stadig er knyttet til hans stilling, kan du tildele Joe Healy til samme stilling, så tildelingen træder i kraft efter Sanjays sidste dag på jobbet.




