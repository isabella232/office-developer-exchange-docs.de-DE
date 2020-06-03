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
description: Das ResolveNames-Element definiert eine Anforderung zum Auflösen eindeutiger Namen.
ms.openlocfilehash: 9c36a5f84451f91e90a8e7148cf384b5cacd7f29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467949"
---
# <a name="resolvenames"></a>ResolveNames

Das **ResolveNames** -Element definiert eine Anforderung zum Auflösen eindeutiger Namen. 
  
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
|**ReturnFullContactData** <br/> |Beschreibt, ob die vollständigen Kontaktdetails für öffentliche Kontakte für einen aufgelösten Namen in der Antwort zurückgegeben werden. Dieses Attribut ist für öffentliche Kontakte erforderlich. Dieser Wert wirkt sich nicht auf private Kontakte und private Verteilerlisten aus, für die [ItemID](itemid.md) immer zurückgegeben wird.  <br/> |
|**SearchScope** <br/> |Gibt die Reihenfolge und den Bereich für eine ResolveNames-Suche an.  <br/> |
|ContactDataShape  <br/> |Gibt den Eigenschaftensatz an, der für Kontakte zurückgegeben wurde. Dieses Attribut wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a>ReturnFullContactData-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Wahr  <br/> |Die vollständigen Kontaktdetails für öffentliche Kontakte werden zurückgegeben.  <br/> |
|Falsch  <br/> |Die vollständigen Kontaktdetails für öffentliche Kontakte werden nicht zurückgegeben.  <br/> |
   
#### <a name="searchscope-attribute-values"></a>SearchScope-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|ActiveDirectory  <br/> |Es wird nur der Active Directory-Verzeichnisdienst durchsucht.  <br/> |
|ActiveDirectoryContacts  <br/> |Active Directory wird zuerst durchsucht, und dann werden die in der [ParentFolderIds](parentfolderids.md) -Eigenschaft angegebenen Kontaktordner durchsucht.  <br/> |
|Kontakte  <br/> |Nur die Kontaktordner, die von der [ParentFolderIds](parentfolderids.md) -Eigenschaft identifiziert werden, werden durchsucht.  <br/> |
|ContactsActiveDirectory  <br/> |Kontaktordner, die von der [ParentFolderIds](parentfolderids.md) -Eigenschaft identifiziert werden, werden zuerst durchsucht, und dann wird Active Directory durchsucht.  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a>ContactDataShape-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|IdOnly  <br/> |Die Eigenschaft Contact Item Identifier wird zurückgegeben.  <br/> |
|Standard  <br/> |Die Standardeinstellungen für Kontaktelemente werden zurückgegeben. Weitere Informationen finden Sie unter [Response Shapes in EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).  <br/> |
|AllProperties  <br/> |Die allproperties-Gruppe der Kontaktelement Eigenschaften wird zurückgegeben. Weitere Informationen finden Sie unter [Response Shapes in EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ParentFolderIds](parentfolderids.md) <br/> |Enthält ein Array von Kontaktordner Bezeichnern, die durchsucht werden, wenn das **SearchScope** -Attribut auf ActiveDirectoryContacts, Contacts oder ContactsActiveDirectory festgelegt ist. Das ParentFolderIds-Array kann nur einen einzelnen Kontaktordner Bezeichner enthalten. Wenn das **ParentFolderIds** -Element nicht vorhanden ist, wird der Standardordner Kontakte durchsucht.  <br/> Die Ordner-ID kann für den Stellvertretungszugriff verwendet werden.  <br/> Active Directory suchen werden mithilfe von Zugriffssteuerungslisten (Access Control Lists, ACLs) ausgeführt. Einige Benutzer verfügen möglicherweise nicht über die Rechte zum Anzeigen einiger Active Directory-Objekte.  <br/> Dieses Element ist optional.  <br/> |
|[UnresolvedEntry](unresolvedentry.md) <br/> |Enthält den Namen eines Kontakts oder einer Verteilerliste, die aufgelöst werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ResolveNames-Vorgang](resolvenames-operation.md)
  
[ResolveNamesType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[ResolveNamesSearchScopeType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Verwenden der Namensauflösung](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

