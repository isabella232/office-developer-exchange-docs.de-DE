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
description: Das EncryptedSharedFolderData-Element enthält die verschlüsselten Daten, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.
ms.openlocfilehash: 52e91eaf1ded31602b11e50c1b62159f72c101cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530663"
---
# <a name="encryptedsharedfolderdata"></a><span data-ttu-id="3929a-103">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="3929a-103">EncryptedSharedFolderData</span></span>

<span data-ttu-id="3929a-104">Das **EncryptedSharedFolderData** -Element enthält die verschlüsselten Daten, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="3929a-104">The **EncryptedSharedFolderData** element contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span> 
  
```xml
<EncryptedSharedFolderData>   <Token/>   <Data/></EncryptedSharedFolderData>
```

 <span data-ttu-id="3929a-105">**EncryptedSharedFolderDataType**</span><span class="sxs-lookup"><span data-stu-id="3929a-105">**EncryptedSharedFolderDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3929a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3929a-106">Attributes and elements</span></span>

<span data-ttu-id="3929a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3929a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3929a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3929a-108">Attributes</span></span>

<span data-ttu-id="3929a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3929a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3929a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3929a-110">Child elements</span></span>

|<span data-ttu-id="3929a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3929a-111">**Element**</span></span>|<span data-ttu-id="3929a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3929a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3929a-113">Token</span><span class="sxs-lookup"><span data-stu-id="3929a-113">Token</span></span>](token.md) <br/> |<span data-ttu-id="3929a-114">Enthält verschlüsselte Daten, die das Identifikations Token für die freigegebenen Daten darstellen.</span><span class="sxs-lookup"><span data-stu-id="3929a-114">Contains encrypted data that represents the identification token for the shared data.</span></span>  <br/> |
|[<span data-ttu-id="3929a-115">Daten</span><span class="sxs-lookup"><span data-stu-id="3929a-115">Data</span></span>](data.md) <br/> |<span data-ttu-id="3929a-116">Enthält verschlüsselte Daten, die die freigegebenen Daten darstellen.</span><span class="sxs-lookup"><span data-stu-id="3929a-116">Contains encrypted data that represents the shared data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3929a-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3929a-117">Parent elements</span></span>

|<span data-ttu-id="3929a-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="3929a-118">**Element**</span></span>|<span data-ttu-id="3929a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3929a-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3929a-120">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="3929a-120">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="3929a-121">Stellt eine Auflistung von Datenstrukturen dar, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="3929a-121">Represents a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3929a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3929a-122">Remarks</span></span>

<span data-ttu-id="3929a-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3929a-123">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3929a-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3929a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3929a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="3929a-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3929a-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3929a-126">Schema Name</span></span>  <br/> |<span data-ttu-id="3929a-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3929a-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="3929a-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3929a-128">Validation File</span></span>  <br/> |<span data-ttu-id="3929a-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3929a-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3929a-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3929a-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="3929a-131">False</span><span class="sxs-lookup"><span data-stu-id="3929a-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3929a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3929a-132">See also</span></span>

- [<span data-ttu-id="3929a-133">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3929a-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="3929a-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3929a-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

