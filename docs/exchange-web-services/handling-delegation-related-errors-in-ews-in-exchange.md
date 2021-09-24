---
title: Fehlerbehandlung Delegierung-bezogene in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 631d364f-e324-4838-a92c-820286f771f8
description: Erfahren Sie, wie Sie delegierungsbezogene Fehler in Anwendungen behandeln, die Sie mithilfe der verwalteten EWS-API oder EWS in Exchange entwickeln.
ms.openlocfilehash: 17e4e7898f5cbed7a6dc524a84db6ba4080eab88
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512296"
---
# <a name="handling-delegation-related-errors-in-ews-in-exchange"></a>Fehlerbehandlung Delegierung-bezogene in EWS in Exchange

Erfahren Sie, wie Sie delegierungsbezogene Fehler in Anwendungen behandeln, die Sie mithilfe der verwalteten EWS-API oder EWS in Exchange entwickeln.
  
Wenn Ihre Anwendung Stellvertretungen verwendet oder Stellvertretungen hinzufügt oder entfernt, müssen Sie möglicherweise Delegierungsfehler behandeln. Sie können diese Fehler zur Laufzeit oder während der Entwicklung Ihrer EWS-Anwendung behandeln. Diese Fehler werden durch die EWS Managed API [ServiceError-Enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) und das EWS [ResponseCode-Element](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) definiert. 
  
## <a name="delegation-related-errors"></a>Delegierungsbezogene Fehler

|**Error**|**Tritt auf, wenn Sie versuchen, ...**|**Behandeln von...**|
|:-----|:-----|:-----|
|ErrorItemNotFound  <br/> ErrorFolderNotFound  <br/> |Führen Sie einen Vorgang für ein Postfach, einen Ordner oder ein Element aus, auf das Sie keinen Zugriff haben.  <br/> |Aktualisieren der Berechtigungen der Stellvertretung, damit sie auf den Ordner oder das Element zugreifen können, indem sie die verwaltete EWS-API-Methode von [UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) oder den EWS-Vorgang ["UpdateDelegate"](https://msdn.microsoft.com/library/03f618ac-ad1a-4772-9b81-c5bb0f12d6ab%28Office.15%29.aspx) aufrufen und dann die Anforderung wiederholen.  <br/> |
|ErrorAccessDenied  <br/> |Ändern eines Elements, für das Sie nicht über ausreichende Berechtigungen zum Ändern verfügen.  <br/> |Aktualisieren der Stellvertretungsberechtigungen durch Aufrufen der verwalteten EWS-API-Methode **"UpdateDelegate"** oder des EWS-Vorgangs **"UpdateDelegate"** und anschließendes Wiederholen der Anforderung.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |Versuchen Sie, den Postfachbesitzer als Stellvertretung zu ihrem eigenen Postfach hinzuzufügen.  <br/> |[Hinzufügen eines anderen Benutzers als Stellvertretung,](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)nicht des Postfachbesitzers.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |Fügen Sie den Delegaten hinzu, wenn der Delegat bereits vorhanden ist.  <br/> |Nichts tun, da der Delegat bereits für den Postfachbesitzer vorhanden ist. Wenn Sie versuchen, die Berechtigungen eines vorhandenen Delegaten zu ändern, verwenden Sie die **UpdateDelegates-Methode** oder den **UpdateDelegate-Vorgang.**  <br/> |
|ErrorNotDelegate  <br/> |Ändern von Stellvertretungsberechtigungen für einen Benutzer, der über keine Stellvertretungsberechtigungen für das Postfach verfügt.  <br/> |[Hinzufügen des Benutzers als Stellvertretung](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) für das Postfach, bevor versucht wird, seine Berechtigungen zu aktualisieren oder zu entfernen.  <br/> |
|ErrorDelegateNoUser  <br/> |Ändern von Stellvertretungsberechtigungen für einen Benutzer, der sich nicht im Active Directory Domain Service (AD DS) befindet.  <br/> |Erstellen des Benutzers in AD DS oder Korrigieren der Delegatinformationen in der Anforderung.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |Verwenden Sie einen Delegaten, um Benachrichtigungen im Namen des Postfachbesitzers zu abonnieren.  <br/> |Abonnieren von Benachrichtigungen als Postfachbesitzer.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |Stellen Sie eine Anforderung von einem Delegaten, der eine andere Serverversion als der Postfachserver des Prinzipals aufweist.  <br/> |Verwenden eines Delegaten oder Hinzufügen eines Delegaten, dessen Postfach die gleiche Serverversion wie der Postfachbesitzer hat.  <br/> |
|ErrorMissingEmailAddress  <br/> |Stellen Sie eine Anforderung mithilfe eines Stellvertretungskontos, das nicht über ein Postfach verfügt.  <br/> |Hinzufügen eines Postfachs zum Konto der Stellvertretung.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

