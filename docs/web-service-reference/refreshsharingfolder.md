---
title: RefreshSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolder
api_type:
- schema
ms.assetid: 14571c28-effa-430a-802e-82fb99bafa7f
description: Das RefreshSharingFolder-Element definiert eine Anforderung zum Aktualisieren des angegebenen lokalen Ordners. Es ist das Basiselement für den RefreshSharingFolder-Vorgang.
ms.openlocfilehash: 4454607fa2c3114cc7279fd7c30f8aee74707baa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467928"
---
# <a name="refreshsharingfolder"></a><span data-ttu-id="9667f-104">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="9667f-104">RefreshSharingFolder</span></span>

<span data-ttu-id="9667f-105">Das **RefreshSharingFolder** -Element definiert eine Anforderung zum Aktualisieren des angegebenen lokalen Ordners.</span><span class="sxs-lookup"><span data-stu-id="9667f-105">The **RefreshSharingFolder** element defines a request to refresh the specified local folder.</span></span> <span data-ttu-id="9667f-106">Es ist das Basiselement für den [RefreshSharingFolder-Vorgang](refreshsharingfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="9667f-106">It is the base element for the [RefreshSharingFolder operation](refreshsharingfolder-operation.md).</span></span>
  
```xml
<RefreshSharingFolder>   <SharingFolderId/></RefreshSharingFolder>
```

 <span data-ttu-id="9667f-107">**RefreshSharingFolderType**</span><span class="sxs-lookup"><span data-stu-id="9667f-107">**RefreshSharingFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9667f-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9667f-108">Attributes and elements</span></span>

<span data-ttu-id="9667f-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9667f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9667f-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="9667f-110">Attributes</span></span>

<span data-ttu-id="9667f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="9667f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9667f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9667f-112">Child elements</span></span>

|<span data-ttu-id="9667f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9667f-113">**Element**</span></span>|<span data-ttu-id="9667f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9667f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9667f-115">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="9667f-115">SharingFolderId</span></span>](sharingfolderid.md) <br/> |<span data-ttu-id="9667f-116">Stellt den Bezeichner des lokalen Ordners in einer Freigabebeziehung dar.</span><span class="sxs-lookup"><span data-stu-id="9667f-116">Represents the identifier of the local folder in a sharing relationship.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9667f-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9667f-117">Parent elements</span></span>

<span data-ttu-id="9667f-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="9667f-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9667f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9667f-119">Remarks</span></span>

<span data-ttu-id="9667f-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9667f-120">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9667f-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9667f-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9667f-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="9667f-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9667f-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9667f-123">Schema Name</span></span>  <br/> |<span data-ttu-id="9667f-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9667f-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9667f-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9667f-125">Validation File</span></span>  <br/> |<span data-ttu-id="9667f-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9667f-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9667f-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9667f-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="9667f-128">False</span><span class="sxs-lookup"><span data-stu-id="9667f-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9667f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9667f-129">See also</span></span>



- [<span data-ttu-id="9667f-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9667f-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

