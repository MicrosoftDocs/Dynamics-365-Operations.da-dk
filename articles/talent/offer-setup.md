---
title: Konfigurere tilbudsstyring
description: I dette emne beskrives, hvordan du kan konfigurere tilbud i Talent.
author: josaw
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa6c8c80870dd7bd06498c7571ba8a110be85c86
ms.sourcegitcommit: 3b12ff5ca81650ae666ff443b0bc998182f3931e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2019
ms.locfileid: "376501"
---
# <a name="set-up-offer-management"></a>Konfigurere tilbudsstyring 

[!include [banner](includes/banner.md)]

Når en kandidat overgår til tilbudsstadiet i Dynamics 365 for Talent: Attract, skal du sikre dig, at der hurtigt kan oprettes tilbud til kandidaten, at de kan godkendes efter behov og sendes til kandidaten. Da de fleste tilbud er standard, kan de oprettes fra genanvendelige skabeloner. I Attract er alle tilbud samlet i en tilbudspakke, der er en samling af et eller flere tilbudsdokumenter. 

I dette emne beskrives de trin, som Attract-administratorer skal følge for at konfigurere forskellige tilbudspakkeskabeloner som en del af tilbudsstyringsfunktionerne i Attract. Brugere med ikke-administrator roller har ikke adgang til disse funktioner.

>[!NOTE]
> Tilbudsstyringsfunktioner er tilgængelige som en del af tilføjelsesprogrammet til omfattende ansættelser.

## <a name="offer-data"></a>Tilbudsdata 

Tilbudsdata er den mindste enhed i tilbudspakkeskabelonen. Et typisk tilbud består af standardtekst og et sæt værdier. Værdisættene er de eneste enheder, der kan skifte fra tilbud til tilbud. Under oprettelsen af tilbuddet er det vigtigste aspekt, som den, der har oprettet tilbuddet, kan fokusere på, listen over pladsholderefor tilbudsdata, som findes i en tilbudspakkeskabelon. Du kan angive tilbudsdata ved at gøre følgende:

1.  Gå til **Tilbudsstyring**.

1.  Udvid sektionen **Bibliotek** i den venstre navigationsrude, og gå derefter til **Tilbudsdata**.

    >[!NOTE]
    > På siden **Tilbudsdata** finder du sektionerne **Detaljer om kandidat** og **Jobdetaljer**. Attract indeholder som standard nogle tilbudsdatapladsholdere.
    
    > Der er sektioner på siden, hvor du kan organisere forskellige tilbudsdatapladsholdere i logiske grupper. Disse sektioner kan hjælpe med vedligeholdelse af tilbudsdata og udfyldning af data under oprettelsen af tilbuddet.

1.  Hvis du vil oprette en ny sektion med tilbudsdata, skal du klikke på **Tilføj en sektion** og angive et entydigt navn til sektionen.

1.  Hvis du vil tilføje tilbudsdatapladsholdere i en bestemt sektion, skal du klikke på **Tilføj tilbudsdata** og angive et entydigt navn til pladsholderen.

1.  Hvis du vil redigere navnet på en sektion, skal du pege på navnet på sektionen og opdatere navnet.

1.  Hvis du vil redigere navnet på en eksisterende tilbudsdatapladsholder, skal du først sikre dig, at pladsholderen ikke allerede er en del af en skabelon. Derefter skal du pege på navnet på tilbudsdatapladsholderen og opdatere navnet efter behov.

1. Hvis du vil slette en eksisterende tilbudsdatapladsholder, skal du først sikre dig, at pladsholderen ikke er en del af en anden skabelon. Derefter skal du pege på pladsholderen, og når ikonet Papirkurv vises, skal du klikke på papirkurven for at slette tilbudsdatapladsholderen.
    >[!NOTE]
    > Du kan se, hvor mange skabeloner en tilbudsdatapladsholder er en del af ved hjælp af antalsindikatoren ud for de enkelte tilbudsdata. 

1. Hvis du vil slette en sektion, skal du pege på navnet. Hvis ingen af tilbudsdatapladsholderne i sektionen vises i en skabelon, kan du klikke på ikonet for papirkurven for at slette den. 
    >[!NOTE]
    > Når du sletter sektionen, slettes også alle tilbudsdatapladsholdere i sektionen.

Når tilbudsdatapladsholderne er konfigureret, kan du bruge dem på tværs af alle dokumentskabeloner. Tilbudsdatapladsholdere er ikke begrænset til en bestemt skabelon – det samme sæt kan bruges på tværs af alle skabeloner.

## <a name="offer-data-rules"></a>Regler for tilbudsdata

De fleste organisationer har regler for, hvordan tilbud skal oprettes. En organisation kan f.eks. kræve, at den maksimale årsløn for en bestemt kombination af sted og anciennitetsniveau skal ligge inden for et bestemt interval, eller at der kun kan anvendes nogle få bestemte værdier for tilbudsniveauet i den nye stilling. Attract understøtter aktuelt alle sådanne dataregler ved hjælp af en CSV-fil.

Når du vil forberede CSV-filen med datareglerne, skal du gøre følgende:

1.  Bestem tilbudsdatapladsholderen for regelsættet. F.eks. **Årsløn**.

1.  Identificer de afhængige værdier for tilbudspladsholderdata. F.eks. **Placering af stilling** og **Niveau**.

1.  Angiv kolonne 1 og 2 som **Placering af stilling** og **Niveau**.

1.  Du kan overføre en værdi i intervallet ved at vælge **Årsløn** i kolonne 3 og 4. Du kan overføre en bestemt værdi i stedet for et interval ved kun at vælge **Årsløn** i kolonne 3.

1.  Angiv værdier i Microsoft Excel-filen ud fra de roller, du anvender.

1.  Sørg for, at hver række er en entydig kombination af alle de værdier, der er sat sammen.

1.  Gem filen i CSV-format.

Når du vil overføre filen med tilbudsdatareglerne, skal du gøre følgende.

1.  Gå til **Tilbudsstyring**.

1.  Udvid sektionen **Bibliotek** i det venstre navigationspanel, og gå derefter til **Regler for tilbudsdata**.

1.  Klik på **Nyt datasæt** for at åbne dialogboksen **Overfør**.

1.  Angiv et entydigt navn til regelsættet, og overfør derefter den gemte CSV-fil.

1.  Klik på **Tilføj**.
    Regelsættet behandles i baggrunden, og du får besked i app og via e-mail, når behandlingen er fuldført.

    Du får besked, hvis der opstår fejl under behandlingen af overførslen. Du kan derefter hente fejlloggen, rette filen og overføre den igen.

1.  Du kan bruge knappen (**...**), hvis du vil hente regelsættet og opdatere værdisættet. Når du har opdateret, kan du overføre filen igen.

1.  Du kan slette et eksisterende overført regelsæt, hvis den pladsholder, der defineres, ikke bruges i en anden dokumentskabelon.

>[!NOTE]
> - Hver enkelt pladsholder kan kun have ét entydigt sæt kolonner, som den er afhængig af. F.eks. hvis **Årsløn** er afhængig af **Placering af stilling** og **Niveau**, du kan ikke overføre et andet regelsæt, hvor **Årsløn** er afhængig af et andet sæt af kolonner.

> - Du kan hente eksempelregelsæt med tilbudsdata under fanen **Eksempler** på siden **Regler for tilbudsdata**.

> - Når den, der har oprettet et tilbud, tilsidesætter de værdier, der anbefales i tilbudsdatareglerne, markeres tilbuddet som ikke-standard, og arbejdsgangen for tilbudsgodkendelse gøres obligatorisk.

## <a name="document-templates"></a>Dokumentskabeloner

En tilbudsdokumentskabelon kan hjælpe administratorer oprette tilbudsbreve. Tilbudsdokumentskabelonen er en kombination af den tekst, der skal være en del af tilbuddet, samt de definerede tilbudsdatapladsholdere. 

Gør følgende for at oprette en tilbudsdokumentskabelon.

1.  Gå til **Tilbudsstyring**.

1.  Udvid sektionen **Bibliotek** i den venstre navigationsrude, og gå til **Skabeloner**.

    Siden **Skabeloner** indeholder en liste over de dokumentskabeloner, der er defineret.

1.  Klik på **Ny skabelon** for at oprette en ny dokumentskabelon.

1.  Angiv et entydigt navn til skabelonen, og klik på **Opret**.

1.  Du kan bruge RTF-editoren til at indsætte eller redigere tilbudsdokumentets indhold. Du kan indsætte tabeller, billeder og hyperlinks ved hjælp af de tilgængelige indstillinger øverst i teksteditoren.

1.  Du kan indsætte tilbudsdatapladsholdere i tilbudsskabelondokumentet ved at:

    - Trække og slippe fra højre rude.

    - Indsætte hashtag for tilbudsdatapladsholderen direkte på den ønskede placering. Skriv **\#**, og begynd at skrive navnet på tilbudsdatapladsholderen. Der vises indstillinger på rullelisten. Klik eller tryk på **Enter** for at indsætte tilbudsdatapladsholderen.

    >[!NOTE]
    > - Hvis du vil knytte en pladsholder til tilbudsdokumentskabelonen, uden at kandidaten kan se pladsholderværdien, skal du pege på tilbudsdatapladsholderen og klikke på ikonet **Fastgør**. Dette overfører pladsholderen til sektionen **Fastgjorte tilbudsdata** i tilbudsdokumentskabelonen. Du kan fjerne fastgørelsen ved at følge samme fremgangsmåde, men klikke på **Frigør** på listen over tilbudsdatapladsholdere.

    > - For at få vist listen over aktive tilbudsdatapladsholdere skal du skifte til fanen **Aktiv** i den højre rude.

    > - Hvis du indsætter en pladsholder, der styres af et regelsæt for tilbudsdata, kan du se tilbudsdatapladsholderens afhængighed af andre værdier.

    > - Alternativt kan vælge **Importér** for at importere indholdet fra en .docx-fil på din lokale computer og redigere den efter behov. På denne måde behøver du ikke at skrive i alt indhold i editoren.

1. Hvis du vil se tilbudsdokumentet formateret, kan du bruge indstillingen **Eksempel** øverst på siden.

1. Hvis du vil styre, om den, der opretter et tilbud, skal kunne redigere tilbudsdokumentets indhold, skal du bruge indstillingen **Administrer rettighed** øverst på siden. Hvis den, der har oprettet tilbuddet, kun skal kunne indsætte pladsholderværdier og ikke redigere tekst, skal du indstille rettighedsværdien til **Nej**.

1. Klik på **Gem** for at gemme ændringerne. Skabelonen gemmes i kladdetilstand.

1. Hvis du vil afslutte og markere dokumentet som publiceret, skal du klikke på **Afslut**.

1. Du kan se, hvilke dokumentskabeloner der er aktive, i kladdetilstand og er arkiveret og ikke længere i brug på dokumentskabelonbibliotekets landingsside.

>[!NOTE]
> Du kan slette alle tilbudsdokumentskabeloner, der ikke er en del af en eksisterende tilbudspakkeskabelon.


## <a name="offer-package-templates"></a>Skabeloner til tilbudspakker

Tilbudspakker er de tilbudselementer, der deles med kandidaten. De består af en kombination af en eller flere tilbudsdokumentskabeloner. Gør følgende for at oprette en tilbudspakke.

1.  Gå til **Tilbudsstyring**.

1.  Gå til **Pakker** fra den venstre navigationsrude.

    Der vises en liste over aktive pakkeskabeloner, der er tilgængelige for personer, der vil oprette tilbud.

1.  Hvis du vil oprette en ny tilbudspakke, skal du klikke på **Ny pakke**.

1.  Angiv et entydigt navn, og klik på **Opret**.

1.  Klik på **Tilføj skabelon**.

    >[!NOTE]
    > - Du kan vælge at oprette en ny skabelon eller vælge fra en eksisterende.

    > - Hvis du vil tilføje en eksisterende skabelon, skal du kontrollere, at tilbudsdokumentskabelonen er gemt, færdiggjort og markeret som aktiv.
    
    > - Du kan vælge lige så mange dokumentskabeloner, som du vil. 
    
1.  Klik på **Udført** for at vende tilbage til **Pakkestyring**.

    Du kan konfigurere rækkefølgen af dokumenterne, og du kan også angive, om der kræves bestemte tilbudsdokumenter under oprettelsen af tilbuddet. Den, der opretter tilbuddet, får mulighed for at slette de dokumenter, der er markeret som **Kræves ikke**.

1. Hvis du vil gemme tilbudspakkeskabelonen, så den kan bruges af alle, der opretter tilbud, skal du klikke på **Gem og udgiv**.

   Du kan se udkast til tilbudspakkeskabeloner ved at gå til fanen **Kladder**. Hvis der foretages en ændring af tilbudspakkeskabelonen, skal den gemmes og udgives igen.

## <a name="configure-an-offer-process"></a>Konfigurere en tilbudsproces

Der er flere dele af tilbudsoprettelsesprocessen, som kan konfigureres af en Attract-administrator.

- **Godkendelser af tilbud** - Vælg, om der skal kræves godkendelser af et tilbud, før det kan sendes til kandidaten. Som administrator kan du også bestemme, om alle tilbudsgodkendelser skal ske fortløbende eller i en parallel godkendelsesproces. Du kan også bestemme, om godkendere af tilbuddet skal tilføje en kommentar sammen med deres tilbudsgodkendelse. Tilbudsgodkendelser er obligatoriske for alle ikke-standard tilbud.

- **Kandidatens tilbudsoplevelse** - Som administrator kan du vælge at angive, om alle tilbud skal have en udløbsdato, og i så fald hvad udløbsdatoens forskydning skal være som standard. Du kan også konfigurere, om kandidater kan vælge at afvise et tilbud.

- **e-signaturer** - Som administrator kan du også vælge den metode, som ansøgerne kan bruge til at signere tilbud.
    - Adobe Sign - Alle tilbudspakker sendes og signeres via Adobe Sign. For den, der opretter tilbuddet, skal have Adobe Sign-licensen være tilknyttet Attract. 

    - ESign - Dette er standardindstillingen, der leveres som standard, hvor brugeren kan signere et tilbud ved at skrive sit navn og sine initialer.

>[!NOTE]
> For Adobe Sign-licenser og en gratis prøveversion skal du på dette [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).

Hvis du vil vide mere om oprettelsen af tilbuddet, kan du se under [Oprettelse, godkendelse og signering af tilbud](./creating-offers.md).
