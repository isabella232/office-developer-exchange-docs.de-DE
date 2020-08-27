---
title: Identitätswechsel und EWS in Exchange
manager: sethgros
ms.date: 08/24/2020
ms.audience: Developer
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: Erfahren Sie mehr über den Identitätswechsel und wann er in Ihren Exchange-Dienstanwendungen eingesetzt werden kann.
localization_priority: Priority
ms.openlocfilehash: da35fb04f316c21a1c85c71b789b7f1485653466
ms.sourcegitcommit: 636c05a929279812c6ef87d75b01c166a4a05584
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "47254972"
---
# <a name="impersonation-and-ews-in-exchange"></a>Identitätswechsel und EWS in Exchange

Erfahren Sie mehr über den Identitätswechsel und wann er in Ihren Exchange-[Dienstanwendungen](ews-application-types.md) eingesetzt werden kann.
  
Benutzer können mithilfe der folgenden drei Möglichkeiten auf Postfächer anderer Benutzer zugreifen:
  
- Durch das Hinzufügen von Stellvertretungen und dem Angeben von Berechtigungen für die einzelnen Stellvertreter
    
- Durch direktes Ändern der Ordnerberechtigungen
    
- Durch Verwenden eines Identitätswechsels
    
Wann sollten eher der Identitätswechsel als Stellvertreter oder Ordnerberechtigungen eingesetzt werden? Die folgenden Richtlinien unterstützen Sie bei der Entscheidung:
  
- Verwenden Sie Ordnerberechtigungen, wenn Sie einen Benutzerzugriff auf einen Ordner bereitstellen möchten, dem Benutzer jedoch keine „Senden im Auftrag von"-Berechtigungen geben möchten. 
    
- Verwenden Sie den Stellvertreterzugriff , wenn Sie einem Benutzer die Berechtigung erteilen möchten, Arbeiten im Auftrag eines anderen Benutzers durchzuführen. In der Regel handelt es sich dabei um eine 1:1- oder 1:viele-Berechtigung - beispielsweise ein einzelner Verwaltungsassistent, der den Kalender für einen Administrator verwaltet, oder ein einzelner Raumbelegungsplaner, der die Kalender für eine Gruppe von Besprechungsräumen verwaltet.
    
- Verwenden Sie den Identitätswechsel, wenn Sie eine Dienstanwendung haben, die auf mehrere Postfächer zugreifen muss und als Postfachbesitzer agieren soll.
    
Der Identitätswechsel ist die beste Wahl für den Umgang mit mehreren Postfächern, da Sie einfach einem Dienstkonto die Berechtigung erteilen können, auf alle Postfächer in einer Datenbank zuzugreifen. Die Stellvertretung und Ordnerberechtigungen sind die beste Wahl, wenn Sie nur einigen Benutzern den Zugriff gewähren, da Sie für jedes Postfach einzeln Berechtigungen hinzufügen müssen. Abbildung 1 veranschaulicht einige der Unterschiede zwischen den einzelnen Zugriffstypen.
  
**Abbildung 1. Möglichkeiten für den Zugriff auf Postfächer anderer Benutzer**

![Diagramm, das Postfachzugriffstypen, die die Beziehung zwischen dem/den Postfacheigentümer(n) und dem Delegaten für jeden Typ und den Berechtigungstyp zeigt. Senden im Namen von Berechtigungen für Delegation und/oder Ordnerberechtigungen. Senden als Berechtigungen für Identitätswechsel.](media/Ex15_Delegate_Overview.png)
  
Der Identitätswechsel ist ideal für Anwendungen, die eine Verbindung zu Exchange Online, Exchange Online als Teil von Office 365 und lokalen Versionen von Exchange herstellen und Vorgänge ausführen, wie z. B. das Archivieren von E-Mails, das automatische Einstellen von Abwesenheitsnachrichten für abwesende Benutzer oder eine andere Aufgabe, für die die Anwendung als Besitzer eines Postfachs agieren muss. Wenn eine Anwendung den Identitätswechsel zum Senden einer Nachricht verwendet, wird die E-Mail so angezeigt, als hätte Sie der Postfachbesitzer gesendet. Es gibt für den Empfänger keine Möglichkeit, herauszufinden, dass die Nachricht vom Dienstkonto versendet wurde. Die Stellvertretung hingegen erteilt einem anderen Postfachkonto die Berechtigung, im Auftrag eines Postfachbesitzers zu agieren. Wenn eine Nachricht durch einen Stellvertreter gesendet wird, identifiziert der „von"-Wert den Postfachbesitzer und der „Absender"-Wert den Stellvertreter, der die E-Mail versendet hat. 
  
## <a name="security-considerations-for-impersonation"></a>Sicherheitsaspekte für Identitätswechsel

Mit dem Identitätswechsel kann ein Aufrufer einen Identitätswechsel für ein angegebenes Benutzerkonto vornehmen. Dadurch kann der Aufrufer Vorgänge ausführen, indem er die Berechtigungen verwendet, die dem imitierten Konto zugeordnet sind, statt die Berechtigungen zu verwenden, die dem Konto des Aufrufers zugeordnet sind. Aus diesem Grund sollten Sie folgende Sicherheitsaspekte berücksichtigen:
  
- Nur Konten, denen von einem Exchange-Serveradministrator die **ApplicationImpersonation**-Rolle gewährt wurde, können den Identitätswechsel verwenden. 
    
- Sie sollten einen Verwaltungsbereich erstellen, der den Identitätswechsel auf eine bestimmte Kontogruppe begrenzt. Wenn Sie keinen Verwaltungsbereich erstellen, wird die **ApplicationImpersonation**-Rolle allen Konten in einem Unternehmen gewährt. 
    
- In der Regel wird die **ApplicationImpersonation**-Rolle einem Dienstkonto gewährt, das einer bestimmten Anwendung oder eine Gruppe von Anwendungen zugeordnet ist, statt einem Benutzerkonto. Sie können beliebig viele Dienstkonten erstellen. 
    
Sie können weitere Informationen über die [Konfiguration des Identitätswechsels](how-to-configure-impersonation.md) lesen, Sie sollten jedoch mit Ihrem Exchange-Administrator zusammenarbeiten, um zu gewährleisten, dass die erforderlichen Dienstkonten mit den [Berechtigungen und dem Zugriff](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) erstellt werden, der die Sicherheitsanforderungen Ihres Unternehmens erfüllt. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Konfigurieren eines Identitätswechsels](how-to-configure-impersonation.md)
    
- [Identifizieren des Kontos für Identitätswechsel](how-to-identify-the-account-to-impersonate.md)
    
- [Hinzufügen von Terminen mit Exchange-Identitätswechsel](how-to-add-appointments-by-using-exchange-impersonation.md)

## <a name="performance-considerations-for-ews-impersonation"></a>Überlegungen zur Leistung für EWS-Identitätswechsel

Wenn ein EWS-Identitätswechsel verwendet wird, sollte X-AnchorMailbox immer ordnungsgemäß festgelegt werden.  Andernfalls erhalten Sie möglicherweise die Fehlermeldungen 500 oder 503. Dies ist wichtig für die Leistung sowie für Benachrichtigungen mit Exchange Online/Exchange 2013.  Wenn Sie die Einstellung nicht festlegen, kann Sie die für die Ausführung des Aufrufs benötigte Zeit verdoppeln oder vervielfachen. In einigen Fällen können auch Timeouts auftreten. 
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Exchange 2013-Berechtigungen](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)
    

