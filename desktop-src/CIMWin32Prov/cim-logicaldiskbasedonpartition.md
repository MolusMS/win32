---
Description: The CIM\_LogicalDiskBasedOnPartition class associates a logical disk with the disk partition on which it resides.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.prod: windows-server-dev
ms.technology:
- cimwin32
- windows-management-instrumentation
ms.tgt_platform: multiple
title: CIM\_LogicalDiskBasedOnPartition class
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# CIM\_LogicalDiskBasedOnPartition class

The **CIM\_LogicalDiskBasedOnPartition** class associates a logical disk with the disk partition on which it resides.

For example, a computer's drive C can be located on a partition on local physical media, which dictates that a logical disk cannot span more than one partition. When a logical disk can span more than one partition, however, the logical disk is based on RAID configuration (for example, a mirror or stripe set). In which case, the logical disk is based on storage volume. To prevent using the **CIM\_LogicalDiskBasedOnPartition** association incorrectly, the **Max(1)** qualifier was put on the **Antecedent** reference to the disk partition.

> \[!Important\]  
> The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built. WMI currently supports only the [CIM 2.x version schemas](Http://Go.Microsoft.Com/FWLink/p/?LinkID=309367).

 

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties. Properties are listed in alphabetic order, not MOF order.

## Syntax

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## Members

The **CIM\_LogicalDiskBasedOnPartition** class has these types of members:

-   [Properties](#properties)

### Properties

The **CIM\_LogicalDiskBasedOnPartition** class has these properties.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Data type: **CIM\_DiskPartition**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Override**](https://msdn.microsoft.com/library/aa393650) ("Antecedent"), [**Max**](https://msdn.microsoft.com/library/aa393650) (1)
</dt> </dl>

A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Data type: **CIM\_LogicalDisk**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Override**](https://msdn.microsoft.com/library/aa393650) ("Dependent")
</dt> </dl>

A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the partition.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Data type: **uint64**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Indicates the end of the high-level extent in lower-level storage. This property is useful when mapping non-contiguous extents into a higher-level grouping.

For more information about using **uint64** values in scripts, see [Scripting in WMI](https://msdn.microsoft.com/library/aa389763).

This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Data type: **uint64**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Indicates the beginning of the high-level extent in lower-level storage.

For more information about using **uint64** values in scripts, see [Scripting in WMI](https://msdn.microsoft.com/library/aa389763).

This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).

</dd> </dl>

## Remarks

The **CIM\_LogicalDiskBasedOnPartition** class is derived from [**CIM\_BasedOn**](cim-basedon.md).

WMI does not implement this class. For classes derived from **CIM\_LogicalDiskBasedOnPartition**, see [Win32 Classes](win32-provider.md).

This documentation is derived from the CIM class descriptions published by the DMTF. Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## See also

<dl> <dt>

[**CIM\_BasedOn**](cim-basedon.md)
</dt> </dl>

 

 



