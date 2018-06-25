---
title: Token
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Token
api_type:
- schema
ms.assetid: 62b700e1-88c7-41ef-b431-d7af4a8b54a7
description: Das Token-Element enthält die verschlüsselte Daten, die das Token Kennung für die freigegebenen Daten darstellt.
ms.openlocfilehash: cec11d9f2c24a250483c5be6e273f981fdf0a8e6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839233"
---
# <a name="token"></a><span data-ttu-id="28a34-103">Token</span><span class="sxs-lookup"><span data-stu-id="28a34-103">Token</span></span>

<span data-ttu-id="28a34-104">Das **Token** Element enthält die verschlüsselte Daten, die das Token Kennung für die freigegebenen Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="28a34-104">The **Token** element contains encrypted data that represents the identification token for the shared data.</span></span> 
  
```xml
<Token/>
```

 <span data-ttu-id="28a34-105">**EncryptedDataContainerType**</span><span class="sxs-lookup"><span data-stu-id="28a34-105">**EncryptedDataContainerType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28a34-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28a34-106">Attributes and elements</span></span>

<span data-ttu-id="28a34-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28a34-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28a34-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="28a34-108">Attributes</span></span>

<span data-ttu-id="28a34-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="28a34-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28a34-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28a34-110">Child elements</span></span>

<span data-ttu-id="28a34-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="28a34-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="28a34-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28a34-112">Parent elements</span></span>

|<span data-ttu-id="28a34-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="28a34-113">**Element**</span></span>|<span data-ttu-id="28a34-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28a34-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28a34-115">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="28a34-115">EncryptedSharedFolderData</span></span>](encryptedsharedfolderdata.md) <br/> |<span data-ttu-id="28a34-116">Enthält die verschlüsselten Daten, die ein Client verwenden können, um die Freigabe von dessen Kalender zu autorisieren, oder wenden Sie Daten mit anderen Clients.</span><span class="sxs-lookup"><span data-stu-id="28a34-116">Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28a34-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28a34-117">Remarks</span></span>

<span data-ttu-id="28a34-118">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="28a34-118">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28a34-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="28a34-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28a34-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="28a34-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="28a34-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28a34-121">Schema Name</span></span>  <br/> |<span data-ttu-id="28a34-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="28a34-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="28a34-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28a34-123">Validation File</span></span>  <br/> |<span data-ttu-id="28a34-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="28a34-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="28a34-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="28a34-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="28a34-126">False</span><span class="sxs-lookup"><span data-stu-id="28a34-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28a34-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28a34-127">See also</span></span>



[<span data-ttu-id="28a34-128">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="28a34-128">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="28a34-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="28a34-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

