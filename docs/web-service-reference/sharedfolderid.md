---
title: SharedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharedFolderId
api_type:
- schema
ms.assetid: 21181ba3-9626-4284-9717-0b1c16948e8f
description: Das Element SharedFolderId stellt den Bezeichner des freigegebenen Ordner mit der ID der lokalen Ordner, für die durch die Anforderung einer GetSharingFolder-Operation zurückgegeben werden sollen.
ms.openlocfilehash: 6d4e541ef3cae89e413efa8cc5f1beaf651dc4dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831477"
---
# <a name="sharedfolderid"></a><span data-ttu-id="2a6bf-103">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="2a6bf-103">SharedFolderId</span></span>

<span data-ttu-id="2a6bf-104">Das Element **SharedFolderId** stellt den Bezeichner des freigegebenen Ordner mit der ID der lokalen Ordner, für die eine Anforderung [GetSharingFolder Vorgang](getsharingfolder-operation.md) zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-104">The **SharedFolderId** element represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```xml
<SharedFolderId/>
```

 <span data-ttu-id="2a6bf-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a6bf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2a6bf-106">Attributes and elements</span></span>

<span data-ttu-id="2a6bf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a6bf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2a6bf-108">Attributes</span></span>

<span data-ttu-id="2a6bf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a6bf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a6bf-110">Child elements</span></span>

<span data-ttu-id="2a6bf-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2a6bf-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a6bf-112">Parent elements</span></span>

|<span data-ttu-id="2a6bf-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-113">**Element**</span></span>|<span data-ttu-id="2a6bf-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a6bf-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="2a6bf-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="2a6bf-116">Definiert eine Anforderung an den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2a6bf-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="2a6bf-117">Text value</span></span>

<span data-ttu-id="2a6bf-118">Der Textwert ist eine Zeichenfolge, die den Bezeichner des freigegebenen Ordners darstellt, der lokalen Ordner Bezeichner für die durch eine Anforderung [GetSharingFolder Vorgang](getsharingfolder-operation.md) zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-118">The text value is a string that represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2a6bf-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2a6bf-119">Remarks</span></span>

<span data-ttu-id="2a6bf-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a6bf-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2a6bf-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a6bf-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a6bf-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2a6bf-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2a6bf-123">Schema Name</span></span>  <br/> |<span data-ttu-id="2a6bf-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2a6bf-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2a6bf-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2a6bf-125">Validation File</span></span>  <br/> |<span data-ttu-id="2a6bf-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2a6bf-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2a6bf-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2a6bf-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="2a6bf-128">False</span><span class="sxs-lookup"><span data-stu-id="2a6bf-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a6bf-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a6bf-129">See also</span></span>



[<span data-ttu-id="2a6bf-130">GetSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2a6bf-130">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="2a6bf-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2a6bf-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

