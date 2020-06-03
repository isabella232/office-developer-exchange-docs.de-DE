---
title: Kommunizieren mit EWS unter Verwendung der verwalteten EWS-API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: d1b78293-da02-413a-875c-681e99146af3
description: Informationen dazu, wie Sie die verwaltete EWS-API zur Kommunikation mit EWS in Exchange verwenden.
localization_priority: Priority
ms.openlocfilehash: be807f2d936bf79d181476ec8eb12f20fca7950f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528244"
---
# <a name="communicate-with-ews-by-using-the-ews-managed-api"></a>Kommunizieren mit EWS unter Verwendung der verwalteten EWS-API

Informationen dazu, wie Sie die verwaltete EWS-API zur Kommunikation mit EWS in Exchange verwenden.
  
Die [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Klasse in der verwalteten EWS-API enthält die Methoden und Eigenschaften, die Sie zum Festlegen der Benutzeranmeldeinformationen, zum Identifizieren des EWS-Endpunkts, zum Senden und Empfangen von SOPA-Nachrichten und zum Konfigurieren der Bindung für die Kommunikation mit EWS verwenden. Bevor Sie die verwaltete EWS-API zum Durchführen von Aufgaben verwenden, müssen Sie eine Instanz der **ExchangeService** -Klasse verwenden und diese an EWS binden. 
  
Nachdem Sie ein [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) -Objekt mit Benutzeranmeldeinformationen und dem EWS-Endpunkt eingerichtet haben, können alle Postfachobjekte, die auf das [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) -Objekt verweisen, die folgenden Methodentypen für die Kommunikation mit EWS verwenden: 
  
- ExchangeService-Objektmethoden - Alle Methoden im **ExchangeService** -Objekt, die nicht vom Basis- **Object** -Typ geerbt werden, rufen EWS auf. 
    
- Methoden für Exchange-Postfachelement und Ordnertypen.
    
**Tabelle 1. Postfachelement- und Ordnertypmethoden, die mit EWS kommunizieren**

|Methode|Funktionsweise|Aufgerufene Vorgänge|
|:-----|:-----|:-----|
|[Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.load%28v=exchg.80%29.aspx) <br/> |Ruft Eigenschaften für ein Element, eine Anlage oder ein Benutzerkonfigurationsobjekt ab.  <br/> |[GetItem-Vorgang](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/><br/> [GetAttachment-Vorgang](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) <br/><br/> [GetUserConfiguration-Vorgang](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |
|[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |Füllt ein neues Element auf dem Client mit Informationen von einem vorhandenen Element auf dem Server.  <br/> |[GetItem Operation](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|[Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) <br/> |Speichert die Kopie des Clientelements auf dem Server.  <br/> |[UpdateItem Operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/> [UpdateFolder-Vorgang](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/><br/>[CreateItem Operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/><br/>[CreateFolder Operation](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|[Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> |Aktualisiert den Server mit Änderungen, die am Client vorgenommen wurden.<br/><br/>Bei Elementen und Ordnern verwendet die **Update** -Methode [UpdateItem Operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) und [UpdateFolder-Vorgang](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx).  <br/> |[UpdateItem Operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/>[UpdateFolder-Vorgang](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|[Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> |Löscht ein Element auf dem Server.<br/><br/>Bei Elementen und Ordnern verwendet die **Delete** -Methode [DeleteFolder-Vorgang](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx).  <br/> |[DeleteItem-Operation](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/><br/> [DeleteFolder-Vorgang](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
|[Copy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> |Erstellt eine Kopie des Elements oder Ordners auf dem Server.  <br/> |[CopyItem Operation](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/><br/> [CopyFolder-Vorgang](https://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx) <br/> |
|[Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> |Verschiebt Elemente oder Ordner auf den Server.  <br/> |[MoveItem Operation](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/><br/> [MoveFolder-Vorgang](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
## <a name="to-use-the-ews-managed-api-to-communicate-with-ews"></a>So verwenden Sie die verwaltete EWS-API zur Kommunikation mit EWS

1. Instanziieren Sie die **ExchangeService** -Klasse. 
    
   ```csharp
    ExchangeService service = new ExchangeService();
   ```

   > [!NOTE]
   > [!HINWEIS] Durch Instanziieren von **ExchangeService** mit einem leeren Konstruktor wird eine Instanz erstellt, die an die letzte bekannte Version von Exchange gebunden ist. Alternativ können Sie auf eine bestimmte Version von Exchange abzielen, indem Sie die Version als Parameter angeben. `ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);`
  
2. Legen Sie die Anmeldeinformationen des Benutzers fest, der Anforderungen an den Exchange-Server sendet. Wenn Sie mithilfe der Anmeldeinformationen des authentifizierten Benutzers eine Verbindung zu EWS von einem Computer herstellen möchten, der bei der Domäne angemeldet ist, legen Sie die **UseDefaultCredentials** -Eigenschaft im **ExchangeService** -Objekt auf **true** fest.
    
   ```cs
    // Connect by using the default credentials of the authenticated user.
    service.UseDefaultCredentials = true;
   ```

   Wenn Sie nicht mithilfe der standardmäßigen Benutzeranmeldeinformationen eine Verbindung herstellen möchten, legen Sie die **Credentials** -Eigenschaft im **ExchangeService** -Objekt so fest, dass explizit die Anmeldeinformationen eines anderen Benutzers angegeben werden. Wenn Sie Exchange Online oder Exchange Online als Teil von Office 365 verwenden, verwenden Sie die Standardauthentifizierung mit nur einem Benutzernamen und einem Kennwort. Für die NTLM-Authentifizierung ist ein Domänenname erforderlich. 
    
   ```cs
    // Connect by using the credentials of user1 at contoso.com.
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

   Sie können auch die Anmeldeinformationen des Benutzers mithilfe des Domänennamens und des Kennworts des Benutzers angeben.
    
   ```cs
    // Connect by using the credentials of contoso/user1.
    service.Credentials = new WebCredentials("user1", "password", "contoso");
   ```

   > [!NOTE]
   > [!HINWEIS] Wenn die **UseDefaultCredentials** -Eigenschaft auf **true** festgelegt ist, wird der Wert der **Credentials** -Eigenschaft ignoriert. 
  
3. Legen Sie die URL des EWS-Endpunkts fest. Diese URL sucht die Datei "exchange.asmx" auf dem Clientzugriffsserver.
    
   ```cs
    // Use Autodiscover to set the URL endpoint.
    service.AutodiscoverUrl("user1@contoso.com");
   ```

   > [!NOTE]
   >  Sie können die **Url** -Eigenschaft des **ExchangeService** zwar explizit auf einen hartcodierten Wert festlegen, es wird aber empfohlen, dass Sie stattdessen aus den folgenden Gründen den AutoErmittlungsdienst verwenden: >  Bei der AutoErmittlung wird der beste Endpunkt für einen bestimmten Benutzer ermittelt (der Entpunkt, der dem Postfachserver des Benutzers am nächsten ist). >  Die EWS-URL ändert sich möglicherweise, wenn neue Clientzugriffsserver bereitgestellt werden. In diesem Szenario bedeutet die Verwendung von [AutoErmittlung](autodiscover-for-exchange.md), dass keine Codeänderungen erforderlich sind. >  Sie sollten entweder die URL explizit festlegen oder **AutodiscoverUrl** aufrufen, aber nicht beides. 
  
## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md) 
- [Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten](how-to-use-autodiscover-to-find-connection-points.md)   
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

