---
title: ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: c85207e1-1315-443b-94ec-2b58f405076b
description: Das ResolveNames-Element definiert eine Anforderung zum Auflösen von mehrdeutigen Namen.
ms.openlocfilehash: 8fbf933593b43de656bf8731aa86cc8c8eb76bb4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514144"
---
# <a name="resolvenames"></a>ResolveNames

Das **ResolveNames-Element** definiert eine Anforderung zum Auflösen von mehrdeutigen Namen. 
  
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
|**ReturnFullContactData** <br/> |Beschreibt, ob die vollständigen Kontaktdetails für öffentliche Kontakte für einen aufgelösten Namen in der Antwort zurückgegeben werden. Dieses Attribut ist für öffentliche Kontakte erforderlich. Dieser Wert wirkt sich nicht auf private Kontakte und private Verteilerlisten aus, für die [ItemId](itemid.md) immer zurückgegeben wird.  <br/> |
|**SearchScope** <br/> |Gibt die Reihenfolge und den Bereich für eine ResolveNames-Suche an.  <br/> |
|ContactDataShape  <br/> |Identifies the property set returned for contacts. Dieses Attribut wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a>ReturnFullContactData-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Richtig  <br/> |Vollständige Kontaktdetails für öffentliche Kontakte werden zurückgegeben.  <br/> |
|Nicht richtig  <br/> |Vollständige Kontaktdetails für öffentliche Kontakte werden nicht zurückgegeben.  <br/> |
   
#### <a name="searchscope-attribute-values"></a>SearchScope-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Activedirectory  <br/> |Es wird nur der Active Directory-Verzeichnisdienst durchsucht.  <br/> |
|ActiveDirectoryContacts  <br/> |Active Directory wird zuerst durchsucht, und dann werden die Kontaktordner durchsucht, die in der [ParentFolderIds-Eigenschaft](parentfolderids.md) angegeben sind.  <br/> |
|Kontakte  <br/> |Es werden nur die Kontaktordner durchsucht, die durch die [ParentFolderIds-Eigenschaft](parentfolderids.md) identifiziert werden.  <br/> |
|ContactsActiveDirectory  <br/> |Kontaktordner, die durch die [ParentFolderIds-Eigenschaft](parentfolderids.md) identifiziert werden, werden zuerst durchsucht, und dann wird Active Directory durchsucht.  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a>ContactDataShape-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|IdOnly  <br/> |Die Bezeichnereigenschaft des Kontaktelements wird zurückgegeben.  <br/> |
|Standard  <br/> |Der Standardsatz von Kontaktelementeigenschaften wird zurückgegeben. Weitere Informationen finden Sie unter [Antwortshapes in EWS.](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx)  <br/> |
|AllProperties  <br/> |Der AllProperties-Satz von Kontaktelementeigenschaften wird zurückgegeben. Weitere Informationen finden Sie unter [Antwortshapes in EWS.](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx)  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ParentFolderIds](parentfolderids.md) <br/> |Enthält ein Array von Kontaktordnerbezeichnern, die durchsucht würden, wenn das **SearchScope-Attribut** auf ActiveDirectoryContacts, Kontakte oder ContactsActiveDirectory festgelegt ist. Das ParentFolderIds-Array kann nur einen einzelnen Kontaktordnerbezeichner enthalten. Wenn das **ParentFolderIds-Element** nicht vorhanden ist, wird der Standardordner "Kontakte" durchsucht.  <br/> Der Ordnerbezeichner kann für den Stellvertretungszugriff verwendet werden.  <br/> Active Directory-Suchvorgänge werden mithilfe von Zugriffssteuerungslisten (Access Control Lists, ACLs) ausgeführt. Einige Benutzer haben möglicherweise nicht die Rechte, einige Active Directory-Objekte anzuzeigen.  <br/> Dieses Element ist optional.  <br/> |
|[UnresolvedEntry](unresolvedentry.md) <br/> |Enthält den Namen eines Kontakts oder einer Verteilerliste, der aufgelöst werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ResolveNames-Vorgang](resolvenames-operation.md)
  
[ResolveNamesType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[ResolveNamesSearchScopeType](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Verwenden der Namensauflösung](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

