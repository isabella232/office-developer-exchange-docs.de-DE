---
title: Fehlerbehandlung Delegierung-bezogene in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 631d364f-e324-4838-a92c-820286f771f8
description: Erfahren Sie, wie Sie mit Delegierungs Fehlern in Anwendungen umgehen, die Sie mit dem verwaltete EWS-API oder EWS in Exchange entwickeln.
ms.openlocfilehash: 145783c4e7f49ed6e2aa3a2dbe0d10909e06d7e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455352"
---
# <a name="handling-delegation-related-errors-in-ews-in-exchange"></a>Fehlerbehandlung Delegierung-bezogene in EWS in Exchange

Erfahren Sie, wie Sie mit Delegierungs Fehlern in Anwendungen umgehen, die Sie mit dem verwaltete EWS-API oder EWS in Exchange entwickeln.
  
Wenn Ihre Anwendung Delegierung verwendet oder Delegaten hinzugefügt oder entfernt, müssen Sie möglicherweise Delegierungs bezogene Fehler behandeln. Sie können diese Fehler zur Laufzeit oder während der Entwicklung ihrer EWS-Anwendung behandeln. Diese Fehler werden durch die verwaltete EWS-API [Service Error](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) -Aufzählung und das EWS- [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element definiert. 
  
## <a name="delegation-related-errors"></a>Delegierungs bezogene Fehler

|**Error**|**Tritt auf, wenn Sie versuchen,...**|**Behandeln von...**|
|:-----|:-----|:-----|
|ErrorItemNotFound  <br/> ErrorFolderNotFound  <br/> |Führen Sie einen Vorgang für ein Postfach, einen Ordner oder ein Element aus, auf das Sie keinen Zugriff haben.  <br/> |Aktualisieren der Berechtigungen der Stellvertretung, damit diese auf den Ordner oder das Element zugreifen können, indem Sie die [UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode oder den [UpdateDelegate](https://msdn.microsoft.com/library/03f618ac-ad1a-4772-9b81-c5bb0f12d6ab%28Office.15%29.aspx) -EWS-Vorgang aufrufen und dann die Anforderung erneut ausprobieren.  <br/> |
|ErrorAccessDenied  <br/> |Ändern eines Elements, für das Sie nicht über ausreichende Berechtigungen zum Ändern verfügen.  <br/> |Aktualisieren der Stell Vertretungs Berechtigungen durch Aufrufen der **UpdateDelegate** verwaltete EWS-API-Methode oder des **UpdateDelegate** -EWS-Vorgangs und erneutes Testen der Anforderung.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |Versuchen Sie, den Postfachbesitzer als Stellvertreter zu Ihrem eigenen Postfach hinzuzufügen.  <br/> |[Hinzufügen eines anderen Benutzers als Stellvertreter](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md), nicht des Postfachbesitzers.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |Fügen Sie die Stellvertretung hinzu, wenn die Stellvertretung bereits vorhanden ist.  <br/> |Nichts zu tun, da die Stellvertretung bereits für den Postfachbesitzer vorhanden ist. Wenn Sie versuchen, die Berechtigungen eines vorhandenen Delegaten zu ändern, verwenden Sie die **UpdateDelegates** -Methode oder den **UpdateDelegate** -Vorgang.  <br/> |
|ErrorNotDelegate  <br/> |Ändern Sie Stellvertretungsberechtigungen für einen Benutzer, der über keine Stell Vertretungs Berechtigungen für das Postfach verfügt.  <br/> |[Hinzufügen des Benutzers als Stellvertreter](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) für das Postfach, bevor versucht wird, seine Berechtigungen zu aktualisieren oder zu entfernen.  <br/> |
|ErrorDelegateNoUser  <br/> |Ändern Sie Stellvertretungsberechtigungen für einen Benutzer, der sich nicht in Active Directory Domänendienst befindet (AD DS).  <br/> |Erstellen des Benutzers in AD DS oder korrigieren der Stellvertreter Informationen in der Anforderung.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |Verwenden Sie einen Delegaten, um Benachrichtigungen im Namen des Postfachbesitzers zu abonnieren.  <br/> |Abonnieren von Benachrichtigungen als Postfachbesitzer.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |Stellen Sie eine Anforderung von einem Delegaten mit einer anderen Server Version als dem Postfachserver des Prinzipals an.  <br/> |Verwenden einer Stellvertretung oder Hinzufügen einer Stellvertretung, deren Postfach dieselbe Server Version wie der Postfachbesitzer hat.  <br/> |
|ErrorMissingEmailAddress  <br/> |Stellen Sie eine Anforderung mithilfe eines Stellvertretungs Kontos, das kein Postfach besitzt.  <br/> |Hinzufügen eines Postfachs zum Konto des Stellvertreters.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Tools und Ressourcen für die Problembehandlung bei EWS-Anwendungen für Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

