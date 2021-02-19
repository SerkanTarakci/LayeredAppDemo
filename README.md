# LayeredAppDemo
This is a demo project created using layered architecture that I made for learning purposes. With this application, you can simulate the operations like searching products by name or category and adding, deleting, updating products.
## Introduction
* This is a simple **Windows Forms** application. **Northwind** database for **SQL Server** is being used.
* **Entity Framework** is being used.
* There are **Business**, **DataAccess**, **Entities** and **WebFormsUI** layers.
## Insallation & Usage
* Northwind database query can be accessed via [this link](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs).
* **EntityFramework.6.2.0** package was added to **Northwind.DataAccess** and **Northwind.WebFormsUI** layers via **NuGet Package Manager**.
* **FluentValidation** package was added to **Northwind.Business** layer via **NuGet Package Manager**.
* **Ninject** package was added to **Northwind.Business** layer via **NuGet Package Manager**.
* Set Northwind.WebFormsUI Startup Project.
## Layers
🗃 Northwind.Business

    📂 Abstract
         📃 ICategoryService.cs
         📃 IProductService.cs
         
    📂 Concrete
         📃 CategoryManager.cs
         📃 ProductManager.cs
         
    📂 DependencyResolvers
       📂 Ninject
            📃 BusinessModule.cs
            📃 InstanceModule.cs
            
    📂 Utilities
         📃 ValidationTool.cs
         
    📂 ValidationRules
       📂 FluentValidation
            📃 ProductValidator.cs         
            
🗃 Northwind.DataAccess

    📂 Abstract
         📃 ICategoryDal.cs
         📃 IEntityRepository.cs
         📃 IProductDal.cs

    📂 Concrete
       📂 EntityFramework
            📃 EfCategoryDal.cs
            📃 EfEntityRepositoryBase.cs
            📃 EfProductDal.cs
            📃 NorthwindContext.cs
       📂 NHibernate
            📃 NhProductDal.cs

🗃 Northwind.Entities    

    📂 Abstract
         📃 IEntity.cs
         
    📂 Abstract
         📃 Category.cs
         📃 Product.cs

🗃 Northwind.WebFormsUI

    📃 Form1.cs
    📃 Program.cs

## Output

![](https://cdn-images-1.medium.com/max/1200/1*9O2yDoMNel2g24HKCgok6A.png)





