---
title: Parametre til aktivstyring
description: I aktivstyring skal der oprettes generelle parametre vedrørende aktiver, arbejdsordrer og planlægning af arbejdsordrer.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3336a3357578b25522e1ac457a48349f88b7318d
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024562"
---
# <a name="asset-management-parameters"></a>Parametre til aktivstyring

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I aktivstyring skal der oprettes generelle parametre vedrørende aktiver, arbejdsordrer og planlægning af arbejdsordrer. Dette emne forklarer, hvordan du konfigurerer dem. Vælg **Styring af aktiver** > **Opsætning** > **Parametre til aktivstyring** for at åbne formen.

Knappen **Guiden Opret data** kan bruges til automatisk at oprette opsætningsdata til test- eller demodataformål i et firma i Dynamics 365 Supply Chain Management. Se hvidbogen "Konfigurere testdata i aktivstyring" for at få oplysninger om, hvordan du bruger guiden.

**Aktiver**-link

- **Standardarbejdssted** er det standardarbejdssted, som automatisk vælges på aktiver, når du opretter nye aktiver.  
- I feltet **Standardkalender** skal du vælge en kalender, der skal bruges til beregning af KPI'er for aktiver, hvis der ikke er valgt en ressource for et aktiv.  
- I feltet **Vis** skal du vælge den standardvisning, der vises, når du åbner formen **Aktivvisning** (**Styring af aktiver** > **Almindeligt** > **Aktiver** > **Aktivvisning**).
- **Standardanmodningstype** er standardtypen for vedligeholdelsesanmodning, som vælges automatisk, når du opretter en ny anmodning.  
- Hvis du vil oprette projekter, der relaterer til aktiver, oprettes projektrelationer vedrørende valg af **Hovedprojekt**, **Projekthierarki** og indstillingen til **Automatisk oprettelse af projekter** i **Parametre til aktivstyring**.  
- I feltet **Projekt maske for arbejdsordre** definerer du antallet af underordnede projekter, som er tilladt for arbejdsordrer og underaktiver. En arbejdsordremaske bruges til at definere, hvor mange arbejdsordrer der kan oprettes på et aktiv og bruges i det relaterede arbejdsordreprojekt. Arbejdsordremasken konfigureres i feltet **Relateret arbejdsordremaske** i **Parametre til aktivstyring** (**Styring af aktiver** > **Opsætning** > **Parametre til aktivstyring** > **Arbejdsordrer**).  
>[!NOTE]
>Formatet for en relateret arbejdsordremaske er et antal nummertegn (#), afhængigt af det maksimale antal arbejdsordrer, du forventer at oprette på et aktiv. Eksempel: ## giver dig mulighed for at oprette op til 99 underprojekter.  
- Budgetter for jobtyper gemmes på det projekt, der er valgt i feltet **Budgetprojekt**. For hver jobtype oprettes der automatisk en ny aktivitet på budgetprojektet. Budgetter for jobtypen gemmes derefter i budgetprojektet.  
- I feltet **Model** skal du vælge den budgetmodel, der bruges på jobtype- og arbejdsordrebudgetter.  


**Arbejdsordrer**-link

- **Standardarbejdsordretype** definerer standardindstillinger, når der oprettes en arbejdsordre.  
- **Forebyggende arbejdsordretype** definerer den arbejdsordretype, der bruges ved oprettelse af arbejdsordrer ud fra vedligeholdelsesplaner. Hvis feltet ikke udfyldes, bruges arbejdsordretypen i feltet **Standardarbejdsordretype**.  
- I feltet **Relateret arbejdsordremaske** definerer du det maksimale antal arbejdsordrer, der kan relateres til en arbejdsordre. Eksempel: ## giver dig mulighed for at have op til 99 relaterede arbejdsordrer. Hvis du definerer en maske som beskrevet her, nummereres relaterede arbejdsordrer [arbejdsordre-id for den arbejdsordre, som en arbejdsordre er relateret til] -01, -02, -03 osv. Hvis du ikke definerer en maske i dette felt, får en relateret arbejdsordre det næste sekventielle arbejdsordre-id.  
- Vælg "Ja" på til/fra-knappen **Kopiér fejl**, hvis du automatisk vil kopiere fejl, der er registreret på arbejdsordrer, til relaterede vedligeholdelsesanmodninger.  
- I feltet **Niveau** skal du definere det arbejdsstedsniveau, der automatisk indsættes på en arbejdsordre, hvis alle relaterede arbejdsordrejob refererer til det samme arbejdssted. Hvis arbejdsordrens job ikke alle er relateret til det samme arbejdssted på det definerede niveau, er feltet **Arbejdssted** tomt i arbejdsordren. Eksempel: Hvis du indsætter tallet "1" i dette felt, er det øverste niveau i en arbejdsstedsstruktur. Hvis du indsætter tallet "0" i dette felt, har du ikke defineret et bestemt arbejdsstedsniveau, kun at alle arbejdsordrejob på en arbejdsordre skal relateres til det samme arbejdssted, for at dette arbejdssted kan føjes til arbejdsordren.  
- Kladder, der bruges ved bogføring af forbrug på en arbejdsordre, kan vælges i oversigtspanelet **Generelt** i felterne **Time**, **Vare** og **Udgift**.  
- I feltet **Produktsprogkilde** skal du vælge, hvilket sprog der skal bruges til produktnavne i Styring af aktiver-rapporter. Du kan vælge det sprog, der er angivet på firmakontoen, eller det sprog, der er angivet for den bruger, som aktuelt er logget på.  
- Vælg "Ja" på til/fra-knappen **Realtidsopdatering** , hvis du automatisk vil opdatere ændringer af jobtypestandarder, vedligeholdelsesplaner og vedligeholdelsesrunder.
> - Hvis du vælger "Nej", opdateres ændringer i jobtypestandarder, vedligeholdelsesplaner og vedligeholdelsesrunder ikke automatisk i Styring af aktiver.  
> - Vælg "Nej" på til/fra-knappen, hvis du har store mængder data, der synkroniseres, for eksempel mange aktiver eller arbejdssteder, der er konfigureret på vedligeholdelsesplaner eller vedligeholdelsesrunder, eller et stort antal vedligeholdelsesplaner eller -runder.  
> - Hvis du foretager ændringer af jobtypestandarder eller vedligeholdelsesplaner eller vedligeholdelsesrunder, og du har valgt "Nej" til realtidsopdatering, vises der muligvis ikke en advarsel, hvis ændringerne påvirker:
>   - arbejdssteder, der er oprettet på vedligeholdelsesplaner eller -runder  
>   - objekter, der er oprettet på vedligeholdelsesplaner eller -runder  
>   - opsætning af vedligeholdelsesplaner  
>   - opsætning af vedligeholdelsesrunder  
- I oversigtspanelet **Kategori** kan du definere standardkategorier vedrørende forbrug på arbejdsordrer.  


**Lægning af arbejdsordre**-link

- **Planlæg tidshorisont** definerer periode i dage, beregnet ud fra den forventede startdato for arbejdsordren, hvor arbejdsordrens job er planlagt.  
- **Behovsplanen** relaterer til ressourcer i modulet **Organisationsadministration**. Hvis du vælger en behovsplan i dette felt, kan du se kapacitetsreservationer, der er relateret til arbejdsordrer, i **Kapacitetsreservationer** (**Virksomhedsadministration** > **Ressourcer** > **Ressourcer** > vælg ressource > fanen **Ressource** > knappen **Kapacitetsreservationer**). Hvis du lader feltet være tomt, kan du se den kapacitetsbelastning, der er relateret til arbejdsordrer, i **Kapacitetsbelastning** (**Virksomhedsadministration** \> **Ressourcer** \> **Ressourcer** \> vælg ressource \> **Ressource**-fanen \> **Kapacitetsbelastning**-knappen).  

>[!NOTE]
>Valget vedrørende brug af en behovsplan eller ej i modulet **Styring af aktiver** og den relaterede form, der bruges til at få en oversigt over kapacitetsreservationer eller kapacitetsbelastning er standardopsætningen. Afhængigt af opsætningen i feltet **Behovsplan** vil du kunne få adgang til kapacitetsoplysninger i enten **Kapacitetsreservationer** eller **Kapacitetsbelastning** i **Virksomhedsadministration**-modulet. Det er ikke muligt at oprette en opsætning, hvor kapacitetsreservationer kan ses i begge visninger.  

De felter, der er beskrevet i punktopstillingen nedenfor, relaterer alle til beregnede rangeringsscorer, som bruges til at beregne arbejdsordrens prioritet under planlægningen af arbejdsordren.

- **Prioritet** - en rangeringsscore beregnet sammen med rangeringsscoren i felterne **Kritikalitet** og **Startdato**. Tallet i dette felt divideres med tallet i feltet **Prioritet** på en arbejdsordre. Eksempel: Hvis værdien "5,00" er indsat i dette felt, og en arbejdsordre har prioritet "20", er rangeringsscoren for prioritet 0,25.  
- **Kritikalitet** - en rangeringsscore beregnet sammen med rangeringsscoren i felterne **Prioritet** og **Startdato**. Tallet i dette felt multipliceres med tallet i feltet **Kritikalitet** på en arbejdsordre. Eksempel: Hvis værdien "10,00" er indsat i dette felt, og en arbejdsordre har kritikalitet "5", er rangeringsscoren for kritikalitet 50.  
- **Startdato** - en rangeringsscore beregnet sammen med rangeringsscoren i felterne **Prioritet** og **Kritikalitet**. Dette felt angiver det daglige resultat som en negativ værdi og sammenlignes med feltet **Forventet start** på en arbejdsordre. Eksempel: Hvis værdien "10,00" er indsat i dette felt, og den forventede startdato for en arbejdsordre er tre dage fra nu, er rangeringsscoren minus 30,00. Addering af resultaterne fra 0,25 og 50 fra eksemplerne i felterne **Prioritet** og **Kritikalitet** beskrevet ovenfor giver en total af plus 20,25. Dette tal sammenlignes med alle andre rangeringsscorer for arbejdsordrer under planlægning af arbejdsordrer, og de højeste rangeringsscorer planlægges derefter først.  
- **Ansvarlig arbejder** - en rangeringsscore beregnet sammen med rangeringsscoreværdierne af **Ansvarlig arbejdergruppe**, **Foretrukken arbejder**, **Foretrukken arbejdergruppe**, **Aktivlokation** og **Startdato**. Hvis værdien "50,00" er indsat i dette felt, og der er valgt en ansvarlig arbejder på en arbejdsordre, får arbejderen 50 point i den overordnede arbejderberegning under planlægning af arbejdsordre.  
- **Ansvarlig arbejdergruppe** - en rangeringsscore beregnet sammen med rangeringsscoreværdierne af **Ansvarlig arbejder**, **Foretrukken arbejder**, **Foretrukken arbejdergruppe**, **Aktivlokation** og **Startdato**. Hvis værdien "50,00" er indsat i dette felt, og der er valgt en ansvarlig arbejder på en arbejdsordre, får arbejderen 50 point i den overordnede arbejderberegning under planlægning af arbejdsordre.  
- Ja/Nej-knappen **Begræns til ansvarlig** begrænser antallet af arbejdere, der er tilgængelige for planlægning af arbejdsordre. Vælg "Nej", hvis du vil beregne en score for alle arbejdere, uanset om de er oprettet som ansvarlige arbejdere eller en del af en ansvarlig arbejdergruppe. Vælg "Ja", hvis du vil beregne en score for arbejdere, der er oprettet som ansvarlig arbejder på arbejdsordren og/eller medtaget i en ansvarlig arbejdsgruppe, som er valgt i arbejdsordren.  
- **Foretrukken arbejder** - en rangeringsscore beregnet sammen med rangeringsscoreværdierne af **Ansvarlig arbejder**, **Foretrukken arbejder**, **Foretrukken arbejdergruppe**, **Aktivlokation** og **Startdato**. De fire rangeringsscorer beregnes og lægges sammen for at give en score, der bruges til at vælge, hvilken arbejder der skal tildeles hvilken arbejdsordre under planlægning af arbejdsordren. Hvis værdien "10,00" er indsat i dette felt, og der er valgt en foretrukken arbejder på en arbejdsordre, får arbejderen 10 point i den overordnede arbejderberegning under planlægning af arbejdsordre.  
- **Foretrukken arbejdergruppe** - en rangeringsscore beregnet sammen med rangeringsscoreværdierne af **Ansvarlig arbejder**, **Foretrukken arbejder**, **Foretrukken arbejdergruppe**, **Aktivlokation** og **Startdato**. Hvis værdien "10,00" er indsat i dette felt, og en arbejder er tildelt en foretrukken arbejdergruppe, der er valgt på en arbejdsordre, får arbejderen 10 point i den overordnede arbejderberegning under planlægning af arbejdsordre.  
- Ja/Nej-knappen **Begræns til foretrukken** begrænser antallet af arbejdere, der er tilgængelige for planlægning af arbejdsordre. Vælg "Nej", hvis du vil beregne en score for alle arbejdere, uanset om de er oprettet som foretrukne arbejdere eller en del af en foretrukken arbejdergruppe. Vælg "Ja", hvis du kun vil beregne en score for arbejdere, som er oprettet som foretrukne arbejdere og/eller en del af en foretrukken arbejdergruppe.  
- **Sted** - en rangeringsscore beregnet sammen med rangeringsscoreværdierne af **Ansvarlig arbejder**, **Foretrukken arbejder**, **Foretrukken arbejdergruppe**, **Aktivlokation** og **Startdato**. Hvis værdien "3.000,00" er indsat i dette felt, får en arbejder 3.000 point i beregningen, hvis arbejderen er i samme fabrik eller facilitet som det aktiv, som et job skal planlægges på.  

  - Hvis din virksomhed bruger arbejdssteder, får medarbejderne fuld score, hvis de er på det arbejdssted, der er relateret til aktivet. Hvis aktivets arbejdssted har et overordnet aktiv, får arbejdere på det pågældende arbejdssted 1/2 score. Hvis dette sted også har et overordnet sted, vil arbejdere på dette sted få 1/3 score. Hvis dette sted også har et overordnet sted, vil arbejdere på dette sted få 1/4 score osv.  
  - Hvis dit firma bruger aktivlokation, hvilket vi fraråder, bruges lokation, område og zone til at beregne lokationsscore. Arbejdere får fuld score, hvis de er placeret i lokationen og området og zonen, der er relateret til aktivet. Hvis arbejderens lokation kun svarer til lokation og område, er rangeringsscoren for arbejderen 2/3 af den fulde score. Hvis arbejderens lokation kun svarer til lokation, er rangeringsscoren for arbejderen 1/3 af den fulde score.  

- Ja/Nej-knappen **Begræns til sted** begrænser antallet af arbejdere, der er tilgængelige for planlægning af arbejdsordre. Vælg "Nej", hvis du vil beregne en score for alle arbejdere på tværs af alle arbejdssteder. Vælg "Ja", hvis du kun vil beregne en score for arbejdere, der er tilknyttet arbejdsordrens arbejdssted.

>[!NOTE]
>De tre til/fra-knapper "Begræns til..." introduceres for at øge hastigheden af arbejdsordreplanlægning ved at begrænse antallet af scorer, der beregnes for arbejdere.

**Startdato for medarbejder** - en rangeringsscore beregnet sammen med rangeringsscoreværdierne af **Ansvarlig arbejder**, **Foretrukken arbejder**, **Foretrukken arbejdergruppe**, **Aktivlokation** og **Startdato**. Dette felt angiver det daglige resultat som en negativ værdi og sammenlignes med feltet **Forventet start** på en arbejdsordre. Hvis værdien "10,00" er indsat i dette felt, og den forventede startdato for en arbejdsordre er i morgen, er rangeringsscoren minus 10,00.

  - Hvis det antages, at der ikke er valgt en ansvarlig arbejder og en ansvarlig arbejdergruppe på en arbejdsordre, der skal planlægges, og du adderer og subtraherer overstående eksempelværdier af **Foretrukken arbejder**, **Foretrukken arbejdergruppe**, **Aktivplacering**og **Startdato**, får du i alt 3.010,00. Det betyder en høj score for den arbejder, der allerede er valgt som foretrukken arbejder, og som er medtaget i den foretrukne arbejdergruppe på arbejdsordren, og arbejderen er også placeret i samme facilitet som det aktiv, som et job skal planlægges for. Alt i alt betyder det, at der er en god chance for, at den pågældende arbejder vil blive valgt til at fuldføre jobbet under arbejdsordreplanlægning.  
  - Hvis værdien "0,00" er indsat i et af de otte felter ovenfor, vil rangeringsscoren ikke blive brugt under planlægningen af arbejdsordren.  


**Dokumenttyper**-link

Vælg de dokumenttyper, der skal være tilgængelige for udskrivning af vedhæftede filer i forbindelse med en arbejdsordrerapport. Dette gøres ved at klikke på en dokumenttype i sektionen **Tilgængelig** og klikke på knappen ![fremadrettet pil](media/15-setup-for-objects.png). Hvis du vil fjerne en valgt dokumenttype, skal du vælge dokumenttypen i sektionen **Valgt** og klikke på knappen ![tilbage-pil](media/16-setup-for-objects.png).



**Nummerserier**-link

Vælg de påkrævede nummerserier i dette afsnit. Der er to nummerserier for aktiver: én for manuelt oprettede aktiver og én for aktiver, som er oprettet via ventende aktiver.
