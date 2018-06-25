---
title: Fehlerbehandlung Delegierung-bezogene in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 631d364f-e324-4838-a92c-820286f771f8
description: Erfahren Sie, wie Delegierung-bezogene Behandlung von Fehlern in Anwendungen, die Sie entwickeln, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 3851709888e3a1087df02eea5d4d58888ad168e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756832"
---
# <a name="handling-delegation-related-errors-in-ews-in-exchange"></a>Fehlerbehandlung Delegierung-bezogene in EWS in Exchange

Erfahren Sie, wie Delegierung-bezogene Behandlung von Fehlern in Anwendungen, die Sie entwickeln, indem Sie die EWS Managed API oder EWS in Exchange.
  
Wenn Ihre Anwendung Delegierung verwendet oder hinzugefügt oder Stellvertretungen entfernt, müssen Sie möglicherweise Delegierung-bezogene Fehler zu behandeln. Sie können diese Fehler zur Laufzeit oder während Sie die EWS-Anwendung entwickeln behandeln. Diese Fehler werden durch die EWS Managed API [ServiceError](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) -Enumeration und die EWS- [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element definiert. 
  
## <a name="delegation-related-errors"></a>Delegierung-bezogene Fehler

|**Fehler**|**Tritt auf, wenn Sie versuchen...**|**Behandeln von...**|
|:-----|:-----|:-----|
|ErrorItemNotFound  <br/> ErrorFolderNotFound  <br/> |Führen Sie einen Vorgang für ein Postfach, Ordner oder Element, das Sie nicht über Zugriff auf verfügen.  <br/> |Aktualisieren der Stellvertretung Berechtigungen zum Zugriff auf die Ordner oder Element durch Aufrufen der [UpdateDelegates](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) EWS Managed API-Methode oder [UpdateDelegate](http://msdn.microsoft.com/library/03f618ac-ad1a-4772-9b81-c5bb0f12d6ab%28Office.15%29.aspx) EWS-Vorgangs, und klicken Sie dann wiederholen die Anforderung zu aktivieren.  <br/> |
|ErrorAccessDenied  <br/> |Ändern Sie ein Element, das Sie nicht über ausreichende Berechtigungen zum Ändern verfügen.  <br/> |Aktualisieren Ihre Stellvertretungsberechtigungen durch Aufrufen der **UpdateDelegate** EWS Managed API-Methode oder die **UpdateDelegate** EWS-Vorgang, und klicken Sie dann Wiederholung der Anforderung.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |Versuchen Sie, den Besitzer des Postfachs als Stellvertreter ihres eigenen Postfachs hinzufügen.  <br/> |[Hinzufügen eines anderen Benutzers als Stellvertreter](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md), nicht der Postfachbesitzer.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |Fügen Sie der stellvertretungs, wenn die Stellvertretung bereits vorhanden ist.  <br/> |Nichts, da die Stellvertretung für den Besitzer des Postfachs bereits vorhanden ist. Oder, wenn Sie die Berechtigungen eines vorhandenen Delegaten ändern möchten, verwenden Sie die **UpdateDelegates** -Methode oder **UpdateDelegate** -Vorgang.  <br/> |
|ErrorNotDelegate  <br/> |Ändern Sie die Berechtigungen der Stellvertretung für einen Benutzer, der keine Delegaten Berechtigungen für das Postfach verfügt.  <br/> |[Hinzufügen des Benutzers als Stellvertreter](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) für das Postfach, bevor Sie versuchen, aktualisieren oder ihre Berechtigungen entfernen.  <br/> |
|ErrorDelegateNoUser  <br/> |Ändern Sie die Berechtigungen der Stellvertretung für einen Benutzer, die nicht in Active Directory-Domänendienst (AD DS) ist.  <br/> |Erstellen den Benutzer in AD DS oder korrigieren die Stellvertretung Informationen in der Anforderung.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |Verwenden Sie ein Stellvertreter zum Abonnieren von Benachrichtigungen im Auftrag des Postfachbesitzers.  <br/> |Abonnieren von Benachrichtigungen als Besitzer des Postfachs.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |Stellen Sie eine Anforderung von einer Stellvertretung, die eine anderen Server-Version als der Prinzipal Postfachserver hat.  <br/> |Verwenden ein Stellvertreter oder Hinzufügen einer Stellvertretung, dessen Postfach die gleiche Serverversion als der Postfachbesitzer aufweist.  <br/> |
|ErrorMissingEmailAddress  <br/> |Stellen Sie eine Anforderung von einem Delegaten-Konto, das nicht über ein Postfach verfügt.  <br/> |Hinzufügen eines Postfachs mit der Stellvertretung Konto.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

