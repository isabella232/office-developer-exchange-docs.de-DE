---
title: Persistent Anwendungseinstellungen in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394d4e70-8517-4073-809a-5b61780ff923
description: Informationen Sie über die verschiedenen Optionen, dass die EWS Managed API oder EWS-Anwendung zum Erstellen von persistent benutzerdefinierte Anwendungseinstellungen in Exchange verwenden kann.
ms.openlocfilehash: b384fd5608dc647950d7cd31e861e24c12e3316f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757121"
---
# <a name="persistent-application-settings-in-ews-in-exchange"></a>Persistent Anwendungseinstellungen in EWS in Exchange

Informationen Sie über die verschiedenen Optionen, dass die EWS Managed API oder EWS-Anwendung zum Erstellen von persistent benutzerdefinierte Anwendungseinstellungen in Exchange verwenden kann.
  

  
Die einfachste Möglichkeit, benutzerdefinierte Client-Konfigurationen für ein Postfach oder Ordner und Elemente in einem Postfach synchron ist Anwendungseinstellungen auf einem Exchange-Server gespeichert werden. Sie können sicherstellen, dass diese Einstellungen für ein Postfach beibehalten werden, mithilfe einer der folgenden: 
  
- Konfiguration der Benutzerobjekte
    
- Erweiterte Eigenschaften
    
- Benutzerdefinierte Elemente
    
## <a name="what-are-my-options-for-creating-persistent-application-settings"></a>Was sind meine Optionen zum Erstellen von persistent Anwendungseinstellungen?
<a name="Options"> </a>

Konfiguration der Benutzerobjekte sind die beste Option zum Speichern von Konfigurationseinstellungen für den EWS-Clientanwendungen. Sie können auch Eigenschaften oder benutzerdefinierte Elemente oder eine Kombination aus allen drei erweitern. Wählen Sie die Option basierend auf den Bereich der Einstelllungen und gibt an, ob die Einstellungen für andere Clientanwendungen verfügbar sein müssen.
  
**In Tabelle 1. Empfohlene Optionen zum Erstellen von persistent Anwendungseinstellungen basierend auf Bereich**

|**Festlegen des Bereichs**|**Verwenden Sie...**|**Diensten zugegriffen wird.Handbuch herunterladen**|
|:-----|:-----|:-----|
|Element  <br/> |Erweiterte Eigenschaft für ein vorhandenes Element.  <br/> |Alle EWS-Anwendung. Nur EWS-Clients, die die Eigenschaftenbezeichner kennen, können eine erweiterte Eigenschaft zugreifen.  <br/> |
|Ordner  <br/> |Ein Benutzer-Konfigurationsobjekt für den Zielordner. Dies ist eine gute Möglichkeit zum Speichern von Einstellungen für die Ansicht für einen Ordner.  <br/> |Alle EWS-Anwendung.  <br/> |
|Postfach  <br/> |Ein Benutzer-Konfigurationsobjekt auf den Standardordner Msgrootfolder.  <br/> |Alle EWS-Anwendung.  <br/> |
   
### <a name="user-configuration-objects"></a>Konfiguration der Benutzerobjekte
<a name="UserConfig"> </a>

Konfiguration der Benutzerobjekte sind spezielle Elemente, die Ordner in einem Postfach zugeordnet sind. Konfiguration Benutzerobjekte, auch bekannt als Elemente von Ordner verknüpft ist, sind in der Regel die beste Möglichkeit zum Speichern von Anwendungseinstellungen, insbesondere dann, wenn die Konfigurationsinformationen eines Ordners oder ein Postfach zugeordnet ist. Sie sind nicht in der Regel für Endbenutzer angezeigt. Da systemintern Datenströme und Wörterbücher Daten gespeichert werden können, werden sie zum Speichern von Konfigurationsinformationen ideal. Die beste Möglichkeit zum Benutzerobjekte Konfiguration verwenden werden eine Reihe von Konfigurationen in einem XML-Dokument zu speichern, und speichern Sie diese Informationen in einem Stream-Objekt die Benutzereigenschaften-Konfiguration ab.
  
Konfiguration der Benutzerobjekte erfolgt anders als die anderen Typen von Elementen in einem Postfach gespeichert. Sie können die [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=EXCHG.80%29.aspx) EWS Managed API-Methode oder die [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS-Vorgang nach allen Elementen gesucht, doch Sie müssen die Option **zugeordneter** Suche durchqueren verwenden, um Benutzerobjekte Konfiguration finden. Der **zugeordnete** Suche Durchlauf gibt an, dass die Ergebnisse der Konfiguration nur Benutzerobjekte enthalten soll. EWS enthält eine Reihe von Operationen, die für die Konfiguration der Benutzerobjekte spezifisch sind. 
  
**In Tabelle 1. EWS-Vorgänge und EWS Managed API-Methoden zum Arbeiten mit der Konfiguration der Benutzerobjekte**

|**Gewünschte Aktion**|**Zu verwendender EWS-Vorgang**|**Verwenden Sie diese Methode EWS Managed API**|
|:-----|:-----|:-----|
|Erstellen Sie eine Benutzer-Konfigurationsobjekt  <br/> |[CreateUserConfiguration-Vorgang](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) <br/> |[UserConfiguration.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) <br/> |
|Abrufen einer Benutzer-Konfigurationsobjekt  <br/> |[GetUserConfiguration-Vorgang](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |[UserConfiguration.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> [UserConfiguration.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.load%28v=exchg.80%29.aspx) <br/> |
|Aktualisieren einer Benutzer-Konfigurationsobjekt  <br/> |[UpdateUserConfiguration-Vorgang](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) <br/> |[UserConfiguration.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> |
|Löschen einer Benutzer-Konfigurationsobjekt  <br/> |[DeleteUserConfiguration-Vorgang](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |
   
> [!NOTE]
> Benutzerobjekte-Konfiguration mithilfe des EWS erstellt haben, ein Präfix für den [ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) , die mit "IPM. beginnt Konfiguration. ". Die **ItemClass** eines Benutzers Configuration-Objekts ist das Präfix des Benutzers Konfiguration-Objekt und Ihr Benutzername des Configuration-Objekts. Sie können die [Item.ItemClass](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API-Eigenschaft oder das **ItemClass** EWS-Element um für Benutzerobjekte Konfiguration zu suchen, die Sie definiert haben. 
  
### <a name="extended-properties"></a>Erweiterte Eigenschaften
<a name="ExtendedProperties"> </a>

Wenn Sie Konfigurationsinformationen für Elemente speichern möchten, verwenden Sie [Erweiterte Eigenschaften](properties-and-extended-properties-in-ews-in-exchange.md) . EWS, im Gegensatz zu MAPI, gibt keinen Eigenschaftenbehälter für Elemente zurück. Dies bedeutet, dass ein EWS-Client den erweiterten Eigenschaftenbezeichner, um die Suche und Zugriff auf die erweiterte Eigenschaft wissen muss. Wenn Sie zum Speichern von Konfigurationsinformationen für Elemente als Benutzerobjekte Konfiguration müssen, kann die Nutzung der erweiterten Eigenschaften zum Erstellen von benutzerdefinierter Eigenschaften der Lösung für Sie sein. Erweiterte Eigenschaften können Sie zugreifen, und Speichern von Informationen auf Eigenschaften, die nicht Teil der standard-Eigenschaft für ein Element festgelegt sind. 
  
> [!IMPORTANT]
> Das Exchange-Datenbankschema verfügt über eine begrenzte Anzahl von Eigenschaften. Die maximale Anzahl von Eigenschaftenbezeichner für eine Exchange-Datenbank ist 32.767. Wenn Sie viele Einstellungen gespeichert werden erweiterte Eigenschaften verwenden, empfehlen wir, dass Sie einen einzelnen erweiterten Eigenschaft verwenden, um diese Einstellungen speichern, damit Sie diese Obergrenze nicht überschreiten. 
  
Sie können die [Item.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=EXCHG.80%29.aspx) EWS Managed API-Methode oder die [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS-Vorgang verwenden, um erweiterte Eigenschaften für Benutzerobjekte Konfiguration festzulegen. 
  
### <a name="custom-items"></a>Benutzerdefinierte Elemente
<a name="CustomItems"> </a>

Benutzerdefinierte Elemente können auch verwendet werden, um Informationen zu speichern. Eigenschaften der vorhandenen können zugewiesen werden, um Konfigurationsinformationen enthalten. Oder Sie können erweiterte Eigenschaften verwenden, um Ihre eigene Eigenschaften für die Anwendung zu definieren. Die Verwendung benutzerdefinierter Elemente zum Speichern der Konfiguration bietet folgende Vorteile: 
  
- Sie arbeiten für alle Versionen von Exchange, EWS unterstützen.
    
- Wenn Sie erweiterte Eigenschaften für das Element nicht verwenden, wird das Budget der Eigenschaften von Exchange nicht berechnet.
    
## <a name="where-should-i-store-my-application-settings"></a>Wo sollen die Einstellungen für meine Anwendung werden gespeichert?
<a name="ApplicationSettingsLocation"> </a>

Postfachordner und die darin enthaltenen Elemente befinden sich im Stammordner der Nachricht. Dieser Ordner wird durch den Wert [WellKnownFolderName.msgfolderroot](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) in die EWS Managed API identifiziert. MAPI-ausgedrückt ist dies das Äquivalent von IPM-Unterstruktur eines Postfachs. Konfiguration Benutzerobjekte sind häufig zur UI-basiertes Einstellungen zu erstellen, damit der Einstellungen für die Ansicht basierend auf den Ordner, der ein Benutzer den Zugriff auf ist eine Anwendung gerendert werden kann. Ansichtsoptionen für Ordner werden in der Regel auf eine Benutzer-Konfigurationsobjekt festgelegt, die dem Ordner zugeordnet ist. Aber in einigen Fällen möglicherweise sollen Einstelllungen global für die Anwendung. In diesem Fall können Sie Ihre Einstellungen im Stammordner Nachricht speichern. 
  
Die meisten Benutzer sind nicht kennen und in der Regel nicht den Stammordner des Postfachs zuzugreifen. Dieser Ordner wird durch den Wert [WellKnownFolderName.root](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) in die EWS Managed API identifiziert. MAPI-ausgedrückt ist dies das Äquivalent von der IPM Unterstruktur eines Postfachs an. Informationen, die Endbenutzer direkt zugreifen werden im Postfach Stammordner gespeichert. Möglicherweise möchten Ihre Anwendung Einstellung in diesem Ordner gespeichert werden, da Clientanwendungen nicht in der Regel, es zugreifen. 
  
## <a name="version-differences"></a>Versionsunterschiede
<a name="VersionDifferences"> </a>

Konfiguration der Benutzerobjekte sind in Exchange Online, Exchange Online als Teil von Office 365 und Exchange beginnend mit Exchange 2010-Versionen verfügbar.
  
## <a name="see-also"></a>Siehe auch


- [Verwalten der permanenten Anwendungseinstellungen mithilfe von EWS in Exchange](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    
- [Eigenschaften und erweiterte Eigenschaften in EWS in Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Arbeiten Sie mit Ordnern in Exchange mithilfe der Exchange-Webdienste](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Arbeiten Sie mit Exchange-Postfach-Elementen mithilfe von EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    

