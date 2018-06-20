---
title: EncryptedSharedFolderDataCollection
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EncryptedSharedFolderDataCollection
api_type:
- schema
ms.assetid: 25c6ae87-bbb9-4dd5-a85a-d669fcea137f
description: Das EncryptedSharedFolderDataCollection-Element enthält eine Auflistung von Datenstrukturen, die ein Client zum Autorisieren die Freigabe von dessen Kalender oder Kontaktdaten mit anderen Clients verwenden kann.
ms.openlocfilehash: e4d37f5df10f5e270be5126479485239f2205d6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758215"
---
# <a name="encryptedsharedfolderdatacollection"></a><span data-ttu-id="b1ab2-103">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="b1ab2-103">EncryptedSharedFolderDataCollection</span></span>

<span data-ttu-id="b1ab2-104">Das **EncryptedSharedFolderDataCollection** -Element enthält eine Auflistung von Datenstrukturen, die ein Client zum Autorisieren die Freigabe von dessen Kalender oder Kontaktdaten mit anderen Clients verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="b1ab2-104">The **EncryptedSharedFolderDataCollection** element contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span> 
  
```xml
<EncryptedSharedFolderDataCollection>   <EncryptedSharedFolderData/></EncryptedSharedFolderDataCollection>
```

 <span data-ttu-id="b1ab2-105">**ArrayOfEncryptedSharedFolderDataType**</span><span class="sxs-lookup"><span data-stu-id="b1ab2-105">**ArrayOfEncryptedSharedFolderDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1ab2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b1ab2-106">Attributes and elements</span></span>

<span data-ttu-id="b1ab2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b1ab2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1ab2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b1ab2-108">Attributes</span></span>

<span data-ttu-id="b1ab2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b1ab2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1ab2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b1ab2-110">Child elements</span></span>

|<span data-ttu-id="b1ab2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b1ab2-111">**Element**</span></span>|<span data-ttu-id="b1ab2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b1ab2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1ab2-113">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="b1ab2-113">EncryptedSharedFolderData</span></span>](encryptedsharedfolderdata.md) <br/> |<span data-ttu-id="b1ab2-114">Enthält die verschlüsselten Daten, die ein Client verwenden können, um die Freigabe von dessen Kalender zu autorisieren, oder wenden Sie Daten mit anderen Clients.</span><span class="sxs-lookup"><span data-stu-id="b1ab2-114">Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b1ab2-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b1ab2-115">Parent elements</span></span>

|<span data-ttu-id="b1ab2-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b1ab2-116">**Element**</span></span>|<span data-ttu-id="b1ab2-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b1ab2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1ab2-118">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="b1ab2-118">GetSharingMetadataResponse</span></span>](getsharingmetadataresponse.md) <br/> |<span data-ttu-id="b1ab2-119">Definiert eine Antwort auf eine [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="b1ab2-119">Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="b1ab2-120">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b1ab2-120">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md) <br/> |<span data-ttu-id="b1ab2-121">Enthält den Status und das Ergebnis einer einzelnen [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b1ab2-121">Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1ab2-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1ab2-122">Remarks</span></span>

<span data-ttu-id="b1ab2-123">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1ab2-123">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1ab2-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b1ab2-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1ab2-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1ab2-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b1ab2-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b1ab2-126">Schema Name</span></span>  <br/> |<span data-ttu-id="b1ab2-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b1ab2-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b1ab2-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b1ab2-128">Validation File</span></span>  <br/> |<span data-ttu-id="b1ab2-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b1ab2-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b1ab2-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b1ab2-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="b1ab2-131">False</span><span class="sxs-lookup"><span data-stu-id="b1ab2-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1ab2-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1ab2-132">See also</span></span>

- [<span data-ttu-id="b1ab2-133">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b1ab2-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="b1ab2-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b1ab2-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

