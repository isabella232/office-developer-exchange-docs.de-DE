---
title: Persistent Anwendungseinstellungen in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 394d4e70-8517-4073-809a-5b61780ff923
description: Erfahren Sie mehr über die verschiedenen Optionen, die Ihre verwaltete EWS-API oder EWS-Anwendung zum Erstellen persistenter benutzerdefinierter Anwendungseinstellungen in Exchange verwenden kann.
ms.openlocfilehash: 3fdc7ad3d5acabf6b498743afe8d93f0eff048c3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516138"
---
# <a name="persistent-application-settings-in-ews-in-exchange"></a>Persistent Anwendungseinstellungen in EWS in Exchange

Erfahren Sie mehr über die verschiedenen Optionen, die Ihre verwaltete EWS-API oder EWS-Anwendung zum Erstellen persistenter benutzerdefinierter Anwendungseinstellungen in Exchange verwenden kann.
  

  
Die einfachste Möglichkeit, benutzerdefinierte Clientkonfigurationen für ein Postfach oder Ordner und Elemente in einem Postfach synchron zu halten, besteht darin, Anwendungseinstellungen auf einem Exchange Server zu speichern. Sie können sicherstellen, dass diese Einstellungen für ein Postfach beibehalten werden, indem Sie eine der folgenden Optionen verwenden: 
  
- Benutzerkonfigurationsobjekte
    
- Erweiterte Eigenschaften
    
- Benutzerdefinierte Elemente
    
## <a name="what-are-my-options-for-creating-persistent-application-settings"></a>Welche Optionen habe ich für das Erstellen persistenter Anwendungseinstellungen?
<a name="Options"> </a>

Benutzerkonfigurationsobjekte sind die beste Option zum Speichern von Konfigurationseinstellungen für Ihre EWS-Clientanwendungen. Sie können auch Erweiterungseigenschaften oder benutzerdefinierte Elemente oder eine Kombination aller drei Elemente verwenden. Wählen Sie Ihre Option basierend auf dem Umfang Ihrer Einstellungen und ob Ihre Einstellungen für andere Anwendungen verfügbar sein müssen.
  
**Tabelle 1. Empfohlene Optionen zum Erstellen persistenter Anwendungseinstellungen basierend auf dem Bereich**

|**Festlegen des Bereichs**|**Verwendung**|**Zugriff durch**|
|:-----|:-----|:-----|
|Element  <br/> |Eine erweiterte Eigenschaft für ein vorhandenes Element.  <br/> |Eine beliebige EWS-Anwendung. Nur EWS-Clients, die den Eigenschaftenbezeichner kennen, können auf eine erweiterte Eigenschaft zugreifen.  <br/> |
|Ordner  <br/> |Ein Benutzerkonfigurationsobjekt im Zielordner. Dies ist eine gute Möglichkeit zum Speichern von Ansichtseinstellungen für einen Ordner.  <br/> |Eine beliebige EWS-Anwendung.  <br/> |
|Postfach  <br/> |Ein Benutzerkonfigurationsobjekt im Standardordner "msgrootfolder".  <br/> |Eine beliebige EWS-Anwendung.  <br/> |
   
### <a name="user-configuration-objects"></a>Benutzerkonfigurationsobjekte
<a name="UserConfig"> </a>

Benutzerkonfigurationsobjekte sind spezielle Elemente, die Ordnern in einem Postfach zugeordnet sind. Benutzerkonfigurationsobjekte, auch als Ordner zugeordnete Elemente bezeichnet, sind in der Regel die beste Option zum Beibehalten von Anwendungseinstellungen, insbesondere, wenn die Konfigurationsinformationen einem Ordner oder Postfach zugeordnet sind. Sie werden in der Regel nicht für Endbenutzer angezeigt. Da sie Datenströme und Datenwörterbücher nativ speichern können, eignen sie sich ideal zum Speichern von Konfigurationsinformationen. Die beste Möglichkeit zum Verwenden von Benutzerkonfigurationsobjekten besteht darin, eine Reihe von Konfigurationen in einem XML-Dokument zu speichern und diese Informationen dann in einer der Eigenschaften des Benutzerkonfigurationsstreams zu speichern.
  
Auf Benutzerkonfigurationsobjekte wird anders zugegriffen als auf die anderen in einem Postfach gespeicherten Elementtypen. Sie können die verwaltete EWS-API-Methode [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=EXCHG.80%29.aspx) oder den [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS-Vorgang verwenden, um alle Elemente zu suchen. Sie müssen jedoch die Option **"Zugeordnete** Suche durchlaufen" verwenden, um Benutzerkonfigurationsobjekte zu suchen. Das Traversal der **zugeordneten** Suche gibt an, dass die Suchergebnisse nur Benutzerkonfigurationsobjekte enthalten sollen. EWS enthält eine Reihe von Vorgängen, die für Benutzerkonfigurationsobjekte spezifisch sind. 
  
**Tabelle 1. EWS-Vorgänge und EWS Managed API-Methoden zum Arbeiten mit Benutzerkonfigurationsobjekten**

|**Gewünschte Aktion**|**Zu verwendender EWS-Vorgang**|**Verwenden dieser verwalteten EWS-API-Methode**|
|:-----|:-----|:-----|
|Erstellen eines Benutzerkonfigurationsobjekts  <br/> |[CreateUserConfiguration-Vorgang](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) <br/> |[UserConfiguration.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) <br/> |
|Abrufen eines Benutzerkonfigurationsobjekts  <br/> |[GetUserConfiguration-Vorgang](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |[UserConfiguration.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> [UserConfiguration.Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.load%28v=exchg.80%29.aspx) <br/> |
|Aktualisieren eines Benutzerkonfigurationsobjekts  <br/> |[UpdateUserConfiguration-Vorgang](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) <br/> |[UserConfiguration.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> |
|Löschen eines Benutzerkonfigurationsobjekts  <br/> |[DeleteUserConfiguration-Vorgang](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |
   
> [!NOTE]
> Benutzerkonfigurationsobjekte, die mithilfe von EWS erstellt wurden, verfügen über ein [ItemClass-Präfix,](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) das mit "IPM" beginnt. Configuration.". Die **ItemClass** eines Benutzerkonfigurationsobjekts ist das Präfix des Benutzerkonfigurationsobjekts und der Name des Benutzerkonfigurationsobjekts. Sie können die eigenschaft ["Item.ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API" oder das **Element "ItemClass** EWS" verwenden, um nach von Ihnen definierten Benutzerkonfigurationsobjekten zu suchen. 
  
### <a name="extended-properties"></a>Erweiterte Eigenschaften
<a name="ExtendedProperties"> </a>

Verwenden Sie [erweiterte Eigenschaften,](properties-and-extended-properties-in-ews-in-exchange.md) wenn Sie Konfigurationsinformationen für Elemente speichern möchten. EWS gibt im Gegensatz zur MAPI keinen Eigenschaftenbehälter für Elemente zurück. Dies bedeutet, dass ein EWS-Client den Bezeichner der erweiterten Eigenschaft kennen muss, um die erweiterte Eigenschaft zu suchen und darauf zuzugreifen. Wenn Sie Konfigurationsinformationen für andere Elemente als Benutzerkonfigurationsobjekte speichern müssen, kann die Verwendung erweiterter Eigenschaften zum Erstellen benutzerdefinierter Eigenschaften die Lösung für Sie sein. Mit erweiterten Eigenschaften können Sie auf Informationen zu Eigenschaften zugreifen und diese speichern, die nicht Teil des Standardeigenschaftensatzes für ein Element sind. 
  
> [!IMPORTANT]
> Das Exchange Datenbankschema verfügt über eine begrenzte Anzahl von Eigenschaften. Die maximale Anzahl von Eigenschaftsbezeichnern für eine Exchange Datenbank beträgt 32.767. Wenn Sie erweiterte Eigenschaften verwenden, um viele Einstellungen zu speichern, empfehlen wir, diese Einstellungen mit einer einzigen erweiterten Eigenschaft zu speichern, damit Sie diesen Höchstwert nicht überschreiten. 
  
Sie können die verwaltete EWS-API-Methode [Item.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=EXCHG.80%29.aspx) oder den [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS-Vorgang verwenden, um erweiterte Eigenschaften für Benutzerkonfigurationsobjekte festzulegen. 
  
### <a name="custom-items"></a>Benutzerdefinierte Elemente
<a name="CustomItems"> </a>

Benutzerdefinierte Elemente können auch zum Speichern von Informationen verwendet werden. Die vorhandenen Elementeigenschaften können so umfunktioniert werden, dass sie Konfigurationsinformationen enthalten. Sie können auch erweiterte Eigenschaften verwenden, um Ihre eigenen Eigenschaften für Ihre Anwendung zu definieren. Die Verwendung von benutzerdefinierten Elementen zum Speichern der Konfiguration bietet die folgenden Vorteile: 
  
- Sie funktionieren für alle Versionen von Exchange, die EWS unterstützen.
    
- Wenn Sie keine erweiterten Eigenschaften für das Element verwenden, wird das Budget Exchange Eigenschaften nicht berechnet.
    
## <a name="where-should-i-store-my-application-settings"></a>Wo sollte ich meine Anwendungseinstellungen speichern?
<a name="ApplicationSettingsLocation"> </a>

Postfachordner und die darin enthaltenen Elemente befinden sich im Stammnachrichtenordner. Dieser Ordner wird durch den [Wert "WellKnownFolderName.msgfolderroot"](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) in der verwalteten EWS-API identifiziert. In MAPI-Begriffen entspricht dies der IPM-Unterstruktur eines Postfachs. Benutzerkonfigurationsobjekte werden häufig zum Erstellen benutzeroberflächenbasierter Einstellungen verwendet, sodass eine Anwendung Ansichtseinstellungen basierend auf dem Ordner rendern kann, auf den ein Benutzer zugreift. Ordnerbasierte Ansichtseinstellungen werden in der Regel für ein Benutzerkonfigurationsobjekt festgelegt, das dem Ordner zugeordnet ist. Aber manchmal möchten Sie Ihre Einstellungen für Ihre Anwendung global festlegen. In diesem Fall können Sie Ihre Einstellungen im Stammnachrichtenordner speichern. 
  
Die meisten Benutzer sind sich dessen nicht bewusst und greifen in der Regel nicht auf den Stammpostfachordner zu. Dieser Ordner wird durch den [Wert "WellKnownFolderName.root"](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) in der verwalteten EWS-API identifiziert. In MAPI-Begriffen entspricht dies der Nicht-IPM-Unterstruktur eines Postfachs. Informationen, auf die Endbenutzer nicht direkt zugreifen, werden im Stammpostfachordner gespeichert. Möglicherweise möchten Sie ihre Anwendungseinstellung in diesem Ordner speichern, da Clientanwendungen in der Regel nicht darauf zugreifen. 
  
## <a name="version-differences"></a>Versionsunterschiede
<a name="VersionDifferences"> </a>

Benutzerkonfigurationsobjekte sind ab Exchange 2010 in Exchange Online, Exchange Online als Teil Office 365 und Versionen von Exchange verfügbar.
  
## <a name="see-also"></a>Siehe auch


- [Persistente Anwendungseinstellungen mithilfe von EWS in Exchange verwalten](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    
- [Eigenschaften und erweiterte Eigenschaften in EWS in Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Arbeiten mit Ordnern unter Verwendung von EWS in Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Arbeiten mit Exchange-Postfachelementen mithilfe von EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    

