---
title: Umgang mit Fehlern in Exchange im Zusammenhang mit Löschungen in EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: Erfahren Sie, wie Sie mit Lösch Fehlern in Anwendungen umgehen können, die Sie mit dem verwaltete EWS-API oder EWS in Exchange entwickeln.
ms.openlocfilehash: 41c217c1c3815606d898b8237ea327f34869174b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455947"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a>Umgang mit Fehlern in Exchange im Zusammenhang mit Löschungen in EWS

Erfahren Sie, wie Sie mit Lösch Fehlern in Anwendungen umgehen können, die Sie mit dem verwaltete EWS-API oder EWS in Exchange entwickeln.
  
Wenn Ihre Anwendung [Elemente und Ordner löscht](deleting-items-by-using-ews-in-exchange.md), müssen Sie möglicherweise Lösch bezogene Fehler behandeln. Sie können diese Fehler zur Laufzeit oder während der Entwicklung ihrer EWS-Anwendung behandeln.
  
**Tabelle 1: Fehler im Zusammenhang mit Löschungen und deren Behandlung**

|**Error**|**Tritt auf, wenn Sie versuchen,...**|**Behandeln von...**|
|:-----|:-----|:-----|
|ErrorAffectedTaskOccurrencesRequired  <br/> |Löschen Sie eine Instanz einer wiederkehrenden Aufgabe, und die **AffectedTaskOccurrence** -Eigenschaft ist nicht festgelegt.  <br/> |Festlegen der **AffectedTaskOccurrence** -Eigenschaft und erneutes ausprobieren des Löschvorgangs.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> |Aktualisieren eines Kalenderelements, das sich im Ordner "Gelöschte Elemente" befindet, wenn das Update dazu führen würde, dass eine Besprechungseinladung an die Teilnehmer gesendet wird.  <br/> |Abbrechen des Updates oder Verschieben des Kalenderelements zurück in den Standardkalenderordner und Aktualisieren des Kalenderelements.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |Verweisen auf ein gelöschtes Vorkommen einer Terminserie.  <br/> |Entfernen eines Verweises auf ein gelöschtes vorkommen.  <br/> |
|ErrorCannotDeleteObject  <br/> |Löscht ein Element, das nicht gelöscht werden kann.  <br/> |Beenden versucht, das Element zu löschen.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |Löschen Sie ein Vorkommen einer nicht wiederkehrenden Aufgabe, oder löschen Sie das letzte Vorkommen einer wiederkehrenden Aufgabe.  <br/> |Löschen einer nicht wiederkehrenden Aufgabe oder Beenden von versuchen, das letzte Vorkommen einer wiederkehrenden Aufgabe zu löschen.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |Löschen eines Distinguished Folders.  <br/> |Zeigt an, dass die Standardordner nicht gelöscht werden können.  <br/> |
|ErrorItemNotFound  <br/> |Zugriff auf ein dauerhaft gelöschtes Element.  <br/> |Entfernen von Verweisen auf ein Element, wenn es aus dem Speicher gelöscht wird. Wenn ein Element wiederhergestellt wird, stellen Sie sicher, dass Sie die erforderlichen Verweise auf den Client erneut aktivieren.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |Löschen Sie ein Kalenderelement, ohne anzugeben, ob Besprechungsabsagen gesendet werden sollen.  <br/> |Angeben, dass Besprechungsabsagen gesendet werden sollen oder nicht.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Pullbenachrichtigungen in Exchange für Postfachereignisse im Zusammenhang mit Löschungen in EWS](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [Mithilfe von EWS in Exchange Termine löschen und Besprechungen absagen](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

