---
title: Svar på leverandørspørgsmål i forbindelse med tilbudsanmodninger
description: Leverandører, der har spørgsmål til en RFP, kan sende deres spørgsmål og læse svarene på siden til **Kreditorsamarbejde**.
author: GalynaFedorova
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQVendQuestionAnswer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: public sector
ms.author: gfedorova
ms.search.validFrom: 2020-1-22
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: ad8a99547e3822fa6042283741f8fb8c76f495ce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889503"
---
# <a name="responding-to-vendor-questions-on-request-for-quotations"></a>Svar på leverandørspørgsmål i forbindelse med tilbudsanmodninger

[!include [banner](../includes/banner.md)]

Når dit kontor har sendt en tilbudsanmodning, har leverandørerne nogle gange spørgsmål, der vedrører anmodningen. Leverandører, der har spørgsmål til en RFP, kan sende deres spørgsmål og læse svarene på siden til **Kreditorsamarbejde**, når du gør siden tilgængelig for dem. Når leverandørspørgsmål er accepteret, er **Spørgsmål og svar** tilgængelige på siden **Bud på tilbudsanmodning** i **Kreditorsamarbejde** og for dit kontor via siden **Tilbudsanmodning** i **Spørgsmål og svar**. 

Brugerne kan udgive svar på leverandørspørgsmål mere end én gang. Kreditorer kan ikke længere postere spørgsmål, når en leverandør er valgt, og tilbudsanmodningen er tildelt, eller når skæringsdatoen for spørgsmål er nået.

## <a name="turn-on-the-feature"></a>Slå funktionen til

Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret. Administratorer kan bruge siden [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere eller deaktivere den, hvis det er nødvendigt. Her er funktionen angivet som:

- **Modul:** *Indkøb og forsyning*
- **Funktionsnavn:** *Spørgsmål og svar vedrørende tilbudsanmodninger*

## <a name="allow-questions-and-answers-to-be-used-in-rfqs"></a>Tillad, at spørgsmål og svar bruges i tilbudsanmodninger

1. Gå til **Indkøb og forsyning \> Opsætning \> Indkøbs- og forsyningsparametre**.
1. Åbn fanen **Tilbudsanmodning**.
1. Angiv følgende indstillinger efter behov:
    - **Tillad leverandørspørgsmål**: Aktiverer eller deaktiverer leverandørspørgsmål om tilbudsanmodningssager. Du skal indstille denne til *Ja*, hvis du vil bruge de funktioner, der er beskrevet i denne artikel.
    - **Direkte standardsvar**: Når du besvarer et spørgsmål, kan du vælge at besvare alle de leverandører, der har modtaget tilbudsanmodningen, eller kun at svare den bestemte leverandør, som har sendt spørgsmålet. Du kan vælge denne indstilling, hver gang du svarer, men denne indstilling styrer standardindstillingen. Hvis du normalt besvarer alle leverandører, skal du vælge *Nej*. Hvis du normalt besvarer leverandører hver for sig, skal du vælge *Ja*.

## <a name="setting-up-for-vendor-questions"></a>Opsætning af leverandørspørgsmål

Når du opretter en tilbudsanmodning, bestemmer du, om leverandører kan stille spørgsmål til tilbudsanmodningen.

1. Gå til **Indkøb og forsyning > Tilbudsanmodninger**, og klik på **Ny > Tilbudsanmodning**. 
1. På siden **Ny tilbudsanmodning** skal **Hoved** angives til **Indstillinger for leverandørspørgsmål** for at tillade spørgsmål før en bestemt dato.
1. Angiv indstillingen **Tillad leverandørspørgsmål** til **Ja**, så leverandørerne kan skrive spørgsmål. Brugerne kan angive og besvare spørgsmål og udpege ofte stillede spørgsmål til udgivelse for leverandører, når tilbudsanmodningen er sendt til leverandørerne.
1. Valgfrit: Definer feltet **Skæringsdato**, hvor spørgsmål senest skal indsendes. Hvis der ikke angives en skæringsdato, accepteres spørgsmålene, så længe tilbudsanmodningen er åben og accepterer bud.
1. Klik på **Gem** for at gemme tilbudsanmodningen.
1. Klik på **Send** for at sende tilbudsanmodningen til leverandører.

## <a name="entering-and-replying-to-vendor-questions"></a>Angive og besvare leverandørspørgsmål

Leverandører skriver spørgsmål i **Kreditorsamarbejde > Bud på tilbudsanmodning**, oversigtspanelet **Leverandørspørgsmål**. Spørgsmålet er kun synligt for leverandøren og brugerne.

## <a name="entering-a-vendor-question"></a>Angive et leverandørspørgsmål

1. I Kreditorsamarbejde skal du på siden **Bud på tilbudsanmodning** klikke på **Spørgsmål og svar** og derefter klikke på **+ Stil et spørgsmål**.

    > [!NOTE]
    > Alternativt kan en bruger skrive spørgsmål til en leverandør på siden **Tilbudsanmodning** ved at klikke **Administrer svar**, **Rediger svar på tilbudsanmodning** og derefter klikke på **Spørgsmål og svar**.

2. Skriv teksten til spørgsmålet i feltet **Spørgsmål**.
3. Klik på **Send**. Gentag trin 1-3 for at tilføje et spørgsmål.
4. Når du er færdig, skal du klikke på **Gem** for at gemme dine spørgsmål.

## <a name="replying-to-a-single-vendor"></a>Besvare en enkelt leverandør

Spørgsmål og svar er kun synlige for leverandøren og brugerne.

1. På siden **Tilbudsanmodning** skal du klikke på **Spørgsmål og svar** for at åbne siden **Spørgsmål og svar**.
1. Klik på **Rediger**.
1. Indtast tekst i **Svar**-feltet for at svare på leverandørspørgsmålet.
1. Markér feltet **Direkte svar**.
1. Klik på **Gem** for at gemme svarene.
1. Klik på **Send svar** for at sende svarene til leverandøren.

## <a name="replying-to-all-vendors"></a>Besvare alle leverandører

Hvis du modtager samme spørgsmål fra flere leverandører, kan du gruppere spørgsmålene og reagere med det samme svar. Alle leverandører modtager en besked, når de ofte stillede spørgsmål og svar udgives. Leverandørerne og alle, der har adgang til tilbudsanmodningen, kan få vist oversigten over spørgsmål og svar.

1. På siden **Tilbudsanmodning** skal du klikke på **Spørgsmål og svar** for at åbne siden **Spørgsmål og svar**.
2. Klik på **Rediger**.
3. Vælg en kode for det almindelige spørgsmål, f.eks. bogstavet 'a'.
4. For hver linje, der stiller et lignende spørgsmål, skal du angive koden i feltet **Gruppekode**. For hver linje, der spørger til varens farve, skal du f.eks. angive 'a'.
5. Vælg en af linjerne med kodeværdien, og angiv det spørgsmål og svar, som de skal læse i oversigten, og som skal være tilgængeligt, når spørgsmålene og svarene publiceres (**Gruppespørgsmål, Gruppesvar** som felter).
6. Valgfrit: Du kan markere afkrydsningsfeltet **Direkte svar** for kun at sende svarene til de valgte leverandører.
7. Klik på **Gem** for at gemme svarene.
8. Valgfrit: Du kan ændre spørgsmålene og svarene til de tidligere udgivne værdier, hvis du vil fortryde dine ændringer.
9. Klik på **Send svar** for at sende svarene til leverandørerne.

## <a name="changing-rfq-to-allow-or-disallow-questions"></a>Ændre tilbudsanmodning for at tillade eller forbyde spørgsmål

Du kan foretage ændringer for at tillade eller ikke tillade spørgsmål til tilbudsanmodninger, indtil tilbudsanmodningen er belønnet. Du kan også udvide eller forkorte den tidsramme, som leverandørerne kan indsende spørgsmål i.
I forbindelse med publicerede tilbudsanmodninger skal du redigere en tilbudsanmodning for at tillade eller ikke tillade leverandørspørgsmål eller justere tidsrammen for spørgsmål.

> [!IMPORTANT]
> Hvis du ændrer en eksisterende tilbudsanmodning med det formål at tillade leverandørspørgsmål, rydder systemet alle eksisterende svar, når du sender tilbudsanmodningen igen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]