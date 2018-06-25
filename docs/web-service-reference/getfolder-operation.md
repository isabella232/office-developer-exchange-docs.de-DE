---
title: GetFolder Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 355bcf93-dc71-4493-b177-622afac5fdb9
description: GetFolder-Vorgang ruft Ordnern aus dem Exchange-Speicher ab.
ms.openlocfilehash: 1d2806e4febb6059b8a866d585bc70f49befbdef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758684"
---
# <a name="getfolder-operation"></a>GetFolder Operation

**GetFolder** -Vorgang ruft Ordnern aus dem Exchange-Speicher ab. 
  
## <a name="getfolder-request-example"></a>GetFolder-anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung **GetFolder** veranschaulicht erhalten eine Ordner-ID, Name, die Anzahl der Elemente in dem Ordner, die Anzahl der untergeordneten Ordner und die Anzahl der ungelesenen Elemente im Ordner anzuzeigen. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
   xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <FolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </FolderIds>
    </GetFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Anfordern von Elementen

Diese **GetFolder** -Anforderung enthält die folgenden Elemente: 
  
- [GetFolder](getfolder.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [FolderIds](folderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
Finden Sie im Schema für zusätzliche Elemente, die Sie verwenden können, um eine Anforderung **GetFolder** bilden. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet. 
  
## <a name="getfolder-response-example"></a>GetFolder-Antwort-Beispiel

### <a name="description"></a>Beschreibung

Das folgende (SOAP = Simple Object Access Protocol)-Body-Beispiel zeigt eine erfolgreiche Antwort auf die **GetFolder** -Anforderung. 
  
> [!NOTE]
> Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AQApA=" ChangeKey="AQAAAB" />
              <t:DisplayName>Inbox</t:DisplayName>
              <t:TotalCount>2</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:UnreadCount>2</t:UnreadCount>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </GetFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a>Antwortelemente

Dieser Antwort **GetFolder** umfasst die folgenden Elemente: 
  
- [GetFolderResponse](getfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetFolderResponseMessage](getfolderresponsemessage.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
- [TotalCount](totalcount.md)
    
- [ChildFolderCount](childfoldercount.md)
    
- [UnreadCount](unreadcount.md)
    
## <a name="getfolder-error-response-example"></a>GetFolder-Fehler antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende SOAP-Body-Beispiel zeigt eine Fehlerantwort an, die durch eine falsche [FolderId](folderid.md) in der Anforderung verursacht wird. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </GetFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a>Antwortelemente

Diese **GetFolder** -Fehlerantwort umfasst die folgenden Elemente: 
  
- [GetFolderResponse](getfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetFolderResponseMessage](getfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
## <a name="version-differences"></a>Versionsunterschiede

Für Applikationen werden, Exchange Online abzielen, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange beginnend mit Exchange 2013 Ordnerberechtigungen nicht zurückgegeben, wenn das Element [BaseShape](baseshape.md) **AllProperties** Wert hat in der Anforderung [GetFolder](getfolder-operation.md) -Vorgang. Um Ordnerberechtigungen abzurufen, fügen Sie dem [AdditionalProperties](additionalproperties.md) -Element in der Anforderung **GetFolder** die [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) -Element hinzu. 
  
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

