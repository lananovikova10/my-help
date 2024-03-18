# Flowcart

Start typing here...

```mermaid
graph TD;
    A[初始化] --> B{是否初始化成功?}
    B -->|是| C[准备关机]
    B -->|否| D[清除缓存]
    D --> A
```