---
title: EncryptedSharedFolderData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EncryptedSharedFolderData
api_type:
- schema
ms.assetid: c1d4ca18-c5ce-41ff-bab4-f75e358c8b9f
description: Das EncryptedSharedFolderData-Element enthält die verschlüsselten Daten, die ein Client verwenden können, um die Freigabe von dessen Kalender zu autorisieren, oder wenden Sie Daten mit anderen Clients.
ms.openlocfilehash: 63966e95becaab4b3b1e54aa81f1b20a8b09dfd3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758217"
---
# <a name="encryptedsharedfolderdata"></a><span data-ttu-id="03f61-103">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="03f61-103">EncryptedSharedFolderData</span></span>

<span data-ttu-id="03f61-104">Das **EncryptedSharedFolderData** -Element enthält die verschlüsselten Daten, die ein Client verwenden können, um die Freigabe von dessen Kalender zu autorisieren, oder wenden Sie Daten mit anderen Clients.</span><span class="sxs-lookup"><span data-stu-id="03f61-104">The **EncryptedSharedFolderData** element contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span> 
  
```xml
<EncryptedSharedFolderData>   <Token/>   <Data/></EncryptedSharedFolderData>
```

 <span data-ttu-id="03f61-105">**EncryptedSharedFolderDataType**</span><span class="sxs-lookup"><span data-stu-id="03f61-105">**EncryptedSharedFolderDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="03f61-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="03f61-106">Attributes and elements</span></span>

<span data-ttu-id="03f61-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="03f61-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="03f61-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="03f61-108">Attributes</span></span>

<span data-ttu-id="03f61-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="03f61-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="03f61-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="03f61-110">Child elements</span></span>

|<span data-ttu-id="03f61-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="03f61-111">**Element**</span></span>|<span data-ttu-id="03f61-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03f61-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="03f61-113">Token</span><span class="sxs-lookup"><span data-stu-id="03f61-113">Token</span></span>](token.md) <br/> |<span data-ttu-id="03f61-114">Enthält die verschlüsselte Daten, die das Token Kennung für die freigegebenen Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="03f61-114">Contains encrypted data that represents the identification token for the shared data.</span></span>  <br/> |
|[<span data-ttu-id="03f61-115">Data</span><span class="sxs-lookup"><span data-stu-id="03f61-115">Data</span></span>](data.md) <br/> |<span data-ttu-id="03f61-116">Enthält die verschlüsselte Daten, die die freigegebenen Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="03f61-116">Contains encrypted data that represents the shared data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="03f61-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="03f61-117">Parent elements</span></span>

|<span data-ttu-id="03f61-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="03f61-118">**Element**</span></span>|<span data-ttu-id="03f61-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03f61-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="03f61-120">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="03f61-120">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="03f61-121">Stellt eine Auflistung von Datenstrukturen, die ein Client zum Autorisieren die Freigabe von dessen Kalender oder Kontaktdaten mit anderen Clients verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="03f61-121">Represents a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03f61-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="03f61-122">Remarks</span></span>

<span data-ttu-id="03f61-123">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="03f61-123">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="03f61-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="03f61-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03f61-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="03f61-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="03f61-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="03f61-126">Schema Name</span></span>  <br/> |<span data-ttu-id="03f61-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="03f61-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="03f61-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="03f61-128">Validation File</span></span>  <br/> |<span data-ttu-id="03f61-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="03f61-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="03f61-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="03f61-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="03f61-131">False</span><span class="sxs-lookup"><span data-stu-id="03f61-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03f61-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03f61-132">See also</span></span>

- [<span data-ttu-id="03f61-133">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="03f61-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="03f61-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="03f61-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

