---
title: Komponenter i elektronisk rapportering
description: Dette emne indeholder en beskrivelse af ER-komponenterne (Elektronisk rapportering).
author: nselin
ms.date: 09/28/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6356fdaee4c6298dd87ef965fcd91937144cd529
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985728"
---
# <a name="electronic-reporting-components"></a>Komponenter i elektronisk rapportering

[!include [banner](../includes/banner.md)]

Elektronisk rapportering (ER) understøtter følgende komponenttyper:

- Datamodel
- Modeltilknytning
- Formater
- Metadata

## <a name="data-model-component"></a>Datamodelkomponent

En datamodelkomponent er en abstrakt repræsentation af en datastruktur. Den beskriver et bestemt forretningsdomæneområde tilstrækkeligt detaljeret til at opfylde kravene til rapportering for det pågældende domæne. En data modelkomponent består af følgende dele:

- **Datamodel** - Et sæt af domænespecifikke forretningsenheder samt en hierarkisk struktureret definition af relationerne mellem enhederne.
- **Modeltilknytning** - Valgte programdatakilder med enkelte elementer i en datamodel, der under kørsel angiver dataflow og regler for angivelse af forretningsdata til en datamodelkomponent.

Forretningsenheden til en datamodel er repræsenteret som en beholder eller post. Egenskaber for forretningsenheden er repræsenteret som dataelementer eller felter. Hvert dataelement har et entydigt navn, etiket, beskrivelse og værdi. Værdien af hvert dataelement kan være udformet, så den kan genkendes som en streng, heltal, reelt tal, dato, fasttekst eller boolesk værdi. Desuden kan dataelementet være en anden post eller postliste.

En enkelt modelkomponent kan indeholde flere hierarkier af domænespecifikke forretningsobjekter. Den kan også indeholde modeltilknytninger, der understøtter et rapportspecifikt dataflow på kørselstidspunktet. Hierarkierne afpasses efter en enkelt post, der er valgt som en rod for modeltilknytningen. Datamodellen for betalingsdomæneområdet kan f.eks. understøtte følgende tilknytninger:


- Virksomhed \> Kreditor \> Betalingstransaktioner for AP-domænet
- Debitor \> Virksomhed \> Betalingstransaktioner for AR-domænet

Forretningsenheder som f.eks firma- og betalingsposteringer angives én gang. Forskellige tilknytninger kan genbruge dem efter behov.

## <a name="model-mapping-component"></a>Komponent til modeltilknytning

Modeltilknytning til programdatakilder med enkelte elementer i en datamodel, der under kørsel angiver dataflow og regler for angivelse af forretningsdata til en datamodelkomponent.

En modeltilknytning, der understøtter udgående elektroniske dokumenter, har følgende muligheder:

- Den kan bruge forskellige datatyper som datakilder til en datamodel. Disse datatyper omfatter tabeller, dataenheder, metoder og fasttekster.
- Den understøtter brugerinputparametre, der kan defineres som datakilder for en datamodel, når data skal angives på kørselstidspunktet.
- Den understøtter datatransformationen til de grupper, der kræves. Du kan også filtrere, sortere og summere data og tilføje logisk beregnede felter, der er designet via formler, der ligner Microsoft Excel-formler. Du kan finde flere oplysninger under [Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md).

En modeltilknytning, der understøtter indgående elektroniske dokumenter, har følgende muligheder:

- Det kan bruge forskellige opdaterbare dataelementer som mål. Disse dataelementer omfatter tabeller, dataenheder og visninger. Dataene kan opdateres ved hjælp af indgående dataene fra de elektroniske dokumenter. Der kan bruges flere destinationer i en enkelt modeltilknytning.
- Den understøtter brugerinputparametre, der kan defineres som datakilder for en datamodel, når data skal angives på kørselstidspunktet.

En datamodelkomponent er udviklet til hvert forretningsdomæne, der bruges som en samlet datakilde til rapportering. Den samlede datakilde afrapporterer fra den fysiske implementering af datakilder. Komponenten repræsenterer domænespecifikke forretningsbegreber og -funktioner i en formular, der gør et rapporteringsformats oprindelige design og yderligere vedligeholdelse mere effektivt.

## <a name="format-component"></a>Formatkomponent

### <a name="format-components-for-outgoing-electronic-documents"></a>Formatkomponenter for udgående elektroniske dokumenter

En formatkomponent er skemaet for rapporteringsoutput, der skal oprettes på kørselstidspunktet. Et skema består af følgende elementer:

- Et format, der definerer strukturen og indholdet af det udgående elektroniske dokument, der oprettes på kørselstidspunktet.
- Datakilder som et sæt brugerinputparametre og en domænespecifik datamodel, der bruger en valgt modeltilknytning.
- En formattilknytning som et sæt bindinger af formatdatakilder, der har enkelte elementer af et format, der angiver dataflow og regler for formatoutputgenerering på kørselstidspunktet.
- En formatvalidering som et sæt konfigurerbare regler, der styrer oprettelsen af rapporten på kørselstidspunktet afhængigt af kørselskonteksten. Eksempelvis kan der være en regel, der standser outputgenerering af en kreditors betalinger og medfører en undtagelse, når bestemte attributter for den valgte kreditor mangler, f.eks. bankkontonummeret.

En formatkomponent understøtter følgende funktioner:

- Oprettelse af rapporteringsoutput som separate filer i forskellige formater, f.eks. tekst, XML, Microsoft Word-dokument eller regneark
- Separat oprettelse af flere filer og indkapsling af disse filer i zip-filer

En formatkomponent gør det muligt at vedhæfte bestemte filer, der kan bruges i rapporteringsoutputtet:

- Excel-projektmapper, der indeholder et regneark, der kan bruges som skabelon for output i regnearksformat OPENXML:
- Word-filer, der indeholder et dokument, der kan bruges som skabelon for output i Microsoft Word-dokumentformatet
- Andre filer kan indgå i formatets output som foruddefinerede filer.

I følgende illustration vises, hvordan dataene flyder for disse formater.

[![Dataflow for indgående formatkomponenter.](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Hvis du vil køre en enkelt ER-formatkonfigurationen for at importere data fra et indgående elektronisk dokument, skal du identificere den ønskede tilknytning af en formatkonfiguration samt integrationspunktet for en modeltilknytning. Du kan bruge den samme modeltilknytning og de samme destinationer sammen med forskellige formater for forskellige typer indgående dokumenter.

## <a name="component-versioning"></a>Komponentversioner

Versionering understøttes for ER-komponenter. Der findes følgende arbejdsgang til håndtering af ændringer i ER-komponenter:

1. Den oprindelige version, der blev oprettet, er markeret som en **Kladde**-version. Denne version kan redigeres og er tilgængelig for testkørsler.
2. **Kladde** versionen kan konverteres til en **Fuldført** version. Denne version kan bruges i lokale rapporteringsprocesser.
3. Versionen **Fuldført** kan konverteres til en **Delt** version. Denne version udgives på Microsoft Dynamics Lifecycle Services (LCS) og kan bruges i globale rapportingsprocesser.
4. Versionen **Delt** kan konverteres til en **Annulleret** version. Denne version kan slettes.

Versioner, der har status som enten **Fuldført** eller **Delt** er tilgængelige for anden dataudveksling. Følgende handlinger kan udføres på en komponent, der har disse statusser:

- Komponenten kan serialiseres i XML-format og eksporteres som en fil i XML-format.
- Komponenten kan reserialiseres fra en XML-fil og importeres til programmet som en ny version af en ER-komponent.

## <a name="component-date-effectivity"></a>Komponentens datogyldighed

ER-komponentversioner har en ikrafttrædelsesdato. Du kan indstille datoen "Gyldig fra" for en ER-komponent for at angive startdatoen, hvor komponenten træder i kraft for rapporteringsprocesser. Programsessionsdatoen bruges til at definere, om en komponent er gyldig til udførelse. Hvis mere end én version er gyldig for en bestemt dato, bruges den nyeste version til rapporteringsprocesser.

## <a name="component-access"></a>Komponentadgang

Adgangen til ER-formatkomponenter afhænger af indstillingen for ISO-lande-/områdekoden (International Organization for Standardization). Hvis denne indstilling er tom for en valgt version af en formatkonfiguration, kan en formatkomponent åbnes fra ethvert firma på kørselstidspunktet. Hvis denne indstilling indeholder ISO-land/område-koder, er en formatkomponent kun tilgængelig fra firmaer, der har en primær adresse, som er defineret for en af en formatkomponents ISO-land/område-koder.

Forskellige versioner af en dataformatkomponent kan have forskellige indstillinger for ISO-land/område-koder.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

