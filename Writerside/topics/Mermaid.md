# Mermaid

```mermaid
classDiagram
    IRepository~T~ <|-- IWarehouseRepository
    IWarehouseRepository <|-- WarehouseRepository: implements
    GenericRepository~T~ <|-- WarehouseRepository
    IRepository~T~ <|-- GenericRepository~T~: implements

    class GenericRepository~T~ {
        <<abstract>>
        #JobturaDbContext dbContext
        -ICachingService _cachingService
        -ILogger? _logger
    }
    class WarehouseRepository {
    }
    class IRepository~T~ {
        <<interface>>
        +GetByHashcodeAsync(string hashcode) Task~T?~
        +GetRangeAsync(int start, int limit) Task~List~T?~~
        +CreateAsync(T entity) Task
        +Task UpdateAsync(T entity) Task
        +DeleteAsync(string hashcode) Task
        +Search(Expression<Func&lt;T, bool&gt;> query) Task~List~T~~
    }
    class IWarehouseRepository {
        <<interface>>
    }

```

```mermaid
classDiagram
    IRepository <|-- IWarehouseRepository
    IWarehouseRepository <|-- WarehouseRepository: implements
    GenericRepository <|-- WarehouseRepository
    IRepository <|-- GenericRepository: implements

    class GenericRepository {
        <<abstract>>
        #JobturaDbContext dbContext
        -ICachingService _cachingService
        -ILogger? _logger
    }
    class WarehouseRepository {
    }
    class IRepository {
        <<interface>>
        +GetByHashcodeAsync(string hashcode) Task~T?~
        +GetRangeAsync(int start, int limit) Task~List~T?~~
        +CreateAsync(T entity) Task
        +Task UpdateAsync(T entity) Task
        +DeleteAsync(string hashcode) Task
        +Search(query: string) Task~List~T~~
    }
    class IWarehouseRepository {
        <<interface>>
    }


```

```
fff
```


