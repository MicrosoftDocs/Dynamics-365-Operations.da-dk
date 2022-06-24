---
title: Vælge mellem Store Commerce og Cloud POS
description: Denne artikel forklarer de vigtigste forskelle mellem Store Commerce og Cloud POS og beskriver de forskellige faktorer, som detailhandlere, der implementerer Dynamics 365 Commerce, bør hjælpe dem med at træffe de bedste valg i forhold til deres behov.
author: jblucher
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26f6e94b13b3058ac42c4c7b83dcf7179bae18e3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854000"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Vælge mellem Store Commerce og Cloud POS

[!include [banner](includes/banner.md)]

Denne artikel forklarer de vigtigste forskelle mellem Store Commerce og Cloud POS og beskriver de forskellige faktorer, som detailhandlere, der implementerer Dynamics 365 Commerce, bør hjælpe dem med at træffe de bedste valg i forhold til deres behov. Det giver også implementeringskonsulenter yderligere baggrund, tip og vejledning til de faktorer, som de skal overveje, når de installerer Dynamics 365 Commerce. Ved at gennemse og følge denne vejledning som en del af installationsprocessen kan implementeringskonsulenter undgå problemer, der kan påvirke brugertilfredsheden eller ydeevnen.

## <a name="insights"></a>Indsigt

Commerce indeholder en lang række installations- og topologiindstillinger. Detailhandlere kan derfor vælge de komponenter og den konfiguration, der bedst opfylder deres forretnings- og teknologikrav. Et aspekt af implementering, der kræver nøje overvejelser, er valget af en platform og formfaktor til POS-komponenten.

### <a name="pos-platform-and-form-factor-considerations"></a>Overvejelser i forbindelse med POS-platform og formfaktor

Commerce understøtter følgende POS-indstillinger:

- Store Commerce til Microsoft Windows
- Store Commerce til iOS og Android
- Cloud POS (CPOS), som understøtter Microsoft Edge- og Google Chrome-browsere
- Moderne POS (MPOS) til Microsoft Windows (MPOS udfases i oktober 2023.) 

I alle tilfælde deler POS (Store Commerce and CPOS) samme kerneprogramkode. Dette er vigtigt af følgende årsager:

- Brugergrænsefladen (UI) er ensartet på tværs af platformen eller formfaktoren.
- De fleste af de funktionelle egenskaber er de samme, uanset platform eller formfaktor. Der er dog nogle vigtige forskelle. Disse forskelle er anført i denne artikel.
- I hver butik kan POS-variationerne kombineres og kan køre samtidigt. For eksempel kan en forhandler til sine overordnede kasseapparater bruge Store Commerce på computere, der kører Windows. Forhandleren kan imidlertid supplere disse kasseapparater med browserbaserede terminaler eller mobilenheder.
- Tilpasninger og udvidelser kan nemt bruges på tværs af platforme og formfaktorer. Da kerneprogramkoden er delt, kan de fleste tilpasninger implementeres én gang i stedet for flere gange.

### <a name="store-commerce-vs-cpos"></a>Store Commerce vs. CPOS

Selvom Store Commerce og CPOS stort set er ens, er der nogle vigtige forskelle, som du skal kende.

#### <a name="store-commerce"></a>Store Commerce

Store Commerce er et skrivebordsprogram, der er installeret og serviceret på en enhed.

- **Windows** – Store Commerce for Windows-programmet indeholder al programkode, Commerce Runtime (CRT) og Hardware Station (HWS).
- **iOS/Android** – På disse platforme fungerer programmet som vært for CPOS-programkoden. Med andre ord kommer programkoden fra CPOS-serveren, der hostes på Commerce Scale Unit. Du kan finde flere oplysninger i [Oversigt over Commerce Scale Unit](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Da CPOS kører i en browser, bliver programmet ikke installeret på enheden. I stedet får browseren adgang til programkoden fra CPOS-serveren. Derfor kan CPOS ikke få direkte adgang til POS-hardware eller arbejde i offlinetilstand.

### <a name="store-deployment-considerations"></a>Overvejelser om installation i butik

Ud over en platform og formfaktor skal detailhandlere også vælge en implementeringsindstilling i butikken. I følgende tabel vises de konfigurationer, der er tilgængelige for hver POS-indstilling.

| POS-program            | Commerce Scale Unit | Tilgængelig offline | Lokal HWS-understøttelse |
|----------------------------|---------------------|-------------------|-------------------|
| Store Commerce til Windows | Cloud eller RSSU       | Ja               | Ja               |
| Store Commerce til Android | Cloud eller RSSU       | Nej                | Ja               |
| Store Commerce til iOS     | Cloud eller RSSU       | Nej                | Nej                |
| Cloud POS                  | Cloud eller RSSU       | Nej                | Nej                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce Scale Unit er en komponent, der er vært for CRT. CRT indeholder al forretningslogik, som POS bruger, og giver adgang til kanaldatabasen. Mens de er online, kan alle POS-klienter i butikken bruge Commerce Scale Unit. Commerce Scale Unit kan implementeres enten i skyen eller i butikken.

#### <a name="offline-mode"></a>Offlinetilstand

Store Commerce til Windows understøtter offline-tilstand. I offlinetilstand kan POS fortsætte med at behandle salg, selvom forbindelsen til Commerce Scale Unit bliver afbrudt. Det kan derefter synkroniseres med kanaldatabasen, når forbindelsen er genoprettet. Store Commerce bruger sin egen integrerede forekomst af CRT og bruger midlertidigt sin egen lokale datakilde (offline SQL Server-database). Du kan finde flere oplysninger om offlinefunktionalitet under [POS-offlinefunktionalitet](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>Overvejelser i forbindelse med eksterne POS-enheder/POS-hardware

Detailhandlere skal også overveje, hvordan POS kan få adgang til enheder og eksterne enheder som printere, pengeskuffer og betalingsterminaler. Hardwarestationer kan dedikeres til et POS-kasseapparat eller deles af kasseapparaterne i butikken.

| POS-program            | Lokal HWS OPOS | Eksterne netværksenheder | Delt HWS-support |
|----------------------------|----------------|---------------------|--------------------|
| Store Commerce til Windows | Ja            | Ja                 | Ja                |
| Store Commerce til Android | Nej             | Ja                 | Ja                |
| Store Commerce til iOS     | Nej             | Nej                  | Ja                |
| Cloud POS                  | Nej             | Nej                  | Ja                |

Du kan finde flere oplysninger om hardwarestationener i [Konfigurere og installere hardwarestation til detail](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Overvejelser i forbindelse med implementering

Når du planlægger POS-implementeringen i dine butikker, skal du overveje følgende oplysninger:

- **Funktionskrav** – Kerneforretningsaktiviteter og -egenskaber er de samme, uanset platform, formfaktor eller topologien til installationen. De fleste forhandlere behøver derfor ikke at overveje funktionskrav, når de planlægger deres implementering.
- **Forbindelse** – Tilgængelighed på netværket (Wide Area Network \[WAN\] og Local Area Network \[LAN\]) er en vigtig faktor, der kræver nøje overvejelser. Eventuelle fordele, som en ikke-pladskrævende, skybaseret løsning giver dig med hensyn til omkostninger og enkelhed, går tabt, hvis systemet ikke er tilgængeligt for forretningskritiske processer.

    Medmindre forbindelsen for en given enhed er meget pålidelig og fleksibel, eller medmindre en bestemt mængde nedetid er acceptabel for detailhandleren, anbefaler vi en af følgende muligheder:

    - Brug Store Commerce i Windows, og aktivér offlinetilstand.
    - Installer en Commerce Scale Unit i det lokale miljø.

    Disse to indstillinger udelukker ikke gensidigt hinanden. Den mest pålidelige topologi detailhandlere kan implementere en lokal RSSU for at mindske afhængigheden af forbindelse til internettet eller Azure tilgængelighed og de kan også installere POS-kasseapparater, hvor offline-tilstand er aktiveret, hvis der er et problem med den lokale server eller et netværk.

- **Hardwareenheder/eksterne enheder/** – Et vigtigt aspekt ved et Retail POS-system er dets evne til at bruge eksterne POS-enheder som printere, pengeskuffer og betalingsterminaler. Selvom alle de tilgængelige POS-muligheder kan bruge eksterne enheder, er det kun Store Commerce til Windows der understøtter dem direkte. Alle andre programmer kræver en eller flere hardwarestationer. Selvom denne metode giver fleksibilitet, skal yderligere komponenter installeres, konfigureres og serviceres.
- **Systemkrav** – Systemkravene til POS-programmet varierer. Sørg for at se de seneste oplysninger, før du foretager dit valg. For eksempel kører CPOS i en browser og understøtter derfor flere operativsystemer. Du kan finde flere oplysninger om systemkrav i [Systemkrav til skyinstallationer](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Installation og vedligeholdelse** – Kompleksiteten i installations- og vedligeholdelseskrav kan variere, afhængigt af program- og installationsvalg. En skybaseret CPOS-installation kræver f.eks. ikke, at du installerer og opdaterer på hver enhed. Denne metode reducerer derfor kompleksitet og omkostninger meget. Men hvis du installerer Store Commerce på hvert kasseapparat og aktiverer offlinetilstand og også installerer delte hardwarestationer, øger du antallet af slutpunkter, der skal administreres, meget.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
