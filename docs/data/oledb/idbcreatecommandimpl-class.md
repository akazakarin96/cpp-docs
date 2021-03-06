---
title: "IDBCreateCommandImpl Class"
ms.date: "11/04/2016"
f1_keywords: ["ATL::IDBCreateCommandImpl", "IDBCreateCommandImpl", "ATL.IDBCreateCommandImpl", "IDBCreateCommandImpl.CreateCommand", "CreateCommand", "IDBCreateCommandImpl::CreateCommand"]
helpviewer_keywords: ["IDBCreateCommandImpl class", "CreateCommand method"]
ms.assetid: eac4755e-1668-42e1-958e-a35620c385ae
---
# IDBCreateCommandImpl Class

Provides an implementation of the [IDBCreateCommand](https://docs.microsoft.com/previous-versions/windows/desktop/ms711625(v=vs.85)) interface.

## Syntax

```cpp
template <class T, class CommandClass >
class ATL_NO_VTABLE IDBCreateCommandImpl
   : public IDBCreateCommand
```

### Parameters

*T*<br/>
The session object derived from `IDBCreateCommandImpl`.

*CommandClass*<br/>
Your command class.

## Requirements

**Header:** atldb.h

## Members

### Interface Methods

|||
|-|-|
|[CreateCommand](#createcommand)|Creates a new command.|

## Remarks

An optional interface on the session object to obtain a new command.

## <a name="createcommand"></a> IDBCreateCommandImpl::CreateCommand

Creates a new command and returns the requested interface.

### Syntax

```cpp
STDMETHOD(CreateCommand)(IUnknown * pUnkOuter,
   REFIID riid,
   IUnknown ** ppvCommand);
```

#### Parameters

See [IDBCreateCommand::CreateCommand](https://docs.microsoft.com/previous-versions/windows/desktop/ms709772(v=vs.85)) in the *OLE DB Programmer's Reference*.

Some parameters correspond to *OLE DB Programmer's Reference* parameters of different names, which are described in `IDBCreateCommand::CreateCommand`:

|OLE DB Template parameters|*OLE DB Programmer's Reference* parameters|
|--------------------------------|------------------------------------------------|
|*ppvCommand*|*ppCommand*|

## See Also

[OLE DB Provider Templates](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[OLE DB Provider Template Architecture](../../data/oledb/ole-db-provider-template-architecture.md)