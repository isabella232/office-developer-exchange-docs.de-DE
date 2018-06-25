---
title: ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: c85207e1-1315-443b-94ec-2b58f405076b
description: Das ResolveNames-Element definiert eine Anforderung zum Auflösen von Names nicht eindeutig.
ms.openlocfilehash: e97b6e78d99cf8ffa3d680907916882d40963f59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831172"
---
# <a name="resolvenames"></a>ResolveNames

Das **ResolveNames** -Element definiert eine Anforderung zum Auflösen von Names nicht eindeutig. 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 **ResolveNamesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ReturnFullContactData** <br/> |Beschreibt, ob der vollständige Kontaktdetails für Öffentliche Kontakte für einen aufgelösten Namen in der Antwort zurückgegeben werden. Dieses Attribut ist für Öffentliche Kontakte erforderlich. Dieser Wert wirkt sich nicht private Kontakte und private Verteilerlisten, für die [ItemId](itemid.md) immer zurückgegeben wird.  <br/> |
|**SearchScope** <br/> |Gibt die Reihenfolge und ResolveNames Suchbereich.  <br/> |
|ContactDataShape  <br/> |Identifiziert den Eigenschaftensatz für Kontakte zurückgegeben werden. Dieses Attribut wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a>Attributwerte ReturnFullContactData

|**Wert**|**Beschreibung**|
|:-----|:-----|
|True  <br/> |Vollständige Kontaktdetails für Öffentliche Kontakte werden zurückgegeben.  <br/> |
|False  <br/> |Vollständige Kontaktdetails für Öffentliche Kontakte werden nicht zurückgegeben.  <br/> |
   
#### <a name="searchscope-attribute-values"></a>SearchScope-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|ActiveDirectory-Umgebung  <br/> |Nur der Active Directory-Verzeichnisdienst wird durchsucht.  <br/> |
|ActiveDirectoryContacts  <br/> |Active Directory wird zuerst durchsucht, und klicken Sie dann die Kontakten in der [ParentFolderIds](parentfolderids.md) -Eigenschaft angegebenen Ordnern durchsucht werden.  <br/> |
|Kontakte  <br/> |Es werden nur der Ordner für Kontakte, die von der [ParentFolderIds](parentfolderids.md) -Eigenschaft identifiziert werden durchsucht.  <br/> |
|ContactsActiveDirectory  <br/> |Ordner, die von der [ParentFolderIds](parentfolderids.md) -Eigenschaft identifiziert werden für Kontakte werden zuerst durchsucht, und klicken Sie dann auf Active Directory durchsucht wird.  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a>Attributwerte ContactDataShape

|**Wert**|**Beschreibung**|
|:-----|:-----|
|IdOnly  <br/> |Die Kontaktelement Identifier-Eigenschaft wird zurückgegeben.  <br/> |
|Standard  <br/> |Die Standardgruppe von Eigenschaften für Kontaktelemente wird zurückgegeben. Weitere Informationen finden Sie unter [Antwort Shapes in der Exchange-Webdienste](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).  <br/> |
|AllProperties  <br/> |Der AllProperties Satz von Eigenschaften für Kontaktelemente werden zurückgegeben. Weitere Informationen finden Sie unter [Antwort Shapes in der Exchange-Webdienste](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ParentFolderIds](parentfolderids.md) <br/> |Enthält ein Array mit den Kontaktordner-IDs, die durchsucht werden würde, wenn das **SearchScope** -Attribut auf ActiveDirectoryContacts, Kontakte oder ContactsActiveDirectory festgelegt ist. Das Array ParentFolderIds kann nur einen einzigen Kontaktordner Bezeichner enthalten. Wenn das **ParentFolderIds** -Element nicht vorhanden ist, wird der Standardordner Kontakte durchsucht.  <br/> Die Ordner-ID kann für Stellvertretungszugriff verwendet werden.  <br/> Active Directory durchsucht werden mithilfe von Zugriffssteuerungslisten (ACLs) ausgeführt. Einige Benutzer haben möglicherweise nicht die Rechte für einige Active Directory-Objekte finden Sie unter.  <br/> Dieses Element ist optional.  <br/> |
|[UnresolvedEntry](unresolvedentry.md) <br/> |Enthält den Namen des einen Kontakt oder Verteilerliste aus, zu beheben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ResolveNames-Vorgang](resolvenames-operation.md)
  
[ResolveNamesType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[ResolveNamesSearchScopeType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Verwenden von namensauflösung](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

