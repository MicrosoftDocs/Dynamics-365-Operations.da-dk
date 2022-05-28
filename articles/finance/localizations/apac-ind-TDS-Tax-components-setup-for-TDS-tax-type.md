---
title: Konfigurere skattekomponenter for skattetypen Kildeskat
description: Dette emne beskriver, hvordan du opretter komponenter for A-skat i forbindelse med kildeskat (TDS – Tax Deducted at Source). Det beskriver også, hvordan du definerer den grænseværdi, der bruges til at beregne kildeskatten for hver skattekomponent.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 9c86341f7528e2c85b813e4f825ae34f10680a9b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727111"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>Konfigurere skattekomponenter for skattetypen Kildeskat

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opretter komponenter for A-skat i forbindelse med kildeskat (TDS – Tax Deducted at Source). Skattekomponenterne er Kildeskat, Tillægsafgift, PE-Cess og SHE Cess. Dette emne beskriver også, hvordan du definerer den tærskel, der bruges til at beregne kildeskatten for hver skattekomponent. Derudover kan du definere en tærskel for fritagelse, der bruges til at beregne kildeskat for hver skattekomponent.

Følg disse trin for at konfigurere skattekomponenter.

1. Gå til **Skat \> Opsætning \> A-skat \> Komponenter for A-skat**.

    [![Siden Komponenter for A-skat.](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. Vælg **Kildeskat** i feltet **Skattetype** for at konfigurere komponenter for A-skat for skattetypen Kildeskat.
3. Vælg **Ny** i handlingsruden for at oprette en linje.
4. Angiv et navn for komponenten for A-skat i feltet **Komponent for A-skat**.
5. Vælg den komponentgruppe for A-skat, som skattekomponenten skal knyttes til, i feltet **Komponentgruppe for A-skat**.
6. Indtast en beskrivelse af kildeskattekomponenten i feltet **Beskrivelse** i oversigtspanelet **Generelt**.
7. Vælg **Tærskel** i handlingsruden for at åbne siden **Tærskel**, hvor du kan definere den tærskel, der skal bruges til at beregne kildeskat for skattekomponenten.
8. Brug felterne **Fra dato** og **Til dato** til at definere den periode, som tærsklen gælder for.
9. I feltet **Tærskel** i oversigtspanelet **Generelt** skal du angive det grænsebeløb, der bruges til beregning af kildeskat for skattekomponenten. Skatten fratrækkes kun ved kilden, når det akkumulerede fakturabeløb overskrider tærsklen.

    Hvis grænsebeløbet f.eks. er 10.000, beregnes kildeskatten, når det akkumulerede fakturabeløb overstiger 10.000 (er 10.001 eller mere).

10. I feltet **Tærskel for fritagelse** skal du angive grænsebeløbet for fritagelse, som skal bruges til beregning af kildeskat for skattekomponenten. Skatten på en fakturalinje fratrækkes kun ved kilden, når beløbet overskrider tærsklen for fritagelse.

    Hvis grænsebeløbet for fritagelse f.eks. er 5.000, beregnes kildeskatten på en specifik fakturalinje, hvis beløbet på fakturalinjen overstiger 5.000 (er 5.001 eller mere).

    [![Siden Tærskel.](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > Grænseværdien for fritagelse skal være mindre end eller lig med grænsebeløbet.
    >
    > Skatten fratrækkes for en transaktion, hvis transaktionsbeløbet overstiger tærsklen for fritagelse, selvom det akkumulerede fakturabeløb ikke overstiger den tærskel, der er angivet i feltet **Tærskel**.

11. Luk siden **Tærskel** for at vende tilbage til siden **Komponenter for A-skat**.
12. Vælg **Kopiér** i handlingsruden for at åbne dialogboksen **Kopiér komponenter for A-skat**, så du kan kopiere de komponenter for kildeskat, der er konfigureret for én komponentgruppe til en anden komponentgruppe for kildeskat.
13. I feltet **Fra** skal du vælge den komponentgruppe for kildeskat, som skattekomponenterne skal kopieres fra. Vælg den komponentgruppe for A-skat, du vil kopiere komponenter for kildeskat til, i feltet **Til**.

    > [!NOTE]
    > Almindelige skattekomponenter, der er knyttet til begge komponentgrupper for kildeskat, kopieres ikke.

14. Vælg **OK** for at kopiere og oprette skattekomponenter for den anden komponentgruppe for kildeskat på siden **Komponenter for A-skat**.

    [![Dialogboksen Kopier komponenter for A-skat.](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Luk siden.
