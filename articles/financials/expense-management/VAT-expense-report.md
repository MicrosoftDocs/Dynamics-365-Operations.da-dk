---
title: Inddrivelse af moms i Udgiftsstyring
description: "Dette emne forklarer, hvordan du kan få refunderet beløb fra berettigede momstransaktioner."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: da-dk
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a>Inddrivelse af moms i Udgiftsstyring

For at få beløb refunderet fra berettigede momstransaktioner skal en virksomhed eller organisation identificere, indsamle, kontrollere og indsende nøjagtige oplysninger. Denne proces omfatter flere forskellige opgaver, og afhængigt af virksomhedens størrelse, kan den omfatte flere medarbejdere eller roller.

For at få moms retur vha. Udgiftsstyring skal følgende opgaver fuldføres:

- Der skal oprettes momsgrupper for lande/områder fordelt på udgiftsarter.
- Der skal oprettes en momsgruppe for hver momskode.
- Der skal oprettes en varemomskode for hver momsgruppe.

Når dette er fuldført, kan medarbejdere udføre disse trin for at anmode om momsrefusioner.

1. I en udgiftsrapport skal der angives momsoplysninger om kreditkorttransaktioner for at identificere berettiget inddrivelse af moms.
2. Kontroller, at alle momsoplysninger er fuldstændige, og bogfør derefter udgiftsrapporten.
3. Behandl udgifter, der er berettigede til international momsopkrævning.
4. Sende momsinddrivelsesdata til en tredjepartsleverandør for registrering af international inddrivelse af moms.
5. Behandle udgifter for indenlandsk inddrivelse af moms.

De følgende afsnit indeholder eksempler på, hvordan Contoso-medarbejdere udfører de enkelte trin.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>I en udgiftsrapport skal du angive momsoplysninger om kreditkorttransaktioner for at identificere berettigede momsrefusioner

Nancy, som er sælger hos Contoso i USA, er for nylig kommet hjem fra en forretningsrejse til Storbritannien. I løbet af rejsen har hun brugt sit private kreditkort til at betale for måltider. Nancy skal nu oprette en udgiftsrapport for at få dækket sine udgifter.

Når Nancy indtaster oplysninger i sin udgiftsrapport, vælger hun **Storbritannien** i feltet **Land/område** på siden **Rediger udgiftsrapport**. Listen over momsgrupper filtreres derefter, så den kun viser de grupper, der gælder for Storbritannien. Nancy vælger momsgruppen **Storbritannien 001**, og derefter vælger hun varemomsgruppen **Måltider**. Derefter tilføjer hun en ny postering for overnatning. Da der kun er én momsgruppe og varemomsgruppe for overnatning i Storbritannien, udfyldes disse oplysninger automatisk i Nancys udgiftsrapport.

I henhold til Contosos politik skal alle udgifter have en sammenholdelseskvittering. Når Nancy gemmer sin udgiftsrapport, modtager hun derfor en meddelelse om, at hun skal vedhæfte en kvittering for hver transaktion, hun har angivet på udgiftsrapporten. Nancy kontrollerer, at hun har vedhæftet et digitalt billede af alle kvitteringer til udgiftsrapporten, og derefter sender hun rapporten til godkendelse. Derefter sender hun papirkvitteringerne til back-office-teamet. Dette team sender de relevante momsdata til tredjepartsleverandøren, der administrerer international momsinddrivelse for Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Kontroller, at alle momsoplysninger er fuldstændige, og bogfør derefter udgiftsrapporten

April, som er kreditorkoordinator hos Contoso, skal angive alle momsoplysninger, der mangler i en udgiftsrapport, før rapporten kan blive bogført. Hun åbner siden **Detaljer om udgiftsrapporter** og ser Nancys godkendte udgiftsrapport. April åbner derefter udgiftsrapporten for at få vist posteringsdetaljerne. Hun kan se, at Nancy ikke har angivet en varemomsgruppe for en af posteringerne. Da disse oplysninger ikke er angivet, kan April ikke bogføre udgiftsrapporten. April ser derfor på siden **Momskonfigurationer** i Udgiftsstyring og finder den relevante varemomsgruppe for landet/området samt posteringstypen. Nu kan April bogføre udgiftsrapporten i finansmodulet.

Når April bogfører udgiftsrapporten, opretter der et arbejdselement for momsinddrivelse. Dette arbejdselement tildeles et medlem af back-office-teamet. April får en meddelelse, der bekræfter, at bogføringen er fuldført. Denne meddelelse viser også antallet af fundne momstransaktioner, der kan refunderes.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Behandl udgifter, der er berettigede til international momsopkrævning

Arnie, som er medlem af Contosos back-office-team, er ansvarlig for at bekræfte, at alle de påkrævede oplysninger i forbindelse med momsinddrivelse er inkluderet i udgiftsrapporter. Han åbner siden **Udgift med momsopkrævning** og vælger den udgiftsrapport, som Nancy har sendt. Arnie kontrollerer, at alle de nødvendige kvitteringer er vedhæftet, og at den korrekte momsgruppe og varemomsgruppe er angivet.

Da Arnie modtager papirkvitteringerne fra Nancy, kontrollerer han dem mod de digitale kvitteringer og ændrer derefter status for udgiftsrapporten til **Klar til opkrævning**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Sende momsinddrivelsesdata til en tredjepartsleverandør for registrering af international inddrivelse af moms

Da Arnie er klar til at sende udgiftsrapportdataene til den tredjepartsleverandør, der registrerer momsinddrivelsen, åbner han siden **Udgift med momsopkrævning**. Han filtrerer siden, så den kun viser de udgiftsrapporter, der er markeret som **Klar til opkrævning**. Derefter vælger han **Filer** &gt; **Eksportér til Excel**. Momsoplysningerne fra udgiftsrapporten eksporteres til et Microsoft Excel-regneark. Arnie sender regnearket til tredjepartsleverandøren og medsender en besked om, at papirkvitteringerne er blevet sendt med kurer.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Behandle udgifter for indenlandsk inddrivelse af moms

Arnie skal kontrollere, at udgiftsrapportposteringerne er berettigede for inddrivelse af moms, og at de digitale kvitteringer er vedhæftet rapporterne. For at starte behandlingen af berettigede udgifter til indenlandsk inddrivelse åbner Arnie siden **Udgift med momsopkrævning** og vælger den udgiftsrapport, der kræver godkendelse. Han bekræfter, at kvitteringerne lyder på virksomhedens navn frem for medarbejderens. Ved momsopkrævning skal kvitteringer være udstedt i virksomhedens navn. Arnie kontrollerer derefter, at den korrekte momsgruppe og varemomsgruppe er angivet.

Da Arnie modtager papirkvitteringerne, ændrer han status for udgiftsrapporten til **Klar til opkrævning**. Han kan derefter indsende anmodningen om refusion til den relevante skattemyndighed. I dette tilfælde er skattemyndighederne det amerikanske skattevæsen (IRS - Internal Revenue Service).

