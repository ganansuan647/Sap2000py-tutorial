Saproject 类
================

Saproject 类是一个用于与 SAP2000 程序交互的 Python 类。它封装了 SAP2000 的 API，使得用户可以方便地创建、操作和分析 SAP2000 项目。

类定义
-------

.. autoclass:: Saproject
   :members:
   :undoc-members:
   :show-inheritance:

SapScripts 子类
---------------

Saproject 类还包含一个子类 SapScripts，用于执行一些预先定义的方便工程师和研究者的批量脚本操作，所有这些操作都可以通过Saproject内的其他函数完成。

.. autoclass:: SapScripts
   :members:
   :undoc-members:
   :show-inheritance:

示例代码
---------

以下是一个使用 Saproject 类的示例代码：

.. code-block:: python

    from pathlib import Path
    from Saproject import Saproject

    Sap = Saproject()
    Sap.openSap()
    Sap.File.New_Blank()
    Sap.File.Open(Path('.')/"Test"/"Test.sdb")
    
    print(Sap.Units)
    Sap.getUnits()
    
    print(Sap.SapVersion)
    Sap.getSapVersion()
    
    Sap.setProjectInfo(field="Company Name",value="Tongji University")
    Sap.setProjectInfo("Author","Gou Lingyun")
    Sap.setProjectInfo("Email","gulangyu@tongji.edu.cn")
    print(Sap.ProjectInfo)
    Sap.getProjectInfo()
    
    print(Sap.FileName)
    Sap.getFileName()
    
    print(Sap.CoordSystem)
    Sap.getCoordSystem()
    # Test setUnits
    Sap.setUnits("KN_m_E")
    Sap.setUnits("KN_m_C")
