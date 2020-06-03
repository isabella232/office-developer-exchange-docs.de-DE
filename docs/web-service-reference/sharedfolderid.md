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
description: Das SharedFolderId-Element stellt den Bezeichner des freigegebenen Ordners dar, für den der lokale Ordner Bezeichner von einer GetSharingFolder-Vorgangsanforderung zurückgegeben werden soll.
ms.openlocfilehash: 546e148540708725bcf335f39bf69d193124d210
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466122"
---
# <a name="sharedfolderid"></a><span data-ttu-id="04a91-103">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="04a91-103">SharedFolderId</span></span>

<span data-ttu-id="04a91-104">Das **SharedFolderId** -Element stellt den Bezeichner des freigegebenen Ordners dar, für den der lokale Ordner Bezeichner von einer [GetSharingFolder-Vorgangs](getsharingfolder-operation.md) Anforderung zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="04a91-104">The **SharedFolderId** element represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```xml
<SharedFolderId/>
```

 <span data-ttu-id="04a91-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="04a91-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04a91-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="04a91-106">Attributes and elements</span></span>

<span data-ttu-id="04a91-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="04a91-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04a91-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="04a91-108">Attributes</span></span>

<span data-ttu-id="04a91-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="04a91-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04a91-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="04a91-110">Child elements</span></span>

<span data-ttu-id="04a91-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="04a91-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="04a91-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="04a91-112">Parent elements</span></span>

|<span data-ttu-id="04a91-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="04a91-113">**Element**</span></span>|<span data-ttu-id="04a91-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="04a91-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04a91-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="04a91-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="04a91-116">Definiert eine Anforderung zum Abrufen der lokalen Ordner-ID eines angegebenen freigegebenen Ordners.</span><span class="sxs-lookup"><span data-stu-id="04a91-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="04a91-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="04a91-117">Text value</span></span>

<span data-ttu-id="04a91-118">Der Textwert ist eine Zeichenfolge, die den Bezeichner des freigegebenen Ordners darstellt, für den die lokale Ordner-ID von einer [GetSharingFolder-Vorgangs](getsharingfolder-operation.md) Anforderung zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="04a91-118">The text value is a string that represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="04a91-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04a91-119">Remarks</span></span>

<span data-ttu-id="04a91-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="04a91-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04a91-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="04a91-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04a91-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="04a91-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="04a91-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="04a91-123">Schema Name</span></span>  <br/> |<span data-ttu-id="04a91-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="04a91-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="04a91-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="04a91-125">Validation File</span></span>  <br/> |<span data-ttu-id="04a91-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="04a91-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="04a91-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="04a91-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="04a91-128">False</span><span class="sxs-lookup"><span data-stu-id="04a91-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04a91-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04a91-129">See also</span></span>



[<span data-ttu-id="04a91-130">GetSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="04a91-130">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="04a91-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="04a91-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

