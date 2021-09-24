---
title: Umgang mit Fehlern in Exchange im Zusammenhang mit Löschungen in EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: Erfahren Sie, wie Sie Löschfehler in Anwendungen behandeln, die Sie mithilfe der verwalteten EWS-API oder EWS in Exchange entwickeln.
ms.openlocfilehash: d82901a2ebc8577258e191cbd014db93cc40d099
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513255"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a>Umgang mit Fehlern in Exchange im Zusammenhang mit Löschungen in EWS

Erfahren Sie, wie Sie Löschfehler in Anwendungen behandeln, die Sie mithilfe der verwalteten EWS-API oder EWS in Exchange entwickeln.
  
Wenn Ihre Anwendung [Elemente und Ordner löscht,](deleting-items-by-using-ews-in-exchange.md)müssen Sie möglicherweise fehlerbezogene Löschvorgänge behandeln. Sie können diese Fehler zur Laufzeit oder während der Entwicklung Ihrer EWS-Anwendung behandeln.
  
**Tabelle 1: Fehler im Zusammenhang mit Löschvorgängen und deren Behandlung**

|**Error**|**Tritt auf, wenn Sie versuchen, ...**|**Behandeln von...**|
|:-----|:-----|:-----|
|ErrorAffectedTaskOccurrencesRequired  <br/> |Löschen sie eine Instanz einer wiederkehrenden Aufgabe, und die **AffectedTaskOccurrence-Eigenschaft** ist nicht festgelegt.  <br/> |Festlegen der **AffectedTaskOccurrence-Eigenschaft** und Wiederholen des Löschvorgangs.  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> |Aktualisieren Sie ein Kalenderelement, das sich im Ordner "Gelöschte Elemente" befindet, wenn die Aktualisierung dazu führen würde, dass eine Besprechungseinladung an die Teilnehmer gesendet wird.  <br/> |Abbrechen der Aktualisierung oder Zurückverlagern des Kalenderelements in den Standardordner "Kalender" und Aktualisieren des Kalenderelements.  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |Verweisen auf ein gelöschtes Vorkommen einer Terminserie.  <br/> |Entfernen eines Verweises auf ein gelöschtes Vorkommen.  <br/> |
|ErrorCannotDeleteObject  <br/> |Löschen eines Elements, das nicht gelöscht werden kann.  <br/> |Beim Beenden wird versucht, das Element zu löschen.  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |Löschen eines Vorkommens eines nicht wiederkehrenden Vorgangs oder Löschen des letzten Vorkommens einer Terminserie.  <br/> |Löschen eines nicht wiederkehrenden Vorgangs oder Beenden von Versuchen, das letzte Vorkommen einer Wiederkehrenden Aufgabe zu löschen.  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |Löschen eines definierten Ordners.  <br/> |Gibt an, dass Standardordner nicht gelöscht werden können.  <br/> |
|ErrorItemNotFound  <br/> |Zugriff auf ein endgültig gelöschtes Element.  <br/> |Entfernen von Verweisen auf ein Element, wenn es aus dem Speicher gelöscht wird. Wenn ein Element wiederhergestellt wird, stellen Sie sicher, dass Sie die erforderlichen Verweise auf den Client wieder aktivieren.  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |Löschen Sie ein Kalenderelement, ohne anzugeben, ob Besprechungsabsagen gesendet werden sollen.  <br/> |Angeben, dass Besprechungsabsagen gesendet werden sollen oder nicht.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Pullbenachrichtigungen in Exchange für Postfachereignisse im Zusammenhang mit Löschungen in EWS](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [Mithilfe von EWS in Exchange Termine löschen und Besprechungen absagen](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

