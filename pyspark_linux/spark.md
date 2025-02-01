# SparkSession vs SparkContext

| Característica                | SparkContext                                          | SparkSession                                        |
|-------------------------------|-------------------------------------------------------|-----------------------------------------------------|
| **Objetivo**                  | Conectar-se ao cluster e gerenciar execução de tarefas | Abstração unificada para trabalhar com dados estruturados (DataFrames, SQL, etc.) |
| **Abstração de Dados**        | RDDs (Resilient Distributed Datasets)                 | DataFrames, Datasets e RDDs                         |
| **Interação SQL**             | Não possui suporte direto para SQL                    | Suporta SQL diretamente via `spark.sql()`           |
| **Funções**                   | Mais baixo nível, precisa de configuração manual      | Abstração mais simples e moderna                    |
| **Integração com Hive**       | Não diretamente                                       | Suporta integrações com Hive e dados estruturados   |
| **Instância**                 | `sc` ou `SparkContext`                                | `spark` ou `SparkSession`                           |

---

# When to Use Checkpoints

- **Fault Tolerance**: If your job is long-running or involves multiple stages, checkpointing helps you recover from failures by providing a saved state.
- **Iterative Algorithms**: If you're using algorithms that involve multiple iterations (such as in machine learning models like PageRank), checkpointing can avoid recomputing the data in each iteration, improving performance.
- **Long Pipelines**: In some cases, complex data processing pipelines can benefit from checkpointing to optimize execution.

---

# Differences Between `cache()` and `checkpoint()`

| Feature                       | `cache()`                                             | `checkpoint()`                                      |
|-------------------------------|-------------------------------------------------------|-----------------------------------------------------|
| **Storage Location**          | Persists data in memory                               | Saves data to stable storage (e.g., HDFS, S3)       |
| **Recovery**                  | Does not help if the node fails                       | Allows recovery in case of failure                  |
| **Performance**               | Faster since data is stored in memory                 | Slower due to disk I/O                              |
| **Use Case**                  | Reusing data within the same job                      | Long-running jobs or fault tolerance scenarios      |