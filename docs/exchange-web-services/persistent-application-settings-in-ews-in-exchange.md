---
title: Persistent Anwendungseinstellungen in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394d4e70-8517-4073-809a-5b61780ff923
description: In diesem Artikel erfahren Sie mehr über die verschiedenen Optionen, die Ihre verwaltete EWS-API oder EWS-Anwendung zum Erstellen beständiger benutzerdefinierter Anwendungseinstellungen in Exchange verwenden kann.
ms.openlocfilehash: b1faa057e5a0c1a96498efcc23738c83d25ae986
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457403"
---
# <a name="persistent-application-settings-in-ews-in-exchange"></a>Persistent Anwendungseinstellungen in EWS in Exchange

In diesem Artikel erfahren Sie mehr über die verschiedenen Optionen, die Ihre verwaltete EWS-API oder EWS-Anwendung zum Erstellen beständiger benutzerdefinierter Anwendungseinstellungen in Exchange verwenden kann.
  

  
Die einfachste Möglichkeit, benutzerdefinierte Clientkonfigurationen für ein Postfach oder Ordner und Elemente in einem Postfach synchron zu halten, besteht darin, Anwendungseinstellungen auf einem Exchange-Server zu speichern. Sie können sicherstellen, dass diese Einstellungen für ein Postfach mit einem der folgenden Werte dauerhaft gespeichert werden: 
  
- Benutzer Konfigurationsobjekte
    
- Erweiterte Eigenschaften
    
- Benutzerdefinierte Elemente
    
## <a name="what-are-my-options-for-creating-persistent-application-settings"></a>Welche Optionen habe ich zum Erstellen von Einstellungen für beständige Anwendungen?
<a name="Options"> </a>

Benutzer Konfigurationsobjekte sind die beste Option zum Speichern von Konfigurationseinstellungen für Ihre EWS-Clientanwendungen. Sie können auch Extend-Eigenschaften oder benutzerdefinierte Elemente oder eine Kombination aus allen drei verwenden. Wählen Sie Ihre Option basierend auf dem Bereich Ihrer Einstellungen und aus, ob Ihre Einstellungen für andere Anwendungen zur Verfügung stehen müssen.
  
**Tabelle 1. Empfohlene Optionen zum Erstellen von Einstellungen für beständige Anwendungen basierend auf dem Bereich**

|**Festlegen des Bereichs**|**Verwendung**|**Zugriff durch**|
|:-----|:-----|:-----|
|Element  <br/> |Eine erweiterte Eigenschaft für ein vorhandenes Element.  <br/> |Jede EWS-Anwendung. Nur EWS-Clients, die den Eigenschaftenbezeichner kennen, können auf eine erweiterte Eigenschaft zugreifen.  <br/> |
|Ordner  <br/> |Ein Benutzer Konfigurationsobjekt für den Zielordner. Dies ist eine gute Möglichkeit, Ansichtseinstellungen für einen Ordner zu speichern.  <br/> |Jede EWS-Anwendung.  <br/> |
|Postfach  <br/> |Ein Benutzer Konfigurationsobjekt im standardmäßigen msgrootfolder-Ordner.  <br/> |Jede EWS-Anwendung.  <br/> |
   
### <a name="user-configuration-objects"></a>Benutzer Konfigurationsobjekte
<a name="UserConfig"> </a>

Benutzer Konfigurationsobjekte sind spezielle Elemente, die Ordnern in einem Postfach zugeordnet sind. Benutzer Konfigurationsobjekte, die auch als Ordner zugeordnete Elemente bezeichnet werden, sind in der Regel die beste Option zum Speichern von Anwendungseinstellungen, insbesondere dann, wenn die Konfigurationsinformationen einem Ordner oder einem Postfach zugeordnet sind. Sie werden normalerweise nicht für Endbenutzer aufgetaucht. Da Sie Datenströme und Daten Wörterbücher nativ speichern können, eignen Sie sich ideal zum Speichern von Konfigurationsinformationen. Die beste Möglichkeit zum Verwenden von Benutzer Konfigurationsobjekten besteht darin, eine Reihe von Konfigurationen in einem XML-Dokument zu speichern und diese Informationen dann in einer der Eigenschaften des Benutzerkonfigurationsdaten Stroms zu speichern.
  
Der Zugriff auf Benutzer Konfigurationsobjekte erfolgt unterschiedlich als die anderen Elementtypen, die in einem Postfach gespeichert sind. Sie können die [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=EXCHG.80%29.aspx) verwaltete EWS-API-Methode oder den [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -EWS-Vorgang verwenden, um nach allen Elementen zu suchen, aber Sie müssen die Option **zugeordnete** Such Traversal verwenden, um Benutzer Konfigurationsobjekte zu finden. Der **zugeordnete** Such Durchlauf gibt an, dass die Suchergebnisse nur Benutzer Konfigurationsobjekte enthalten sollen. EWS enthält eine Reihe von Vorgängen, die für Benutzer Konfigurationsobjekte spezifisch sind. 
  
**Tabelle 1. EWS-Vorgänge und verwaltete EWS-API Methoden zum Arbeiten mit Benutzer Konfigurationsobjekten**

|**Gewünschte Aktion**|**Zu verwendender EWS-Vorgang**|**Verwenden Sie diese verwaltete EWS-API-Methode**|
|:-----|:-----|:-----|
|Erstellen eines Benutzer Konfigurationsobjekts  <br/> |[CreateUserConfiguration-Vorgang](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) <br/> |[UserConfiguration. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) <br/> |
|Abrufen eines Benutzer Konfigurationsobjekts  <br/> |[GetUserConfiguration-Vorgang](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |[UserConfiguration. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> [UserConfiguration. Laden](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.load%28v=exchg.80%29.aspx) <br/> |
|Aktualisieren eines Benutzer Konfigurationsobjekts  <br/> |[UpdateUserConfiguration-Vorgang](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) <br/> |[UserConfiguration. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> |
|Löschen eines Benutzer Konfigurationsobjekts  <br/> |[DeleteUserConfiguration-Vorgang](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |
   
> [!NOTE]
> Benutzer Konfigurationsobjekte, die mit EWS erstellt wurden, weisen ein [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) -Präfix auf, das mit "IPM beginnt. Konfiguration. ". Das **ItemClass** eines Benutzer Konfigurationsobjekts ist das Benutzer Konfigurationsobjekt Präfix und Ihr Benutzer Konfigurationsobjekt Name. Sie können die [Item. ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) verwaltete EWS-API-Eigenschaft oder das **ItemClass** -EWS-Element verwenden, um nach Benutzer Konfigurationsobjekten zu suchen, die Sie definiert haben. 
  
### <a name="extended-properties"></a>Erweiterte Eigenschaften
<a name="ExtendedProperties"> </a>

Verwenden Sie [Erweiterte Eigenschaften](properties-and-extended-properties-in-ews-in-exchange.md) , wenn Sie Konfigurationsinformationen zu Elementen speichern möchten. Im Gegensatz zu MAPI gibt EWS keinen Eigenschaftenbehälter für Elemente zurück. Dies bedeutet, dass ein EWS-Client den erweiterten Eigenschaftenbezeichner kennen muss, um nach der erweiterten Eigenschaft zu suchen und darauf zuzugreifen. Wenn Sie Konfigurationsinformationen für andere Elemente als Benutzer Konfigurationsobjekte speichern müssen, ist die Lösung für Sie möglicherweise mithilfe erweiterter Eigenschaften zum Erstellen benutzerdefinierter Eigenschaften. Erweiterte Eigenschaften ermöglichen den Zugriff auf und das Speichern von Informationen zu Eigenschaften, die nicht Teil des Standard-Eigenschaftensatzes für ein Element sind. 
  
> [!IMPORTANT]
> Das Exchange-Datenbankschema verfügt über eine begrenzte Anzahl von Eigenschaften. Die maximale Anzahl von Eigenschaftenbezeichnern für eine Exchange-Datenbank lautet 32.767. Wenn Sie erweiterte Eigenschaften zum Speichern vieler Einstellungen verwenden, wird empfohlen, dass Sie eine einzelne erweiterte Eigenschaft zum Speichern dieser Einstellungen verwenden, damit Sie diesen Höchstwert nicht überschreiten. 
  
Sie können die [Item. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=EXCHG.80%29.aspx) verwaltete EWS-API-Methode oder den [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) -EWS-Vorgang verwenden, um erweiterte Eigenschaften für Benutzer Konfigurationsobjekte festzulegen. 
  
### <a name="custom-items"></a>Benutzerdefinierte Elemente
<a name="CustomItems"> </a>

Benutzerdefinierte Elemente können auch zum Speichern von Informationen verwendet werden. Die vorhandenen Elementeigenschaften können umfunktioniert werden, um Konfigurationsinformationen zu enthalten. Sie können auch erweiterte Eigenschaften verwenden, um Ihre eigenen Eigenschaften für Ihre Anwendung zu definieren. Die Verwendung benutzerdefinierter Elemente zum Speichern der Konfiguration bietet die folgenden Vorteile: 
  
- Sie funktionieren für alle Versionen von Exchange, die EWS unterstützen.
    
- Wenn Sie keine erweiterten Eigenschaften für das Element verwenden, wird das Budget von Exchange-Eigenschaften nicht aufgeladen.
    
## <a name="where-should-i-store-my-application-settings"></a>Wo sollte ich meine Anwendungseinstellungen speichern?
<a name="ApplicationSettingsLocation"> </a>

Postfachordner und die darin enthaltenen Elemente befinden sich im Stamm Nachrichten Ordner. Dieser Ordner wird durch den [WellKnownFolderName. msgfolderroot-](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) Wert in der verwaltete EWS-API identifiziert. In MAPI-Ausdrücken entspricht dies der IPM-Unterstruktur eines Postfachs. Benutzer Konfigurationsobjekte werden häufig verwendet, um benutzeroberflächenbasierte Einstellungen zu erstellen, damit eine Anwendung Ansichtseinstellungen basierend auf dem Ordner rendern kann, auf den ein Benutzer zugreift. Ordnerbasierte Ansichtseinstellungen werden normalerweise für ein Benutzer Konfigurationsobjekt festgelegt, das dem Ordner zugeordnet ist. Es kann jedoch vorkommen, dass Sie die Einstellungen global für Ihre Anwendung festlegen möchten. In diesem Fall können Sie die Einstellungen im Stamm Nachrichten Ordner speichern. 
  
Die meisten Benutzer kennen den Stamm Postfachordner nicht und greifen in der Regel nicht auf diesen zu. Dieser Ordner wird durch den Wert [WellKnownFolderName. root](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) im verwaltete EWS-API identifiziert. In MAPI-Ausdrücken entspricht dies der nicht-IPM-Unterstruktur eines Postfachs. Informationen, auf die Endbenutzer nicht direkt zugreifen, werden im Stamm Postfachordner gespeichert. Möglicherweise möchten Sie die Anwendungseinstellung in diesem Ordner speichern, da Clientanwendungen normalerweise nicht darauf zugreifen. 
  
## <a name="version-differences"></a>Versionsunterschiede
<a name="VersionDifferences"> </a>

Benutzer Konfigurationsobjekte stehen auf Exchange Online zur Verfügung, Exchange Online im Rahmen von Office 365 und Exchange-Versionen, die mit Exchange 2010 beginnen.
  
## <a name="see-also"></a>Siehe auch


- [Persistente Anwendungseinstellungen mithilfe von EWS in Exchange verwalten](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    
- [Eigenschaften und erweiterte Eigenschaften in EWS in Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Arbeiten mit Ordnern unter Verwendung von EWS in Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Arbeiten mit Exchange-Postfachelementen mithilfe von EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    

