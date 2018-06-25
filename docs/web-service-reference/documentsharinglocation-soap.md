---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: Das DocumentSharingLocation-Element enthält, Speicherort und Metadateninformationen für ein Dokument sharing-Location.
ms.openlocfilehash: d258efecb46d570138c7c2c78ed9d2fa9a275103
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758082"
---
# <a name="documentsharinglocation-soap"></a>DocumentSharingLocation (SOAP)

Das **DocumentSharingLocation** -Element enthält, Speicherort und Metadateninformationen für ein Dokument sharing-Location. 
  
```XML
<DocumentSharingLocation>
   <ServiceUrl />
   <LocationUrl />
   <DisplayName />
   <SupportedFileExtensions />
   <ExternalAccessAllowed />
   <AnonymousAccessAllowed />
   <CanModifyPermissions />
   <IsDefault />
</DocumentSharingLocation>
```

 **DocumentSharingLocation**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ServiceUrl (SOAP)](serviceurl-soap.md) <br/> |Stellt die URL des Dokuments Freigabe-Webdienst.  <br/> |
|[LocationUrl (SOAP)](locationurl-soap.md) <br/> |Stellt die URL des Dokuments sharing-Location.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Stellt den Namen des Dokuments sharing-Location in der Benutzeroberfläche verwendet.  <br/> |
|[SupportedFileExtensions (SOAP)](supportedfileextensions-soap.md) <br/> |Stellt die Dateierweiterungen, die im Dokument sharing-Location gespeichert werden können.  <br/> |
|[ExternalAccessAllowed (SOAP)](externalaccessallowed-soap.md) <br/> |Gibt an, ob das Dokument sharing-Location außerhalb Verbindungen zur Verfügung steht.  <br/> |
|[AnonymousAccessAllowed (SOAP)](anonymousaccessallowed-soap.md) <br/> |Gibt an, ob der Zugriff auf den freigegebenen Speicherort als authentifizierten Benutzer erforderlich ist.  <br/> |
|[CanModifyPermissions (SOAP)](canmodifypermissions-soap.md) <br/> |Gibt an, ob der Benutzer die Zugriffsberechtigungen für das Dokument sharing-Location ändern kann.  <br/> |
|[IsDefault (SOAP)](isdefault-soap.md) <br/> |Gibt an, ob das Dokument sharing-Location des Benutzers Standard sharing-Location ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DocumentSharingLocations (SOAP)](documentsharinglocations-soap.md) <br/> |Enthält eine Liste der Dokumentfreigabe Speicherorte und Metadaten.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [SOAP-Autodiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

