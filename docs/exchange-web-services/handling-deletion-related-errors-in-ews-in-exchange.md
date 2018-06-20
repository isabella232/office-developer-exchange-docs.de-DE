---
title: Fehlerbehandlung Löschung-bezogene in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: Erfahren Sie, wie Löschung-bezogene Behandlung von Fehlern in Anwendungen, die Sie entwickeln, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 0dc16c3350bb75fb1e91650f0a0f0b7423727eeb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756829"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a>Fehlerbehandlung Löschung-bezogene in EWS in Exchange

Erfahren Sie, wie Löschung-bezogene Behandlung von Fehlern in Anwendungen, die Sie entwickeln, indem Sie die EWS Managed API oder EWS in Exchange.
  
Wenn Ihre Anwendung, [löscht Elemente und Ordner](deleting-items-by-using-ews-in-exchange.md)ist, Sie möglicherweise löschen-bezogene Fehler zu behandeln müssen. Sie können diese Fehler zur Laufzeit oder während Sie die EWS-Anwendung entwickeln behandeln.
  
**Tabelle 1: Löschung-bezogene Fehler und deren Behandlung**

|**Fehler**|**Tritt auf, wenn Sie versuchen...**|**Behandeln von...**|
|:-----|:-----|:-----|
|ErrorAffectedTaskOccurrencesRequired  <br/> |Löschen Sie eine Instanz einer Aufgabenserie und die **AffectedTaskOccurrence** -Eigenschaft nicht festgelegt ist.  <br/> |Festlegen der **AffectedTaskOccurrence** -Eigenschaft, und wiederholen den Löschvorgang.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> |Ein Kalenderelement befindet sich im Ordner "Gelöschte Elemente", wenn das Update führen würde, senden Sie eine besprechungseinladung an die Teilnehmer zu aktualisieren.  <br/> |Das Update stornieren oder das Kalenderelement zurück auf den Standardordner Kalender verschieben, und aktualisieren das Kalenderelement.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |Verweisen auf eine gelöschte Vorkommen einer Terminserie.  <br/> |Entfernen einen Verweis auf eine gelöschte vorkommen.  <br/> |
|ErrorCannotDeleteObject  <br/> |Löschen eines Elements, das gelöscht werden kann.  <br/> |Beenden von Versuche zum Löschen des Elements.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |Löschen Sie einer Vorkommen eines einmaligen Vorgangs oder das letzte Vorkommen einer wiederkehrenden Aufgabe.  <br/> |Wenn Sie eine einmalige Aufgabe oder Beenden von versucht, das letzte Vorkommen einer wiederkehrenden Aufgabe zu löschen.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |Löschen eines definierten Ordners an.  <br/> |Gibt an, dass Standardordnern können nicht gelöscht werden.  <br/> |
|ErrorItemNotFound  <br/> |Zugriff auf eine endgültig gelöschte Elemente.  <br/> |Entfernen von Verweisen auf ein Element aus, wenn es aus dem Speicher gelöscht wird. Wenn ein Element wiederhergestellt wird, stellen Sie sicher, dass die erforderlichen Verweise an den Client wieder zu aktivieren.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |Löschen Sie ein Kalenderelement ohne Angabe, ob Besprechungsabsagen gesendet werden sollen.  <br/> |Gibt an, dass Besprechungsabsagen soll oder nicht gesendet werden soll.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Ziehen Sie Benachrichtigungen für EWS Postfach löschen-bezogenen Ereignisse in Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [Löschen von Terminen und Abbrechen an Besprechungen mithilfe von EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

