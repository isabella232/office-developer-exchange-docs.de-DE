---
title: AnonymousAccessAllowed (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bf819a65-30f2-4881-a34f-cb30a9c2b6a7
description: Das AnonymousAccessAllowed-Element gibt an, ob ein Dokumentfreigabe Speicherort einen authentifizierten Benutzer erfordert.
ms.openlocfilehash: b3ff22fbba603bbd74dc08a0dbb1d8687714fe7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466080"
---
# <a name="anonymousaccessallowed-soap"></a><span data-ttu-id="e656c-103">AnonymousAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e656c-103">AnonymousAccessAllowed (SOAP)</span></span>

<span data-ttu-id="e656c-104">Das **AnonymousAccessAllowed** -Element gibt an, ob ein Dokumentfreigabe Speicherort einen authentifizierten Benutzer erfordert.</span><span class="sxs-lookup"><span data-stu-id="e656c-104">The **AnonymousAccessAllowed** element indicates whether a document sharing location requires an authenticated user.</span></span> 
  
```XML
<AnonymousAccessAllowed /> 
```

 <span data-ttu-id="e656c-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="e656c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e656c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e656c-106">Attributes and elements</span></span>

<span data-ttu-id="e656c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e656c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e656c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e656c-108">Attributes</span></span>

<span data-ttu-id="e656c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e656c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e656c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e656c-110">Child elements</span></span>

<span data-ttu-id="e656c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e656c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e656c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e656c-112">Parent elements</span></span>

|<span data-ttu-id="e656c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e656c-113">**Element**</span></span>|<span data-ttu-id="e656c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e656c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e656c-115">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e656c-115">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="e656c-116">Stellt Speicherort-und Metadateninformationen für einen Dokumentfreigabe Speicherort dar.</span><span class="sxs-lookup"><span data-stu-id="e656c-116">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e656c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="e656c-117">Text value</span></span>

<span data-ttu-id="e656c-118">Der boolesche Wert des **AnonymousAccessAllowed** -Elements gibt an, ob für den Freigabespeicherort ein authentifizierter Benutzer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e656c-118">The Boolean value of the **AnonymousAccessAllowed** element indicates whether the sharing location requires an authenticated user.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e656c-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e656c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e656c-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="e656c-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e656c-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e656c-121">Schema Name</span></span>  <br/> |<span data-ttu-id="e656c-122">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="e656c-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e656c-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e656c-123">Validation File</span></span>  <br/> |<span data-ttu-id="e656c-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e656c-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e656c-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e656c-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="e656c-126">True</span><span class="sxs-lookup"><span data-stu-id="e656c-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e656c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e656c-127">See also</span></span>

- [<span data-ttu-id="e656c-128">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e656c-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="e656c-129">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="e656c-129">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="e656c-130">XML-Elemente der SOAP-AutoErmittlung für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="e656c-130">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

